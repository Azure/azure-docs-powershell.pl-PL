---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
ms.openlocfilehash: 4953e914cc52784cd815be80307babfe05f3b63c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177651"
---
# New-AzVmss

## SYNOPSIS
Tworzy maszyny wirtualne.

## SKŁADNIA

### DefaultParameters (domyślne)
```
New-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SimpleParameterSet
```
New-AzVmss [[-ResourceGroupName] <String>] [-VMScaleSetName] <String> [-AsJob] [-ImageName <String>]
 -Credential <PSCredential> [-InstanceCount <Int32>] [-VirtualNetworkName <String>] [-SubnetName <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-SecurityGroupName <String>]
 [-LoadBalancerName <String>] [-BackendPort <Int32[]>] [-Location <String>] [-VmSize <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-AllocationMethod <String>] [-VnetAddressPrefix <String>]
 [-SubnetAddressPrefix <String>] [-FrontendPoolName <String>] [-BackendPoolName <String>]
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-EnableUltraSSD]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-NatBackendPort <Int32[]>]
 [-DataDiskSizeInGb <Int32[]>] [-ProximityPlacementGroupId <String>] [-HostGroupId <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-ScaleInPolicy <String[]>]
 [-SkipExtensionsOnOverprovisionedVMs] [-EncryptionAtHost] [-PlatformFaultDomainCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-SinglePlacementGroup] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet New-AzVmss** tworzy na platformie Azure zestaw skal maszyn wirtualnych (VIRTUAL Machine Scale Set).
Użyj prostego zestawu parametrów () w celu szybkiego utworzenia wstępnie ustawionej maszyny `SimpleParameterSet` wirtualnej i skojarzonych zasobów. Użyj domyślnego zestawu parametrów () w bardziej zaawansowanych scenariuszach, gdy musisz dokładnie skonfigurować każdy składnik usługi VMSS i każdego skojarzonego zasobu przed `DefaultParameter` utworzeniem.

## PRZYKŁADY

### Przykład 1. Tworzenie maszyny wirtualnej przy użyciu **`SimpleParameterSet`**
```powershell
$vmssName = <VMSSNAME>
# Create credentials, I am using one way to create credentials, there are others as well. 
# Pick one that makes the most sense according to your use case.
$vmPassword = ConvertTo-SecureString <PASSWORD_HERE> -AsPlainText -Force
$vmCred = New-Object System.Management.Automation.PSCredential(<USERNAME_HERE>, $vmPassword)

#Create a VMSS using the default settings
New-AzVmss -Credential $vmCred -VMScaleSetName $vmssName
```

Powyższe polecenie tworzy następujące polecenie o `$vmssName` nazwie:
* Grupa zasobów
* Sieć wirtualna
* Równoważenie obciążenia
* Publiczny adres IP
* maszyny wirtualnej z 2 wystąpieniami

Domyślny obraz wybrany dla maszyn wirtualnych w maszyny wirtualnej jest, `2016-Datacenter Windows Server` a wersja SKU to `Standard_DS1_v2`

### Przykład 2. Tworzenie maszyny wirtualnej przy użyciu **`DefaultParameterSet`**
```powershell
# Common
$LOC = "WestUs";
$RGName = "rgkyvms";

New-AzResourceGroup -Name $RGName -Location $LOC -Force;

# SRP
$STOName = "STO" + $RGName;
$STOType = "Standard_GRS";
New-AzStorageAccount -ResourceGroupName $RGName -Name $STOName -Location $LOC -Type $STOType;
$STOAccount = Get-AzStorageAccount -ResourceGroupName $RGName -Name $STOName; 

# NRP
$SubNet = New-AzVirtualNetworkSubnetConfig -Name ("subnet" + $RGName) -AddressPrefix "10.0.0.0/24";
$VNet = New-AzVirtualNetwork -Force -Name ("vnet" + $RGName) -ResourceGroupName $RGName -Location $LOC -AddressPrefix "10.0.0.0/16" -DnsServer "10.1.1.1" -Subnet $SubNet;
$VNet = Get-AzVirtualNetwork -Name ('vnet' + $RGName) -ResourceGroupName $RGName;
$SubNetId = $VNet.Subnets[0].Id;

$PubIP = New-AzPublicIpAddress -Force -Name ("PubIP" + $RGName) -ResourceGroupName $RGName -Location $LOC -AllocationMethod Dynamic -DomainNameLabel ("PubIP" + $RGName);
$PubIP = Get-AzPublicIpAddress -Name ("PubIP"  + $RGName) -ResourceGroupName $RGName;

# Create LoadBalancer
$FrontendName = "fe" + $RGName
$BackendAddressPoolName = "bepool" + $RGName
$ProbeName = "vmssprobe" + $RGName
$InboundNatPoolName  = "innatpool" + $RGName
$LBRuleName = "lbrule" + $RGName
$LBName = "vmsslb" + $RGName

$Frontend = New-AzLoadBalancerFrontendIpConfig -Name $FrontendName -PublicIpAddress $PubIP
$BackendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name $BackendAddressPoolName
$Probe = New-AzLoadBalancerProbeConfig -Name $ProbeName -RequestPath healthcheck.aspx -Protocol http -Port 80 -IntervalInSeconds 15 -ProbeCount 2
$InboundNatPool = New-AzLoadBalancerInboundNatPoolConfig -Name $InboundNatPoolName  -FrontendIPConfigurationId `
    $Frontend.Id -Protocol Tcp -FrontendPortRangeStart 3360 -FrontendPortRangeEnd 3362 -BackendPort 3370;
