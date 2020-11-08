---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
ms.openlocfilehash: deb33c8e26dcedd96a6cdb3073b9c71f26750abf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064283"
---
# <span data-ttu-id="21cfb-101">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="21cfb-101">New-AzVmss</span></span>

## <span data-ttu-id="21cfb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="21cfb-102">SYNOPSIS</span></span>
<span data-ttu-id="21cfb-103">Tworzy VMSS.</span><span class="sxs-lookup"><span data-stu-id="21cfb-103">Creates a VMSS.</span></span>

## <span data-ttu-id="21cfb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="21cfb-104">SYNTAX</span></span>

### <span data-ttu-id="21cfb-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="21cfb-105">DefaultParameter (Default)</span></span>
```
New-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21cfb-106">SimpleParameterSet</span><span class="sxs-lookup"><span data-stu-id="21cfb-106">SimpleParameterSet</span></span>
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
 [-SkipExtensionsOnOverprovisionedVMs] [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>]
 [-SinglePlacementGroup] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21cfb-107">Opis</span><span class="sxs-lookup"><span data-stu-id="21cfb-107">DESCRIPTION</span></span>
<span data-ttu-id="21cfb-108">Polecenie cmdlet **New-AzVmss** umożliwia utworzenie zestawu skali maszyny wirtualnej (VMSS) na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="21cfb-108">The **New-AzVmss** cmdlet creates a Virtual Machine Scale Set (VMSS) in Azure.</span></span>
<span data-ttu-id="21cfb-109">Użyj prostego zestawu parametrów ( `SimpleParameterSet` ), aby szybko utworzyć wstępnie ustawiony VMSS i skojarzone zasoby.</span><span class="sxs-lookup"><span data-stu-id="21cfb-109">Use the simple parameter set (`SimpleParameterSet`) to quickly create a pre-set VMSS and associated resources.</span></span> <span data-ttu-id="21cfb-110">Użyj domyślnego zestawu parametrów ( `DefaultParameter` ), aby bardziej zaawansowane scenariusze można było precyzyjnie skonfigurować poszczególne składniki VMSS oraz wszystkie skojarzone z nimi zasoby przed utworzeniem.</span><span class="sxs-lookup"><span data-stu-id="21cfb-110">Use the default parameter set (`DefaultParameter`) for more advanced scenarios when you need to precisely configure each component of the VMSS and each associated resource before creation.</span></span>

## <span data-ttu-id="21cfb-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="21cfb-111">EXAMPLES</span></span>

### <span data-ttu-id="21cfb-112">Przykład 1. Tworzenie VMSS przy użyciu **`SimpleParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="21cfb-112">Example 1: Create a VMSS using the **`SimpleParameterSet`**</span></span>
```powershell
$vmssName = <VMSSNAME>
# Create credentials, I am using one way to create credentials, there are others as well. 
# Pick one that makes the most sense according to your use case.
$vmPassword = ConvertTo-SecureString <PASSWORD_HERE> -AsPlainText -Force
$vmCred = New-Object System.Management.Automation.PSCredential(<USERNAME_HERE>, $vmPassword)

#Create a VMSS using the default settings
New-AzVmss -Credential $vmCred -VMScaleSetName $vmssName
```

<span data-ttu-id="21cfb-113">W powyższym poleceniu zostanie utworzona następująca nazwa `$vmssName` :</span><span class="sxs-lookup"><span data-stu-id="21cfb-113">The command above creates the following with the name `$vmssName` :</span></span>
* <span data-ttu-id="21cfb-114">Grupa zasobów</span><span class="sxs-lookup"><span data-stu-id="21cfb-114">A Resource Group</span></span>
* <span data-ttu-id="21cfb-115">Sieć wirtualna</span><span class="sxs-lookup"><span data-stu-id="21cfb-115">A virtual network</span></span>
* <span data-ttu-id="21cfb-116">Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="21cfb-116">A load balancer</span></span>
* <span data-ttu-id="21cfb-117">Publiczny adres IP</span><span class="sxs-lookup"><span data-stu-id="21cfb-117">A public IP</span></span>
* <span data-ttu-id="21cfb-118">VMSS z dwoma wystąpieniami</span><span class="sxs-lookup"><span data-stu-id="21cfb-118">the VMSS with 2 instances</span></span>

<span data-ttu-id="21cfb-119">Domyślnym obrazem wybranym dla maszyn wirtualnych w VMSS jest `2016-Datacenter Windows Server` , a wersja SKU to `Standard_DS1_v2`</span><span class="sxs-lookup"><span data-stu-id="21cfb-119">The default image chosen for the VMs in the VMSS is `2016-Datacenter Windows Server` and the SKU is `Standard_DS1_v2`</span></span>

