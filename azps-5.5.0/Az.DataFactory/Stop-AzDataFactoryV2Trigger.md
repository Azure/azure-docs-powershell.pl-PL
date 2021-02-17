---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 80e9ed345b9d1b80dd75be2036826559ac3bbb9a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177138"
---
# <span data-ttu-id="2b8f5-101">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="2b8f5-101">Stop-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="2b8f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b8f5-102">SYNOPSIS</span></span>
<span data-ttu-id="2b8f5-103">Powoduje zatrzymanie wyzwalacza w zakładzie danych.</span><span class="sxs-lookup"><span data-stu-id="2b8f5-103">Stops a trigger in a data factory.</span></span>

## <span data-ttu-id="2b8f5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2b8f5-104">SYNTAX</span></span>

### <span data-ttu-id="2b8f5-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="2b8f5-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b8f5-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2b8f5-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b8f5-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2b8f5-107">ByResourceId</span></span>
```
Stop-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b8f5-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="2b8f5-108">DESCRIPTION</span></span>
<span data-ttu-id="2b8f5-109">Polecenie **cmdlet Stop-AzDataFactoryV2Trigger** powoduje zatrzymanie wyzwalacza w fabrycznej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="2b8f5-109">The **Stop-AzDataFactoryV2Trigger** cmdlet stops a trigger in a data factory.</span></span> <span data-ttu-id="2b8f5-110">Jeśli wyzwalacz znajduje się w stanie "Uruchomiona", polecenie cmdlet zatrzyma wyzwalacz i nie będzie już wywoływać potoków.</span><span class="sxs-lookup"><span data-stu-id="2b8f5-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="2b8f5-111">Jeśli wyzwalacz znajduje się już w stanie "Zatrzymano", to polecenie cmdlet nie ma wpływu.</span><span class="sxs-lookup"><span data-stu-id="2b8f5-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span> <span data-ttu-id="2b8f5-112">Jeśli parametr Force jest określony, polecenie cmdlet nie wyświetla monitu przed zatrzymaniem wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="2b8f5-112">If the Force parameter is specified, the cmdlet doesn't prompt before stopping the trigger.</span></span>

## <span data-ttu-id="2b8f5-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2b8f5-113">EXAMPLES</span></span>

### <span data-ttu-id="2b8f5-114">Przykład 1. Zatrzymanie wyzwalacza</span><span class="sxs-lookup"><span data-stu-id="2b8f5-114">Example 1: Stop a trigger</span></span>
```
Stop-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to stop trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="2b8f5-115">Powoduje zatrzymanie wyzwalacza o nazwie "ScheduledTrigger" w zakładzie danych "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="2b8f5-115">Stops a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="2b8f5-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2b8f5-116">PARAMETERS</span></span>

### <span data-ttu-id="2b8f5-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="2b8f5-117">-DataFactoryName</span></span>
<span data-ttu-id="2b8f5-118">Nazwa fabryczna danych.</span><span class="sxs-lookup"><span data-stu-id="2b8f5-118">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b8f5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b8f5-119">-DefaultProfile</span></span>
<span data-ttu-id="2b8f5-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2b8f5-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b8f5-121">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="2b8f5-121">-Force</span></span>
<span data-ttu-id="2b8f5-122">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2b8f5-122">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b8f5-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b8f5-123">-InputObject</span></span>
<span data-ttu-id="2b8f5-124">Wyzwalanie obiektu do uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="2b8f5-124">Trigger object to start.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b8f5-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2b8f5-125">-Name</span></span>
<span data-ttu-id="2b8f5-126">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="2b8f5-126">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b8f5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b8f5-127">-ResourceGroupName</span></span>
<span data-ttu-id="2b8f5-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2b8f5-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b8f5-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b8f5-129">-ResourceId</span></span>
<span data-ttu-id="2b8f5-130">Identyfikator zasobu Azure.</span><span class="sxs-lookup"><span data-stu-id="2b8f5-130">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b8f5-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2b8f5-131">-Confirm</span></span>
<span data-ttu-id="2b8f5-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2b8f5-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b8f5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b8f5-133">-WhatIf</span></span>
<span data-ttu-id="2b8f5-134">Pokazuje, co się stanie, jeśli polecenie cmdlet zostanie uruchomione, ale nie uruchomi polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b8f5-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b8f5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b8f5-135">CommonParameters</span></span>
<span data-ttu-id="2b8f5-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b8f5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b8f5-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b8f5-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b8f5-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2b8f5-138">INPUTS</span></span>

### <span data-ttu-id="2b8f5-139">System.String</span><span class="sxs-lookup"><span data-stu-id="2b8f5-139">System.String</span></span>

### <span data-ttu-id="2b8f5-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="2b8f5-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="2b8f5-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2b8f5-141">OUTPUTS</span></span>

### <span data-ttu-id="2b8f5-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="2b8f5-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="2b8f5-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2b8f5-143">NOTES</span></span>

## <span data-ttu-id="2b8f5-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2b8f5-144">RELATED LINKS</span></span>

[<span data-ttu-id="2b8f5-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="2b8f5-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="2b8f5-146">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="2b8f5-146">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="2b8f5-147">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="2b8f5-147">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="2b8f5-148">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="2b8f5-148">Remove-AzDataFactoryV2Trigger</span></span>]()
