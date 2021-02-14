---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseTrigger.md
ms.openlocfilehash: 4e35814be14c2be3b5ba0fd1ca5960d297590dca
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197307"
---
# <span data-ttu-id="30524-101">Stop-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="30524-101">Stop-AzSynapseTrigger</span></span>

## <span data-ttu-id="30524-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30524-102">SYNOPSIS</span></span>
<span data-ttu-id="30524-103">Powoduje zatrzymanie wyzwalacza w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="30524-103">Stops a trigger in a workspace.</span></span>

## <span data-ttu-id="30524-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="30524-104">SYNTAX</span></span>

### <span data-ttu-id="30524-105">StopByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="30524-105">StopByName (Default)</span></span>
```
Stop-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30524-106">StopByObject</span><span class="sxs-lookup"><span data-stu-id="30524-106">StopByObject</span></span>
```
Stop-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30524-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="30524-107">StopByInputObject</span></span>
```
Stop-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30524-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="30524-108">DESCRIPTION</span></span>
<span data-ttu-id="30524-109">Polecenie **cmdlet Stop-AzSynapseTrigger** powoduje zatrzymanie wyzwalacza w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="30524-109">The **Stop-AzSynapseTrigger** cmdlet stops a trigger in a workspace.</span></span> <span data-ttu-id="30524-110">Jeśli wyzwalacz znajduje się w stanie "Uruchomiona", polecenie cmdlet zatrzyma wyzwalacz i nie będzie już wywoływać potoków.</span><span class="sxs-lookup"><span data-stu-id="30524-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="30524-111">Jeśli wyzwalacz znajduje się już w stanie "Zatrzymano", to polecenie cmdlet nie ma wpływu.</span><span class="sxs-lookup"><span data-stu-id="30524-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span>

## <span data-ttu-id="30524-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="30524-112">EXAMPLES</span></span>

### <span data-ttu-id="30524-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="30524-113">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="30524-114">Powoduje zatrzymanie wyzwalacza o nazwie ContosoTrigger w obszarze roboczym ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="30524-114">Stops a trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="30524-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="30524-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Stop-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="30524-116">Powoduje zatrzymanie wyzwalacza o nazwie ContosoTrigger w obszarze roboczym ContosoWorkspace w potoku.</span><span class="sxs-lookup"><span data-stu-id="30524-116">Stops a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="30524-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="30524-117">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Stop-AzSynapseTrigger
```

<span data-ttu-id="30524-118">Zatrzymanie wyzwalacza o nazwie ContosoTrigger w obszarze roboczym ContosoWorkspace przez potok.</span><span class="sxs-lookup"><span data-stu-id="30524-118">Stop a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="30524-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30524-119">PARAMETERS</span></span>

### <span data-ttu-id="30524-120">— AsJob</span><span class="sxs-lookup"><span data-stu-id="30524-120">-AsJob</span></span>
<span data-ttu-id="30524-121">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="30524-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="30524-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30524-122">-DefaultProfile</span></span>
<span data-ttu-id="30524-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="30524-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30524-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="30524-124">-InputObject</span></span>
<span data-ttu-id="30524-125">Obiekt wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="30524-125">The trigger object.</span></span>

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

### <span data-ttu-id="30524-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="30524-126">-Name</span></span>
<span data-ttu-id="30524-127">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="30524-127">The trigger name.</span></span>

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

### <span data-ttu-id="30524-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="30524-128">-PassThru</span></span>
<span data-ttu-id="30524-129">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="30524-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="30524-130">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="30524-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="30524-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="30524-131">-WorkspaceName</span></span>
<span data-ttu-id="30524-132">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="30524-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="30524-133">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="30524-133">-WorkspaceObject</span></span>
<span data-ttu-id="30524-134">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="30524-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="30524-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="30524-135">-Confirm</span></span>
<span data-ttu-id="30524-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="30524-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30524-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30524-137">-WhatIf</span></span>
<span data-ttu-id="30524-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30524-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="30524-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="30524-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30524-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30524-140">CommonParameters</span></span>
<span data-ttu-id="30524-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30524-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30524-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30524-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30524-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="30524-143">INPUTS</span></span>

### <span data-ttu-id="30524-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="30524-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="30524-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="30524-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="30524-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="30524-146">OUTPUTS</span></span>

### <span data-ttu-id="30524-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="30524-147">System.Boolean</span></span>

## <span data-ttu-id="30524-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="30524-148">NOTES</span></span>

## <span data-ttu-id="30524-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="30524-149">RELATED LINKS</span></span>
