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
# <span data-ttu-id="3240a-101">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3240a-101">New-AzVmss</span></span>

## <span data-ttu-id="3240a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3240a-102">SYNOPSIS</span></span>
<span data-ttu-id="3240a-103">Tworzy maszyny wirtualne.</span><span class="sxs-lookup"><span data-stu-id="3240a-103">Creates a VMSS.</span></span>

## <span data-ttu-id="3240a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3240a-104">SYNTAX</span></span>

### <span data-ttu-id="3240a-105">DefaultParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="3240a-105">DefaultParameter (Default)</span></span>
```
New-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3240a-106">SimpleParameterSet</span><span class="sxs-lookup"><span data-stu-id="3240a-106">SimpleParameterSet</span></span>
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

## <span data-ttu-id="3240a-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="3240a-107">DESCRIPTION</span></span>
<span data-ttu-id="3240a-108">Polecenie **cmdlet New-AzVmss** tworzy na platformie Azure zestaw skal maszyn wirtualnych (VIRTUAL Machine Scale Set).</span><span class="sxs-lookup"><span data-stu-id="3240a-108">The **New-AzVmss** cmdlet creates a Virtual Machine Scale Set (VMSS) in Azure.</span></span>
<span data-ttu-id="3240a-109">Użyj prostego zestawu parametrów () w celu szybkiego utworzenia wstępnie ustawionej maszyny `SimpleParameterSet` wirtualnej i skojarzonych zasobów.</span><span class="sxs-lookup"><span data-stu-id="3240a-109">Use the simple parameter set (`SimpleParameterSet`) to quickly create a pre-set VMSS and associated resources.</span></span> <span data-ttu-id="3240a-110">Użyj domyślnego zestawu parametrów () w bardziej zaawansowanych scenariuszach, gdy musisz dokładnie skonfigurować każdy składnik usługi VMSS i każdego skojarzonego zasobu przed `DefaultParameter` utworzeniem.</span><span class="sxs-lookup"><span data-stu-id="3240a-110">Use the default parameter set (`DefaultParameter`) for more advanced scenarios when you need to precisely configure each component of the VMSS and each associated resource before creation.</span></span>

## <span data-ttu-id="3240a-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3240a-111">EXAMPLES</span></span>

### <span data-ttu-id="3240a-112">Przykład 1. Tworzenie maszyny wirtualnej przy użyciu **`SimpleParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="3240a-112">Example 1: Create a VMSS using the **`SimpleParameterSet`**</span></span>
```powershell
$vmssName = <VMSSNAME>
# Create credentials, I am using one way to create credentials, there are others as well. 
# Pick one that makes the most sense according to your use case.
$vmPassword = ConvertTo-SecureString <PASSWORD_HERE> -AsPlainText -Force
$vmCred = New-Object System.Management.Automation.PSCredential(<USERNAME_HERE>, $vmPassword)

#Create a VMSS using the default settings
New-AzVmss -Credential $vmCred -VMScaleSetName $vmssName
```

<span data-ttu-id="3240a-113">Powyższe polecenie tworzy następujące polecenie o `$vmssName` nazwie:</span><span class="sxs-lookup"><span data-stu-id="3240a-113">The command above creates the following with the name `$vmssName` :</span></span>
* <span data-ttu-id="3240a-114">Grupa zasobów</span><span class="sxs-lookup"><span data-stu-id="3240a-114">A Resource Group</span></span>
* <span data-ttu-id="3240a-115">Sieć wirtualna</span><span class="sxs-lookup"><span data-stu-id="3240a-115">A virtual network</span></span>
* <span data-ttu-id="3240a-116">Równoważenie obciążenia</span><span class="sxs-lookup"><span data-stu-id="3240a-116">A load balancer</span></span>
* <span data-ttu-id="3240a-117">Publiczny adres IP</span><span class="sxs-lookup"><span data-stu-id="3240a-117">A public IP</span></span>
* <span data-ttu-id="3240a-118">maszyny wirtualnej z 2 wystąpieniami</span><span class="sxs-lookup"><span data-stu-id="3240a-118">the VMSS with 2 instances</span></span>

<span data-ttu-id="3240a-119">Domyślny obraz wybrany dla maszyn wirtualnych w maszyny wirtualnej jest, `2016-Datacenter Windows Server` a wersja SKU to `Standard_DS1_v2`</span><span class="sxs-lookup"><span data-stu-id="3240a-119">The default image chosen for the VMs in the VMSS is `2016-Datacenter Windows Server` and the SKU is `Standard_DS1_v2`</span></span>

### <span data-ttu-id="3240a-120">Przykład 2. Tworzenie maszyny wirtualnej przy użyciu **`DefaultParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="3240a-120">Example 2: Create a VMSS using the **`DefaultParameterSet`**</span></span>
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

