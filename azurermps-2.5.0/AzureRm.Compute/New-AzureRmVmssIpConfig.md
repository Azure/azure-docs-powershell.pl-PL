---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmssipconfig
schema: 2.0.0
ms.openlocfilehash: 82c27b6f8f926d273948bdfcb519a10ee1e0a3c7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898970"
---
# <span data-ttu-id="476c7-101">New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="476c7-101">New-AzureRmVmssIpConfig</span></span>

## <span data-ttu-id="476c7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="476c7-102">SYNOPSIS</span></span>
<span data-ttu-id="476c7-103">Tworzy konfigurację IP dla interfejsu sieciowego VMSS.</span><span class="sxs-lookup"><span data-stu-id="476c7-103">Creates an IP configuration for a network interface of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="476c7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="476c7-104">SYNTAX</span></span>

```
New-AzureRmVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-Primary] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="476c7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="476c7-105">DESCRIPTION</span></span>
<span data-ttu-id="476c7-106">Polecenie cmdlet **New-AzureRmVmssIpConfig** tworzy obiekt konfiguracji IP dla interfejsu sieciowego zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="476c7-106">The **New-AzureRmVmssIpConfig** cmdlet creates an IP configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="476c7-107">Określ konfigurację tego polecenia cmdlet jako parametr *IPConfiguration* polecenia cmdlet Add-AzureRmVmssNetworkInterfaceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="476c7-107">Specify the configuration from this cmdlet as the *IPConfiguration* parameter of the Add-AzureRmVmssNetworkInterfaceConfiguration cmdlet.</span></span>

## <span data-ttu-id="476c7-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="476c7-108">EXAMPLES</span></span>

### <span data-ttu-id="476c7-109">Przykład 1. Tworzenie obiektu konfiguracji IP dla interfejsu VMSS</span><span class="sxs-lookup"><span data-stu-id="476c7-109">Example 1: Create an IP configuration object for a VMSS interface</span></span>
```
PS C:\> $IPConfiguration = New-AzureRmVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

<span data-ttu-id="476c7-110">To polecenie tworzy obiekt konfiguracji IP o nazwie ContosoVmssInterface02.</span><span class="sxs-lookup"><span data-stu-id="476c7-110">This command creates an IP configuration object named ContosoVmssInterface02.</span></span>
<span data-ttu-id="476c7-111">W poleceniu użyto uprzednio zdefiniowanego identyfikatora podsieci przechowywanego w $SubnetId.</span><span class="sxs-lookup"><span data-stu-id="476c7-111">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="476c7-112">Polecenie zapisuje ustawienia konfiguracji w zmiennej $IPConfiguration w celu późniejszego użycia z **dodatkiem Add-AzureRmVmssNetworkInterfaceConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="476c7-112">The command stores the configuration settings in the $IPConfiguration variable for later use with **Add-AzureRmVmssNetworkInterfaceConfiguration**.</span></span>

