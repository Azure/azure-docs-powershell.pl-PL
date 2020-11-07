---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
ms.openlocfilehash: 97e10d75d17748f1a9e96ada498afe456700f61d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869004"
---
# <span data-ttu-id="15776-101">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="15776-101">New-AzVmss</span></span>

## <span data-ttu-id="15776-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="15776-102">SYNOPSIS</span></span>
<span data-ttu-id="15776-103">Tworzy VMSS.</span><span class="sxs-lookup"><span data-stu-id="15776-103">Creates a VMSS.</span></span>

## <span data-ttu-id="15776-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="15776-104">SYNTAX</span></span>

### <span data-ttu-id="15776-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="15776-105">DefaultParameter (Default)</span></span>
```
New-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15776-106">SimpleParameterSet</span><span class="sxs-lookup"><span data-stu-id="15776-106">SimpleParameterSet</span></span>
```
New-AzVmss [[-ResourceGroupName] <String>] [-VMScaleSetName] <String> [-AsJob] [-ImageName <String>]
 -Credential <PSCredential> [-InstanceCount <Int32>] [-VirtualNetworkName <String>] [-SubnetName <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-SecurityGroupName <String>]
 [-LoadBalancerName <String>] [-BackendPort <Int32[]>] [-Location <String>] [-VmSize <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-AllocationMethod <String>] [-VnetAddressPrefix <String>]
 [-SubnetAddressPrefix <String>] [-FrontendPoolName <String>] [-BackendPoolName <String>]
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-EnableUltraSSD]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-NatBackendPort <Int32[]>]
 [-DataDiskSizeInGb <Int32[]>] [-DefaultProfile <IAzureContextContainer>] [-SinglePlacementGroup] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15776-107">Opis</span><span class="sxs-lookup"><span data-stu-id="15776-107">DESCRIPTION</span></span>
<span data-ttu-id="15776-108">Polecenie cmdlet **New-AzVmss** umożliwia utworzenie zestawu skali maszyny wirtualnej (VMSS) na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="15776-108">The **New-AzVmss** cmdlet creates a Virtual Machine Scale Set (VMSS) in Azure.</span></span>
<span data-ttu-id="15776-109">Użyj prostego zestawu parametrów ( `SimpleParameterSet` ), aby szybko utworzyć wstępnie ustawiony VMSS i skojarzone zasoby.</span><span class="sxs-lookup"><span data-stu-id="15776-109">Use the simple parameter set (`SimpleParameterSet`) to quickly create a pre-set VMSS and associated resources.</span></span> <span data-ttu-id="15776-110">Użyj domyślnego zestawu parametrów ( `DefaultParameter` ), aby bardziej zaawansowane scenariusze można było precyzyjnie skonfigurować poszczególne składniki VMSS oraz wszystkie skojarzone z nimi zasoby przed utworzeniem.</span><span class="sxs-lookup"><span data-stu-id="15776-110">Use the default parameter set (`DefaultParameter`) for more advanced scenarios when you need to precisely configure each component of the VMSS and each associated resource before creation.</span></span>

## <span data-ttu-id="15776-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="15776-111">EXAMPLES</span></span>

### <span data-ttu-id="15776-112">Przykład 1. Tworzenie VMSS przy użyciu **`SimpleParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="15776-112">Example 1: Create a VMSS using the **`SimpleParameterSet`**</span></span>
```powershell
$vmssName = <VMSSNAME>
# Create credentials, I am using one way to create credentials, there are others as well. 
# Pick one that makes the most sense according to your use case.
$vmPassword = ConvertTo-SecureString <PASSWORD_HERE> -AsPlainText -Force
$vmCred = New-Object System.Management.Automation.PSCredential(<USERNAME_HERE>, $vmPassword)

#Create a VMSS using the default settings
New-AzVmss -Credential $vmCred -VMScaleSetName $vmssName
```

