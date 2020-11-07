---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmss
schema: 2.0.0
ms.openlocfilehash: f93e05448278e2aaa70ff226a5d3618fdad0e6b4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898976"
---
# <span data-ttu-id="8b4c4-101">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8b4c4-101">New-AzureRmVmss</span></span>

## <span data-ttu-id="8b4c4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8b4c4-102">SYNOPSIS</span></span>
<span data-ttu-id="8b4c4-103">Tworzy VMSS.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-103">Creates a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b4c4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8b4c4-104">SYNTAX</span></span>

### <span data-ttu-id="8b4c4-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8b4c4-105">DefaultParameter (Default)</span></span>
```
New-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b4c4-106">SimpleParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b4c4-106">SimpleParameterSet</span></span>
```
New-AzureRmVmss [[-ResourceGroupName] <String>] [-VMScaleSetName] <String> [-AsJob] [-ImageName <String>]
 -Credential <PSCredential> [-InstanceCount <Int32>] [-VirtualNetworkName <String>] [-SubnetName <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-SecurityGroupName <String>]
 [-LoadBalancerName <String>] [-BackendPort <Int32[]>] [-Location <String>] [-VmSize <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-AllocationMethod <String>] [-VnetAddressPrefix <String>]
 [-SubnetAddressPrefix <String>] [-FrontendPoolName <String>] [-BackendPoolName <String>]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-NatBackendPort <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b4c4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8b4c4-107">DESCRIPTION</span></span>
<span data-ttu-id="8b4c4-108">Polecenie cmdlet **New-AzureRmVmss** umożliwia utworzenie zestawu skali maszyny wirtualnej (VMSS) na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-108">The **New-AzureRmVmss** cmdlet creates a Virtual Machine Scale Set (VMSS) in Azure.</span></span>
<span data-ttu-id="8b4c4-109">To polecenie cmdlet pobiera obiekt **VirtualMachineScaleSet** jako dane wejściowe.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-109">This cmdlet takes a **VirtualMachineScaleSet** object as input.</span></span>

## <span data-ttu-id="8b4c4-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8b4c4-110">EXAMPLES</span></span>

### <span data-ttu-id="8b4c4-111">Przykład 1. Tworzenie VMSS</span><span class="sxs-lookup"><span data-stu-id="8b4c4-111">Example 1: Create a VMSS</span></span>
```
# Common
$LOC = "WestUs";
$RGName = "rgkyvms";

New-AzureRmResourceGroup -Name $RGName -Location $LOC -Force;

# SRP
$STOName = "STO" + $RGName;
$STOType = "Standard_GRS";
New-AzureRmStorageAccount -ResourceGroupName $RGName -Name $STOName -Location $LOC -Type $STOType;
$STOAccount = Get-AzureRmStorageAccount -ResourceGroupName $RGName -Name $STOName; 

# NRP
$SubNet = New-AzureRmVirtualNetworkSubnetConfig -Name ("subnet" + $RGName) -AddressPrefix "10.0.0.0/24";
$VNet = New-AzureRmVirtualNetwork -Force -Name ("vnet" + $RGName) -ResourceGroupName $RGName -Location $LOC -AddressPrefix "10.0.0.0/16" -DnsServer "10.1.1.1" -Subnet $SubNet;
$VNet = Get-AzureRmVirtualNetwork -Name ('vnet' + $RGName) -ResourceGroupName $RGName;
$SubNetId = $VNet.Subnets[0].Id;

$PubIP = New-AzureRmPublicIpAddress -Force -Name ("PubIP" + $RGName) -ResourceGroupName $RGName -Location $LOC -AllocationMethod Dynamic -DomainNameLabel ("PubIP" + $RGName);
$PubIP = Get-AzureRmPublicIpAddress -Name ("PubIP"  + $RGName) -ResourceGroupName $RGName;

# Create LoadBalancer
$FrontendName = "fe" + $RGName
$BackendAddressPoolName = "bepool" + $RGName
$ProbeName = "vmssprobe" + $RGName
$InboundNatPoolName  = "innatpool" + $RGName
$LBRuleName = "lbrule" + $RGName
$LBName = "vmsslb" + $RGName

$Frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name $FrontendName -PublicIpAddress $PubIP
$BackendAddressPool = New-AzureRmLoadBalancerBackendAddressPoolConfig -Name $BackendAddressPoolName
$Probe = New-AzureRmLoadBalancerProbeConfig -Name $ProbeName -RequestPath healthcheck.aspx -Protocol http -Port 80 -IntervalInSeconds 15 -ProbeCount 2
$InboundNatPool = New-AzureRmLoadBalancerInboundNatPoolConfig -Name $InboundNatPoolName  -FrontendIPConfigurationId `
    $Frontend.Id -Protocol Tcp -FrontendPortRangeStart 3360 -FrontendPortRangeEnd 3362 -BackendPort 3370;
