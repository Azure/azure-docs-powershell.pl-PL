---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: 4192350397a9ba23e57b77b017ff7409afac7a39
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063807"
---
# <span data-ttu-id="6cbf5-101">Update-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="6cbf5-101">Update-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="6cbf5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6cbf5-102">SYNOPSIS</span></span>
<span data-ttu-id="6cbf5-103">Umożliwia zaktualizowanie węzła środowiska uruchomieniowego integracji na samym własnym poziomie.</span><span class="sxs-lookup"><span data-stu-id="6cbf5-103">Updates self-hosted integration runtime node.</span></span>

## <span data-ttu-id="6cbf5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6cbf5-104">SYNTAX</span></span>

### <span data-ttu-id="6cbf5-105">UpdateByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6cbf5-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -Name <String> -ConcurrentJobsLimit <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cbf5-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cbf5-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -Name <String> -ConcurrentJobsLimit <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6cbf5-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cbf5-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -ResourceId <String> -Name <String> -ConcurrentJobsLimit <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cbf5-108">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cbf5-108">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -Name <String>
 -ConcurrentJobsLimit <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6cbf5-109">Opis</span><span class="sxs-lookup"><span data-stu-id="6cbf5-109">DESCRIPTION</span></span>
<span data-ttu-id="6cbf5-110">Polecenie cmdlet **Update-AzSynapseIntegrationRuntimeNode** aktualizuje właściwości węzła w obszarze roboczym do obsługi integracji samodzielnego.</span><span class="sxs-lookup"><span data-stu-id="6cbf5-110">The **Update-AzSynapseIntegrationRuntimeNode** cmdlet updates properties of self-hosted integration runtime node in a workspace.</span></span> <span data-ttu-id="6cbf5-111">Obecnie obsługuje tylko aktualizowanie "ConcurrentJobsLimit".</span><span class="sxs-lookup"><span data-stu-id="6cbf5-111">Currently only supports updating 'ConcurrentJobsLimit'.</span></span>

## <span data-ttu-id="6cbf5-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6cbf5-112">EXAMPLES</span></span>

### <span data-ttu-id="6cbf5-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6cbf5-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -ConcurrentJobsLimit 3
```

<span data-ttu-id="6cbf5-114">Polecenie cmdlet aktualizuje "ConcurrentJobsLimit" to 3 dla węzła "Node_1" w środowisku wykonawczym "test-SelfHost-IR" w ramach samodzielnej integracji.</span><span class="sxs-lookup"><span data-stu-id="6cbf5-114">The cmdlet updates 'ConcurrentJobsLimit' to 3 for node 'Node_1' in self-hosted integration runtime 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="6cbf5-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6cbf5-115">PARAMETERS</span></span>

### <span data-ttu-id="6cbf5-116">-ConcurrentJobsLimit</span><span class="sxs-lookup"><span data-stu-id="6cbf5-116">-ConcurrentJobsLimit</span></span>
<span data-ttu-id="6cbf5-117">Liczba współbieżnych zadań, które mogą działać w węźle środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="6cbf5-117">The number of concurrent jobs permitted to run on the integration runtime node.</span></span>
<span data-ttu-id="6cbf5-118">Dozwolone są wartości z zakresu od 1 do maxConcurrentJobs.</span><span class="sxs-lookup"><span data-stu-id="6cbf5-118">Values between 1 and maxConcurrentJobs are allowed.</span></span>

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

### <span data-ttu-id="6cbf5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cbf5-119">-DefaultProfile</span></span>
<span data-ttu-id="6cbf5-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6cbf5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cbf5-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6cbf5-121">-InputObject</span></span>
<span data-ttu-id="6cbf5-122">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="6cbf5-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="6cbf5-123">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="6cbf5-123">-IntegrationRuntimeName</span></span>
<span data-ttu-id="6cbf5-124">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="6cbf5-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="6cbf5-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6cbf5-125">-Name</span></span>
<span data-ttu-id="6cbf5-126">Nazwa węzła środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="6cbf5-126">The integration runtime node name.</span></span>

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

### <span data-ttu-id="6cbf5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cbf5-127">-ResourceGroupName</span></span>
<span data-ttu-id="6cbf5-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6cbf5-128">Resource group name.</span></span>

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

### <span data-ttu-id="6cbf5-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6cbf5-129">-ResourceId</span></span>
<span data-ttu-id="6cbf5-130">Identyfikator zasobu środowiska uruchomieniowego integracji Synapse.</span><span class="sxs-lookup"><span data-stu-id="6cbf5-130">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="6cbf5-131">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="6cbf5-131">-WorkspaceName</span></span>
<span data-ttu-id="6cbf5-132">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="6cbf5-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="6cbf5-133">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="6cbf5-133">-WorkspaceObject</span></span>
<span data-ttu-id="6cbf5-134">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="6cbf5-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="6cbf5-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6cbf5-135">-Confirm</span></span>
<span data-ttu-id="6cbf5-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6cbf5-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cbf5-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cbf5-137">-WhatIf</span></span>
<span data-ttu-id="6cbf5-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6cbf5-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cbf5-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6cbf5-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cbf5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cbf5-140">CommonParameters</span></span>
<span data-ttu-id="6cbf5-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cbf5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cbf5-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6cbf5-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cbf5-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6cbf5-143">INPUTS</span></span>

### <span data-ttu-id="6cbf5-144">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6cbf5-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="6cbf5-145">Microsoft. Azure. Commands. Synapse. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6cbf5-145">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="6cbf5-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6cbf5-146">OUTPUTS</span></span>

### <span data-ttu-id="6cbf5-147">Microsoft. Azure. Commands. Synapse. models. PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="6cbf5-147">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="6cbf5-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6cbf5-148">NOTES</span></span>

## <span data-ttu-id="6cbf5-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6cbf5-149">RELATED LINKS</span></span>
