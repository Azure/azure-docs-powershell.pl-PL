---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
ms.openlocfilehash: 096fb182ae330750eeb23e365bc929edb17b21f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007745"
---
# <span data-ttu-id="b9f09-101">New-AzApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="b9f09-101">New-AzApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="b9f09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9f09-102">SYNOPSIS</span></span>
<span data-ttu-id="b9f09-103">Tworzy warunek dopasowania dla reguły niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="b9f09-103">Creates a match condition for custom rule</span></span>

## <span data-ttu-id="b9f09-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b9f09-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCondition -MatchVariable <PSApplicationGatewayFirewallMatchVariable[]>
 -Operator <String> [-NegationCondition <Boolean>] -MatchValue <String[]> [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9f09-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b9f09-105">DESCRIPTION</span></span>
<span data-ttu-id="b9f09-106">Reguła **New-AzApplicationGatewayFirewallCondition** tworzy warunek dopasowania dla reguły niestandardowej zapory.</span><span class="sxs-lookup"><span data-stu-id="b9f09-106">The **New-AzApplicationGatewayFirewallCondition** creates a match condition for firewall custom rule.</span></span>

## <span data-ttu-id="b9f09-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b9f09-107">EXAMPLES</span></span>

### <span data-ttu-id="b9f09-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b9f09-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallCondition -MatchVariable $variable -Operator Contains -NegationCondition false -Transforms Lowercase, Trim -MatchValue abc, cde
```

<span data-ttu-id="b9f09-109">Polecenie tworzy nowy warunek dopasowania przy użyciu zmiennej zgodnej zdefiniowanej w $variable, operator zawiera, a warunek negacji ma wartość fałszywą, transfroms, w tym małe litery i przycinanie, wartość dopasowania to abc i cde.</span><span class="sxs-lookup"><span data-stu-id="b9f09-109">The command creates a new match condition using the match variable defined in the $variable, the operator is Contains and negation condition is false, Transfroms including lowercase and trim, the match value is abc and cde.</span></span> <span data-ttu-id="b9f09-110">Nowy warunek dopasowania zostanie zapisany w $condition.</span><span class="sxs-lookup"><span data-stu-id="b9f09-110">The new match condition is saved in $condition.</span></span>

## <span data-ttu-id="b9f09-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9f09-111">PARAMETERS</span></span>

### <span data-ttu-id="b9f09-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9f09-112">-DefaultProfile</span></span>
<span data-ttu-id="b9f09-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b9f09-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9f09-114">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="b9f09-114">-MatchValue</span></span>
<span data-ttu-id="b9f09-115">Dopasuj wartość.</span><span class="sxs-lookup"><span data-stu-id="b9f09-115">Match value.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9f09-116">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="b9f09-116">-MatchVariable</span></span>
<span data-ttu-id="b9f09-117">Lista zmiennych dopasowania.</span><span class="sxs-lookup"><span data-stu-id="b9f09-117">List of match variables.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9f09-118">-NegationCondition</span><span class="sxs-lookup"><span data-stu-id="b9f09-118">-NegationCondition</span></span>
<span data-ttu-id="b9f09-119">W tym artykule opisano, czy jest to warunek negatywowy, czy nie.</span><span class="sxs-lookup"><span data-stu-id="b9f09-119">Describes if this is negate condition or not.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9f09-120">-Operator</span><span class="sxs-lookup"><span data-stu-id="b9f09-120">-Operator</span></span>
<span data-ttu-id="b9f09-121">Opis operatora do dopasowania.</span><span class="sxs-lookup"><span data-stu-id="b9f09-121">Describes operator to be matched.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith, Regex

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9f09-122">— Przekształcanie</span><span class="sxs-lookup"><span data-stu-id="b9f09-122">-Transform</span></span>
<span data-ttu-id="b9f09-123">Lista przekształceń.</span><span class="sxs-lookup"><span data-stu-id="b9f09-123">List of transforms.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Lowercase, Trim, UrlDecode, UrlEncode, RemoveNulls, HtmlEntityDecode

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9f09-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9f09-124">CommonParameters</span></span>
<span data-ttu-id="b9f09-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9f09-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9f09-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9f09-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9f09-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b9f09-127">INPUTS</span></span>

### <span data-ttu-id="b9f09-128">Brak</span><span class="sxs-lookup"><span data-stu-id="b9f09-128">None</span></span>

## <span data-ttu-id="b9f09-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b9f09-129">OUTPUTS</span></span>

### <span data-ttu-id="b9f09-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="b9f09-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="b9f09-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b9f09-131">NOTES</span></span>

## <span data-ttu-id="b9f09-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b9f09-132">RELATED LINKS</span></span>
