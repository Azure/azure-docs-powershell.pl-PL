---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/start-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseTrigger.md
ms.openlocfilehash: 39801db0d1cd400fa88868b87098260c9148daa3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992006"
---
# <span data-ttu-id="58b0a-101">Start-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="58b0a-101">Start-AzSynapseTrigger</span></span>

## <span data-ttu-id="58b0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58b0a-102">SYNOPSIS</span></span>
<span data-ttu-id="58b0a-103">Uruchamia wyzwalacz w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="58b0a-103">Starts a trigger in a workspace.</span></span>

## <span data-ttu-id="58b0a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="58b0a-104">SYNTAX</span></span>

### <span data-ttu-id="58b0a-105">StartByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="58b0a-105">StartByName (Default)</span></span>
```
Start-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58b0a-106">StartByObject</span><span class="sxs-lookup"><span data-stu-id="58b0a-106">StartByObject</span></span>
```
Start-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58b0a-107">StartByInputObject</span><span class="sxs-lookup"><span data-stu-id="58b0a-107">StartByInputObject</span></span>
```
Start-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58b0a-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="58b0a-108">DESCRIPTION</span></span>
<span data-ttu-id="58b0a-109">Polecenie **cmdlet Start-AzSynapseTrigger** uruchamia wyzwalacz w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="58b0a-109">The **Start-AzSynapseTrigger** cmdlet starts a trigger in a workspace.</span></span> <span data-ttu-id="58b0a-110">Jeśli wyzwalacz znajduje się w stanie "Zatrzymano", polecenie cmdlet uruchamia wyzwalacz i ostatecznie wywołuje potoki na podstawie jego definicji.</span><span class="sxs-lookup"><span data-stu-id="58b0a-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="58b0a-111">Jeśli wyzwalacz znajduje się już w stanie "Uruchomiliśmy", to polecenie cmdlet nie ma wpływu.</span><span class="sxs-lookup"><span data-stu-id="58b0a-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span>

## <span data-ttu-id="58b0a-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="58b0a-112">EXAMPLES</span></span>

### <span data-ttu-id="58b0a-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="58b0a-113">Example 1</span></span>
```powershell
PS C:\> Start-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="58b0a-114">Uruchamia wyzwalacz o nazwie ContosoTrigger w obszarze roboczym ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="58b0a-114">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="58b0a-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="58b0a-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Start-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="58b0a-116">Uruchamia wyzwalacz o nazwie ContosoTrigger w obszarze roboczym ContosoWorkspace przez potok.</span><span class="sxs-lookup"><span data-stu-id="58b0a-116">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="58b0a-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="58b0a-117">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Start-AzSynapseTrigger
```

<span data-ttu-id="58b0a-118">Uruchamia wyzwalacz o nazwie ContosoTrigger w obszarze roboczym ContosoWorkspace przez potok.</span><span class="sxs-lookup"><span data-stu-id="58b0a-118">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="58b0a-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58b0a-119">PARAMETERS</span></span>

### <span data-ttu-id="58b0a-120">— AsJob</span><span class="sxs-lookup"><span data-stu-id="58b0a-120">-AsJob</span></span>
<span data-ttu-id="58b0a-121">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="58b0a-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="58b0a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58b0a-122">-DefaultProfile</span></span>
<span data-ttu-id="58b0a-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="58b0a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58b0a-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58b0a-124">-InputObject</span></span>
<span data-ttu-id="58b0a-125">Obiekt wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="58b0a-125">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: StartByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58b0a-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="58b0a-126">-Name</span></span>
<span data-ttu-id="58b0a-127">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="58b0a-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: StartByName, StartByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58b0a-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="58b0a-128">-PassThru</span></span>
<span data-ttu-id="58b0a-129">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="58b0a-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="58b0a-130">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="58b0a-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="58b0a-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="58b0a-131">-WorkspaceName</span></span>
<span data-ttu-id="58b0a-132">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="58b0a-132">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StartByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58b0a-133">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="58b0a-133">-WorkspaceObject</span></span>
<span data-ttu-id="58b0a-134">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="58b0a-134">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: StartByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58b0a-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="58b0a-135">-Confirm</span></span>
<span data-ttu-id="58b0a-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="58b0a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58b0a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58b0a-137">-WhatIf</span></span>
<span data-ttu-id="58b0a-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58b0a-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="58b0a-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="58b0a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58b0a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58b0a-140">CommonParameters</span></span>
<span data-ttu-id="58b0a-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58b0a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58b0a-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58b0a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58b0a-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58b0a-143">INPUTS</span></span>

### <span data-ttu-id="58b0a-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="58b0a-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="58b0a-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="58b0a-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="58b0a-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58b0a-146">OUTPUTS</span></span>

### <span data-ttu-id="58b0a-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="58b0a-147">System.Boolean</span></span>

## <span data-ttu-id="58b0a-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="58b0a-148">NOTES</span></span>

## <span data-ttu-id="58b0a-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="58b0a-149">RELATED LINKS</span></span>