$LBRule = New-AzureRmLoadBalancerRuleConfig -Name $LBRuleName `
    -FrontendIPConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -Protocol Tcp -FrontendPort 80 -BackendPort 80 `
    -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP;
$ActualLb = New-AzureRmLoadBalancer -Name $LBName -ResourceGroupName $RGName -Location $LOC `
    -FrontendIpConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -LoadBalancingRule $LBRule -InboundNatPool $InboundNatPool;
$ExpectedLb = Get-AzureRmLoadBalancer -Name $LBName -ResourceGroupName $RGName

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
$IPCfg = New-AzureRmVmssIPConfig -Name "Test" `
    -LoadBalancerInboundNatPoolsId $ExpectedLb.InboundNatPools[0].Id `
    -LoadBalancerBackendAddressPoolsId $ExpectedLb.BackendAddressPools[0].Id `
    -SubnetId $SubNetId;
            
#VMSS Config
$VMSS = New-AzureRmVmssConfig -Location $LOC -SkuCapacity 2 -SkuName "Standard_A2" -UpgradePolicyMode "Automatic" `
    | Add-AzureRmVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
    | Add-AzureRmVmssNetworkInterfaceConfiguration -Name "Test2"  -IPConfiguration $IPCfg `
    | Set-AzureRmVmssOSProfile -ComputerNamePrefix "Test"  -AdminUsername $AdminUsername -AdminPassword $AdminPassword `
    | Set-AzureRmVmssStorageProfile -Name "Test"  -OsDiskCreateOption 'FromImage' -OsDiskCaching "None" `
    -ImageReferenceOffer $Offer -ImageReferenceSku $Sku -ImageReferenceVersion $Version `
    -ImageReferencePublisher $PublisherName -VhdContainer $VHDContainer `
    | Add-AzureRmVmssExtension -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True

#Create the VMSS
New-AzureRmVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

