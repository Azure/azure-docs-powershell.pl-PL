---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleexclusionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleExclusionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleExclusionObject.md
ms.openlocfilehash: 4f8764a40d536897ee71e36c1be1d691040e2ab9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970890"
---
# <span data-ttu-id="a966e-101">New-AzFrontDoorWafManagedRuleExclusionObject</span><span class="sxs-lookup"><span data-stu-id="a966e-101">New-AzFrontDoorWafManagedRuleExclusionObject</span></span>

## <span data-ttu-id="a966e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a966e-102">SYNOPSIS</span></span>
<span data-ttu-id="a966e-103">Utwórz obiekt wykluczeń reguł zarządzanych dla zestawów reguł zarządzanych przez sieć WAF, grup lub reguł.</span><span class="sxs-lookup"><span data-stu-id="a966e-103">Create managed rule exclusion object for WAF managed rule sets, groups, or rules.</span></span>

## <span data-ttu-id="a966e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a966e-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleExclusionObject -Variable <String> -Operator <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a966e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a966e-105">DESCRIPTION</span></span>
<span data-ttu-id="a966e-106">Utwórz obiekt wykluczeń reguł zarządzanych dla zestawów reguł zarządzanych przez sieć WAF, grup lub reguł.</span><span class="sxs-lookup"><span data-stu-id="a966e-106">Create managed rule exclusion object for WAF managed rule sets, groups, or rules.</span></span>

## <span data-ttu-id="a966e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a966e-107">EXAMPLES</span></span>

### <span data-ttu-id="a966e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a966e-108">Example 1</span></span>
```powershell
PS C:> New-AzFrontDoorWafManagedRuleExclusionObject -Variable QueryStringArgNames -Operator Equals -Selector "ParameterName"

MatchVariable       SelectorMatchOperator Selector
-------------       --------------------- --------
QueryStringArgNames Equals                ParameterName
```

## <span data-ttu-id="a966e-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a966e-109">PARAMETERS</span></span>

### <span data-ttu-id="a966e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a966e-110">-DefaultProfile</span></span>
<span data-ttu-id="a966e-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a966e-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a966e-112">-Operator</span><span class="sxs-lookup"><span data-stu-id="a966e-112">-Operator</span></span>
<span data-ttu-id="a966e-113">Operator do użycia podczas dopasowywania selektora, równa sięAny oznacza brak selektora (wszystkie zmienne dopasowania określonego typu)</span><span class="sxs-lookup"><span data-stu-id="a966e-113">Operator to use when matching the selector, EqualsAny means no selector (all match variables of the specified type)</span></span>

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

### <span data-ttu-id="a966e-114">— Selektor</span><span class="sxs-lookup"><span data-stu-id="a966e-114">-Selector</span></span>
<span data-ttu-id="a966e-115">Wzorzec selektora do dopasowania przy użyciu operatora (jeśli operator nie jest równyAny)</span><span class="sxs-lookup"><span data-stu-id="a966e-115">Selector pattern to match using the operator (if the operator is not EqualsAny)</span></span>

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

### <span data-ttu-id="a966e-116">—Zmienna</span><span class="sxs-lookup"><span data-stu-id="a966e-116">-Variable</span></span>
<span data-ttu-id="a966e-117">Dopasuj zmienną.</span><span class="sxs-lookup"><span data-stu-id="a966e-117">Match variable.</span></span> <span data-ttu-id="a966e-118">Dopuszczalne wartości to: RequestHeaderNames, RequestCookieNames, QueryStringArgNames, RequestBodyPostArgNames.</span><span class="sxs-lookup"><span data-stu-id="a966e-118">Possible values are RequestHeaderNames, RequestCookieNames, QueryStringArgNames, RequestBodyPostArgNames.</span></span>
<span data-ttu-id="a966e-119">Na przykład zapytanieStringArgNames jest wykluczeniem parametrów GET pasujących selektora do danego operatora.</span><span class="sxs-lookup"><span data-stu-id="a966e-119">For example, QueryStringArgNames is an exclusion of GET parameters matching the selector with the given operator.</span></span>

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

### <span data-ttu-id="a966e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a966e-120">CommonParameters</span></span>
<span data-ttu-id="a966e-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a966e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a966e-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a966e-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a966e-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a966e-123">INPUTS</span></span>

### <span data-ttu-id="a966e-124">Brak</span><span class="sxs-lookup"><span data-stu-id="a966e-124">None</span></span>

## <span data-ttu-id="a966e-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a966e-125">OUTPUTS</span></span>

### <span data-ttu-id="a966e-126">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion</span><span class="sxs-lookup"><span data-stu-id="a966e-126">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion</span></span>

## <span data-ttu-id="a966e-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a966e-127">NOTES</span></span>

## <span data-ttu-id="a966e-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a966e-128">RELATED LINKS</span></span>

<span data-ttu-id="a966e-129">[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md) 
 [New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md) 
 [New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="a966e-129">[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
