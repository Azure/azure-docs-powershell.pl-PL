---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: 5c2d7c8aa81cb45b6b49898c95b27256aa504b73
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963434"
---
# <span data-ttu-id="b4bee-101">Update-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="b4bee-101">Update-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="b4bee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4bee-102">SYNOPSIS</span></span>
<span data-ttu-id="b4bee-103">Aktualizuje węzeł środowiska uruchomieniowego integracji samoobsługowej.</span><span class="sxs-lookup"><span data-stu-id="b4bee-103">Updates self-hosted integration runtime node.</span></span>

## <span data-ttu-id="b4bee-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b4bee-104">SYNTAX</span></span>

### <span data-ttu-id="b4bee-105">UpdateByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="b4bee-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -Name <String> -ConcurrentJobsLimit <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4bee-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4bee-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -Name <String> -ConcurrentJobsLimit <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4bee-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4bee-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -ResourceId <String> -Name <String> -ConcurrentJobsLimit <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4bee-108">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4bee-108">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -Name <String>
 -ConcurrentJobsLimit <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b4bee-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="b4bee-109">DESCRIPTION</span></span>
<span data-ttu-id="b4bee-110">Polecenie **cmdlet Update-AzSynapseIntegrationRuntimeNode** aktualizuje właściwości węzła środowiska uruchomieniowego integracji z własnym hostem w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="b4bee-110">The **Update-AzSynapseIntegrationRuntimeNode** cmdlet updates properties of self-hosted integration runtime node in a workspace.</span></span> <span data-ttu-id="b4bee-111">Obecnie obsługuje tylko aktualizowanie "ConcurrentJobsLimit".</span><span class="sxs-lookup"><span data-stu-id="b4bee-111">Currently only supports updating 'ConcurrentJobsLimit'.</span></span>

## <span data-ttu-id="b4bee-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b4bee-112">EXAMPLES</span></span>

### <span data-ttu-id="b4bee-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b4bee-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -ConcurrentJobsLimit 3
```

<span data-ttu-id="b4bee-114">Polecenie cmdlet aktualizuje "ConcurrentJobsLimit" na 3 dla węzła "Node_1" w środowisku integracji samodzielnej "test-selfhost-ir".</span><span class="sxs-lookup"><span data-stu-id="b4bee-114">The cmdlet updates 'ConcurrentJobsLimit' to 3 for node 'Node_1' in self-hosted integration runtime 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="b4bee-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4bee-115">PARAMETERS</span></span>

### <span data-ttu-id="b4bee-116">-ConcurrentJobsLimit</span><span class="sxs-lookup"><span data-stu-id="b4bee-116">-ConcurrentJobsLimit</span></span>
<span data-ttu-id="b4bee-117">Liczba jednoczesnych zadań, które mogą być uruchamiane w węźle środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="b4bee-117">The number of concurrent jobs permitted to run on the integration runtime node.</span></span>
<span data-ttu-id="b4bee-118">Dozwolone są wartości od 1 do maxConcurrentJobs.</span><span class="sxs-lookup"><span data-stu-id="b4bee-118">Values between 1 and maxConcurrentJobs are allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4bee-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4bee-119">-DefaultProfile</span></span>
<span data-ttu-id="b4bee-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b4bee-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4bee-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4bee-121">-InputObject</span></span>
<span data-ttu-id="b4bee-122">Obiekt środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="b4bee-122">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4bee-123">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="b4bee-123">-IntegrationRuntimeName</span></span>
<span data-ttu-id="b4bee-124">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="b4bee-124">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4bee-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b4bee-125">-Name</span></span>
<span data-ttu-id="b4bee-126">Nazwa węzła integracji środowiska uruchomieniowego.</span><span class="sxs-lookup"><span data-stu-id="b4bee-126">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4bee-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4bee-127">-ResourceGroupName</span></span>
<span data-ttu-id="b4bee-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b4bee-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4bee-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4bee-129">-ResourceId</span></span>
<span data-ttu-id="b4bee-130">Identyfikator zasobu środowiska uruchomieniowego integracji Synapse.</span><span class="sxs-lookup"><span data-stu-id="b4bee-130">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4bee-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b4bee-131">-WorkspaceName</span></span>
<span data-ttu-id="b4bee-132">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="b4bee-132">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4bee-133">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b4bee-133">-WorkspaceObject</span></span>
<span data-ttu-id="b4bee-134">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="b4bee-134">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4bee-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b4bee-135">-Confirm</span></span>
<span data-ttu-id="b4bee-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b4bee-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4bee-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4bee-137">-WhatIf</span></span>
<span data-ttu-id="b4bee-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4bee-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4bee-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b4bee-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4bee-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4bee-140">CommonParameters</span></span>
<span data-ttu-id="b4bee-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4bee-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4bee-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b4bee-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4bee-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4bee-143">INPUTS</span></span>

### <span data-ttu-id="b4bee-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b4bee-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="b4bee-145">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b4bee-145">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="b4bee-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4bee-146">OUTPUTS</span></span>

### <span data-ttu-id="b4bee-147">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="b4bee-147">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="b4bee-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b4bee-148">NOTES</span></span>

## <span data-ttu-id="b4bee-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b4bee-149">RELATED LINKS</span></span>