<span data-ttu-id="8b4c4-112">W poniższym przykładzie złożonym przedstawiono tworzenie VMSS.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-112">The following complex example creates a VMSS.</span></span>
<span data-ttu-id="8b4c4-113">Pierwsze polecenie tworzy grupę zasobów o określonej nazwie i lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-113">The first command creates a resource group with the specified name and location.</span></span>
<span data-ttu-id="8b4c4-114">Drugie polecenie używa polecenia cmdlet **New-AzureRmStorageAccount** w celu utworzenia konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-114">The second command uses the **New-AzureRmStorageAccount** cmdlet to create a storage account.</span></span>
<span data-ttu-id="8b4c4-115">Trzecia komenda używa polecenia cmdlet **Get-AzureRmStorageAccount** w celu uzyskania konta magazynu utworzonego w drugim poleceniu i zapisanie wyniku w zmiennej $STOAccount.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-115">The third command then uses the **Get-AzureRmStorageAccount** cmdlet to get the storage account created in the second command and stores the result in the $STOAccount variable.</span></span>
<span data-ttu-id="8b4c4-116">W piątym poleceniu użyto polecenia cmdlet **New-AzureRmVirtualNetworkSubnetConfig** w celu utworzenia podsieci i zapisanie wyniku w zmiennej o nazwie $Subnet.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-116">The fifth command uses the **New-AzureRmVirtualNetworkSubnetConfig** cmdlet to create a subnet and stores the result in the variable named $SubNet.</span></span>
<span data-ttu-id="8b4c4-117">W szóstym poleceniu użyto polecenia cmdlet **New-AzureRmVirtualNetwork** w celu utworzenia sieci wirtualnej i zapisu wyniku w zmiennej o nazwie $VNET.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-117">The sixth command uses the **New-AzureRmVirtualNetwork** cmdlet to create a virtual network and stores the result in the variable named $VNet.</span></span>
<span data-ttu-id="8b4c4-118">W przypadku siódmego polecenia w celu uzyskania informacji o sieci wirtualnej utworzonej w szóstym poleceniu jest używane polecenie **Get-AzureRmVirtualNetwork** , a informacje są przechowywane w zmiennej o nazwie $VNET.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-118">The seventh command uses the **Get-AzureRmVirtualNetwork** to get information about the virtual network created in the sixth command and stores the information in the variable named $VNet.</span></span>
<span data-ttu-id="8b4c4-119">W przypadku ośmiu i Dziewiątych poleceń do tworzenia i pobierania informacji z tego publicznego adresu IP użyto polecenia **New-AzureRmPublicIpAddress** i **Get-AzureRmPublicIpAddress** .</span><span class="sxs-lookup"><span data-stu-id="8b4c4-119">The eighth and ninth command uses the **New-AzureRmPublicIpAddress** and **Get- AzureRmPublicIpAddress** to create and get information from that public IP address.</span></span>
<span data-ttu-id="8b4c4-120">Te polecenia przechowują informacje w zmiennej o nazwie $PubIP.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-120">The commands store the information in the variable named $PubIP.</span></span>
<span data-ttu-id="8b4c4-121">W poleceniu dziesiątym użyto polecenia cmdlet **New-AzureRmLoadBalancerFrontendIpConfig** w celu utworzenia modułu równoważenia obciążenia frontonu i zapisu wyniku w zmiennej o nazwie $frontend.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-121">The tenth command uses the **New- AzureRmLoadBalancerFrontendIpConfig** cmdlet to create a frontend load balancer and stores the result in the variable named $Frontend.</span></span>
<span data-ttu-id="8b4c4-122">W jedenastym poleceniu użyto polecenia **New-AzureRmLoadBalancerBackendAddressPoolConfig** w celu utworzenia konfiguracji puli adresów zaplecza i zapisu wyniku w zmiennej o nazwie $BackendAddressPool.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-122">The eleventh command uses the **New-AzureRmLoadBalancerBackendAddressPoolConfig** to create a backend address pool configuration and stores the result in the variable named $BackendAddressPool.</span></span>
<span data-ttu-id="8b4c4-123">W poleceniu dwunasta jest używana funkcja **New-AzureRmLoadBalancerProbeConfig** w celu utworzenia sondy i zapisanie informacji dotyczących sondy w zmiennej o nazwie $Probe.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-123">The twelfth command uses the **New-AzureRmLoadBalancerProbeConfig** to create a probe and stores the probe information in the variable named $Probe.</span></span>
<span data-ttu-id="8b4c4-124">Polecenie trzynaste używa polecenia cmdlet **New-AzureRmLoadBalancerInboundNatPoolConfig** w celu utworzenia konfiguracji puli NAT (Network Address Translation) modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-124">The thirteenth command uses the **New-AzureRmLoadBalancerInboundNatPoolConfig** cmdlet to create a load balancer inbound network address translation (NAT) pool configuration.</span></span>
<span data-ttu-id="8b4c4-125">Polecenie czternaste używa polecenia **New-AzureRmLoadBalancerRuleConfig** w celu utworzenia konfiguracji reguł modułu równoważenia obciążenia i zapisu wyniku w zmiennej o nazwie $LBRule.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-125">The fourteenth command uses the **New-AzureRmLoadBalancerRuleConfig** to create a load balancer rule configuration and stores the result in the variable named $LBRule.</span></span>
<span data-ttu-id="8b4c4-126">W poleceniu piętnaste polecenie cmdlet **New-AzureRmLoadBalancer** jest używane do utworzenia modułu równoważenia obciążenia i zapisuje wynik w zmiennej o nazwie $ActualLb.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-126">The fifteenth command uses the **New-AzureRmLoadBalancer** cmdlet to create a load balancer and stores the result in the variable named $ActualLb.</span></span>
<span data-ttu-id="8b4c4-127">Polecenie szesnaste używa polecenia **Get-AzureRmLoadBalancer** w celu uzyskania informacji na temat modułu równoważenia obciążenia utworzonego w piętnastym poleceniu i zapisanie informacji w zmiennej o nazwie $ExpectedLb.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-127">The sixteenth command uses the **Get-AzureRmLoadBalancer** to get information about the load balancer that was created in the fifteenth command and stores the information in the variable named $ExpectedLb.</span></span>
<span data-ttu-id="8b4c4-128">W poleceniu siedemnasta użyto polecenia cmdlet **New-AzureRmVmssIPConfig** w celu utworzenia VMSS konfiguracji adresu IP i zapisu informacji w zmiennej o nazwie $IPCfg.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-128">The seventeenth command uses the **New-AzureRmVmssIPConfig** cmdlet to create a VMSS IP configuration and stores the information in the variable named $IPCfg.</span></span>
<span data-ttu-id="8b4c4-129">Polecenie osiemnastym miesiącem korzysta z polecenia cmdlet **New-AzureRmVmssConfig** w celu utworzenia obiektu konfiguracji VMSS i zapisanie wyniku w zmiennej o nazwie $VMSS.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-129">The eighteenth command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="8b4c4-130">W poleceniu XIX użyto polecenia cmdlet **New-AzureRmVmss** w celu utworzenia VMSS.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-130">The nineteenth command uses the **New-AzureRmVmss** cmdlet to create the VMSS.</span></span>