### <span data-ttu-id="21cfb-120">Przykład 2: Tworzenie VMSS przy użyciu **`DefaultParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="21cfb-120">Example 2: Create a VMSS using the **`DefaultParameterSet`**</span></span>
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

<span data-ttu-id="21cfb-121">W złożonym przykładzie powyżej powstaje VMSS, poniżej przedstawiono wyjaśnienie, co się dzieje:</span><span class="sxs-lookup"><span data-stu-id="21cfb-121">The complex example above creates a VMSS, following is an explanation of what is happening:</span></span>
* <span data-ttu-id="21cfb-122">Pierwsze polecenie tworzy grupę zasobów o określonej nazwie i lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="21cfb-122">The first command creates a resource group with the specified name and location.</span></span>
* <span data-ttu-id="21cfb-123">Drugie polecenie używa polecenia cmdlet **New-AzStorageAccount** w celu utworzenia konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="21cfb-123">The second command uses the **New-AzStorageAccount** cmdlet to create a storage account.</span></span>
* <span data-ttu-id="21cfb-124">Trzecia komenda używa polecenia cmdlet **Get-AzStorageAccount** w celu uzyskania konta magazynu utworzonego w drugim poleceniu i zapisanie wyniku w zmiennej $STOAccount.</span><span class="sxs-lookup"><span data-stu-id="21cfb-124">The third command then uses the **Get-AzStorageAccount** cmdlet to get the storage account created in the second command and stores the result in the $STOAccount variable.</span></span>
* <span data-ttu-id="21cfb-125">W piątym poleceniu użyto polecenia cmdlet **New-AzVirtualNetworkSubnetConfig** w celu utworzenia podsieci i zapisanie wyniku w zmiennej o nazwie $Subnet.</span><span class="sxs-lookup"><span data-stu-id="21cfb-125">The fifth command uses the **New-AzVirtualNetworkSubnetConfig** cmdlet to create a subnet and stores the result in the variable named $SubNet.</span></span>
* <span data-ttu-id="21cfb-126">W szóstym poleceniu użyto polecenia cmdlet **New-AzVirtualNetwork** w celu utworzenia sieci wirtualnej i zapisu wyniku w zmiennej o nazwie $VNET.</span><span class="sxs-lookup"><span data-stu-id="21cfb-126">The sixth command uses the **New-AzVirtualNetwork** cmdlet to create a virtual network and stores the result in the variable named $VNet.</span></span>
* <span data-ttu-id="21cfb-127">W przypadku siódmego polecenia w celu uzyskania informacji o sieci wirtualnej utworzonej w szóstym poleceniu jest używane polecenie **Get-AzVirtualNetwork** , a informacje są przechowywane w zmiennej o nazwie $VNET.</span><span class="sxs-lookup"><span data-stu-id="21cfb-127">The seventh command uses the **Get-AzVirtualNetwork** to get information about the virtual network created in the sixth command and stores the information in the variable named $VNet.</span></span>
* <span data-ttu-id="21cfb-128">W przypadku ośmiu i Dziewiątych poleceń do tworzenia i pobierania informacji z tego publicznego adresu IP użyto polecenia **New-AzPublicIpAddress** i **Get-AzureRmPublicIpAddress** .</span><span class="sxs-lookup"><span data-stu-id="21cfb-128">The eighth and ninth command uses the **New-AzPublicIpAddress** and **Get- AzureRmPublicIpAddress** to create and get information from that public IP address.</span></span>
* <span data-ttu-id="21cfb-129">Te polecenia przechowują informacje w zmiennej o nazwie $PubIP.</span><span class="sxs-lookup"><span data-stu-id="21cfb-129">The commands store the information in the variable named $PubIP.</span></span>
* <span data-ttu-id="21cfb-130">W poleceniu dziesiątym użyto polecenia cmdlet **New-AzureRmLoadBalancerFrontendIpConfig** w celu utworzenia modułu równoważenia obciążenia frontonu i zapisu wyniku w zmiennej o nazwie $frontend.</span><span class="sxs-lookup"><span data-stu-id="21cfb-130">The tenth command uses the **New- AzureRmLoadBalancerFrontendIpConfig** cmdlet to create a frontend load balancer and stores the result in the variable named $Frontend.</span></span>
* <span data-ttu-id="21cfb-131">W jedenastym poleceniu użyto polecenia **New-AzLoadBalancerBackendAddressPoolConfig** w celu utworzenia konfiguracji puli adresów zaplecza i zapisu wyniku w zmiennej o nazwie $BackendAddressPool.</span><span class="sxs-lookup"><span data-stu-id="21cfb-131">The eleventh command uses the **New-AzLoadBalancerBackendAddressPoolConfig** to create a backend address pool configuration and stores the result in the variable named $BackendAddressPool.</span></span>
* <span data-ttu-id="21cfb-132">W poleceniu dwunasta jest używana funkcja **New-AzLoadBalancerProbeConfig** w celu utworzenia sondy i zapisanie informacji dotyczących sondy w zmiennej o nazwie $Probe.</span><span class="sxs-lookup"><span data-stu-id="21cfb-132">The twelfth command uses the **New-AzLoadBalancerProbeConfig** to create a probe and stores the probe information in the variable named $Probe.</span></span>
* <span data-ttu-id="21cfb-133">Polecenie trzynaste używa polecenia cmdlet **New-AzLoadBalancerInboundNatPoolConfig** w celu utworzenia konfiguracji puli NAT (Network Address Translation) modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="21cfb-133">The thirteenth command uses the **New-AzLoadBalancerInboundNatPoolConfig** cmdlet to create a load balancer inbound network address translation (NAT) pool configuration.</span></span>
* <span data-ttu-id="21cfb-134">Polecenie czternaste używa polecenia **New-AzLoadBalancerRuleConfig** w celu utworzenia konfiguracji reguł modułu równoważenia obciążenia i zapisu wyniku w zmiennej o nazwie $LBRule.</span><span class="sxs-lookup"><span data-stu-id="21cfb-134">The fourteenth command uses the **New-AzLoadBalancerRuleConfig** to create a load balancer rule configuration and stores the result in the variable named $LBRule.</span></span>
* <span data-ttu-id="21cfb-135">W poleceniu piętnaste polecenie cmdlet **New-AzLoadBalancer** jest używane do utworzenia modułu równoważenia obciążenia i zapisuje wynik w zmiennej o nazwie $ActualLb.</span><span class="sxs-lookup"><span data-stu-id="21cfb-135">The fifteenth command uses the **New-AzLoadBalancer** cmdlet to create a load balancer and stores the result in the variable named $ActualLb.</span></span>
* <span data-ttu-id="21cfb-136">Polecenie szesnaste używa polecenia **Get-AzLoadBalancer** w celu uzyskania informacji na temat modułu równoważenia obciążenia utworzonego w piętnastym poleceniu i zapisanie informacji w zmiennej o nazwie $ExpectedLb.</span><span class="sxs-lookup"><span data-stu-id="21cfb-136">The sixteenth command uses the **Get-AzLoadBalancer** to get information about the load balancer that was created in the fifteenth command and stores the information in the variable named $ExpectedLb.</span></span>
* <span data-ttu-id="21cfb-137">W poleceniu siedemnasta użyto polecenia cmdlet **New-AzVmssIPConfig** w celu utworzenia VMSS konfiguracji adresu IP i zapisu informacji w zmiennej o nazwie $IPCfg.</span><span class="sxs-lookup"><span data-stu-id="21cfb-137">The seventeenth command uses the **New-AzVmssIPConfig** cmdlet to create a VMSS IP configuration and stores the information in the variable named $IPCfg.</span></span>
* <span data-ttu-id="21cfb-138">Polecenie osiemnastym miesiącem korzysta z polecenia cmdlet **New-AzVmssConfig** w celu utworzenia obiektu konfiguracji VMSS i zapisanie wyniku w zmiennej o nazwie $VMSS.</span><span class="sxs-lookup"><span data-stu-id="21cfb-138">The eighteenth command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
* <span data-ttu-id="21cfb-139">W poleceniu XIX użyto polecenia cmdlet **New-AzVmss** w celu utworzenia VMSS.</span><span class="sxs-lookup"><span data-stu-id="21cfb-139">The nineteenth command uses the **New-AzVmss** cmdlet to create the VMSS.</span></span>