<span data-ttu-id="3240a-121">W powyższym złożonym przykładzie jest powodna maszyny wirtualnej. Poniżej przedstawiono wyjaśnienie tego, co się dzieje:</span><span class="sxs-lookup"><span data-stu-id="3240a-121">The complex example above creates a VMSS, following is an explanation of what is happening:</span></span>
* <span data-ttu-id="3240a-122">Pierwsze polecenie tworzy grupę zasobów o określonej nazwie i lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="3240a-122">The first command creates a resource group with the specified name and location.</span></span>
* <span data-ttu-id="3240a-123">Drugie polecenie tworzy konto magazynu za pomocą polecenia cmdlet **New-AzStorageAccount.**</span><span class="sxs-lookup"><span data-stu-id="3240a-123">The second command uses the **New-AzStorageAccount** cmdlet to create a storage account.</span></span>
* <span data-ttu-id="3240a-124">Trzecie polecenie użyje następnie polecenia cmdlet **Get-AzStorageAccount** w celu uzyskania konta magazynu utworzonego w drugim poleceniu i przechowuje wynik w $STOAccount danych.</span><span class="sxs-lookup"><span data-stu-id="3240a-124">The third command then uses the **Get-AzStorageAccount** cmdlet to get the storage account created in the second command and stores the result in the $STOAccount variable.</span></span>
* <span data-ttu-id="3240a-125">Piąte polecenie używa polecenia cmdlet **New-AzVirtualNetworkSubnetConfig** do utworzenia podsieci i przechowuje wynik w zmiennej o nazwie $SubNet.</span><span class="sxs-lookup"><span data-stu-id="3240a-125">The fifth command uses the **New-AzVirtualNetworkSubnetConfig** cmdlet to create a subnet and stores the result in the variable named $SubNet.</span></span>
* <span data-ttu-id="3240a-126">Szóste polecenie używa polecenia cmdlet **New-AzVirtualNetwork** do utworzenia sieci wirtualnej i zapisuje wynik w zmiennej o nazwie $VNet.</span><span class="sxs-lookup"><span data-stu-id="3240a-126">The sixth command uses the **New-AzVirtualNetwork** cmdlet to create a virtual network and stores the result in the variable named $VNet.</span></span>
* <span data-ttu-id="3240a-127">Siódme polecenie korzysta z polecenia **Get-AzVirtualNetwork** w celu uzyskania informacji o sieci wirtualnej utworzonej w szóstym poleceniu i przechowuje informacje w zmiennej o nazwie $VNet.</span><span class="sxs-lookup"><span data-stu-id="3240a-127">The seventh command uses the **Get-AzVirtualNetwork** to get information about the virtual network created in the sixth command and stores the information in the variable named $VNet.</span></span>
* <span data-ttu-id="3240a-128">W ósmym i dziewiątym poleceniu są używane polecenia **New-AzPublicIpAddress** i **Get- AzureRmPublicIpAddress** w celu utworzenia i uzyskania informacji z tego publicznego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="3240a-128">The eighth and ninth command uses the **New-AzPublicIpAddress** and **Get- AzureRmPublicIpAddress** to create and get information from that public IP address.</span></span>
* <span data-ttu-id="3240a-129">Polecenia przechowują informacje w zmiennej o nazwie $PubIP.</span><span class="sxs-lookup"><span data-stu-id="3240a-129">The commands store the information in the variable named $PubIP.</span></span>
* <span data-ttu-id="3240a-130">Dziesiąte polecenie używa polecenia cmdlet **New- AzureRmLoadBalancerFrontendIpConfig** w celu utworzenia narzędzia do równoważenia obciążenia frontendu i przechowuje wynik w zmiennej o nazwie $Frontend.</span><span class="sxs-lookup"><span data-stu-id="3240a-130">The tenth command uses the **New- AzureRmLoadBalancerFrontendIpConfig** cmdlet to create a frontend load balancer and stores the result in the variable named $Frontend.</span></span>
* <span data-ttu-id="3240a-131">Polecenie jedenaste używa polecenia **New-AzLoadBalancerBackendAddressPoolConfig** w celu utworzenia konfiguracji puli adresów zaplecza i przechowuje wynik w zmiennej o nazwie $BackendAddressPool.</span><span class="sxs-lookup"><span data-stu-id="3240a-131">The eleventh command uses the **New-AzLoadBalancerBackendAddressPoolConfig** to create a backend address pool configuration and stores the result in the variable named $BackendAddressPool.</span></span>
* <span data-ttu-id="3240a-132">10. polecenie używa polecenia **New-AzLoadBalancerProbeConfig** w celu utworzenia agory i przechowuje informacje o tym pliku w zmiennej o nazwie $Probe.</span><span class="sxs-lookup"><span data-stu-id="3240a-132">The twelfth command uses the **New-AzLoadBalancerProbeConfig** to create a probe and stores the probe information in the variable named $Probe.</span></span>
* <span data-ttu-id="3240a-133">Trzynaste polecenie używa polecenia cmdlet **New-AzLoadBalancerInboundNatPoolConfig** w celu utworzenia konfiguracji puli translacji przychodzącego adresu sieciowego (NAT, load balancer).</span><span class="sxs-lookup"><span data-stu-id="3240a-133">The thirteenth command uses the **New-AzLoadBalancerInboundNatPoolConfig** cmdlet to create a load balancer inbound network address translation (NAT) pool configuration.</span></span>
* <span data-ttu-id="3240a-134">Polecenie czternaste używa polecenia **New-AzLoadBalancerRuleConfig** w celu utworzenia konfiguracji reguły równoważenia obciążenia i przechowuje wynik w zmiennej o nazwie $LBRule.</span><span class="sxs-lookup"><span data-stu-id="3240a-134">The fourteenth command uses the **New-AzLoadBalancerRuleConfig** to create a load balancer rule configuration and stores the result in the variable named $LBRule.</span></span>
* <span data-ttu-id="3240a-135">To polecenie używa polecenia cmdlet **New-AzLoadBalancer** w celu utworzenia równoważenia obciążenia i zapisuje wynik w zmiennej o nazwie $ActualLb.</span><span class="sxs-lookup"><span data-stu-id="3240a-135">The fifteenth command uses the **New-AzLoadBalancer** cmdlet to create a load balancer and stores the result in the variable named $ActualLb.</span></span>
* <span data-ttu-id="3240a-136">Polecenie **Get-AzLoadBalancer używa polecenia Get-AzLoadBalancer** w celu uzyskania informacji o równoważeniu obciążenia, które zostało utworzone w piętnastym poleceniu i przechowuje informacje w zmiennej o nazwie $ExpectedLb.</span><span class="sxs-lookup"><span data-stu-id="3240a-136">The sixteenth command uses the **Get-AzLoadBalancer** to get information about the load balancer that was created in the fifteenth command and stores the information in the variable named $ExpectedLb.</span></span>
* <span data-ttu-id="3240a-137">Polecenie w programie **New-AzVmssIPConfig używa polecenia cmdlet New-AzVmssIPConfig** do utworzenia konfiguracji ip usługi VMSS i przechowuje informacje w zmiennej o nazwie $IPCfg.</span><span class="sxs-lookup"><span data-stu-id="3240a-137">The seventeenth command uses the **New-AzVmssIPConfig** cmdlet to create a VMSS IP configuration and stores the information in the variable named $IPCfg.</span></span>
* <span data-ttu-id="3240a-138">W osiemnastym poleceniu jest używane polecenie cmdlet **New-AzVmssConfig** w celu utworzenia obiektu konfiguracji maszyny WIRTUALNEJ i zapisuje wynik w zmiennej o nazwie $VMSS.</span><span class="sxs-lookup"><span data-stu-id="3240a-138">The eighteenth command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
* <span data-ttu-id="3240a-139">Polecenie tego typu używa polecenia cmdlet **New-AzVmss w** celu utworzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3240a-139">The nineteenth command uses the **New-AzVmss** cmdlet to create the VMSS.</span></span>