<span data-ttu-id="15776-113">W powyższym poleceniu zostanie utworzona następująca nazwa `$vmssName` :</span><span class="sxs-lookup"><span data-stu-id="15776-113">The command above creates the following with the name `$vmssName` :</span></span>
* <span data-ttu-id="15776-114">Grupa zasobów</span><span class="sxs-lookup"><span data-stu-id="15776-114">A Resource Group</span></span>
* <span data-ttu-id="15776-115">Sieć wirtualna</span><span class="sxs-lookup"><span data-stu-id="15776-115">A virtual network</span></span>
* <span data-ttu-id="15776-116">Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="15776-116">A load balancer</span></span>
* <span data-ttu-id="15776-117">Publiczny adres IP</span><span class="sxs-lookup"><span data-stu-id="15776-117">A public IP</span></span>
* <span data-ttu-id="15776-118">VMSS z dwoma wystąpieniami</span><span class="sxs-lookup"><span data-stu-id="15776-118">the VMSS with 2 instances</span></span>

<span data-ttu-id="15776-119">Domyślnym obrazem wybranym dla maszyn wirtualnych w VMSS jest `2016-Datacenter Windows Server` , a wersja SKU to `Standard_DS1_v2`</span><span class="sxs-lookup"><span data-stu-id="15776-119">The default image chosen for the VMs in the VMSS is `2016-Datacenter Windows Server` and the SKU is `Standard_DS1_v2`</span></span>

### <span data-ttu-id="15776-120">Przykład 2: Tworzenie VMSS przy użyciu **`DefaultParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="15776-120">Example 2: Create a VMSS using the **`DefaultParameterSet`**</span></span>
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

