---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/start-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseTrigger.md
ms.openlocfilehash: d2488a99bba1813c192df5ef8561d83c06f2f6e7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197314"
---
# <span data-ttu-id="06842-101">Start-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="06842-101">Start-AzSynapseTrigger</span></span>

## <span data-ttu-id="06842-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06842-102">SYNOPSIS</span></span>
<span data-ttu-id="06842-103">Uruchamia wyzwalacz w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="06842-103">Starts a trigger in a workspace.</span></span>

## <span data-ttu-id="06842-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="06842-104">SYNTAX</span></span>

### <span data-ttu-id="06842-105">StartByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="06842-105">StartByName (Default)</span></span>
```
Start-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06842-106">StartByObject</span><span class="sxs-lookup"><span data-stu-id="06842-106">StartByObject</span></span>
```
Start-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06842-107">StartByInputObject</span><span class="sxs-lookup"><span data-stu-id="06842-107">StartByInputObject</span></span>
```
Start-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06842-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="06842-108">DESCRIPTION</span></span>
<span data-ttu-id="06842-109">Polecenie **cmdlet Start-AzSynapseTrigger** uruchamia wyzwalacz w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="06842-109">The **Start-AzSynapseTrigger** cmdlet starts a trigger in a workspace.</span></span> <span data-ttu-id="06842-110">Jeśli wyzwalacz znajduje się w stanie "Zatrzymano", polecenie cmdlet uruchamia wyzwalacz i ostatecznie wywołuje potoki na podstawie jego definicji.</span><span class="sxs-lookup"><span data-stu-id="06842-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="06842-111">Jeśli wyzwalacz znajduje się już w stanie "Uruchomiliśmy", to polecenie cmdlet nie ma wpływu.</span><span class="sxs-lookup"><span data-stu-id="06842-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span>

## <span data-ttu-id="06842-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="06842-112">EXAMPLES</span></span>

### <span data-ttu-id="06842-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="06842-113">Example 1</span></span>
```powershell
PS C:\> Start-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="06842-114">Uruchamia wyzwalacz o nazwie ContosoTrigger w obszarze roboczym ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="06842-114">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="06842-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="06842-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Start-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="06842-116">Uruchamia wyzwalacz o nazwie ContosoTrigger w obszarze roboczym ContosoWorkspace za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="06842-116">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="06842-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="06842-117">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Start-AzSynapseTrigger
```

<span data-ttu-id="06842-118">Uruchamia wyzwalacz o nazwie ContosoTrigger w obszarze roboczym ContosoWorkspace za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="06842-118">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="06842-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06842-119">PARAMETERS</span></span>

### <span data-ttu-id="06842-120">— AsJob</span><span class="sxs-lookup"><span data-stu-id="06842-120">-AsJob</span></span>
<span data-ttu-id="06842-121">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="06842-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="06842-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06842-122">-DefaultProfile</span></span>
<span data-ttu-id="06842-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="06842-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06842-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06842-124">-InputObject</span></span>
<span data-ttu-id="06842-125">Obiekt wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="06842-125">The trigger object.</span></span>

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

### <span data-ttu-id="06842-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="06842-126">-Name</span></span>
<span data-ttu-id="06842-127">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="06842-127">The trigger name.</span></span>

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

### <span data-ttu-id="06842-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06842-128">-PassThru</span></span>
<span data-ttu-id="06842-129">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="06842-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="06842-130">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="06842-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="06842-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="06842-131">-WorkspaceName</span></span>
<span data-ttu-id="06842-132">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="06842-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="06842-133">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="06842-133">-WorkspaceObject</span></span>
<span data-ttu-id="06842-134">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="06842-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="06842-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="06842-135">-Confirm</span></span>
<span data-ttu-id="06842-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="06842-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06842-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06842-137">-WhatIf</span></span>
<span data-ttu-id="06842-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06842-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="06842-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="06842-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06842-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06842-140">CommonParameters</span></span>
<span data-ttu-id="06842-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06842-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06842-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="06842-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06842-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06842-143">INPUTS</span></span>

### <span data-ttu-id="06842-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="06842-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="06842-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="06842-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="06842-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="06842-146">OUTPUTS</span></span>

### <span data-ttu-id="06842-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="06842-147">System.Boolean</span></span>

## <span data-ttu-id="06842-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="06842-148">NOTES</span></span>

## <span data-ttu-id="06842-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="06842-149">RELATED LINKS</span></span>
