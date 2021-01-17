---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C23BEF37-D472-43EC-90AA-F8742247ABA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: a16b625c4624753943659ba796b169ef338888f2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356671"
---
# <span data-ttu-id="b4800-101">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b4800-101">Set-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="b4800-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b4800-102">SYNOPSIS</span></span>
<span data-ttu-id="b4800-103">Umożliwia zaktualizowanie konfiguracji adresu IP frontonu dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="b4800-103">Updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="b4800-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b4800-104">SYNTAX</span></span>

### <span data-ttu-id="b4800-105">SetByResourceSubnet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b4800-105">SetByResourceSubnet (Default)</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4800-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="b4800-106">SetByResourceIdSubnet</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4800-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b4800-107">SetByResourceIdPublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4800-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b4800-108">SetByResourcePublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4800-109">SetByResourceIdPublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b4800-109">SetByResourceIdPublicIpAddressPrefix</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressPrefixId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4800-110">SetByResourcePublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b4800-110">SetByResourcePublicIpAddressPrefix</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressPrefix <PSPublicIpPrefix> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b4800-111">Opis</span><span class="sxs-lookup"><span data-stu-id="b4800-111">DESCRIPTION</span></span>
<span data-ttu-id="b4800-112">Polecenie cmdlet **Set-AzLoadBalancerFrontendIpConfig** umożliwia zaktualizowanie konfiguracji adresu IP frontonu dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="b4800-112">The **Set-AzLoadBalancerFrontendIpConfig** cmdlet updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="b4800-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b4800-113">EXAMPLES</span></span>