## <span data-ttu-id="8b4c4-131">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8b4c4-131">PARAMETERS</span></span>

### <span data-ttu-id="8b4c4-132">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="8b4c4-132">-AllocationMethod</span></span>
<span data-ttu-id="8b4c4-133">Metoda alokacji dla publicznego adresu IP zestawu skali (statycznego lub dynamicznego).</span><span class="sxs-lookup"><span data-stu-id="8b4c4-133">Allocation method for the Public IP Address of the Scale Set (Static or Dynamic).</span></span>  <span data-ttu-id="8b4c4-134">Jeśli nie podano żadnej wartości, alokacja będzie statyczna.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-134">If no value is supplied, allocation will be static.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b4c4-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8b4c4-135">-AsJob</span></span>
<span data-ttu-id="8b4c4-136">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-136">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b4c4-137">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="8b4c4-137">-BackendPoolName</span></span>
<span data-ttu-id="8b4c4-138">Nazwa puli adresów zaplecza, która ma być używana w usłudze równoważenia obciążenia dla tego zestawu skali.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-138">The name of the backend address pool to use in the load balancer for this Scale Set.</span></span>  <span data-ttu-id="8b4c4-139">Jeśli nie podano żadnej wartości, zostanie utworzona nowa pula zaplecza z tą samą nazwą co zestaw skali.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-139">If no value is provided, a new backend pool will be created, with the same name as the Scale Set.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b4c4-140">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="8b4c4-140">-BackendPort</span></span>
<span data-ttu-id="8b4c4-141">Numery portów zaplecza używane przez moduł skalowania, ustawiony w celu komunikowania się z maszynami wirtualnymi w zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-141">Backend port numbers used by the Scale Set load balancer to communicate with VMs in the Scale Set.</span></span>  <span data-ttu-id="8b4c4-142">Jeśli nie określono żadnych wartości, porty 3389 i 5985 będą używane na potrzeby maszyn wirtualnych systemu Windows, a w przypadku maszyn wirtualnych Linux będzie używana wartość port 22.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-142">If no values are specified, ports 3389 and 5985 will be used for Windows VMS, and port 22 will be used for Linux VMs.</span></span>

