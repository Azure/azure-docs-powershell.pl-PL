---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/add-azsynapsetriggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
ms.openlocfilehash: d9ff2e46b7b4ccf7b3d2fafd1aa8142efd0675b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981377"
---
# <span data-ttu-id="37941-101">Add-AzSynapseTriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="37941-101">Add-AzSynapseTriggerSubscription</span></span>

## <span data-ttu-id="37941-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37941-102">SYNOPSIS</span></span>
<span data-ttu-id="37941-103">Zasubskrybuj wyzwalacz zdarzenia zdarzenia w usłudze zewnętrznej.</span><span class="sxs-lookup"><span data-stu-id="37941-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="37941-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="37941-104">SYNTAX</span></span>

### <span data-ttu-id="37941-105">AddByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="37941-105">AddByName (Default)</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceName <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37941-106">AddByObject</span><span class="sxs-lookup"><span data-stu-id="37941-106">AddByObject</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37941-107">AddByInputObject</span><span class="sxs-lookup"><span data-stu-id="37941-107">AddByInputObject</span></span>
```
Add-AzSynapseTriggerSubscription -InputObject <PSTriggerResource> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37941-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="37941-108">DESCRIPTION</span></span>
<span data-ttu-id="37941-109">Polecenie **cmdlet Add-AzSynapseTriggerSubscription** subskrybuje wyzwalacz zdarzenia określonym zdarzeniami usługi zewnętrznej z definicji wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="37941-109">The **Add-AzSynapseTriggerSubscription** cmdlet subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="37941-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="37941-110">EXAMPLES</span></span>

### <span data-ttu-id="37941-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="37941-111">Example 1</span></span>
```powershell
PS C:\> Add-AzSynapseTriggerSubscription -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="37941-112">To polecenie subskrybuje wyzwalacz o nazwie ContosoTrigger do określonych zdarzeń z definicji wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="37941-112">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion.</span></span>

### <span data-ttu-id="37941-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="37941-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Add-AzSynapseTriggerSubscription -Name ContosoTrigger
```

<span data-ttu-id="37941-114">To polecenie subskrybuje wyzwalacz o nazwie ContosoTrigger do określonych zdarzeń z definicji wyzwalacza za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="37941-114">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

### <span data-ttu-id="37941-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="37941-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Add-AzSynapseTriggerSubscription
```

<span data-ttu-id="37941-116">To polecenie subskrybuje wyzwalacz o nazwie ContosoTrigger do określonych zdarzeń z definicji wyzwalacza za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="37941-116">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

## <span data-ttu-id="37941-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37941-117">PARAMETERS</span></span>

### <span data-ttu-id="37941-118">— AsJob</span><span class="sxs-lookup"><span data-stu-id="37941-118">-AsJob</span></span>
<span data-ttu-id="37941-119">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="37941-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="37941-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37941-120">-DefaultProfile</span></span>
<span data-ttu-id="37941-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="37941-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37941-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37941-122">-InputObject</span></span>
<span data-ttu-id="37941-123">Obiekt wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="37941-123">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: AddByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37941-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="37941-124">-Name</span></span>
<span data-ttu-id="37941-125">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="37941-125">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: AddByName, AddByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37941-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="37941-126">-WorkspaceName</span></span>
<span data-ttu-id="37941-127">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="37941-127">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: AddByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37941-128">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="37941-128">-WorkspaceObject</span></span>
<span data-ttu-id="37941-129">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="37941-129">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: AddByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37941-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="37941-130">-Confirm</span></span>
<span data-ttu-id="37941-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="37941-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37941-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37941-132">-WhatIf</span></span>
<span data-ttu-id="37941-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37941-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37941-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="37941-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37941-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37941-135">CommonParameters</span></span>
<span data-ttu-id="37941-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37941-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37941-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37941-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37941-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="37941-138">INPUTS</span></span>

### <span data-ttu-id="37941-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="37941-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="37941-140">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="37941-140">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="37941-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="37941-141">OUTPUTS</span></span>

### <span data-ttu-id="37941-142">System.Object</span><span class="sxs-lookup"><span data-stu-id="37941-142">System.Object</span></span>
## <span data-ttu-id="37941-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="37941-143">NOTES</span></span>

## <span data-ttu-id="37941-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="37941-144">RELATED LINKS</span></span>