## <span data-ttu-id="3240a-140">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3240a-140">PARAMETERS</span></span>

### <span data-ttu-id="3240a-141">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="3240a-141">-AllocationMethod</span></span>
<span data-ttu-id="3240a-142">Metoda alokacji dla publicznego adresu IP zestawu skali (statycznego lub dynamicznego).</span><span class="sxs-lookup"><span data-stu-id="3240a-142">Allocation method for the Public IP Address of the Scale Set (Static or Dynamic).</span></span>  <span data-ttu-id="3240a-143">Jeśli nie zostanie podany żadna wartość, alokacja będzie statyczna.</span><span class="sxs-lookup"><span data-stu-id="3240a-143">If no value is supplied, allocation will be static.</span></span>

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

### <span data-ttu-id="3240a-144">— AsJob</span><span class="sxs-lookup"><span data-stu-id="3240a-144">-AsJob</span></span>
<span data-ttu-id="3240a-145">Uruchom polecenie cmdlet w tle i zwróć zadanie w celu śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="3240a-145">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="3240a-146">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="3240a-146">-BackendPoolName</span></span>
<span data-ttu-id="3240a-147">Nazwa puli adresów zaplecza do użycia w saldzie równoważenia obciążenia dla tego zestawu skali.</span><span class="sxs-lookup"><span data-stu-id="3240a-147">The name of the backend address pool to use in the load balancer for this Scale Set.</span></span>  <span data-ttu-id="3240a-148">Jeśli nie podano żadnej wartości, zostanie utworzona nowa pula zaplecza o takiej samej nazwie jak zestaw skali.</span><span class="sxs-lookup"><span data-stu-id="3240a-148">If no value is provided, a new backend pool will be created, with the same name as the Scale Set.</span></span>

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

