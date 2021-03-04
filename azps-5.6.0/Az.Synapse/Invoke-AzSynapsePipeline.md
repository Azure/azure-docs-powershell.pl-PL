---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/invoke-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapsePipeline.md
ms.openlocfilehash: 756db1072eec6546f6e495b3ec2115ca77389a73
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984001"
---
# <span data-ttu-id="7c264-101">Invoke-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="7c264-101">Invoke-AzSynapsePipeline</span></span>

## <span data-ttu-id="7c264-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c264-102">SYNOPSIS</span></span>
<span data-ttu-id="7c264-103">Wywołuje potok, aby rozpocząć jego uruchamianie.</span><span class="sxs-lookup"><span data-stu-id="7c264-103">Invokes a pipeline to start a run for it.</span></span>

## <span data-ttu-id="7c264-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7c264-104">SYNTAX</span></span>

### <span data-ttu-id="7c264-105">NewByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="7c264-105">NewByName (Default)</span></span>
```
Invoke-AzSynapsePipeline -WorkspaceName <String> -PipelineName <String> [-Parameter <Hashtable>]
 [-ParameterFile <String>] [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c264-106">NewByInputObject</span><span class="sxs-lookup"><span data-stu-id="7c264-106">NewByInputObject</span></span>
```
Invoke-AzSynapsePipeline -InputObject <PSPipelineResource> [-Parameter <Hashtable>] [-ParameterFile <String>]
 [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c264-107">NewByObject</span><span class="sxs-lookup"><span data-stu-id="7c264-107">NewByObject</span></span>
```
Invoke-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -PipelineName <String> [-Parameter <Hashtable>]
 [-ParameterFile <String>] [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c264-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="7c264-108">DESCRIPTION</span></span>
<span data-ttu-id="7c264-109">Polecenie **Invoke-AzSynapsePipeline** uruchamia uruchomienie w określonym potoku i zwraca identyfikator tego uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="7c264-109">The **Invoke-AzSynapsePipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="7c264-110">Ten identyfikator GUID może zostać przekazany do użytkownika **Get-AzSynapsePipelineRun** lub **Get-AzSynapseActivityRun,** aby uzyskać szczegółowe informacje o tym uruchomieniu.</span><span class="sxs-lookup"><span data-stu-id="7c264-110">This GUID can be passed to **Get-AzSynapsePipelineRun** or **Get-AzSynapseActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="7c264-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7c264-111">EXAMPLES</span></span>

### <span data-ttu-id="7c264-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7c264-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSynapsePipeline -WorkspaceName ContosoWorkspace -PipelineName ContosoPipeline
```

<span data-ttu-id="7c264-113">To polecenie uruchamia uruchomienie potoku o nazwie ContosoPipeline w obszarze roboczym ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="7c264-113">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="7c264-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="7c264-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Invoke-AzSynapsePipeline -PipelineName ContosoPipeline
```

<span data-ttu-id="7c264-115">To polecenie uruchamia potok o nazwie ContosoPipeline w obszarze roboczym ContosoWorkspace za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="7c264-115">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="7c264-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="7c264-116">Example 3</span></span>
```powershell
PS C:\> $pipeline = Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
PS C:\> $pipeline | Invoke-AzSynapsePipeline
```

<span data-ttu-id="7c264-117">To polecenie uruchamia potok o nazwie ContosoPipeline w obszarze roboczym ContosoWorkspace za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="7c264-117">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="7c264-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c264-118">PARAMETERS</span></span>

### <span data-ttu-id="7c264-119">— AsJob</span><span class="sxs-lookup"><span data-stu-id="7c264-119">-AsJob</span></span>
<span data-ttu-id="7c264-120">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7c264-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7c264-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c264-121">-DefaultProfile</span></span>
<span data-ttu-id="7c264-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7c264-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c264-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c264-123">-InputObject</span></span>
<span data-ttu-id="7c264-124">Informacje o uruchomieniu potoku.</span><span class="sxs-lookup"><span data-stu-id="7c264-124">The information about the pipeline run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource
Parameter Sets: NewByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c264-125">— IsRecovery</span><span class="sxs-lookup"><span data-stu-id="7c264-125">-IsRecovery</span></span>
<span data-ttu-id="7c264-126">Flaga trybu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="7c264-126">Recovery mode flag.</span></span>
<span data-ttu-id="7c264-127">Jeśli tryb odzyskiwania ma wartość True (Prawda), potok, do których prowadzi odwołanie, zostanie pogrupowany pod tym samym wartością groupId(a).</span><span class="sxs-lookup"><span data-stu-id="7c264-127">If recovery mode is set to true, the specified referenced pipeline run and the new run will be grouped under the same groupId.</span></span>

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

### <span data-ttu-id="7c264-128">- Parametr</span><span class="sxs-lookup"><span data-stu-id="7c264-128">-Parameter</span></span>
<span data-ttu-id="7c264-129">Parametry uruchomienia potoku.</span><span class="sxs-lookup"><span data-stu-id="7c264-129">Parameters for pipeline run.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c264-130">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="7c264-130">-ParameterFile</span></span>
<span data-ttu-id="7c264-131">Nazwa pliku z parametrami do uruchomienia potoku.</span><span class="sxs-lookup"><span data-stu-id="7c264-131">The name of the file with parameters for pipeline run.</span></span>

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

### <span data-ttu-id="7c264-132">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="7c264-132">-PipelineName</span></span>
<span data-ttu-id="7c264-133">Nazwa potoku.</span><span class="sxs-lookup"><span data-stu-id="7c264-133">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByName, NewByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c264-134">-ReferencePipelineRunId</span><span class="sxs-lookup"><span data-stu-id="7c264-134">-ReferencePipelineRunId</span></span>
<span data-ttu-id="7c264-135">Identyfikator uruchomienia potoku dla ponownego uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="7c264-135">The pipeline run ID for rerun.</span></span>
<span data-ttu-id="7c264-136">Jeśli zostanie określony identyfikator uruchomienia, parametry określonego uruchomienia zostaną użyte do utworzenia nowego uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="7c264-136">If run ID is specified, the parameters of the specified run will be used to create a new run.</span></span>

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

### <span data-ttu-id="7c264-137">-StartActivityName</span><span class="sxs-lookup"><span data-stu-id="7c264-137">-StartActivityName</span></span>
<span data-ttu-id="7c264-138">W trybie odzyskiwania ponowne uruchomienie rozpocznie się od tego działania.</span><span class="sxs-lookup"><span data-stu-id="7c264-138">In recovery mode, the rerun will start from this activity.</span></span>
<span data-ttu-id="7c264-139">Jeśli nie zostanie określona, zostaną uruchomione wszystkie działania.</span><span class="sxs-lookup"><span data-stu-id="7c264-139">If not specified, all activities will run.</span></span>

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

### <span data-ttu-id="7c264-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7c264-140">-WorkspaceName</span></span>
<span data-ttu-id="7c264-141">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="7c264-141">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c264-142">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7c264-142">-WorkspaceObject</span></span>
<span data-ttu-id="7c264-143">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="7c264-143">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: NewByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c264-144">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7c264-144">-Confirm</span></span>
<span data-ttu-id="7c264-145">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7c264-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c264-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c264-146">-WhatIf</span></span>
<span data-ttu-id="7c264-147">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c264-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c264-148">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7c264-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c264-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c264-149">CommonParameters</span></span>
<span data-ttu-id="7c264-150">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c264-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c264-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7c264-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c264-152">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7c264-152">INPUTS</span></span>

### <span data-ttu-id="7c264-153">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="7c264-153">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

### <span data-ttu-id="7c264-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7c264-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="7c264-155">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7c264-155">OUTPUTS</span></span>

### <span data-ttu-id="7c264-156">Microsoft.Azure.Commands.Synapse.Models.PSCreateRunResponse</span><span class="sxs-lookup"><span data-stu-id="7c264-156">Microsoft.Azure.Commands.Synapse.Models.PSCreateRunResponse</span></span>

## <span data-ttu-id="7c264-157">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7c264-157">NOTES</span></span>

## <span data-ttu-id="7c264-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7c264-158">RELATED LINKS</span></span>
