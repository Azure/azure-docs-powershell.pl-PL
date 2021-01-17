---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/invoke-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapsePipeline.md
ms.openlocfilehash: fc8f24cb124194bc2d2acd5ab5f19a4484571079
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370526"
---
# <span data-ttu-id="49b13-101">Invoke-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="49b13-101">Invoke-AzSynapsePipeline</span></span>

## <span data-ttu-id="49b13-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="49b13-102">SYNOPSIS</span></span>
<span data-ttu-id="49b13-103">Wywołuje potok w celu uruchomienia go.</span><span class="sxs-lookup"><span data-stu-id="49b13-103">Invokes a pipeline to start a run for it.</span></span>

## <span data-ttu-id="49b13-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="49b13-104">SYNTAX</span></span>

### <span data-ttu-id="49b13-105">NewByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="49b13-105">NewByName (Default)</span></span>
```
Invoke-AzSynapsePipeline -WorkspaceName <String> -PipelineName <String> [-Parameter <Hashtable>]
 [-ParameterFile <String>] [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49b13-106">NewByInputObject</span><span class="sxs-lookup"><span data-stu-id="49b13-106">NewByInputObject</span></span>
```
Invoke-AzSynapsePipeline -InputObject <PSPipelineResource> [-Parameter <Hashtable>] [-ParameterFile <String>]
 [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49b13-107">NewByObject</span><span class="sxs-lookup"><span data-stu-id="49b13-107">NewByObject</span></span>
```
Invoke-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -PipelineName <String> [-Parameter <Hashtable>]
 [-ParameterFile <String>] [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49b13-108">Opis</span><span class="sxs-lookup"><span data-stu-id="49b13-108">DESCRIPTION</span></span>
<span data-ttu-id="49b13-109">Polecenie **Invoke-AzSynapsePipeline** rozpoczyna działanie w określonym potoku i zwraca identyfikator.</span><span class="sxs-lookup"><span data-stu-id="49b13-109">The **Invoke-AzSynapsePipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="49b13-110">Ten identyfikator GUID można przekazać do **AzSynapsePipelineRun** lub **Get-AzSynapseActivityRun** , aby uzyskać więcej informacji na temat tego uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="49b13-110">This GUID can be passed to **Get-AzSynapsePipelineRun** or **Get-AzSynapseActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="49b13-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="49b13-111">EXAMPLES</span></span>

### <span data-ttu-id="49b13-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="49b13-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSynapsePipeline -WorkspaceName ContosoWorkspace -PipelineName ContosoPipeline
```

<span data-ttu-id="49b13-113">To polecenie rozpoczyna uruchamianie rurociągu o nazwie ContosoPipeline w obszarze roboczym ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="49b13-113">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="49b13-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="49b13-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Invoke-AzSynapsePipeline -PipelineName ContosoPipeline
```

<span data-ttu-id="49b13-115">To polecenie rozpoczyna uruchamianie rurociągu o nazwie ContosoPipeline w obszarze roboczym ContosoWorkspace za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="49b13-115">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="49b13-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="49b13-116">Example 3</span></span>
```powershell
PS C:\> $pipeline = Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
PS C:\> $pipeline | Invoke-AzSynapsePipeline
```

<span data-ttu-id="49b13-117">To polecenie rozpoczyna uruchamianie rurociągu o nazwie ContosoPipeline w obszarze roboczym ContosoWorkspace za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="49b13-117">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="49b13-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="49b13-118">PARAMETERS</span></span>

### <span data-ttu-id="49b13-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="49b13-119">-AsJob</span></span>
<span data-ttu-id="49b13-120">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="49b13-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="49b13-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49b13-121">-DefaultProfile</span></span>
<span data-ttu-id="49b13-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="49b13-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49b13-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="49b13-123">-InputObject</span></span>
<span data-ttu-id="49b13-124">Informacje o uruchomieniu rurociągu.</span><span class="sxs-lookup"><span data-stu-id="49b13-124">The information about the pipeline run.</span></span>

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

### <span data-ttu-id="49b13-125">-Isrecovery</span><span class="sxs-lookup"><span data-stu-id="49b13-125">-IsRecovery</span></span>
<span data-ttu-id="49b13-126">Flaga trybu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="49b13-126">Recovery mode flag.</span></span>
<span data-ttu-id="49b13-127">Jeśli tryb odzyskiwania jest ustawiony na wartość true, określony potok zostanie uruchomiony, a nowy proces zostanie zgrupowany w tym samym identyfikatorze groupId.</span><span class="sxs-lookup"><span data-stu-id="49b13-127">If recovery mode is set to true, the specified referenced pipeline run and the new run will be grouped under the same groupId.</span></span>

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

### <span data-ttu-id="49b13-128">-Parameter</span><span class="sxs-lookup"><span data-stu-id="49b13-128">-Parameter</span></span>
<span data-ttu-id="49b13-129">Parametry uruchamiania rurociągu.</span><span class="sxs-lookup"><span data-stu-id="49b13-129">Parameters for pipeline run.</span></span>

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

### <span data-ttu-id="49b13-130">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="49b13-130">-ParameterFile</span></span>
<span data-ttu-id="49b13-131">Nazwa pliku z parametrami w celu uruchomienia rurociągu.</span><span class="sxs-lookup"><span data-stu-id="49b13-131">The name of the file with parameters for pipeline run.</span></span>

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

### <span data-ttu-id="49b13-132">-Pipelinename</span><span class="sxs-lookup"><span data-stu-id="49b13-132">-PipelineName</span></span>
<span data-ttu-id="49b13-133">Nazwa potoku.</span><span class="sxs-lookup"><span data-stu-id="49b13-133">The pipeline name.</span></span>

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

### <span data-ttu-id="49b13-134">-ReferencePipelineRunId</span><span class="sxs-lookup"><span data-stu-id="49b13-134">-ReferencePipelineRunId</span></span>
<span data-ttu-id="49b13-135">Identyfikator uruchomienia potoku w celu ponownego uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="49b13-135">The pipeline run ID for rerun.</span></span>
<span data-ttu-id="49b13-136">Jeśli jest określony identyfikator uruchomienia, w celu utworzenia nowego uruchomienia zostanie użyte parametry określonego uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="49b13-136">If run ID is specified, the parameters of the specified run will be used to create a new run.</span></span>

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

### <span data-ttu-id="49b13-137">-StartActivityName</span><span class="sxs-lookup"><span data-stu-id="49b13-137">-StartActivityName</span></span>
<span data-ttu-id="49b13-138">W trybie odzyskiwania rozpocznie się ponowne uruchomienie od tego działania.</span><span class="sxs-lookup"><span data-stu-id="49b13-138">In recovery mode, the rerun will start from this activity.</span></span>
<span data-ttu-id="49b13-139">Jeśli nie określono, zostaną uruchomione wszystkie działania.</span><span class="sxs-lookup"><span data-stu-id="49b13-139">If not specified, all activities will run.</span></span>

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

### <span data-ttu-id="49b13-140">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="49b13-140">-WorkspaceName</span></span>
<span data-ttu-id="49b13-141">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="49b13-141">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="49b13-142">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="49b13-142">-WorkspaceObject</span></span>
<span data-ttu-id="49b13-143">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="49b13-143">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="49b13-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="49b13-144">-Confirm</span></span>
<span data-ttu-id="49b13-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49b13-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49b13-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49b13-146">-WhatIf</span></span>
<span data-ttu-id="49b13-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49b13-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49b13-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="49b13-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49b13-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49b13-149">CommonParameters</span></span>
<span data-ttu-id="49b13-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49b13-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49b13-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="49b13-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49b13-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49b13-152">INPUTS</span></span>

### <span data-ttu-id="49b13-153">Microsoft. Azure. Commands. Synapse. models. PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="49b13-153">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

### <span data-ttu-id="49b13-154">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="49b13-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="49b13-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="49b13-155">OUTPUTS</span></span>

### <span data-ttu-id="49b13-156">Microsoft. Azure. Commands. Synapse. models. PSCreateRunResponse</span><span class="sxs-lookup"><span data-stu-id="49b13-156">Microsoft.Azure.Commands.Synapse.Models.PSCreateRunResponse</span></span>

## <span data-ttu-id="49b13-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="49b13-157">NOTES</span></span>

## <span data-ttu-id="49b13-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="49b13-158">RELATED LINKS</span></span>