### <span data-ttu-id="3240a-149">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="3240a-149">-BackendPort</span></span>
<span data-ttu-id="3240a-150">Numery portów zaplecza używane przez równoważenie obciążenia przez zestaw skalowania do komunikowania się z maszynami maszyn wirtualnych w zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="3240a-150">Backend port numbers used by the Scale Set load balancer to communicate with VMs in the Scale Set.</span></span>  <span data-ttu-id="3240a-151">Jeśli nie określono żadnych wartości, porty 3389 i 5985 będą używane dla maszyn wirtualnych systemu Windows, a port 22 będzie używany dla maszyn wirtualnych systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="3240a-151">If no values are specified, ports 3389 and 5985 will be used for Windows VMS, and port 22 will be used for Linux VMs.</span></span>

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

### <span data-ttu-id="3240a-152">- Credential</span><span class="sxs-lookup"><span data-stu-id="3240a-152">-Credential</span></span>
<span data-ttu-id="3240a-153">Poświadczenia administratora (nazwa użytkownika i hasło) dla maszyn wirtualnych w tym zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="3240a-153">The administrator credentials (username and password) for VMs in this Scale Set.</span></span>

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

### <span data-ttu-id="3240a-154">-DataSizeSizeInGb</span><span class="sxs-lookup"><span data-stu-id="3240a-154">-DataDiskSizeInGb</span></span>
<span data-ttu-id="3240a-155">Określa rozmiary dysków danych w GB.</span><span class="sxs-lookup"><span data-stu-id="3240a-155">Specifies the sizes of data disks in GB.</span></span>

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

### <span data-ttu-id="3240a-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3240a-156">-DefaultProfile</span></span>
<span data-ttu-id="3240a-157">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3240a-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3240a-158">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="3240a-158">-DomainNameLabel</span></span>
<span data-ttu-id="3240a-159">Etykieta nazwy domeny dla publicznej Fully-Qualified domeny (FQDN) dla tego zestawu skali.</span><span class="sxs-lookup"><span data-stu-id="3240a-159">The domain name label for the public Fully-Qualified domain name (FQDN) for this Scale Set.</span></span> <span data-ttu-id="3240a-160">Jest to pierwszy składnik nazwy domeny przypisywany automatycznie do zestawu skali.</span><span class="sxs-lookup"><span data-stu-id="3240a-160">This is the first component of the domain name that is automatically assigned to the Scale Set.</span></span> <span data-ttu-id="3240a-161">Automatycznie przypisane nazwy domen używają formularza ( <DomainNameLabel> <Location> . cloudapp.azure.com).</span><span class="sxs-lookup"><span data-stu-id="3240a-161">Automatically assigned Domain names use the form (<DomainNameLabel>.<Location>.cloudapp.azure.com).</span></span> <span data-ttu-id="3240a-162">Jeśli nie zostanie włączona żadna wartość, domyślną etykietą nazwy domeny będzie złączenie <ScaleSetName> <ResourceGroupName> oraz.</span><span class="sxs-lookup"><span data-stu-id="3240a-162">If no value is supplied, the default domain name label will be the concatenation of <ScaleSetName> and <ResourceGroupName>.</span></span>

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

### <span data-ttu-id="3240a-163">-EnableUltrasSD</span><span class="sxs-lookup"><span data-stu-id="3240a-163">-EnableUltraSSD</span></span>
<span data-ttu-id="3240a-164">Użyj płyty ultrassd dla maszyn wirtualnych w zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="3240a-164">Use UltraSSD disks for the VMs in the scale set.</span></span>

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

### <span data-ttu-id="3240a-165">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="3240a-165">-EncryptionAtHost</span></span>
<span data-ttu-id="3240a-166">Ten parametr umożliwia szyfrowanie dla wszystkich dysków dysków, w tym dysku zasobu/tempa na samym hoście.</span><span class="sxs-lookup"><span data-stu-id="3240a-166">This parameter will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="3240a-167">Domyślne: Szyfrowanie na hoście zostanie wyłączone, chyba że dla zasobu ta właściwość jest ustawiona na prawda.</span><span class="sxs-lookup"><span data-stu-id="3240a-167">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

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