<span data-ttu-id="15776-121">W złożonym przykładzie powyżej powstaje VMSS, poniżej przedstawiono wyjaśnienie, co się dzieje:</span><span class="sxs-lookup"><span data-stu-id="15776-121">The complex example above creates a VMSS, following is an explanation of what is happening:</span></span>
* <span data-ttu-id="15776-122">Pierwsze polecenie tworzy grupę zasobów o określonej nazwie i lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="15776-122">The first command creates a resource group with the specified name and location.</span></span>
* <span data-ttu-id="15776-123">Drugie polecenie używa polecenia cmdlet **New-AzStorageAccount** w celu utworzenia konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="15776-123">The second command uses the **New-AzStorageAccount** cmdlet to create a storage account.</span></span>
* <span data-ttu-id="15776-124">Trzecia komenda używa polecenia cmdlet **Get-AzStorageAccount** w celu uzyskania konta magazynu utworzonego w drugim poleceniu i zapisanie wyniku w zmiennej $STOAccount.</span><span class="sxs-lookup"><span data-stu-id="15776-124">The third command then uses the **Get-AzStorageAccount** cmdlet to get the storage account created in the second command and stores the result in the $STOAccount variable.</span></span>
* <span data-ttu-id="15776-125">W piątym poleceniu użyto polecenia cmdlet **New-AzVirtualNetworkSubnetConfig** w celu utworzenia podsieci i zapisanie wyniku w zmiennej o nazwie $Subnet.</span><span class="sxs-lookup"><span data-stu-id="15776-125">The fifth command uses the **New-AzVirtualNetworkSubnetConfig** cmdlet to create a subnet and stores the result in the variable named $SubNet.</span></span>
* <span data-ttu-id="15776-126">W szóstym poleceniu użyto polecenia cmdlet **New-AzVirtualNetwork** w celu utworzenia sieci wirtualnej i zapisu wyniku w zmiennej o nazwie $VNET.</span><span class="sxs-lookup"><span data-stu-id="15776-126">The sixth command uses the **New-AzVirtualNetwork** cmdlet to create a virtual network and stores the result in the variable named $VNet.</span></span>
* <span data-ttu-id="15776-127">W przypadku siódmego polecenia w celu uzyskania informacji o sieci wirtualnej utworzonej w szóstym poleceniu jest używane polecenie **Get-AzVirtualNetwork** , a informacje są przechowywane w zmiennej o nazwie $VNET.</span><span class="sxs-lookup"><span data-stu-id="15776-127">The seventh command uses the **Get-AzVirtualNetwork** to get information about the virtual network created in the sixth command and stores the information in the variable named $VNet.</span></span>
* <span data-ttu-id="15776-128">W przypadku ośmiu i Dziewiątych poleceń do tworzenia i pobierania informacji z tego publicznego adresu IP użyto polecenia **New-AzPublicIpAddress** i **Get-AzureRmPublicIpAddress** .</span><span class="sxs-lookup"><span data-stu-id="15776-128">The eighth and ninth command uses the **New-AzPublicIpAddress** and **Get- AzureRmPublicIpAddress** to create and get information from that public IP address.</span></span>
* <span data-ttu-id="15776-129">Te polecenia przechowują informacje w zmiennej o nazwie $PubIP.</span><span class="sxs-lookup"><span data-stu-id="15776-129">The commands store the information in the variable named $PubIP.</span></span>
* <span data-ttu-id="15776-130">W poleceniu dziesiątym użyto polecenia cmdlet **New-AzureRmLoadBalancerFrontendIpConfig** w celu utworzenia modułu równoważenia obciążenia frontonu i zapisu wyniku w zmiennej o nazwie $frontend.</span><span class="sxs-lookup"><span data-stu-id="15776-130">The tenth command uses the **New- AzureRmLoadBalancerFrontendIpConfig** cmdlet to create a frontend load balancer and stores the result in the variable named $Frontend.</span></span>
* <span data-ttu-id="15776-131">W jedenastym poleceniu użyto polecenia **New-AzLoadBalancerBackendAddressPoolConfig** w celu utworzenia konfiguracji puli adresów zaplecza i zapisu wyniku w zmiennej o nazwie $BackendAddressPool.</span><span class="sxs-lookup"><span data-stu-id="15776-131">The eleventh command uses the **New-AzLoadBalancerBackendAddressPoolConfig** to create a backend address pool configuration and stores the result in the variable named $BackendAddressPool.</span></span>
* <span data-ttu-id="15776-132">W poleceniu dwunasta jest używana funkcja **New-AzLoadBalancerProbeConfig** w celu utworzenia sondy i zapisanie informacji dotyczących sondy w zmiennej o nazwie $Probe.</span><span class="sxs-lookup"><span data-stu-id="15776-132">The twelfth command uses the **New-AzLoadBalancerProbeConfig** to create a probe and stores the probe information in the variable named $Probe.</span></span>
* <span data-ttu-id="15776-133">Polecenie trzynaste używa polecenia cmdlet **New-AzLoadBalancerInboundNatPoolConfig** w celu utworzenia konfiguracji puli NAT (Network Address Translation) modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="15776-133">The thirteenth command uses the **New-AzLoadBalancerInboundNatPoolConfig** cmdlet to create a load balancer inbound network address translation (NAT) pool configuration.</span></span>
* <span data-ttu-id="15776-134">Polecenie czternaste używa polecenia **New-AzLoadBalancerRuleConfig** w celu utworzenia konfiguracji reguł modułu równoważenia obciążenia i zapisu wyniku w zmiennej o nazwie $LBRule.</span><span class="sxs-lookup"><span data-stu-id="15776-134">The fourteenth command uses the **New-AzLoadBalancerRuleConfig** to create a load balancer rule configuration and stores the result in the variable named $LBRule.</span></span>
* <span data-ttu-id="15776-135">W poleceniu piętnaste polecenie cmdlet **New-AzLoadBalancer** jest używane do utworzenia modułu równoważenia obciążenia i zapisuje wynik w zmiennej o nazwie $ActualLb.</span><span class="sxs-lookup"><span data-stu-id="15776-135">The fifteenth command uses the **New-AzLoadBalancer** cmdlet to create a load balancer and stores the result in the variable named $ActualLb.</span></span>
* <span data-ttu-id="15776-136">Polecenie szesnaste używa polecenia **Get-AzLoadBalancer** w celu uzyskania informacji na temat modułu równoważenia obciążenia utworzonego w piętnastym poleceniu i zapisanie informacji w zmiennej o nazwie $ExpectedLb.</span><span class="sxs-lookup"><span data-stu-id="15776-136">The sixteenth command uses the **Get-AzLoadBalancer** to get information about the load balancer that was created in the fifteenth command and stores the information in the variable named $ExpectedLb.</span></span>
* <span data-ttu-id="15776-137">W poleceniu siedemnasta użyto polecenia cmdlet **New-AzVmssIPConfig** w celu utworzenia VMSS konfiguracji adresu IP i zapisu informacji w zmiennej o nazwie $IPCfg.</span><span class="sxs-lookup"><span data-stu-id="15776-137">The seventeenth command uses the **New-AzVmssIPConfig** cmdlet to create a VMSS IP configuration and stores the information in the variable named $IPCfg.</span></span>
* <span data-ttu-id="15776-138">Polecenie osiemnastym miesiącem korzysta z polecenia cmdlet **New-AzVmssConfig** w celu utworzenia obiektu konfiguracji VMSS i zapisanie wyniku w zmiennej o nazwie $VMSS.</span><span class="sxs-lookup"><span data-stu-id="15776-138">The eighteenth command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
* <span data-ttu-id="15776-139">W poleceniu XIX użyto polecenia cmdlet **New-AzVmss** w celu utworzenia VMSS.</span><span class="sxs-lookup"><span data-stu-id="15776-139">The nineteenth command uses the **New-AzVmss** cmdlet to create the VMSS.</span></span>