## <span data-ttu-id="21cfb-140">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="21cfb-140">PARAMETERS</span></span>

### <span data-ttu-id="21cfb-141">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="21cfb-141">-AllocationMethod</span></span>
<span data-ttu-id="21cfb-142">Metoda alokacji dla publicznego adresu IP zestawu skali (statycznego lub dynamicznego).</span><span class="sxs-lookup"><span data-stu-id="21cfb-142">Allocation method for the Public IP Address of the Scale Set (Static or Dynamic).</span></span>  <span data-ttu-id="21cfb-143">Jeśli nie podano żadnej wartości, alokacja będzie statyczna.</span><span class="sxs-lookup"><span data-stu-id="21cfb-143">If no value is supplied, allocation will be static.</span></span>

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

### <span data-ttu-id="21cfb-144">-AsJob</span><span class="sxs-lookup"><span data-stu-id="21cfb-144">-AsJob</span></span>
<span data-ttu-id="21cfb-145">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="21cfb-145">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="21cfb-146">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="21cfb-146">-BackendPoolName</span></span>
<span data-ttu-id="21cfb-147">Nazwa puli adresów zaplecza, która ma być używana w usłudze równoważenia obciążenia dla tego zestawu skali.</span><span class="sxs-lookup"><span data-stu-id="21cfb-147">The name of the backend address pool to use in the load balancer for this Scale Set.</span></span>  <span data-ttu-id="21cfb-148">Jeśli nie podano żadnej wartości, zostanie utworzona nowa pula zaplecza z tą samą nazwą co zestaw skali.</span><span class="sxs-lookup"><span data-stu-id="21cfb-148">If no value is provided, a new backend pool will be created, with the same name as the Scale Set.</span></span>

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