### <span data-ttu-id="3240a-168">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="3240a-168">-EvictionPolicy</span></span>
<span data-ttu-id="3240a-169">Zasady wywłasowania dla zestawu skali maszyny wirtualnej o niskim priorytecie.</span><span class="sxs-lookup"><span data-stu-id="3240a-169">The eviction policy for the low priority virtual machine scale set.</span></span>  <span data-ttu-id="3240a-170">Obsługiwane są tylko wartości "Deallocate" i "Delete".</span><span class="sxs-lookup"><span data-stu-id="3240a-170">Only supported values are 'Deallocate' and 'Delete'.</span></span>

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

### <span data-ttu-id="3240a-171">-FrontendPoolName</span><span class="sxs-lookup"><span data-stu-id="3240a-171">-FrontendPoolName</span></span>
<span data-ttu-id="3240a-172">Nazwa puli adresów frontendowych do użycia w zestawie skalowania równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="3240a-172">The name of the frontend address pool to use in the Scale Set load balancer.</span></span>  <span data-ttu-id="3240a-173">Jeśli nie zostanie podany żadna wartość, zostanie utworzona nowa pula adresów frontendowych o takiej samej nazwie jak zestaw skali.</span><span class="sxs-lookup"><span data-stu-id="3240a-173">If no value is supplied, a new Frontend Address Pool will be created, with the same name as the scale set.</span></span>

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

### <span data-ttu-id="3240a-174">-HostGroupId</span><span class="sxs-lookup"><span data-stu-id="3240a-174">-HostGroupId</span></span>
<span data-ttu-id="3240a-175">Określa dedykowaną grupę hosta, w którym będzie znajdować się zestaw skal maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="3240a-175">Specifies the dedicated host group the virtual machine scale set will reside in.</span></span>

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

### <span data-ttu-id="3240a-176">-ImageName</span><span class="sxs-lookup"><span data-stu-id="3240a-176">-ImageName</span></span>
<span data-ttu-id="3240a-177">Nazwa obrazu dla maszyn wirtualnych w tym zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="3240a-177">The name of the image for VMs in this Scale Set.</span></span> <span data-ttu-id="3240a-178">Jeśli nie podano żadnej wartości, zostanie użyty obraz "Windows Server 2016 DataCenter".</span><span class="sxs-lookup"><span data-stu-id="3240a-178">If no value is provided, the "Windows Server 2016 DataCenter" image will be used.</span></span>

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

### <span data-ttu-id="3240a-179">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="3240a-179">-InstanceCount</span></span>
<span data-ttu-id="3240a-180">Liczba obrazów maszyny wirtualnej w zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="3240a-180">The number of VM images in the Scale Set.</span></span>  <span data-ttu-id="3240a-181">Jeśli nie podano żadnej wartości, zostaną utworzone 2 wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="3240a-181">If no value is provided, 2 instances will be created.</span></span>

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

### <span data-ttu-id="3240a-182">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="3240a-182">-LoadBalancerName</span></span>
<span data-ttu-id="3240a-183">Nazwa równoważenia obciążenia do użycia z tym zestawem skal.</span><span class="sxs-lookup"><span data-stu-id="3240a-183">The name of the load balancer to use with this Scale Set.</span></span>  <span data-ttu-id="3240a-184">Jeśli nie zostanie określona żadna wartość, zostanie utworzone nowe równoważenie obciążenia o takiej samej nazwie jak zestaw skali.</span><span class="sxs-lookup"><span data-stu-id="3240a-184">A new load balancer using the same name as the Scale Set will be created if no value is specified.</span></span>

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

### <span data-ttu-id="3240a-185">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3240a-185">-Location</span></span>
<span data-ttu-id="3240a-186">Lokalizacja platformy Azure, w której zostanie utworzony ten zestaw skali.</span><span class="sxs-lookup"><span data-stu-id="3240a-186">The Azure location where this Scale Set will be created.</span></span>  <span data-ttu-id="3240a-187">Jeśli nie zostanie określona żadna wartość, lokalizacja zostanie wywłaszona na przykład z lokalizacji innych zasobów, do których odwołują się parametry.</span><span class="sxs-lookup"><span data-stu-id="3240a-187">If no value is specified, the location will be inferred from the location of other resources referenced in the parameters.</span></span>

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

### <span data-ttu-id="3240a-188">- MaxCena</span><span class="sxs-lookup"><span data-stu-id="3240a-188">-MaxPrice</span></span>
<span data-ttu-id="3240a-189">Maksymalna cena rozliczenia zestawu skal maszyn wirtualnych o niskim priorytecie.</span><span class="sxs-lookup"><span data-stu-id="3240a-189">The max price of the billing of a low priority virtual machine scale set.</span></span>

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