## <span data-ttu-id="15776-140">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="15776-140">PARAMETERS</span></span>

### <span data-ttu-id="15776-141">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="15776-141">-AllocationMethod</span></span>
<span data-ttu-id="15776-142">Metoda alokacji dla publicznego adresu IP zestawu skali (statycznego lub dynamicznego).</span><span class="sxs-lookup"><span data-stu-id="15776-142">Allocation method for the Public IP Address of the Scale Set (Static or Dynamic).</span></span>  <span data-ttu-id="15776-143">Jeśli nie podano żadnej wartości, alokacja będzie statyczna.</span><span class="sxs-lookup"><span data-stu-id="15776-143">If no value is supplied, allocation will be static.</span></span>

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

### <span data-ttu-id="15776-144">-AsJob</span><span class="sxs-lookup"><span data-stu-id="15776-144">-AsJob</span></span>
<span data-ttu-id="15776-145">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="15776-145">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="15776-146">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="15776-146">-BackendPoolName</span></span>
<span data-ttu-id="15776-147">Nazwa puli adresów zaplecza, która ma być używana w usłudze równoważenia obciążenia dla tego zestawu skali.</span><span class="sxs-lookup"><span data-stu-id="15776-147">The name of the backend address pool to use in the load balancer for this Scale Set.</span></span>  <span data-ttu-id="15776-148">Jeśli nie podano żadnej wartości, zostanie utworzona nowa pula zaplecza z tą samą nazwą co zestaw skali.</span><span class="sxs-lookup"><span data-stu-id="15776-148">If no value is provided, a new backend pool will be created, with the same name as the Scale Set.</span></span>

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

### <span data-ttu-id="15776-149">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="15776-149">-BackendPort</span></span>
<span data-ttu-id="15776-150">Numery portów zaplecza używane przez moduł skalowania, ustawiony w celu komunikowania się z maszynami wirtualnymi w zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="15776-150">Backend port numbers used by the Scale Set load balancer to communicate with VMs in the Scale Set.</span></span>  <span data-ttu-id="15776-151">Jeśli nie określono żadnych wartości, porty 3389 i 5985 będą używane na potrzeby maszyn wirtualnych systemu Windows, a w przypadku maszyn wirtualnych Linux będzie używana wartość port 22.</span><span class="sxs-lookup"><span data-stu-id="15776-151">If no values are specified, ports 3389 and 5985 will be used for Windows VMS, and port 22 will be used for Linux VMs.</span></span>

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

