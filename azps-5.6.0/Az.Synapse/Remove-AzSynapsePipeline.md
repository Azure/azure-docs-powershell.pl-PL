---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapsePipeline.md
ms.openlocfilehash: b7bd7866ec6c6ff41a6ef7474b71cfc880e28f49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981802"
---
# <span data-ttu-id="4efef-101">Remove-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="4efef-101">Remove-AzSynapsePipeline</span></span>

## <span data-ttu-id="4efef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4efef-102">SYNOPSIS</span></span>
<span data-ttu-id="4efef-103">Usuwa potok z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="4efef-103">Removes a pipeline from workspace.</span></span>

## <span data-ttu-id="4efef-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4efef-104">SYNTAX</span></span>

### <span data-ttu-id="4efef-105">RemoveByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="4efef-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapsePipeline -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4efef-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="4efef-106">RemoveByObject</span></span>
```
Remove-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4efef-107">NewByInputObject</span><span class="sxs-lookup"><span data-stu-id="4efef-107">NewByInputObject</span></span>
```
Remove-AzSynapsePipeline -Name <String> -InputObject <PSPipelineResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4efef-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="4efef-108">DESCRIPTION</span></span>
<span data-ttu-id="4efef-109">Polecenie **cmdlet Remove-AzSynapsePipeline** usuwa potok z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="4efef-109">The **Remove-AzSynapsePipeline** cmdlet removes a pipeline from workspace.</span></span>

## <span data-ttu-id="4efef-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4efef-110">EXAMPLES</span></span>

### <span data-ttu-id="4efef-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4efef-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
```

<span data-ttu-id="4efef-112">To polecenie cmdlet usuwa potok o nazwie ContosoPipeline z obszaru roboczego o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="4efef-112">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="4efef-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="4efef-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapsePipeline -Name ContosoPipeline
```

<span data-ttu-id="4efef-114">To polecenie cmdlet usuwa potok o nazwie ContosoPipeline z obszaru roboczego o nazwie ContosoWorkspace z potoku.</span><span class="sxs-lookup"><span data-stu-id="4efef-114">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="4efef-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="4efef-115">Example 3</span></span>
```powershell
PS C:\> $pipeline = Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
PS C:\> $pipeline | Remove-AzSynapsePipeline
```

<span data-ttu-id="4efef-116">To polecenie cmdlet usuwa potok o nazwie ContosoPipeline z obszaru roboczego o nazwie ContosoWorkspace z potoku.</span><span class="sxs-lookup"><span data-stu-id="4efef-116">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="4efef-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4efef-117">PARAMETERS</span></span>

### <span data-ttu-id="4efef-118">— AsJob</span><span class="sxs-lookup"><span data-stu-id="4efef-118">-AsJob</span></span>
<span data-ttu-id="4efef-119">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="4efef-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4efef-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4efef-120">-DefaultProfile</span></span>
<span data-ttu-id="4efef-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4efef-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4efef-122">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="4efef-122">-Force</span></span>
<span data-ttu-id="4efef-123">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4efef-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4efef-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4efef-124">-InputObject</span></span>
<span data-ttu-id="4efef-125">Obiekt potoku.</span><span class="sxs-lookup"><span data-stu-id="4efef-125">The pipeline object.</span></span>

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

### <span data-ttu-id="4efef-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4efef-126">-Name</span></span>
<span data-ttu-id="4efef-127">Nazwa potoku.</span><span class="sxs-lookup"><span data-stu-id="4efef-127">The pipeline name.</span></span>

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

### <span data-ttu-id="4efef-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4efef-128">-PassThru</span></span>
<span data-ttu-id="4efef-129">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="4efef-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="4efef-130">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="4efef-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="4efef-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4efef-131">-WorkspaceName</span></span>
<span data-ttu-id="4efef-132">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="4efef-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="4efef-133">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="4efef-133">-WorkspaceObject</span></span>
<span data-ttu-id="4efef-134">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="4efef-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="4efef-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4efef-135">-Confirm</span></span>
<span data-ttu-id="4efef-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4efef-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4efef-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4efef-137">-WhatIf</span></span>
<span data-ttu-id="4efef-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4efef-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4efef-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4efef-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4efef-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4efef-140">CommonParameters</span></span>
<span data-ttu-id="4efef-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4efef-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4efef-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4efef-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4efef-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4efef-143">INPUTS</span></span>

### <span data-ttu-id="4efef-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4efef-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="4efef-145">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="4efef-145">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="4efef-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4efef-146">OUTPUTS</span></span>

### <span data-ttu-id="4efef-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4efef-147">System.Boolean</span></span>

## <span data-ttu-id="4efef-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4efef-148">NOTES</span></span>

## <span data-ttu-id="4efef-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4efef-149">RELATED LINKS</span></span>
