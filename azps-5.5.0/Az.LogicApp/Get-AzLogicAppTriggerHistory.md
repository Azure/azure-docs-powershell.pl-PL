---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: C1F6BBF9-0DB5-46FD-B8A8-9029B0AB6166
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapptriggerhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerHistory.md
ms.openlocfilehash: 33102de45a929db4016b7e9cf523f0395f335875
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194235"
---
# <span data-ttu-id="23e51-101">Get-AzLogicAppTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="23e51-101">Get-AzLogicAppTriggerHistory</span></span>

## <span data-ttu-id="23e51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23e51-102">SYNOPSIS</span></span>

<span data-ttu-id="23e51-103">Pobiera historię wyzwalaczy w aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="23e51-103">Gets the history of triggers in a logic app.</span></span>

## <span data-ttu-id="23e51-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="23e51-104">SYNTAX</span></span>

```powershell
Get-AzLogicAppTriggerHistory -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-HistoryName <String>] [-FollowNextPageLink] [-MaximumFollowNextPageLink <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23e51-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="23e51-105">DESCRIPTION</span></span>

<span data-ttu-id="23e51-106">Polecenie **cmdlet Get-AzLogicAppTriggerHistory** pobiera historię wyzwalaczy w aplikacji logiki w funkcji aplikacje logiki.</span><span class="sxs-lookup"><span data-stu-id="23e51-106">The **Get-AzLogicAppTriggerHistory** cmdlet gets the history of triggers in a logic app in the Logic Apps feature.</span></span>
<span data-ttu-id="23e51-107">To polecenie cmdlet zwraca obiekt **WorkflowTriggerHistory.**</span><span class="sxs-lookup"><span data-stu-id="23e51-107">This cmdlet returns a **WorkflowTriggerHistory** object.</span></span>
<span data-ttu-id="23e51-108">Określanie aplikacji logiki, grupy zasobów i wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="23e51-108">Specify the logic app, resource group, and trigger.</span></span>
<span data-ttu-id="23e51-109">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="23e51-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="23e51-110">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="23e51-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="23e51-111">Aby wykryć nazwy parametrów dynamicznych, wpisz łącznik (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić przez dostępne parametry.</span><span class="sxs-lookup"><span data-stu-id="23e51-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="23e51-112">Jeśli pominiesz wymagany parametr szablonu, polecenie cmdlet wyświetli monit o wartość.</span><span class="sxs-lookup"><span data-stu-id="23e51-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="23e51-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="23e51-113">EXAMPLES</span></span>

### <span data-ttu-id="23e51-114">Przykład 1. Uzyskiwanie historii wyzwalacza aplikacji logiki</span><span class="sxs-lookup"><span data-stu-id="23e51-114">Example 1: Get a trigger history of a logic app</span></span>

```powershell
PS C:\>Get-AzLogicAppTriggerHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03" -TriggerName "Trigger01" -HistoryName "08587489107387695768"
Code        : BadRequest
EndTime     : 1/13/2016 2:42:26 PM
Error       : {code, message}
Fired       : False
InputsLink  : https://flowprodcu02by01.blob.core.windows.net/flow3ea9ffd11c684c9f9f258b1a6ea5cb6020160113t000000zcontent/A7392_d1e831de68ac4ef89d19a40f05e663
              cb_httpTrigger:5Finputs:2Ejson?sv=2014-02-14&sr=b&sig=&se=2016-01-14T16%3A15%3A16Z&sp=r
