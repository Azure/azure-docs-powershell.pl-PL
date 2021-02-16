---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryrulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
ms.openlocfilehash: 7d7d15fdbaac3de1a212c13fb35dee134dde5381
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177867"
---
# <span data-ttu-id="ecd6a-101">New-AzCdnDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="ecd6a-101">New-AzCdnDeliveryRuleCondition</span></span>

## <span data-ttu-id="ecd6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecd6a-102">SYNOPSIS</span></span>
<span data-ttu-id="ecd6a-103">Tworzy warunek reguły dostarczania.</span><span class="sxs-lookup"><span data-stu-id="ecd6a-103">Creates a delivery rule condition.</span></span>

## <span data-ttu-id="ecd6a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ecd6a-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRuleCondition -MatchVariable <String> -Operator <String> [-Selector <String>]
 -MatchValue <String[]> [-Transform <String>] [-NegateCondition] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ecd6a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ecd6a-105">DESCRIPTION</span></span>
<span data-ttu-id="ecd6a-106">Polecenie **cmdlet New-AzCdnDeliveryRule** tworzy regułę dostarczania dla tworzenia punktu końcowego sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="ecd6a-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="ecd6a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ecd6a-107">EXAMPLES</span></span>

### <span data-ttu-id="ecd6a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ecd6a-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleCondition -MatchVariable UrlPath -Operator Equal -MatchValue "abc"

MatchVariable   : UrlPath
Operator        : Equal
Selector        :
MatchValue      : {abc}
NegateCondition : False
Transfroms      :
```

<span data-ttu-id="ecd6a-109">Utwórz prosty warunek.</span><span class="sxs-lookup"><span data-stu-id="ecd6a-109">Create a simple condition.</span></span>

## <span data-ttu-id="ecd6a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ecd6a-110">PARAMETERS</span></span>

### <span data-ttu-id="ecd6a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecd6a-111">-DefaultProfile</span></span>
<span data-ttu-id="ecd6a-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ecd6a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecd6a-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="ecd6a-113">-MatchValue</span></span>
<span data-ttu-id="ecd6a-114">Lista możliwych wartości dopasowań.</span><span class="sxs-lookup"><span data-stu-id="ecd6a-114">List of possible match values.</span></span>

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

### <span data-ttu-id="ecd6a-115">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="ecd6a-115">-MatchVariable</span></span>
<span data-ttu-id="ecd6a-116">Zmienna dopasowania warunku.</span><span class="sxs-lookup"><span data-stu-id="ecd6a-116">Match variable of the condition.</span></span>

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

### <span data-ttu-id="ecd6a-117">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="ecd6a-117">-NegateCondition</span></span>
<span data-ttu-id="ecd6a-118">W tym artykule opisano, czy wynik tego warunku powinien zostać negowany.</span><span class="sxs-lookup"><span data-stu-id="ecd6a-118">Describes if the result of this condition should be negated.</span></span>

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

### <span data-ttu-id="ecd6a-119">-Operator</span><span class="sxs-lookup"><span data-stu-id="ecd6a-119">-Operator</span></span>
<span data-ttu-id="ecd6a-120">Opis operatora do dopasowania</span><span class="sxs-lookup"><span data-stu-id="ecd6a-120">Describes operator to be matched</span></span>

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

### <span data-ttu-id="ecd6a-121">— Selektor</span><span class="sxs-lookup"><span data-stu-id="ecd6a-121">-Selector</span></span>
<span data-ttu-id="ecd6a-122">Nazwa selektora do dopasowania</span><span class="sxs-lookup"><span data-stu-id="ecd6a-122">Name of Selector to be matched</span></span>

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

### <span data-ttu-id="ecd6a-123">— Przekształcanie</span><span class="sxs-lookup"><span data-stu-id="ecd6a-123">-Transform</span></span>
<span data-ttu-id="ecd6a-124">Przekształć, aby zastosować przed dopasowaniem.</span><span class="sxs-lookup"><span data-stu-id="ecd6a-124">Transform to apply before matching.</span></span>
<span data-ttu-id="ecd6a-125">Dopuszczalne wartości to małe i wielkie litery</span><span class="sxs-lookup"><span data-stu-id="ecd6a-125">Possible values are Lowercase and Uppercase</span></span>

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

### <span data-ttu-id="ecd6a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecd6a-126">CommonParameters</span></span>
<span data-ttu-id="ecd6a-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecd6a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecd6a-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ecd6a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecd6a-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ecd6a-129">INPUTS</span></span>

### <span data-ttu-id="ecd6a-130">Brak</span><span class="sxs-lookup"><span data-stu-id="ecd6a-130">None</span></span>

## <span data-ttu-id="ecd6a-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ecd6a-131">OUTPUTS</span></span>

### <span data-ttu-id="ecd6a-132">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDEliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="ecd6a-132">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span></span>

## <span data-ttu-id="ecd6a-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ecd6a-133">NOTES</span></span>

## <span data-ttu-id="ecd6a-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ecd6a-134">RELATED LINKS</span></span>
