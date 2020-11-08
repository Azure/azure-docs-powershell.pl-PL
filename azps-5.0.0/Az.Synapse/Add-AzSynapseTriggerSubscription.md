---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/add-azsynapsetriggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
ms.openlocfilehash: ca5501115b7c75b2e3c1baca368ebaac841e0ae1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232435"
---
# <span data-ttu-id="dbec6-101">Add-AzSynapseTriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="dbec6-101">Add-AzSynapseTriggerSubscription</span></span>

## <span data-ttu-id="dbec6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dbec6-102">SYNOPSIS</span></span>
<span data-ttu-id="dbec6-103">Zasubskrybuj wyzwalacz zdarzeń na zdarzenia usługi zewnętrznej.</span><span class="sxs-lookup"><span data-stu-id="dbec6-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="dbec6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dbec6-104">SYNTAX</span></span>

### <span data-ttu-id="dbec6-105">AddByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="dbec6-105">AddByName (Default)</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceName <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbec6-106">AddByObject</span><span class="sxs-lookup"><span data-stu-id="dbec6-106">AddByObject</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbec6-107">AddByInputObject</span><span class="sxs-lookup"><span data-stu-id="dbec6-107">AddByInputObject</span></span>
```
Add-AzSynapseTriggerSubscription -InputObject <PSTriggerResource> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbec6-108">Opis</span><span class="sxs-lookup"><span data-stu-id="dbec6-108">DESCRIPTION</span></span>
<span data-ttu-id="dbec6-109">Polecenie cmdlet **Add-AzSynapseTriggerSubscription** umożliwia zasubskrybowanie wyzwalacza zdarzeń do określonych zdarzeń usług zewnętrznych z poziomu wyzwalacza defintion.</span><span class="sxs-lookup"><span data-stu-id="dbec6-109">The **Add-AzSynapseTriggerSubscription** cmdlet subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="dbec6-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dbec6-110">EXAMPLES</span></span>

### <span data-ttu-id="dbec6-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dbec6-111">Example 1</span></span>
```powershell
PS C:\> Add-AzSynapseTriggerSubscription -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="dbec6-112">To polecenie spowoduje zasubskrybowanie wyzwalacza o nazwie ContosoTrigger do określonych zdarzeń z poziomu wyzwalacza defintion.</span><span class="sxs-lookup"><span data-stu-id="dbec6-112">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion.</span></span>

### <span data-ttu-id="dbec6-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="dbec6-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Add-AzSynapseTriggerSubscription -Name ContosoTrigger
```

<span data-ttu-id="dbec6-114">To polecenie spowoduje zasubskrybowanie wyzwalacza o nazwie ContosoTrigger do określonych zdarzeń z wyzwalacza defintion za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="dbec6-114">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

### <span data-ttu-id="dbec6-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="dbec6-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Add-AzSynapseTriggerSubscription
```

<span data-ttu-id="dbec6-116">To polecenie spowoduje zasubskrybowanie wyzwalacza o nazwie ContosoTrigger do określonych zdarzeń z wyzwalacza defintion za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="dbec6-116">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

## <span data-ttu-id="dbec6-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dbec6-117">PARAMETERS</span></span>

### <span data-ttu-id="dbec6-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dbec6-118">-AsJob</span></span>
<span data-ttu-id="dbec6-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="dbec6-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dbec6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbec6-120">-DefaultProfile</span></span>
<span data-ttu-id="dbec6-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dbec6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbec6-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="dbec6-122">-InputObject</span></span>
<span data-ttu-id="dbec6-123">Obiekt Trigger.</span><span class="sxs-lookup"><span data-stu-id="dbec6-123">The trigger object.</span></span>

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

### <span data-ttu-id="dbec6-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dbec6-124">-Name</span></span>
<span data-ttu-id="dbec6-125">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="dbec6-125">The trigger name.</span></span>

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

### <span data-ttu-id="dbec6-126">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="dbec6-126">-WorkspaceName</span></span>
<span data-ttu-id="dbec6-127">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="dbec6-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="dbec6-128">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="dbec6-128">-WorkspaceObject</span></span>
<span data-ttu-id="dbec6-129">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="dbec6-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="dbec6-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dbec6-130">-Confirm</span></span>
<span data-ttu-id="dbec6-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbec6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbec6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbec6-132">-WhatIf</span></span>
<span data-ttu-id="dbec6-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbec6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbec6-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dbec6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbec6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbec6-135">CommonParameters</span></span>
<span data-ttu-id="dbec6-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbec6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbec6-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dbec6-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbec6-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dbec6-138">INPUTS</span></span>

### <span data-ttu-id="dbec6-139">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="dbec6-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="dbec6-140">Microsoft. Azure. Commands. Synapse. models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="dbec6-140">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="dbec6-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dbec6-141">OUTPUTS</span></span>

### <span data-ttu-id="dbec6-142">System. Object</span><span class="sxs-lookup"><span data-stu-id="dbec6-142">System.Object</span></span>
## <span data-ttu-id="dbec6-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dbec6-143">NOTES</span></span>

## <span data-ttu-id="dbec6-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dbec6-144">RELATED LINKS</span></span>
