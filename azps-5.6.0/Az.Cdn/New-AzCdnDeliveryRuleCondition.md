---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/new-azcdndeliveryrulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
ms.openlocfilehash: 6367910117ff00219c3194a06bb51754913df063
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009217"
---
# <span data-ttu-id="69141-101">New-AzCdnDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="69141-101">New-AzCdnDeliveryRuleCondition</span></span>

## <span data-ttu-id="69141-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69141-102">SYNOPSIS</span></span>
<span data-ttu-id="69141-103">Tworzy warunek reguły dostarczania.</span><span class="sxs-lookup"><span data-stu-id="69141-103">Creates a delivery rule condition.</span></span>

## <span data-ttu-id="69141-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="69141-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRuleCondition -MatchVariable <String> -Operator <String> [-Selector <String>]
 -MatchValue <String[]> [-Transform <String>] [-NegateCondition] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="69141-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="69141-105">DESCRIPTION</span></span>
<span data-ttu-id="69141-106">Polecenie **cmdlet New-AzCdnDeliveryRule** tworzy regułę dostarczania dla tworzenia punktu końcowego sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="69141-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="69141-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="69141-107">EXAMPLES</span></span>

### <span data-ttu-id="69141-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="69141-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleCondition -MatchVariable UrlPath -Operator Equal -MatchValue "abc"

MatchVariable   : UrlPath
Operator        : Equal
Selector        :
MatchValue      : {abc}
NegateCondition : False
Transfroms      :
```

<span data-ttu-id="69141-109">Utwórz prosty warunek.</span><span class="sxs-lookup"><span data-stu-id="69141-109">Create a simple condition.</span></span>

## <span data-ttu-id="69141-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69141-110">PARAMETERS</span></span>

### <span data-ttu-id="69141-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69141-111">-DefaultProfile</span></span>
<span data-ttu-id="69141-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="69141-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69141-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="69141-113">-MatchValue</span></span>
<span data-ttu-id="69141-114">Lista możliwych wartości dopasowań.</span><span class="sxs-lookup"><span data-stu-id="69141-114">List of possible match values.</span></span>

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

### <span data-ttu-id="69141-115">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="69141-115">-MatchVariable</span></span>
<span data-ttu-id="69141-116">Zmienna dopasowania warunku.</span><span class="sxs-lookup"><span data-stu-id="69141-116">Match variable of the condition.</span></span>

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

### <span data-ttu-id="69141-117">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="69141-117">-NegateCondition</span></span>
<span data-ttu-id="69141-118">W tym artykule opisano, czy wynik tego warunku powinien zostać negowany.</span><span class="sxs-lookup"><span data-stu-id="69141-118">Describes if the result of this condition should be negated.</span></span>

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

### <span data-ttu-id="69141-119">-Operator</span><span class="sxs-lookup"><span data-stu-id="69141-119">-Operator</span></span>
<span data-ttu-id="69141-120">Opis operatora do dopasowania</span><span class="sxs-lookup"><span data-stu-id="69141-120">Describes operator to be matched</span></span>

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

### <span data-ttu-id="69141-121">— Selektor</span><span class="sxs-lookup"><span data-stu-id="69141-121">-Selector</span></span>
<span data-ttu-id="69141-122">Nazwa selektora do dopasowania</span><span class="sxs-lookup"><span data-stu-id="69141-122">Name of Selector to be matched</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69141-123">— Przekształcanie</span><span class="sxs-lookup"><span data-stu-id="69141-123">-Transform</span></span>
<span data-ttu-id="69141-124">Przekształć, aby zastosować przed dopasowaniem.</span><span class="sxs-lookup"><span data-stu-id="69141-124">Transform to apply before matching.</span></span>
<span data-ttu-id="69141-125">Dopuszczalne wartości to małe i wielkie litery</span><span class="sxs-lookup"><span data-stu-id="69141-125">Possible values are Lowercase and Uppercase</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69141-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69141-126">CommonParameters</span></span>
<span data-ttu-id="69141-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69141-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69141-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="69141-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69141-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69141-129">INPUTS</span></span>

### <span data-ttu-id="69141-130">Brak</span><span class="sxs-lookup"><span data-stu-id="69141-130">None</span></span>

## <span data-ttu-id="69141-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69141-131">OUTPUTS</span></span>

### <span data-ttu-id="69141-132">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDEliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="69141-132">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span></span>

## <span data-ttu-id="69141-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="69141-133">NOTES</span></span>

## <span data-ttu-id="69141-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="69141-134">RELATED LINKS</span></span>
