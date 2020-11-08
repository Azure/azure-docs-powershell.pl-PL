---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleexclusionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleExclusionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleExclusionObject.md
ms.openlocfilehash: 1f59a7366106c59f6dc5e5af3a32368594a00537
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223488"
---
# <span data-ttu-id="2a3c9-101">New-AzFrontDoorWafManagedRuleExclusionObject</span><span class="sxs-lookup"><span data-stu-id="2a3c9-101">New-AzFrontDoorWafManagedRuleExclusionObject</span></span>

## <span data-ttu-id="2a3c9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2a3c9-102">SYNOPSIS</span></span>
<span data-ttu-id="2a3c9-103">Tworzenie obiektu wykluczania reguły zarządzanej dla zestawów reguł, grup lub reguł zarządzanych dla WAF.</span><span class="sxs-lookup"><span data-stu-id="2a3c9-103">Create managed rule exclusion object for WAF managed rule sets, groups, or rules.</span></span>

## <span data-ttu-id="2a3c9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2a3c9-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleExclusionObject -Variable <String> -Operator <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a3c9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2a3c9-105">DESCRIPTION</span></span>
<span data-ttu-id="2a3c9-106">Tworzenie obiektu wykluczania reguły zarządzanej dla zestawów reguł, grup lub reguł zarządzanych dla WAF.</span><span class="sxs-lookup"><span data-stu-id="2a3c9-106">Create managed rule exclusion object for WAF managed rule sets, groups, or rules.</span></span>

## <span data-ttu-id="2a3c9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2a3c9-107">EXAMPLES</span></span>

### <span data-ttu-id="2a3c9-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2a3c9-108">Example 1</span></span>
```powershell
PS C:> New-AzFrontDoorWafManagedRuleExclusionObject -Variable QueryStringArgNames -Operator Equals -Selector "ParameterName"

MatchVariable       SelectorMatchOperator Selector
-------------       --------------------- --------
QueryStringArgNames Equals                ParameterName
```

## <span data-ttu-id="2a3c9-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2a3c9-109">PARAMETERS</span></span>

### <span data-ttu-id="2a3c9-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a3c9-110">-DefaultProfile</span></span>
<span data-ttu-id="2a3c9-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2a3c9-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a3c9-112">-Operator</span><span class="sxs-lookup"><span data-stu-id="2a3c9-112">-Operator</span></span>
<span data-ttu-id="2a3c9-113">Operator do użycia podczas dopasowywania selektora EqualsAny oznacza brak selektora (wszystkie zmienne pasują do określonego typu)</span><span class="sxs-lookup"><span data-stu-id="2a3c9-113">Operator to use when matching the selector, EqualsAny means no selector (all match variables of the specified type)</span></span>

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

### <span data-ttu-id="2a3c9-114">-Selector</span><span class="sxs-lookup"><span data-stu-id="2a3c9-114">-Selector</span></span>
<span data-ttu-id="2a3c9-115">Deseń selektora zgodny z operatorem (jeśli operator nie jest EqualsAny)</span><span class="sxs-lookup"><span data-stu-id="2a3c9-115">Selector pattern to match using the operator (if the operator is not EqualsAny)</span></span>

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

### <span data-ttu-id="2a3c9-116">-Zmienna</span><span class="sxs-lookup"><span data-stu-id="2a3c9-116">-Variable</span></span>
<span data-ttu-id="2a3c9-117">Zmienna dopasowania.</span><span class="sxs-lookup"><span data-stu-id="2a3c9-117">Match variable.</span></span> <span data-ttu-id="2a3c9-118">Możliwe wartości to RequestHeaderNames, RequestCookieNames, QueryStringArgNames, RequestBodyPostArgNames.</span><span class="sxs-lookup"><span data-stu-id="2a3c9-118">Possible values are RequestHeaderNames, RequestCookieNames, QueryStringArgNames, RequestBodyPostArgNames.</span></span>
<span data-ttu-id="2a3c9-119">Na przykład QueryStringArgNames jest wykluczeniem parametrów GET, które pasują do selektora za pomocą danego operatora.</span><span class="sxs-lookup"><span data-stu-id="2a3c9-119">For example, QueryStringArgNames is an exclusion of GET parameters matching the selector with the given operator.</span></span>

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

### <span data-ttu-id="2a3c9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a3c9-120">CommonParameters</span></span>
<span data-ttu-id="2a3c9-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a3c9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a3c9-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a3c9-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a3c9-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a3c9-123">INPUTS</span></span>

### <span data-ttu-id="2a3c9-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="2a3c9-124">None</span></span>

## <span data-ttu-id="2a3c9-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2a3c9-125">OUTPUTS</span></span>

### <span data-ttu-id="2a3c9-126">Microsoft. Azure. Commands. FrontDoor. models. PSManagedRuleExclusion</span><span class="sxs-lookup"><span data-stu-id="2a3c9-126">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion</span></span>

## <span data-ttu-id="2a3c9-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2a3c9-127">NOTES</span></span>

## <span data-ttu-id="2a3c9-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2a3c9-128">RELATED LINKS</span></span>

<span data-ttu-id="2a3c9-129">[Nowe — AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md) 
 [Nowe — AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md) 
 [Nowe — AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="2a3c9-129">[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