$LBRule = New-AzLoadBalancerRuleConfig -Name $LBRuleName `
    -FrontendIPConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -Protocol Tcp -FrontendPort 80 -BackendPort 80 `
    -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP;
$ActualLb = New-AzLoadBalancer -Name $LBName -ResourceGroupName $RGName -Location $LOC `
    -FrontendIpConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -LoadBalancingRule $LBRule -InboundNatPool $InboundNatPool;
$ExpectedLb = Get-AzLoadBalancer -Name $LBName -ResourceGroupName $RGName

# New VMSS Parameters
$VMSSName = "VMSS" + $RGName;

$AdminUsername = "Admin01";
$AdminPassword = "p4ssw0rd@123" + $RGName;

$PublisherName = "MicrosoftWindowsServer" 
$Offer         = "WindowsServer" 
$Sku           = "2012-R2-Datacenter" 
$Version       = "latest"
        
$VHDContainer = "https://" + $STOName + ".blob.core.contoso.net/" + $VMSSName;

$ExtName = "CSETest";
$Publisher = "Microsoft.Compute";
$ExtType = "BGInfo";
$ExtVer = "2.1";

#IP Config for the NIC
$IPCfg = New-AzVmssIPConfig -Name "Test" `
    -LoadBalancerInboundNatPoolsId $ExpectedLb.InboundNatPools[0].Id `
    -LoadBalancerBackendAddressPoolsId $ExpectedLb.BackendAddressPools[0].Id `
    -SubnetId $SubNetId;
            
#VMSS Config
$VMSS = New-AzVmssConfig -Location $LOC -SkuCapacity 2 -SkuName "Standard_E4-2ds_v4" -UpgradePolicyMode "Automatic" `
    | Add-AzVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
    | Add-AzVmssNetworkInterfaceConfiguration -Name "Test2"  -IPConfiguration $IPCfg `
    | Set-AzVmssOSProfile -ComputerNamePrefix "Test"  -AdminUsername $AdminUsername -AdminPassword $AdminPassword `
    | Set-AzVmssStorageProfile -Name "Test"  -OsDiskCreateOption 'FromImage' -OsDiskCaching "None" `
    -ImageReferenceOffer $Offer -ImageReferenceSku $Sku -ImageReferenceVersion $Version `
    -ImageReferencePublisher $PublisherName -VhdContainer $VHDContainer `
    | Add-AzVmssExtension -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True

#Create the VMSS
New-AzVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

