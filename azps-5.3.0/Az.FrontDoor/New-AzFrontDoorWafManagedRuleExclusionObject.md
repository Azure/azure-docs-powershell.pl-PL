---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleexclusionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleExclusionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleExclusionObject.md
ms.openlocfilehash: 1f59a7366106c59f6dc5e5af3a32368594a00537
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489713"
---
# <span data-ttu-id="70035-101">New-AzFrontDoorWafManagedRuleExclusionObject</span><span class="sxs-lookup"><span data-stu-id="70035-101">New-AzFrontDoorWafManagedRuleExclusionObject</span></span>

## <span data-ttu-id="70035-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="70035-102">SYNOPSIS</span></span>
<span data-ttu-id="70035-103">Tworzenie obiektu wykluczania reguły zarządzanej dla zestawów reguł, grup lub reguł zarządzanych dla WAF.</span><span class="sxs-lookup"><span data-stu-id="70035-103">Create managed rule exclusion object for WAF managed rule sets, groups, or rules.</span></span>

## <span data-ttu-id="70035-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="70035-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleExclusionObject -Variable <String> -Operator <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70035-105">Opis</span><span class="sxs-lookup"><span data-stu-id="70035-105">DESCRIPTION</span></span>
<span data-ttu-id="70035-106">Tworzenie obiektu wykluczania reguły zarządzanej dla zestawów reguł, grup lub reguł zarządzanych dla WAF.</span><span class="sxs-lookup"><span data-stu-id="70035-106">Create managed rule exclusion object for WAF managed rule sets, groups, or rules.</span></span>

## <span data-ttu-id="70035-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="70035-107">EXAMPLES</span></span>

### <span data-ttu-id="70035-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="70035-108">Example 1</span></span>
```powershell
PS C:> New-AzFrontDoorWafManagedRuleExclusionObject -Variable QueryStringArgNames -Operator Equals -Selector "ParameterName"

MatchVariable       SelectorMatchOperator Selector
-------------       --------------------- --------
QueryStringArgNames Equals                ParameterName
```

## <span data-ttu-id="70035-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="70035-109">PARAMETERS</span></span>

### <span data-ttu-id="70035-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70035-110">-DefaultProfile</span></span>
<span data-ttu-id="70035-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="70035-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70035-112">-Operator</span><span class="sxs-lookup"><span data-stu-id="70035-112">-Operator</span></span>
<span data-ttu-id="70035-113">Operator do użycia podczas dopasowywania selektora EqualsAny oznacza brak selektora (wszystkie zmienne pasują do określonego typu)</span><span class="sxs-lookup"><span data-stu-id="70035-113">Operator to use when matching the selector, EqualsAny means no selector (all match variables of the specified type)</span></span>

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

### <span data-ttu-id="70035-114">-Selector</span><span class="sxs-lookup"><span data-stu-id="70035-114">-Selector</span></span>
<span data-ttu-id="70035-115">Deseń selektora zgodny z operatorem (jeśli operator nie jest EqualsAny)</span><span class="sxs-lookup"><span data-stu-id="70035-115">Selector pattern to match using the operator (if the operator is not EqualsAny)</span></span>

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

### <span data-ttu-id="70035-116">-Zmienna</span><span class="sxs-lookup"><span data-stu-id="70035-116">-Variable</span></span>
<span data-ttu-id="70035-117">Zmienna dopasowania.</span><span class="sxs-lookup"><span data-stu-id="70035-117">Match variable.</span></span> <span data-ttu-id="70035-118">Możliwe wartości to RequestHeaderNames, RequestCookieNames, QueryStringArgNames, RequestBodyPostArgNames.</span><span class="sxs-lookup"><span data-stu-id="70035-118">Possible values are RequestHeaderNames, RequestCookieNames, QueryStringArgNames, RequestBodyPostArgNames.</span></span>
<span data-ttu-id="70035-119">Na przykład QueryStringArgNames jest wykluczeniem parametrów GET, które pasują do selektora za pomocą danego operatora.</span><span class="sxs-lookup"><span data-stu-id="70035-119">For example, QueryStringArgNames is an exclusion of GET parameters matching the selector with the given operator.</span></span>

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

### <span data-ttu-id="70035-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70035-120">CommonParameters</span></span>
<span data-ttu-id="70035-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70035-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70035-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="70035-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70035-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="70035-123">INPUTS</span></span>

### <span data-ttu-id="70035-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="70035-124">None</span></span>

## <span data-ttu-id="70035-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="70035-125">OUTPUTS</span></span>

### <span data-ttu-id="70035-126">Microsoft. Azure. Commands. FrontDoor. models. PSManagedRuleExclusion</span><span class="sxs-lookup"><span data-stu-id="70035-126">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion</span></span>

## <span data-ttu-id="70035-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="70035-127">NOTES</span></span>

## <span data-ttu-id="70035-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="70035-128">RELATED LINKS</span></span>

<span data-ttu-id="70035-129">[Nowe — AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md) 
 [Nowe — AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md) 
 [Nowe — AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="70035-129">[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
