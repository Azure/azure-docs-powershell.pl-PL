---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallcustomrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCustomRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCustomRule.md
ms.openlocfilehash: 1f8e165d8353c046749bd2ea0eb749a75fb2d6c7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870548"
---
# <span data-ttu-id="60fcc-101">New-AzApplicationGatewayFirewallCustomRule</span><span class="sxs-lookup"><span data-stu-id="60fcc-101">New-AzApplicationGatewayFirewallCustomRule</span></span>

## <span data-ttu-id="60fcc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="60fcc-102">SYNOPSIS</span></span>
<span data-ttu-id="60fcc-103">Tworzy nową regułę niestandardową dla zasad zapory Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="60fcc-103">Creates a new custom rule for the application gateway firewall policy.</span></span>

## <span data-ttu-id="60fcc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="60fcc-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCustomRule -Name <String> -Priority <Int32> -RuleType <String>
 -MatchCondition <PSApplicationGatewayFirewallCondition[]> -Action <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60fcc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="60fcc-105">DESCRIPTION</span></span>
<span data-ttu-id="60fcc-106">**Nowy-AzApplicationGatewayFirewallCustomRule** tworzy regułę niestandardową dla zasad zapory.</span><span class="sxs-lookup"><span data-stu-id="60fcc-106">The **New-AzApplicationGatewayFirewallCustomRule** creates a custom rule for firewall policy.</span></span>

## <span data-ttu-id="60fcc-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="60fcc-107">EXAMPLES</span></span>

### <span data-ttu-id="60fcc-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="60fcc-108">Example 1</span></span>
```powershell
PS C:\> $customRule = New-AzApplicationGatewayFirewallCustomRule -Name example-rule -Priority 1 -RuleType MatchRule -matchConditons $condtion -Action Allow
```

<span data-ttu-id="60fcc-109">Polecenie tworzy nową regułę niestandardową z nazwą przykładu — regułą, priorytetem 1, a typ reguły będzie MatchRule z warunkiem zdefiniowanym w zmiennej Condition, akcja będzie dozwolona.</span><span class="sxs-lookup"><span data-stu-id="60fcc-109">The command creates a new custom rule with name of example-rule, priority 1 and the rule type will be MatchRule with condition defined in the condition variable, the action will the allow.</span></span> <span data-ttu-id="60fcc-110">Nowa reguła dopasowania jest zapisywana w $customRule.</span><span class="sxs-lookup"><span data-stu-id="60fcc-110">The new match custom rule is saved in $customRule.</span></span>

## <span data-ttu-id="60fcc-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="60fcc-111">PARAMETERS</span></span>

### <span data-ttu-id="60fcc-112">-Action</span><span class="sxs-lookup"><span data-stu-id="60fcc-112">-Action</span></span>
<span data-ttu-id="60fcc-113">Typ akcji.</span><span class="sxs-lookup"><span data-stu-id="60fcc-113">Type of Actions.</span></span>

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

### <span data-ttu-id="60fcc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60fcc-114">-DefaultProfile</span></span>
<span data-ttu-id="60fcc-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="60fcc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60fcc-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="60fcc-116">-MatchCondition</span></span>
<span data-ttu-id="60fcc-117">Lista warunków zgodności.</span><span class="sxs-lookup"><span data-stu-id="60fcc-117">List of match conditions.</span></span>

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

### <span data-ttu-id="60fcc-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="60fcc-118">-Name</span></span>
<span data-ttu-id="60fcc-119">Nazwa reguły.</span><span class="sxs-lookup"><span data-stu-id="60fcc-119">The Name of the Rule.</span></span>

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

### <span data-ttu-id="60fcc-120">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="60fcc-120">-Priority</span></span>
<span data-ttu-id="60fcc-121">Opisuje priorytet reguły.</span><span class="sxs-lookup"><span data-stu-id="60fcc-121">Describes priority of the rule.</span></span>
<span data-ttu-id="60fcc-122">Reguły o niższej wartości zostaną ocenione przed regułami o wyższej wartości.</span><span class="sxs-lookup"><span data-stu-id="60fcc-122">Rules with a lower value will be evaluated before rules with a higher value.</span></span>

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

### <span data-ttu-id="60fcc-123">-Ruletype</span><span class="sxs-lookup"><span data-stu-id="60fcc-123">-RuleType</span></span>
<span data-ttu-id="60fcc-124">Opisuje typ reguły.</span><span class="sxs-lookup"><span data-stu-id="60fcc-124">Describes type of rule.</span></span>

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

### <span data-ttu-id="60fcc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60fcc-125">CommonParameters</span></span>
<span data-ttu-id="60fcc-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60fcc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60fcc-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60fcc-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60fcc-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="60fcc-128">INPUTS</span></span>

### <span data-ttu-id="60fcc-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="60fcc-129">None</span></span>

## <span data-ttu-id="60fcc-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="60fcc-130">OUTPUTS</span></span>

### <span data-ttu-id="60fcc-131">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayFirewallCustomRule</span><span class="sxs-lookup"><span data-stu-id="60fcc-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule</span></span>

## <span data-ttu-id="60fcc-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="60fcc-132">NOTES</span></span>

## <span data-ttu-id="60fcc-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="60fcc-133">RELATED LINKS</span></span>
