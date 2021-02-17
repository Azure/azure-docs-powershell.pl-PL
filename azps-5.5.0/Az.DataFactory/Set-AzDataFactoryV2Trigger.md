---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Trigger.md
ms.openlocfilehash: cb0d548e1fcbc7acecf1ae1457eb762d4cf81645
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186243"
---
# <span data-ttu-id="5ff10-101">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5ff10-101">Set-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="5ff10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ff10-102">SYNOPSIS</span></span>
<span data-ttu-id="5ff10-103">Tworzy wyzwalacz w zakładzie danych.</span><span class="sxs-lookup"><span data-stu-id="5ff10-103">Creates a trigger in a data factory.</span></span>

## <span data-ttu-id="5ff10-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5ff10-104">SYNTAX</span></span>

### <span data-ttu-id="5ff10-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="5ff10-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Trigger [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ff10-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5ff10-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Trigger [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ff10-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="5ff10-107">DESCRIPTION</span></span>
<span data-ttu-id="5ff10-108">Polecenie **cmdlet Set-AzDataFactoryV2Trigger** tworzy wyzwalacz w fabrycznej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="5ff10-108">The **Set-AzDataFactoryV2Trigger** cmdlet creates a trigger in a data factory.</span></span> <span data-ttu-id="5ff10-109">Jeśli określisz nazwę wyzwalacza, który już istnieje, polecenie cmdlet wyświetli monit o potwierdzenie przed zastąpieniem wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="5ff10-109">If you specify a name for a trigger that already exists, the cmdlet prompts for confirmation before replacing the trigger.</span></span> <span data-ttu-id="5ff10-110">W przypadku określenia _parametru Force_ polecenie cmdlet zastępuje istniejący wyzwalacz bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5ff10-110">If you specify the _Force_ parameter, the cmdlet replaces the existing trigger without prompting for confirmation.</span></span> <span data-ttu-id="5ff10-111">Wyzwalacze są tworzone w stanie "Zatrzymano", co oznacza, że nie rozpoczynają od razu wywoływania potoków, do których się odwołują.</span><span class="sxs-lookup"><span data-stu-id="5ff10-111">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="5ff10-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5ff10-112">EXAMPLES</span></span>

### <span data-ttu-id="5ff10-113">Przykład 1. Tworzenie wyzwalacza</span><span class="sxs-lookup"><span data-stu-id="5ff10-113">Example 1: Create a trigger</span></span>
```
PS C:\> Set-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger" -DefinitionFile ".\scheduledTrigger.json"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="5ff10-114">Utwórz nowy wyzwalacz o nazwie "ScheduledTrigger" w fabrycznej układzie danych "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="5ff10-114">Create a new trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span> <span data-ttu-id="5ff10-115">Wyzwalacz zostanie utworzony w stanie "Zatrzymano", co oznacza, że nie uruchamia się od razu.</span><span class="sxs-lookup"><span data-stu-id="5ff10-115">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="5ff10-116">Wyzwalacz można rozpocząć przy użyciu `Start-AzDataFactoryV2Trigger` polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ff10-116">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="5ff10-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ff10-117">PARAMETERS</span></span>

### <span data-ttu-id="5ff10-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5ff10-118">-DataFactoryName</span></span>
<span data-ttu-id="5ff10-119">Nazwa fabryczna danych.</span><span class="sxs-lookup"><span data-stu-id="5ff10-119">The data factory name.</span></span>

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

### <span data-ttu-id="5ff10-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ff10-120">-DefaultProfile</span></span>
<span data-ttu-id="5ff10-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5ff10-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ff10-122">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="5ff10-122">-DefinitionFile</span></span>
<span data-ttu-id="5ff10-123">Ścieżka pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="5ff10-123">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ff10-124">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="5ff10-124">-Force</span></span>
<span data-ttu-id="5ff10-125">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5ff10-125">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="5ff10-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5ff10-126">-Name</span></span>
<span data-ttu-id="5ff10-127">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="5ff10-127">The trigger name.</span></span>

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

### <span data-ttu-id="5ff10-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ff10-128">-ResourceGroupName</span></span>
<span data-ttu-id="5ff10-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5ff10-129">The resource group name.</span></span>

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

### <span data-ttu-id="5ff10-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ff10-130">-ResourceId</span></span>
<span data-ttu-id="5ff10-131">Identyfikator zasobu Azure.</span><span class="sxs-lookup"><span data-stu-id="5ff10-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="5ff10-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5ff10-132">-Confirm</span></span>
<span data-ttu-id="5ff10-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5ff10-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ff10-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ff10-134">-WhatIf</span></span>
<span data-ttu-id="5ff10-135">Pokazuje, co się stanie, jeśli polecenie cmdlet zostanie uruchomione, ale nie uruchomi polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ff10-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="5ff10-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ff10-136">CommonParameters</span></span>
<span data-ttu-id="5ff10-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ff10-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ff10-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ff10-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ff10-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ff10-139">INPUTS</span></span>

### <span data-ttu-id="5ff10-140">System.String</span><span class="sxs-lookup"><span data-stu-id="5ff10-140">System.String</span></span>

## <span data-ttu-id="5ff10-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ff10-141">OUTPUTS</span></span>

### <span data-ttu-id="5ff10-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="5ff10-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="5ff10-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5ff10-143">NOTES</span></span>

## <span data-ttu-id="5ff10-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ff10-144">RELATED LINKS</span></span>

[<span data-ttu-id="5ff10-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5ff10-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="5ff10-146">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5ff10-146">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="5ff10-147">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5ff10-147">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="5ff10-148">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5ff10-148">Remove-AzDataFactoryV2Trigger</span></span>]()