W powyższym złożonym przykładzie jest powodna maszyny wirtualnej. Poniżej przedstawiono wyjaśnienie tego, co się dzieje:
* Pierwsze polecenie tworzy grupę zasobów o określonej nazwie i lokalizacji.
* Drugie polecenie tworzy konto magazynu za pomocą polecenia cmdlet **New-AzStorageAccount.**
* Trzecie polecenie użyje następnie polecenia cmdlet **Get-AzStorageAccount** w celu uzyskania konta magazynu utworzonego w drugim poleceniu i przechowuje wynik w $STOAccount danych.
* Piąte polecenie używa polecenia cmdlet **New-AzVirtualNetworkSubnetConfig** do utworzenia podsieci i przechowuje wynik w zmiennej o nazwie $SubNet.
* Szóste polecenie używa polecenia cmdlet **New-AzVirtualNetwork** do utworzenia sieci wirtualnej i zapisuje wynik w zmiennej o nazwie $VNet.
* Siódme polecenie korzysta z polecenia **Get-AzVirtualNetwork** w celu uzyskania informacji o sieci wirtualnej utworzonej w szóstym poleceniu i przechowuje informacje w zmiennej o nazwie $VNet.
* W ósmym i dziewiątym poleceniu są używane polecenia **New-AzPublicIpAddress** i **Get- AzureRmPublicIpAddress** w celu utworzenia i uzyskania informacji z tego publicznego adresu IP.
* Polecenia przechowują informacje w zmiennej o nazwie $PubIP.
* Dziesiąte polecenie używa polecenia cmdlet **New- AzureRmLoadBalancerFrontendIpConfig** w celu utworzenia narzędzia do równoważenia obciążenia frontendu i przechowuje wynik w zmiennej o nazwie $Frontend.
* Polecenie jedenaste używa polecenia **New-AzLoadBalancerBackendAddressPoolConfig** w celu utworzenia konfiguracji puli adresów zaplecza i przechowuje wynik w zmiennej o nazwie $BackendAddressPool.
* 10. polecenie używa polecenia **New-AzLoadBalancerProbeConfig** w celu utworzenia agory i przechowuje informacje o tym pliku w zmiennej o nazwie $Probe.
* Trzynaste polecenie używa polecenia cmdlet **New-AzLoadBalancerInboundNatPoolConfig** w celu utworzenia konfiguracji puli translacji przychodzącego adresu sieciowego (NAT, load balancer).
* Polecenie czternaste używa polecenia **New-AzLoadBalancerRuleConfig** w celu utworzenia konfiguracji reguły równoważenia obciążenia i przechowuje wynik w zmiennej o nazwie $LBRule.
* To polecenie używa polecenia cmdlet **New-AzLoadBalancer** w celu utworzenia równoważenia obciążenia i zapisuje wynik w zmiennej o nazwie $ActualLb.
* Polecenie **Get-AzLoadBalancer używa polecenia Get-AzLoadBalancer** w celu uzyskania informacji o równoważeniu obciążenia, które zostało utworzone w piętnastym poleceniu i przechowuje informacje w zmiennej o nazwie $ExpectedLb.
* Polecenie w programie **New-AzVmssIPConfig używa polecenia cmdlet New-AzVmssIPConfig** do utworzenia konfiguracji ip usługi VMSS i przechowuje informacje w zmiennej o nazwie $IPCfg.
* W osiemnastym poleceniu jest używane polecenie cmdlet **New-AzVmssConfig** w celu utworzenia obiektu konfiguracji maszyny WIRTUALNEJ i zapisuje wynik w zmiennej o nazwie $VMSS.
* Polecenie tego typu używa polecenia cmdlet **New-AzVmss w** celu utworzenia maszyny wirtualnej.

## PARAMETERS

