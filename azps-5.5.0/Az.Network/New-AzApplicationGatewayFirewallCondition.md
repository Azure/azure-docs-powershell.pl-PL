---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
ms.openlocfilehash: 64157cd137e9f3b784404dccee6513b6fe023d0f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179795"
---
# <span data-ttu-id="1a83e-101">New-AzApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="1a83e-101">New-AzApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="1a83e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a83e-102">SYNOPSIS</span></span>
<span data-ttu-id="1a83e-103">Tworzy warunek dopasowania dla reguły niestandardowej</span><span class="sxs-lookup"><span data-stu-id="1a83e-103">Creates a match condition for custom rule</span></span>

## <span data-ttu-id="1a83e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1a83e-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCondition -MatchVariable <PSApplicationGatewayFirewallMatchVariable[]>
 -Operator <String> [-NegationCondition <Boolean>] -MatchValue <String[]> [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a83e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="1a83e-105">DESCRIPTION</span></span>
<span data-ttu-id="1a83e-106">Reguła **New-AzApplicationGatewayFirewallCondition** tworzy warunek dopasowania dla reguły niestandardowej zapory.</span><span class="sxs-lookup"><span data-stu-id="1a83e-106">The **New-AzApplicationGatewayFirewallCondition** creates a match condition for firewall custom rule.</span></span>

## <span data-ttu-id="1a83e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1a83e-107">EXAMPLES</span></span>

### <span data-ttu-id="1a83e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1a83e-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallCondition -MatchVariable $variable -Operator Contains -NegationCondition false -Transforms Lowercase, Trim -MatchValue abc, cde
```

<span data-ttu-id="1a83e-109">Polecenie tworzy nowy warunek dopasowania przy użyciu zmiennej dopasowania zdefiniowanej w $variable, operator zawiera, a warunek negacji ma wartość fałszywą, transfroms, w tym małe litery i przycinanie, wartość dopasowania to abc i cde.</span><span class="sxs-lookup"><span data-stu-id="1a83e-109">The command creates a new match condition using the match variable defined in the $variable, the operator is Contains and negation condition is false, Transfroms including lowercase and trim, the match value is abc and cde.</span></span> <span data-ttu-id="1a83e-110">Nowy warunek dopasowania zostanie zapisany w $condition.</span><span class="sxs-lookup"><span data-stu-id="1a83e-110">The new match condition is saved in $condition.</span></span>

## <span data-ttu-id="1a83e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a83e-111">PARAMETERS</span></span>

### <span data-ttu-id="1a83e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a83e-112">-DefaultProfile</span></span>
<span data-ttu-id="1a83e-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1a83e-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a83e-114">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="1a83e-114">-MatchValue</span></span>
<span data-ttu-id="1a83e-115">Dopasuj wartość.</span><span class="sxs-lookup"><span data-stu-id="1a83e-115">Match value.</span></span>

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

### <span data-ttu-id="1a83e-116">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="1a83e-116">-MatchVariable</span></span>
<span data-ttu-id="1a83e-117">Lista zmiennych dopasowania.</span><span class="sxs-lookup"><span data-stu-id="1a83e-117">List of match variables.</span></span>

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

### <span data-ttu-id="1a83e-118">-NegationCondition</span><span class="sxs-lookup"><span data-stu-id="1a83e-118">-NegationCondition</span></span>
<span data-ttu-id="1a83e-119">W tym artykule opisano, czy jest to warunek negatywowy, czy nie.</span><span class="sxs-lookup"><span data-stu-id="1a83e-119">Describes if this is negate condition or not.</span></span>

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

### <span data-ttu-id="1a83e-120">-Operator</span><span class="sxs-lookup"><span data-stu-id="1a83e-120">-Operator</span></span>
<span data-ttu-id="1a83e-121">Opis operatora do dopasowania.</span><span class="sxs-lookup"><span data-stu-id="1a83e-121">Describes operator to be matched.</span></span>

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

### <span data-ttu-id="1a83e-122">— Przekształcanie</span><span class="sxs-lookup"><span data-stu-id="1a83e-122">-Transform</span></span>
<span data-ttu-id="1a83e-123">Lista przekształceń.</span><span class="sxs-lookup"><span data-stu-id="1a83e-123">List of transforms.</span></span>

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

### <span data-ttu-id="1a83e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a83e-124">CommonParameters</span></span>
<span data-ttu-id="1a83e-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a83e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a83e-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a83e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a83e-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1a83e-127">INPUTS</span></span>

### <span data-ttu-id="1a83e-128">Brak</span><span class="sxs-lookup"><span data-stu-id="1a83e-128">None</span></span>

## <span data-ttu-id="1a83e-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1a83e-129">OUTPUTS</span></span>

### <span data-ttu-id="1a83e-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="1a83e-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="1a83e-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1a83e-131">NOTES</span></span>

## <span data-ttu-id="1a83e-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1a83e-132">RELATED LINKS</span></span>