Name        : 08587489107387695768
OutputsLink : 
Run         : 
StartTime   : 1/13/2016 2:42:26 PM
Status      : Failed
TrackingId  : f88a499b-f80f-4a28-9bbf-c4cc0d129700
Type        : Microsoft.Logic/workflows/triggers/histories
```

<span data-ttu-id="23e51-115">To polecenie pobiera określoną historię wyzwalacza aplikacji logiki dla wyzwalacza w aplikacji logiki o nazwie LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="23e51-115">This command gets a specific logic app trigger history for a trigger in the logic app named LogicApp03.</span></span>

### <span data-ttu-id="23e51-116">Przykład 2. Uzyskiwanie historii wyzwalaczy aplikacji logiki</span><span class="sxs-lookup"><span data-stu-id="23e51-116">Example 2: Get trigger histories of a logic app</span></span>

```powershell
PS C:\>Get-AzLogicAppTriggerHistory -ResourceGroupName "ResourceGroup11" -Name "LogicApp07" -TriggerName "Trigger01"
Code        : BadRequest
EndTime     : 1/13/2016 2:43:33 PM
Error       : {code, message}
Fired       : False
InputsLink  : https://flowprodcu02by01.blob.core.windows.net/flow3ea9ffd11c684c9f9f258b1a6ea5cb6020160113t000000zcontent/CAB46_60e2ad0f0e1947e8b5798716914c5d
              b6_httpTrigger:5Finputs:2Ejson?sv=2014-02-14&sr=b&sig=&se=2016-01-14T16%3A18%3A27Z&sp=r
Name        : 08587489106716457817
OutputsLink : 
Run         : 
StartTime   : 1/13/2016 2:43:33 PM
Status      : Failed
TrackingId  : c91a63f1-48b4-4eae-91eb-8f6dbfa9fe06
Type        : Microsoft.Logic/workflows/triggers/histories

Code        : BadRequest
EndTime     : 1/13/2016 2:42:26 PM
Error       : {code, message}
Fired       : False
InputsLink  : https://flowprodcu02by01.blob.core.windows.net/flow3ea9ffd11c684c9f9f258b1a6ea5cb6020160113t000000zcontent/A7392_d1e831de68ac4ef89d19a40f05e663
              cb_httpTrigger:5Finputs:2Ejson?sv=2014-02-14&sr=b&sig=&se=2016-01-14T16%3A18%3A27Z&sp=r
