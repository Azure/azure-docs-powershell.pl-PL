---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
ms.openlocfilehash: 780e2f9e222ec173fcce6bca88fb85f37dda1450
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706314"
---
# <span data-ttu-id="5ba89-101">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="5ba89-101">New-AzVmss</span></span>

## <span data-ttu-id="5ba89-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5ba89-102">SYNOPSIS</span></span>
<span data-ttu-id="5ba89-103">Tworzy VMSS.</span><span class="sxs-lookup"><span data-stu-id="5ba89-103">Creates a VMSS.</span></span>

## <span data-ttu-id="5ba89-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5ba89-104">SYNTAX</span></span>

### <span data-ttu-id="5ba89-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5ba89-105">DefaultParameter (Default)</span></span>
```
New-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ba89-106">SimpleParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ba89-106">SimpleParameterSet</span></span>
```
New-AzVmss [[-ResourceGroupName] <String>] [-VMScaleSetName] <String> [-AsJob] [-ImageName <String>]
 -Credential <PSCredential> [-InstanceCount <Int32>] [-VirtualNetworkName <String>] [-SubnetName <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-SecurityGroupName <String>]
 [-LoadBalancerName <String>] [-BackendPort <Int32[]>] [-Location <String>] [-VmSize <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-AllocationMethod <String>] [-VnetAddressPrefix <String>]
 [-SubnetAddressPrefix <String>] [-FrontendPoolName <String>] [-BackendPoolName <String>]
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-EnableUltraSSD]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-NatBackendPort <Int32[]>]
 [-DataDiskSizeInGb <Int32[]>] [-ProximityPlacementGroup <String>] [-Priority <String>]
 [-EvictionPolicy <String>] [-MaxPrice <Double>] [-DefaultProfile <IAzureContextContainer>]
 [-SinglePlacementGroup] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ba89-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5ba89-107">DESCRIPTION</span></span>
<span data-ttu-id="5ba89-108">Polecenie cmdlet **New-AzVmss** umożliwia utworzenie zestawu skali maszyny wirtualnej (VMSS) na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="5ba89-108">The **New-AzVmss** cmdlet creates a Virtual Machine Scale Set (VMSS) in Azure.</span></span>
<span data-ttu-id="5ba89-109">Użyj prostego zestawu parametrów ( `SimpleParameterSet` ), aby szybko utworzyć wstępnie ustawiony VMSS i skojarzone zasoby.</span><span class="sxs-lookup"><span data-stu-id="5ba89-109">Use the simple parameter set (`SimpleParameterSet`) to quickly create a pre-set VMSS and associated resources.</span></span> <span data-ttu-id="5ba89-110">Użyj domyślnego zestawu parametrów ( `DefaultParameter` ), aby bardziej zaawansowane scenariusze można było precyzyjnie skonfigurować poszczególne składniki VMSS oraz wszystkie skojarzone z nimi zasoby przed utworzeniem.</span><span class="sxs-lookup"><span data-stu-id="5ba89-110">Use the default parameter set (`DefaultParameter`) for more advanced scenarios when you need to precisely configure each component of the VMSS and each associated resource before creation.</span></span>

## <span data-ttu-id="5ba89-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5ba89-111">EXAMPLES</span></span>

### <span data-ttu-id="5ba89-112">Przykład 1. Tworzenie VMSS przy użyciu **`SimpleParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="5ba89-112">Example 1: Create a VMSS using the **`SimpleParameterSet`**</span></span>
```powershell
$vmssName = <VMSSNAME>
# Create credentials, I am using one way to create credentials, there are others as well. 
# Pick one that makes the most sense according to your use case.
$vmPassword = ConvertTo-SecureString <PASSWORD_HERE> -AsPlainText -Force
$vmCred = New-Object System.Management.Automation.PSCredential(<USERNAME_HERE>, $vmPassword)

#Create a VMSS using the default settings
New-AzVmss -Credential $vmCred -VMScaleSetName $vmssName
```

