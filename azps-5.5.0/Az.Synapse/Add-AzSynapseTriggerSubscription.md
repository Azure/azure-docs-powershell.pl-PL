---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/add-azsynapsetriggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
ms.openlocfilehash: ca5501115b7c75b2e3c1baca368ebaac841e0ae1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182810"
---
# <span data-ttu-id="969d9-101">Add-AzSynapseTriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="969d9-101">Add-AzSynapseTriggerSubscription</span></span>

## <span data-ttu-id="969d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="969d9-102">SYNOPSIS</span></span>
<span data-ttu-id="969d9-103">Zasubskrybuj wyzwalacz zdarzenia zdarzenia w usłudze zewnętrznej.</span><span class="sxs-lookup"><span data-stu-id="969d9-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="969d9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="969d9-104">SYNTAX</span></span>

### <span data-ttu-id="969d9-105">AddByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="969d9-105">AddByName (Default)</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceName <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="969d9-106">AddByObject</span><span class="sxs-lookup"><span data-stu-id="969d9-106">AddByObject</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="969d9-107">AddByInputObject</span><span class="sxs-lookup"><span data-stu-id="969d9-107">AddByInputObject</span></span>
```
Add-AzSynapseTriggerSubscription -InputObject <PSTriggerResource> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="969d9-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="969d9-108">DESCRIPTION</span></span>
<span data-ttu-id="969d9-109">Polecenie **cmdlet Add-AzSynapseTriggerSubscription** subskrybuje wyzwalacz zdarzenia określonym zdarzeniami usługi zewnętrznej z definicji wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="969d9-109">The **Add-AzSynapseTriggerSubscription** cmdlet subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="969d9-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="969d9-110">EXAMPLES</span></span>

### <span data-ttu-id="969d9-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="969d9-111">Example 1</span></span>
```powershell
PS C:\> Add-AzSynapseTriggerSubscription -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="969d9-112">To polecenie subskrybuje wyzwalacz o nazwie ContosoTrigger do określonych zdarzeń z definicji wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="969d9-112">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion.</span></span>

### <span data-ttu-id="969d9-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="969d9-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Add-AzSynapseTriggerSubscription -Name ContosoTrigger
```

<span data-ttu-id="969d9-114">To polecenie zasubskrybuje wyzwalacz o nazwie ContosoTrigger do określonych zdarzeń z definicji wyzwalacza za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="969d9-114">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

### <span data-ttu-id="969d9-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="969d9-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Add-AzSynapseTriggerSubscription
```

<span data-ttu-id="969d9-116">To polecenie subskrybuje wyzwalacz o nazwie ContosoTrigger do określonych zdarzeń z definicji wyzwalacza za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="969d9-116">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

## <span data-ttu-id="969d9-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="969d9-117">PARAMETERS</span></span>

### <span data-ttu-id="969d9-118">— AsJob</span><span class="sxs-lookup"><span data-stu-id="969d9-118">-AsJob</span></span>
<span data-ttu-id="969d9-119">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="969d9-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="969d9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="969d9-120">-DefaultProfile</span></span>
<span data-ttu-id="969d9-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="969d9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="969d9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="969d9-122">-InputObject</span></span>
<span data-ttu-id="969d9-123">Obiekt wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="969d9-123">The trigger object.</span></span>

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

### <span data-ttu-id="969d9-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="969d9-124">-Name</span></span>
<span data-ttu-id="969d9-125">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="969d9-125">The trigger name.</span></span>

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

### <span data-ttu-id="969d9-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="969d9-126">-WorkspaceName</span></span>
<span data-ttu-id="969d9-127">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="969d9-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="969d9-128">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="969d9-128">-WorkspaceObject</span></span>
<span data-ttu-id="969d9-129">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="969d9-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="969d9-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="969d9-130">-Confirm</span></span>
<span data-ttu-id="969d9-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="969d9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="969d9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="969d9-132">-WhatIf</span></span>
<span data-ttu-id="969d9-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="969d9-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="969d9-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="969d9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="969d9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="969d9-135">CommonParameters</span></span>
<span data-ttu-id="969d9-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="969d9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="969d9-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="969d9-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="969d9-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="969d9-138">INPUTS</span></span>

### <span data-ttu-id="969d9-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="969d9-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="969d9-140">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="969d9-140">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="969d9-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="969d9-141">OUTPUTS</span></span>

### <span data-ttu-id="969d9-142">System.Object</span><span class="sxs-lookup"><span data-stu-id="969d9-142">System.Object</span></span>
## <span data-ttu-id="969d9-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="969d9-143">NOTES</span></span>

## <span data-ttu-id="969d9-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="969d9-144">RELATED LINKS</span></span>