### <span data-ttu-id="21cfb-149">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="21cfb-149">-BackendPort</span></span>
<span data-ttu-id="21cfb-150">Numery portów zaplecza używane przez moduł skalowania, ustawiony w celu komunikowania się z maszynami wirtualnymi w zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="21cfb-150">Backend port numbers used by the Scale Set load balancer to communicate with VMs in the Scale Set.</span></span>  <span data-ttu-id="21cfb-151">Jeśli nie określono żadnych wartości, porty 3389 i 5985 będą używane na potrzeby maszyn wirtualnych systemu Windows, a w przypadku maszyn wirtualnych Linux będzie używana wartość port 22.</span><span class="sxs-lookup"><span data-stu-id="21cfb-151">If no values are specified, ports 3389 and 5985 will be used for Windows VMS, and port 22 will be used for Linux VMs.</span></span>

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

### <span data-ttu-id="21cfb-152">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="21cfb-152">-Credential</span></span>
<span data-ttu-id="21cfb-153">Poświadczenia administratora (nazwa użytkownika i hasło) dla maszyn wirtualnych w tym zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="21cfb-153">The administrator credentials (username and password) for VMs in this Scale Set.</span></span>

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

### <span data-ttu-id="21cfb-154">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="21cfb-154">-DataDiskSizeInGb</span></span>
<span data-ttu-id="21cfb-155">Określa rozmiary dysków z danymi w GB.</span><span class="sxs-lookup"><span data-stu-id="21cfb-155">Specifies the sizes of data disks in GB.</span></span>

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

### <span data-ttu-id="21cfb-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21cfb-156">-DefaultProfile</span></span>
<span data-ttu-id="21cfb-157">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="21cfb-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21cfb-158">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="21cfb-158">-DomainNameLabel</span></span>
<span data-ttu-id="21cfb-159">Etykieta nazwy domeny dla publicznej nazwy domeny Fully-Qualified (FQDN) dla tego zestawu skali.</span><span class="sxs-lookup"><span data-stu-id="21cfb-159">The domain name label for the public Fully-Qualified domain name (FQDN) for this Scale Set.</span></span> <span data-ttu-id="21cfb-160">Jest to pierwszy składnik nazwy domeny, który jest automatycznie przypisywany do zestawu skali.</span><span class="sxs-lookup"><span data-stu-id="21cfb-160">This is the first component of the domain name that is automatically assigned to the Scale Set.</span></span> <span data-ttu-id="21cfb-161">Automatycznie przypisane nazwy domen używają formularza ( <DomainNameLabel> . <Location> . cloudapp.azure.com).</span><span class="sxs-lookup"><span data-stu-id="21cfb-161">Automatically assigned Domain names use the form (<DomainNameLabel>.<Location>.cloudapp.azure.com).</span></span> <span data-ttu-id="21cfb-162">Jeśli nie zostanie podana żadna wartość, domyślna etykieta nazwy domeny będzie łączyć się z <ScaleSetName> i <ResourceGroupName> .</span><span class="sxs-lookup"><span data-stu-id="21cfb-162">If no value is supplied, the default domain name label will be the concatenation of <ScaleSetName> and <ResourceGroupName>.</span></span>

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

### <span data-ttu-id="21cfb-163">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="21cfb-163">-EnableUltraSSD</span></span>
<span data-ttu-id="21cfb-164">Użyj dysków UltraSSD dla maszyn wirtualnych w zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="21cfb-164">Use UltraSSD disks for the VMs in the scale set.</span></span>

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

### <span data-ttu-id="21cfb-165">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="21cfb-165">-EncryptionAtHost</span></span>
<span data-ttu-id="21cfb-166">Ten parametr umożliwia szyfrowanie wszystkich dysków, w tym dysku Resource/temp, na hoście.</span><span class="sxs-lookup"><span data-stu-id="21cfb-166">This parameter will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="21cfb-167">Wartość domyślna: szyfrowanie na hoście zostanie wyłączone, chyba że dla tego zasobu zostanie ustawiona wartość true dla tej właściwości.</span><span class="sxs-lookup"><span data-stu-id="21cfb-167">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

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

