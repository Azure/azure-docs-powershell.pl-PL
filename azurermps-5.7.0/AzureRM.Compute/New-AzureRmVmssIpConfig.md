---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssIpConfig.md
ms.openlocfilehash: 448f6236f5c9545ff1a1194c8103463f78a8fefd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544487"
---
# <span data-ttu-id="764a0-101">New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="764a0-101">New-AzureRmVmssIpConfig</span></span>

## <span data-ttu-id="764a0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="764a0-102">SYNOPSIS</span></span>
<span data-ttu-id="764a0-103">Tworzy konfigurację IP dla interfejsu sieciowego VMSS.</span><span class="sxs-lookup"><span data-stu-id="764a0-103">Creates an IP configuration for a network interface of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="764a0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="764a0-104">SYNTAX</span></span>

```
New-AzureRmVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="764a0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="764a0-105">DESCRIPTION</span></span>
<span data-ttu-id="764a0-106">Polecenie cmdlet **New-AzureRmVmssIpConfig** tworzy obiekt konfiguracji IP dla interfejsu sieciowego zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="764a0-106">The **New-AzureRmVmssIpConfig** cmdlet creates an IP configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="764a0-107">Określ konfigurację tego polecenia cmdlet jako parametr *IPConfiguration* polecenia cmdlet Add-AzureRmVmssNetworkInterfaceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="764a0-107">Specify the configuration from this cmdlet as the *IPConfiguration* parameter of the Add-AzureRmVmssNetworkInterfaceConfiguration cmdlet.</span></span>

## <span data-ttu-id="764a0-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="764a0-108">EXAMPLES</span></span>

### <span data-ttu-id="764a0-109">Przykład 1. Tworzenie obiektu konfiguracji IP dla interfejsu VMSS</span><span class="sxs-lookup"><span data-stu-id="764a0-109">Example 1: Create an IP configuration object for a VMSS interface</span></span>
```
PS C:\> $IPConfiguration = New-AzureRmVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

<span data-ttu-id="764a0-110">To polecenie tworzy obiekt konfiguracji IP o nazwie ContosoVmssInterface02.</span><span class="sxs-lookup"><span data-stu-id="764a0-110">This command creates an IP configuration object named ContosoVmssInterface02.</span></span>
<span data-ttu-id="764a0-111">W poleceniu użyto uprzednio zdefiniowanego identyfikatora podsieci przechowywanego w $SubnetId.</span><span class="sxs-lookup"><span data-stu-id="764a0-111">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="764a0-112">Polecenie zapisuje ustawienia konfiguracji w zmiennej $IPConfiguration w celu późniejszego użycia z **dodatkiem Add-AzureRmVmssNetworkInterfaceConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="764a0-112">The command stores the configuration settings in the $IPConfiguration variable for later use with **Add-AzureRmVmssNetworkInterfaceConfiguration**.</span></span>

