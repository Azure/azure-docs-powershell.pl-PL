---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C23BEF37-D472-43EC-90AA-F8742247ABA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: bd8a5ef28d9ccc168df86d542156f709add87f52
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869560"
---
# <span data-ttu-id="7ec1a-101">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7ec1a-101">Set-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="7ec1a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7ec1a-102">SYNOPSIS</span></span>
<span data-ttu-id="7ec1a-103">Umożliwia zaktualizowanie konfiguracji adresu IP frontonu dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7ec1a-103">Updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="7ec1a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7ec1a-104">SYNTAX</span></span>

### <span data-ttu-id="7ec1a-105">SetByResourceSubnet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7ec1a-105">SetByResourceSubnet (Default)</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ec1a-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="7ec1a-106">SetByResourceIdSubnet</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ec1a-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7ec1a-107">SetByResourceIdPublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7ec1a-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7ec1a-108">SetByResourcePublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7ec1a-109">Opis</span><span class="sxs-lookup"><span data-stu-id="7ec1a-109">DESCRIPTION</span></span>
<span data-ttu-id="7ec1a-110">Polecenie cmdlet **Set-AzLoadBalancerFrontendIpConfig** umożliwia zaktualizowanie konfiguracji adresu IP frontonu dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7ec1a-110">The **Set-AzLoadBalancerFrontendIpConfig** cmdlet updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="7ec1a-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7ec1a-111">EXAMPLES</span></span>

