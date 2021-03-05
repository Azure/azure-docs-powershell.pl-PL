---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapseintegrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeMetric.md
ms.openlocfilehash: 158d4a54cdbeec0dd8cf756a3c685aede97f5bed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994743"
---
# <span data-ttu-id="ada85-101">Get-AzSynapseIntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="ada85-101">Get-AzSynapseIntegrationRuntimeMetric</span></span>

## <span data-ttu-id="ada85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ada85-102">SYNOPSIS</span></span>
<span data-ttu-id="ada85-103">Pobiera dane metryczne dla środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="ada85-103">Gets metric data for an integration runtime.</span></span> 

## <span data-ttu-id="ada85-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ada85-104">SYNTAX</span></span>

### <span data-ttu-id="ada85-105">GetByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="ada85-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ada85-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ada85-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ada85-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ada85-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ada85-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ada85-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ada85-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="ada85-109">DESCRIPTION</span></span>
<span data-ttu-id="ada85-110">Polecenie **cmdlet Get-AzSynapseIntegrationRuntimeMetric** pobiera metryczne dane dotyczące środowiska uruchomieniowego integracji w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="ada85-110">The **Get-AzSynapseIntegrationRuntimeMetric** cmdlet gets metric data about integration runtime in a workspace.</span></span>

## <span data-ttu-id="ada85-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ada85-111">EXAMPLES</span></span>

### <span data-ttu-id="ada85-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ada85-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeMetric -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="ada85-113">To polecenie wyświetla dane metryczne dotyczące środowiska uruchomieniowego integracji o nazwie "test-selfhost-ir" w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="ada85-113">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="ada85-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ada85-114">PARAMETERS</span></span>

### <span data-ttu-id="ada85-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ada85-115">-DefaultProfile</span></span>
<span data-ttu-id="ada85-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ada85-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ada85-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ada85-117">-InputObject</span></span>
<span data-ttu-id="ada85-118">Obiekt środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="ada85-118">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ada85-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ada85-119">-Name</span></span>
<span data-ttu-id="ada85-120">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="ada85-120">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada85-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ada85-121">-ResourceGroupName</span></span>
<span data-ttu-id="ada85-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ada85-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada85-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ada85-123">-ResourceId</span></span>
<span data-ttu-id="ada85-124">Identyfikator zasobu środowiska uruchomieniowego integracji Synapse.</span><span class="sxs-lookup"><span data-stu-id="ada85-124">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada85-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ada85-125">-WorkspaceName</span></span>
<span data-ttu-id="ada85-126">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="ada85-126">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ada85-127">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ada85-127">-WorkspaceObject</span></span>
<span data-ttu-id="ada85-128">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="ada85-128">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ada85-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ada85-129">CommonParameters</span></span>
<span data-ttu-id="ada85-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ada85-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ada85-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ada85-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ada85-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ada85-132">INPUTS</span></span>

### <span data-ttu-id="ada85-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ada85-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="ada85-134">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ada85-134">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="ada85-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ada85-135">OUTPUTS</span></span>

### <span data-ttu-id="ada85-136">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="ada85-136">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="ada85-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ada85-137">NOTES</span></span>

## <span data-ttu-id="ada85-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ada85-138">RELATED LINKS</span></span>
