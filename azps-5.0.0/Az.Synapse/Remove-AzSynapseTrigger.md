---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTrigger.md
ms.openlocfilehash: 0882789e230c012fe9f23dcdbeeb5378e9b91781
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94231605"
---
# <span data-ttu-id="77e7c-101">Remove-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="77e7c-101">Remove-AzSynapseTrigger</span></span>

## <span data-ttu-id="77e7c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="77e7c-102">SYNOPSIS</span></span>
<span data-ttu-id="77e7c-103">Usuwa wyzwalacz z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="77e7c-103">Removes a trigger from a workspace.</span></span>

## <span data-ttu-id="77e7c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="77e7c-104">SYNTAX</span></span>

### <span data-ttu-id="77e7c-105">RemoveByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="77e7c-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77e7c-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="77e7c-106">RemoveByObject</span></span>
```
Remove-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77e7c-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="77e7c-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77e7c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="77e7c-108">DESCRIPTION</span></span>
<span data-ttu-id="77e7c-109">Polecenie cmdlet **Remove-AzSynapseTrigger** usuwa wyzwalacz z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="77e7c-109">The **Remove-AzSynapseTrigger** cmdlet removes a trigger from a workspace.</span></span>

## <span data-ttu-id="77e7c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="77e7c-110">EXAMPLES</span></span>

### <span data-ttu-id="77e7c-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="77e7c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="77e7c-112">Usuwanie wyzwalacza o nazwie ContosoTrigger z obszaru roboczego ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="77e7c-112">Remove a trigger called ContosoTrigger from the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="77e7c-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="77e7c-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="77e7c-114">Usuwanie wyzwalacza o nazwie ContosoTrigger z obszaru roboczego ContosoWorkspace za pomocą rurociągu.</span><span class="sxs-lookup"><span data-stu-id="77e7c-114">Remove a trigger called ContosoTrigger from the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="77e7c-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="77e7c-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Remove-AzSynapseTrigger
```

<span data-ttu-id="77e7c-116">Usuwanie wyzwalacza o nazwie ContosoTrigger z obszaru roboczego ContosoWorkspace za pomocą rurociągu.</span><span class="sxs-lookup"><span data-stu-id="77e7c-116">Remove a trigger called ContosoTrigger from the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="77e7c-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="77e7c-117">PARAMETERS</span></span>

### <span data-ttu-id="77e7c-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="77e7c-118">-AsJob</span></span>
<span data-ttu-id="77e7c-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="77e7c-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="77e7c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77e7c-120">-DefaultProfile</span></span>
<span data-ttu-id="77e7c-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="77e7c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77e7c-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="77e7c-122">-InputObject</span></span>
<span data-ttu-id="77e7c-123">Obiekt Trigger.</span><span class="sxs-lookup"><span data-stu-id="77e7c-123">The trigger object.</span></span>

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

### <span data-ttu-id="77e7c-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="77e7c-124">-Name</span></span>
<span data-ttu-id="77e7c-125">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="77e7c-125">The trigger name.</span></span>

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

### <span data-ttu-id="77e7c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="77e7c-126">-PassThru</span></span>
<span data-ttu-id="77e7c-127">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="77e7c-127">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="77e7c-128">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="77e7c-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="77e7c-129">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="77e7c-129">-WorkspaceName</span></span>
<span data-ttu-id="77e7c-130">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="77e7c-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="77e7c-131">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="77e7c-131">-WorkspaceObject</span></span>
<span data-ttu-id="77e7c-132">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="77e7c-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="77e7c-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="77e7c-133">-Confirm</span></span>
<span data-ttu-id="77e7c-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77e7c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77e7c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77e7c-135">-WhatIf</span></span>
<span data-ttu-id="77e7c-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77e7c-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="77e7c-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="77e7c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77e7c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77e7c-138">CommonParameters</span></span>
<span data-ttu-id="77e7c-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77e7c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77e7c-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77e7c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77e7c-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="77e7c-141">INPUTS</span></span>

### <span data-ttu-id="77e7c-142">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="77e7c-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="77e7c-143">Microsoft. Azure. Commands. Synapse. models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="77e7c-143">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="77e7c-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="77e7c-144">OUTPUTS</span></span>

### <span data-ttu-id="77e7c-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="77e7c-145">System.Boolean</span></span>

## <span data-ttu-id="77e7c-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="77e7c-146">NOTES</span></span>

## <span data-ttu-id="77e7c-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="77e7c-147">RELATED LINKS</span></span>
