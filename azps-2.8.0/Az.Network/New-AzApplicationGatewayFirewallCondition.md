---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
ms.openlocfilehash: aec627fdc8889d6bcfc4fb8e7762eb3be7bf0432
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870019"
---
# <span data-ttu-id="ab1cd-101">New-AzApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="ab1cd-101">New-AzApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="ab1cd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ab1cd-102">SYNOPSIS</span></span>
<span data-ttu-id="ab1cd-103">Tworzy warunek zgodności dla reguły niestandardowej</span><span class="sxs-lookup"><span data-stu-id="ab1cd-103">Creates a match condition for custom rule</span></span>

## <span data-ttu-id="ab1cd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ab1cd-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCondition -MatchVariable <PSApplicationGatewayFirewallMatchVariable[]>
 -Operator <String> [-NegationCondition <Boolean>] -MatchValue <String[]> [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab1cd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ab1cd-105">DESCRIPTION</span></span>
<span data-ttu-id="ab1cd-106">**Nowy — AzApplicationGatewayFirewallCondition** tworzy warunek zgodności dla niestandardowej reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="ab1cd-106">The **New-AzApplicationGatewayFirewallCondition** creates a match condition for firewall custom rule.</span></span>

## <span data-ttu-id="ab1cd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ab1cd-107">EXAMPLES</span></span>

### <span data-ttu-id="ab1cd-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ab1cd-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallConditon -MatchVariables $variable -Operator Contains -NegationConditon false -Transforms Lowercase, Trim -MatchValues abc, cde
```

<span data-ttu-id="ab1cd-109">Polecenie tworzy nowy warunek dopasowywania przy użyciu zmiennej Match zdefiniowanej w $variable, operator jest Contains, a warunek Negacja ma wartość FAŁSZ, transargumentami, w tym małe litery i przycinanie, to wartość dopasowania to ABC i CDE.</span><span class="sxs-lookup"><span data-stu-id="ab1cd-109">The command creates a new match condition using the match variable defined in the $variable, the operator is Contains and negation condition is false, Transfroms including lowercase and trim, the match value is abc and cde.</span></span> <span data-ttu-id="ab1cd-110">Nowy warunek zgodności zostanie zapisany w $condition.</span><span class="sxs-lookup"><span data-stu-id="ab1cd-110">The new match condition is saved in $condition.</span></span>

## <span data-ttu-id="ab1cd-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ab1cd-111">PARAMETERS</span></span>

### <span data-ttu-id="ab1cd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab1cd-112">-DefaultProfile</span></span>
<span data-ttu-id="ab1cd-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ab1cd-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab1cd-114">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="ab1cd-114">-MatchValue</span></span>
<span data-ttu-id="ab1cd-115">Wartość dopasowania.</span><span class="sxs-lookup"><span data-stu-id="ab1cd-115">Match value.</span></span>

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

### <span data-ttu-id="ab1cd-116">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="ab1cd-116">-MatchVariable</span></span>
<span data-ttu-id="ab1cd-117">Lista pasujących zmiennych.</span><span class="sxs-lookup"><span data-stu-id="ab1cd-117">List of match variables.</span></span>

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

### <span data-ttu-id="ab1cd-118">-NegationCondition</span><span class="sxs-lookup"><span data-stu-id="ab1cd-118">-NegationCondition</span></span>
<span data-ttu-id="ab1cd-119">W tym artykule opisano, czy jest to stan Negate.</span><span class="sxs-lookup"><span data-stu-id="ab1cd-119">Describes if this is negate condition or not.</span></span>

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

### <span data-ttu-id="ab1cd-120">-Operator</span><span class="sxs-lookup"><span data-stu-id="ab1cd-120">-Operator</span></span>
<span data-ttu-id="ab1cd-121">Opis operatora do dopasowania.</span><span class="sxs-lookup"><span data-stu-id="ab1cd-121">Describes operator to be matched.</span></span>

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

### <span data-ttu-id="ab1cd-122">-Transform</span><span class="sxs-lookup"><span data-stu-id="ab1cd-122">-Transform</span></span>
<span data-ttu-id="ab1cd-123">Lista przekształceń.</span><span class="sxs-lookup"><span data-stu-id="ab1cd-123">List of transforms.</span></span>

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

### <span data-ttu-id="ab1cd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab1cd-124">CommonParameters</span></span>
<span data-ttu-id="ab1cd-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab1cd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab1cd-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab1cd-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab1cd-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab1cd-127">INPUTS</span></span>

### <span data-ttu-id="ab1cd-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ab1cd-128">None</span></span>

## <span data-ttu-id="ab1cd-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ab1cd-129">OUTPUTS</span></span>

### <span data-ttu-id="ab1cd-130">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="ab1cd-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="ab1cd-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ab1cd-131">NOTES</span></span>

## <span data-ttu-id="ab1cd-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ab1cd-132">RELATED LINKS</span></span>