### <span data-ttu-id="21cfb-168">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="21cfb-168">-EvictionPolicy</span></span>
<span data-ttu-id="21cfb-169">Zasady wykluczenia dla zestawu skali maszyny wirtualnej o niskim priorytecie.</span><span class="sxs-lookup"><span data-stu-id="21cfb-169">The eviction policy for the low priority virtual machine scale set.</span></span>  <span data-ttu-id="21cfb-170">Jedyne obsługiwane wartości to "allocate" i "Delete".</span><span class="sxs-lookup"><span data-stu-id="21cfb-170">Only supported values are 'Deallocate' and 'Delete'.</span></span>

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

### <span data-ttu-id="21cfb-171">-FrontendPoolName</span><span class="sxs-lookup"><span data-stu-id="21cfb-171">-FrontendPoolName</span></span>
<span data-ttu-id="21cfb-172">Nazwa puli adresów frontonu, która ma być używana w usłudze równoważenia obciążenia ustawionej na poziomie skali.</span><span class="sxs-lookup"><span data-stu-id="21cfb-172">The name of the frontend address pool to use in the Scale Set load balancer.</span></span>  <span data-ttu-id="21cfb-173">Jeśli nie podano żadnej wartości, zostanie utworzona nowa pula adresów frontonu o takiej samej nazwie jak ustawiona skala.</span><span class="sxs-lookup"><span data-stu-id="21cfb-173">If no value is supplied, a new Frontend Address Pool will be created, with the same name as the scale set.</span></span>

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

### <span data-ttu-id="21cfb-174">-HostGroupId</span><span class="sxs-lookup"><span data-stu-id="21cfb-174">-HostGroupId</span></span>
<span data-ttu-id="21cfb-175">Określa dedykowaną grupę hostów, w której znajduje się zestaw Skala maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="21cfb-175">Specifies the dedicated host group the virtual machine scale set will reside in.</span></span>

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

### <span data-ttu-id="21cfb-176">-ImageName</span><span class="sxs-lookup"><span data-stu-id="21cfb-176">-ImageName</span></span>
<span data-ttu-id="21cfb-177">Nazwa obrazu maszyny wirtualnej w tym zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="21cfb-177">The name of the image for VMs in this Scale Set.</span></span> <span data-ttu-id="21cfb-178">Jeśli nie podano żadnej wartości, zostanie wykorzystany obraz "Windows Server 2016 DataCenter".</span><span class="sxs-lookup"><span data-stu-id="21cfb-178">If no value is provided, the "Windows Server 2016 DataCenter" image will be used.</span></span>

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

### <span data-ttu-id="21cfb-179">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="21cfb-179">-InstanceCount</span></span>
<span data-ttu-id="21cfb-180">Liczba obrazów maszyny wirtualnej w zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="21cfb-180">The number of VM images in the Scale Set.</span></span>  <span data-ttu-id="21cfb-181">Jeśli nie podano żadnej wartości, zostaną utworzone 2 wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="21cfb-181">If no value is provided, 2 instances will be created.</span></span>

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

### <span data-ttu-id="21cfb-182">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="21cfb-182">-LoadBalancerName</span></span>
<span data-ttu-id="21cfb-183">Nazwa modułu równoważenia obciążenia do użycia z tym zestawem skali.</span><span class="sxs-lookup"><span data-stu-id="21cfb-183">The name of the load balancer to use with this Scale Set.</span></span>  <span data-ttu-id="21cfb-184">Jeśli nie zostanie określona żadna wartość, zostanie utworzona nowa usługa równoważenia obciążenia z tą samą nazwą co zestaw skali.</span><span class="sxs-lookup"><span data-stu-id="21cfb-184">A new load balancer using the same name as the Scale Set will be created if no value is specified.</span></span>

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

### <span data-ttu-id="21cfb-185">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="21cfb-185">-Location</span></span>
<span data-ttu-id="21cfb-186">Lokalizacja platformy Azure, w której zostanie utworzony ten zestaw skali.</span><span class="sxs-lookup"><span data-stu-id="21cfb-186">The Azure location where this Scale Set will be created.</span></span>  <span data-ttu-id="21cfb-187">Jeśli nie podano żadnej wartości, lokalizacja zostanie wywnioskowana z lokalizacji innych zasobów, do których odwołuje się parametr.</span><span class="sxs-lookup"><span data-stu-id="21cfb-187">If no value is specified, the location will be inferred from the location of other resources referenced in the parameters.</span></span>

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

### <span data-ttu-id="21cfb-188">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="21cfb-188">-MaxPrice</span></span>
<span data-ttu-id="21cfb-189">Maksymalna cena rozliczeń zestawu skali maszyny wirtualnej o niskim priorytecie.</span><span class="sxs-lookup"><span data-stu-id="21cfb-189">The max price of the billing of a low priority virtual machine scale set.</span></span>

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

