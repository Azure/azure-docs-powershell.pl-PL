---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsepipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapsePipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapsePipelineRun.md
ms.openlocfilehash: f907afbc573d558a08d514c019cbcbe3fa999bf6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225566"
---
# <span data-ttu-id="abe4b-101">Stop-AzSynapsePipelineRun</span><span class="sxs-lookup"><span data-stu-id="abe4b-101">Stop-AzSynapsePipelineRun</span></span>

## <span data-ttu-id="abe4b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="abe4b-102">SYNOPSIS</span></span>
<span data-ttu-id="abe4b-103">Zatrzymuje uruchamianie rurociągu w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="abe4b-103">Stops a pipeline run in a workspace.</span></span>

## <span data-ttu-id="abe4b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="abe4b-104">SYNTAX</span></span>

### <span data-ttu-id="abe4b-105">RemoveByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="abe4b-105">RemoveByName (Default)</span></span>
```
Stop-AzSynapsePipelineRun -WorkspaceName <String> -PipelineRunId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abe4b-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="abe4b-106">RemoveByObject</span></span>
```
Stop-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -PipelineRunId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abe4b-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="abe4b-107">RemoveByInputObject</span></span>
```
Stop-AzSynapsePipelineRun -InputObject <PSPipelineRun> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abe4b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="abe4b-108">DESCRIPTION</span></span>
<span data-ttu-id="abe4b-109">Polecenie cmdlet **stop-AzSynapsePipelineRun** zatrzymuje potok uruchomiony w obszarze roboczym określonym przy użyciu identyfikatora uruchomienia potoku.</span><span class="sxs-lookup"><span data-stu-id="abe4b-109">The **Stop-AzSynapsePipelineRun** cmdlet stops a pipeline run in a workspace specified with the pipeline run ID.</span></span>

## <span data-ttu-id="abe4b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="abe4b-110">EXAMPLES</span></span>

### <span data-ttu-id="abe4b-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="abe4b-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
```

<span data-ttu-id="abe4b-112">To polecenie zatrzymuje potok uruchomiony z identyfikatorem b9730a13-AA12-4926-a8b3-8e3a974ab0bd w obszarze roboczym ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="abe4b-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="abe4b-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="abe4b-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Stop-AzSynapsePipelineRun -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
```

<span data-ttu-id="abe4b-114">To polecenie zatrzymuje potok uruchomiony z identyfikatorem b9730a13-AA12-4926-a8b3-8e3a974ab0bd w obszarze roboczym ContosoWorkspace za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="abe4b-114">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="abe4b-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="abe4b-115">Example 3</span></span>
```powershell
PS C:\> $pipelineRun = Get-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
PS C:\> $pipelineRun | Stop-AzSynapsePipelineRun
```

<span data-ttu-id="abe4b-116">To polecenie zatrzymuje potok uruchomiony z identyfikatorem b9730a13-AA12-4926-a8b3-8e3a974ab0bd w obszarze roboczym ContosoWorkspace za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="abe4b-116">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="abe4b-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="abe4b-117">PARAMETERS</span></span>

### <span data-ttu-id="abe4b-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="abe4b-118">-AsJob</span></span>
<span data-ttu-id="abe4b-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="abe4b-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="abe4b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abe4b-120">-DefaultProfile</span></span>
<span data-ttu-id="abe4b-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="abe4b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abe4b-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="abe4b-122">-InputObject</span></span>
<span data-ttu-id="abe4b-123">Informacje o uruchomieniu rurociągu.</span><span class="sxs-lookup"><span data-stu-id="abe4b-123">The information about the pipeline run.</span></span>

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

### <span data-ttu-id="abe4b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="abe4b-124">-PassThru</span></span>
<span data-ttu-id="abe4b-125">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="abe4b-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="abe4b-126">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="abe4b-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="abe4b-127">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="abe4b-127">-PipelineRunId</span></span>
<span data-ttu-id="abe4b-128">Identyfikator uruchomienia rurociągu.</span><span class="sxs-lookup"><span data-stu-id="abe4b-128">The pipeline run identifier.</span></span>

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

### <span data-ttu-id="abe4b-129">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="abe4b-129">-WorkspaceName</span></span>
<span data-ttu-id="abe4b-130">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="abe4b-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="abe4b-131">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="abe4b-131">-WorkspaceObject</span></span>
<span data-ttu-id="abe4b-132">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="abe4b-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="abe4b-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="abe4b-133">-Confirm</span></span>
<span data-ttu-id="abe4b-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="abe4b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abe4b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abe4b-135">-WhatIf</span></span>
<span data-ttu-id="abe4b-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="abe4b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abe4b-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="abe4b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abe4b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abe4b-138">CommonParameters</span></span>
<span data-ttu-id="abe4b-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abe4b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abe4b-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="abe4b-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abe4b-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="abe4b-141">INPUTS</span></span>

### <span data-ttu-id="abe4b-142">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="abe4b-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="abe4b-143">Microsoft. Azure. Commands. Synapse. models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="abe4b-143">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span></span>

## <span data-ttu-id="abe4b-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="abe4b-144">OUTPUTS</span></span>

### <span data-ttu-id="abe4b-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="abe4b-145">System.Boolean</span></span>

## <span data-ttu-id="abe4b-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="abe4b-146">NOTES</span></span>

## <span data-ttu-id="abe4b-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="abe4b-147">RELATED LINKS</span></span>