### <span data-ttu-id="15776-152">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="15776-152">-Credential</span></span>
<span data-ttu-id="15776-153">Poświadczenia administratora (nazwa użytkownika i hasło) dla maszyn wirtualnych w tym zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="15776-153">The administrator credentials (username and password) for VMs in this Scale Set.</span></span>

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

### <span data-ttu-id="15776-154">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="15776-154">-DataDiskSizeInGb</span></span>
<span data-ttu-id="15776-155">Określa rozmiary dysków z danymi w GB.</span><span class="sxs-lookup"><span data-stu-id="15776-155">Specifies the sizes of data disks in GB.</span></span>

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

### <span data-ttu-id="15776-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15776-156">-DefaultProfile</span></span>
<span data-ttu-id="15776-157">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="15776-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15776-158">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="15776-158">-DomainNameLabel</span></span>
<span data-ttu-id="15776-159">Etykieta nazwy domeny dla publicznej nazwy domeny Fully-Qualified (FQDN) dla tego zestawu skali.</span><span class="sxs-lookup"><span data-stu-id="15776-159">The domain name label for the public Fully-Qualified domain name (FQDN) for this Scale Set.</span></span> <span data-ttu-id="15776-160">Jest to pierwszy składnik nazwy domeny, który jest automatycznie przypisywany do zestawu skali.</span><span class="sxs-lookup"><span data-stu-id="15776-160">This is the first component of the domain name that is automatically assigned to the Scale Set.</span></span> <span data-ttu-id="15776-161">Automatycznie przypisane nazwy domen używają formularza ( <DomainNameLabel> . <Location> . cloudapp.azure.com).</span><span class="sxs-lookup"><span data-stu-id="15776-161">Automatically assigned Domain names use the form (<DomainNameLabel>.<Location>.cloudapp.azure.com).</span></span> <span data-ttu-id="15776-162">Jeśli nie zostanie podana żadna wartość, domyślna etykieta nazwy domeny będzie łączyć się z <ScaleSetName> i <ResourceGroupName> .</span><span class="sxs-lookup"><span data-stu-id="15776-162">If no value is supplied, the default domain name label will be the concatenation of <ScaleSetName> and <ResourceGroupName>.</span></span>

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

### <span data-ttu-id="15776-163">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="15776-163">-EnableUltraSSD</span></span>
<span data-ttu-id="15776-164">Użyj dysków UltraSSD dla maszyn wirtualnych w zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="15776-164">Use UltraSSD disks for the VMs in the scale set.</span></span>

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

### <span data-ttu-id="15776-165">-FrontendPoolName</span><span class="sxs-lookup"><span data-stu-id="15776-165">-FrontendPoolName</span></span>
<span data-ttu-id="15776-166">Nazwa puli adresów frontonu, która ma być używana w usłudze równoważenia obciążenia ustawionej na poziomie skali.</span><span class="sxs-lookup"><span data-stu-id="15776-166">The name of the frontend address pool to use in the Scale Set load balancer.</span></span>  <span data-ttu-id="15776-167">Jeśli nie podano żadnej wartości, zostanie utworzona nowa pula adresów frontonu o takiej samej nazwie jak ustawiona skala.</span><span class="sxs-lookup"><span data-stu-id="15776-167">If no value is supplied, a new Frontend Address Pool will be created, with the same name as the scale set.</span></span>

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

### <span data-ttu-id="15776-168">-ImageName</span><span class="sxs-lookup"><span data-stu-id="15776-168">-ImageName</span></span>
<span data-ttu-id="15776-169">Nazwa obrazu maszyny wirtualnej w tym zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="15776-169">The name of the image for VMs in this Scale Set.</span></span> <span data-ttu-id="15776-170">Jeśli nie podano żadnej wartości, zostanie wykorzystany obraz "Windows Server 2016 DataCenter".</span><span class="sxs-lookup"><span data-stu-id="15776-170">If no value is provided, the "Windows Server 2016 DataCenter" image will be used.</span></span>

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

