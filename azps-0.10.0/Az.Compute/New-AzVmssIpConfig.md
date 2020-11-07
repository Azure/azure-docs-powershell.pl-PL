---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmssIpConfig.md
ms.openlocfilehash: 41b176d5952e9a33d0d0868b97fc71a14d6b43d8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893602"
---
# <span data-ttu-id="f2921-101">New-AzVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="f2921-101">New-AzVmssIpConfig</span></span>

## <span data-ttu-id="f2921-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f2921-102">SYNOPSIS</span></span>
<span data-ttu-id="f2921-103">Tworzy konfigurację IP dla interfejsu sieciowego VMSS.</span><span class="sxs-lookup"><span data-stu-id="f2921-103">Creates an IP configuration for a network interface of a VMSS.</span></span>

## <span data-ttu-id="f2921-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f2921-104">SYNTAX</span></span>

```
New-AzVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-Primary] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2921-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f2921-105">DESCRIPTION</span></span>
<span data-ttu-id="f2921-106">Polecenie cmdlet **New-AzVmssIpConfig** tworzy obiekt konfiguracji IP dla interfejsu sieciowego zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="f2921-106">The **New-AzVmssIpConfig** cmdlet creates an IP configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="f2921-107">Określ konfigurację tego polecenia cmdlet jako parametr *IPConfiguration* polecenia cmdlet Add-AzVmssNetworkInterfaceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f2921-107">Specify the configuration from this cmdlet as the *IPConfiguration* parameter of the Add-AzVmssNetworkInterfaceConfiguration cmdlet.</span></span>

## <span data-ttu-id="f2921-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f2921-108">EXAMPLES</span></span>

### <span data-ttu-id="f2921-109">Przykład 1. Tworzenie obiektu konfiguracji IP dla interfejsu VMSS</span><span class="sxs-lookup"><span data-stu-id="f2921-109">Example 1: Create an IP configuration object for a VMSS interface</span></span>
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

<span data-ttu-id="f2921-110">To polecenie tworzy obiekt konfiguracji IP o nazwie ContosoVmssInterface02.</span><span class="sxs-lookup"><span data-stu-id="f2921-110">This command creates an IP configuration object named ContosoVmssInterface02.</span></span>
<span data-ttu-id="f2921-111">W poleceniu użyto uprzednio zdefiniowanego identyfikatora podsieci przechowywanego w $SubnetId.</span><span class="sxs-lookup"><span data-stu-id="f2921-111">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="f2921-112">Polecenie zapisuje ustawienia konfiguracji w zmiennej $IPConfiguration w celu późniejszego użycia z **dodatkiem Add-AzVmssNetworkInterfaceConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="f2921-112">The command stores the configuration settings in the $IPConfiguration variable for later use with **Add-AzVmssNetworkInterfaceConfiguration**.</span></span>

### <span data-ttu-id="f2921-113">Przykład 2: Tworzenie obiektu konfiguracji IP zawierającego ustawienia puli NAT</span><span class="sxs-lookup"><span data-stu-id="f2921-113">Example 2: Create an IP configuration object that includes NAT pool settings</span></span>
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

<span data-ttu-id="f2921-114">To polecenie tworzy obiekt konfiguracji IP o nazwie ContosoVmssInterface03, a następnie zapisuje go w zmiennej $IPConfiguration do późniejszego użycia.</span><span class="sxs-lookup"><span data-stu-id="f2921-114">This command creates an IP configuration object named ContosoVmssInterface03, and then stores it in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="f2921-115">W poleceniu użyto uprzednio zdefiniowanego identyfikatora podsieci przechowywanego w $SubnetId.</span><span class="sxs-lookup"><span data-stu-id="f2921-115">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="f2921-116">Polecenie zapisuje ustawienia konfiguracji w zmiennej $IPConfiguration do późniejszego użycia.</span><span class="sxs-lookup"><span data-stu-id="f2921-116">The command stores the configuration settings in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="f2921-117">Polecenie określa wartości parametrów *LoadBalancerInboundNatPoolsId* oraz *LoadBalancerBackendAddressPoolsId* .</span><span class="sxs-lookup"><span data-stu-id="f2921-117">The command specifies values for the *LoadBalancerInboundNatPoolsId* and *LoadBalancerBackendAddressPoolsId* parameters.</span></span>

## <span data-ttu-id="f2921-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f2921-118">PARAMETERS</span></span>

### <span data-ttu-id="f2921-119">-ApplicationGatewayBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="f2921-119">-ApplicationGatewayBackendAddressPoolsId</span></span>
<span data-ttu-id="f2921-120">Określa tablicę odwołań do pul adresów zaplecza modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="f2921-120">Specifies an array of references to backend address pools of load balancers.</span></span>
<span data-ttu-id="f2921-121">Zestaw skali może odwoływać się do pul adresów zaplecza jednego publicznego i jednego wewnętrznego modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="f2921-121">A scale set can reference backend address pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="f2921-122">Wiele zestawów skali nie może korzystać z tego samego modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="f2921-122">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2921-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2921-123">-DefaultProfile</span></span>
<span data-ttu-id="f2921-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f2921-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2921-125">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="f2921-125">-DnsSetting</span></span>
<span data-ttu-id="f2921-126">Ustawienia DNS, które mają zostać zastosowane do adresów publicIP.</span><span class="sxs-lookup"><span data-stu-id="f2921-126">The dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="f2921-127">Etykieta nazwy domeny ustawień DNS, które mają zostać zastosowane na adres publicIP.</span><span class="sxs-lookup"><span data-stu-id="f2921-127">The domain name label of the Dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="f2921-128">Połączenie etykiety nazwy domeny i indeksu maszyny wirtualnej będzie zawierać etykiety nazw domen publicznych zasobów adresów IP, które zostaną utworzone.</span><span class="sxs-lookup"><span data-stu-id="f2921-128">The concatenation of the domain name label and vm index will be the domain name labels of the Public IP Address resources that will be created.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: PublicIPAddressDomainNameLabel

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2921-129">-ID</span><span class="sxs-lookup"><span data-stu-id="f2921-129">-Id</span></span>
<span data-ttu-id="f2921-130">Określa identyfikator.</span><span class="sxs-lookup"><span data-stu-id="f2921-130">Specifies an ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2921-131">-LoadBalancerBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="f2921-131">-LoadBalancerBackendAddressPoolsId</span></span>
<span data-ttu-id="f2921-132">Określa tablicę odwołań do pul translacji adresów sieciowych (NAT) przychodzących modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="f2921-132">Specifies an array of references to incoming network address translation (NAT) pools of the load balancers.</span></span>
<span data-ttu-id="f2921-133">Zestaw skali może odwoływać się do pul adresów NAT przychodzących z jednego publicznego i jednego wewnętrznego modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="f2921-133">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="f2921-134">Wiele zestawów skali nie może korzystać z tego samego modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="f2921-134">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2921-135">-LoadBalancerInboundNatPoolsId</span><span class="sxs-lookup"><span data-stu-id="f2921-135">-LoadBalancerInboundNatPoolsId</span></span>
<span data-ttu-id="f2921-136">Określa tablicę odwołań do pul NAT przychodzących modułów równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="f2921-136">Specifies an array of references to incoming NAT pools of the load balancers.</span></span>
<span data-ttu-id="f2921-137">Zestaw skali może odwoływać się do pul adresów NAT przychodzących z jednego publicznego i jednego wewnętrznego modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="f2921-137">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="f2921-138">Wiele zestawów skali nie może korzystać z tego samego modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="f2921-138">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2921-139">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f2921-139">-Name</span></span>
<span data-ttu-id="f2921-140">Określa nazwę konfiguracji adresu IP.</span><span class="sxs-lookup"><span data-stu-id="f2921-140">Specifies the name of the IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2921-141">-Primary</span><span class="sxs-lookup"><span data-stu-id="f2921-141">-Primary</span></span>
<span data-ttu-id="f2921-142">Określa podstawową konfigurację adresu IP na wypadek, gdyby interfejs sieciowy miał więcej niż jeden sposób konfiguracji IP.</span><span class="sxs-lookup"><span data-stu-id="f2921-142">Specifies the primary IP Configuration in case the network interface has more than one IP Configuration.</span></span>

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

### <span data-ttu-id="f2921-143">-PrivateIPAddressVersion</span><span class="sxs-lookup"><span data-stu-id="f2921-143">-PrivateIPAddressVersion</span></span>
<span data-ttu-id="f2921-144">Określ konfigurację adresu IP: IPv4 lub IPv6.</span><span class="sxs-lookup"><span data-stu-id="f2921-144">Specify the ip configuration is either IPv4 or IPv6.</span></span> <span data-ttu-id="f2921-145">Domyślnie przyjmowany jest protokół IPv4.</span><span class="sxs-lookup"><span data-stu-id="f2921-145">Default is taken as IPv4.</span></span>  <span data-ttu-id="f2921-146">Możliwe wartości: "IPv4" i "IPv6".</span><span class="sxs-lookup"><span data-stu-id="f2921-146">Possible values are: 'IPv4' and 'IPv6'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2921-147">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="f2921-147">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span></span>
<span data-ttu-id="f2921-148">Limit czasu bezczynności publicznego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="f2921-148">The idle timeout of the public IP address.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: PublicIPAddressIdleTimeoutInMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2921-149">-PublicIPAddressConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f2921-149">-PublicIPAddressConfigurationName</span></span>
<span data-ttu-id="f2921-150">Nazwa konfiguracji adresu publicIP.</span><span class="sxs-lookup"><span data-stu-id="f2921-150">The publicIP address configuration name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: PublicIPAddressName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2921-151">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="f2921-151">-SubnetId</span></span>
<span data-ttu-id="f2921-152">Określa identyfikator podsieci, w którym konfiguracja tworzy interfejs sieciowy VMSS.</span><span class="sxs-lookup"><span data-stu-id="f2921-152">Specifies the subnet ID in which the configuration creates  the VMSS network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2921-153">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f2921-153">-Confirm</span></span>
<span data-ttu-id="f2921-154">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2921-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2921-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2921-155">-WhatIf</span></span>
<span data-ttu-id="f2921-156">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2921-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f2921-157">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f2921-157">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2921-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2921-158">CommonParameters</span></span>
<span data-ttu-id="f2921-159">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2921-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2921-160">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2921-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2921-161">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2921-161">INPUTS</span></span>

### <span data-ttu-id="f2921-162">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f2921-162">None</span></span>
<span data-ttu-id="f2921-163">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="f2921-163">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f2921-164">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f2921-164">OUTPUTS</span></span>

### <span data-ttu-id="f2921-165">Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSetIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f2921-165">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration</span></span>

## <span data-ttu-id="f2921-166">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f2921-166">NOTES</span></span>

## <span data-ttu-id="f2921-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f2921-167">RELATED LINKS</span></span>

[<span data-ttu-id="f2921-168">Dodaj-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="f2921-168">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)


