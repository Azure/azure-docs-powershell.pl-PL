---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
ms.openlocfilehash: 271d4c9d9fd4a7eb34d4ced4b32dc3929a32b31b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706310"
---
# <span data-ttu-id="78028-101">New-AzVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="78028-101">New-AzVmssIpConfig</span></span>

## <span data-ttu-id="78028-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="78028-102">SYNOPSIS</span></span>
<span data-ttu-id="78028-103">Tworzy konfigurację IP dla interfejsu sieciowego VMSS.</span><span class="sxs-lookup"><span data-stu-id="78028-103">Creates an IP configuration for a network interface of a VMSS.</span></span>

## <span data-ttu-id="78028-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="78028-104">SYNTAX</span></span>

```
New-AzVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-Primary] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-IpTag <VirtualMachineScaleSetIpTag[]>] [-PublicIPPrefix <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78028-105">Opis</span><span class="sxs-lookup"><span data-stu-id="78028-105">DESCRIPTION</span></span>
<span data-ttu-id="78028-106">Polecenie cmdlet **New-AzVmssIpConfig** tworzy obiekt konfiguracji IP dla interfejsu sieciowego zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="78028-106">The **New-AzVmssIpConfig** cmdlet creates an IP configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="78028-107">Określ konfigurację tego polecenia cmdlet jako parametr *IPConfiguration* polecenia cmdlet Add-AzVmssNetworkInterfaceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="78028-107">Specify the configuration from this cmdlet as the *IPConfiguration* parameter of the Add-AzVmssNetworkInterfaceConfiguration cmdlet.</span></span>

## <span data-ttu-id="78028-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="78028-108">EXAMPLES</span></span>

### <span data-ttu-id="78028-109">Przykład 1. Tworzenie obiektu konfiguracji IP dla interfejsu VMSS</span><span class="sxs-lookup"><span data-stu-id="78028-109">Example 1: Create an IP configuration object for a VMSS interface</span></span>
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

<span data-ttu-id="78028-110">To polecenie tworzy obiekt konfiguracji IP o nazwie ContosoVmssInterface02.</span><span class="sxs-lookup"><span data-stu-id="78028-110">This command creates an IP configuration object named ContosoVmssInterface02.</span></span>
<span data-ttu-id="78028-111">W poleceniu użyto uprzednio zdefiniowanego identyfikatora podsieci przechowywanego w $SubnetId.</span><span class="sxs-lookup"><span data-stu-id="78028-111">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="78028-112">Polecenie zapisuje ustawienia konfiguracji w zmiennej $IPConfiguration w celu późniejszego użycia z **dodatkiem Add-AzVmssNetworkInterfaceConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="78028-112">The command stores the configuration settings in the $IPConfiguration variable for later use with **Add-AzVmssNetworkInterfaceConfiguration**.</span></span>

### <span data-ttu-id="78028-113">Przykład 2: Tworzenie obiektu konfiguracji IP zawierającego ustawienia puli NAT</span><span class="sxs-lookup"><span data-stu-id="78028-113">Example 2: Create an IP configuration object that includes NAT pool settings</span></span>
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

<span data-ttu-id="78028-114">To polecenie tworzy obiekt konfiguracji IP o nazwie ContosoVmssInterface03, a następnie zapisuje go w zmiennej $IPConfiguration do późniejszego użycia.</span><span class="sxs-lookup"><span data-stu-id="78028-114">This command creates an IP configuration object named ContosoVmssInterface03, and then stores it in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="78028-115">W poleceniu użyto uprzednio zdefiniowanego identyfikatora podsieci przechowywanego w $SubnetId.</span><span class="sxs-lookup"><span data-stu-id="78028-115">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="78028-116">Polecenie zapisuje ustawienia konfiguracji w zmiennej $IPConfiguration do późniejszego użycia.</span><span class="sxs-lookup"><span data-stu-id="78028-116">The command stores the configuration settings in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="78028-117">Polecenie określa wartości parametrów *LoadBalancerInboundNatPoolsId* oraz *LoadBalancerBackendAddressPoolsId* .</span><span class="sxs-lookup"><span data-stu-id="78028-117">The command specifies values for the *LoadBalancerInboundNatPoolsId* and *LoadBalancerBackendAddressPoolsId* parameters.</span></span>

## <span data-ttu-id="78028-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="78028-118">PARAMETERS</span></span>

### <span data-ttu-id="78028-119">-ApplicationGatewayBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="78028-119">-ApplicationGatewayBackendAddressPoolsId</span></span>
<span data-ttu-id="78028-120">Określa tablicę odwołań do pul adresów zaplecza modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="78028-120">Specifies an array of references to backend address pools of load balancers.</span></span>
<span data-ttu-id="78028-121">Zestaw skali może odwoływać się do pul adresów zaplecza jednego publicznego i jednego wewnętrznego modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="78028-121">A scale set can reference backend address pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="78028-122">Wiele zestawów skali nie może korzystać z tego samego modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="78028-122">Multiple scale sets cannot use the same load balancer.</span></span>

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

### <span data-ttu-id="78028-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78028-123">-DefaultProfile</span></span>
<span data-ttu-id="78028-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="78028-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78028-125">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="78028-125">-DnsSetting</span></span>
<span data-ttu-id="78028-126">Ustawienia DNS, które mają zostać zastosowane do adresów publicIP.</span><span class="sxs-lookup"><span data-stu-id="78028-126">The dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="78028-127">Etykieta nazwy domeny ustawień DNS, które mają zostać zastosowane na adres publicIP.</span><span class="sxs-lookup"><span data-stu-id="78028-127">The domain name label of the Dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="78028-128">Połączenie etykiety nazwy domeny i indeksu maszyny wirtualnej będzie zawierać etykiety nazw domen publicznych zasobów adresów IP, które zostaną utworzone.</span><span class="sxs-lookup"><span data-stu-id="78028-128">The concatenation of the domain name label and vm index will be the domain name labels of the Public IP Address resources that will be created.</span></span>

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

### <span data-ttu-id="78028-129">-ID</span><span class="sxs-lookup"><span data-stu-id="78028-129">-Id</span></span>
<span data-ttu-id="78028-130">Określa identyfikator.</span><span class="sxs-lookup"><span data-stu-id="78028-130">Specifies an ID.</span></span>

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

### <span data-ttu-id="78028-131">-IpTag</span><span class="sxs-lookup"><span data-stu-id="78028-131">-IpTag</span></span>
<span data-ttu-id="78028-132">Określa tablicę obiektów tagów IP.</span><span class="sxs-lookup"><span data-stu-id="78028-132">Specifies an array of Ip Tag objects.</span></span>

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

### <span data-ttu-id="78028-133">-LoadBalancerBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="78028-133">-LoadBalancerBackendAddressPoolsId</span></span>
<span data-ttu-id="78028-134">Określa tablicę odwołań do pul translacji adresów sieciowych (NAT) przychodzących modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="78028-134">Specifies an array of references to incoming network address translation (NAT) pools of the load balancers.</span></span>
<span data-ttu-id="78028-135">Zestaw skali może odwoływać się do pul adresów NAT przychodzących z jednego publicznego i jednego wewnętrznego modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="78028-135">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="78028-136">Wiele zestawów skali nie może korzystać z tego samego modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="78028-136">Multiple scale sets cannot use the same load balancer.</span></span>

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

### <span data-ttu-id="78028-137">-LoadBalancerInboundNatPoolsId</span><span class="sxs-lookup"><span data-stu-id="78028-137">-LoadBalancerInboundNatPoolsId</span></span>
<span data-ttu-id="78028-138">Określa tablicę odwołań do pul NAT przychodzących modułów równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="78028-138">Specifies an array of references to incoming NAT pools of the load balancers.</span></span>
<span data-ttu-id="78028-139">Zestaw skali może odwoływać się do pul adresów NAT przychodzących z jednego publicznego i jednego wewnętrznego modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="78028-139">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="78028-140">Wiele zestawów skali nie może korzystać z tego samego modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="78028-140">Multiple scale sets cannot use the same load balancer.</span></span>

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

### <span data-ttu-id="78028-141">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="78028-141">-Name</span></span>
<span data-ttu-id="78028-142">Określa nazwę konfiguracji adresu IP.</span><span class="sxs-lookup"><span data-stu-id="78028-142">Specifies the name of the IP configuration.</span></span>

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

### <span data-ttu-id="78028-143">-Primary</span><span class="sxs-lookup"><span data-stu-id="78028-143">-Primary</span></span>
<span data-ttu-id="78028-144">Określa podstawową konfigurację adresu IP na wypadek, gdyby interfejs sieciowy miał więcej niż jeden sposób konfiguracji IP.</span><span class="sxs-lookup"><span data-stu-id="78028-144">Specifies the primary IP Configuration in case the network interface has more than one IP Configuration.</span></span>

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

### <span data-ttu-id="78028-145">-PrivateIPAddressVersion</span><span class="sxs-lookup"><span data-stu-id="78028-145">-PrivateIPAddressVersion</span></span>
<span data-ttu-id="78028-146">Określ konfigurację adresu IP: IPv4 lub IPv6.</span><span class="sxs-lookup"><span data-stu-id="78028-146">Specify the ip configuration is either IPv4 or IPv6.</span></span> <span data-ttu-id="78028-147">Domyślnie przyjmowany jest protokół IPv4.</span><span class="sxs-lookup"><span data-stu-id="78028-147">Default is taken as IPv4.</span></span>  <span data-ttu-id="78028-148">Możliwe wartości: "IPv4" i "IPv6".</span><span class="sxs-lookup"><span data-stu-id="78028-148">Possible values are: 'IPv4' and 'IPv6'.</span></span>

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

### <span data-ttu-id="78028-149">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="78028-149">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span></span>
<span data-ttu-id="78028-150">Limit czasu bezczynności publicznego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="78028-150">The idle timeout of the public IP address.</span></span>

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

### <span data-ttu-id="78028-151">-PublicIPAddressConfigurationName</span><span class="sxs-lookup"><span data-stu-id="78028-151">-PublicIPAddressConfigurationName</span></span>
<span data-ttu-id="78028-152">Nazwa konfiguracji adresu publicIP.</span><span class="sxs-lookup"><span data-stu-id="78028-152">The publicIP address configuration name.</span></span>

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

### <span data-ttu-id="78028-153">-PublicIPPrefix</span><span class="sxs-lookup"><span data-stu-id="78028-153">-PublicIPPrefix</span></span>
<span data-ttu-id="78028-154">Identyfikator publicznego prefiksu adresu IP</span><span class="sxs-lookup"><span data-stu-id="78028-154">The ID of Public IP Prefix</span></span>

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

### <span data-ttu-id="78028-155">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="78028-155">-SubnetId</span></span>
<span data-ttu-id="78028-156">Określa identyfikator podsieci, w którym konfiguracja tworzy interfejs sieciowy VMSS.</span><span class="sxs-lookup"><span data-stu-id="78028-156">Specifies the subnet ID in which the configuration creates  the VMSS network interface.</span></span>

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

### <span data-ttu-id="78028-157">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="78028-157">-Confirm</span></span>
<span data-ttu-id="78028-158">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78028-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78028-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78028-159">-WhatIf</span></span>
<span data-ttu-id="78028-160">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78028-160">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="78028-161">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="78028-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78028-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78028-162">CommonParameters</span></span>
<span data-ttu-id="78028-163">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78028-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78028-164">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78028-164">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78028-165">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78028-165">INPUTS</span></span>

### <span data-ttu-id="78028-166">System. String</span><span class="sxs-lookup"><span data-stu-id="78028-166">System.String</span></span>

### <span data-ttu-id="78028-167">System. String []</span><span class="sxs-lookup"><span data-stu-id="78028-167">System.String[]</span></span>

### <span data-ttu-id="78028-168">System. Int32</span><span class="sxs-lookup"><span data-stu-id="78028-168">System.Int32</span></span>

### <span data-ttu-id="78028-169">Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSetIpTag []</span><span class="sxs-lookup"><span data-stu-id="78028-169">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]</span></span>

## <span data-ttu-id="78028-170">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="78028-170">OUTPUTS</span></span>

### <span data-ttu-id="78028-171">Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSetIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="78028-171">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration</span></span>

## <span data-ttu-id="78028-172">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="78028-172">NOTES</span></span>

## <span data-ttu-id="78028-173">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="78028-173">RELATED LINKS</span></span>

[<span data-ttu-id="78028-174">Dodaj-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="78028-174">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)


