---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorrulesengineruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineRuleObject.md
ms.openlocfilehash: 7bef36412f8b1b5977e94b32d0645ccdaa8d0324
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970938"
---
# <span data-ttu-id="69c9a-101">New-AzFrontDoorRulesEngineRuleObject</span><span class="sxs-lookup"><span data-stu-id="69c9a-101">New-AzFrontDoorRulesEngineRuleObject</span></span>

## <span data-ttu-id="69c9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69c9a-102">SYNOPSIS</span></span>
<span data-ttu-id="69c9a-103">Tworzenie obiektu PSRulesEngineRule do tworzenia aparatu reguł.</span><span class="sxs-lookup"><span data-stu-id="69c9a-103">Create a PSRulesEngineRule object for Rules Engine creation.</span></span>

## <span data-ttu-id="69c9a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="69c9a-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngineRuleObject -Name <String> -Priority <Int32> -Action <PSRulesEngineAction>
 [-MatchProcessingBehavior <PSMatchProcessingBehavior>] [-MatchCondition <PSRulesEngineMatchCondition[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69c9a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="69c9a-105">DESCRIPTION</span></span>
<span data-ttu-id="69c9a-106">Tworzenie obiektu PSRulesEngineRule do tworzenia aparatu reguł.</span><span class="sxs-lookup"><span data-stu-id="69c9a-106">Create a PSRulesEngineRule object for Rules Engine creation.</span></span>

<span data-ttu-id="69c9a-107">Użyj polecenia cmdlet "New-AzFrontDoorRulesEngineActionObject", aby utworzyć obiekt PSRulesEngineAction w celu przekazania do parametru "-Action".</span><span class="sxs-lookup"><span data-stu-id="69c9a-107">Use cmdlet "New-AzFrontDoorRulesEngineActionObject" to create PSRulesEngineAction object to pass into the "-Action" parameter.</span></span>
<span data-ttu-id="69c9a-108">Użyj polecenia cmdlet "New-AzFrontDoorRulesEngineMatchConditionObject", aby utworzyć obiekt PSRulesEngineMatchCondition w celu przekazania do parametru "-MatchCondition".</span><span class="sxs-lookup"><span data-stu-id="69c9a-108">Use cmdlet "New-AzFrontDoorRulesEngineMatchConditionObject" to create PSRulesEngineMatchCondition object to pass into the "-MatchCondition" parameter.</span></span>

## <span data-ttu-id="69c9a-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="69c9a-109">EXAMPLES</span></span>

### <span data-ttu-id="69c9a-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="69c9a-110">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngineRuleObject -Name rules1 -Priority 0 -Action $rulesEngineAction -MatchProcessingBehavior Stop -MatchCondition $rulesEngineMatchCondition

Name                    : rules1
Priority                : 0
MatchProcessingBehavior : Stop
MatchCondition          : {Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchCondition}
Action                  : Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineAction


PS C:\> $rulesEngineRule1.Action

RequestHeaderActions           ResponseHeaderActions RouteConfigurationOverride
--------------------           --------------------- --------------------------
{headeraction1, headeraction2} {}                    Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingConfigurati�

PS C:\> $rulesEngineRule1.MatchCondition[0]

RulesEngineMatchVariable : RequestHeader
RulesEngineMatchValue    : {allowoverride}
Selector                 : Rules-Engine-Route-Forward
RulesEngineOperator      : Equal
NegateCondition          : False
Transforms               : {Lowercase, Uppercase}
```

<span data-ttu-id="69c9a-111">Utwórz nowy obiekt PSRulesEngineRule i zademonstruj, jak wyświetlić podpola.</span><span class="sxs-lookup"><span data-stu-id="69c9a-111">Create new PSRulesEngineRule object and demonstrate how to see the subfields.</span></span>

### <span data-ttu-id="69c9a-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="69c9a-112">Example 2</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngineRuleObject -Name rules1 -Priority -1
New-AzFrontDoorRulesEngineRuleObject : Cannot validate argument on parameter 'Priority'. The -1 argument is less than the minimum allowed range of 0. Supply an argument that is greater than or equal to 0 and then try the command again.
At line:1 char:81
+ ... ule1 = New-AzFrontDoorRulesEngineRuleObject -Name rules1 -Priority -1
+                                                                        ~~
+ CategoryInfo          : InvalidData: (:) [New-AzFrontDoorRulesEngineRuleObject], ParameterBindingValidationException
+ FullyQualifiedErrorId : ParameterArgumentValidationError,Microsoft.Azure.Commands.FrontDoor.Cmdlets.NewFrontDoorRulesEngineRuleObject
```

<span data-ttu-id="69c9a-113">Oczekiwanie wyniku podczas przekazywania wartości nieprawidłowego priorytetu.</span><span class="sxs-lookup"><span data-stu-id="69c9a-113">Expect output when passing in invalid priority value.</span></span>

## <span data-ttu-id="69c9a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69c9a-114">PARAMETERS</span></span>

### <span data-ttu-id="69c9a-115">— Akcja</span><span class="sxs-lookup"><span data-stu-id="69c9a-115">-Action</span></span>
<span data-ttu-id="69c9a-116">Akcje do wykonania w związku z żądaniem i odpowiedzią, jeśli są spełnione wszystkie warunki.</span><span class="sxs-lookup"><span data-stu-id="69c9a-116">Actions to perform on the request and response if all of the match conditions are met.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineAction
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69c9a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69c9a-117">-DefaultProfile</span></span>
<span data-ttu-id="69c9a-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="69c9a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69c9a-119">- MatchCondition</span><span class="sxs-lookup"><span data-stu-id="69c9a-119">-MatchCondition</span></span>
<span data-ttu-id="69c9a-120">Lista warunków dopasowania, które muszą zostać spełnione, aby działania tej reguły były uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="69c9a-120">A list of match conditions that must meet in order for the actions of this rule to run.</span></span> <span data-ttu-id="69c9a-121">Brak dopasowania oznacza, że akcje będą zawsze uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="69c9a-121">Having no match conditions means the actions will always run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchCondition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69c9a-122">-MatchProcessingBehavior</span><span class="sxs-lookup"><span data-stu-id="69c9a-122">-MatchProcessingBehavior</span></span>
<span data-ttu-id="69c9a-123">Jeśli ta reguła jest zgodne, aparat reguł powinien nadal uruchamiać pozostałe reguły lub je zatrzymać.</span><span class="sxs-lookup"><span data-stu-id="69c9a-123">If this rule is a match should the rules engine continue running the remaining rules or stop.</span></span>
<span data-ttu-id="69c9a-124">Dopuszczalne wartości to Continue (Kontynuuj) i Stop (Zatrzymaj).</span><span class="sxs-lookup"><span data-stu-id="69c9a-124">Possible values are Continue and Stop.</span></span>
<span data-ttu-id="69c9a-125">Jeśli nie jest obecna, domyślnie jest to ciąg Kontynuuj.</span><span class="sxs-lookup"><span data-stu-id="69c9a-125">If not present, defaults to Continue.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMatchProcessingBehavior
Parameter Sets: (All)
Aliases:
Accepted values: Continue, Stop

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69c9a-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="69c9a-126">-Name</span></span>
<span data-ttu-id="69c9a-127">Nazwa odwołująca się do tej konkretnej reguły.</span><span class="sxs-lookup"><span data-stu-id="69c9a-127">A name to refer to this specific rule.</span></span>

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

### <span data-ttu-id="69c9a-128">— Priority (Priorytet)</span><span class="sxs-lookup"><span data-stu-id="69c9a-128">-Priority</span></span>
<span data-ttu-id="69c9a-129">Priorytet przypisany do tej reguły.</span><span class="sxs-lookup"><span data-stu-id="69c9a-129">A priority assigned to this rule.</span></span>
<span data-ttu-id="69c9a-130">Nie może być ujemna.</span><span class="sxs-lookup"><span data-stu-id="69c9a-130">Cannot be negative.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69c9a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69c9a-131">CommonParameters</span></span>
<span data-ttu-id="69c9a-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69c9a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69c9a-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="69c9a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69c9a-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69c9a-134">INPUTS</span></span>

### <span data-ttu-id="69c9a-135">Brak</span><span class="sxs-lookup"><span data-stu-id="69c9a-135">None</span></span>

## <span data-ttu-id="69c9a-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69c9a-136">OUTPUTS</span></span>

### <span data-ttu-id="69c9a-137">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineRule</span><span class="sxs-lookup"><span data-stu-id="69c9a-137">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineRule</span></span>

## <span data-ttu-id="69c9a-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="69c9a-138">NOTES</span></span>

## <span data-ttu-id="69c9a-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="69c9a-139">RELATED LINKS</span></span>