### -AllocationMethod
Metoda alokacji dla publicznego adresu IP zestawu skali (statycznego lub dynamicznego).  Jeśli nie zostanie podany żadna wartość, alokacja będzie statyczna.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### — AsJob
Uruchom polecenie cmdlet w tle i zwróć zadanie w celu śledzenia postępu.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendPoolName
Nazwa puli adresów zaplecza do użycia w saldzie równoważenia obciążenia dla tego zestawu skali.  Jeśli nie podano żadnej wartości, zostanie utworzona nowa pula zaplecza o takiej samej nazwie jak zestaw skali.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendPort
Numery portów zaplecza używane przez równoważenie obciążenia przez zestaw skalowania do komunikowania się z maszynami maszyn wirtualnych w zestawie skali.  Jeśli nie określono żadnych wartości, porty 3389 i 5985 będą używane dla maszyn wirtualnych systemu Windows, a port 22 będzie używany dla maszyn wirtualnych systemu Linux.

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - Credential
Poświadczenia administratora (nazwa użytkownika i hasło) dla maszyn wirtualnych w tym zestawie skali.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: SimpleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DataSizeSizeInGb
Określa rozmiary dysków danych w GB.

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainNameLabel
Etykieta nazwy domeny dla publicznej Fully-Qualified domeny (FQDN) dla tego zestawu skali. Jest to pierwszy składnik nazwy domeny przypisywany automatycznie do zestawu skali. Automatycznie przypisane nazwy domen używają formularza ( <DomainNameLabel> <Location> . cloudapp.azure.com). Jeśli nie zostanie włączona żadna wartość, domyślną etykietą nazwy domeny będzie złączenie <ScaleSetName> <ResourceGroupName> oraz.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableUltrasSD
Użyj płyty ultrassd dla maszyn wirtualnych w zestawie skali.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EncryptionAtHost
Ten parametr umożliwia szyfrowanie dla wszystkich dysków dysków, w tym dysku zasobu/tempa na samym hoście. Domyślne: Szyfrowanie na hoście zostanie wyłączone, chyba że dla zasobu ta właściwość jest ustawiona na prawda.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EvictionPolicy
Zasady wywłasowania dla zestawu skali maszyny wirtualnej o niskim priorytecie.  Obsługiwane są tylko wartości "Deallocate" i "Delete".

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FrontendPoolName
Nazwa puli adresów frontendowych do użycia w zestawie skalowania równoważenia obciążenia.  Jeśli nie zostanie podany żadna wartość, zostanie utworzona nowa pula adresów frontendowych o takiej samej nazwie jak zestaw skali.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostGroupId
Określa dedykowaną grupę hosta, w którym będzie znajdować się zestaw skal maszyn wirtualnych.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: HostGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### -ImageName
Nazwa obrazu dla maszyn wirtualnych w tym zestawie skali. Jeśli nie podano żadnej wartości, zostanie użyty obraz "Windows Server 2016 DataCenter".

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstanceCount
Liczba obrazów maszyny wirtualnej w zestawie skali.  Jeśli nie podano żadnej wartości, zostaną utworzone 2 wystąpienia.

```yaml
Type: System.Int32
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False
```

### -LoadBalancerName
Nazwa równoważenia obciążenia do użycia z tym zestawem skal.  Jeśli nie zostanie określona żadna wartość, zostanie utworzone nowe równoważenie obciążenia o takiej samej nazwie jak zestaw skali.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Lokalizacja
Lokalizacja platformy Azure, w której zostanie utworzony ten zestaw skali.  Jeśli nie zostanie określona żadna wartość, lokalizacja zostanie wywłaszona na przykład z lokalizacji innych zasobów, do których odwołują się parametry.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - MaxCena
Maksymalna cena rozliczenia zestawu skal maszyn wirtualnych o niskim priorytecie.