### <span data-ttu-id="15776-171">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="15776-171">-InstanceCount</span></span>
<span data-ttu-id="15776-172">Liczba obrazów maszyny wirtualnej w zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="15776-172">The number of VM images in the Scale Set.</span></span>  <span data-ttu-id="15776-173">Jeśli nie podano żadnej wartości, zostaną utworzone 2 wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="15776-173">If no value is provided, 2 instances will be created.</span></span>

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

### <span data-ttu-id="15776-174">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="15776-174">-LoadBalancerName</span></span>
<span data-ttu-id="15776-175">Nazwa modułu równoważenia obciążenia do użycia z tym zestawem skali.</span><span class="sxs-lookup"><span data-stu-id="15776-175">The name of the load balancer to use with this Scale Set.</span></span>  <span data-ttu-id="15776-176">Jeśli nie zostanie określona żadna wartość, zostanie utworzona nowa usługa równoważenia obciążenia z tą samą nazwą co zestaw skali.</span><span class="sxs-lookup"><span data-stu-id="15776-176">A new load balancer using the same name as the Scale Set will be created if no value is specified.</span></span>

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

### <span data-ttu-id="15776-177">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="15776-177">-Location</span></span>
<span data-ttu-id="15776-178">Lokalizacja platformy Azure, w której zostanie utworzony ten zestaw skali.</span><span class="sxs-lookup"><span data-stu-id="15776-178">The Azure location where this Scale Set will be created.</span></span>  <span data-ttu-id="15776-179">Jeśli nie podano żadnej wartości, lokalizacja zostanie wywnioskowana z lokalizacji innych zasobów, do których odwołuje się parametr.</span><span class="sxs-lookup"><span data-stu-id="15776-179">If no value is specified, the location will be inferred from the location of other resources referenced in the parameters.</span></span>

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

### <span data-ttu-id="15776-180">-NatBackendPort</span><span class="sxs-lookup"><span data-stu-id="15776-180">-NatBackendPort</span></span>
<span data-ttu-id="15776-181">Port zaplecza translacji adresów sieciowych.</span><span class="sxs-lookup"><span data-stu-id="15776-181">Backend port for inbound network address translation.</span></span>

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

### <span data-ttu-id="15776-182">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="15776-182">-PublicIpAddressName</span></span>
<span data-ttu-id="15776-183">Nazwa publicznego adresu IP, który ma być używany z tym zestawem skali.</span><span class="sxs-lookup"><span data-stu-id="15776-183">The name of the public IP Address to use with this scale set.</span></span>  <span data-ttu-id="15776-184">Jeśli nie zostanie podana żadna wartość, zostanie utworzony nowy publiczny adres IP o takiej samej nazwie jak zestaw skali.</span><span class="sxs-lookup"><span data-stu-id="15776-184">A new Public IPAddress with the same name as the Scale Set will be created if no value is provided.</span></span>

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

### <span data-ttu-id="15776-185">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15776-185">-ResourceGroupName</span></span>
<span data-ttu-id="15776-186">Określa nazwę grupy zasobów VMSS.</span><span class="sxs-lookup"><span data-stu-id="15776-186">Specifies the name of the resource group of the VMSS.</span></span>  <span data-ttu-id="15776-187">Jeśli nie podano żadnej wartości, zostanie utworzony nowy element resourceName o tej samej nazwie co zestaw skali.</span><span class="sxs-lookup"><span data-stu-id="15776-187">If no value is specified, a new ResourceGroup will be created using the same name as the Scale Set.</span></span>

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