<span data-ttu-id="5ba89-113">W powyższym poleceniu zostanie utworzona następująca nazwa `$vmssName` :</span><span class="sxs-lookup"><span data-stu-id="5ba89-113">The command above creates the following with the name `$vmssName` :</span></span>
* <span data-ttu-id="5ba89-114">Grupa zasobów</span><span class="sxs-lookup"><span data-stu-id="5ba89-114">A Resource Group</span></span>
* <span data-ttu-id="5ba89-115">Sieć wirtualna</span><span class="sxs-lookup"><span data-stu-id="5ba89-115">A virtual network</span></span>
* <span data-ttu-id="5ba89-116">Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="5ba89-116">A load balancer</span></span>
* <span data-ttu-id="5ba89-117">Publiczny adres IP</span><span class="sxs-lookup"><span data-stu-id="5ba89-117">A public IP</span></span>
* <span data-ttu-id="5ba89-118">VMSS z dwoma wystąpieniami</span><span class="sxs-lookup"><span data-stu-id="5ba89-118">the VMSS with 2 instances</span></span>

<span data-ttu-id="5ba89-119">Domyślnym obrazem wybranym dla maszyn wirtualnych w VMSS jest `2016-Datacenter Windows Server` , a wersja SKU to `Standard_DS1_v2`</span><span class="sxs-lookup"><span data-stu-id="5ba89-119">The default image chosen for the VMs in the VMSS is `2016-Datacenter Windows Server` and the SKU is `Standard_DS1_v2`</span></span>

