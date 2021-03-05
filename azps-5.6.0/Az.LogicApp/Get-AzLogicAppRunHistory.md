---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F271BCB1-6D43-48E5-BB51-00288F57BFFB
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azlogicapprunhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
ms.openlocfilehash: 01bba193f763eff784bdd5f3f67118d84c6235a5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008945"
---
# <span data-ttu-id="64721-101">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="64721-101">Get-AzLogicAppRunHistory</span></span>

## <span data-ttu-id="64721-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64721-102">SYNOPSIS</span></span>

<span data-ttu-id="64721-103">Pobiera historię uruchamiania aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="64721-103">Gets the run history of a logic app.</span></span>

## <span data-ttu-id="64721-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="64721-104">SYNTAX</span></span>

```powershell
Get-AzLogicAppRunHistory -ResourceGroupName <String> -Name <String> [-RunName <String>] [-FollowNextPageLink]
 [-MaximumFollowNextPageLink <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64721-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="64721-105">DESCRIPTION</span></span>

<span data-ttu-id="64721-106">Polecenie **cmdlet Get-AzLogicAppRunHistory** pobiera historię uruchamiania aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="64721-106">The **Get-AzLogicAppRunHistory** cmdlet gets the run history of a logic app.</span></span>
<span data-ttu-id="64721-107">To polecenie cmdlet zwraca kolekcję **obiektów WorkflowRun.**</span><span class="sxs-lookup"><span data-stu-id="64721-107">This cmdlet returns a collection of **WorkflowRun** objects.</span></span>
<span data-ttu-id="64721-108">Określanie aplikacji logiki i grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="64721-108">Specify the logic app and resource group.</span></span>
<span data-ttu-id="64721-109">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="64721-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="64721-110">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="64721-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="64721-111">Aby wykryć nazwy parametrów dynamicznych, wpisz łącznik (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić przez dostępne parametry.</span><span class="sxs-lookup"><span data-stu-id="64721-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="64721-112">Jeśli pominiesz wymagany parametr szablonu, polecenie cmdlet wyświetli monit o wartość.</span><span class="sxs-lookup"><span data-stu-id="64721-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="64721-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="64721-113">EXAMPLES</span></span>

### <span data-ttu-id="64721-114">Przykład 1. Uzyskiwanie historii uruchamiania aplikacji logiki</span><span class="sxs-lookup"><span data-stu-id="64721-114">Example 1: Get the run history of a logic app</span></span>

```powershell
PS C:\>Get-AzLogicAppRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03"
CorrelationId    : 55830326-9042-404d-a4c3-fab198106a57
EndTime          : 1/13/2016 2:46:55 PM
Error            : {code, message}
Name             : 08587489104702792076
Outputs          : {}
StartTime        : 1/13/2016 2:46:55 PM
Status           : Failed
TriggerName      : 
LogicAppName     : LogicApp03
LogicAppVersion  : 08587489107859952540