### <span data-ttu-id="15776-188">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="15776-188">-SecurityGroupName</span></span>
<span data-ttu-id="15776-189">Nazwa grupy zabezpieczeń sieci do zastosowania do tego zestawu skali.</span><span class="sxs-lookup"><span data-stu-id="15776-189">The name of the network security group to apply to this Scale Set.</span></span>  <span data-ttu-id="15776-190">Jeśli nie podano żadnej wartości, zostanie utworzona i zastosowana domyślna grupa zabezpieczeń sieci z tą samą nazwą co zestaw skali.</span><span class="sxs-lookup"><span data-stu-id="15776-190">If no value is provided, a default network security group with the same name as the Scale Set will be created and applied to the Scale Set.</span></span>

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

### <span data-ttu-id="15776-191">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="15776-191">-SinglePlacementGroup</span></span>
<span data-ttu-id="15776-192">Za pomocą tej pozycji można utworzyć zestaw skali w jednej grupie położenia, domyślnie jest to wiele grup</span><span class="sxs-lookup"><span data-stu-id="15776-192">Use this to create the Scale set in a single placement group, default is multiple groups</span></span>

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

### <span data-ttu-id="15776-193">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="15776-193">-SubnetAddressPrefix</span></span>
<span data-ttu-id="15776-194">Prefiks adresu podsieci, który będzie używany przez tę ScaleSet.</span><span class="sxs-lookup"><span data-stu-id="15776-194">The address prefix of the Subnet this ScaleSet will use.</span></span> <span data-ttu-id="15776-195">Domyślne ustawienia podsieci (192.168.1.0/24) zostaną zastosowane, jeśli nie podano żadnej wartości.</span><span class="sxs-lookup"><span data-stu-id="15776-195">Default Subnet settings (192.168.1.0/24) will be applied if no value is provided.</span></span>

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

### <span data-ttu-id="15776-196">-Subnetname</span><span class="sxs-lookup"><span data-stu-id="15776-196">-SubnetName</span></span>
<span data-ttu-id="15776-197">Nazwa podsieci do użycia z tym zestawem skali.</span><span class="sxs-lookup"><span data-stu-id="15776-197">The name of the subnet to use with this Scale Set.</span></span>  <span data-ttu-id="15776-198">Zostanie utworzona nowa podsieć o takiej samej nazwie jak skala ustawiona, jeśli nie podano żadnej wartości.</span><span class="sxs-lookup"><span data-stu-id="15776-198">A new Subnet will be created with the same name as the Scale Set if no value is provided.</span></span>

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

### <span data-ttu-id="15776-199">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="15776-199">-SystemAssignedIdentity</span></span>
<span data-ttu-id="15776-200">Jeśli parametr jest obecny, w przypadku maszyn wirtualnych w zestawie skali jest przypisana automatycznie generowana tożsamość systemu zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="15776-200">If the parameter is present then the VM(s) in the scale set is(are) assigned a managed system identity that is auto generated.</span></span>

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

### <span data-ttu-id="15776-201">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="15776-201">-UpgradePolicyMode</span></span>
<span data-ttu-id="15776-202">Tryb zasad uaktualniania dla wystąpień maszyny wirtualnej w tym zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="15776-202">The upgrade policy mode for VM instances in this Scale Set.</span></span>  <span data-ttu-id="15776-203">Zasady uaktualniania mogą określać uaktualnianie automatyczne, ręczne lub stopniowe.</span><span class="sxs-lookup"><span data-stu-id="15776-203">Upgrade policy could specify Automatic, Manual, or Rolling upgrades.</span></span>

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

### <span data-ttu-id="15776-204">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="15776-204">-UserAssignedIdentity</span></span>
<span data-ttu-id="15776-205">Nazwa tożsamości usługi zarządzanej, która powinna być przypisana do maszyn wirtualnych w zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="15776-205">The name of a managed service identity that should be assigned to the VM(s) in the scale set.</span></span>

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