### <span data-ttu-id="3240a-190">-NatBackendPort</span><span class="sxs-lookup"><span data-stu-id="3240a-190">-NatBackendPort</span></span>
<span data-ttu-id="3240a-191">Port zaplecza do translacji przychodzącego adresu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="3240a-191">Backend port for inbound network address translation.</span></span>

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

### <span data-ttu-id="3240a-192">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="3240a-192">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="3240a-193">Liczba domen błędów dla każdej grupy położenia.</span><span class="sxs-lookup"><span data-stu-id="3240a-193">Fault Domain count for each placement group.</span></span>

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

### <span data-ttu-id="3240a-194">— Priority (Priorytet)</span><span class="sxs-lookup"><span data-stu-id="3240a-194">-Priority</span></span>
<span data-ttu-id="3240a-195">Priorytet maszyny wirtualnej w zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="3240a-195">The priority for the virtual machine in the scale set.</span></span>  <span data-ttu-id="3240a-196">Obsługiwane są tylko wartości "Zwykła", "Spot" i "Niska".</span><span class="sxs-lookup"><span data-stu-id="3240a-196">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="3240a-197">"Zwykła" jest dla zwykłej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3240a-197">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="3240a-198">"Spot" jest dla maszyny wirtualnej spot.</span><span class="sxs-lookup"><span data-stu-id="3240a-198">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="3240a-199">"Low" jest również dla spot virtual machine, ale jest zastępowany przez "Spot".</span><span class="sxs-lookup"><span data-stu-id="3240a-199">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="3240a-200">Użyj pozycji Spot (Spot) zamiast "Low" (Najniszej).</span><span class="sxs-lookup"><span data-stu-id="3240a-200">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="3240a-201">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="3240a-201">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="3240a-202">Identyfikator zasobu grupy Położenie odległości do użycia z tym zestawem skali.</span><span class="sxs-lookup"><span data-stu-id="3240a-202">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="3240a-203">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="3240a-203">-PublicIpAddressName</span></span>
<span data-ttu-id="3240a-204">Nazwa publicznego adresu IP, który ma być podany w tym zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="3240a-204">The name of the public IP Address to use with this scale set.</span></span>  <span data-ttu-id="3240a-205">Jeśli nie podano żadnej wartości, zostanie utworzona nowa publiczna adres IPAddress o takiej samej nazwie jak zestaw skali.</span><span class="sxs-lookup"><span data-stu-id="3240a-205">A new Public IPAddress with the same name as the Scale Set will be created if no value is provided.</span></span>

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

### <span data-ttu-id="3240a-206">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3240a-206">-ResourceGroupName</span></span>
<span data-ttu-id="3240a-207">Określa nazwę grupy zasobów maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="3240a-207">Specifies the name of the resource group of the VMSS.</span></span>  <span data-ttu-id="3240a-208">Jeśli nie zostanie określona żadna wartość, nowa grupa zasobów zostanie utworzona pod taką samą nazwą jak zestaw skali.</span><span class="sxs-lookup"><span data-stu-id="3240a-208">If no value is specified, a new ResourceGroup will be created using the same name as the Scale Set.</span></span>

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

### <span data-ttu-id="3240a-209">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="3240a-209">-ScaleInPolicy</span></span>
<span data-ttu-id="3240a-210">Reguły, które mają być stosowane podczas skalowania w zestawie skalowania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3240a-210">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="3240a-211">Dopuszczalne wartości to: "Domyślne", "NajstarszeVM" i "NajnowszeVM".</span><span class="sxs-lookup"><span data-stu-id="3240a-211">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="3240a-212">Ustawienie "Domyślne", gdy skala zestawu maszyn wirtualnych jest skalowana w, zestaw skali zostanie najpierw wyrównany w różnych strefach, jeśli jest to zestaw skali zonal.</span><span class="sxs-lookup"><span data-stu-id="3240a-212">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="3240a-213">Następnie zostanie on w możliwie najdalej sytą równowagi między domenami błędów.</span><span class="sxs-lookup"><span data-stu-id="3240a-213">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="3240a-214">W obrębie każdej domeny błędu maszyny wirtualne wybrane do usunięcia będą najnowszymi, które nie są chronione przez skalowanie.</span><span class="sxs-lookup"><span data-stu-id="3240a-214">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="3240a-215">Podczas skalowania zestawu skalowania dla maszyny wirtualnej najstarsze maszyny wirtualne, które nie są chronione przez skalowanie, zostaną wybrane do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="3240a-215">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="3240a-216">W przypadku zestawów skali zonal virtual machine(zonal virtual machine) zestaw skal zostanie najpierw zrównoważony w różnych strefach.</span><span class="sxs-lookup"><span data-stu-id="3240a-216">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="3240a-217">W każdej strefie najstarsze komputery wirtualne, które nie są chronione, zostaną wybrane do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="3240a-217">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="3240a-218">"Najnowsza wersja VM", gdy jest skalowany zestaw skalowania zestawu maszyn wirtualnych, najnowsze maszyny wirtualne, które nie są chronione przez skalowanie, zostaną wybrane do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="3240a-218">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="3240a-219">W przypadku zestawów skali zonal virtual machine(zonal virtual machine) zestaw skal zostanie najpierw syrównowany w różnych strefach.</span><span class="sxs-lookup"><span data-stu-id="3240a-219">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="3240a-220">W każdej strefie do usunięcia zostaną wybrane najnowsze maszyny wirtualne, które nie są chronione.</span><span class="sxs-lookup"><span data-stu-id="3240a-220">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

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

