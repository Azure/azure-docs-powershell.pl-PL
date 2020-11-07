---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C23BEF37-D472-43EC-90AA-F8742247ABA2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 93313b6a2d9623ed518d6e79fabcda8fea5cc7b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717064"
---
# <span data-ttu-id="f7f8d-101">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f7f8d-101">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="f7f8d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f7f8d-102">SYNOPSIS</span></span>
<span data-ttu-id="f7f8d-103">Ustawia stan celu dla konfiguracji frontonu IP w usłudze równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="f7f8d-103">Sets the goal state for a front-end IP configuration in a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7f8d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f7f8d-104">SYNTAX</span></span>

### <span data-ttu-id="f7f8d-105">SetByResourceSubnet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f7f8d-105">SetByResourceSubnet (Default)</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-PrivateIpAddress <String>] [-Zone <System.Collections.Generic.List`1[System.String]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7f8d-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="f7f8d-106">SetByResourceIdSubnet</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-PrivateIpAddress <String>] [-Zone <System.Collections.Generic.List`1[System.String]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7f8d-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f7f8d-107">SetByResourceIdPublicIpAddress</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] -PublicIpAddressId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7f8d-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f7f8d-108">SetByResourcePublicIpAddress</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] -PublicIpAddress <PSPublicIpAddress>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7f8d-109">Opis</span><span class="sxs-lookup"><span data-stu-id="f7f8d-109">DESCRIPTION</span></span>
<span data-ttu-id="f7f8d-110">Polecenie cmdlet **Set-AzureRmLoadBalancerFrontendIpConfig** ustawia stan celu dla konfiguracji frontonu IP w usłudze równoważenia obciążenia Azure.</span><span class="sxs-lookup"><span data-stu-id="f7f8d-110">The **Set-AzureRmLoadBalancerFrontendIpConfig** cmdlet sets the goal state for a front-end IP configuration in an Azure load balancer.</span></span>

## <span data-ttu-id="f7f8d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f7f8d-111">EXAMPLES</span></span>