### <span data-ttu-id="21cfb-190">-NatBackendPort</span><span class="sxs-lookup"><span data-stu-id="21cfb-190">-NatBackendPort</span></span>
<span data-ttu-id="21cfb-191">Port zaplecza translacji adresów sieciowych.</span><span class="sxs-lookup"><span data-stu-id="21cfb-191">Backend port for inbound network address translation.</span></span>

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

### <span data-ttu-id="21cfb-192">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="21cfb-192">-Priority</span></span>
<span data-ttu-id="21cfb-193">Priorytet maszyny wirtualnej w zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="21cfb-193">The priority for the virtual machine in the scale set.</span></span>  <span data-ttu-id="21cfb-194">Obsługiwane są tylko wartości "Regular", "spot" i "Low".</span><span class="sxs-lookup"><span data-stu-id="21cfb-194">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="21cfb-195">"Zwykła" dotyczy zwykłej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="21cfb-195">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="21cfb-196">"Miejsce na maszynie wirtualnej" jest na miejscu.</span><span class="sxs-lookup"><span data-stu-id="21cfb-196">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="21cfb-197">"Niski" jest również na odniesieniu do maszyny wirtualnej, ale został zastąpiony przez "punkt".</span><span class="sxs-lookup"><span data-stu-id="21cfb-197">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="21cfb-198">Użyj "spot" zamiast "niski".</span><span class="sxs-lookup"><span data-stu-id="21cfb-198">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="21cfb-199">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="21cfb-199">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="21cfb-200">Identyfikator zasobu grupy położenia zbliżeniowe, który ma być używany z tym zestawem skali.</span><span class="sxs-lookup"><span data-stu-id="21cfb-200">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="21cfb-201">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="21cfb-201">-PublicIpAddressName</span></span>
<span data-ttu-id="21cfb-202">Nazwa publicznego adresu IP, który ma być używany z tym zestawem skali.</span><span class="sxs-lookup"><span data-stu-id="21cfb-202">The name of the public IP Address to use with this scale set.</span></span>  <span data-ttu-id="21cfb-203">Jeśli nie zostanie podana żadna wartość, zostanie utworzony nowy publiczny adres IP o takiej samej nazwie jak zestaw skali.</span><span class="sxs-lookup"><span data-stu-id="21cfb-203">A new Public IPAddress with the same name as the Scale Set will be created if no value is provided.</span></span>

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

### <span data-ttu-id="21cfb-204">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21cfb-204">-ResourceGroupName</span></span>
<span data-ttu-id="21cfb-205">Określa nazwę grupy zasobów VMSS.</span><span class="sxs-lookup"><span data-stu-id="21cfb-205">Specifies the name of the resource group of the VMSS.</span></span>  <span data-ttu-id="21cfb-206">Jeśli nie podano żadnej wartości, zostanie utworzony nowy element resourceName o tej samej nazwie co zestaw skali.</span><span class="sxs-lookup"><span data-stu-id="21cfb-206">If no value is specified, a new ResourceGroup will be created using the same name as the Scale Set.</span></span>

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

### <span data-ttu-id="21cfb-207">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="21cfb-207">-ScaleInPolicy</span></span>
<span data-ttu-id="21cfb-208">Reguły, których należy przestrzegać podczas skalowania — w zestawie skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="21cfb-208">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="21cfb-209">Możliwe wartości: "default", "OldestVM" i "NewestVM".</span><span class="sxs-lookup"><span data-stu-id="21cfb-209">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="21cfb-210">"Domyślny" gdy zestaw skali maszyny wirtualnej jest skalowany, zestaw skali będzie najpierw równoważony między strefami, jeśli jest ustawionym skalą zona.</span><span class="sxs-lookup"><span data-stu-id="21cfb-210">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="21cfb-211">Następnie będzie on w miarę możliwości równoważony między domenami błędów.</span><span class="sxs-lookup"><span data-stu-id="21cfb-211">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="21cfb-212">W każdej domenie błędów maszyny wirtualne wybrane do usunięcia będą to najnowsze, które nie są chronione przed skalą.</span><span class="sxs-lookup"><span data-stu-id="21cfb-212">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="21cfb-213">OldestVM ' po przeskalowaniu zestawu skali maszyny wirtualnej do usunięcia zostanie wybrana najstarsza maszyna wirtualna, która nie jest chroniona przed przeskalowaniem.</span><span class="sxs-lookup"><span data-stu-id="21cfb-213">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="21cfb-214">W przypadku zestawów skali maszyny wirtualnej zona zestaw skali będzie najpierw równoważony między strefami.</span><span class="sxs-lookup"><span data-stu-id="21cfb-214">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="21cfb-215">W obrębie każdej strefy do usunięcia zostaną wybrane najstarsze maszyny wirtualne, które nie są chronione.</span><span class="sxs-lookup"><span data-stu-id="21cfb-215">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="21cfb-216">NewestVM ' po przeskalowaniu zestawu skali maszyny wirtualnej w celu usunięcia zostanie wybrana Najnowsza maszyna wirtualna, która nie jest chroniona przed przeskalowaniem.</span><span class="sxs-lookup"><span data-stu-id="21cfb-216">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="21cfb-217">W przypadku zestawów skali maszyny wirtualnej zona zestaw skali będzie najpierw równoważony między strefami.</span><span class="sxs-lookup"><span data-stu-id="21cfb-217">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="21cfb-218">W ramach każdej strefy do usunięcia zostaną wybrane najnowsze maszyny wirtualne, które nie są chronione.</span><span class="sxs-lookup"><span data-stu-id="21cfb-218">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

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

