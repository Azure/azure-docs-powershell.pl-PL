---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseTrigger.md
ms.openlocfilehash: 0852cbbce26e1f95bfb75975418fae30038316ab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992048"
---
# <span data-ttu-id="127c4-101">Set-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="127c4-101">Set-AzSynapseTrigger</span></span>

## <span data-ttu-id="127c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="127c4-102">SYNOPSIS</span></span>
<span data-ttu-id="127c4-103">Tworzy wyzwalacz w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="127c4-103">Creates a trigger in a workspace.</span></span>

## <span data-ttu-id="127c4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="127c4-104">SYNTAX</span></span>

### <span data-ttu-id="127c4-105">SetByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="127c4-105">SetByName (Default)</span></span>
```
Set-AzSynapseTrigger -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="127c4-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="127c4-106">SetByObject</span></span>
```
Set-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="127c4-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="127c4-107">DESCRIPTION</span></span>
<span data-ttu-id="127c4-108">Polecenie **cmdlet Set-AzSynapseTrigger** tworzy wyzwalacz w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="127c4-108">The **Set-AzSynapseTrigger** cmdlet creates a trigger in a workspace.</span></span> <span data-ttu-id="127c4-109">Wyzwalacze są tworzone w stanie "Zatrzymano", co oznacza, że nie rozpoczynają od razu wywoływania potoków, do których się odwołują.</span><span class="sxs-lookup"><span data-stu-id="127c4-109">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="127c4-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="127c4-110">EXAMPLES</span></span>

### <span data-ttu-id="127c4-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="127c4-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger -DefinitionFile ".\scheduledTrigger.json"
```

<span data-ttu-id="127c4-112">Utwórz nowy wyzwalacz o nazwie ContosoTrigger w obszarze roboczym ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="127c4-112">Create a new trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span> <span data-ttu-id="127c4-113">Wyzwalacz zostanie utworzony w stanie "Zatrzymano", co oznacza, że nie uruchamia się od razu.</span><span class="sxs-lookup"><span data-stu-id="127c4-113">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="127c4-114">Wyzwalacz można rozpocząć przy użyciu `Start-AzDataFactoryV2Trigger` polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="127c4-114">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

### <span data-ttu-id="127c4-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="127c4-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseTrigger -Name ContosoTrigger -DefinitionFile ".\scheduledTrigger.json"
```

<span data-ttu-id="127c4-116">Utwórz nowy wyzwalacz o nazwie ContosoTrigger w obszarze roboczym ContosoWorkspace za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="127c4-116">Create a new trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span> <span data-ttu-id="127c4-117">Wyzwalacz zostanie utworzony w stanie "Zatrzymano", co oznacza, że nie uruchamia się od razu.</span><span class="sxs-lookup"><span data-stu-id="127c4-117">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="127c4-118">Wyzwalacz można rozpocząć przy użyciu `Start-AzDataFactoryV2Trigger` polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="127c4-118">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="127c4-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="127c4-119">PARAMETERS</span></span>

### <span data-ttu-id="127c4-120">— AsJob</span><span class="sxs-lookup"><span data-stu-id="127c4-120">-AsJob</span></span>
<span data-ttu-id="127c4-121">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="127c4-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="127c4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="127c4-122">-DefaultProfile</span></span>
<span data-ttu-id="127c4-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="127c4-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="127c4-124">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="127c4-124">-DefinitionFile</span></span>
<span data-ttu-id="127c4-125">Ścieżka pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="127c4-125">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="127c4-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="127c4-126">-Name</span></span>
<span data-ttu-id="127c4-127">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="127c4-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="127c4-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="127c4-128">-WorkspaceName</span></span>
<span data-ttu-id="127c4-129">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="127c4-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="127c4-130">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="127c4-130">-WorkspaceObject</span></span>
<span data-ttu-id="127c4-131">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="127c4-131">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="127c4-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="127c4-132">-Confirm</span></span>
<span data-ttu-id="127c4-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="127c4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="127c4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="127c4-134">-WhatIf</span></span>
<span data-ttu-id="127c4-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="127c4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="127c4-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="127c4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="127c4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="127c4-137">CommonParameters</span></span>
<span data-ttu-id="127c4-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="127c4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="127c4-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="127c4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="127c4-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="127c4-140">INPUTS</span></span>

### <span data-ttu-id="127c4-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="127c4-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="127c4-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="127c4-142">OUTPUTS</span></span>

### <span data-ttu-id="127c4-143">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="127c4-143">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="127c4-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="127c4-144">NOTES</span></span>

## <span data-ttu-id="127c4-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="127c4-145">RELATED LINKS</span></span>
