---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 5652615cf8072e4a448f2fe6c6d4b3fd784cc330
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996276"
---
# <span data-ttu-id="eea58-101">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="eea58-101">Remove-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="eea58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eea58-102">SYNOPSIS</span></span>
<span data-ttu-id="eea58-103">Usuwa konfigurację reguł ruchu wychodzącego z urządzenia do równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="eea58-103">Removes an outbound rule configuration from a load balancer.</span></span>

## <span data-ttu-id="eea58-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="eea58-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eea58-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="eea58-105">DESCRIPTION</span></span>
<span data-ttu-id="eea58-106">Polecenie **cmdlet Remove-AzLoadBalancerOutboundRuleConfig** usuwa konfigurację reguł ruchu wychodzącego z narzędzia do równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="eea58-106">The **Remove-AzLoadBalancerOutboundRuleConfig** cmdlet removes an outbound rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="eea58-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="eea58-107">EXAMPLES</span></span>

### <span data-ttu-id="eea58-108">Przykład 1. Usuwanie reguły ruchu wychodzącego z narzędzia do równoważenia obciążenia platformy Azure</span><span class="sxs-lookup"><span data-stu-id="eea58-108">Example 1: Delete an outbound rule from an Azure load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Remove-AzLoadBalancerOutboundRuleConfig -Name "RuleName" -LoadBalancer $slb
PS C:\>Set-AzLoadBalancer -LoadBalancer $slb
```

<span data-ttu-id="eea58-109">Pierwsze polecenie pobiera równoważenie obciążenia skojarzone z konfiguracją reguły ruchu wychodzącego, którą chcesz usunąć, a następnie przechowuje je w $slb sieci.</span><span class="sxs-lookup"><span data-stu-id="eea58-109">The first command gets the load balancer that is associated with the outbound rule configuration you want to remove, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="eea58-110">Drugie polecenie usuwa skojarzoną konfigurację reguły ruchu wychodzącego z równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="eea58-110">The second command removes the associated outbound rule configuration from the load balancer.</span></span>
<span data-ttu-id="eea58-111">Trzecie polecenie aktualizuje równoważenie obciążenia.</span><span class="sxs-lookup"><span data-stu-id="eea58-111">The third command updates the load balancer.</span></span>

## <span data-ttu-id="eea58-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eea58-112">PARAMETERS</span></span>

### <span data-ttu-id="eea58-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eea58-113">-DefaultProfile</span></span>
<span data-ttu-id="eea58-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="eea58-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eea58-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="eea58-115">-LoadBalancer</span></span>
<span data-ttu-id="eea58-116">Odwołanie do zasobu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="eea58-116">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="eea58-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="eea58-117">-Name</span></span>
<span data-ttu-id="eea58-118">Nazwa reguły ruchu wychodzącego</span><span class="sxs-lookup"><span data-stu-id="eea58-118">The Name of outbound rule</span></span>

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

### <span data-ttu-id="eea58-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="eea58-119">-Confirm</span></span>
<span data-ttu-id="eea58-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="eea58-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eea58-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eea58-121">-WhatIf</span></span>
<span data-ttu-id="eea58-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eea58-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eea58-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="eea58-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eea58-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eea58-124">CommonParameters</span></span>
<span data-ttu-id="eea58-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eea58-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eea58-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eea58-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eea58-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eea58-127">INPUTS</span></span>

### <span data-ttu-id="eea58-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="eea58-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="eea58-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eea58-129">OUTPUTS</span></span>

### <span data-ttu-id="eea58-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="eea58-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="eea58-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="eea58-131">NOTES</span></span>

## <span data-ttu-id="eea58-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eea58-132">RELATED LINKS</span></span>

[<span data-ttu-id="eea58-133">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="eea58-133">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="eea58-134">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="eea58-134">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="eea58-135">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="eea58-135">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="eea58-136">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="eea58-136">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
