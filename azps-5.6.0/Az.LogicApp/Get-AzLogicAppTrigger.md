---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 5307F1F1-E84C-4949-A557-99EF0012C3DF
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azlogicapptrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTrigger.md
ms.openlocfilehash: 28a7cd76f03dd3b6d2fc79e5d0b8d4d963a7f55c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008929"
---
# <span data-ttu-id="3cc3b-101">Get-AzLogicAppTrigger</span><span class="sxs-lookup"><span data-stu-id="3cc3b-101">Get-AzLogicAppTrigger</span></span>

## <span data-ttu-id="3cc3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cc3b-102">SYNOPSIS</span></span>
<span data-ttu-id="3cc3b-103">Pobiera wyzwalacze aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="3cc3b-103">Gets the triggers of a logic app.</span></span>

## <span data-ttu-id="3cc3b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3cc3b-104">SYNTAX</span></span>

```
Get-AzLogicAppTrigger -ResourceGroupName <String> -Name <String> [-TriggerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3cc3b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="3cc3b-105">DESCRIPTION</span></span>
<span data-ttu-id="3cc3b-106">Polecenie **cmdlet Get-AzLogicAppTrigger** pobiera wyzwalacze z aplikacji logiki.</span><span class="sxs-lookup"><span data-stu-id="3cc3b-106">The **Get-AzLogicAppTrigger** cmdlet gets triggers from a logic app.</span></span>
<span data-ttu-id="3cc3b-107">To polecenie cmdlet zwraca obiekt **WorkflowTrigger.**</span><span class="sxs-lookup"><span data-stu-id="3cc3b-107">This cmdlet returns a **WorkflowTrigger** object.</span></span>
<span data-ttu-id="3cc3b-108">Określanie przepływu pracy, grupy zasobów i wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="3cc3b-108">Specify the workflow, resource group, and trigger.</span></span>
<span data-ttu-id="3cc3b-109">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="3cc3b-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="3cc3b-110">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="3cc3b-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="3cc3b-111">Aby wykryć nazwy parametrów dynamicznych, wpisz łącznik (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić przez dostępne parametry.</span><span class="sxs-lookup"><span data-stu-id="3cc3b-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="3cc3b-112">Jeśli pominiesz wymagany parametr szablonu, polecenie cmdlet wyświetli monit o wartość.</span><span class="sxs-lookup"><span data-stu-id="3cc3b-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="3cc3b-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3cc3b-113">EXAMPLES</span></span>

### <span data-ttu-id="3cc3b-114">Przykład 1. Uzyskiwanie wyzwalacza aplikacji logiki</span><span class="sxs-lookup"><span data-stu-id="3cc3b-114">Example 1: Get a trigger of a logic app</span></span>
```
PS C:\>Get-AzLogicAppTrigger -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -TriggerName "Trigger01"
ChangedTime         : 1/14/2016 11:45:07 AM
CreatedTime         : 1/13/2016 2:42:26 PM
LastExecutionTime   : 1/14/2016 11:45:07 AM
Name                : Trigger01
NextExecutionTime   : 1/14/2016 12:45:07 PM
RecurrenceFrequency : Minute
RecurrenceInterval  : 60
Status              : Waiting
Type                : Microsoft.Logic/workflows/triggers
LogicAppName        : LogicApp05
LogicAppVersion     : 08587489107406290826
```

<span data-ttu-id="3cc3b-115">To polecenie pobiera wyzwalacz o nazwie Trigger01 z aplikacji logiki o nazwie LogicApp05.</span><span class="sxs-lookup"><span data-stu-id="3cc3b-115">This command gets the trigger named Trigger01 from the logic app named LogicApp05.</span></span>

### <span data-ttu-id="3cc3b-116">Przykład 2. Uzyskiwanie wszystkich wyzwalaczy aplikacji logiki</span><span class="sxs-lookup"><span data-stu-id="3cc3b-116">Example 2: Get all triggers of a logic app</span></span>
```
PS C:\>Get-AzLogicAppTrigger -ResourceGroupName "ResourceGroup11" -Name "LogicApp07"
ChangedTime         : 1/14/2016 11:45:07 AM
CreatedTime         : 1/13/2016 2:42:26 PM
LastExecutionTime   : 1/14/2016 11:45:07 AM
Name                : Trigger02
NextExecutionTime   : 1/14/2016 12:45:07 PM
RecurrenceFrequency : Minute
RecurrenceInterval  : 60
Status              : Waiting
Type                : Microsoft.Logic/workflows/triggers
LogicAppName        : LogicApp07
LogicAppVersion     : 08587489107406290826
```

<span data-ttu-id="3cc3b-117">To polecenie pobiera wyzwalacze aplikacji logiki o nazwie LogicApp07.</span><span class="sxs-lookup"><span data-stu-id="3cc3b-117">This command gets the triggers of the logic app named LogicApp07.</span></span>

## <span data-ttu-id="3cc3b-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3cc3b-118">PARAMETERS</span></span>

### <span data-ttu-id="3cc3b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cc3b-119">-DefaultProfile</span></span>
<span data-ttu-id="3cc3b-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="3cc3b-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3cc3b-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3cc3b-121">-Name</span></span>
<span data-ttu-id="3cc3b-122">Określa nazwę aplikacji logiki, z której to polecenie cmdlet uzyskuje wyzwalacz.</span><span class="sxs-lookup"><span data-stu-id="3cc3b-122">Specifies the name of the logic app from which this cmdlet gets a trigger.</span></span>

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

### <span data-ttu-id="3cc3b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cc3b-123">-ResourceGroupName</span></span>
<span data-ttu-id="3cc3b-124">Określa nazwę grupy zasobów, w której to polecenie cmdlet uzyskuje wyzwalacz.</span><span class="sxs-lookup"><span data-stu-id="3cc3b-124">Specifies the name of a resource group in which this cmdlet gets a trigger.</span></span>

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

### <span data-ttu-id="3cc3b-125">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="3cc3b-125">-TriggerName</span></span>
<span data-ttu-id="3cc3b-126">Określa nazwę wyzwalacza, który otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cc3b-126">Specifies the name of the trigger that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3cc3b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cc3b-127">CommonParameters</span></span>
<span data-ttu-id="3cc3b-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cc3b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cc3b-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cc3b-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cc3b-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3cc3b-130">INPUTS</span></span>

### <span data-ttu-id="3cc3b-131">System.String</span><span class="sxs-lookup"><span data-stu-id="3cc3b-131">System.String</span></span>

## <span data-ttu-id="3cc3b-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3cc3b-132">OUTPUTS</span></span>

### <span data-ttu-id="3cc3b-133">Microsoft.Azure.Management.Logic.Models.WorkflowTrigger</span><span class="sxs-lookup"><span data-stu-id="3cc3b-133">Microsoft.Azure.Management.Logic.Models.WorkflowTrigger</span></span>

## <span data-ttu-id="3cc3b-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3cc3b-134">NOTES</span></span>

## <span data-ttu-id="3cc3b-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3cc3b-135">RELATED LINKS</span></span>

[<span data-ttu-id="3cc3b-136">Get-AzLogicAppTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="3cc3b-136">Get-AzLogicAppTriggerHistory</span></span>](./Get-AzLogicAppTriggerHistory.md)

[<span data-ttu-id="3cc3b-137">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="3cc3b-137">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


