---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: 4192350397a9ba23e57b77b017ff7409afac7a39
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182651"
---
# <span data-ttu-id="9a8a3-101">Update-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="9a8a3-101">Update-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="9a8a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a8a3-102">SYNOPSIS</span></span>
<span data-ttu-id="9a8a3-103">Aktualizuje węzeł środowiska uruchomieniowego integracji samoobsługowej.</span><span class="sxs-lookup"><span data-stu-id="9a8a3-103">Updates self-hosted integration runtime node.</span></span>

## <span data-ttu-id="9a8a3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9a8a3-104">SYNTAX</span></span>

### <span data-ttu-id="9a8a3-105">UpdateByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="9a8a3-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -Name <String> -ConcurrentJobsLimit <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a8a3-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a8a3-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -Name <String> -ConcurrentJobsLimit <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9a8a3-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a8a3-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -ResourceId <String> -Name <String> -ConcurrentJobsLimit <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a8a3-108">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a8a3-108">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -Name <String>
 -ConcurrentJobsLimit <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9a8a3-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="9a8a3-109">DESCRIPTION</span></span>
<span data-ttu-id="9a8a3-110">Polecenie **cmdlet Update-AzSynapseIntegrationRuntimeNode** aktualizuje właściwości węzła środowiska uruchomieniowego integracji samoobsługowej w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="9a8a3-110">The **Update-AzSynapseIntegrationRuntimeNode** cmdlet updates properties of self-hosted integration runtime node in a workspace.</span></span> <span data-ttu-id="9a8a3-111">Obecnie obsługuje tylko aktualizowanie "ConcurrentJobsLimit".</span><span class="sxs-lookup"><span data-stu-id="9a8a3-111">Currently only supports updating 'ConcurrentJobsLimit'.</span></span>

## <span data-ttu-id="9a8a3-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9a8a3-112">EXAMPLES</span></span>

### <span data-ttu-id="9a8a3-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9a8a3-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -ConcurrentJobsLimit 3
```

<span data-ttu-id="9a8a3-114">Polecenie cmdlet aktualizuje "ConcurrentJobsLimit" na 3 dla węzła "Node_1" w środowisku integracji samoobsługowej "test-selfhost-ir".</span><span class="sxs-lookup"><span data-stu-id="9a8a3-114">The cmdlet updates 'ConcurrentJobsLimit' to 3 for node 'Node_1' in self-hosted integration runtime 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="9a8a3-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a8a3-115">PARAMETERS</span></span>

### <span data-ttu-id="9a8a3-116">-ConcurrentJobsLimit</span><span class="sxs-lookup"><span data-stu-id="9a8a3-116">-ConcurrentJobsLimit</span></span>
<span data-ttu-id="9a8a3-117">Liczba jednoczesnych zadań dozwolonych do uruchamiania w węźle środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="9a8a3-117">The number of concurrent jobs permitted to run on the integration runtime node.</span></span>
<span data-ttu-id="9a8a3-118">Dozwolone są wartości od 1 do maxConcurrentJobs.</span><span class="sxs-lookup"><span data-stu-id="9a8a3-118">Values between 1 and maxConcurrentJobs are allowed.</span></span>

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

### <span data-ttu-id="9a8a3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a8a3-119">-DefaultProfile</span></span>
<span data-ttu-id="9a8a3-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9a8a3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a8a3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a8a3-121">-InputObject</span></span>
<span data-ttu-id="9a8a3-122">Obiekt środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="9a8a3-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="9a8a3-123">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="9a8a3-123">-IntegrationRuntimeName</span></span>
<span data-ttu-id="9a8a3-124">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="9a8a3-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="9a8a3-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9a8a3-125">-Name</span></span>
<span data-ttu-id="9a8a3-126">Nazwa węzła integracji środowiska uruchomieniowego.</span><span class="sxs-lookup"><span data-stu-id="9a8a3-126">The integration runtime node name.</span></span>

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

### <span data-ttu-id="9a8a3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a8a3-127">-ResourceGroupName</span></span>
<span data-ttu-id="9a8a3-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9a8a3-128">Resource group name.</span></span>

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

### <span data-ttu-id="9a8a3-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a8a3-129">-ResourceId</span></span>
<span data-ttu-id="9a8a3-130">Identyfikator zasobu środowiska uruchomieniowego integracji Synapse.</span><span class="sxs-lookup"><span data-stu-id="9a8a3-130">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="9a8a3-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9a8a3-131">-WorkspaceName</span></span>
<span data-ttu-id="9a8a3-132">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="9a8a3-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="9a8a3-133">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9a8a3-133">-WorkspaceObject</span></span>
<span data-ttu-id="9a8a3-134">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="9a8a3-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="9a8a3-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9a8a3-135">-Confirm</span></span>
<span data-ttu-id="9a8a3-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9a8a3-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a8a3-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a8a3-137">-WhatIf</span></span>
<span data-ttu-id="9a8a3-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a8a3-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a8a3-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9a8a3-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a8a3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a8a3-140">CommonParameters</span></span>
<span data-ttu-id="9a8a3-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a8a3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a8a3-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9a8a3-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a8a3-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9a8a3-143">INPUTS</span></span>

### <span data-ttu-id="9a8a3-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="9a8a3-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="9a8a3-145">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="9a8a3-145">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="9a8a3-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9a8a3-146">OUTPUTS</span></span>

### <span data-ttu-id="9a8a3-147">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="9a8a3-147">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="9a8a3-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9a8a3-148">NOTES</span></span>

## <span data-ttu-id="9a8a3-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9a8a3-149">RELATED LINKS</span></span>