Name        : 08587489107387695768
OutputsLink : 
Run         : 
StartTime   : 1/13/2016 2:42:26 PM
Status      : Failed
TrackingId  : f88a499b-f80f-4a28-9bbf-c4cc0d129700
Type        : Microsoft.Logic/workflows/triggers/histories
```

<span data-ttu-id="23e51-117">To polecenie pobiera historie wyzwalacza przepływu pracy dla wyzwalacza w aplikacji logiki o nazwie LogicApp07.</span><span class="sxs-lookup"><span data-stu-id="23e51-117">This command gets the workflow trigger histories for a trigger in the logic app named LogicApp07.</span></span>

### <span data-ttu-id="23e51-118">Przykład 3. Uzyskiwanie całej historii wyzwalacza aplikacji logiki</span><span class="sxs-lookup"><span data-stu-id="23e51-118">Example 3: Get entire trigger history of a logic app</span></span>

```powershell
PS C:\>Get-AzLogicAppTriggerHistory -ResourceGroupName "ResourceGroup11" -Name "LogicApp08" -TriggerName "Trigger01" -FollowNextPageLink
```

<span data-ttu-id="23e51-119">To polecenie pobiera całą historię wyzwalacza przepływu pracy dla wyzwalacza w aplikacji logiki o nazwie LogicApp08, korzystając z polecenia NextPageLink.</span><span class="sxs-lookup"><span data-stu-id="23e51-119">This command gets the entire workflow trigger history for a trigger in the logic app named LogicApp08 by following the NextPageLink.</span></span>

### <span data-ttu-id="23e51-120">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="23e51-120">Example 4</span></span>

```powershell
PS C:\>Get-AzLogicAppTriggerHistory -ResourceGroupName "ResourceGroup11" -Name "LogicApp08" -TriggerName "Trigger01" -FollowNextPageLink -MaximumFollowNextPageLink 1
```

<span data-ttu-id="23e51-121">To polecenie pobiera dwie pierwsze strony historii wyzwalacza przepływu pracy dla wyzwalacza w aplikacji logiki o nazwie LogicApp09, korzystając z łącza NextPageLink i ograniczając rozmiar wyniku do dwóch stron.</span><span class="sxs-lookup"><span data-stu-id="23e51-121">This command gets the first two pages of workflow trigger history for a trigger in the logic app named LogicApp09 by following the NextPageLink and limiting the result size to two pages.</span></span>
<span data-ttu-id="23e51-122">Każda strona zawiera 30 wyników.</span><span class="sxs-lookup"><span data-stu-id="23e51-122">Each page contains thirty results.</span></span>

## <span data-ttu-id="23e51-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23e51-123">PARAMETERS</span></span>

### <span data-ttu-id="23e51-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23e51-124">-DefaultProfile</span></span>

<span data-ttu-id="23e51-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="23e51-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23e51-126">-FollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="23e51-126">-FollowNextPageLink</span></span>

<span data-ttu-id="23e51-127">Wskazuje, że polecenie cmdlet powinno postępować zgodnie z linkami do następnej strony.</span><span class="sxs-lookup"><span data-stu-id="23e51-127">Indicates the cmdlet should follow next page links.</span></span>

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

### <span data-ttu-id="23e51-128">-HistoryName</span><span class="sxs-lookup"><span data-stu-id="23e51-128">-HistoryName</span></span>

<span data-ttu-id="23e51-129">Określa nazwę historii, która pobiera to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23e51-129">Specifies the name of the history that this cmdlet gets.</span></span>

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

### <span data-ttu-id="23e51-130">-MaximumFollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="23e51-130">-MaximumFollowNextPageLink</span></span>

<span data-ttu-id="23e51-131">Określa, ile razy mają być używane łącza następnej strony, jeśli jest używana opcja FollowNextPageLink.</span><span class="sxs-lookup"><span data-stu-id="23e51-131">Specifies how many times to follow next page links if FollowNextPageLink is used.</span></span>

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

### <span data-ttu-id="23e51-132">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="23e51-132">-Name</span></span>

<span data-ttu-id="23e51-133">Określa nazwę aplikacji logiki, dla której to polecenie cmdlet pobiera historię wyzwalaczy.</span><span class="sxs-lookup"><span data-stu-id="23e51-133">Specifies the name of the logic app for which this cmdlet gets trigger history.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23e51-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23e51-134">-ResourceGroupName</span></span>

<span data-ttu-id="23e51-135">Określa nazwę grupy zasobów, w której to polecenie cmdlet pobiera historię.</span><span class="sxs-lookup"><span data-stu-id="23e51-135">Specifies the name of the resource group in which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="23e51-136">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="23e51-136">-TriggerName</span></span>

<span data-ttu-id="23e51-137">Określa nazwę wyzwalacza, dla którego to polecenie cmdlet pobiera historię.</span><span class="sxs-lookup"><span data-stu-id="23e51-137">Specifies the name of the trigger for which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="23e51-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23e51-138">CommonParameters</span></span>

<span data-ttu-id="23e51-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23e51-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23e51-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="23e51-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23e51-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23e51-141">INPUTS</span></span>

### <span data-ttu-id="23e51-142">System.String</span><span class="sxs-lookup"><span data-stu-id="23e51-142">System.String</span></span>

## <span data-ttu-id="23e51-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23e51-143">OUTPUTS</span></span>

### <span data-ttu-id="23e51-144">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="23e51-144">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerHistory</span></span>

## <span data-ttu-id="23e51-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="23e51-145">NOTES</span></span>

## <span data-ttu-id="23e51-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="23e51-146">RELATED LINKS</span></span>

[<span data-ttu-id="23e51-147">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="23e51-147">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="23e51-148">Get-AzLogicAppTrigger</span><span class="sxs-lookup"><span data-stu-id="23e51-148">Get-AzLogicAppTrigger</span></span>](./Get-AzLogicAppTrigger.md)

[<span data-ttu-id="23e51-149">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="23e51-149">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)