### <span data-ttu-id="5ba89-120">Przykład 2: Tworzenie VMSS przy użyciu **`DefaultParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="5ba89-120">Example 2: Create a VMSS using the **`DefaultParameterSet`**</span></span>
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
$VMSS = New-AzVmssConfig -Location $LOC -SkuCapacity 2 -SkuName "Standard_A2" -UpgradePolicyMode "Automatic" `
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

<span data-ttu-id="5ba89-121">W złożonym przykładzie powyżej powstaje VMSS, poniżej przedstawiono wyjaśnienie, co się dzieje:</span><span class="sxs-lookup"><span data-stu-id="5ba89-121">The complex example above creates a VMSS, following is an explanation of what is happening:</span></span>
* <span data-ttu-id="5ba89-122">Pierwsze polecenie tworzy grupę zasobów o określonej nazwie i lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="5ba89-122">The first command creates a resource group with the specified name and location.</span></span>
* <span data-ttu-id="5ba89-123">Drugie polecenie używa polecenia cmdlet **New-AzStorageAccount** w celu utworzenia konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="5ba89-123">The second command uses the **New-AzStorageAccount** cmdlet to create a storage account.</span></span>
* <span data-ttu-id="5ba89-124">Trzecia komenda używa polecenia cmdlet **Get-AzStorageAccount** w celu uzyskania konta magazynu utworzonego w drugim poleceniu i zapisanie wyniku w zmiennej $STOAccount.</span><span class="sxs-lookup"><span data-stu-id="5ba89-124">The third command then uses the **Get-AzStorageAccount** cmdlet to get the storage account created in the second command and stores the result in the $STOAccount variable.</span></span>
* <span data-ttu-id="5ba89-125">W piątym poleceniu użyto polecenia cmdlet **New-AzVirtualNetworkSubnetConfig** w celu utworzenia podsieci i zapisanie wyniku w zmiennej o nazwie $Subnet.</span><span class="sxs-lookup"><span data-stu-id="5ba89-125">The fifth command uses the **New-AzVirtualNetworkSubnetConfig** cmdlet to create a subnet and stores the result in the variable named $SubNet.</span></span>
* <span data-ttu-id="5ba89-126">W szóstym poleceniu użyto polecenia cmdlet **New-AzVirtualNetwork** w celu utworzenia sieci wirtualnej i zapisu wyniku w zmiennej o nazwie $VNET.</span><span class="sxs-lookup"><span data-stu-id="5ba89-126">The sixth command uses the **New-AzVirtualNetwork** cmdlet to create a virtual network and stores the result in the variable named $VNet.</span></span>
* <span data-ttu-id="5ba89-127">W przypadku siódmego polecenia w celu uzyskania informacji o sieci wirtualnej utworzonej w szóstym poleceniu jest używane polecenie **Get-AzVirtualNetwork** , a informacje są przechowywane w zmiennej o nazwie $VNET.</span><span class="sxs-lookup"><span data-stu-id="5ba89-127">The seventh command uses the **Get-AzVirtualNetwork** to get information about the virtual network created in the sixth command and stores the information in the variable named $VNet.</span></span>
* <span data-ttu-id="5ba89-128">W przypadku ośmiu i Dziewiątych poleceń do tworzenia i pobierania informacji z tego publicznego adresu IP użyto polecenia **New-AzPublicIpAddress** i **Get-AzureRmPublicIpAddress** .</span><span class="sxs-lookup"><span data-stu-id="5ba89-128">The eighth and ninth command uses the **New-AzPublicIpAddress** and **Get- AzureRmPublicIpAddress** to create and get information from that public IP address.</span></span>
* <span data-ttu-id="5ba89-129">Te polecenia przechowują informacje w zmiennej o nazwie $PubIP.</span><span class="sxs-lookup"><span data-stu-id="5ba89-129">The commands store the information in the variable named $PubIP.</span></span>
* <span data-ttu-id="5ba89-130">W poleceniu dziesiątym użyto polecenia cmdlet **New-AzureRmLoadBalancerFrontendIpConfig** w celu utworzenia modułu równoważenia obciążenia frontonu i zapisu wyniku w zmiennej o nazwie $frontend.</span><span class="sxs-lookup"><span data-stu-id="5ba89-130">The tenth command uses the **New- AzureRmLoadBalancerFrontendIpConfig** cmdlet to create a frontend load balancer and stores the result in the variable named $Frontend.</span></span>
* <span data-ttu-id="5ba89-131">W jedenastym poleceniu użyto polecenia **New-AzLoadBalancerBackendAddressPoolConfig** w celu utworzenia konfiguracji puli adresów zaplecza i zapisu wyniku w zmiennej o nazwie $BackendAddressPool.</span><span class="sxs-lookup"><span data-stu-id="5ba89-131">The eleventh command uses the **New-AzLoadBalancerBackendAddressPoolConfig** to create a backend address pool configuration and stores the result in the variable named $BackendAddressPool.</span></span>
* <span data-ttu-id="5ba89-132">W poleceniu dwunasta jest używana funkcja **New-AzLoadBalancerProbeConfig** w celu utworzenia sondy i zapisanie informacji dotyczących sondy w zmiennej o nazwie $Probe.</span><span class="sxs-lookup"><span data-stu-id="5ba89-132">The twelfth command uses the **New-AzLoadBalancerProbeConfig** to create a probe and stores the probe information in the variable named $Probe.</span></span>
* <span data-ttu-id="5ba89-133">Polecenie trzynaste używa polecenia cmdlet **New-AzLoadBalancerInboundNatPoolConfig** w celu utworzenia konfiguracji puli NAT (Network Address Translation) modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="5ba89-133">The thirteenth command uses the **New-AzLoadBalancerInboundNatPoolConfig** cmdlet to create a load balancer inbound network address translation (NAT) pool configuration.</span></span>
* <span data-ttu-id="5ba89-134">Polecenie czternaste używa polecenia **New-AzLoadBalancerRuleConfig** w celu utworzenia konfiguracji reguł modułu równoważenia obciążenia i zapisu wyniku w zmiennej o nazwie $LBRule.</span><span class="sxs-lookup"><span data-stu-id="5ba89-134">The fourteenth command uses the **New-AzLoadBalancerRuleConfig** to create a load balancer rule configuration and stores the result in the variable named $LBRule.</span></span>
* <span data-ttu-id="5ba89-135">W poleceniu piętnaste polecenie cmdlet **New-AzLoadBalancer** jest używane do utworzenia modułu równoważenia obciążenia i zapisuje wynik w zmiennej o nazwie $ActualLb.</span><span class="sxs-lookup"><span data-stu-id="5ba89-135">The fifteenth command uses the **New-AzLoadBalancer** cmdlet to create a load balancer and stores the result in the variable named $ActualLb.</span></span>
* <span data-ttu-id="5ba89-136">Polecenie szesnaste używa polecenia **Get-AzLoadBalancer** w celu uzyskania informacji na temat modułu równoważenia obciążenia utworzonego w piętnastym poleceniu i zapisanie informacji w zmiennej o nazwie $ExpectedLb.</span><span class="sxs-lookup"><span data-stu-id="5ba89-136">The sixteenth command uses the **Get-AzLoadBalancer** to get information about the load balancer that was created in the fifteenth command and stores the information in the variable named $ExpectedLb.</span></span>
* <span data-ttu-id="5ba89-137">W poleceniu siedemnasta użyto polecenia cmdlet **New-AzVmssIPConfig** w celu utworzenia VMSS konfiguracji adresu IP i zapisu informacji w zmiennej o nazwie $IPCfg.</span><span class="sxs-lookup"><span data-stu-id="5ba89-137">The seventeenth command uses the **New-AzVmssIPConfig** cmdlet to create a VMSS IP configuration and stores the information in the variable named $IPCfg.</span></span>
* <span data-ttu-id="5ba89-138">Polecenie osiemnastym miesiącem korzysta z polecenia cmdlet **New-AzVmssConfig** w celu utworzenia obiektu konfiguracji VMSS i zapisanie wyniku w zmiennej o nazwie $VMSS.</span><span class="sxs-lookup"><span data-stu-id="5ba89-138">The eighteenth command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
* <span data-ttu-id="5ba89-139">W poleceniu XIX użyto polecenia cmdlet **New-AzVmss** w celu utworzenia VMSS.</span><span class="sxs-lookup"><span data-stu-id="5ba89-139">The nineteenth command uses the **New-AzVmss** cmdlet to create the VMSS.</span></span>

## <span data-ttu-id="5ba89-140">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5ba89-140">PARAMETERS</span></span>

### <span data-ttu-id="5ba89-141">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="5ba89-141">-AllocationMethod</span></span>
<span data-ttu-id="5ba89-142">Metoda alokacji dla publicznego adresu IP zestawu skali (statycznego lub dynamicznego).</span><span class="sxs-lookup"><span data-stu-id="5ba89-142">Allocation method for the Public IP Address of the Scale Set (Static or Dynamic).</span></span>  <span data-ttu-id="5ba89-143">Jeśli nie podano żadnej wartości, alokacja będzie statyczna.</span><span class="sxs-lookup"><span data-stu-id="5ba89-143">If no value is supplied, allocation will be static.</span></span>

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

### <span data-ttu-id="5ba89-144">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ba89-144">-AsJob</span></span>
<span data-ttu-id="5ba89-145">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="5ba89-145">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="5ba89-146">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="5ba89-146">-BackendPoolName</span></span>
<span data-ttu-id="5ba89-147">Nazwa puli adresów zaplecza, która ma być używana w usłudze równoważenia obciążenia dla tego zestawu skali.</span><span class="sxs-lookup"><span data-stu-id="5ba89-147">The name of the backend address pool to use in the load balancer for this Scale Set.</span></span>  <span data-ttu-id="5ba89-148">Jeśli nie podano żadnej wartości, zostanie utworzona nowa pula zaplecza z tą samą nazwą co zestaw skali.</span><span class="sxs-lookup"><span data-stu-id="5ba89-148">If no value is provided, a new backend pool will be created, with the same name as the Scale Set.</span></span>

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

### <span data-ttu-id="5ba89-149">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="5ba89-149">-BackendPort</span></span>
<span data-ttu-id="5ba89-150">Numery portów zaplecza używane przez moduł skalowania, ustawiony w celu komunikowania się z maszynami wirtualnymi w zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="5ba89-150">Backend port numbers used by the Scale Set load balancer to communicate with VMs in the Scale Set.</span></span>  <span data-ttu-id="5ba89-151">Jeśli nie określono żadnych wartości, porty 3389 i 5985 będą używane na potrzeby maszyn wirtualnych systemu Windows, a w przypadku maszyn wirtualnych Linux będzie używana wartość port 22.</span><span class="sxs-lookup"><span data-stu-id="5ba89-151">If no values are specified, ports 3389 and 5985 will be used for Windows VMS, and port 22 will be used for Linux VMs.</span></span>

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

### <span data-ttu-id="5ba89-152">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="5ba89-152">-Credential</span></span>
<span data-ttu-id="5ba89-153">Poświadczenia administratora (nazwa użytkownika i hasło) dla maszyn wirtualnych w tym zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="5ba89-153">The administrator credentials (username and password) for VMs in this Scale Set.</span></span>

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

### <span data-ttu-id="5ba89-154">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="5ba89-154">-DataDiskSizeInGb</span></span>
<span data-ttu-id="5ba89-155">Określa rozmiary dysków z danymi w GB.</span><span class="sxs-lookup"><span data-stu-id="5ba89-155">Specifies the sizes of data disks in GB.</span></span>

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

### <span data-ttu-id="5ba89-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ba89-156">-DefaultProfile</span></span>
<span data-ttu-id="5ba89-157">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5ba89-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ba89-158">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="5ba89-158">-DomainNameLabel</span></span>
<span data-ttu-id="5ba89-159">Etykieta nazwy domeny dla publicznej nazwy domeny Fully-Qualified (FQDN) dla tego zestawu skali.</span><span class="sxs-lookup"><span data-stu-id="5ba89-159">The domain name label for the public Fully-Qualified domain name (FQDN) for this Scale Set.</span></span> <span data-ttu-id="5ba89-160">Jest to pierwszy składnik nazwy domeny, który jest automatycznie przypisywany do zestawu skali.</span><span class="sxs-lookup"><span data-stu-id="5ba89-160">This is the first component of the domain name that is automatically assigned to the Scale Set.</span></span> <span data-ttu-id="5ba89-161">Automatycznie przypisane nazwy domen używają formularza ( <DomainNameLabel> . <Location> . cloudapp.azure.com).</span><span class="sxs-lookup"><span data-stu-id="5ba89-161">Automatically assigned Domain names use the form (<DomainNameLabel>.<Location>.cloudapp.azure.com).</span></span> <span data-ttu-id="5ba89-162">Jeśli nie zostanie podana żadna wartość, domyślna etykieta nazwy domeny będzie łączyć się z <ScaleSetName> i <ResourceGroupName> .</span><span class="sxs-lookup"><span data-stu-id="5ba89-162">If no value is supplied, the default domain name label will be the concatenation of <ScaleSetName> and <ResourceGroupName>.</span></span>

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

### <span data-ttu-id="5ba89-163">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="5ba89-163">-EnableUltraSSD</span></span>
<span data-ttu-id="5ba89-164">Użyj dysków UltraSSD dla maszyn wirtualnych w zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="5ba89-164">Use UltraSSD disks for the VMs in the scale set.</span></span>

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

### <span data-ttu-id="5ba89-165">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="5ba89-165">-EvictionPolicy</span></span>
<span data-ttu-id="5ba89-166">Zasady wykluczenia dla zestawu skali maszyny wirtualnej o niskim priorytecie.</span><span class="sxs-lookup"><span data-stu-id="5ba89-166">The eviction policy for the low priority virtual machine scale set.</span></span>  <span data-ttu-id="5ba89-167">Jedyne obsługiwane wartości to "allocate" i "Delete".</span><span class="sxs-lookup"><span data-stu-id="5ba89-167">Only supported values are 'Deallocate' and 'Delete'.</span></span>

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

### <span data-ttu-id="5ba89-168">-FrontendPoolName</span><span class="sxs-lookup"><span data-stu-id="5ba89-168">-FrontendPoolName</span></span>
<span data-ttu-id="5ba89-169">Nazwa puli adresów frontonu, która ma być używana w usłudze równoważenia obciążenia ustawionej na poziomie skali.</span><span class="sxs-lookup"><span data-stu-id="5ba89-169">The name of the frontend address pool to use in the Scale Set load balancer.</span></span>  <span data-ttu-id="5ba89-170">Jeśli nie podano żadnej wartości, zostanie utworzona nowa pula adresów frontonu o takiej samej nazwie jak ustawiona skala.</span><span class="sxs-lookup"><span data-stu-id="5ba89-170">If no value is supplied, a new Frontend Address Pool will be created, with the same name as the scale set.</span></span>

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

### <span data-ttu-id="5ba89-171">-ImageName</span><span class="sxs-lookup"><span data-stu-id="5ba89-171">-ImageName</span></span>
<span data-ttu-id="5ba89-172">Nazwa obrazu maszyny wirtualnej w tym zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="5ba89-172">The name of the image for VMs in this Scale Set.</span></span> <span data-ttu-id="5ba89-173">Jeśli nie podano żadnej wartości, zostanie wykorzystany obraz "Windows Server 2016 DataCenter".</span><span class="sxs-lookup"><span data-stu-id="5ba89-173">If no value is provided, the "Windows Server 2016 DataCenter" image will be used.</span></span>

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

### <span data-ttu-id="5ba89-174">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="5ba89-174">-InstanceCount</span></span>
<span data-ttu-id="5ba89-175">Liczba obrazów maszyny wirtualnej w zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="5ba89-175">The number of VM images in the Scale Set.</span></span>  <span data-ttu-id="5ba89-176">Jeśli nie podano żadnej wartości, zostaną utworzone 2 wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="5ba89-176">If no value is provided, 2 instances will be created.</span></span>

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

### <span data-ttu-id="5ba89-177">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="5ba89-177">-LoadBalancerName</span></span>
<span data-ttu-id="5ba89-178">Nazwa modułu równoważenia obciążenia do użycia z tym zestawem skali.</span><span class="sxs-lookup"><span data-stu-id="5ba89-178">The name of the load balancer to use with this Scale Set.</span></span>  <span data-ttu-id="5ba89-179">Jeśli nie zostanie określona żadna wartość, zostanie utworzona nowa usługa równoważenia obciążenia z tą samą nazwą co zestaw skali.</span><span class="sxs-lookup"><span data-stu-id="5ba89-179">A new load balancer using the same name as the Scale Set will be created if no value is specified.</span></span>

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

### <span data-ttu-id="5ba89-180">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="5ba89-180">-Location</span></span>
<span data-ttu-id="5ba89-181">Lokalizacja platformy Azure, w której zostanie utworzony ten zestaw skali.</span><span class="sxs-lookup"><span data-stu-id="5ba89-181">The Azure location where this Scale Set will be created.</span></span>  <span data-ttu-id="5ba89-182">Jeśli nie podano żadnej wartości, lokalizacja zostanie wywnioskowana z lokalizacji innych zasobów, do których odwołuje się parametr.</span><span class="sxs-lookup"><span data-stu-id="5ba89-182">If no value is specified, the location will be inferred from the location of other resources referenced in the parameters.</span></span>

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

### <span data-ttu-id="5ba89-183">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="5ba89-183">-MaxPrice</span></span>
<span data-ttu-id="5ba89-184">Maksymalna cena rozliczeń zestawu skali maszyny wirtualnej o niskim priorytecie.</span><span class="sxs-lookup"><span data-stu-id="5ba89-184">The max price of the billing of a low priority virtual machine scale set.</span></span>

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

### <span data-ttu-id="5ba89-185">-NatBackendPort</span><span class="sxs-lookup"><span data-stu-id="5ba89-185">-NatBackendPort</span></span>
<span data-ttu-id="5ba89-186">Port zaplecza translacji adresów sieciowych.</span><span class="sxs-lookup"><span data-stu-id="5ba89-186">Backend port for inbound network address translation.</span></span>

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

### <span data-ttu-id="5ba89-187">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="5ba89-187">-Priority</span></span>
<span data-ttu-id="5ba89-188">Priorytet zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5ba89-188">The priority for the virtual machine scale set.</span></span>  <span data-ttu-id="5ba89-189">Obsługiwane są tylko wartości "zwykła" i "niskie".</span><span class="sxs-lookup"><span data-stu-id="5ba89-189">Only supported values are 'Regular' and 'Low'.</span></span>

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

### <span data-ttu-id="5ba89-190">-ProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="5ba89-190">-ProximityPlacementGroup</span></span>
<span data-ttu-id="5ba89-191">Nazwa lub identyfikator zasobu grupy położenia zbliżeniowe do użycia z tym zestawem skali.</span><span class="sxs-lookup"><span data-stu-id="5ba89-191">The name or resource id of the Proximity Placement Group to use with this Scale Set.</span></span>

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

### <span data-ttu-id="5ba89-192">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="5ba89-192">-PublicIpAddressName</span></span>
<span data-ttu-id="5ba89-193">Nazwa publicznego adresu IP, który ma być używany z tym zestawem skali.</span><span class="sxs-lookup"><span data-stu-id="5ba89-193">The name of the public IP Address to use with this scale set.</span></span>  <span data-ttu-id="5ba89-194">Jeśli nie zostanie podana żadna wartość, zostanie utworzony nowy publiczny adres IP o takiej samej nazwie jak zestaw skali.</span><span class="sxs-lookup"><span data-stu-id="5ba89-194">A new Public IPAddress with the same name as the Scale Set will be created if no value is provided.</span></span>

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

### <span data-ttu-id="5ba89-195">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ba89-195">-ResourceGroupName</span></span>
<span data-ttu-id="5ba89-196">Określa nazwę grupy zasobów VMSS.</span><span class="sxs-lookup"><span data-stu-id="5ba89-196">Specifies the name of the resource group of the VMSS.</span></span>  <span data-ttu-id="5ba89-197">Jeśli nie podano żadnej wartości, zostanie utworzony nowy element resourceName o tej samej nazwie co zestaw skali.</span><span class="sxs-lookup"><span data-stu-id="5ba89-197">If no value is specified, a new ResourceGroup will be created using the same name as the Scale Set.</span></span>

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

### <span data-ttu-id="5ba89-198">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="5ba89-198">-SecurityGroupName</span></span>
<span data-ttu-id="5ba89-199">Nazwa grupy zabezpieczeń sieci do zastosowania do tego zestawu skali.</span><span class="sxs-lookup"><span data-stu-id="5ba89-199">The name of the network security group to apply to this Scale Set.</span></span>  <span data-ttu-id="5ba89-200">Jeśli nie podano żadnej wartości, zostanie utworzona i zastosowana domyślna grupa zabezpieczeń sieci z tą samą nazwą co zestaw skali.</span><span class="sxs-lookup"><span data-stu-id="5ba89-200">If no value is provided, a default network security group with the same name as the Scale Set will be created and applied to the Scale Set.</span></span>

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

### <span data-ttu-id="5ba89-201">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="5ba89-201">-SinglePlacementGroup</span></span>
<span data-ttu-id="5ba89-202">Za pomocą tej pozycji można utworzyć zestaw skali w jednej grupie położenia, domyślnie jest to wiele grup</span><span class="sxs-lookup"><span data-stu-id="5ba89-202">Use this to create the Scale set in a single placement group, default is multiple groups</span></span>

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

### <span data-ttu-id="5ba89-203">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="5ba89-203">-SubnetAddressPrefix</span></span>
<span data-ttu-id="5ba89-204">Prefiks adresu podsieci, który będzie używany przez tę ScaleSet.</span><span class="sxs-lookup"><span data-stu-id="5ba89-204">The address prefix of the Subnet this ScaleSet will use.</span></span> <span data-ttu-id="5ba89-205">Domyślne ustawienia podsieci (192.168.1.0/24) zostaną zastosowane, jeśli nie podano żadnej wartości.</span><span class="sxs-lookup"><span data-stu-id="5ba89-205">Default Subnet settings (192.168.1.0/24) will be applied if no value is provided.</span></span>

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

### <span data-ttu-id="5ba89-206">-Subnetname</span><span class="sxs-lookup"><span data-stu-id="5ba89-206">-SubnetName</span></span>
<span data-ttu-id="5ba89-207">Nazwa podsieci do użycia z tym zestawem skali.</span><span class="sxs-lookup"><span data-stu-id="5ba89-207">The name of the subnet to use with this Scale Set.</span></span>  <span data-ttu-id="5ba89-208">Zostanie utworzona nowa podsieć o takiej samej nazwie jak skala ustawiona, jeśli nie podano żadnej wartości.</span><span class="sxs-lookup"><span data-stu-id="5ba89-208">A new Subnet will be created with the same name as the Scale Set if no value is provided.</span></span>

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

### <span data-ttu-id="5ba89-209">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="5ba89-209">-SystemAssignedIdentity</span></span>
<span data-ttu-id="5ba89-210">Jeśli parametr jest obecny, w przypadku maszyn wirtualnych w zestawie skali jest przypisana automatycznie generowana tożsamość systemu zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="5ba89-210">If the parameter is present then the VM(s) in the scale set is(are) assigned a managed system identity that is auto generated.</span></span>

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

### <span data-ttu-id="5ba89-211">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="5ba89-211">-UpgradePolicyMode</span></span>
<span data-ttu-id="5ba89-212">Tryb zasad uaktualniania dla wystąpień maszyny wirtualnej w tym zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="5ba89-212">The upgrade policy mode for VM instances in this Scale Set.</span></span>  <span data-ttu-id="5ba89-213">Zasady uaktualniania mogą określać uaktualnianie automatyczne, ręczne lub stopniowe.</span><span class="sxs-lookup"><span data-stu-id="5ba89-213">Upgrade policy could specify Automatic, Manual, or Rolling upgrades.</span></span>

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

### <span data-ttu-id="5ba89-214">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="5ba89-214">-UserAssignedIdentity</span></span>
<span data-ttu-id="5ba89-215">Nazwa tożsamości usługi zarządzanej, która powinna być przypisana do maszyn wirtualnych w zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="5ba89-215">The name of a managed service identity that should be assigned to the VM(s) in the scale set.</span></span>

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

### <span data-ttu-id="5ba89-216">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5ba89-216">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="5ba89-217">Określa obiekt **VirtualMachineScaleSet** , który zawiera właściwości VMSS, które tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ba89-217">Specifies the **VirtualMachineScaleSet** object that contains the properties of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="5ba89-218">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="5ba89-218">-VirtualNetworkName</span></span>
<span data-ttu-id="5ba89-219">Nazwa fo sieci wirtualnej do użycia z tym zestawem skali.</span><span class="sxs-lookup"><span data-stu-id="5ba89-219">The name fo the Virtual Network to use with this scale set.</span></span>  <span data-ttu-id="5ba89-220">Jeśli nie podano żadnej wartości, zostanie utworzona nowa sieć wirtualna o takiej samej nazwie jak zestaw skali.</span><span class="sxs-lookup"><span data-stu-id="5ba89-220">If no value is supplied, a new virtual network with the same name as the Scale Set will be created.</span></span>

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

### <span data-ttu-id="5ba89-221">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="5ba89-221">-VMScaleSetName</span></span>
<span data-ttu-id="5ba89-222">Określa nazwę VMSS, które tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ba89-222">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="5ba89-223">-VmSize</span><span class="sxs-lookup"><span data-stu-id="5ba89-223">-VmSize</span></span>
<span data-ttu-id="5ba89-224">Rozmiar wystąpień maszyny wirtualnej w tym zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="5ba89-224">The size of the VM instances in this scale set.</span></span>  <span data-ttu-id="5ba89-225">Jeśli nie określono rozmiaru, zostanie wykorzystana wartość domyślna (Standard_DS1_v2).</span><span class="sxs-lookup"><span data-stu-id="5ba89-225">A default size (Standard_DS1_v2) will be used if no Size is specified.</span></span>

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

### <span data-ttu-id="5ba89-226">-VnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="5ba89-226">-VnetAddressPrefix</span></span>
<span data-ttu-id="5ba89-227">Prefiks adresu sieci wirtualnej używanej z tym zestawem skali.</span><span class="sxs-lookup"><span data-stu-id="5ba89-227">The address prefix for the virtual network used with this Scale Set.</span></span>  <span data-ttu-id="5ba89-228">Jeśli nie zostanie podana żadna wartość, zostanie użyty domyślny prefiks adresu sieci wirtualnej (192.168.0.0/16).</span><span class="sxs-lookup"><span data-stu-id="5ba89-228">Default virtual network address prefix settings (192.168.0.0/16) will be used if no value is supplied.</span></span>

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

### <span data-ttu-id="5ba89-229">-Zone</span><span class="sxs-lookup"><span data-stu-id="5ba89-229">-Zone</span></span>
<span data-ttu-id="5ba89-230">Lista stref dostępności oznaczająca adres IP przydzielony dla zasobu musi pochodzić od.</span><span class="sxs-lookup"><span data-stu-id="5ba89-230">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="5ba89-231">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5ba89-231">-Confirm</span></span>
<span data-ttu-id="5ba89-232">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ba89-232">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ba89-233">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ba89-233">-WhatIf</span></span>
<span data-ttu-id="5ba89-234">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ba89-234">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ba89-235">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5ba89-235">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ba89-236">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ba89-236">CommonParameters</span></span>
<span data-ttu-id="5ba89-237">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ba89-237">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ba89-238">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ba89-238">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ba89-239">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ba89-239">INPUTS</span></span>

### <span data-ttu-id="5ba89-240">System. String</span><span class="sxs-lookup"><span data-stu-id="5ba89-240">System.String</span></span>

### <span data-ttu-id="5ba89-241">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5ba89-241">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="5ba89-242">System. Collections. Generic. list "1 [[System. String; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5ba89-242">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="5ba89-243">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5ba89-243">OUTPUTS</span></span>

### <span data-ttu-id="5ba89-244">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5ba89-244">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="5ba89-245">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5ba89-245">NOTES</span></span>

## <span data-ttu-id="5ba89-246">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ba89-246">RELATED LINKS</span></span>

[<span data-ttu-id="5ba89-247">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="5ba89-247">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="5ba89-248">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="5ba89-248">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="5ba89-249">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="5ba89-249">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="5ba89-250">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="5ba89-250">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="5ba89-251">Start — AzVmss</span><span class="sxs-lookup"><span data-stu-id="5ba89-251">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="5ba89-252">Zatrzymaj — AzVmss</span><span class="sxs-lookup"><span data-stu-id="5ba89-252">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="5ba89-253">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="5ba89-253">Update-AzVmss</span></span>](./Update-AzVmss.md)