```yaml
Type: Int32[]
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b4c4-143">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="8b4c4-143">-Credential</span></span>
<span data-ttu-id="8b4c4-144">Poświadczenia administratora (nazwa użytkownika i hasło) dla maszyn wirtualnych w tym zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-144">The administrator credentials (username and password) for VMs in this Scale Set.</span></span>

```yaml
Type: PSCredential
Parameter Sets: SimpleParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b4c4-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b4c4-145">-DefaultProfile</span></span>
<span data-ttu-id="8b4c4-146">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b4c4-147">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="8b4c4-147">-DomainNameLabel</span></span>
<span data-ttu-id="8b4c4-148">Etykieta nazwy domeny dla publicznej nazwy domeny Fully-Qualified (FQDN) dla tego zestawu skali.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-148">The domain name label for the public Fully-Qualified domain name (FQDN) for this Scale Set.</span></span> <span data-ttu-id="8b4c4-149">Jest to pierwszy składnik nazwy domeny, który jest automatycznie przypisywany do zestawu skali.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-149">This is the first component of the domain name that is automatically assigned to the Scale Set.</span></span> <span data-ttu-id="8b4c4-150">Automatycznie przypisane nazwy domen używają formularza ( <DomainNameLabel> . <Location> . cloudapp.azure.com).</span><span class="sxs-lookup"><span data-stu-id="8b4c4-150">Automatically assigned Domain names use the form (<DomainNameLabel>.<Location>.cloudapp.azure.com).</span></span> <span data-ttu-id="8b4c4-151">Jeśli nie zostanie podana żadna wartość, domyślna etykieta nazwy domeny będzie łączyć się z <ScaleSetName> i <ResourceGroupName> .</span><span class="sxs-lookup"><span data-stu-id="8b4c4-151">If no value is supplied, the default domain name label will be the concatenation of <ScaleSetName> and <ResourceGroupName>.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b4c4-152">-FrontendPoolName</span><span class="sxs-lookup"><span data-stu-id="8b4c4-152">-FrontendPoolName</span></span>
<span data-ttu-id="8b4c4-153">Nazwa puli adresów frontonu, która ma być używana w usłudze równoważenia obciążenia ustawionej na poziomie skali.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-153">The name of the frontend address pool to use in the Scale Set load balancer.</span></span>  <span data-ttu-id="8b4c4-154">Jeśli nie podano żadnej wartości, zostanie utworzona nowa pula adresów frontonu o takiej samej nazwie jak ustawiona skala.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-154">If no value is supplied, a new Frontend Address Pool will be created, with the same name as the scale set.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b4c4-155">-ImageName</span><span class="sxs-lookup"><span data-stu-id="8b4c4-155">-ImageName</span></span>
<span data-ttu-id="8b4c4-156">Nazwa obrazu maszyny wirtualnej w tym zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-156">The name of the image for VMs in this Scale Set.</span></span> <span data-ttu-id="8b4c4-157">Jeśli nie podano żadnej wartości, zostanie wykorzystany obraz "Windows Server 2016 DataCenter".</span><span class="sxs-lookup"><span data-stu-id="8b4c4-157">If no value is provided, the "Windows Server 2016 DataCenter" image will be used.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b4c4-158">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="8b4c4-158">-InstanceCount</span></span>
<span data-ttu-id="8b4c4-159">Liczba obrazów maszyny wirtualnej w zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-159">The number of VM images in the Scale Set.</span></span>  <span data-ttu-id="8b4c4-160">Jeśli nie podano żadnej wartości, zostaną utworzone 2 wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-160">If no value is provided, 2 instances will be created.</span></span>

