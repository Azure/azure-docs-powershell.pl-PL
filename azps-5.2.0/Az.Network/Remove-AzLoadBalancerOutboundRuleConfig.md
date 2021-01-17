---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 824675d331d37c93e6bcf3bb3d5da0fa8cbde78b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333001"
---
# <span data-ttu-id="503af-101">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="503af-101">Remove-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="503af-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="503af-102">SYNOPSIS</span></span>
<span data-ttu-id="503af-103">Usuwa konfigurację reguły ruchu wychodzącego z modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="503af-103">Removes an outbound rule configuration from a load balancer.</span></span>

## <span data-ttu-id="503af-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="503af-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="503af-105">Opis</span><span class="sxs-lookup"><span data-stu-id="503af-105">DESCRIPTION</span></span>
<span data-ttu-id="503af-106">Polecenie cmdlet **Remove-AzLoadBalancerOutboundRuleConfig** usuwa konfigurację reguły wychodzącą z modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="503af-106">The **Remove-AzLoadBalancerOutboundRuleConfig** cmdlet removes an outbound rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="503af-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="503af-107">EXAMPLES</span></span>

### <span data-ttu-id="503af-108">Przykład 1: Usuwanie reguły wychodzącej z modułu równoważenia obciążenia platformy Azure</span><span class="sxs-lookup"><span data-stu-id="503af-108">Example 1: Delete an outbound rule from an Azure load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Remove-AzLoadBalancerOutboundRuleConfig -Name "RuleName" -LoadBalancer $slb
PS C:\>Set-AzLoadBalancer -LoadBalancer $slb
```

<span data-ttu-id="503af-109">Pierwsze polecenie uzyskuje moduł równoważenia obciążenia skojarzony z konfiguracją reguły ruchu wychodzącego, którą chcesz usunąć, a następnie zapisze ją w zmiennej $slb.</span><span class="sxs-lookup"><span data-stu-id="503af-109">The first command gets the load balancer that is associated with the outbound rule configuration you want to remove, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="503af-110">Drugie polecenie usuwa konfigurację skojarzonej reguły wychodzącej z modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="503af-110">The second command removes the associated outbound rule configuration from the load balancer.</span></span>
<span data-ttu-id="503af-111">W trzecim poleceniu jest aktualizowana usługa równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="503af-111">The third command updates the load balancer.</span></span>

## <span data-ttu-id="503af-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="503af-112">PARAMETERS</span></span>

### <span data-ttu-id="503af-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="503af-113">-DefaultProfile</span></span>
<span data-ttu-id="503af-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="503af-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="503af-115">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="503af-115">-LoadBalancer</span></span>
<span data-ttu-id="503af-116">Odwołanie do zasobu modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="503af-116">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="503af-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="503af-117">-Name</span></span>
<span data-ttu-id="503af-118">Nazwa reguły ruchu wychodzącego</span><span class="sxs-lookup"><span data-stu-id="503af-118">The Name of outbound rule</span></span>

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

### <span data-ttu-id="503af-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="503af-119">-Confirm</span></span>
<span data-ttu-id="503af-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="503af-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="503af-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="503af-121">-WhatIf</span></span>
<span data-ttu-id="503af-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="503af-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="503af-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="503af-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="503af-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="503af-124">CommonParameters</span></span>
<span data-ttu-id="503af-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="503af-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="503af-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="503af-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="503af-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="503af-127">INPUTS</span></span>

### <span data-ttu-id="503af-128">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="503af-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="503af-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="503af-129">OUTPUTS</span></span>

### <span data-ttu-id="503af-130">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="503af-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="503af-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="503af-131">NOTES</span></span>

## <span data-ttu-id="503af-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="503af-132">RELATED LINKS</span></span>

[<span data-ttu-id="503af-133">Dodaj-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="503af-133">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="503af-134">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="503af-134">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="503af-135">Nowe — AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="503af-135">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="503af-136">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="503af-136">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