### <span data-ttu-id="b4800-114">Przykład 1: modyfikowanie konfiguracji adresu IP frontonu modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="b4800-114">Example 1: Modify the front-end IP configuration of a load balancer</span></span>
```powershell
PS C:\> $Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "Subnet"
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="b4800-115">Pierwsze polecenie uzyskuje podsieć wirtualną o nazwie Subnet, a następnie zapisuje ją w zmiennej $Subnet.</span><span class="sxs-lookup"><span data-stu-id="b4800-115">The first command gets the virtual subnet named Subnet, and then stores it in the $Subnet variable.</span></span>
<span data-ttu-id="b4800-116">Drugie polecenie uzyskuje skojarzony moduł równoważenia obciążenia o nazwie MyLoadBalancer, a następnie zapisuje go w zmiennej $slb.</span><span class="sxs-lookup"><span data-stu-id="b4800-116">The second command gets the associated load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="b4800-117">W trzecim poleceniu jest używany operator potoku umożliwiający przekazanie modułu równoważenia obciążenia w $slb do polecenia Add-AzLoadBalancerFrontendIpConfig, które powoduje utworzenie zewnętrznej konfiguracji adresu IP o nazwie NewFrontend dla $slb.</span><span class="sxs-lookup"><span data-stu-id="b4800-117">The third command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerFrontendIpConfig, which creates a front-end IP configuration named NewFrontend for $slb.</span></span>
<span data-ttu-id="b4800-118">Czwarte polecenie przekazuje moduł równoważenia obciążenia w $slb do polecenia **Set-AzLoadBalancerFrontendIpConfig**, które umożliwia zapisywanie i aktualizowanie konfiguracji frontonu IP.</span><span class="sxs-lookup"><span data-stu-id="b4800-118">The fourth command passes the load balancer in $slb to **Set-AzLoadBalancerFrontendIpConfig**, which saves and updates the front-end IP configuration.</span></span>

## <span data-ttu-id="b4800-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b4800-119">PARAMETERS</span></span>

### <span data-ttu-id="b4800-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4800-120">-DefaultProfile</span></span>
<span data-ttu-id="b4800-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b4800-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4800-122">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="b4800-122">-LoadBalancer</span></span>
<span data-ttu-id="b4800-123">Umożliwia określenie modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="b4800-123">Specifies a load balancer.</span></span>
<span data-ttu-id="b4800-124">To polecenie cmdlet powoduje zaktualizowanie konfiguracji frontonu dla modułu równoważenia obciążenia, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="b4800-124">This cmdlet updates a front-end configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="b4800-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b4800-125">-Name</span></span>
<span data-ttu-id="b4800-126">Określa nazwę konfiguracji adresu IP frontonu do ustawienia.</span><span class="sxs-lookup"><span data-stu-id="b4800-126">Specifies the name of the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="b4800-127">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="b4800-127">-PrivateIpAddress</span></span>
<span data-ttu-id="b4800-128">Określa prywatny adres IP modułu równoważenia obciążenia, który jest skojarzony z konfiguracją frontonu IP do ustawienia.</span><span class="sxs-lookup"><span data-stu-id="b4800-128">Specifies the private IP address of the load balancer that is associated with the front-end IP configuration to set.</span></span>
<span data-ttu-id="b4800-129">Ten parametr należy określić tylko wtedy, gdy jest określany również parametr *Subnet* .</span><span class="sxs-lookup"><span data-stu-id="b4800-129">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="b4800-130">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="b4800-130">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="b4800-131">Prywatny adres IP konfiguracji protokołu IP.</span><span class="sxs-lookup"><span data-stu-id="b4800-131">The private IP address version of the IP configuration.</span></span>

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

### <span data-ttu-id="b4800-132">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b4800-132">-PublicIpAddress</span></span>
<span data-ttu-id="b4800-133">Określa obiekt **PublicIpAddress** , który jest skojarzony z konfiguracją frontonu IP do ustawienia.</span><span class="sxs-lookup"><span data-stu-id="b4800-133">Specifies the **PublicIpAddress** object that is associated with the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="b4800-134">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="b4800-134">-PublicIpAddressId</span></span>
<span data-ttu-id="b4800-135">Określa identyfikator obiektu **PublicIpAddress** skojarzonego z konfiguracją adresu IP frontonu, którą ustawia to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4800-135">Specifies the ID of the **PublicIpAddress** object that is associated with the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="b4800-136">-PublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b4800-136">-PublicIpAddressPrefix</span></span>
<span data-ttu-id="b4800-137">Określa obiekt **PublicIpAddressPrefix** , który ma zostać skojarzony z konfiguracją adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="b4800-137">Specifies the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: SetByResourcePublicIpAddressPrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4800-138">-PublicIpAddressPrefixId</span><span class="sxs-lookup"><span data-stu-id="b4800-138">-PublicIpAddressPrefixId</span></span>
<span data-ttu-id="b4800-139">Określa identyfikator obiektu **PublicIpAddressPrefix** , który ma zostać skojarzony z konfiguracją adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="b4800-139">Specifies the ID of the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddressPrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4800-140">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="b4800-140">-Subnet</span></span>
<span data-ttu-id="b4800-141">Określa obiekt **podsieci** , który zawiera konfigurację adresu IP frontonu ustawianą przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4800-141">Specifies the **Subnet** object that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="b4800-142">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="b4800-142">-SubnetId</span></span>
<span data-ttu-id="b4800-143">Określa identyfikator podsieci, w której znajduje się konfiguracja frontonu IP, która jest ustawiana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4800-143">Specifies the ID of the subnet that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="b4800-144">-Zone</span><span class="sxs-lookup"><span data-stu-id="b4800-144">-Zone</span></span>
<span data-ttu-id="b4800-145">Lista stref dostępności oznaczająca adres IP przydzielony dla zasobu musi pochodzić od.</span><span class="sxs-lookup"><span data-stu-id="b4800-145">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="b4800-146">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b4800-146">-Confirm</span></span>
<span data-ttu-id="b4800-147">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4800-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4800-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4800-148">-WhatIf</span></span>
<span data-ttu-id="b4800-149">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4800-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b4800-150">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b4800-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4800-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4800-151">CommonParameters</span></span>
<span data-ttu-id="b4800-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4800-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4800-153">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4800-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4800-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4800-154">INPUTS</span></span>

### <span data-ttu-id="b4800-155">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b4800-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="b4800-156">System. String</span><span class="sxs-lookup"><span data-stu-id="b4800-156">System.String</span></span>

### <span data-ttu-id="b4800-157">System. String []</span><span class="sxs-lookup"><span data-stu-id="b4800-157">System.String[]</span></span>

### <span data-ttu-id="b4800-158">Microsoft. Azure. Commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="b4800-158">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="b4800-159">Microsoft. Azure. Commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b4800-159">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="b4800-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b4800-160">OUTPUTS</span></span>

### <span data-ttu-id="b4800-161">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b4800-161">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b4800-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b4800-162">NOTES</span></span>

## <span data-ttu-id="b4800-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b4800-163">RELATED LINKS</span></span>

[<span data-ttu-id="b4800-164">Dodaj-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b4800-164">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="b4800-165">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b4800-165">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="b4800-166">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b4800-166">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="b4800-167">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b4800-167">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="b4800-168">Nowe — AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b4800-168">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="b4800-169">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b4800-169">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)


