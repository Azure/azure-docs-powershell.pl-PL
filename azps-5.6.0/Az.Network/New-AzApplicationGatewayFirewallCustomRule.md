---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallcustomrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCustomRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCustomRule.md
ms.openlocfilehash: f3cd7edf0def90f4245e20c540332d08e045865f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955809"
---
# <span data-ttu-id="e0482-101">New-AzApplicationGatewayFirewallCustomRule</span><span class="sxs-lookup"><span data-stu-id="e0482-101">New-AzApplicationGatewayFirewallCustomRule</span></span>

## <span data-ttu-id="e0482-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0482-102">SYNOPSIS</span></span>
<span data-ttu-id="e0482-103">Tworzy nową regułę niestandardową dla zasad zapory bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e0482-103">Creates a new custom rule for the application gateway firewall policy.</span></span>

## <span data-ttu-id="e0482-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e0482-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCustomRule -Name <String> -Priority <Int32> -RuleType <String>
 -MatchCondition <PSApplicationGatewayFirewallCondition[]> -Action <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0482-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e0482-105">DESCRIPTION</span></span>
<span data-ttu-id="e0482-106">Reguła **New-AzApplicationGatewayFirewallCustomRule** tworzy regułę niestandardową dla zasad zapory.</span><span class="sxs-lookup"><span data-stu-id="e0482-106">The **New-AzApplicationGatewayFirewallCustomRule** creates a custom rule for firewall policy.</span></span>

## <span data-ttu-id="e0482-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e0482-107">EXAMPLES</span></span>

### <span data-ttu-id="e0482-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e0482-108">Example 1</span></span>
```powershell
PS C:\> $customRule = New-AzApplicationGatewayFirewallCustomRule -Name example-rule -Priority 1 -RuleType MatchRule -MatchCondition $condtion -Action Allow
```

<span data-ttu-id="e0482-109">Polecenie tworzy nową regułę niestandardową z nazwą reguły przykładowej o priorytecie 1, a typem reguły będzie reguła MatchRule z warunkiem zdefiniowanym w zmiennej warunku, a akcja będzie zezwalać.</span><span class="sxs-lookup"><span data-stu-id="e0482-109">The command creates a new custom rule with name of example-rule, priority 1 and the rule type will be MatchRule with condition defined in the condition variable, the action will the allow.</span></span> <span data-ttu-id="e0482-110">Nowa reguła niestandardowa dopasowania zostanie zapisana w $customRule.</span><span class="sxs-lookup"><span data-stu-id="e0482-110">The new match custom rule is saved in $customRule.</span></span>

## <span data-ttu-id="e0482-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0482-111">PARAMETERS</span></span>

### <span data-ttu-id="e0482-112">— Akcja</span><span class="sxs-lookup"><span data-stu-id="e0482-112">-Action</span></span>
<span data-ttu-id="e0482-113">Typ akcji.</span><span class="sxs-lookup"><span data-stu-id="e0482-113">Type of Actions.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Block, Log

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0482-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0482-114">-DefaultProfile</span></span>
<span data-ttu-id="e0482-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e0482-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0482-116">- MatchCondition</span><span class="sxs-lookup"><span data-stu-id="e0482-116">-MatchCondition</span></span>
<span data-ttu-id="e0482-117">Lista warunków dopasowania.</span><span class="sxs-lookup"><span data-stu-id="e0482-117">List of match conditions.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0482-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e0482-118">-Name</span></span>
<span data-ttu-id="e0482-119">Nazwa reguły.</span><span class="sxs-lookup"><span data-stu-id="e0482-119">The Name of the Rule.</span></span>

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

### <span data-ttu-id="e0482-120">— Priority (Priorytet)</span><span class="sxs-lookup"><span data-stu-id="e0482-120">-Priority</span></span>
<span data-ttu-id="e0482-121">W tym artykule opisano priorytet reguły.</span><span class="sxs-lookup"><span data-stu-id="e0482-121">Describes priority of the rule.</span></span>
<span data-ttu-id="e0482-122">Reguły o niższej wartości będą obliczane przed regułami o większej wartości.</span><span class="sxs-lookup"><span data-stu-id="e0482-122">Rules with a lower value will be evaluated before rules with a higher value.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0482-123">-RuleType</span><span class="sxs-lookup"><span data-stu-id="e0482-123">-RuleType</span></span>
<span data-ttu-id="e0482-124">W tym artykule opisano typ reguły.</span><span class="sxs-lookup"><span data-stu-id="e0482-124">Describes type of rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MatchRule

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0482-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0482-125">CommonParameters</span></span>
<span data-ttu-id="e0482-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0482-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0482-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0482-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0482-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0482-128">INPUTS</span></span>

### <span data-ttu-id="e0482-129">Brak</span><span class="sxs-lookup"><span data-stu-id="e0482-129">None</span></span>

## <span data-ttu-id="e0482-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0482-130">OUTPUTS</span></span>

### <span data-ttu-id="e0482-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule</span><span class="sxs-lookup"><span data-stu-id="e0482-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule</span></span>

## <span data-ttu-id="e0482-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e0482-132">NOTES</span></span>

## <span data-ttu-id="e0482-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e0482-133">RELATED LINKS</span></span>
