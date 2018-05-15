# <a name="breaking-changes-for-microsoft-azure-powershell-300"></a><span data-ttu-id="9dd66-101">Istotne zmiany dotyczące programu Microsoft Azure PowerShell 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="9dd66-101">Breaking changes for Microsoft Azure PowerShell 3.0.0.</span></span>

<span data-ttu-id="9dd66-102">Ten dokument służy jako przewodnik zarówno po powiadomieniach o istotnych zmianach, jak i migracji dla użytkowników poleceń cmdlet programu Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9dd66-102">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span>  <span data-ttu-id="9dd66-103">Każda sekcja opisuje zarówno tempo istotnej zmiany, jak i ścieżkę migracji najmniejszego oporu.</span><span class="sxs-lookup"><span data-stu-id="9dd66-103">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span>  <span data-ttu-id="9dd66-104">Aby uzyskać szczegółowy kontekst, zapoznaj się z żądaniem ściągnięcia skojarzonym z każdą zmianą.</span><span class="sxs-lookup"><span data-stu-id="9dd66-104">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="9dd66-105">Spis treści</span><span class="sxs-lookup"><span data-stu-id="9dd66-105">Table of Contents</span></span>
1. [<span data-ttu-id="9dd66-106">Istotne zmiany w poleceniach cmdlet usługi Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="9dd66-106">Breaking changes to Data Lake Store cmdlets</span></span>](#breaking-changes-to-data-lake-store-cmdlets)
2. [<span data-ttu-id="9dd66-107">Istotne zmiany w poleceniach cmdlet usługi ApiManagement</span><span class="sxs-lookup"><span data-stu-id="9dd66-107">Breaking changes to ApiManagement cmdlets</span></span>](#breaking-changes-to-apimanagement-cmdlets)
3. [<span data-ttu-id="9dd66-108">Istotne zmiany w poleceniach cmdlet usługi Network</span><span class="sxs-lookup"><span data-stu-id="9dd66-108">Breaking changes to Network cmdlets</span></span>](#breaking-changes-to-network-cmdlets)

## <a name="breaking-changes-to-data-lake-store-cmdlets"></a><span data-ttu-id="9dd66-109">Istotne zmiany w poleceniach cmdlet usługi Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="9dd66-109">Breaking changes to Data Lake Store cmdlets</span></span>

<span data-ttu-id="9dd66-110">Następujące polecenia cmdlet miały wpływ na tę wersję ([PR 2965](https://github.com/Azure/azure-powershell/pull/2965)):</span><span class="sxs-lookup"><span data-stu-id="9dd66-110">The following cmdlets were affected this release ([PR 2965](https://github.com/Azure/azure-powershell/pull/2965)):</span></span>

<span data-ttu-id="9dd66-111">**Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)**</span><span class="sxs-lookup"><span data-stu-id="9dd66-111">**Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)**</span></span>
- <span data-ttu-id="9dd66-112">To polecenie cmdlet zostało usunięte i zastąpione przez ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)``.</span><span class="sxs-lookup"><span data-stu-id="9dd66-112">This cmdlet was removed and replaced with ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)``.</span></span>
- <span data-ttu-id="9dd66-113">Stare polecenie cmdlet zwracało obiekt złożony reprezentujący listę kontroli dostępu (ACL).</span><span class="sxs-lookup"><span data-stu-id="9dd66-113">The old cmdlet returned a complex object representing the access control list (ACL).</span></span> <span data-ttu-id="9dd66-114">Nowe polecenie cmdlet zwraca prostą listę wpisów w liście ACL wybranej ścieżki.</span><span class="sxs-lookup"><span data-stu-id="9dd66-114">The new cmdlet returns a simple list of entries in the chosen path's ACL.</span></span>

```powershell
# Old
Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo

# New
Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
```

<span data-ttu-id="9dd66-115">**Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)**</span><span class="sxs-lookup"><span data-stu-id="9dd66-115">**Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)**</span></span>
- <span data-ttu-id="9dd66-116">To polecenie cmdlet zastępuje stare polecenie cmdlet ``Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)``.</span><span class="sxs-lookup"><span data-stu-id="9dd66-116">This cmdlet replaces the old cmdlet ``Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)``.</span></span>
- <span data-ttu-id="9dd66-117">To nowe polecenie cmdlet zwraca prostą listę wpisów w liście ACL wybranej ścieżki o typie ``DataLakeStoreItemAce[]``.</span><span class="sxs-lookup"><span data-stu-id="9dd66-117">This new cmdlet returns a simple list of entries in the chosen path's ACL, with type ``DataLakeStoreItemAce[]``.</span></span>
- <span data-ttu-id="9dd66-118">Dane wyjściowe tego polecenia cmdlet mogą być przekazane do parametru ``-Acl`` następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="9dd66-118">The output of this cmdlet can be passed in to the ``-Acl`` parameter of the following cmdlets:</span></span>
   - ``Remove-AzureRmDataLakeStoreItemAcl``
   - ``Set-AzureRmDataLakeStoreItemAcl``
   - ``Set-AzureRmDataLakeStoreItemAclEntry``

