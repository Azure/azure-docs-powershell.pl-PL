# <a name="breaking-changes-for-microsoft-azure-powershell-300"></a>Istotne zmiany dotyczące programu Microsoft Azure PowerShell 3.0.0.

Ten dokument służy jako przewodnik zarówno po powiadomieniach o istotnych zmianach, jak i migracji dla użytkowników poleceń cmdlet programu Microsoft Azure PowerShell.  Każda sekcja opisuje zarówno tempo istotnej zmiany, jak i ścieżkę migracji najmniejszego oporu.  Aby uzyskać szczegółowy kontekst, zapoznaj się z żądaniem ściągnięcia skojarzonym z każdą zmianą.

## <a name="table-of-contents"></a>Spis treści
1. [Istotne zmiany w poleceniach cmdlet usługi Data Lake Store](#breaking-changes-to-data-lake-store-cmdlets)
2. [Istotne zmiany w poleceniach cmdlet usługi ApiManagement](#breaking-changes-to-apimanagement-cmdlets)
3. [Istotne zmiany w poleceniach cmdlet usługi Network](#breaking-changes-to-network-cmdlets)

## <a name="breaking-changes-to-data-lake-store-cmdlets"></a>Istotne zmiany w poleceniach cmdlet usługi Data Lake Store

Następujące polecenia cmdlet miały wpływ na tę wersję ([PR 2965](https://github.com/Azure/azure-powershell/pull/2965)):

**Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)**
- To polecenie cmdlet zostało usunięte i zastąpione przez ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)``.
- Stare polecenie cmdlet zwracało obiekt złożony reprezentujący listę kontroli dostępu (ACL). Nowe polecenie cmdlet zwraca prostą listę wpisów w liście ACL wybranej ścieżki.

```powershell
# Old
Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo

# New
Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
```

**Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)**
- To polecenie cmdlet zastępuje stare polecenie cmdlet ``Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)``.
- To nowe polecenie cmdlet zwraca prostą listę wpisów w liście ACL wybranej ścieżki o typie ``DataLakeStoreItemAce[]``.
- Dane wyjściowe tego polecenia cmdlet mogą być przekazane do parametru ``-Acl`` następujących poleceń cmdlet:
   - ``Remove-AzureRmDataLakeStoreItemAcl``
   - ``Set-AzureRmDataLakeStoreItemAcl``
   - ``Set-AzureRmDataLakeStoreItemAclEntry``

```powershell
# Old
Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo

# New
Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
```

**Remove-AzureRmDataLakeStoreItemAcl (Remove-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAcl (Set-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAclEntry (Set-AdlStoreItemAclEntry)**
- Te polecenia cmdlet obecnie akceptują typ ``DataLakeStoreItemAce[]`` dla parametru ``-Acl``.
- Typ ``DataLakeStoreItemAce[]`` jest zwracany przez polecenie ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)``.

```powershell
# Old
$acl = Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo
Set-AdlStoreItemAcl -Account myadlsaccount -Path /foo -Acl $acl

# New
$aclEntries = Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
Set-AdlStoreItemAcl -Account myadlsaccount -Path /foo -Acl $aclEntries
```

## <a name="breaking-changes-to-apimanagement-cmdlets"></a>Istotne zmiany w poleceniach cmdlet usługi ApiManagement

Następujące polecenia cmdlet miały wpływ na tę wersję ([PR 2971](https://github.com/Azure/azure-powershell/pull/2971)):

**New-AzureRmApiManagementVirtualNetwork**
- Wymagane parametry na potrzeby odwołania do sieci wirtualnej zostały zmienione z SubnetName i VnetId na wymaganie parametru SubnetResourceId w formacie ``/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ClassicNetwork/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}``

```powershell
# Old
$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetName <String> -VnetId <Guid>

# New
$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>

```

**Wycofano polecenie cmdlet Set-AzureRmApiManagementVirtualNetworks**
- Polecenie cmdlet jest wycofywane, ponieważ istniał więcej niż jeden sposób ustawienia sieci wirtualnej skojarzony z wdrożeniem operacji ApiManagement.

```powershell
# Old
$networksList = @()
$networksList += New-AzureRmApiManagementVirtualNetwork -Location $vnetLocation -VnetId $vnetId -SubnetName $subnetName
Set-AzureRmApiManagementVirtualNetworks -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetworks $networksList

# New
$masterRegionVirtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $masterRegionVirtualNetwork
```

## <a name="breaking-changes-to-network-cmdlets"></a>Istotne zmiany w poleceniach cmdlet usługi Network

Następujące polecenia cmdlet miały wpływ na tę wersję ([PR 2982](https://github.com/Azure/azure-powershell/pull/2982)):

**New-AzureRmVirtualNetworkGateway**
- Opis zmian ``:- Bool parameter:-ActiveActive`` został usunięty i dodano ``SwitchParameter:-EnableActiveActiveFeature`` na potrzeby włączania funkcji Active-Active w nowo tworzonej bramie sieci wirtualnej.

```powershell
# Old 
# Sample of how the cmdlet was previously called
New-AzureRmVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -Location $location -IpConfigurations $vnetIpConfig1,$vnetIpConfig2 -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku HighPerformance -ActiveActive $true

# New
# Sample of how the cmdlet should now be called
New-AzureRmVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -Location $location -IpConfigurations $vnetIpConfig1,$vnetIpConfig2 -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku HighPerformance -EnableActiveActiveFeature
```

Set-AzureRmVirtualNetworkGateway
- Opis zmian ``:- Bool parameter:-ActiveActive`` został usunięty i dodano 2 ``SwitchParameters:-EnableActiveActiveFeature`` / ``DisableActiveActiveFeature`` na potrzeby włączania i wyłączania funkcji Active-Active w bramie sieci wirtualnej.

```powershell
# Old
# Sample of how the cmdlet was previously called
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $gw -ActiveActive $true
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $gw -ActiveActive $false  

# New
# Sample of how the cmdlet should now be called
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $gw -EnableActiveActiveFeature
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $gw -DisableActiveActiveFeature
```