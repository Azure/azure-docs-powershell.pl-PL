---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsetriggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTriggerSubscription.md
ms.openlocfilehash: ac0606b73145a0d72a5776ede00a24bb802642e7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346078"
---
# <span data-ttu-id="3e841-101">Remove-AzSynapseTriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="3e841-101">Remove-AzSynapseTriggerSubscription</span></span>

## <span data-ttu-id="3e841-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3e841-102">SYNOPSIS</span></span>
<span data-ttu-id="3e841-103">Anulowanie subskrypcji wyzwalacza zdarzeń na zdarzenia usługi zewnętrznej.</span><span class="sxs-lookup"><span data-stu-id="3e841-103">Unsubscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="3e841-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3e841-104">SYNTAX</span></span>

### <span data-ttu-id="3e841-105">RemoveByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3e841-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseTriggerSubscription -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e841-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="3e841-106">RemoveByObject</span></span>
```
Remove-AzSynapseTriggerSubscription -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e841-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="3e841-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseTriggerSubscription -InputObject <PSTriggerResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e841-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3e841-108">DESCRIPTION</span></span>
<span data-ttu-id="3e841-109">Polecenie cmdlet **Remove-AzSynapseTriggerSubscription** powoduje anulowanie subskrypcji wyzwalacza zdarzeń dla określonych zdarzeń usług zewnętrznych z poziomu wyzwalacza defintion.</span><span class="sxs-lookup"><span data-stu-id="3e841-109">The **Remove-AzSynapseTriggerSubscription** cmdlet unsubscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="3e841-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3e841-110">EXAMPLES</span></span>

### <span data-ttu-id="3e841-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3e841-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseTriggerSubscription -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="3e841-112">To polecenie spowoduje anulowanie subskrypcji wyzwalacza o nazwie ContosoTrigger z określonymi zdarzeniami z wyzwalacza defintion.</span><span class="sxs-lookup"><span data-stu-id="3e841-112">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion.</span></span>

### <span data-ttu-id="3e841-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="3e841-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseTriggerSubscription -Name ContosoTrigger
```

<span data-ttu-id="3e841-114">To polecenie spowoduje anulowanie subskrypcji wyzwalacza o nazwie ContosoTrigger do określonych zdarzeń z wyzwalacza defintion za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="3e841-114">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

### <span data-ttu-id="3e841-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="3e841-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Remove-AzSynapseTriggerSubscription
```

<span data-ttu-id="3e841-116">To polecenie spowoduje anulowanie subskrypcji wyzwalacza o nazwie ContosoTrigger do określonych zdarzeń z wyzwalacza defintion za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="3e841-116">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

## <span data-ttu-id="3e841-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3e841-117">PARAMETERS</span></span>

### <span data-ttu-id="3e841-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3e841-118">-AsJob</span></span>
<span data-ttu-id="3e841-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="3e841-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3e841-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e841-120">-DefaultProfile</span></span>
<span data-ttu-id="3e841-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3e841-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e841-122">-Force</span><span class="sxs-lookup"><span data-stu-id="3e841-122">-Force</span></span>
<span data-ttu-id="3e841-123">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3e841-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3e841-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3e841-124">-InputObject</span></span>
<span data-ttu-id="3e841-125">Obiekt Trigger.</span><span class="sxs-lookup"><span data-stu-id="3e841-125">The trigger object.</span></span>

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

### <span data-ttu-id="3e841-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3e841-126">-Name</span></span>
<span data-ttu-id="3e841-127">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="3e841-127">The trigger name.</span></span>

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

### <span data-ttu-id="3e841-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3e841-128">-PassThru</span></span>
<span data-ttu-id="3e841-129">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="3e841-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="3e841-130">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="3e841-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="3e841-131">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="3e841-131">-WorkspaceName</span></span>
<span data-ttu-id="3e841-132">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="3e841-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="3e841-133">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="3e841-133">-WorkspaceObject</span></span>
<span data-ttu-id="3e841-134">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="3e841-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="3e841-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3e841-135">-Confirm</span></span>
<span data-ttu-id="3e841-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e841-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e841-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e841-137">-WhatIf</span></span>
<span data-ttu-id="3e841-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e841-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3e841-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3e841-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e841-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e841-140">CommonParameters</span></span>
<span data-ttu-id="3e841-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e841-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e841-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e841-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e841-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e841-143">INPUTS</span></span>

### <span data-ttu-id="3e841-144">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3e841-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="3e841-145">Microsoft. Azure. Commands. Synapse. models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="3e841-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="3e841-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3e841-146">OUTPUTS</span></span>

### <span data-ttu-id="3e841-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3e841-147">System.Boolean</span></span>

## <span data-ttu-id="3e841-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3e841-148">NOTES</span></span>

## <span data-ttu-id="3e841-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3e841-149">RELATED LINKS</span></span>
