---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
ms.openlocfilehash: 64157cd137e9f3b784404dccee6513b6fe023d0f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234422"
---
# <span data-ttu-id="735e8-101">New-AzApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="735e8-101">New-AzApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="735e8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="735e8-102">SYNOPSIS</span></span>
<span data-ttu-id="735e8-103">Tworzy warunek zgodności dla reguły niestandardowej</span><span class="sxs-lookup"><span data-stu-id="735e8-103">Creates a match condition for custom rule</span></span>

## <span data-ttu-id="735e8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="735e8-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCondition -MatchVariable <PSApplicationGatewayFirewallMatchVariable[]>
 -Operator <String> [-NegationCondition <Boolean>] -MatchValue <String[]> [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="735e8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="735e8-105">DESCRIPTION</span></span>
<span data-ttu-id="735e8-106">**Nowy — AzApplicationGatewayFirewallCondition** tworzy warunek zgodności dla niestandardowej reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="735e8-106">The **New-AzApplicationGatewayFirewallCondition** creates a match condition for firewall custom rule.</span></span>

## <span data-ttu-id="735e8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="735e8-107">EXAMPLES</span></span>

### <span data-ttu-id="735e8-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="735e8-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallCondition -MatchVariable $variable -Operator Contains -NegationCondition false -Transforms Lowercase, Trim -MatchValue abc, cde
```

<span data-ttu-id="735e8-109">Polecenie tworzy nowy warunek dopasowywania przy użyciu zmiennej Match zdefiniowanej w $variable, operator jest Contains, a warunek Negacja ma wartość FAŁSZ, transargumentami, w tym małe litery i przycinanie, to wartość dopasowania to ABC i CDE.</span><span class="sxs-lookup"><span data-stu-id="735e8-109">The command creates a new match condition using the match variable defined in the $variable, the operator is Contains and negation condition is false, Transfroms including lowercase and trim, the match value is abc and cde.</span></span> <span data-ttu-id="735e8-110">Nowy warunek zgodności zostanie zapisany w $condition.</span><span class="sxs-lookup"><span data-stu-id="735e8-110">The new match condition is saved in $condition.</span></span>

## <span data-ttu-id="735e8-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="735e8-111">PARAMETERS</span></span>

### <span data-ttu-id="735e8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="735e8-112">-DefaultProfile</span></span>
<span data-ttu-id="735e8-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="735e8-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="735e8-114">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="735e8-114">-MatchValue</span></span>
<span data-ttu-id="735e8-115">Wartość dopasowania.</span><span class="sxs-lookup"><span data-stu-id="735e8-115">Match value.</span></span>

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

### <span data-ttu-id="735e8-116">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="735e8-116">-MatchVariable</span></span>
<span data-ttu-id="735e8-117">Lista pasujących zmiennych.</span><span class="sxs-lookup"><span data-stu-id="735e8-117">List of match variables.</span></span>

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

### <span data-ttu-id="735e8-118">-NegationCondition</span><span class="sxs-lookup"><span data-stu-id="735e8-118">-NegationCondition</span></span>
<span data-ttu-id="735e8-119">W tym artykule opisano, czy jest to stan Negate.</span><span class="sxs-lookup"><span data-stu-id="735e8-119">Describes if this is negate condition or not.</span></span>

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

### <span data-ttu-id="735e8-120">-Operator</span><span class="sxs-lookup"><span data-stu-id="735e8-120">-Operator</span></span>
<span data-ttu-id="735e8-121">Opis operatora do dopasowania.</span><span class="sxs-lookup"><span data-stu-id="735e8-121">Describes operator to be matched.</span></span>

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

### <span data-ttu-id="735e8-122">-Transform</span><span class="sxs-lookup"><span data-stu-id="735e8-122">-Transform</span></span>
<span data-ttu-id="735e8-123">Lista przekształceń.</span><span class="sxs-lookup"><span data-stu-id="735e8-123">List of transforms.</span></span>

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

### <span data-ttu-id="735e8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="735e8-124">CommonParameters</span></span>
<span data-ttu-id="735e8-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="735e8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="735e8-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="735e8-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="735e8-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="735e8-127">INPUTS</span></span>

### <span data-ttu-id="735e8-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="735e8-128">None</span></span>

## <span data-ttu-id="735e8-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="735e8-129">OUTPUTS</span></span>

### <span data-ttu-id="735e8-130">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="735e8-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="735e8-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="735e8-131">NOTES</span></span>

## <span data-ttu-id="735e8-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="735e8-132">RELATED LINKS</span></span>