CorrelationId    : d3ddc917-9aaa-47b3-8814-c621c2ae530b
EndTime          : 1/13/2016 2:42:56 PM
Error            : {code, message}
Name             : 08587489107100664541
Outputs          : {}
StartTime        : 1/13/2016 2:42:55 PM
Status           : Failed
TriggerName      : httpTrigger
LogicAppName     : LogicApp03
LogicAppVersion  : 08587489107859952120
```

<span data-ttu-id="64721-115">To polecenie pobiera historię uruchamiania aplikacji logiki o nazwie LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="64721-115">This command gets the run history of a logic app named LogicApp03.</span></span>

### <span data-ttu-id="64721-116">Przykład 2. Uruchamianie aplikacji logiki</span><span class="sxs-lookup"><span data-stu-id="64721-116">Example 2: Get a logic app run</span></span>

```powershell
PS C:\>Get-AzLogicAppRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03" -RunName "08587489104702792076"
CorrelationId    : 55830326-9042-404d-a4c3-fab198106a57
EndTime          : 1/13/2016 2:46:55 PM
Error            : {code, message}
Name             : 08587489104702792076
Outputs          : {}
StartTime        : 1/13/2016 2:46:55 PM
Status           : Failed
TriggerName      : 
LogicAppName     : LogicApp03
LogicAppVersion  : 08587489107859952120
```

<span data-ttu-id="64721-117">To polecenie pobiera uruchomienie określonej aplikacji logiki dla aplikacji logiki o nazwie LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="64721-117">This command gets a specific logic app run for the logic app named LogicApp03.</span></span>

### <span data-ttu-id="64721-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="64721-118">Example 3</span></span>

```powershell
Get-AzLogicAppRunHistory -Name 'LogicApp03' -ResourceGroupName MyResourceGroup -FollowNextPageLink
```

<span data-ttu-id="64721-119">To polecenie pobiera całą historię uruchamiania aplikacji logiki o nazwie LogicApp03, korzystając z polecenia NextPageLink.</span><span class="sxs-lookup"><span data-stu-id="64721-119">This command gets the entire run history of a logic app named LogicApp03 by following the NextPageLink.</span></span>

### <span data-ttu-id="64721-120">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="64721-120">Example 4</span></span>

```powershell
Get-AzLogicAppRunHistory -Name 'LogicApp03' -ResourceGroupName MyResourceGroup -FollowNextPageLink -MaximumFollowNextPageLink 1
```

<span data-ttu-id="64721-121">To polecenie pobiera dwie pierwsze strony historii uruchamiania aplikacji logiki o nazwie LogicApp03, korzystając z łącza NextPageLink i ograniczając rozmiar wyników do dwóch stron.</span><span class="sxs-lookup"><span data-stu-id="64721-121">This command gets the first two pages of run history of a logic app named LogicApp03 by following the NextPageLink and limiting the result size to two pages.</span></span>
<span data-ttu-id="64721-122">Każda strona zawiera 30 wyników.</span><span class="sxs-lookup"><span data-stu-id="64721-122">Each page contains thirty results.</span></span>

## <span data-ttu-id="64721-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64721-123">PARAMETERS</span></span>

### <span data-ttu-id="64721-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64721-124">-DefaultProfile</span></span>

<span data-ttu-id="64721-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="64721-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="64721-126">-FollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="64721-126">-FollowNextPageLink</span></span>

<span data-ttu-id="64721-127">Wskazuje, że polecenie cmdlet powinno postępować zgodnie z linkami do następnej strony.</span><span class="sxs-lookup"><span data-stu-id="64721-127">Indicates the cmdlet should follow next page links.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: FL

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64721-128">-MaximumFollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="64721-128">-MaximumFollowNextPageLink</span></span>

<span data-ttu-id="64721-129">Określa, ile razy mają być używane łącza następnej strony, jeśli jest używana opcja FollowNextPageLink.</span><span class="sxs-lookup"><span data-stu-id="64721-129">Specifies how many times to follow next page links if FollowNextPageLink is used.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: ML

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64721-130">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="64721-130">-Name</span></span>

<span data-ttu-id="64721-131">Określa nazwę aplikacji logiki, dla której to polecenie cmdlet pobiera historię uruchamiania.</span><span class="sxs-lookup"><span data-stu-id="64721-131">Specifies the name of the logic app for which this cmdlet gets run history.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64721-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64721-132">-ResourceGroupName</span></span>

<span data-ttu-id="64721-133">Określa nazwę grupy zasobów zawierającej aplikację logiki.</span><span class="sxs-lookup"><span data-stu-id="64721-133">Specifies the name of a resource group that contains the logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64721-134">-RunName</span><span class="sxs-lookup"><span data-stu-id="64721-134">-RunName</span></span>

<span data-ttu-id="64721-135">Określa nazwę uruchomienia aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="64721-135">Specifies the run name of a logic app.</span></span>
<span data-ttu-id="64721-136">To polecenie cmdlet pobiera uruchomienie przepływu pracy, które określa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64721-136">This cmdlet gets the workflow run that this cmdlet specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64721-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64721-137">CommonParameters</span></span>

<span data-ttu-id="64721-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64721-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64721-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="64721-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64721-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64721-140">INPUTS</span></span>

### <span data-ttu-id="64721-141">System.String</span><span class="sxs-lookup"><span data-stu-id="64721-141">System.String</span></span>

## <span data-ttu-id="64721-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64721-142">OUTPUTS</span></span>

### <span data-ttu-id="64721-143">Microsoft.Azure.Management.Logic.Models.WorkflowRun</span><span class="sxs-lookup"><span data-stu-id="64721-143">Microsoft.Azure.Management.Logic.Models.WorkflowRun</span></span>

## <span data-ttu-id="64721-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="64721-144">NOTES</span></span>

## <span data-ttu-id="64721-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="64721-145">RELATED LINKS</span></span>

[<span data-ttu-id="64721-146">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="64721-146">Get-AzLogicAppRunAction</span></span>](./Get-AzLogicAppRunAction.md)

[<span data-ttu-id="64721-147">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="64721-147">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)

[<span data-ttu-id="64721-148">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="64721-148">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)