### <span data-ttu-id="476c7-113">Przykład 2: Tworzenie obiektu konfiguracji IP zawierającego ustawienia puli NAT</span><span class="sxs-lookup"><span data-stu-id="476c7-113">Example 2: Create an IP configuration object that includes NAT pool settings</span></span>
```
PS C:\> $IPConfiguration = New-AzureRmVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

<span data-ttu-id="476c7-114">To polecenie tworzy obiekt konfiguracji IP o nazwie ContosoVmssInterface03, a następnie zapisuje go w zmiennej $IPConfiguration do późniejszego użycia.</span><span class="sxs-lookup"><span data-stu-id="476c7-114">This command creates an IP configuration object named ContosoVmssInterface03, and then stores it in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="476c7-115">W poleceniu użyto uprzednio zdefiniowanego identyfikatora podsieci przechowywanego w $SubnetId.</span><span class="sxs-lookup"><span data-stu-id="476c7-115">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="476c7-116">Polecenie zapisuje ustawienia konfiguracji w zmiennej $IPConfiguration do późniejszego użycia.</span><span class="sxs-lookup"><span data-stu-id="476c7-116">The command stores the configuration settings in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="476c7-117">Polecenie określa wartości parametrów *LoadBalancerInboundNatPoolsId* oraz *LoadBalancerBackendAddressPoolsId* .</span><span class="sxs-lookup"><span data-stu-id="476c7-117">The command specifies values for the *LoadBalancerInboundNatPoolsId* and *LoadBalancerBackendAddressPoolsId* parameters.</span></span>

## <span data-ttu-id="476c7-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="476c7-118">PARAMETERS</span></span>

### <span data-ttu-id="476c7-119">-ApplicationGatewayBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="476c7-119">-ApplicationGatewayBackendAddressPoolsId</span></span>
<span data-ttu-id="476c7-120">Określa tablicę odwołań do pul adresów zaplecza modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="476c7-120">Specifies an array of references to backend address pools of load balancers.</span></span>
<span data-ttu-id="476c7-121">Zestaw skali może odwoływać się do pul adresów zaplecza jednego publicznego i jednego wewnętrznego modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="476c7-121">A scale set can reference backend address pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="476c7-122">Wiele zestawów skali nie może korzystać z tego samego modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="476c7-122">Multiple scale sets cannot use the same load balancer.</span></span>

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

### <span data-ttu-id="476c7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="476c7-123">-DefaultProfile</span></span>
<span data-ttu-id="476c7-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="476c7-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="476c7-125">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="476c7-125">-DnsSetting</span></span>
<span data-ttu-id="476c7-126">Ustawienia DNS, które mają zostać zastosowane do adresów publicIP.</span><span class="sxs-lookup"><span data-stu-id="476c7-126">The dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="476c7-127">Etykieta nazwy domeny ustawień DNS, które mają zostać zastosowane na adres publicIP.</span><span class="sxs-lookup"><span data-stu-id="476c7-127">The domain name label of the Dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="476c7-128">Połączenie etykiety nazwy domeny i indeksu maszyny wirtualnej będzie zawierać etykiety nazw domen publicznych zasobów adresów IP, które zostaną utworzone.</span><span class="sxs-lookup"><span data-stu-id="476c7-128">The concatenation of the domain name label and vm index will be the domain name labels of the Public IP Address resources that will be created.</span></span>

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

### <span data-ttu-id="476c7-129">-ID</span><span class="sxs-lookup"><span data-stu-id="476c7-129">-Id</span></span>
<span data-ttu-id="476c7-130">Określa identyfikator.</span><span class="sxs-lookup"><span data-stu-id="476c7-130">Specifies an ID.</span></span>

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

### <span data-ttu-id="476c7-131">-LoadBalancerBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="476c7-131">-LoadBalancerBackendAddressPoolsId</span></span>
<span data-ttu-id="476c7-132">Określa tablicę odwołań do pul translacji adresów sieciowych (NAT) przychodzących modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="476c7-132">Specifies an array of references to incoming network address translation (NAT) pools of the load balancers.</span></span>
<span data-ttu-id="476c7-133">Zestaw skali może odwoływać się do pul adresów NAT przychodzących z jednego publicznego i jednego wewnętrznego modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="476c7-133">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="476c7-134">Wiele zestawów skali nie może korzystać z tego samego modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="476c7-134">Multiple scale sets cannot use the same load balancer.</span></span>

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

### <span data-ttu-id="476c7-135">-LoadBalancerInboundNatPoolsId</span><span class="sxs-lookup"><span data-stu-id="476c7-135">-LoadBalancerInboundNatPoolsId</span></span>
<span data-ttu-id="476c7-136">Określa tablicę odwołań do pul NAT przychodzących modułów równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="476c7-136">Specifies an array of references to incoming NAT pools of the load balancers.</span></span>
<span data-ttu-id="476c7-137">Zestaw skali może odwoływać się do pul adresów NAT przychodzących z jednego publicznego i jednego wewnętrznego modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="476c7-137">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="476c7-138">Wiele zestawów skali nie może korzystać z tego samego modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="476c7-138">Multiple scale sets cannot use the same load balancer.</span></span>

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

### <span data-ttu-id="476c7-139">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="476c7-139">-Name</span></span>
<span data-ttu-id="476c7-140">Określa nazwę konfiguracji adresu IP.</span><span class="sxs-lookup"><span data-stu-id="476c7-140">Specifies the name of the IP configuration.</span></span>

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

### <span data-ttu-id="476c7-141">-Primary</span><span class="sxs-lookup"><span data-stu-id="476c7-141">-Primary</span></span>
<span data-ttu-id="476c7-142">Określa podstawową konfigurację adresu IP na wypadek, gdyby interfejs sieciowy miał więcej niż jeden sposób konfiguracji IP.</span><span class="sxs-lookup"><span data-stu-id="476c7-142">Specifies the primary IP Configuration in case the network interface has more than one IP Configuration.</span></span>

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

### <span data-ttu-id="476c7-143">-PrivateIPAddressVersion</span><span class="sxs-lookup"><span data-stu-id="476c7-143">-PrivateIPAddressVersion</span></span>
<span data-ttu-id="476c7-144">Określ konfigurację adresu IP: IPv4 lub IPv6.</span><span class="sxs-lookup"><span data-stu-id="476c7-144">Specify the ip configuration is either IPv4 or IPv6.</span></span> <span data-ttu-id="476c7-145">Domyślnie przyjmowany jest protokół IPv4.</span><span class="sxs-lookup"><span data-stu-id="476c7-145">Default is taken as IPv4.</span></span>  <span data-ttu-id="476c7-146">Możliwe wartości: "IPv4" i "IPv6".</span><span class="sxs-lookup"><span data-stu-id="476c7-146">Possible values are: 'IPv4' and 'IPv6'.</span></span>

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

### <span data-ttu-id="476c7-147">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="476c7-147">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span></span>
<span data-ttu-id="476c7-148">Limit czasu bezczynności publicznego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="476c7-148">The idle timeout of the public IP address.</span></span>

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

### <span data-ttu-id="476c7-149">-PublicIPAddressConfigurationName</span><span class="sxs-lookup"><span data-stu-id="476c7-149">-PublicIPAddressConfigurationName</span></span>
<span data-ttu-id="476c7-150">Nazwa konfiguracji adresu publicIP.</span><span class="sxs-lookup"><span data-stu-id="476c7-150">The publicIP address configuration name.</span></span>

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

### <span data-ttu-id="476c7-151">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="476c7-151">-SubnetId</span></span>
<span data-ttu-id="476c7-152">Określa identyfikator podsieci, w którym konfiguracja tworzy interfejs sieciowy VMSS.</span><span class="sxs-lookup"><span data-stu-id="476c7-152">Specifies the subnet ID in which the configuration creates  the VMSS network interface.</span></span>

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

### <span data-ttu-id="476c7-153">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="476c7-153">-Confirm</span></span>
<span data-ttu-id="476c7-154">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="476c7-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="476c7-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="476c7-155">-WhatIf</span></span>
<span data-ttu-id="476c7-156">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="476c7-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="476c7-157">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="476c7-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="476c7-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="476c7-158">CommonParameters</span></span>
<span data-ttu-id="476c7-159">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="476c7-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="476c7-160">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="476c7-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="476c7-161">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="476c7-161">INPUTS</span></span>

### <span data-ttu-id="476c7-162">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="476c7-162">None</span></span>
<span data-ttu-id="476c7-163">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="476c7-163">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="476c7-164">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="476c7-164">OUTPUTS</span></span>

### <span data-ttu-id="476c7-165">Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSetIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="476c7-165">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration</span></span>

## <span data-ttu-id="476c7-166">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="476c7-166">NOTES</span></span>

## <span data-ttu-id="476c7-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="476c7-167">RELATED LINKS</span></span>

[<span data-ttu-id="476c7-168">Dodaj-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="476c7-168">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)