```yaml
Type: System.Double
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NatBackendPort
Port zaplecza do translacji przychodzącego adresu sieciowego.

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PlatformFaultDomainCount
Liczba domen błędów dla każdej grupy położenia.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Priority (Priorytet)
Priorytet maszyny wirtualnej w zestawie skali.  Obsługiwane są tylko wartości "Zwykła", "Spot" i "Niska".
"Zwykła" jest dla zwykłej maszyny wirtualnej.
"Spot" jest dla maszyny wirtualnej spot.
"Low" jest również dla spot virtual machine, ale jest zastępowany przez "Spot". Użyj pozycji Spot (Spot) zamiast "Low" (Najniszej).

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProximityPlacementGroupId
Identyfikator zasobu grupy Położenie odległości do użycia z tym zestawem skali.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: ProximityPlacementGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIpAddressName
Nazwa publicznego adresu IP, który ma być podany w tym zestawie skali.  Jeśli nie podano żadnej wartości, zostanie utworzona nowa publiczna adres IPAddress o takiej samej nazwie jak zestaw skali.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów maszyn wirtualnych.  Jeśli nie zostanie określona żadna wartość, nowa grupa zasobów zostanie utworzona pod taką samą nazwą jak zestaw skali.

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ScaleInPolicy
Reguły, które mają być stosowane podczas skalowania w zestawie skalowania maszyny wirtualnej.  Dopuszczalne wartości to: "Domyślne", "NajstarszeVM" i "NajnowszeVM".  Ustawienie "Domyślne", gdy skala zestawu maszyn wirtualnych jest skalowana w, zestaw skali zostanie najpierw wyrównany w różnych strefach, jeśli jest to zestaw skali zonal.  Następnie zostanie on w możliwie najdalej sytą równowagi między domenami błędów.  W obrębie każdej domeny błędu maszyny wirtualne wybrane do usunięcia będą najnowszymi, które nie są chronione przez skalowanie.  Podczas skalowania zestawu skalowania dla maszyny wirtualnej najstarsze maszyny wirtualne, które nie są chronione przez skalowanie, zostaną wybrane do usunięcia.  W przypadku zestawów skali zonal virtual machine(zonal virtual machine) zestaw skal zostanie najpierw zrównoważony w różnych strefach.  W każdej strefie najstarsze komputery wirtualne, które nie są chronione, zostaną wybrane do usunięcia.  "Najnowsza wersja VM", gdy jest skalowany zestaw skalowania zestawu maszyn wirtualnych, najnowsze maszyny wirtualne, które nie są chronione przez skalowanie, zostaną wybrane do usunięcia.  W przypadku zestawów skali zonal virtual machine(zonal virtual machine) zestaw skal zostanie najpierw syrównowany w różnych strefach.  W każdej strefie do usunięcia zostaną wybrane najnowsze maszyny wirtualne, które nie są chronione.

```yaml
Type: System.String[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SecurityGroupName
Nazwa grupy zabezpieczeń sieci, która ma być stosowane do tego zestawu skali.  Jeśli nie podano żadnej wartości, domyślna grupa zabezpieczeń sieci o takiej samej nazwie jak zestaw skali zostanie utworzona i zastosowana do zestawu skali.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SinglePlacementGroup
Użyj tej opcji, aby utworzyć zestaw skal w jednej grupie położenia, wartością domyślną jest wiele grup

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipExtensionsOnOverprovisionedVMs
Określa, że rozszerzenia nie są uruchamiane na dodatkowych nadprowizowanych maszyn wirtualnych.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetAddressPrefix
Prefiks adresu podsieci, z których będzie korzystać ten zestaw skal. Domyślne ustawienia podsieci (192.168.1.0/24) zostaną zastosowane, jeśli nie podano żadnej wartości.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetName
Nazwa podsieci, która ma być używania z tym zestawem skali.  Jeśli nie podano żadnej wartości, zostanie utworzona nowa podsieci o takiej samej nazwie jak zestaw skali.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SystemAssignedIdentity
Jeśli parametr istnieje, to maszyny wirtualne w zestawie skali mają przypisaną automatycznie wygenerowaną tożsamość systemu zarządzanego.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpgradePolicyMode
Tryb zasad uaktualniania dla wystąpień maszyny wirtualnej w tym zestawie skali.  Zasady uaktualniania mogą określać uaktualnienia automatyczne, ręczne lub uaktualnianie.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.UpgradeMode
Parameter Sets: SimpleParameterSet
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserAssignedIdentity
Nazwa tożsamości usługi zarządzanej, która powinna być przypisana do maszyn wirtualnych w zestawie skali.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
Określa obiekt **VirtualMachineScaleSet** zawierający właściwości usługi VIRTUALSSS, które tworzy to polecenie cmdlet.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VirtualNetworkName
Nazwa sieci wirtualnej do użycia z tym zestawem skali.  Jeśli nie zostanie podany żadna wartość, zostanie utworzona nowa sieć wirtualna o takiej samej nazwie jak zestaw skali.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMScaleSetName
Określa nazwę usługi MASZYNY.WIRTUALNEj, która jest owana przez to polecenie cmdlet.

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VmSize
Rozmiar wystąpień maszyny wirtualnej w tym zestawie skali.  Rozmiar domyślny (Standard_DS1_v2) będzie używany, jeśli nie określono rozmiaru.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### -VnetAddressPrefix
Prefiks adresu sieci wirtualnej używanej w tym zestawie skal.  Domyślne ustawienia prefiksu adresów sieci wirtualnej (192.168.0.0/16) będą używane, jeśli nie zostanie włączona żadna wartość.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### — Strefa
Lista stref dostępności oznaczających adresy IP przydzielone do zasobu.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Potwierdź
Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.
Polecenie cmdlet nie zostanie uruchomione.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.String

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet

### System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet

## NOTATKI

## LINKI POKREWNE

[Get-AzVmss](./Get-AzVmss.md)

[Remove-AzVmss](./Remove-AzVmss.md)

[Restart-AzVmss](./Restart-AzVmss.md)

[Set-AzVmss](./Set-AzVmss.md)

[Start-AzVmss](./Start-AzVmss.md)

[Stop-AzVmss](./Stop-AzVmss.md)

[Update-AzVmss](./Update-AzVmss.md)


