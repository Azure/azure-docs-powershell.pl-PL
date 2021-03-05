---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorrulesenginematchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineMatchConditionObject.md
ms.openlocfilehash: 4f35b20b7c17a0cd809cb5964fbecfa429b581bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970954"
---
# <span data-ttu-id="14b9a-101">New-AzFrontDoorRulesEngineMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="14b9a-101">New-AzFrontDoorRulesEngineMatchConditionObject</span></span>

## <span data-ttu-id="14b9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14b9a-102">SYNOPSIS</span></span>
<span data-ttu-id="14b9a-103">Tworzenie obiektu PSRulesEngineMatchCondition w celu utworzenia reguły aparatu reguł.</span><span class="sxs-lookup"><span data-stu-id="14b9a-103">Create a PSRulesEngineMatchCondition object for creating a rules engine rule.</span></span>

## <span data-ttu-id="14b9a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="14b9a-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngineMatchConditionObject -MatchVariable <PSRulesEngineMatchVariable>
 -MatchValue <String[]> [-Selector <String>] [-Operator <PSRulesEngineOperator>] [-NegateCondition <Boolean>]
 [-Transform <PSTransform[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14b9a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="14b9a-105">DESCRIPTION</span></span>
<span data-ttu-id="14b9a-106">Tworzenie obiektu PSRulesEngineMatchCondition w celu utworzenia reguły aparatu reguł.</span><span class="sxs-lookup"><span data-stu-id="14b9a-106">Create a PSRulesEngineMatchCondition object for creating a rules engine rule.</span></span>

## <span data-ttu-id="14b9a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="14b9a-107">EXAMPLES</span></span>

### <span data-ttu-id="14b9a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="14b9a-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngineMatchConditionObject -MatchVariable RequestHeader -Operator Equal -MatchValue allowoverride -Transform "LowerCase", "UpperCase"-Selector Rules-Engine-Route-Forward -NegateCondition $false

RulesEngineMatchVariable : RequestHeader
RulesEngineMatchValue    : {allowoverride}
Selector                 : Rules-Engine-Route-Forward
RulesEngineOperator      : Equal
NegateCondition          : False
Transform                : {Lowercase, Uppercase}
```

<span data-ttu-id="14b9a-109">Greate a new PSRulesEngineMatchCondition object.</span><span class="sxs-lookup"><span data-stu-id="14b9a-109">Greate a new PSRulesEngineMatchCondition object.</span></span>

## <span data-ttu-id="14b9a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14b9a-110">PARAMETERS</span></span>

### <span data-ttu-id="14b9a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14b9a-111">-DefaultProfile</span></span>
<span data-ttu-id="14b9a-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="14b9a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14b9a-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="14b9a-113">-MatchValue</span></span>
<span data-ttu-id="14b9a-114">Dopasuj wartości do dopasowania.</span><span class="sxs-lookup"><span data-stu-id="14b9a-114">Match values to match against.</span></span>
<span data-ttu-id="14b9a-115">Operator zostanie tutaj zastosuje do każdej wartości z semantyką OR.</span><span class="sxs-lookup"><span data-stu-id="14b9a-115">The operator will apply to each value in here with OR semantics.</span></span>
<span data-ttu-id="14b9a-116">Jeśli którykolwiek z nich pasuje do zmiennej dla danego operatora, ten warunek dopasowania jest uznawany za dopasowanie.</span><span class="sxs-lookup"><span data-stu-id="14b9a-116">If any of them match the variable with the given operator this match condition is considered a match.</span></span>

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

### <span data-ttu-id="14b9a-117">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="14b9a-117">-MatchVariable</span></span>
<span data-ttu-id="14b9a-118">Dopasuj zmienną.</span><span class="sxs-lookup"><span data-stu-id="14b9a-118">Match Variable.</span></span>
<span data-ttu-id="14b9a-119">Dopuszczalne wartości to IsMobile, RemoteAddr, RequestMethod, QueryString, PostArg, RequestUri, RequestPath, RequestFileName, RequestfilenameExtension, RequestHeader, RequestBody, RequestScheme</span><span class="sxs-lookup"><span data-stu-id="14b9a-119">Possible values are IsMobile, RemoteAddr, RequestMethod, QueryString, PostArg, RequestUri, RequestPath, RequestFileName, RequestfilenameExtension, RequestHeader, RequestBody, RequestScheme</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchVariable
Parameter Sets: (All)
Aliases:
Accepted values: IsMobile, RemoteAddr, RequestMethod, QueryString, PostArgs, RequestUri, RequestPath, RequestFilename, RequestFilenameExtension, RequestHeader, RequestBody, RequestScheme

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14b9a-120">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="14b9a-120">-NegateCondition</span></span>
<span data-ttu-id="14b9a-121">W tym artykule opisano, czy jest to warunek negatywowy, czy nie.</span><span class="sxs-lookup"><span data-stu-id="14b9a-121">Describes if this is negate condition or not</span></span>

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

### <span data-ttu-id="14b9a-122">-Operator</span><span class="sxs-lookup"><span data-stu-id="14b9a-122">-Operator</span></span>
<span data-ttu-id="14b9a-123">W tym artykule opisano operator, który należy zastosować do warunku dopasowania.</span><span class="sxs-lookup"><span data-stu-id="14b9a-123">Describes operator to apply to the match condition.</span></span>
<span data-ttu-id="14b9a-124">Dopuszczalne wartości to Any, IPMatch, GeoMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith.</span><span class="sxs-lookup"><span data-stu-id="14b9a-124">Possible values are Any, IPMatch, GeoMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineOperator
Parameter Sets: (All)
Aliases:
Accepted values: Any, IPMatch, GeoMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14b9a-125">— Selektor</span><span class="sxs-lookup"><span data-stu-id="14b9a-125">-Selector</span></span>
<span data-ttu-id="14b9a-126">Nazwa selektora w polach RequestHeader lub RequestBody do dopasowania</span><span class="sxs-lookup"><span data-stu-id="14b9a-126">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="14b9a-127">— Przekształcanie</span><span class="sxs-lookup"><span data-stu-id="14b9a-127">-Transform</span></span>
<span data-ttu-id="14b9a-128">Lista przekształceń, które są stosowane przed ich dopasowaniem.</span><span class="sxs-lookup"><span data-stu-id="14b9a-128">List of what transforms are applied before matching.</span></span> <span data-ttu-id="14b9a-129">Możliwe wartości poszczególnych przekształceń to Małe litery, Wielkie litery, Trim, UrlDecode, UrlEncode, RemoveNulls.</span><span class="sxs-lookup"><span data-stu-id="14b9a-129">Possible individual transform values are Lowercase, Uppercase, Trim, UrlDecode, UrlEncode, RemoveNulls.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSTransform[]
Parameter Sets: (All)
Aliases:
Accepted values: Lowercase, Uppercase, Trim, UrlDecode, UrlEncode, RemoveNulls

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14b9a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14b9a-130">CommonParameters</span></span>
<span data-ttu-id="14b9a-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14b9a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14b9a-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="14b9a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14b9a-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14b9a-133">INPUTS</span></span>

### <span data-ttu-id="14b9a-134">Brak</span><span class="sxs-lookup"><span data-stu-id="14b9a-134">None</span></span>

## <span data-ttu-id="14b9a-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14b9a-135">OUTPUTS</span></span>

### <span data-ttu-id="14b9a-136">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchCondition</span><span class="sxs-lookup"><span data-stu-id="14b9a-136">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchCondition</span></span>

## <span data-ttu-id="14b9a-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="14b9a-137">NOTES</span></span>

## <span data-ttu-id="14b9a-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="14b9a-138">RELATED LINKS</span></span>
