---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesenginematchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineMatchConditionObject.md
ms.openlocfilehash: 991d3233dd484025e699bba455b7d43e86f586e7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062229"
---
# <span data-ttu-id="f7fb1-101">New-AzFrontDoorRulesEngineMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="f7fb1-101">New-AzFrontDoorRulesEngineMatchConditionObject</span></span>

## <span data-ttu-id="f7fb1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f7fb1-102">SYNOPSIS</span></span>
<span data-ttu-id="f7fb1-103">Utwórz obiekt PSRulesEngineMatchCondition, aby utworzyć regułę aparatu reguł.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-103">Create a PSRulesEngineMatchCondition object for creating a rules engine rule.</span></span>

## <span data-ttu-id="f7fb1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f7fb1-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngineMatchConditionObject -MatchVariable <PSRulesEngineMatchVariable>
 -MatchValue <String[]> [-Selector <String>] [-Operator <PSRulesEngineOperator>] [-NegateCondition <Boolean>]
 [-Transform <PSTransform[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7fb1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f7fb1-105">DESCRIPTION</span></span>
<span data-ttu-id="f7fb1-106">Utwórz obiekt PSRulesEngineMatchCondition, aby utworzyć regułę aparatu reguł.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-106">Create a PSRulesEngineMatchCondition object for creating a rules engine rule.</span></span>

## <span data-ttu-id="f7fb1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f7fb1-107">EXAMPLES</span></span>

### <span data-ttu-id="f7fb1-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f7fb1-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngineMatchConditionObject -MatchVariable RequestHeader -Operator Equal -MatchValue allowoverride -Transform "LowerCase", "UpperCase"-Selector Rules-Engine-Route-Forward -NegateCondition $false

RulesEngineMatchVariable : RequestHeader
RulesEngineMatchValue    : {allowoverride}
Selector                 : Rules-Engine-Route-Forward
RulesEngineOperator      : Equal
NegateCondition          : False
Transform                : {Lowercase, Uppercase}
```

<span data-ttu-id="f7fb1-109">Greate nowy obiekt PSRulesEngineMatchCondition.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-109">Greate a new PSRulesEngineMatchCondition object.</span></span>

## <span data-ttu-id="f7fb1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f7fb1-110">PARAMETERS</span></span>

### <span data-ttu-id="f7fb1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7fb1-111">-DefaultProfile</span></span>
<span data-ttu-id="f7fb1-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7fb1-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="f7fb1-113">-MatchValue</span></span>
<span data-ttu-id="f7fb1-114">Dopasuj wartości do.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-114">Match values to match against.</span></span>
<span data-ttu-id="f7fb1-115">Operator będzie stosować się do każdej wartości w tym miejscu lub z semantyką.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-115">The operator will apply to each value in here with OR semantics.</span></span>
<span data-ttu-id="f7fb1-116">Jeśli którykolwiek z tych elementów odpowiada zmiennej z danym operatorem, ten warunek dopasowywania jest traktowany jako odpowiednik.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-116">If any of them match the variable with the given operator this match condition is considered a match.</span></span>

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

### <span data-ttu-id="f7fb1-117">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="f7fb1-117">-MatchVariable</span></span>
<span data-ttu-id="f7fb1-118">Zmienna dopasowania.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-118">Match Variable.</span></span>
<span data-ttu-id="f7fb1-119">Możliwe wartości to IsMobile, RemoteAddr, RequestMethod, QueryString, PostArg, RequestUri, RequestPath, RequestFileName, RequestfilenameExtension, RequestHeader, RequestBody, RequestScheme</span><span class="sxs-lookup"><span data-stu-id="f7fb1-119">Possible values are IsMobile, RemoteAddr, RequestMethod, QueryString, PostArg, RequestUri, RequestPath, RequestFileName, RequestfilenameExtension, RequestHeader, RequestBody, RequestScheme</span></span>

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

### <span data-ttu-id="f7fb1-120">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="f7fb1-120">-NegateCondition</span></span>
<span data-ttu-id="f7fb1-121">W tym artykule opisano, czy jest to warunek Negate</span><span class="sxs-lookup"><span data-stu-id="f7fb1-121">Describes if this is negate condition or not</span></span>

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

### <span data-ttu-id="f7fb1-122">-Operator</span><span class="sxs-lookup"><span data-stu-id="f7fb1-122">-Operator</span></span>
<span data-ttu-id="f7fb1-123">W tym artykule opisano operator, którego należy użyć do warunku dopasowywania.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-123">Describes operator to apply to the match condition.</span></span>
<span data-ttu-id="f7fb1-124">Możliwe wartości to dowolny, IPMatch, geodopasowanie, równa się, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-124">Possible values are Any, IPMatch, GeoMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith.</span></span>

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

### <span data-ttu-id="f7fb1-125">-Selector</span><span class="sxs-lookup"><span data-stu-id="f7fb1-125">-Selector</span></span>
<span data-ttu-id="f7fb1-126">Nazwa selektora w programie RequestHeader lub RequestBody do dopasowania</span><span class="sxs-lookup"><span data-stu-id="f7fb1-126">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="f7fb1-127">-Transform</span><span class="sxs-lookup"><span data-stu-id="f7fb1-127">-Transform</span></span>
<span data-ttu-id="f7fb1-128">Lista elementów przekształceń, które są stosowane przed dopasowaniem.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-128">List of what transforms are applied before matching.</span></span> <span data-ttu-id="f7fb1-129">Możliwe wartości poszczególnych przekształceń to małe, wielkie, przycinanie, UrlDecode, UrlEncode, RemoveNulls.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-129">Possible individual transform values are Lowercase, Uppercase, Trim, UrlDecode, UrlEncode, RemoveNulls.</span></span>

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

### <span data-ttu-id="f7fb1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7fb1-130">CommonParameters</span></span>
<span data-ttu-id="f7fb1-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7fb1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7fb1-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7fb1-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7fb1-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f7fb1-133">INPUTS</span></span>

### <span data-ttu-id="f7fb1-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f7fb1-134">None</span></span>

## <span data-ttu-id="f7fb1-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f7fb1-135">OUTPUTS</span></span>

### <span data-ttu-id="f7fb1-136">Microsoft. Azure. Commands. FrontDoor. models. PSRulesEngineMatchCondition</span><span class="sxs-lookup"><span data-stu-id="f7fb1-136">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchCondition</span></span>

## <span data-ttu-id="f7fb1-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f7fb1-137">NOTES</span></span>

## <span data-ttu-id="f7fb1-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f7fb1-138">RELATED LINKS</span></span>