### <span data-ttu-id="15776-206">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="15776-206">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="15776-207">Określa obiekt **VirtualMachineScaleSet** , który zawiera właściwości VMSS, które tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15776-207">Specifies the **VirtualMachineScaleSet** object that contains the properties of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="15776-208">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="15776-208">-VirtualNetworkName</span></span>
<span data-ttu-id="15776-209">Nazwa fo sieci wirtualnej do użycia z tym zestawem skali.</span><span class="sxs-lookup"><span data-stu-id="15776-209">The name fo the Virtual Network to use with this scale set.</span></span>  <span data-ttu-id="15776-210">Jeśli nie podano żadnej wartości, zostanie utworzona nowa sieć wirtualna o takiej samej nazwie jak zestaw skali.</span><span class="sxs-lookup"><span data-stu-id="15776-210">If no value is supplied, a new virtual network with the same name as the Scale Set will be created.</span></span>

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

### <span data-ttu-id="15776-211">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="15776-211">-VMScaleSetName</span></span>
<span data-ttu-id="15776-212">Określa nazwę VMSS, które tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15776-212">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="15776-213">-VmSize</span><span class="sxs-lookup"><span data-stu-id="15776-213">-VmSize</span></span>
<span data-ttu-id="15776-214">Rozmiar wystąpień maszyny wirtualnej w tym zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="15776-214">The size of the VM instances in this scale set.</span></span>  <span data-ttu-id="15776-215">Jeśli nie określono rozmiaru, zostanie wykorzystana wartość domyślna (Standard_DS1_v2).</span><span class="sxs-lookup"><span data-stu-id="15776-215">A default size (Standard_DS1_v2) will be used if no Size is specified.</span></span>

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

### <span data-ttu-id="15776-216">-VnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="15776-216">-VnetAddressPrefix</span></span>
<span data-ttu-id="15776-217">Prefiks adresu sieci wirtualnej używanej z tym zestawem skali.</span><span class="sxs-lookup"><span data-stu-id="15776-217">The address prefix for the virtual network used with this Scale Set.</span></span>  <span data-ttu-id="15776-218">Jeśli nie zostanie podana żadna wartość, zostanie użyty domyślny prefiks adresu sieci wirtualnej (192.168.0.0/16).</span><span class="sxs-lookup"><span data-stu-id="15776-218">Default virtual network address prefix settings (192.168.0.0/16) will be used if no value is supplied.</span></span>

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

### <span data-ttu-id="15776-219">-Zone</span><span class="sxs-lookup"><span data-stu-id="15776-219">-Zone</span></span>
<span data-ttu-id="15776-220">Lista stref dostępności oznaczająca adres IP przydzielony dla zasobu musi pochodzić od.</span><span class="sxs-lookup"><span data-stu-id="15776-220">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="15776-221">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="15776-221">-Confirm</span></span>
<span data-ttu-id="15776-222">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15776-222">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15776-223">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15776-223">-WhatIf</span></span>
<span data-ttu-id="15776-224">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15776-224">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15776-225">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="15776-225">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15776-226">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15776-226">CommonParameters</span></span>
<span data-ttu-id="15776-227">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15776-227">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15776-228">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15776-228">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15776-229">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="15776-229">INPUTS</span></span>

### <span data-ttu-id="15776-230">System. String</span><span class="sxs-lookup"><span data-stu-id="15776-230">System.String</span></span>

### <span data-ttu-id="15776-231">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="15776-231">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="15776-232">System. Collections. Generic. list "1 [[System. String; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="15776-232">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="15776-233">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="15776-233">OUTPUTS</span></span>

### <span data-ttu-id="15776-234">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="15776-234">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="15776-235">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="15776-235">NOTES</span></span>

## <span data-ttu-id="15776-236">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="15776-236">RELATED LINKS</span></span>

[<span data-ttu-id="15776-237">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="15776-237">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="15776-238">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="15776-238">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="15776-239">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="15776-239">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="15776-240">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="15776-240">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="15776-241">Start — AzVmss</span><span class="sxs-lookup"><span data-stu-id="15776-241">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="15776-242">Zatrzymaj — AzVmss</span><span class="sxs-lookup"><span data-stu-id="15776-242">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="15776-243">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="15776-243">Update-AzVmss</span></span>](./Update-AzVmss.md)