```powershell
# Old
Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo

# New
Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
```

<span data-ttu-id="9dd66-119">**Remove-AzureRmDataLakeStoreItemAcl (Remove-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAcl (Set-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAclEntry (Set-AdlStoreItemAclEntry)**</span><span class="sxs-lookup"><span data-stu-id="9dd66-119">**Remove-AzureRmDataLakeStoreItemAcl (Remove-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAcl (Set-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAclEntry (Set-AdlStoreItemAclEntry)**</span></span>
- <span data-ttu-id="9dd66-120">Te polecenia cmdlet obecnie akceptują typ ``DataLakeStoreItemAce[]`` dla parametru ``-Acl``.</span><span class="sxs-lookup"><span data-stu-id="9dd66-120">These cmdlets now accept ``DataLakeStoreItemAce[]`` for the ``-Acl`` parameter.</span></span>
- <span data-ttu-id="9dd66-121">Typ ``DataLakeStoreItemAce[]`` jest zwracany przez polecenie ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)``.</span><span class="sxs-lookup"><span data-stu-id="9dd66-121">``DataLakeStoreItemAce[]`` is returned by ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)``.</span></span>

```powershell
# Old
$acl = Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo
Set-AdlStoreItemAcl -Account myadlsaccount -Path /foo -Acl $acl

# New
$aclEntries = Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
Set-AdlStoreItemAcl -Account myadlsaccount -Path /foo -Acl $aclEntries
```

## <a name="breaking-changes-to-apimanagement-cmdlets"></a><span data-ttu-id="9dd66-122">Istotne zmiany w poleceniach cmdlet usługi ApiManagement</span><span class="sxs-lookup"><span data-stu-id="9dd66-122">Breaking changes to ApiManagement cmdlets</span></span>

<span data-ttu-id="9dd66-123">Następujące polecenia cmdlet miały wpływ na tę wersję ([PR 2971](https://github.com/Azure/azure-powershell/pull/2971)):</span><span class="sxs-lookup"><span data-stu-id="9dd66-123">The following cmdlets were affected this release ([PR 2971](https://github.com/Azure/azure-powershell/pull/2971)):</span></span>

<span data-ttu-id="9dd66-124">**New-AzureRmApiManagementVirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="9dd66-124">**New-AzureRmApiManagementVirtualNetwork**</span></span>
- <span data-ttu-id="9dd66-125">Wymagane parametry na potrzeby odwołania do sieci wirtualnej zostały zmienione z SubnetName i VnetId na wymaganie parametru SubnetResourceId w formacie ``/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ClassicNetwork/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}``</span><span class="sxs-lookup"><span data-stu-id="9dd66-125">The required parameters to reference a virtual network changed from requiring SubnetName and VnetId to SubnetResourceId in format ``/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ClassicNetwork/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}``</span></span>

```powershell
# Old
$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetName <String> -VnetId <Guid>

# New
$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>

```

<span data-ttu-id="9dd66-126">**Wycofano polecenie cmdlet Set-AzureRmApiManagementVirtualNetworks**</span><span class="sxs-lookup"><span data-stu-id="9dd66-126">**Deprecating Cmdlet Set-AzureRmApiManagementVirtualNetworks**</span></span>
- <span data-ttu-id="9dd66-127">Polecenie cmdlet jest wycofywane, ponieważ istniał więcej niż jeden sposób ustawienia sieci wirtualnej skojarzony z wdrożeniem operacji ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="9dd66-127">The Cmdlet is getting deprecated as there was more than one way to Set Virtual Network associated to ApiManagement deployment.</span></span>

```powershell
# Old
$networksList = @()
$networksList += New-AzureRmApiManagementVirtualNetwork -Location $vnetLocation -VnetId $vnetId -SubnetName $subnetName
Set-AzureRmApiManagementVirtualNetworks -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetworks $networksList

# New
$masterRegionVirtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $masterRegionVirtualNetwork
```

## <a name="breaking-changes-to-network-cmdlets"></a><span data-ttu-id="9dd66-128">Istotne zmiany w poleceniach cmdlet usługi Network</span><span class="sxs-lookup"><span data-stu-id="9dd66-128">Breaking changes to Network cmdlets</span></span>

<span data-ttu-id="9dd66-129">Następujące polecenia cmdlet miały wpływ na tę wersję ([PR 2982](https://github.com/Azure/azure-powershell/pull/2982)):</span><span class="sxs-lookup"><span data-stu-id="9dd66-129">The following cmdlets were affected this release ([PR 2982](https://github.com/Azure/azure-powershell/pull/2982)):</span></span>

<span data-ttu-id="9dd66-130">**New-AzureRmVirtualNetworkGateway**</span><span class="sxs-lookup"><span data-stu-id="9dd66-130">**New-AzureRmVirtualNetworkGateway**</span></span>
- <span data-ttu-id="9dd66-131">Opis zmian ``:- Bool parameter:-ActiveActive`` został usunięty i dodano ``SwitchParameter:-EnableActiveActiveFeature`` na potrzeby włączania funkcji Active-Active w nowo tworzonej bramie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9dd66-131">Description of what has changed ``:- Bool parameter:-ActiveActive`` is removed and ``SwitchParameter:-EnableActiveActiveFeature`` is added for enabling Active-Active feature on newly creating virtual network gateway.</span></span>

```powershell
# Old 
# Sample of how the cmdlet was previously called
New-AzureRmVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -Location $location -IpConfigurations $vnetIpConfig1,$vnetIpConfig2 -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku HighPerformance -ActiveActive $true

# New
# Sample of how the cmdlet should now be called
New-AzureRmVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -Location $location -IpConfigurations $vnetIpConfig1,$vnetIpConfig2 -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku HighPerformance -EnableActiveActiveFeature
```

<span data-ttu-id="9dd66-132">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9dd66-132">Set-AzureRmVirtualNetworkGateway</span></span>
- <span data-ttu-id="9dd66-133">Opis zmian ``:- Bool parameter:-ActiveActive`` został usunięty i dodano 2 ``SwitchParameters:-EnableActiveActiveFeature`` / ``DisableActiveActiveFeature`` na potrzeby włączania i wyłączania funkcji Active-Active w bramie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9dd66-133">Description of what has changed ``:- Bool parameter:-ActiveActive`` is removed and 2 ``SwitchParameters:-EnableActiveActiveFeature`` / ``DisableActiveActiveFeature`` are added for enabling and disabling Active-Active feature on virtual network gateway.</span></span>

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