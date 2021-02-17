---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeKey.md
ms.openlocfilehash: 08ce91d6d9a942dd20078e0c3b5b537360aac9fc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182802"
---
# <span data-ttu-id="73226-101">Get-AzSynapseIntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="73226-101">Get-AzSynapseIntegrationRuntimeKey</span></span>

## <span data-ttu-id="73226-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73226-102">SYNOPSIS</span></span>
<span data-ttu-id="73226-103">Pobiera klucze dla środowiska integracji z własnym hostem.</span><span class="sxs-lookup"><span data-stu-id="73226-103">Gets keys for a self-hosted integration runtime.</span></span>

## <span data-ttu-id="73226-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="73226-104">SYNTAX</span></span>

### <span data-ttu-id="73226-105">GetByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="73226-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeKey [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73226-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="73226-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73226-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="73226-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="73226-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="73226-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73226-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="73226-109">DESCRIPTION</span></span>
<span data-ttu-id="73226-110">Polecenie **cmdlet Get-AzSynapseIntegrationRuntimeKey** pobiera klucze środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="73226-110">The **Get-AzSynapseIntegrationRuntimeKey** cmdlet gets keys for an integration runtime.</span></span> <span data-ttu-id="73226-111">Klucze są używane do rejestrowania węzła środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="73226-111">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="73226-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="73226-112">EXAMPLES</span></span>

### <span data-ttu-id="73226-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="73226-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeKey -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="73226-114">Polecenie cmdlet pobiera klucze środowiska uruchomieniowego integracji o nazwie "test-selfhost-ir".</span><span class="sxs-lookup"><span data-stu-id="73226-114">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="73226-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73226-115">PARAMETERS</span></span>

### <span data-ttu-id="73226-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73226-116">-DefaultProfile</span></span>
<span data-ttu-id="73226-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="73226-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73226-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73226-118">-InputObject</span></span>
<span data-ttu-id="73226-119">Obiekt środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="73226-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="73226-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="73226-120">-Name</span></span>
<span data-ttu-id="73226-121">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="73226-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="73226-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73226-122">-ResourceGroupName</span></span>
<span data-ttu-id="73226-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="73226-123">Resource group name.</span></span>

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

### <span data-ttu-id="73226-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73226-124">-ResourceId</span></span>
<span data-ttu-id="73226-125">Identyfikator zasobu środowiska uruchomieniowego integracji Synapse.</span><span class="sxs-lookup"><span data-stu-id="73226-125">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="73226-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="73226-126">-WorkspaceName</span></span>
<span data-ttu-id="73226-127">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="73226-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="73226-128">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="73226-128">-WorkspaceObject</span></span>
<span data-ttu-id="73226-129">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="73226-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="73226-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73226-130">CommonParameters</span></span>
<span data-ttu-id="73226-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73226-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73226-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73226-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73226-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="73226-133">INPUTS</span></span>

### <span data-ttu-id="73226-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="73226-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="73226-135">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="73226-135">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="73226-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="73226-136">OUTPUTS</span></span>

### <span data-ttu-id="73226-137">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="73226-137">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="73226-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="73226-138">NOTES</span></span>

## <span data-ttu-id="73226-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="73226-139">RELATED LINKS</span></span>