### <span data-ttu-id="21cfb-219">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="21cfb-219">-SecurityGroupName</span></span>
<span data-ttu-id="21cfb-220">Nazwa grupy zabezpieczeń sieci do zastosowania do tego zestawu skali.</span><span class="sxs-lookup"><span data-stu-id="21cfb-220">The name of the network security group to apply to this Scale Set.</span></span>  <span data-ttu-id="21cfb-221">Jeśli nie podano żadnej wartości, zostanie utworzona i zastosowana domyślna grupa zabezpieczeń sieci z tą samą nazwą co zestaw skali.</span><span class="sxs-lookup"><span data-stu-id="21cfb-221">If no value is provided, a default network security group with the same name as the Scale Set will be created and applied to the Scale Set.</span></span>

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

### <span data-ttu-id="21cfb-222">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="21cfb-222">-SinglePlacementGroup</span></span>
<span data-ttu-id="21cfb-223">Za pomocą tej pozycji można utworzyć zestaw skali w jednej grupie położenia, domyślnie jest to wiele grup</span><span class="sxs-lookup"><span data-stu-id="21cfb-223">Use this to create the Scale set in a single placement group, default is multiple groups</span></span>

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

### <span data-ttu-id="21cfb-224">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="21cfb-224">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="21cfb-225">Określa, że rozszerzenia nie są uruchamiane na dodatkowych zarezerwowych maszynach wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="21cfb-225">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="21cfb-226">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="21cfb-226">-SubnetAddressPrefix</span></span>
<span data-ttu-id="21cfb-227">Prefiks adresu podsieci, który będzie używany przez tę ScaleSet.</span><span class="sxs-lookup"><span data-stu-id="21cfb-227">The address prefix of the Subnet this ScaleSet will use.</span></span> <span data-ttu-id="21cfb-228">Domyślne ustawienia podsieci (192.168.1.0/24) zostaną zastosowane, jeśli nie podano żadnej wartości.</span><span class="sxs-lookup"><span data-stu-id="21cfb-228">Default Subnet settings (192.168.1.0/24) will be applied if no value is provided.</span></span>

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

### <span data-ttu-id="21cfb-229">-Subnetname</span><span class="sxs-lookup"><span data-stu-id="21cfb-229">-SubnetName</span></span>
<span data-ttu-id="21cfb-230">Nazwa podsieci do użycia z tym zestawem skali.</span><span class="sxs-lookup"><span data-stu-id="21cfb-230">The name of the subnet to use with this Scale Set.</span></span>  <span data-ttu-id="21cfb-231">Zostanie utworzona nowa podsieć o takiej samej nazwie jak skala ustawiona, jeśli nie podano żadnej wartości.</span><span class="sxs-lookup"><span data-stu-id="21cfb-231">A new Subnet will be created with the same name as the Scale Set if no value is provided.</span></span>

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

### <span data-ttu-id="21cfb-232">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="21cfb-232">-SystemAssignedIdentity</span></span>
<span data-ttu-id="21cfb-233">Jeśli parametr jest obecny, w przypadku maszyn wirtualnych w zestawie skali jest przypisana automatycznie generowana tożsamość systemu zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="21cfb-233">If the parameter is present then the VM(s) in the scale set is(are) assigned a managed system identity that is auto generated.</span></span>

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

### <span data-ttu-id="21cfb-234">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="21cfb-234">-UpgradePolicyMode</span></span>
<span data-ttu-id="21cfb-235">Tryb zasad uaktualniania dla wystąpień maszyny wirtualnej w tym zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="21cfb-235">The upgrade policy mode for VM instances in this Scale Set.</span></span>  <span data-ttu-id="21cfb-236">Zasady uaktualniania mogą określać uaktualnianie automatyczne, ręczne lub stopniowe.</span><span class="sxs-lookup"><span data-stu-id="21cfb-236">Upgrade policy could specify Automatic, Manual, or Rolling upgrades.</span></span>

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

### <span data-ttu-id="21cfb-237">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="21cfb-237">-UserAssignedIdentity</span></span>
<span data-ttu-id="21cfb-238">Nazwa tożsamości usługi zarządzanej, która powinna być przypisana do maszyn wirtualnych w zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="21cfb-238">The name of a managed service identity that should be assigned to the VM(s) in the scale set.</span></span>

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

