---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/start-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseTrigger.md
ms.openlocfilehash: d2488a99bba1813c192df5ef8561d83c06f2f6e7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221451"
---
# <span data-ttu-id="3d634-101">Start-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="3d634-101">Start-AzSynapseTrigger</span></span>

## <span data-ttu-id="3d634-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3d634-102">SYNOPSIS</span></span>
<span data-ttu-id="3d634-103">Uruchamianie wyzwalacza w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="3d634-103">Starts a trigger in a workspace.</span></span>

## <span data-ttu-id="3d634-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3d634-104">SYNTAX</span></span>

### <span data-ttu-id="3d634-105">StartByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3d634-105">StartByName (Default)</span></span>
```
Start-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d634-106">StartByObject</span><span class="sxs-lookup"><span data-stu-id="3d634-106">StartByObject</span></span>
```
Start-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d634-107">StartByInputObject</span><span class="sxs-lookup"><span data-stu-id="3d634-107">StartByInputObject</span></span>
```
Start-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d634-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3d634-108">DESCRIPTION</span></span>
<span data-ttu-id="3d634-109">Polecenie cmdlet **Start-AzSynapseTrigger** rozpoczyna wyzwalacz w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="3d634-109">The **Start-AzSynapseTrigger** cmdlet starts a trigger in a workspace.</span></span> <span data-ttu-id="3d634-110">Jeśli wyzwalacz jest w stanie "zatrzymany", polecenie cmdlet rozpoczyna wyzwalacz i po pewnym czasie wywoła potoki na podstawie jego definicji.</span><span class="sxs-lookup"><span data-stu-id="3d634-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="3d634-111">Jeśli wyzwalacz jest już w stanie "uruchomiony", to polecenie cmdlet nie ma żadnego wpływu.</span><span class="sxs-lookup"><span data-stu-id="3d634-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span>

## <span data-ttu-id="3d634-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3d634-112">EXAMPLES</span></span>

### <span data-ttu-id="3d634-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3d634-113">Example 1</span></span>
```powershell
PS C:\> Start-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="3d634-114">Uruchamia wyzwalacz o nazwie ContosoTrigger w obszarze roboczym ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="3d634-114">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="3d634-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="3d634-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Start-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="3d634-116">Uruchamia wyzwalacz o nazwie ContosoTrigger w obszarze roboczym ContosoWorkspace za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="3d634-116">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="3d634-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="3d634-117">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Start-AzSynapseTrigger
```

<span data-ttu-id="3d634-118">Uruchamia wyzwalacz o nazwie ContosoTrigger w obszarze roboczym ContosoWorkspace za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="3d634-118">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="3d634-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3d634-119">PARAMETERS</span></span>

### <span data-ttu-id="3d634-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d634-120">-AsJob</span></span>
<span data-ttu-id="3d634-121">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="3d634-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3d634-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d634-122">-DefaultProfile</span></span>
<span data-ttu-id="3d634-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3d634-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d634-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3d634-124">-InputObject</span></span>
<span data-ttu-id="3d634-125">Obiekt Trigger.</span><span class="sxs-lookup"><span data-stu-id="3d634-125">The trigger object.</span></span>

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

### <span data-ttu-id="3d634-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3d634-126">-Name</span></span>
<span data-ttu-id="3d634-127">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="3d634-127">The trigger name.</span></span>

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

### <span data-ttu-id="3d634-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3d634-128">-PassThru</span></span>
<span data-ttu-id="3d634-129">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="3d634-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="3d634-130">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="3d634-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="3d634-131">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="3d634-131">-WorkspaceName</span></span>
<span data-ttu-id="3d634-132">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="3d634-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="3d634-133">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="3d634-133">-WorkspaceObject</span></span>
<span data-ttu-id="3d634-134">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="3d634-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="3d634-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3d634-135">-Confirm</span></span>
<span data-ttu-id="3d634-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d634-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d634-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d634-137">-WhatIf</span></span>
<span data-ttu-id="3d634-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d634-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3d634-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3d634-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d634-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d634-140">CommonParameters</span></span>
<span data-ttu-id="3d634-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d634-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d634-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d634-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d634-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3d634-143">INPUTS</span></span>

### <span data-ttu-id="3d634-144">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3d634-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="3d634-145">Microsoft. Azure. Commands. Synapse. models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="3d634-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="3d634-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3d634-146">OUTPUTS</span></span>

### <span data-ttu-id="3d634-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3d634-147">System.Boolean</span></span>

## <span data-ttu-id="3d634-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3d634-148">NOTES</span></span>

## <span data-ttu-id="3d634-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3d634-149">RELATED LINKS</span></span>