### <span data-ttu-id="7ec1a-112">Przykład 1: modyfikowanie konfiguracji adresu IP frontonu modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="7ec1a-112">Example 1: Modify the front-end IP configuration of a load balancer</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "Subnet"
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
```

<span data-ttu-id="7ec1a-113">Pierwsze polecenie uzyskuje podsieć wirtualną o nazwie Subnet, a następnie zapisuje ją w zmiennej $Subnet.</span><span class="sxs-lookup"><span data-stu-id="7ec1a-113">The first command gets the virtual subnet named Subnet, and then stores it in the $Subnet variable.</span></span>
<span data-ttu-id="7ec1a-114">Drugie polecenie uzyskuje skojarzony moduł równoważenia obciążenia o nazwie MyLoadBalancer, a następnie zapisuje go w zmiennej $slb.</span><span class="sxs-lookup"><span data-stu-id="7ec1a-114">The second command gets the associated load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="7ec1a-115">W trzecim poleceniu jest używany operator potoku umożliwiający przekazanie modułu równoważenia obciążenia w $slb do polecenia Add-AzLoadBalancerFrontendIpConfig, które powoduje utworzenie zewnętrznej konfiguracji adresu IP o nazwie NewFrontend dla $slb.</span><span class="sxs-lookup"><span data-stu-id="7ec1a-115">The third command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerFrontendIpConfig, which creates a front-end IP configuration named NewFrontend for $slb.</span></span>
<span data-ttu-id="7ec1a-116">Czwarte polecenie przekazuje moduł równoważenia obciążenia w $slb do polecenia **Set-AzLoadBalancerFrontendIpConfig** , które umożliwia zapisywanie i aktualizowanie konfiguracji frontonu IP.</span><span class="sxs-lookup"><span data-stu-id="7ec1a-116">The fourth command passes the load balancer in $slb to **Set-AzLoadBalancerFrontendIpConfig** , which saves and updates the front-end IP configuration.</span></span>

## <span data-ttu-id="7ec1a-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7ec1a-117">PARAMETERS</span></span>

### <span data-ttu-id="7ec1a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ec1a-118">-DefaultProfile</span></span>
<span data-ttu-id="7ec1a-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7ec1a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ec1a-120">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="7ec1a-120">-LoadBalancer</span></span>
<span data-ttu-id="7ec1a-121">Umożliwia określenie modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7ec1a-121">Specifies a load balancer.</span></span>
<span data-ttu-id="7ec1a-122">To polecenie cmdlet powoduje zaktualizowanie konfiguracji frontonu dla modułu równoważenia obciążenia, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="7ec1a-122">This cmdlet updates a front-end configuration for the load balancer that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ec1a-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7ec1a-123">-Name</span></span>
<span data-ttu-id="7ec1a-124">Określa nazwę konfiguracji adresu IP frontonu do ustawienia.</span><span class="sxs-lookup"><span data-stu-id="7ec1a-124">Specifies the name of the front-end IP configuration to set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ec1a-125">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="7ec1a-125">-PrivateIpAddress</span></span>
<span data-ttu-id="7ec1a-126">Określa prywatny adres IP modułu równoważenia obciążenia, który jest skojarzony z konfiguracją frontonu IP do ustawienia.</span><span class="sxs-lookup"><span data-stu-id="7ec1a-126">Specifies the private IP address of the load balancer that is associated with the front-end IP configuration to set.</span></span>
<span data-ttu-id="7ec1a-127">Ten parametr należy określić tylko wtedy, gdy jest określany również parametr *Subnet* .</span><span class="sxs-lookup"><span data-stu-id="7ec1a-127">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ec1a-128">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="7ec1a-128">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="7ec1a-129">Prywatny adres IP konfiguracji protokołu IP.</span><span class="sxs-lookup"><span data-stu-id="7ec1a-129">The private IP address version of the IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ec1a-130">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7ec1a-130">-PublicIpAddress</span></span>
<span data-ttu-id="7ec1a-131">Określa obiekt **PublicIpAddress** , który jest skojarzony z konfiguracją frontonu IP do ustawienia.</span><span class="sxs-lookup"><span data-stu-id="7ec1a-131">Specifies the **PublicIpAddress** object that is associated with the front-end IP configuration to set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ec1a-132">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="7ec1a-132">-PublicIpAddressId</span></span>
<span data-ttu-id="7ec1a-133">Określa identyfikator obiektu **PublicIpAddress** skojarzonego z konfiguracją adresu IP frontonu, którą ustawia to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ec1a-133">Specifies the ID of the **PublicIpAddress** object that is associated with the front-end IP configuration that this cmdlet sets.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ec1a-134">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="7ec1a-134">-Subnet</span></span>
<span data-ttu-id="7ec1a-135">Określa obiekt **podsieci** , który zawiera konfigurację adresu IP frontonu ustawianą przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ec1a-135">Specifies the **Subnet** object that contains the front-end IP configuration that this cmdlet sets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ec1a-136">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="7ec1a-136">-SubnetId</span></span>
<span data-ttu-id="7ec1a-137">Określa identyfikator podsieci, w której znajduje się konfiguracja frontonu IP, która jest ustawiana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ec1a-137">Specifies the ID of the subnet that contains the front-end IP configuration that this cmdlet sets.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ec1a-138">-Zone</span><span class="sxs-lookup"><span data-stu-id="7ec1a-138">-Zone</span></span>
<span data-ttu-id="7ec1a-139">Lista stref dostępności oznaczająca adres IP przydzielony dla zasobu musi pochodzić od.</span><span class="sxs-lookup"><span data-stu-id="7ec1a-139">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ec1a-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7ec1a-140">-Confirm</span></span>
<span data-ttu-id="7ec1a-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ec1a-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ec1a-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ec1a-142">-WhatIf</span></span>
<span data-ttu-id="7ec1a-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ec1a-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7ec1a-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7ec1a-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ec1a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ec1a-145">CommonParameters</span></span>
<span data-ttu-id="7ec1a-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ec1a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ec1a-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ec1a-147">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ec1a-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7ec1a-148">INPUTS</span></span>

### <span data-ttu-id="7ec1a-149">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7ec1a-149">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="7ec1a-150">System. String</span><span class="sxs-lookup"><span data-stu-id="7ec1a-150">System.String</span></span>

### <span data-ttu-id="7ec1a-151">System. String []</span><span class="sxs-lookup"><span data-stu-id="7ec1a-151">System.String[]</span></span>

### <span data-ttu-id="7ec1a-152">Microsoft. Azure. Commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="7ec1a-152">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="7ec1a-153">Microsoft. Azure. Commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7ec1a-153">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="7ec1a-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7ec1a-154">OUTPUTS</span></span>

### <span data-ttu-id="7ec1a-155">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7ec1a-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="7ec1a-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7ec1a-156">NOTES</span></span>

## <span data-ttu-id="7ec1a-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7ec1a-157">RELATED LINKS</span></span>

[<span data-ttu-id="7ec1a-158">Dodaj-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7ec1a-158">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="7ec1a-159">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7ec1a-159">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="7ec1a-160">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7ec1a-160">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="7ec1a-161">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7ec1a-161">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="7ec1a-162">Nowe — AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7ec1a-162">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="7ec1a-163">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7ec1a-163">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)


