---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesengineruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineRuleObject.md
ms.openlocfilehash: c02fa092532f70567405f314dc8943e4e2ce51f6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94231880"
---
# <span data-ttu-id="ed2c5-101">New-AzFrontDoorRulesEngineRuleObject</span><span class="sxs-lookup"><span data-stu-id="ed2c5-101">New-AzFrontDoorRulesEngineRuleObject</span></span>

## <span data-ttu-id="ed2c5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ed2c5-102">SYNOPSIS</span></span>
<span data-ttu-id="ed2c5-103">Utwórz obiekt PSRulesEngineRule, aby uzyskać reguły tworzenia aparatu.</span><span class="sxs-lookup"><span data-stu-id="ed2c5-103">Create a PSRulesEngineRule object for Rules Engine creation.</span></span>

## <span data-ttu-id="ed2c5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ed2c5-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngineRuleObject -Name <String> -Priority <Int32> -Action <PSRulesEngineAction>
 [-MatchProcessingBehavior <PSMatchProcessingBehavior>] [-MatchCondition <PSRulesEngineMatchCondition[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed2c5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ed2c5-105">DESCRIPTION</span></span>
<span data-ttu-id="ed2c5-106">Utwórz obiekt PSRulesEngineRule, aby uzyskać reguły tworzenia aparatu.</span><span class="sxs-lookup"><span data-stu-id="ed2c5-106">Create a PSRulesEngineRule object for Rules Engine creation.</span></span>

<span data-ttu-id="ed2c5-107">Użyj polecenia cmdlet "New-AzFrontDoorRulesEngineActionObject", aby utworzyć obiekt PSRulesEngineAction w celu przekazania go do parametru "-Action".</span><span class="sxs-lookup"><span data-stu-id="ed2c5-107">Use cmdlet "New-AzFrontDoorRulesEngineActionObject" to create PSRulesEngineAction object to pass into the "-Action" parameter.</span></span>
<span data-ttu-id="ed2c5-108">Użyj polecenia cmdlet "New-AzFrontDoorRulesEngineMatchConditionObject", aby utworzyć obiekt PSRulesEngineMatchCondition w celu przekazania go do parametru "-MatchCondition".</span><span class="sxs-lookup"><span data-stu-id="ed2c5-108">Use cmdlet "New-AzFrontDoorRulesEngineMatchConditionObject" to create PSRulesEngineMatchCondition object to pass into the "-MatchCondition" parameter.</span></span>

## <span data-ttu-id="ed2c5-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ed2c5-109">EXAMPLES</span></span>

### <span data-ttu-id="ed2c5-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ed2c5-110">Example 1</span></span>
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

<span data-ttu-id="ed2c5-111">Utwórz nowy obiekt PSRulesEngineRule, aby pokazać, jak wyświetlić pola.</span><span class="sxs-lookup"><span data-stu-id="ed2c5-111">Create new PSRulesEngineRule object and demonstrate how to see the subfields.</span></span>

### <span data-ttu-id="ed2c5-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ed2c5-112">Example 2</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngineRuleObject -Name rules1 -Priority -1
New-AzFrontDoorRulesEngineRuleObject : Cannot validate argument on parameter 'Priority'. The -1 argument is less than the minimum allowed range of 0. Supply an argument that is greater than or equal to 0 and then try the command again.
At line:1 char:81
+ ... ule1 = New-AzFrontDoorRulesEngineRuleObject -Name rules1 -Priority -1
+                                                                        ~~
+ CategoryInfo          : InvalidData: (:) [New-AzFrontDoorRulesEngineRuleObject], ParameterBindingValidationException
+ FullyQualifiedErrorId : ParameterArgumentValidationError,Microsoft.Azure.Commands.FrontDoor.Cmdlets.NewFrontDoorRulesEngineRuleObject
```

<span data-ttu-id="ed2c5-113">Oczekiwanie danych wyjściowych podczas przechodzenia do nieprawidłowej wartości priorytetu.</span><span class="sxs-lookup"><span data-stu-id="ed2c5-113">Expect output when passing in invalid priority value.</span></span>

## <span data-ttu-id="ed2c5-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ed2c5-114">PARAMETERS</span></span>

### <span data-ttu-id="ed2c5-115">-Action</span><span class="sxs-lookup"><span data-stu-id="ed2c5-115">-Action</span></span>
<span data-ttu-id="ed2c5-116">Akcje, które należy wykonać na żądanie i odpowiedź, jeśli wszystkie warunki zgodności zostaną spełnione.</span><span class="sxs-lookup"><span data-stu-id="ed2c5-116">Actions to perform on the request and response if all of the match conditions are met.</span></span>

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

### <span data-ttu-id="ed2c5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed2c5-117">-DefaultProfile</span></span>
<span data-ttu-id="ed2c5-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ed2c5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed2c5-119">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="ed2c5-119">-MatchCondition</span></span>
<span data-ttu-id="ed2c5-120">Lista warunków zgodności, które muszą zostać spełnione w celu uruchomienia akcji tej reguły.</span><span class="sxs-lookup"><span data-stu-id="ed2c5-120">A list of match conditions that must meet in order for the actions of this rule to run.</span></span> <span data-ttu-id="ed2c5-121">Brak zgodnych warunków oznacza, że akcje będą zawsze uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ed2c5-121">Having no match conditions means the actions will always run.</span></span>

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

### <span data-ttu-id="ed2c5-122">-MatchProcessingBehavior</span><span class="sxs-lookup"><span data-stu-id="ed2c5-122">-MatchProcessingBehavior</span></span>
<span data-ttu-id="ed2c5-123">Jeśli ta reguła jest zgodna, jeśli aparat reguł nadal uruchamia pozostałe reguły lub Zatrzymaj.</span><span class="sxs-lookup"><span data-stu-id="ed2c5-123">If this rule is a match should the rules engine continue running the remaining rules or stop.</span></span>
<span data-ttu-id="ed2c5-124">Możliwe wartości są kontynuowane i zatrzymane.</span><span class="sxs-lookup"><span data-stu-id="ed2c5-124">Possible values are Continue and Stop.</span></span>
<span data-ttu-id="ed2c5-125">Jeśli nie jest obecny, domyślnie jest to kontynuacja.</span><span class="sxs-lookup"><span data-stu-id="ed2c5-125">If not present, defaults to Continue.</span></span>

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

### <span data-ttu-id="ed2c5-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ed2c5-126">-Name</span></span>
<span data-ttu-id="ed2c5-127">Nazwa odwołująca się do tej konkretnej reguły.</span><span class="sxs-lookup"><span data-stu-id="ed2c5-127">A name to refer to this specific rule.</span></span>

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

### <span data-ttu-id="ed2c5-128">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="ed2c5-128">-Priority</span></span>
<span data-ttu-id="ed2c5-129">Priorytet przypisany do tej reguły.</span><span class="sxs-lookup"><span data-stu-id="ed2c5-129">A priority assigned to this rule.</span></span>
<span data-ttu-id="ed2c5-130">Nie mogą być ujemne.</span><span class="sxs-lookup"><span data-stu-id="ed2c5-130">Cannot be negative.</span></span>

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

### <span data-ttu-id="ed2c5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed2c5-131">CommonParameters</span></span>
<span data-ttu-id="ed2c5-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed2c5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed2c5-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed2c5-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed2c5-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed2c5-134">INPUTS</span></span>

### <span data-ttu-id="ed2c5-135">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ed2c5-135">None</span></span>

## <span data-ttu-id="ed2c5-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ed2c5-136">OUTPUTS</span></span>

### <span data-ttu-id="ed2c5-137">Microsoft. Azure. Commands. FrontDoor. models. PSRulesEngineRule</span><span class="sxs-lookup"><span data-stu-id="ed2c5-137">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineRule</span></span>

## <span data-ttu-id="ed2c5-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ed2c5-138">NOTES</span></span>

## <span data-ttu-id="ed2c5-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ed2c5-139">RELATED LINKS</span></span>