### <span data-ttu-id="3240a-221">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="3240a-221">-SecurityGroupName</span></span>
<span data-ttu-id="3240a-222">Nazwa grupy zabezpieczeń sieci, która ma być stosowane do tego zestawu skali.</span><span class="sxs-lookup"><span data-stu-id="3240a-222">The name of the network security group to apply to this Scale Set.</span></span>  <span data-ttu-id="3240a-223">Jeśli nie podano żadnej wartości, domyślna grupa zabezpieczeń sieci o takiej samej nazwie jak zestaw skali zostanie utworzona i zastosowana do zestawu skali.</span><span class="sxs-lookup"><span data-stu-id="3240a-223">If no value is provided, a default network security group with the same name as the Scale Set will be created and applied to the Scale Set.</span></span>

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

### <span data-ttu-id="3240a-224">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="3240a-224">-SinglePlacementGroup</span></span>
<span data-ttu-id="3240a-225">Użyj tej opcji, aby utworzyć zestaw skal w jednej grupie położenia, wartością domyślną jest wiele grup</span><span class="sxs-lookup"><span data-stu-id="3240a-225">Use this to create the Scale set in a single placement group, default is multiple groups</span></span>

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

### <span data-ttu-id="3240a-226">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="3240a-226">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="3240a-227">Określa, że rozszerzenia nie są uruchamiane na dodatkowych nadprowizowanych maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="3240a-227">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="3240a-228">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3240a-228">-SubnetAddressPrefix</span></span>
<span data-ttu-id="3240a-229">Prefiks adresu podsieci, z których będzie korzystać ten zestaw skal.</span><span class="sxs-lookup"><span data-stu-id="3240a-229">The address prefix of the Subnet this ScaleSet will use.</span></span> <span data-ttu-id="3240a-230">Domyślne ustawienia podsieci (192.168.1.0/24) zostaną zastosowane, jeśli nie podano żadnej wartości.</span><span class="sxs-lookup"><span data-stu-id="3240a-230">Default Subnet settings (192.168.1.0/24) will be applied if no value is provided.</span></span>

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

### <span data-ttu-id="3240a-231">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="3240a-231">-SubnetName</span></span>
<span data-ttu-id="3240a-232">Nazwa podsieci, która ma być używania z tym zestawem skali.</span><span class="sxs-lookup"><span data-stu-id="3240a-232">The name of the subnet to use with this Scale Set.</span></span>  <span data-ttu-id="3240a-233">Jeśli nie podano żadnej wartości, zostanie utworzona nowa podsieci o takiej samej nazwie jak zestaw skali.</span><span class="sxs-lookup"><span data-stu-id="3240a-233">A new Subnet will be created with the same name as the Scale Set if no value is provided.</span></span>

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

### <span data-ttu-id="3240a-234">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="3240a-234">-SystemAssignedIdentity</span></span>
<span data-ttu-id="3240a-235">Jeśli parametr istnieje, to maszyny wirtualne w zestawie skali mają przypisaną automatycznie wygenerowaną tożsamość systemu zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="3240a-235">If the parameter is present then the VM(s) in the scale set is(are) assigned a managed system identity that is auto generated.</span></span>

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

### <span data-ttu-id="3240a-236">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="3240a-236">-UpgradePolicyMode</span></span>
<span data-ttu-id="3240a-237">Tryb zasad uaktualniania dla wystąpień maszyny wirtualnej w tym zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="3240a-237">The upgrade policy mode for VM instances in this Scale Set.</span></span>  <span data-ttu-id="3240a-238">Zasady uaktualniania mogą określać uaktualnienia automatyczne, ręczne lub uaktualnianie.</span><span class="sxs-lookup"><span data-stu-id="3240a-238">Upgrade policy could specify Automatic, Manual, or Rolling upgrades.</span></span>

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