```yaml
Type: Int32
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b4c4-161">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="8b4c4-161">-LoadBalancerName</span></span>
<span data-ttu-id="8b4c4-162">Nazwa modułu równoważenia obciążenia do użycia z tym zestawem skali.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-162">The name of the load balancer to use with this Scale Set.</span></span>  <span data-ttu-id="8b4c4-163">Jeśli nie zostanie określona żadna wartość, zostanie utworzona nowa usługa równoważenia obciążenia z tą samą nazwą co zestaw skali.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-163">A new load balancer using the same name as the Scale Set will be created if no value is specified.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b4c4-164">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="8b4c4-164">-Location</span></span>
<span data-ttu-id="8b4c4-165">Lokalizacja platformy Azure, w której zostanie utworzony ten zestaw skali.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-165">The Azure location where this Scale Set will be created.</span></span>  <span data-ttu-id="8b4c4-166">Jeśli nie podano żadnej wartości, lokalizacja zostanie wywnioskowana z lokalizacji innych zasobów, do których odwołuje się parametr.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-166">If no value is specified, the location will be inferred from the location of other resources referenced in the parameters.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b4c4-167">-NatBackendPort</span><span class="sxs-lookup"><span data-stu-id="8b4c4-167">-NatBackendPort</span></span>
<span data-ttu-id="8b4c4-168">Port zaplecza translacji adresów sieciowych.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-168">Backend port for inbound network address translation.</span></span>

```yaml
Type: Int32[]
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b4c4-169">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="8b4c4-169">-PublicIpAddressName</span></span>
<span data-ttu-id="8b4c4-170">Nazwa publicznego adresu IP, który ma być używany z tym zestawem skali.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-170">The name of the public IP Address to use with this scale set.</span></span>  <span data-ttu-id="8b4c4-171">Jeśli nie zostanie podana żadna wartość, zostanie utworzony nowy publiczny adres IP o takiej samej nazwie jak zestaw skali.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-171">A new Public IPAddress with the same name as the Scale Set will be created if no value is provided.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b4c4-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b4c4-172">-ResourceGroupName</span></span>
<span data-ttu-id="8b4c4-173">Określa nazwę grupy zasobów VMSS.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-173">Specifies the name of the resource group of the VMSS.</span></span>  <span data-ttu-id="8b4c4-174">Jeśli nie podano żadnej wartości, zostanie utworzony nowy element resourceName o tej samej nazwie co zestaw skali.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-174">If no value is specified, a new ResourceGroup will be created using the same name as the Scale Set.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b4c4-175">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="8b4c4-175">-SecurityGroupName</span></span>
<span data-ttu-id="8b4c4-176">Nazwa grupy zabezpieczeń sieci do zastosowania do tego zestawu skali.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-176">The name of the network security group to apply to this Scale Set.</span></span>  <span data-ttu-id="8b4c4-177">Jeśli nie podano żadnej wartości, zostanie utworzona i zastosowana domyślna grupa zabezpieczeń sieci z tą samą nazwą co zestaw skali.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-177">If no value is provided, a default network security group with the same name as the Scale Set will be created and applied to the Scale Set.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b4c4-178">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="8b4c4-178">-SubnetAddressPrefix</span></span>
<span data-ttu-id="8b4c4-179">Prefiks adresu podsieci, który będzie używany przez tę ScaleSet.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-179">The address prefix of the Subnet this ScaleSet will use.</span></span> <span data-ttu-id="8b4c4-180">Domyślne ustawienia podsieci (192.168.1.0/24) zostaną zastosowane, jeśli nie podano żadnej wartości.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-180">Default Subnet settings (192.168.1.0/24) will be applied if no value is provided.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b4c4-181">-Subnetname</span><span class="sxs-lookup"><span data-stu-id="8b4c4-181">-SubnetName</span></span>
<span data-ttu-id="8b4c4-182">Nazwa podsieci do użycia z tym zestawem skali.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-182">The name of the subnet to use with this Scale Set.</span></span>  <span data-ttu-id="8b4c4-183">Zostanie utworzona nowa podsieć o takiej samej nazwie jak skala ustawiona, jeśli nie podano żadnej wartości.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-183">A new Subnet will be created with the same name as the Scale Set if no value is provided.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b4c4-184">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="8b4c4-184">-UpgradePolicyMode</span></span>
<span data-ttu-id="8b4c4-185">Tryb zasad uaktualniania dla wystąpień maszyny wirtualnej w tym zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-185">The upgrade policy mode for VM instances in this Scale Set.</span></span>  <span data-ttu-id="8b4c4-186">Zasady uaktualniania mogą określać uaktualnianie automatyczne, ręczne lub stopniowe.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-186">Upgrade policy could specify Automatic, Manual, or Rolling upgrades.</span></span>

