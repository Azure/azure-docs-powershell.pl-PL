---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseTrigger.md
ms.openlocfilehash: 4e35814be14c2be3b5ba0fd1ca5960d297590dca
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327409"
---
# <span data-ttu-id="429c6-101">Stop-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="429c6-101">Stop-AzSynapseTrigger</span></span>

## <span data-ttu-id="429c6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="429c6-102">SYNOPSIS</span></span>
<span data-ttu-id="429c6-103">Zatrzymuje wyzwalacz w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="429c6-103">Stops a trigger in a workspace.</span></span>

## <span data-ttu-id="429c6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="429c6-104">SYNTAX</span></span>

### <span data-ttu-id="429c6-105">StopByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="429c6-105">StopByName (Default)</span></span>
```
Stop-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="429c6-106">StopByObject</span><span class="sxs-lookup"><span data-stu-id="429c6-106">StopByObject</span></span>
```
Stop-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="429c6-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="429c6-107">StopByInputObject</span></span>
```
Stop-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="429c6-108">Opis</span><span class="sxs-lookup"><span data-stu-id="429c6-108">DESCRIPTION</span></span>
<span data-ttu-id="429c6-109">Polecenie cmdlet **stop-AzSynapseTrigger** zatrzymuje wyzwalacz w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="429c6-109">The **Stop-AzSynapseTrigger** cmdlet stops a trigger in a workspace.</span></span> <span data-ttu-id="429c6-110">Jeśli wyzwalacz jest w stanie "uruchomiony", polecenie cmdlet zatrzymuje wyzwalacz i nie wywoła już potoków.</span><span class="sxs-lookup"><span data-stu-id="429c6-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="429c6-111">Jeśli wyzwalacz jest już w stanie "zatrzymany", to polecenie cmdlet nie ma żadnego wpływu.</span><span class="sxs-lookup"><span data-stu-id="429c6-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span>

## <span data-ttu-id="429c6-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="429c6-112">EXAMPLES</span></span>

### <span data-ttu-id="429c6-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="429c6-113">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="429c6-114">Zatrzymuje wyzwalacz o nazwie ContosoTrigger w obszarze roboczym ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="429c6-114">Stops a trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="429c6-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="429c6-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Stop-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="429c6-116">Zatrzymuje wyzwalacz o nazwie ContosoTrigger w obszarze roboczym ContosoWorkspace za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="429c6-116">Stops a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="429c6-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="429c6-117">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Stop-AzSynapseTrigger
```

<span data-ttu-id="429c6-118">Zatrzymanie wyzwalacza o nazwie ContosoTrigger w obszarze roboczym ContosoWorkspace za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="429c6-118">Stop a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="429c6-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="429c6-119">PARAMETERS</span></span>

### <span data-ttu-id="429c6-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="429c6-120">-AsJob</span></span>
<span data-ttu-id="429c6-121">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="429c6-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="429c6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="429c6-122">-DefaultProfile</span></span>
<span data-ttu-id="429c6-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="429c6-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="429c6-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="429c6-124">-InputObject</span></span>
<span data-ttu-id="429c6-125">Obiekt Trigger.</span><span class="sxs-lookup"><span data-stu-id="429c6-125">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: StopByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="429c6-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="429c6-126">-Name</span></span>
<span data-ttu-id="429c6-127">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="429c6-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByName, StopByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="429c6-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="429c6-128">-PassThru</span></span>
<span data-ttu-id="429c6-129">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="429c6-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="429c6-130">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="429c6-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="429c6-131">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="429c6-131">-WorkspaceName</span></span>
<span data-ttu-id="429c6-132">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="429c6-132">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="429c6-133">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="429c6-133">-WorkspaceObject</span></span>
<span data-ttu-id="429c6-134">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="429c6-134">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: StopByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="429c6-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="429c6-135">-Confirm</span></span>
<span data-ttu-id="429c6-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="429c6-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="429c6-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="429c6-137">-WhatIf</span></span>
<span data-ttu-id="429c6-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="429c6-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="429c6-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="429c6-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="429c6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="429c6-140">CommonParameters</span></span>
<span data-ttu-id="429c6-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="429c6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="429c6-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="429c6-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="429c6-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="429c6-143">INPUTS</span></span>

### <span data-ttu-id="429c6-144">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="429c6-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="429c6-145">Microsoft. Azure. Commands. Synapse. models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="429c6-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="429c6-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="429c6-146">OUTPUTS</span></span>

### <span data-ttu-id="429c6-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="429c6-147">System.Boolean</span></span>

## <span data-ttu-id="429c6-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="429c6-148">NOTES</span></span>

## <span data-ttu-id="429c6-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="429c6-149">RELATED LINKS</span></span>
