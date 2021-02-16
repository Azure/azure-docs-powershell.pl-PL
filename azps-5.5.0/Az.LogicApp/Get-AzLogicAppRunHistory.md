---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F271BCB1-6D43-48E5-BB51-00288F57BFFB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapprunhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
ms.openlocfilehash: 855cab84e4ab9de2cd7afae2a25dbc867a192e96
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187619"
---
# <span data-ttu-id="35f78-101">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="35f78-101">Get-AzLogicAppRunHistory</span></span>

## <span data-ttu-id="35f78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35f78-102">SYNOPSIS</span></span>

<span data-ttu-id="35f78-103">Pobiera historię uruchamiania aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="35f78-103">Gets the run history of a logic app.</span></span>

## <span data-ttu-id="35f78-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="35f78-104">SYNTAX</span></span>

```powershell
Get-AzLogicAppRunHistory -ResourceGroupName <String> -Name <String> [-RunName <String>] [-FollowNextPageLink]
 [-MaximumFollowNextPageLink <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35f78-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="35f78-105">DESCRIPTION</span></span>

<span data-ttu-id="35f78-106">Polecenie **cmdlet Get-AzLogicAppRunHistory** pobiera historię uruchamiania aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="35f78-106">The **Get-AzLogicAppRunHistory** cmdlet gets the run history of a logic app.</span></span>
<span data-ttu-id="35f78-107">To polecenie cmdlet zwraca kolekcję **obiektów WorkflowRun.**</span><span class="sxs-lookup"><span data-stu-id="35f78-107">This cmdlet returns a collection of **WorkflowRun** objects.</span></span>
<span data-ttu-id="35f78-108">Określanie aplikacji logiki i grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="35f78-108">Specify the logic app and resource group.</span></span>
<span data-ttu-id="35f78-109">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="35f78-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="35f78-110">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="35f78-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="35f78-111">Aby wykryć nazwy parametrów dynamicznych, wpisz łącznik (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić przez dostępne parametry.</span><span class="sxs-lookup"><span data-stu-id="35f78-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="35f78-112">Jeśli pominiesz wymagany parametr szablonu, polecenie cmdlet wyświetli monit o wartość.</span><span class="sxs-lookup"><span data-stu-id="35f78-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="35f78-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="35f78-113">EXAMPLES</span></span>

### <span data-ttu-id="35f78-114">Przykład 1. Uzyskiwanie historii uruchamiania aplikacji logiki</span><span class="sxs-lookup"><span data-stu-id="35f78-114">Example 1: Get the run history of a logic app</span></span>

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

<span data-ttu-id="35f78-115">To polecenie pobiera historię uruchamiania aplikacji logiki o nazwie LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="35f78-115">This command gets the run history of a logic app named LogicApp03.</span></span>

### <span data-ttu-id="35f78-116">Przykład 2. Uruchamianie aplikacji logiki</span><span class="sxs-lookup"><span data-stu-id="35f78-116">Example 2: Get a logic app run</span></span>

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

<span data-ttu-id="35f78-117">To polecenie pobiera uruchomienie określonej aplikacji logiki dla aplikacji logiki o nazwie LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="35f78-117">This command gets a specific logic app run for the logic app named LogicApp03.</span></span>

### <span data-ttu-id="35f78-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="35f78-118">Example 3</span></span>

```powershell
Get-AzLogicAppRunHistory -Name 'LogicApp03' -ResourceGroupName MyResourceGroup -FollowNextPageLink
```

<span data-ttu-id="35f78-119">To polecenie pobiera całą historię uruchamiania aplikacji logiki o nazwie LogicApp03, korzystając z polecenia NextPageLink.</span><span class="sxs-lookup"><span data-stu-id="35f78-119">This command gets the entire run history of a logic app named LogicApp03 by following the NextPageLink.</span></span>

### <span data-ttu-id="35f78-120">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="35f78-120">Example 4</span></span>

```powershell
Get-AzLogicAppRunHistory -Name 'LogicApp03' -ResourceGroupName MyResourceGroup -FollowNextPageLink -MaximumFollowNextPageLink 1
```

<span data-ttu-id="35f78-121">To polecenie pobiera dwie pierwsze strony historii uruchamiania aplikacji logiki o nazwie LogicApp03, korzystając z łącza NextPageLink i ograniczając rozmiar wyników do dwóch stron.</span><span class="sxs-lookup"><span data-stu-id="35f78-121">This command gets the first two pages of run history of a logic app named LogicApp03 by following the NextPageLink and limiting the result size to two pages.</span></span>
<span data-ttu-id="35f78-122">Każda strona zawiera 30 wyników.</span><span class="sxs-lookup"><span data-stu-id="35f78-122">Each page contains thirty results.</span></span>

## <span data-ttu-id="35f78-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35f78-123">PARAMETERS</span></span>

### <span data-ttu-id="35f78-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35f78-124">-DefaultProfile</span></span>

<span data-ttu-id="35f78-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="35f78-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35f78-126">-FollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="35f78-126">-FollowNextPageLink</span></span>

<span data-ttu-id="35f78-127">Wskazuje, że polecenie cmdlet powinno być zgodne z linkami do następnej strony.</span><span class="sxs-lookup"><span data-stu-id="35f78-127">Indicates the cmdlet should follow next page links.</span></span>

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

### <span data-ttu-id="35f78-128">-MaximumFollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="35f78-128">-MaximumFollowNextPageLink</span></span>

<span data-ttu-id="35f78-129">Określa, ile razy mają być używane łącza następnej strony, jeśli jest używana opcja FollowNextPageLink.</span><span class="sxs-lookup"><span data-stu-id="35f78-129">Specifies how many times to follow next page links if FollowNextPageLink is used.</span></span>

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

### <span data-ttu-id="35f78-130">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="35f78-130">-Name</span></span>

<span data-ttu-id="35f78-131">Określa nazwę aplikacji logiki, dla której to polecenie cmdlet pobiera historię uruchamiania.</span><span class="sxs-lookup"><span data-stu-id="35f78-131">Specifies the name of the logic app for which this cmdlet gets run history.</span></span>

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

### <span data-ttu-id="35f78-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35f78-132">-ResourceGroupName</span></span>

<span data-ttu-id="35f78-133">Określa nazwę grupy zasobów zawierającej aplikację logiki.</span><span class="sxs-lookup"><span data-stu-id="35f78-133">Specifies the name of a resource group that contains the logic app.</span></span>

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

### <span data-ttu-id="35f78-134">-RunName</span><span class="sxs-lookup"><span data-stu-id="35f78-134">-RunName</span></span>

<span data-ttu-id="35f78-135">Określa nazwę uruchomienia aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="35f78-135">Specifies the run name of a logic app.</span></span>
<span data-ttu-id="35f78-136">To polecenie cmdlet pobiera uruchomienie przepływu pracy, które określa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35f78-136">This cmdlet gets the workflow run that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="35f78-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35f78-137">CommonParameters</span></span>

<span data-ttu-id="35f78-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35f78-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35f78-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="35f78-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35f78-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="35f78-140">INPUTS</span></span>

### <span data-ttu-id="35f78-141">System.String</span><span class="sxs-lookup"><span data-stu-id="35f78-141">System.String</span></span>

## <span data-ttu-id="35f78-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="35f78-142">OUTPUTS</span></span>

### <span data-ttu-id="35f78-143">Microsoft.Azure.Management.Logic.Models.WorkflowRun</span><span class="sxs-lookup"><span data-stu-id="35f78-143">Microsoft.Azure.Management.Logic.Models.WorkflowRun</span></span>

## <span data-ttu-id="35f78-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="35f78-144">NOTES</span></span>

## <span data-ttu-id="35f78-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="35f78-145">RELATED LINKS</span></span>

[<span data-ttu-id="35f78-146">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="35f78-146">Get-AzLogicAppRunAction</span></span>](./Get-AzLogicAppRunAction.md)

[<span data-ttu-id="35f78-147">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="35f78-147">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)

[<span data-ttu-id="35f78-148">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="35f78-148">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)