### <span data-ttu-id="764a0-113">Przykład 2: Tworzenie obiektu konfiguracji IP zawierającego ustawienia puli NAT</span><span class="sxs-lookup"><span data-stu-id="764a0-113">Example 2: Create an IP configuration object that includes NAT pool settings</span></span>
```
PS C:\> $IPConfiguration = New-AzureRmVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

<span data-ttu-id="764a0-114">To polecenie tworzy obiekt konfiguracji IP o nazwie ContosoVmssInterface03, a następnie zapisuje go w zmiennej $IPConfiguration do późniejszego użycia.</span><span class="sxs-lookup"><span data-stu-id="764a0-114">This command creates an IP configuration object named ContosoVmssInterface03, and then stores it in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="764a0-115">W poleceniu użyto uprzednio zdefiniowanego identyfikatora podsieci przechowywanego w $SubnetId.</span><span class="sxs-lookup"><span data-stu-id="764a0-115">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="764a0-116">Polecenie zapisuje ustawienia konfiguracji w zmiennej $IPConfiguration do późniejszego użycia.</span><span class="sxs-lookup"><span data-stu-id="764a0-116">The command stores the configuration settings in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="764a0-117">Polecenie określa wartości parametrów *LoadBalancerInboundNatPoolsId* oraz *LoadBalancerBackendAddressPoolsId* .</span><span class="sxs-lookup"><span data-stu-id="764a0-117">The command specifies values for the *LoadBalancerInboundNatPoolsId* and *LoadBalancerBackendAddressPoolsId* parameters.</span></span>

## <span data-ttu-id="764a0-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="764a0-118">PARAMETERS</span></span>

### <span data-ttu-id="764a0-119">-ApplicationGatewayBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="764a0-119">-ApplicationGatewayBackendAddressPoolsId</span></span>
<span data-ttu-id="764a0-120">Określa tablicę odwołań do pul adresów zaplecza modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="764a0-120">Specifies an array of references to backend address pools of load balancers.</span></span>
<span data-ttu-id="764a0-121">Zestaw skali może odwoływać się do pul adresów zaplecza jednego publicznego i jednego wewnętrznego modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="764a0-121">A scale set can reference backend address pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="764a0-122">Wiele zestawów skali nie może korzystać z tego samego modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="764a0-122">Multiple scale sets cannot use the same load balancer.</span></span>

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

### <span data-ttu-id="764a0-123">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="764a0-123">-DnsSetting</span></span>
<span data-ttu-id="764a0-124">Ustawienia DNS, które mają zostać zastosowane do adresów publicIP.</span><span class="sxs-lookup"><span data-stu-id="764a0-124">The dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="764a0-125">Etykieta nazwy domeny ustawień DNS, które mają zostać zastosowane na adres publicIP.</span><span class="sxs-lookup"><span data-stu-id="764a0-125">The domain name label of the Dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="764a0-126">Połączenie etykiety nazwy domeny i indeksu maszyny wirtualnej będzie zawierać etykiety nazw domen publicznych zasobów adresów IP, które zostaną utworzone.</span><span class="sxs-lookup"><span data-stu-id="764a0-126">The concatenation of the domain name label and vm index will be the domain name labels of the Public IP Address resources that will be created.</span></span>

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

### <span data-ttu-id="764a0-127">-ID</span><span class="sxs-lookup"><span data-stu-id="764a0-127">-Id</span></span>
<span data-ttu-id="764a0-128">Określa identyfikator.</span><span class="sxs-lookup"><span data-stu-id="764a0-128">Specifies an ID.</span></span>

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

### <span data-ttu-id="764a0-129">-LoadBalancerBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="764a0-129">-LoadBalancerBackendAddressPoolsId</span></span>
<span data-ttu-id="764a0-130">Określa tablicę odwołań do pul translacji adresów sieciowych (NAT) przychodzących modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="764a0-130">Specifies an array of references to incoming network address translation (NAT) pools of the load balancers.</span></span>
<span data-ttu-id="764a0-131">Zestaw skali może odwoływać się do pul adresów NAT przychodzących z jednego publicznego i jednego wewnętrznego modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="764a0-131">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="764a0-132">Wiele zestawów skali nie może korzystać z tego samego modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="764a0-132">Multiple scale sets cannot use the same load balancer.</span></span>

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

### <span data-ttu-id="764a0-133">-LoadBalancerInboundNatPoolsId</span><span class="sxs-lookup"><span data-stu-id="764a0-133">-LoadBalancerInboundNatPoolsId</span></span>
<span data-ttu-id="764a0-134">Określa tablicę odwołań do pul NAT przychodzących modułów równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="764a0-134">Specifies an array of references to incoming NAT pools of the load balancers.</span></span>
<span data-ttu-id="764a0-135">Zestaw skali może odwoływać się do pul adresów NAT przychodzących z jednego publicznego i jednego wewnętrznego modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="764a0-135">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="764a0-136">Wiele zestawów skali nie może korzystać z tego samego modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="764a0-136">Multiple scale sets cannot use the same load balancer.</span></span>

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

### <span data-ttu-id="764a0-137">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="764a0-137">-Name</span></span>
<span data-ttu-id="764a0-138">Określa nazwę konfiguracji adresu IP.</span><span class="sxs-lookup"><span data-stu-id="764a0-138">Specifies the name of the IP configuration.</span></span>

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

### <span data-ttu-id="764a0-139">-PrivateIPAddressVersion</span><span class="sxs-lookup"><span data-stu-id="764a0-139">-PrivateIPAddressVersion</span></span>
<span data-ttu-id="764a0-140">Określ konfigurację adresu IP: IPv4 lub IPv6.</span><span class="sxs-lookup"><span data-stu-id="764a0-140">Specify the ip configuration is either IPv4 or IPv6.</span></span> <span data-ttu-id="764a0-141">Domyślnie przyjmowany jest protokół IPv4.</span><span class="sxs-lookup"><span data-stu-id="764a0-141">Default is taken as IPv4.</span></span>  <span data-ttu-id="764a0-142">Możliwe wartości: "IPv4" i "IPv6".</span><span class="sxs-lookup"><span data-stu-id="764a0-142">Possible values are: 'IPv4' and 'IPv6'.</span></span>

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

### <span data-ttu-id="764a0-143">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="764a0-143">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span></span>
<span data-ttu-id="764a0-144">Limit czasu bezczynności publicznego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="764a0-144">The idle timeout of the public IP address.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="764a0-145">-PublicIPAddressConfigurationName</span><span class="sxs-lookup"><span data-stu-id="764a0-145">-PublicIPAddressConfigurationName</span></span>
<span data-ttu-id="764a0-146">Nazwa konfiguracji adresu publicIP.</span><span class="sxs-lookup"><span data-stu-id="764a0-146">The publicIP address configuration name.</span></span>

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

### <span data-ttu-id="764a0-147">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="764a0-147">-SubnetId</span></span>
<span data-ttu-id="764a0-148">Określa identyfikator podsieci, w którym konfiguracja tworzy interfejs sieciowy VMSS.</span><span class="sxs-lookup"><span data-stu-id="764a0-148">Specifies the subnet ID in which the configuration creates  the VMSS network interface.</span></span>

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

### <span data-ttu-id="764a0-149">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="764a0-149">-Confirm</span></span>
<span data-ttu-id="764a0-150">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="764a0-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="764a0-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="764a0-151">-WhatIf</span></span>
<span data-ttu-id="764a0-152">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="764a0-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="764a0-153">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="764a0-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="764a0-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="764a0-154">CommonParameters</span></span>
<span data-ttu-id="764a0-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="764a0-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="764a0-156">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="764a0-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="764a0-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="764a0-157">INPUTS</span></span>

### <span data-ttu-id="764a0-158">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="764a0-158">None</span></span>
<span data-ttu-id="764a0-159">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="764a0-159">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="764a0-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="764a0-160">OUTPUTS</span></span>

## <span data-ttu-id="764a0-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="764a0-161">NOTES</span></span>

## <span data-ttu-id="764a0-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="764a0-162">RELATED LINKS</span></span>

[<span data-ttu-id="764a0-163">Dodaj-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="764a0-163">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)


