---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseTrigger.md
ms.openlocfilehash: 289e601ab80e4842b493cd6852839bec544bcc36
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358458"
---
# <span data-ttu-id="544d7-101">Set-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="544d7-101">Set-AzSynapseTrigger</span></span>

## <span data-ttu-id="544d7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="544d7-102">SYNOPSIS</span></span>
<span data-ttu-id="544d7-103">Tworzy wyzwalacz w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="544d7-103">Creates a trigger in a workspace.</span></span>

## <span data-ttu-id="544d7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="544d7-104">SYNTAX</span></span>

### <span data-ttu-id="544d7-105">SetByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="544d7-105">SetByName (Default)</span></span>
```
Set-AzSynapseTrigger -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="544d7-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="544d7-106">SetByObject</span></span>
```
Set-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="544d7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="544d7-107">DESCRIPTION</span></span>
<span data-ttu-id="544d7-108">Polecenie cmdlet **Set-AzSynapseTrigger** tworzy wyzwalacz w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="544d7-108">The **Set-AzSynapseTrigger** cmdlet creates a trigger in a workspace.</span></span> <span data-ttu-id="544d7-109">Wyzwalacze są tworzone w stanie "zatrzymane", co oznacza, że nie zaczynają od razu rozpoczynać od siebie potoków, do których się odwołują.</span><span class="sxs-lookup"><span data-stu-id="544d7-109">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="544d7-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="544d7-110">EXAMPLES</span></span>

### <span data-ttu-id="544d7-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="544d7-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger -DefinitionFile ".\scheduledTrigger.json"
```

<span data-ttu-id="544d7-112">Tworzenie nowego wyzwalacza o nazwie ContosoTrigger w obszarze roboczym ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="544d7-112">Create a new trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span> <span data-ttu-id="544d7-113">Wyzwalacz jest tworzony w stanie "zatrzymane", co oznacza, że nie jest od razu uruchomiony.</span><span class="sxs-lookup"><span data-stu-id="544d7-113">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="544d7-114">Wyzwalacz można uruchomić przy użyciu `Start-AzDataFactoryV2Trigger` polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="544d7-114">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

### <span data-ttu-id="544d7-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="544d7-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseTrigger -Name ContosoTrigger -DefinitionFile ".\scheduledTrigger.json"
```

<span data-ttu-id="544d7-116">Tworzenie nowego wyzwalacza o nazwie ContosoTrigger w obszarze roboczym ContosoWorkspace za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="544d7-116">Create a new trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span> <span data-ttu-id="544d7-117">Wyzwalacz jest tworzony w stanie "zatrzymane", co oznacza, że nie jest od razu uruchomiony.</span><span class="sxs-lookup"><span data-stu-id="544d7-117">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="544d7-118">Wyzwalacz można uruchomić przy użyciu `Start-AzDataFactoryV2Trigger` polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="544d7-118">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="544d7-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="544d7-119">PARAMETERS</span></span>

### <span data-ttu-id="544d7-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="544d7-120">-AsJob</span></span>
<span data-ttu-id="544d7-121">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="544d7-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="544d7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="544d7-122">-DefaultProfile</span></span>
<span data-ttu-id="544d7-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="544d7-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="544d7-124">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="544d7-124">-DefinitionFile</span></span>
<span data-ttu-id="544d7-125">Ścieżka pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="544d7-125">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="544d7-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="544d7-126">-Name</span></span>
<span data-ttu-id="544d7-127">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="544d7-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="544d7-128">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="544d7-128">-WorkspaceName</span></span>
<span data-ttu-id="544d7-129">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="544d7-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="544d7-130">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="544d7-130">-WorkspaceObject</span></span>
<span data-ttu-id="544d7-131">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="544d7-131">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="544d7-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="544d7-132">-Confirm</span></span>
<span data-ttu-id="544d7-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="544d7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="544d7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="544d7-134">-WhatIf</span></span>
<span data-ttu-id="544d7-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="544d7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="544d7-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="544d7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="544d7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="544d7-137">CommonParameters</span></span>
<span data-ttu-id="544d7-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="544d7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="544d7-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="544d7-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="544d7-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="544d7-140">INPUTS</span></span>

### <span data-ttu-id="544d7-141">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="544d7-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="544d7-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="544d7-142">OUTPUTS</span></span>

### <span data-ttu-id="544d7-143">Microsoft. Azure. Commands. Synapse. models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="544d7-143">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="544d7-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="544d7-144">NOTES</span></span>

## <span data-ttu-id="544d7-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="544d7-145">RELATED LINKS</span></span>