### <span data-ttu-id="f7f8d-112">Przykład 1: modyfikowanie konfiguracji adresu IP frontonu modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="f7f8d-112">Example 1: Modify the front-end IP configuration of a load balancer</span></span>
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyResourceGroup" | Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet"
PS C:\> $slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzureRmLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
```

<span data-ttu-id="f7f8d-113">Pierwsze polecenie uzyskuje podsieć wirtualną o nazwie Subnet, a następnie zapisuje ją w zmiennej $Subnet.</span><span class="sxs-lookup"><span data-stu-id="f7f8d-113">The first command gets the virtual subnet named Subnet, and then stores it in the $Subnet variable.</span></span>
<span data-ttu-id="f7f8d-114">Drugie polecenie uzyskuje skojarzony moduł równoważenia obciążenia o nazwie MyLoadBalancer, a następnie zapisuje go w zmiennej $slb.</span><span class="sxs-lookup"><span data-stu-id="f7f8d-114">The second command gets the associated load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="f7f8d-115">W trzecim poleceniu jest używany operator potoku umożliwiający przekazanie modułu równoważenia obciążenia w $slb do polecenia Add-AzureRmLoadBalancerFrontendIpConfig, które powoduje utworzenie zewnętrznej konfiguracji adresu IP o nazwie NewFrontend dla $slb.</span><span class="sxs-lookup"><span data-stu-id="f7f8d-115">The third command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerFrontendIpConfig, which creates a front-end IP configuration named NewFrontend for $slb.</span></span>
<span data-ttu-id="f7f8d-116">Czwarte polecenie przekazuje moduł równoważenia obciążenia w $slb do polecenia **Set-AzureRmLoadBalancerFrontendIpConfig** , które umożliwia zapisywanie i aktualizowanie konfiguracji frontonu IP.</span><span class="sxs-lookup"><span data-stu-id="f7f8d-116">The fourth command passes the load balancer in $slb to **Set-AzureRmLoadBalancerFrontendIpConfig** , which saves and updates the front-end IP configuration.</span></span>

## <span data-ttu-id="f7f8d-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f7f8d-117">PARAMETERS</span></span>

### <span data-ttu-id="f7f8d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7f8d-118">-DefaultProfile</span></span>
<span data-ttu-id="f7f8d-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f7f8d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7f8d-120">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="f7f8d-120">-LoadBalancer</span></span>
<span data-ttu-id="f7f8d-121">Umożliwia określenie modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="f7f8d-121">Specifies a load balancer.</span></span>
<span data-ttu-id="f7f8d-122">To polecenie cmdlet ustawia stan celu dla konfiguracji frontonu dla modułu równoważenia obciążenia, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="f7f8d-122">This cmdlet sets the goal state for a front-end configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="f7f8d-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f7f8d-123">-Name</span></span>
<span data-ttu-id="f7f8d-124">Określa nazwę konfiguracji adresu IP frontonu do ustawienia.</span><span class="sxs-lookup"><span data-stu-id="f7f8d-124">Specifies the name of the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="f7f8d-125">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="f7f8d-125">-PrivateIpAddress</span></span>
<span data-ttu-id="f7f8d-126">Określa prywatny adres IP modułu równoważenia obciążenia, który jest skojarzony z konfiguracją frontonu IP do ustawienia.</span><span class="sxs-lookup"><span data-stu-id="f7f8d-126">Specifies the private IP address of the load balancer that is associated with the front-end IP configuration to set.</span></span>
<span data-ttu-id="f7f8d-127">Ten parametr należy określić tylko wtedy, gdy jest określany również parametr *Subnet* .</span><span class="sxs-lookup"><span data-stu-id="f7f8d-127">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="f7f8d-128">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f7f8d-128">-PublicIpAddress</span></span>
<span data-ttu-id="f7f8d-129">Określa obiekt **PublicIpAddress** , który jest skojarzony z konfiguracją frontonu IP do ustawienia.</span><span class="sxs-lookup"><span data-stu-id="f7f8d-129">Specifies the **PublicIpAddress** object that is associated with the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="f7f8d-130">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="f7f8d-130">-PublicIpAddressId</span></span>
<span data-ttu-id="f7f8d-131">Określa identyfikator obiektu **PublicIpAddress** skojarzonego z konfiguracją adresu IP frontonu, którą ustawia to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7f8d-131">Specifies the ID of the **PublicIpAddress** object that is associated with the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="f7f8d-132">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="f7f8d-132">-Subnet</span></span>
<span data-ttu-id="f7f8d-133">Określa obiekt **podsieci** , który zawiera konfigurację adresu IP frontonu ustawianą przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7f8d-133">Specifies the **Subnet** object that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="f7f8d-134">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="f7f8d-134">-SubnetId</span></span>
<span data-ttu-id="f7f8d-135">Określa identyfikator podsieci, w której znajduje się konfiguracja frontonu IP, która jest ustawiana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7f8d-135">Specifies the ID of the subnet that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="f7f8d-136">-Zone</span><span class="sxs-lookup"><span data-stu-id="f7f8d-136">-Zone</span></span>
<span data-ttu-id="f7f8d-137">Lista stref dostępności oznaczająca adres IP przydzielony dla zasobu musi pochodzić od.</span><span class="sxs-lookup"><span data-stu-id="f7f8d-137">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7f8d-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f7f8d-138">-Confirm</span></span>
<span data-ttu-id="f7f8d-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7f8d-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7f8d-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7f8d-140">-WhatIf</span></span>
<span data-ttu-id="f7f8d-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7f8d-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f7f8d-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f7f8d-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7f8d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7f8d-143">CommonParameters</span></span>
<span data-ttu-id="f7f8d-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7f8d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7f8d-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7f8d-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7f8d-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f7f8d-146">INPUTS</span></span>

### <span data-ttu-id="f7f8d-147">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f7f8d-147">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="f7f8d-148">Parametry: moduł równoważenia obciążenia (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f7f8d-148">Parameters: LoadBalancer (ByValue)</span></span>

### <span data-ttu-id="f7f8d-149">System. Collections. Generic. list \` 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f7f8d-149">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="f7f8d-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f7f8d-150">OUTPUTS</span></span>

### <span data-ttu-id="f7f8d-151">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f7f8d-151">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f7f8d-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f7f8d-152">NOTES</span></span>

## <span data-ttu-id="f7f8d-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f7f8d-153">RELATED LINKS</span></span>

[<span data-ttu-id="f7f8d-154">Dodaj-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f7f8d-154">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="f7f8d-155">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f7f8d-155">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="f7f8d-156">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f7f8d-156">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="f7f8d-157">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f7f8d-157">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="f7f8d-158">Nowe — AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f7f8d-158">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="f7f8d-159">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f7f8d-159">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)


