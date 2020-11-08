---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapsePipeline.md
ms.openlocfilehash: f28abbca41c68ce08e516fb52f69b7de8c54e67a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232396"
---
# <span data-ttu-id="2aa11-101">Remove-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="2aa11-101">Remove-AzSynapsePipeline</span></span>

## <span data-ttu-id="2aa11-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2aa11-102">SYNOPSIS</span></span>
<span data-ttu-id="2aa11-103">Usuwa potok z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="2aa11-103">Removes a pipeline from workspace.</span></span>

## <span data-ttu-id="2aa11-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2aa11-104">SYNTAX</span></span>

### <span data-ttu-id="2aa11-105">RemoveByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2aa11-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapsePipeline -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2aa11-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="2aa11-106">RemoveByObject</span></span>
```
Remove-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2aa11-107">NewByInputObject</span><span class="sxs-lookup"><span data-stu-id="2aa11-107">NewByInputObject</span></span>
```
Remove-AzSynapsePipeline -Name <String> -InputObject <PSPipelineResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2aa11-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2aa11-108">DESCRIPTION</span></span>
<span data-ttu-id="2aa11-109">Polecenie cmdlet **Remove-AzSynapsePipeline** usuwa potok z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="2aa11-109">The **Remove-AzSynapsePipeline** cmdlet removes a pipeline from workspace.</span></span>

## <span data-ttu-id="2aa11-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2aa11-110">EXAMPLES</span></span>

### <span data-ttu-id="2aa11-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2aa11-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
```

<span data-ttu-id="2aa11-112">To polecenie cmdlet usuwa potok o nazwie ContosoPipeline z obszaru roboczego o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="2aa11-112">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="2aa11-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="2aa11-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapsePipeline -Name ContosoPipeline
```

<span data-ttu-id="2aa11-114">To polecenie cmdlet usuwa potok o nazwie ContosoPipeline z obszaru roboczego o nazwie ContosoWorkspace za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="2aa11-114">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="2aa11-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="2aa11-115">Example 3</span></span>
```powershell
PS C:\> $pipeline = Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
PS C:\> $pipeline | Remove-AzSynapsePipeline
```

<span data-ttu-id="2aa11-116">To polecenie cmdlet usuwa potok o nazwie ContosoPipeline z obszaru roboczego o nazwie ContosoWorkspace za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="2aa11-116">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="2aa11-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2aa11-117">PARAMETERS</span></span>

### <span data-ttu-id="2aa11-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2aa11-118">-AsJob</span></span>
<span data-ttu-id="2aa11-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="2aa11-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2aa11-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aa11-120">-DefaultProfile</span></span>
<span data-ttu-id="2aa11-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2aa11-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2aa11-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2aa11-122">-InputObject</span></span>
<span data-ttu-id="2aa11-123">Obiekt potokowy.</span><span class="sxs-lookup"><span data-stu-id="2aa11-123">The pipeline object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource
Parameter Sets: NewByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2aa11-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2aa11-124">-Name</span></span>
<span data-ttu-id="2aa11-125">Nazwa potoku.</span><span class="sxs-lookup"><span data-stu-id="2aa11-125">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aa11-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2aa11-126">-PassThru</span></span>
<span data-ttu-id="2aa11-127">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="2aa11-127">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="2aa11-128">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="2aa11-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="2aa11-129">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="2aa11-129">-WorkspaceName</span></span>
<span data-ttu-id="2aa11-130">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="2aa11-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="2aa11-131">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="2aa11-131">-WorkspaceObject</span></span>
<span data-ttu-id="2aa11-132">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="2aa11-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="2aa11-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2aa11-133">-Confirm</span></span>
<span data-ttu-id="2aa11-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2aa11-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2aa11-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2aa11-135">-WhatIf</span></span>
<span data-ttu-id="2aa11-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2aa11-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2aa11-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2aa11-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2aa11-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aa11-138">CommonParameters</span></span>
<span data-ttu-id="2aa11-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2aa11-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aa11-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2aa11-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aa11-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2aa11-141">INPUTS</span></span>

### <span data-ttu-id="2aa11-142">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2aa11-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="2aa11-143">Microsoft. Azure. Commands. Synapse. models. PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="2aa11-143">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="2aa11-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2aa11-144">OUTPUTS</span></span>

### <span data-ttu-id="2aa11-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2aa11-145">System.Boolean</span></span>

## <span data-ttu-id="2aa11-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2aa11-146">NOTES</span></span>

## <span data-ttu-id="2aa11-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2aa11-147">RELATED LINKS</span></span>