### <span data-ttu-id="21cfb-239">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="21cfb-239">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="21cfb-240">Określa obiekt **VirtualMachineScaleSet** , który zawiera właściwości VMSS, które tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21cfb-240">Specifies the **VirtualMachineScaleSet** object that contains the properties of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="21cfb-241">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="21cfb-241">-VirtualNetworkName</span></span>
<span data-ttu-id="21cfb-242">Nazwa fo sieci wirtualnej do użycia z tym zestawem skali.</span><span class="sxs-lookup"><span data-stu-id="21cfb-242">The name fo the Virtual Network to use with this scale set.</span></span>  <span data-ttu-id="21cfb-243">Jeśli nie podano żadnej wartości, zostanie utworzona nowa sieć wirtualna o takiej samej nazwie jak zestaw skali.</span><span class="sxs-lookup"><span data-stu-id="21cfb-243">If no value is supplied, a new virtual network with the same name as the Scale Set will be created.</span></span>

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

### <span data-ttu-id="21cfb-244">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="21cfb-244">-VMScaleSetName</span></span>
<span data-ttu-id="21cfb-245">Określa nazwę VMSS, które tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21cfb-245">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="21cfb-246">-VmSize</span><span class="sxs-lookup"><span data-stu-id="21cfb-246">-VmSize</span></span>
<span data-ttu-id="21cfb-247">Rozmiar wystąpień maszyny wirtualnej w tym zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="21cfb-247">The size of the VM instances in this scale set.</span></span>  <span data-ttu-id="21cfb-248">Jeśli nie określono rozmiaru, zostanie wykorzystana wartość domyślna (Standard_DS1_v2).</span><span class="sxs-lookup"><span data-stu-id="21cfb-248">A default size (Standard_DS1_v2) will be used if no Size is specified.</span></span>

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

### <span data-ttu-id="21cfb-249">-VnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="21cfb-249">-VnetAddressPrefix</span></span>
<span data-ttu-id="21cfb-250">Prefiks adresu sieci wirtualnej używanej z tym zestawem skali.</span><span class="sxs-lookup"><span data-stu-id="21cfb-250">The address prefix for the virtual network used with this Scale Set.</span></span>  <span data-ttu-id="21cfb-251">Jeśli nie zostanie podana żadna wartość, zostanie użyty domyślny prefiks adresu sieci wirtualnej (192.168.0.0/16).</span><span class="sxs-lookup"><span data-stu-id="21cfb-251">Default virtual network address prefix settings (192.168.0.0/16) will be used if no value is supplied.</span></span>

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

### <span data-ttu-id="21cfb-252">-Zone</span><span class="sxs-lookup"><span data-stu-id="21cfb-252">-Zone</span></span>
<span data-ttu-id="21cfb-253">Lista stref dostępności oznaczająca adres IP przydzielony dla zasobu musi pochodzić od.</span><span class="sxs-lookup"><span data-stu-id="21cfb-253">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="21cfb-254">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="21cfb-254">-Confirm</span></span>
<span data-ttu-id="21cfb-255">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21cfb-255">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21cfb-256">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21cfb-256">-WhatIf</span></span>
<span data-ttu-id="21cfb-257">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21cfb-257">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21cfb-258">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="21cfb-258">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21cfb-259">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21cfb-259">CommonParameters</span></span>
<span data-ttu-id="21cfb-260">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21cfb-260">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21cfb-261">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="21cfb-261">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21cfb-262">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21cfb-262">INPUTS</span></span>

### <span data-ttu-id="21cfb-263">System. String</span><span class="sxs-lookup"><span data-stu-id="21cfb-263">System.String</span></span>

### <span data-ttu-id="21cfb-264">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="21cfb-264">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="21cfb-265">System. Collections. Generic. list "1 [[System. String; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="21cfb-265">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="21cfb-266">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="21cfb-266">OUTPUTS</span></span>

### <span data-ttu-id="21cfb-267">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="21cfb-267">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="21cfb-268">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="21cfb-268">NOTES</span></span>

## <span data-ttu-id="21cfb-269">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="21cfb-269">RELATED LINKS</span></span>

[<span data-ttu-id="21cfb-270">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="21cfb-270">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="21cfb-271">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="21cfb-271">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="21cfb-272">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="21cfb-272">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="21cfb-273">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="21cfb-273">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="21cfb-274">Start — AzVmss</span><span class="sxs-lookup"><span data-stu-id="21cfb-274">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="21cfb-275">Zatrzymaj — AzVmss</span><span class="sxs-lookup"><span data-stu-id="21cfb-275">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="21cfb-276">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="21cfb-276">Update-AzVmss</span></span>](./Update-AzVmss.md)


