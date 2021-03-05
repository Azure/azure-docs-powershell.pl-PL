---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmssipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
ms.openlocfilehash: 30dbe52805017a00f24cc95c832386545ae036e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965041"
---
# <span data-ttu-id="0a241-101">New-AzVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="0a241-101">New-AzVmssIpConfig</span></span>

## <span data-ttu-id="0a241-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a241-102">SYNOPSIS</span></span>
<span data-ttu-id="0a241-103">Tworzy konfigurację adresów IP dla interfejsu sieciowego maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="0a241-103">Creates an IP configuration for a network interface of a VMSS.</span></span>

## <span data-ttu-id="0a241-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0a241-104">SYNTAX</span></span>

```
New-AzVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-Primary] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-IpTag <VirtualMachineScaleSetIpTag[]>] [-PublicIPPrefix <String>]
 [-PublicIPAddressVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0a241-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="0a241-105">DESCRIPTION</span></span>
<span data-ttu-id="0a241-106">Polecenie **cmdlet New-AzVmssIpConfig** tworzy obiekt konfiguracji adresu IP dla interfejsu sieciowego zestawu skal maszyny wirtualnej (VIRTUAL Machine Scale Set).</span><span class="sxs-lookup"><span data-stu-id="0a241-106">The **New-AzVmssIpConfig** cmdlet creates an IP configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="0a241-107">Określ konfigurację tego polecenia cmdlet jako parametr *IPConfiguration* Add-AzVmssNetworkInterfaceConfiguration cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a241-107">Specify the configuration from this cmdlet as the *IPConfiguration* parameter of the Add-AzVmssNetworkInterfaceConfiguration cmdlet.</span></span>

## <span data-ttu-id="0a241-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0a241-108">EXAMPLES</span></span>

### <span data-ttu-id="0a241-109">Przykład 1. Tworzenie obiektu konfiguracji protokołu IP dla interfejsu usług VMSS</span><span class="sxs-lookup"><span data-stu-id="0a241-109">Example 1: Create an IP configuration object for a VMSS interface</span></span>
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

<span data-ttu-id="0a241-110">To polecenie tworzy obiekt konfiguracji adresu IP o nazwie ContosoVmssInterface02.</span><span class="sxs-lookup"><span data-stu-id="0a241-110">This command creates an IP configuration object named ContosoVmssInterface02.</span></span>
<span data-ttu-id="0a241-111">W poleceniu jest używany wcześniej zdefiniowany identyfikator podsieci przechowywany w $SubnetId.</span><span class="sxs-lookup"><span data-stu-id="0a241-111">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="0a241-112">Polecenie przechowuje ustawienia konfiguracji w zmiennej $IPConfiguration do późniejszego użycia z poleceniem **Add-AzVmssNetworkInterfaceConfiguration.**</span><span class="sxs-lookup"><span data-stu-id="0a241-112">The command stores the configuration settings in the $IPConfiguration variable for later use with **Add-AzVmssNetworkInterfaceConfiguration**.</span></span>

### <span data-ttu-id="0a241-113">Przykład 2. Tworzenie obiektu konfiguracji protokołu IP, który zawiera ustawienia puli NAT</span><span class="sxs-lookup"><span data-stu-id="0a241-113">Example 2: Create an IP configuration object that includes NAT pool settings</span></span>
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

<span data-ttu-id="0a241-114">To polecenie tworzy obiekt konfiguracji adresu IP o nazwie ContosoVmssInterface03, a następnie przechowuje go w $IPConfiguration do późniejszego użycia.</span><span class="sxs-lookup"><span data-stu-id="0a241-114">This command creates an IP configuration object named ContosoVmssInterface03, and then stores it in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="0a241-115">W poleceniu jest używany wcześniej zdefiniowany identyfikator podsieci przechowywany w $SubnetId.</span><span class="sxs-lookup"><span data-stu-id="0a241-115">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="0a241-116">To polecenie przechowuje ustawienia konfiguracji w $IPConfiguration do późniejszego użycia.</span><span class="sxs-lookup"><span data-stu-id="0a241-116">The command stores the configuration settings in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="0a241-117">To polecenie określa wartości parametrów *LoadBalancerInboundNatPoolsId* i *LoadBalancerBackendAddressPoolsId.*</span><span class="sxs-lookup"><span data-stu-id="0a241-117">The command specifies values for the *LoadBalancerInboundNatPoolsId* and *LoadBalancerBackendAddressPoolsId* parameters.</span></span>

## <span data-ttu-id="0a241-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a241-118">PARAMETERS</span></span>

### <span data-ttu-id="0a241-119">-ApplicationGatewayBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="0a241-119">-ApplicationGatewayBackendAddressPoolsId</span></span>
<span data-ttu-id="0a241-120">Określa tablicę odwołań do pul adresów zaplecza dla równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="0a241-120">Specifies an array of references to backend address pools of load balancers.</span></span>
<span data-ttu-id="0a241-121">Zestaw skali może odwoływać się do puli adresów wewnętrznego jednego publicznego i wewnętrznego równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="0a241-121">A scale set can reference backend address pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="0a241-122">W wielu zestawach skal nie można używać tego samego równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="0a241-122">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a241-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a241-123">-DefaultProfile</span></span>
<span data-ttu-id="0a241-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0a241-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a241-125">- DnsSetting</span><span class="sxs-lookup"><span data-stu-id="0a241-125">-DnsSetting</span></span>
<span data-ttu-id="0a241-126">Ustawienia DNS, które mają być stosowane do adresów PUBLICIP.</span><span class="sxs-lookup"><span data-stu-id="0a241-126">The dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="0a241-127">Etykieta nazwy domeny ustawień DNS, które mają być stosowane do adresów PUBLICIP.</span><span class="sxs-lookup"><span data-stu-id="0a241-127">The domain name label of the Dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="0a241-128">Concatenation of the domain name label and maszyny wirtualnej index will be the domain name labels of the Public IP Address resources that will be created.</span><span class="sxs-lookup"><span data-stu-id="0a241-128">The concatenation of the domain name label and vm index will be the domain name labels of the Public IP Address resources that will be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PublicIPAddressDomainNameLabel

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a241-129">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="0a241-129">-Id</span></span>
<span data-ttu-id="0a241-130">Określa identyfikator.</span><span class="sxs-lookup"><span data-stu-id="0a241-130">Specifies an ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a241-131">-IpTag</span><span class="sxs-lookup"><span data-stu-id="0a241-131">-IpTag</span></span>
<span data-ttu-id="0a241-132">Określa tablicę obiektów tagu ip.</span><span class="sxs-lookup"><span data-stu-id="0a241-132">Specifies an array of Ip Tag objects.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a241-133">-LoadBalancerBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="0a241-133">-LoadBalancerBackendAddressPoolsId</span></span>
<span data-ttu-id="0a241-134">Określa tablicę odwołań do pul translacji adresów sieciowych (NAT, incoming network address translation) dla równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="0a241-134">Specifies an array of references to incoming network address translation (NAT) pools of the load balancers.</span></span>
<span data-ttu-id="0a241-135">Zestaw skali może odwoływać się do przychodzących pul NAT jednego publicznego i wewnętrznego równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="0a241-135">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="0a241-136">W wielu zestawach skal nie można używać tego samego równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="0a241-136">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a241-137">-LoadBalancerInboundNatPoolsId</span><span class="sxs-lookup"><span data-stu-id="0a241-137">-LoadBalancerInboundNatPoolsId</span></span>
<span data-ttu-id="0a241-138">Określa tablicę odwołań do przychodzących pul NAT dla równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="0a241-138">Specifies an array of references to incoming NAT pools of the load balancers.</span></span>
<span data-ttu-id="0a241-139">Zestaw skali może odwoływać się do przychodzących pul NAT jednego publicznego i wewnętrznego równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="0a241-139">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="0a241-140">W wielu zestawach skal nie można używać tego samego równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="0a241-140">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a241-141">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0a241-141">-Name</span></span>
<span data-ttu-id="0a241-142">Określa nazwę konfiguracji protokołu IP.</span><span class="sxs-lookup"><span data-stu-id="0a241-142">Specifies the name of the IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a241-143">— podstawowy</span><span class="sxs-lookup"><span data-stu-id="0a241-143">-Primary</span></span>
<span data-ttu-id="0a241-144">Określa podstawową konfigurację adresów IP, jeśli interfejs sieciowy ma więcej niż jedną konfigurację adresów IP.</span><span class="sxs-lookup"><span data-stu-id="0a241-144">Specifies the primary IP Configuration in case the network interface has more than one IP Configuration.</span></span>

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

### <span data-ttu-id="0a241-145">-PrivateIPAddressVersion</span><span class="sxs-lookup"><span data-stu-id="0a241-145">-PrivateIPAddressVersion</span></span>
<span data-ttu-id="0a241-146">Określ konfigurację adresu IP dla prywatnego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="0a241-146">Specify the IP configuration for private IP address.</span></span>  <span data-ttu-id="0a241-147">Protokół IPv4 jest domyślnie przyjmowany jako protokół IPv4.</span><span class="sxs-lookup"><span data-stu-id="0a241-147">Default is taken as IPv4.</span></span>  <span data-ttu-id="0a241-148">Dopuszczalne wartości to: "IPv4" i "IPv6".</span><span class="sxs-lookup"><span data-stu-id="0a241-148">Possible values are: 'IPv4' and 'IPv6'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a241-149">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="0a241-149">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span></span>
<span data-ttu-id="0a241-150">Limit czasu bezczynności publicznego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="0a241-150">The idle timeout of the public IP address.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: PublicIPAddressIdleTimeoutInMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a241-151">-PublicIPAddressConfigurationName</span><span class="sxs-lookup"><span data-stu-id="0a241-151">-PublicIPAddressConfigurationName</span></span>
<span data-ttu-id="0a241-152">Nazwa konfiguracji publicznego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="0a241-152">The publicIP address configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PublicIPAddressName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a241-153">-PublicIPAddressVersion</span><span class="sxs-lookup"><span data-stu-id="0a241-153">-PublicIPAddressVersion</span></span>
<span data-ttu-id="0a241-154">Określ konfigurację adresu IP dla publicznego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="0a241-154">Specify the IP configuration for public IP address.</span></span>  <span data-ttu-id="0a241-155">Protokół IPv4 jest domyślnie przyjmowany jako protokół IPv4.</span><span class="sxs-lookup"><span data-stu-id="0a241-155">Default is taken as IPv4.</span></span>  <span data-ttu-id="0a241-156">Dopuszczalne wartości to: "IPv4" i "IPv6".</span><span class="sxs-lookup"><span data-stu-id="0a241-156">Possible values are: 'IPv4' and 'IPv6'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a241-157">- PublicIPPrefix</span><span class="sxs-lookup"><span data-stu-id="0a241-157">-PublicIPPrefix</span></span>
<span data-ttu-id="0a241-158">Identyfikator publicznego prefiksu IP</span><span class="sxs-lookup"><span data-stu-id="0a241-158">The ID of Public IP Prefix</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a241-159">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="0a241-159">-SubnetId</span></span>
<span data-ttu-id="0a241-160">Określa identyfikator podsieci, w którym konfiguracja tworzy interfejs sieciowy usług WIRTUALNYCH.MASZYN WIRTUALNYCH.</span><span class="sxs-lookup"><span data-stu-id="0a241-160">Specifies the subnet ID in which the configuration creates  the VMSS network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a241-161">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0a241-161">-Confirm</span></span>
<span data-ttu-id="0a241-162">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0a241-162">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a241-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a241-163">-WhatIf</span></span>
<span data-ttu-id="0a241-164">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a241-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0a241-165">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0a241-165">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a241-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a241-166">CommonParameters</span></span>
<span data-ttu-id="0a241-167">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a241-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a241-168">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0a241-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a241-169">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0a241-169">INPUTS</span></span>

### <span data-ttu-id="0a241-170">System.String</span><span class="sxs-lookup"><span data-stu-id="0a241-170">System.String</span></span>

### <span data-ttu-id="0a241-171">System.String[]</span><span class="sxs-lookup"><span data-stu-id="0a241-171">System.String[]</span></span>

### <span data-ttu-id="0a241-172">System.Int32</span><span class="sxs-lookup"><span data-stu-id="0a241-172">System.Int32</span></span>

### <span data-ttu-id="0a241-173">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]</span><span class="sxs-lookup"><span data-stu-id="0a241-173">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]</span></span>

## <span data-ttu-id="0a241-174">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0a241-174">OUTPUTS</span></span>

### <span data-ttu-id="0a241-175">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a241-175">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration</span></span>

## <span data-ttu-id="0a241-176">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0a241-176">NOTES</span></span>

## <span data-ttu-id="0a241-177">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0a241-177">RELATED LINKS</span></span>

[<span data-ttu-id="0a241-178">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a241-178">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)


