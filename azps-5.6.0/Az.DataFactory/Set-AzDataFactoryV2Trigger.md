---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/set-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Trigger.md
ms.openlocfilehash: b0058f21f472f14e97898ea81636fa000034bed5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006929"
---
# <span data-ttu-id="09149-101">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="09149-101">Set-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="09149-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09149-102">SYNOPSIS</span></span>
<span data-ttu-id="09149-103">Tworzy wyzwalacz w zakładzie danych.</span><span class="sxs-lookup"><span data-stu-id="09149-103">Creates a trigger in a data factory.</span></span>

## <span data-ttu-id="09149-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="09149-104">SYNTAX</span></span>

### <span data-ttu-id="09149-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="09149-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Trigger [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="09149-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="09149-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Trigger [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09149-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="09149-107">DESCRIPTION</span></span>
<span data-ttu-id="09149-108">Polecenie **cmdlet Set-AzDataFactoryV2Trigger** tworzy wyzwalacz w fabrycznej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="09149-108">The **Set-AzDataFactoryV2Trigger** cmdlet creates a trigger in a data factory.</span></span> <span data-ttu-id="09149-109">Jeśli określisz nazwę wyzwalacza, który już istnieje, polecenie cmdlet wyświetli monit o potwierdzenie przed zastąpieniem wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="09149-109">If you specify a name for a trigger that already exists, the cmdlet prompts for confirmation before replacing the trigger.</span></span> <span data-ttu-id="09149-110">W przypadku określenia _parametru Force_ polecenie cmdlet zastępuje istniejący wyzwalacz bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="09149-110">If you specify the _Force_ parameter, the cmdlet replaces the existing trigger without prompting for confirmation.</span></span> <span data-ttu-id="09149-111">Wyzwalacze są tworzone w stanie "Zatrzymano", co oznacza, że nie rozpoczynają od razu wywoływania potoków, do których się odwołują.</span><span class="sxs-lookup"><span data-stu-id="09149-111">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="09149-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="09149-112">EXAMPLES</span></span>

### <span data-ttu-id="09149-113">Przykład 1. Tworzenie wyzwalacza</span><span class="sxs-lookup"><span data-stu-id="09149-113">Example 1: Create a trigger</span></span>
```
PS C:\> Set-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger" -DefinitionFile ".\scheduledTrigger.json"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="09149-114">Utwórz nowy wyzwalacz o nazwie "ScheduledTrigger" w fabrycznej układzie danych "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="09149-114">Create a new trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span> <span data-ttu-id="09149-115">Wyzwalacz zostanie utworzony w stanie "Zatrzymano", co oznacza, że nie uruchamia się od razu.</span><span class="sxs-lookup"><span data-stu-id="09149-115">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="09149-116">Wyzwalacz można rozpocząć przy użyciu `Start-AzDataFactoryV2Trigger` polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09149-116">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="09149-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09149-117">PARAMETERS</span></span>

### <span data-ttu-id="09149-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="09149-118">-DataFactoryName</span></span>
<span data-ttu-id="09149-119">Nazwa fabryczna danych.</span><span class="sxs-lookup"><span data-stu-id="09149-119">The data factory name.</span></span>

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

### <span data-ttu-id="09149-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09149-120">-DefaultProfile</span></span>
<span data-ttu-id="09149-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="09149-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09149-122">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="09149-122">-DefinitionFile</span></span>
<span data-ttu-id="09149-123">Ścieżka pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="09149-123">The JSON file path.</span></span>

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

### <span data-ttu-id="09149-124">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="09149-124">-Force</span></span>
<span data-ttu-id="09149-125">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="09149-125">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="09149-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="09149-126">-Name</span></span>
<span data-ttu-id="09149-127">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="09149-127">The trigger name.</span></span>

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

### <span data-ttu-id="09149-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09149-128">-ResourceGroupName</span></span>
<span data-ttu-id="09149-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="09149-129">The resource group name.</span></span>

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

### <span data-ttu-id="09149-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="09149-130">-ResourceId</span></span>
<span data-ttu-id="09149-131">Identyfikator zasobu Azure.</span><span class="sxs-lookup"><span data-stu-id="09149-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="09149-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="09149-132">-Confirm</span></span>
<span data-ttu-id="09149-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="09149-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09149-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09149-134">-WhatIf</span></span>
<span data-ttu-id="09149-135">Pokazuje, co się stanie, jeśli polecenie cmdlet zostanie uruchomione, ale nie uruchomi polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09149-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="09149-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09149-136">CommonParameters</span></span>
<span data-ttu-id="09149-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09149-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09149-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09149-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09149-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="09149-139">INPUTS</span></span>

### <span data-ttu-id="09149-140">System.String</span><span class="sxs-lookup"><span data-stu-id="09149-140">System.String</span></span>

## <span data-ttu-id="09149-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="09149-141">OUTPUTS</span></span>

### <span data-ttu-id="09149-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="09149-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="09149-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="09149-143">NOTES</span></span>

## <span data-ttu-id="09149-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="09149-144">RELATED LINKS</span></span>

[<span data-ttu-id="09149-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="09149-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="09149-146">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="09149-146">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="09149-147">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="09149-147">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="09149-148">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="09149-148">Remove-AzDataFactoryV2Trigger</span></span>]()
