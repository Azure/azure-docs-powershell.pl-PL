---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapseintegrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeKey.md
ms.openlocfilehash: d00e4c137e3b46e7721534264c9273cde5a9ad3f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971633"
---
# <span data-ttu-id="92dff-101">Get-AzSynapseIntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="92dff-101">Get-AzSynapseIntegrationRuntimeKey</span></span>

## <span data-ttu-id="92dff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92dff-102">SYNOPSIS</span></span>
<span data-ttu-id="92dff-103">Pobiera klucze środowiska integracji z własnym hostem.</span><span class="sxs-lookup"><span data-stu-id="92dff-103">Gets keys for a self-hosted integration runtime.</span></span>

## <span data-ttu-id="92dff-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="92dff-104">SYNTAX</span></span>

### <span data-ttu-id="92dff-105">GetByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="92dff-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeKey [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92dff-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="92dff-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92dff-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="92dff-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="92dff-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="92dff-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92dff-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="92dff-109">DESCRIPTION</span></span>
<span data-ttu-id="92dff-110">Polecenie **cmdlet Get-AzSynapseIntegrationRuntimeKey** pobiera klucze środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="92dff-110">The **Get-AzSynapseIntegrationRuntimeKey** cmdlet gets keys for an integration runtime.</span></span> <span data-ttu-id="92dff-111">Klucze służą do rejestrowania węzła środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="92dff-111">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="92dff-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="92dff-112">EXAMPLES</span></span>

### <span data-ttu-id="92dff-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="92dff-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeKey -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="92dff-114">Polecenie cmdlet pobiera klucze środowiska uruchomieniowego integracji o nazwie "test-selfhost-ir".</span><span class="sxs-lookup"><span data-stu-id="92dff-114">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="92dff-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92dff-115">PARAMETERS</span></span>

### <span data-ttu-id="92dff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92dff-116">-DefaultProfile</span></span>
<span data-ttu-id="92dff-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="92dff-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92dff-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92dff-118">-InputObject</span></span>
<span data-ttu-id="92dff-119">Obiekt środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="92dff-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="92dff-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="92dff-120">-Name</span></span>
<span data-ttu-id="92dff-121">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="92dff-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="92dff-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92dff-122">-ResourceGroupName</span></span>
<span data-ttu-id="92dff-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="92dff-123">Resource group name.</span></span>

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

### <span data-ttu-id="92dff-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92dff-124">-ResourceId</span></span>
<span data-ttu-id="92dff-125">Identyfikator zasobu środowiska uruchomieniowego integracji Synapse.</span><span class="sxs-lookup"><span data-stu-id="92dff-125">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="92dff-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="92dff-126">-WorkspaceName</span></span>
<span data-ttu-id="92dff-127">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="92dff-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="92dff-128">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="92dff-128">-WorkspaceObject</span></span>
<span data-ttu-id="92dff-129">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="92dff-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="92dff-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92dff-130">CommonParameters</span></span>
<span data-ttu-id="92dff-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92dff-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92dff-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="92dff-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92dff-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="92dff-133">INPUTS</span></span>

### <span data-ttu-id="92dff-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="92dff-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="92dff-135">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="92dff-135">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="92dff-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="92dff-136">OUTPUTS</span></span>

### <span data-ttu-id="92dff-137">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="92dff-137">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="92dff-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="92dff-138">NOTES</span></span>

## <span data-ttu-id="92dff-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="92dff-139">RELATED LINKS</span></span>