### <span data-ttu-id="3240a-239">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="3240a-239">-UserAssignedIdentity</span></span>
<span data-ttu-id="3240a-240">Nazwa tożsamości usługi zarządzanej, która powinna być przypisana do maszyn wirtualnych w zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="3240a-240">The name of a managed service identity that should be assigned to the VM(s) in the scale set.</span></span>

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

### <span data-ttu-id="3240a-241">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3240a-241">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="3240a-242">Określa obiekt **VirtualMachineScaleSet** zawierający właściwości usługi VIRTUALSSS, które tworzy to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3240a-242">Specifies the **VirtualMachineScaleSet** object that contains the properties of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="3240a-243">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="3240a-243">-VirtualNetworkName</span></span>
<span data-ttu-id="3240a-244">Nazwa sieci wirtualnej do użycia z tym zestawem skali.</span><span class="sxs-lookup"><span data-stu-id="3240a-244">The name fo the Virtual Network to use with this scale set.</span></span>  <span data-ttu-id="3240a-245">Jeśli nie zostanie podany żadna wartość, zostanie utworzona nowa sieć wirtualna o takiej samej nazwie jak zestaw skali.</span><span class="sxs-lookup"><span data-stu-id="3240a-245">If no value is supplied, a new virtual network with the same name as the Scale Set will be created.</span></span>

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

### <span data-ttu-id="3240a-246">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="3240a-246">-VMScaleSetName</span></span>
<span data-ttu-id="3240a-247">Określa nazwę usługi MASZYNY.WIRTUALNEj, która jest owana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3240a-247">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="3240a-248">-VmSize</span><span class="sxs-lookup"><span data-stu-id="3240a-248">-VmSize</span></span>
<span data-ttu-id="3240a-249">Rozmiar wystąpień maszyny wirtualnej w tym zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="3240a-249">The size of the VM instances in this scale set.</span></span>  <span data-ttu-id="3240a-250">Rozmiar domyślny (Standard_DS1_v2) będzie używany, jeśli nie określono rozmiaru.</span><span class="sxs-lookup"><span data-stu-id="3240a-250">A default size (Standard_DS1_v2) will be used if no Size is specified.</span></span>

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

### <span data-ttu-id="3240a-251">-VnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3240a-251">-VnetAddressPrefix</span></span>
<span data-ttu-id="3240a-252">Prefiks adresu sieci wirtualnej używanej w tym zestawie skal.</span><span class="sxs-lookup"><span data-stu-id="3240a-252">The address prefix for the virtual network used with this Scale Set.</span></span>  <span data-ttu-id="3240a-253">Domyślne ustawienia prefiksu adresów sieci wirtualnej (192.168.0.0/16) będą używane, jeśli nie zostanie włączona żadna wartość.</span><span class="sxs-lookup"><span data-stu-id="3240a-253">Default virtual network address prefix settings (192.168.0.0/16) will be used if no value is supplied.</span></span>

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

### <span data-ttu-id="3240a-254">— Strefa</span><span class="sxs-lookup"><span data-stu-id="3240a-254">-Zone</span></span>
<span data-ttu-id="3240a-255">Lista stref dostępności oznaczających adresy IP przydzielone do zasobu.</span><span class="sxs-lookup"><span data-stu-id="3240a-255">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="3240a-256">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3240a-256">-Confirm</span></span>
<span data-ttu-id="3240a-257">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3240a-257">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3240a-258">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3240a-258">-WhatIf</span></span>
<span data-ttu-id="3240a-259">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3240a-259">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3240a-260">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3240a-260">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3240a-261">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3240a-261">CommonParameters</span></span>
<span data-ttu-id="3240a-262">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3240a-262">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3240a-263">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3240a-263">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3240a-264">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3240a-264">INPUTS</span></span>

### <span data-ttu-id="3240a-265">System.String</span><span class="sxs-lookup"><span data-stu-id="3240a-265">System.String</span></span>

### <span data-ttu-id="3240a-266">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3240a-266">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="3240a-267">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3240a-267">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="3240a-268">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3240a-268">OUTPUTS</span></span>

### <span data-ttu-id="3240a-269">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3240a-269">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="3240a-270">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3240a-270">NOTES</span></span>

## <span data-ttu-id="3240a-271">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3240a-271">RELATED LINKS</span></span>

[<span data-ttu-id="3240a-272">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3240a-272">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="3240a-273">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3240a-273">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="3240a-274">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3240a-274">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="3240a-275">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3240a-275">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="3240a-276">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3240a-276">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="3240a-277">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3240a-277">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="3240a-278">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3240a-278">Update-AzVmss</span></span>](./Update-AzVmss.md)


