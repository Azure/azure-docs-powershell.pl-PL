---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsetriggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTriggerSubscription.md
ms.openlocfilehash: ac0606b73145a0d72a5776ede00a24bb802642e7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190579"
---
# <span data-ttu-id="4d8b3-101">Remove-AzSynapseTriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="4d8b3-101">Remove-AzSynapseTriggerSubscription</span></span>

## <span data-ttu-id="4d8b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d8b3-102">SYNOPSIS</span></span>
<span data-ttu-id="4d8b3-103">Anulowanie anulowania wyzwalacza zdarzenia w usłudze zewnętrznej.</span><span class="sxs-lookup"><span data-stu-id="4d8b3-103">Unsubscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="4d8b3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4d8b3-104">SYNTAX</span></span>

### <span data-ttu-id="4d8b3-105">RemoveByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="4d8b3-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseTriggerSubscription -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d8b3-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="4d8b3-106">RemoveByObject</span></span>
```
Remove-AzSynapseTriggerSubscription -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d8b3-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="4d8b3-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseTriggerSubscription -InputObject <PSTriggerResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d8b3-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="4d8b3-108">DESCRIPTION</span></span>
<span data-ttu-id="4d8b3-109">Polecenie **cmdlet Remove-AzSynapseTriggerSubscription** anuluje subskrypcję wyzwalacza zdarzenia na określone zdarzenia usługi zewnętrznej z definicji wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="4d8b3-109">The **Remove-AzSynapseTriggerSubscription** cmdlet unsubscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="4d8b3-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4d8b3-110">EXAMPLES</span></span>

### <span data-ttu-id="4d8b3-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4d8b3-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseTriggerSubscription -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="4d8b3-112">To polecenie anuluje subskrypcję wyzwalacza o nazwie ContosoTrigger dla określonych zdarzeń w definicji wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="4d8b3-112">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion.</span></span>

### <span data-ttu-id="4d8b3-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="4d8b3-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseTriggerSubscription -Name ContosoTrigger
```

<span data-ttu-id="4d8b3-114">To polecenie anuluje subskrypcję wyzwalacza o nazwie ContosoTrigger dla określonych zdarzeń w ramach definicji wyzwalacza za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="4d8b3-114">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

### <span data-ttu-id="4d8b3-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="4d8b3-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Remove-AzSynapseTriggerSubscription
```

<span data-ttu-id="4d8b3-116">To polecenie anuluje subskrypcję wyzwalacza o nazwie ContosoTrigger dla określonych zdarzeń w ramach definicji wyzwalacza za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="4d8b3-116">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

## <span data-ttu-id="4d8b3-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d8b3-117">PARAMETERS</span></span>

### <span data-ttu-id="4d8b3-118">— AsJob</span><span class="sxs-lookup"><span data-stu-id="4d8b3-118">-AsJob</span></span>
<span data-ttu-id="4d8b3-119">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="4d8b3-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4d8b3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d8b3-120">-DefaultProfile</span></span>
<span data-ttu-id="4d8b3-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4d8b3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d8b3-122">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="4d8b3-122">-Force</span></span>
<span data-ttu-id="4d8b3-123">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4d8b3-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4d8b3-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d8b3-124">-InputObject</span></span>
<span data-ttu-id="4d8b3-125">Obiekt wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="4d8b3-125">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d8b3-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4d8b3-126">-Name</span></span>
<span data-ttu-id="4d8b3-127">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="4d8b3-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d8b3-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4d8b3-128">-PassThru</span></span>
<span data-ttu-id="4d8b3-129">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="4d8b3-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="4d8b3-130">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="4d8b3-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="4d8b3-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4d8b3-131">-WorkspaceName</span></span>
<span data-ttu-id="4d8b3-132">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="4d8b3-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="4d8b3-133">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="4d8b3-133">-WorkspaceObject</span></span>
<span data-ttu-id="4d8b3-134">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="4d8b3-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="4d8b3-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4d8b3-135">-Confirm</span></span>
<span data-ttu-id="4d8b3-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4d8b3-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d8b3-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d8b3-137">-WhatIf</span></span>
<span data-ttu-id="4d8b3-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d8b3-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4d8b3-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4d8b3-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d8b3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d8b3-140">CommonParameters</span></span>
<span data-ttu-id="4d8b3-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d8b3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d8b3-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4d8b3-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d8b3-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d8b3-143">INPUTS</span></span>

### <span data-ttu-id="4d8b3-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4d8b3-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="4d8b3-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="4d8b3-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="4d8b3-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d8b3-146">OUTPUTS</span></span>

### <span data-ttu-id="4d8b3-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4d8b3-147">System.Boolean</span></span>

## <span data-ttu-id="4d8b3-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4d8b3-148">NOTES</span></span>

## <span data-ttu-id="4d8b3-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4d8b3-149">RELATED LINKS</span></span>
