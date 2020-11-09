---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeMetric.md
ms.openlocfilehash: 0b6700d11b017f00f10328afae2cc6638087f216
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317533"
---
# <span data-ttu-id="5d429-101">Get-AzSynapseIntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="5d429-101">Get-AzSynapseIntegrationRuntimeMetric</span></span>

## <span data-ttu-id="5d429-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5d429-102">SYNOPSIS</span></span>
<span data-ttu-id="5d429-103">Pobiera dane metryczne dla środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="5d429-103">Gets metric data for an integration runtime.</span></span> 

## <span data-ttu-id="5d429-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5d429-104">SYNTAX</span></span>

### <span data-ttu-id="5d429-105">GetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5d429-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d429-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d429-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d429-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d429-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5d429-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d429-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d429-109">Opis</span><span class="sxs-lookup"><span data-stu-id="5d429-109">DESCRIPTION</span></span>
<span data-ttu-id="5d429-110">Polecenie cmdlet **Get-AzSynapseIntegrationRuntimeMetric** pobiera dane metryki dotyczące środowiska uruchomieniowego integracji w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="5d429-110">The **Get-AzSynapseIntegrationRuntimeMetric** cmdlet gets metric data about integration runtime in a workspace.</span></span>

## <span data-ttu-id="5d429-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5d429-111">EXAMPLES</span></span>

### <span data-ttu-id="5d429-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5d429-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeMetric -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="5d429-113">To polecenie wyświetla dane metryczne dotyczące środowiska wykonawczego integracji o nazwie "test-SelfHost-IR" w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="5d429-113">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="5d429-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5d429-114">PARAMETERS</span></span>

### <span data-ttu-id="5d429-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d429-115">-DefaultProfile</span></span>
<span data-ttu-id="5d429-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5d429-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d429-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5d429-117">-InputObject</span></span>
<span data-ttu-id="5d429-118">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="5d429-118">The integration runtime object.</span></span>

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

### <span data-ttu-id="5d429-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5d429-119">-Name</span></span>
<span data-ttu-id="5d429-120">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="5d429-120">The integration runtime name.</span></span>

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

### <span data-ttu-id="5d429-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d429-121">-ResourceGroupName</span></span>
<span data-ttu-id="5d429-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5d429-122">Resource group name.</span></span>

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

### <span data-ttu-id="5d429-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d429-123">-ResourceId</span></span>
<span data-ttu-id="5d429-124">Identyfikator zasobu środowiska uruchomieniowego integracji Synapse.</span><span class="sxs-lookup"><span data-stu-id="5d429-124">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="5d429-125">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="5d429-125">-WorkspaceName</span></span>
<span data-ttu-id="5d429-126">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="5d429-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="5d429-127">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="5d429-127">-WorkspaceObject</span></span>
<span data-ttu-id="5d429-128">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="5d429-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="5d429-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d429-129">CommonParameters</span></span>
<span data-ttu-id="5d429-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d429-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d429-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5d429-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d429-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5d429-132">INPUTS</span></span>

### <span data-ttu-id="5d429-133">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5d429-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="5d429-134">Microsoft. Azure. Commands. Synapse. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5d429-134">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="5d429-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5d429-135">OUTPUTS</span></span>

### <span data-ttu-id="5d429-136">Microsoft. Azure. Commands. Synapse. models. PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="5d429-136">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="5d429-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5d429-137">NOTES</span></span>

## <span data-ttu-id="5d429-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5d429-138">RELATED LINKS</span></span>