```yaml
Type: UpgradeMode
Parameter Sets: SimpleParameterSet
Aliases: 
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b4c4-187">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8b4c4-187">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="8b4c4-188">Określa obiekt **VirtualMachineScaleSet** , który zawiera właściwości VMSS, które tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-188">Specifies the **VirtualMachineScaleSet** object that contains the properties of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b4c4-189">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="8b4c4-189">-VirtualNetworkName</span></span>
<span data-ttu-id="8b4c4-190">Nazwa fo sieci wirtualnej do użycia z tym zestawem skali.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-190">The name fo the Virtual Network to use with this scale set.</span></span>  <span data-ttu-id="8b4c4-191">Jeśli nie podano żadnej wartości, zostanie utworzona nowa sieć wirtualna o takiej samej nazwie jak zestaw skali.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-191">If no value is supplied, a new virtual network with the same name as the Scale Set will be created.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b4c4-192">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="8b4c4-192">-VMScaleSetName</span></span>
<span data-ttu-id="8b4c4-193">Określa nazwę VMSS, które tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-193">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b4c4-194">-VmSize</span><span class="sxs-lookup"><span data-stu-id="8b4c4-194">-VmSize</span></span>
<span data-ttu-id="8b4c4-195">Rozmiar wystąpień maszyny wirtualnej w tym zestawie skali.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-195">The size of the VM instances in this scale set.</span></span>  <span data-ttu-id="8b4c4-196">Jeśli nie określono rozmiaru, zostanie wykorzystana wartość domyślna (Standard_DS1_v2).</span><span class="sxs-lookup"><span data-stu-id="8b4c4-196">A default size (Standard_DS1_v2) will be used if no Size is specified.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b4c4-197">-VnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="8b4c4-197">-VnetAddressPrefix</span></span>
<span data-ttu-id="8b4c4-198">Prefiks adresu sieci wirtualnej używanej z tym zestawem skali.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-198">The address prefix for the virtual network used with this Scale Set.</span></span>  <span data-ttu-id="8b4c4-199">Jeśli nie zostanie podana żadna wartość, zostanie użyty domyślny prefiks adresu sieci wirtualnej (192.168.0.0/16).</span><span class="sxs-lookup"><span data-stu-id="8b4c4-199">Default virtual network address prefix settings (192.168.0.0/16) will be used if no value is supplied.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b4c4-200">-Zone</span><span class="sxs-lookup"><span data-stu-id="8b4c4-200">-Zone</span></span>
<span data-ttu-id="8b4c4-201">Lista stref dostępności oznaczająca adres IP przydzielony dla zasobu musi pochodzić od.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-201">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="8b4c4-202">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8b4c4-202">-Confirm</span></span>
<span data-ttu-id="8b4c4-203">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-203">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b4c4-204">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b4c4-204">-WhatIf</span></span>
<span data-ttu-id="8b4c4-205">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-205">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="8b4c4-206">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-206">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b4c4-207">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b4c4-207">CommonParameters</span></span>
<span data-ttu-id="8b4c4-208">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-208">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b4c4-209">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b4c4-209">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b4c4-210">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8b4c4-210">INPUTS</span></span>

### <span data-ttu-id="8b4c4-211">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8b4c4-211">VirtualMachineScaleSet</span></span>
<span data-ttu-id="8b4c4-212">Parametr "VirtualMachineScaleSet" akceptuje wartość typu "VirtualMachineScaleSet" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="8b4c4-212">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="8b4c4-213">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8b4c4-213">OUTPUTS</span></span>

### <span data-ttu-id="8b4c4-214">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="8b4c4-214">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="8b4c4-215">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8b4c4-215">NOTES</span></span>

## <span data-ttu-id="8b4c4-216">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8b4c4-216">RELATED LINKS</span></span>

[<span data-ttu-id="8b4c4-217">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8b4c4-217">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="8b4c4-218">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8b4c4-218">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="8b4c4-219">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8b4c4-219">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="8b4c4-220">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8b4c4-220">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="8b4c4-221">Start — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8b4c4-221">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="8b4c4-222">Zatrzymaj — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8b4c4-222">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="8b4c4-223">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8b4c4-223">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


