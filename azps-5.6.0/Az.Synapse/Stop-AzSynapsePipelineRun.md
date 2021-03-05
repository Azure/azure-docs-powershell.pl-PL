---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/stop-azsynapsepipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapsePipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapsePipelineRun.md
ms.openlocfilehash: 607b251deff02ae6a74f0ceb5fc4f88a9c899688
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991999"
---
# <span data-ttu-id="c0368-101">Stop-AzSynapsePipelineRun</span><span class="sxs-lookup"><span data-stu-id="c0368-101">Stop-AzSynapsePipelineRun</span></span>

## <span data-ttu-id="c0368-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0368-102">SYNOPSIS</span></span>
<span data-ttu-id="c0368-103">Zatrzymuje uruchomienie potoku w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="c0368-103">Stops a pipeline run in a workspace.</span></span>

## <span data-ttu-id="c0368-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c0368-104">SYNTAX</span></span>

### <span data-ttu-id="c0368-105">RemoveByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="c0368-105">RemoveByName (Default)</span></span>
```
Stop-AzSynapsePipelineRun -WorkspaceName <String> -PipelineRunId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0368-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="c0368-106">RemoveByObject</span></span>
```
Stop-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -PipelineRunId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0368-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="c0368-107">RemoveByInputObject</span></span>
```
Stop-AzSynapsePipelineRun -InputObject <PSPipelineRun> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0368-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="c0368-108">DESCRIPTION</span></span>
<span data-ttu-id="c0368-109">Polecenie **cmdlet Stop-AzSynapsePipelineRun** zatrzymuje uruchomienie potoku w obszarze roboczym określonym przy użyciu identyfikatora uruchamiania potoku.</span><span class="sxs-lookup"><span data-stu-id="c0368-109">The **Stop-AzSynapsePipelineRun** cmdlet stops a pipeline run in a workspace specified with the pipeline run ID.</span></span>

## <span data-ttu-id="c0368-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c0368-110">EXAMPLES</span></span>

### <span data-ttu-id="c0368-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c0368-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
```

<span data-ttu-id="c0368-112">To polecenie zatrzymuje uruchomienie potoku o identyfikatorze b9730a13-aa12-4926-a8b3-8e3a974ab0bd w obszarze roboczym ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="c0368-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="c0368-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c0368-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Stop-AzSynapsePipelineRun -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
```

<span data-ttu-id="c0368-114">To polecenie zatrzymuje uruchomienie potoku o identyfikatorze b9730a13-aa12-4926-a8b3-8e3a974ab0bd w obszarze roboczym ContosoWorkspace za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="c0368-114">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="c0368-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="c0368-115">Example 3</span></span>
```powershell
PS C:\> $pipelineRun = Get-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
PS C:\> $pipelineRun | Stop-AzSynapsePipelineRun
```

<span data-ttu-id="c0368-116">To polecenie zatrzymuje uruchomienie potoku o identyfikatorze b9730a13-aa12-4926-a8b3-8e3a974ab0bd w obszarze roboczym ContosoWorkspace za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="c0368-116">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="c0368-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0368-117">PARAMETERS</span></span>

### <span data-ttu-id="c0368-118">— AsJob</span><span class="sxs-lookup"><span data-stu-id="c0368-118">-AsJob</span></span>
<span data-ttu-id="c0368-119">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c0368-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c0368-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0368-120">-DefaultProfile</span></span>
<span data-ttu-id="c0368-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c0368-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0368-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0368-122">-InputObject</span></span>
<span data-ttu-id="c0368-123">Informacje o uruchomieniu potoku.</span><span class="sxs-lookup"><span data-stu-id="c0368-123">The information about the pipeline run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0368-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c0368-124">-PassThru</span></span>
<span data-ttu-id="c0368-125">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="c0368-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="c0368-126">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="c0368-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="c0368-127">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="c0368-127">-PipelineRunId</span></span>
<span data-ttu-id="c0368-128">Identyfikator uruchomienia potoku.</span><span class="sxs-lookup"><span data-stu-id="c0368-128">The pipeline run identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0368-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c0368-129">-WorkspaceName</span></span>
<span data-ttu-id="c0368-130">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="c0368-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0368-131">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c0368-131">-WorkspaceObject</span></span>
<span data-ttu-id="c0368-132">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="c0368-132">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0368-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c0368-133">-Confirm</span></span>
<span data-ttu-id="c0368-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c0368-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0368-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0368-135">-WhatIf</span></span>
<span data-ttu-id="c0368-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0368-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0368-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c0368-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0368-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0368-138">CommonParameters</span></span>
<span data-ttu-id="c0368-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0368-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0368-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0368-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0368-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0368-141">INPUTS</span></span>

### <span data-ttu-id="c0368-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c0368-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="c0368-143">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="c0368-143">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span></span>

## <span data-ttu-id="c0368-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0368-144">OUTPUTS</span></span>

### <span data-ttu-id="c0368-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c0368-145">System.Boolean</span></span>

## <span data-ttu-id="c0368-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c0368-146">NOTES</span></span>

## <span data-ttu-id="c0368-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c0368-147">RELATED LINKS</span></span>
