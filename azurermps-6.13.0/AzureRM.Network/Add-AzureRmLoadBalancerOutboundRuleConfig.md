---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: ac96a07fb7ec32589ac351fc592c4c2848e75978
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527877"
---
# <span data-ttu-id="e3130-101">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e3130-101">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="e3130-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e3130-102">SYNOPSIS</span></span>
<span data-ttu-id="e3130-103">Umożliwia dodanie konfiguracji reguły wychodzącej do modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="e3130-103">Adds an outbound rule configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3130-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e3130-104">SYNTAX</span></span>

### <span data-ttu-id="e3130-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e3130-105">SetByResource (Default)</span></span>
```
Add-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSResourceId]>
 -BackendAddressPool <PSBackendAddressPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e3130-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e3130-106">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSResourceId]>
 -BackendAddressPoolId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e3130-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e3130-107">DESCRIPTION</span></span>
<span data-ttu-id="e3130-108">Polecenie cmdlet **Add-AzureRmLoadBalancerOutboundRuleConfig** umożliwia dodanie konfiguracji reguły wychodzącej do modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e3130-108">The **Add-AzureRmLoadBalancerOutboundRuleConfig** cmdlet adds an outbound rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="e3130-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e3130-109">EXAMPLES</span></span>

### <span data-ttu-id="e3130-110">Przykład 1: Dodawanie konfiguracji reguły ruchu wychodzącego do modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="e3130-110">Example 1: Add an outbound rule configuration to a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzureRmLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzureRmLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0]
```

<span data-ttu-id="e3130-111">Pierwsze polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyLoadBalancer, a następnie zapisuje ją w zmiennej $slb.</span><span class="sxs-lookup"><span data-stu-id="e3130-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="e3130-112">Drugie polecenie używa operatora potoku w celu przekazania modułu równoważenia obciążenia w $slb do polecenia **Add-AzureRmLoadBalancerOutboundRuleConfig** , które powoduje dodanie konfiguracji reguły ruchu wychodzącego do modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="e3130-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzureRmLoadBalancerOutboundRuleConfig** , which adds an outbound rule configuration to the load balancer.</span></span>

## <span data-ttu-id="e3130-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e3130-113">PARAMETERS</span></span>

### <span data-ttu-id="e3130-114">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="e3130-114">-AllocatedOutboundPort</span></span>
<span data-ttu-id="e3130-115">Liczba portów wychodzących, które mają być używane do obsługi translatora adresów sieciowych.</span><span class="sxs-lookup"><span data-stu-id="e3130-115">The number of outbound ports to be used for NAT.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3130-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e3130-116">-BackendAddressPool</span></span>
<span data-ttu-id="e3130-117">Odwołanie do puli DIP.</span><span class="sxs-lookup"><span data-stu-id="e3130-117">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="e3130-118">Ruch wychodzący jest zbilansowany losowo w ramach adresów IP w wewnętrznych adresach IP.</span><span class="sxs-lookup"><span data-stu-id="e3130-118">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3130-119">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="e3130-119">-BackendAddressPoolId</span></span>
<span data-ttu-id="e3130-120">Odwołanie do puli DIP.</span><span class="sxs-lookup"><span data-stu-id="e3130-120">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="e3130-121">Ruch wychodzący jest zbilansowany losowo w ramach adresów IP w wewnętrznych adresach IP.</span><span class="sxs-lookup"><span data-stu-id="e3130-121">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3130-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3130-122">-DefaultProfile</span></span>
<span data-ttu-id="e3130-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e3130-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3130-124">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="e3130-124">-EnableTcpReset</span></span>
<span data-ttu-id="e3130-125">Odbieraj dwukierunkowe Resetowanie protokołu TCP na limicie czasu bezczynności przepływu TCP lub nieoczekiwane zakończenie połączenia.</span><span class="sxs-lookup"><span data-stu-id="e3130-125">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="e3130-126">Ten element jest wykorzystywany tylko wtedy, gdy protokół jest ustawiony na protokół TCP.</span><span class="sxs-lookup"><span data-stu-id="e3130-126">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="e3130-127">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="e3130-127">-FrontendIpConfiguration</span></span>
<span data-ttu-id="e3130-128">Adresy IP frontonu modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="e3130-128">The Frontend IP addresses of the load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSResourceId]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3130-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="e3130-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="e3130-130">Limit czasu bezczynności połączenia TCP</span><span class="sxs-lookup"><span data-stu-id="e3130-130">The timeout for the TCP idle connection</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3130-131">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="e3130-131">-LoadBalancer</span></span>
<span data-ttu-id="e3130-132">Odwołanie do zasobu modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="e3130-132">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="e3130-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e3130-133">-Name</span></span>
<span data-ttu-id="e3130-134">Nazwa reguły ruchu wychodzącego.</span><span class="sxs-lookup"><span data-stu-id="e3130-134">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="e3130-135">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="e3130-135">-Protocol</span></span>
<span data-ttu-id="e3130-136">Protocol-TCP, UDP lub All</span><span class="sxs-lookup"><span data-stu-id="e3130-136">Protocol - TCP, UDP or All</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3130-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e3130-137">-Confirm</span></span>
<span data-ttu-id="e3130-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3130-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3130-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3130-139">-WhatIf</span></span>
<span data-ttu-id="e3130-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3130-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3130-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e3130-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3130-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3130-142">CommonParameters</span></span>
<span data-ttu-id="e3130-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3130-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3130-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3130-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3130-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e3130-145">INPUTS</span></span>

### <span data-ttu-id="e3130-146">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e3130-146">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="e3130-147">System. Int32 system. String. String system. Collections. Generic. list \` 1 [[Microsoft. Azure. Commands. models. PSResourceId; Microsoft. Azure. Commands......</span><span class="sxs-lookup"><span data-stu-id="e3130-147">System.Int32 System.String System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSResourceId, Microsoft.Azure.Commands.Network, Version=6.5.0.0, Culture=neutral, PublicKeyToken=null]] Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="e3130-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e3130-148">OUTPUTS</span></span>

### <span data-ttu-id="e3130-149">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e3130-149">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e3130-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e3130-150">NOTES</span></span>

## <span data-ttu-id="e3130-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e3130-151">RELATED LINKS</span></span>
