---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 168a19c6e3900b395841aabbc19359d9fa4858f2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981809"
---
# <span data-ttu-id="eb738-101">Get-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="eb738-101">Get-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="eb738-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb738-102">SYNOPSIS</span></span>
<span data-ttu-id="eb738-103">Pobiera informacje o zasobach środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="eb738-103">Gets information about integration runtime resources.</span></span>

## <span data-ttu-id="eb738-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="eb738-104">SYNTAX</span></span>

### <span data-ttu-id="eb738-105">GetByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="eb738-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb738-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb738-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime [-Name <String>] -WorkspaceObject <PSSynapseWorkspace> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb738-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb738-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime -ResourceId <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eb738-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb738-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb738-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="eb738-109">DESCRIPTION</span></span>
<span data-ttu-id="eb738-110">Polecenie **cmdlet Get-AzSynapseIntegrationRuntime** pobiera informacje o środowiskach uruchomieniowych integracji w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="eb738-110">The **Get-AzSynapseIntegrationRuntime** cmdlet gets information about integration runtimes in a workspace.</span></span>
<span data-ttu-id="eb738-111">Jeśli określisz nazwę środowiska uruchomieniowego integracji, to polecenie cmdlet pobiera informacje o tym środowisku uruchomieniowym integracji.</span><span class="sxs-lookup"><span data-stu-id="eb738-111">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="eb738-112">Jeśli nie określisz nazwy, to polecenie cmdlet pobiera informacje o wszystkich środowiskach uruchomieniowych integracji w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="eb738-112">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a workspace.</span></span>

## <span data-ttu-id="eb738-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="eb738-113">EXAMPLES</span></span>

### <span data-ttu-id="eb738-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="eb738-114">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="eb738-115">Lista wszystkich środowisk uruchomieniowych integracji w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="eb738-115">List all integration runtimes in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="eb738-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="eb738-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="eb738-117">To polecenie wyświetla informacje o środowisku uruchomieniowym integracji o nazwie "test-selfhost-ir" w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="eb738-117">This command displays information about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="eb738-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="eb738-118">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -Status
```

<span data-ttu-id="eb738-119">To polecenie wyświetla stan szczegółów środowiska uruchomieniowego integracji o nazwie "test-selfhost-ir" w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="eb738-119">This command displays detail status about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="eb738-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb738-120">PARAMETERS</span></span>

### <span data-ttu-id="eb738-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb738-121">-DefaultProfile</span></span>
<span data-ttu-id="eb738-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="eb738-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb738-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb738-123">-InputObject</span></span>
<span data-ttu-id="eb738-124">Obiekt środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="eb738-124">The integration runtime object.</span></span>

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

### <span data-ttu-id="eb738-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="eb738-125">-Name</span></span>
<span data-ttu-id="eb738-126">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="eb738-126">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb738-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb738-127">-ResourceGroupName</span></span>
<span data-ttu-id="eb738-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="eb738-128">Resource group name.</span></span>

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

### <span data-ttu-id="eb738-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb738-129">-ResourceId</span></span>
<span data-ttu-id="eb738-130">Identyfikator zasobu środowiska uruchomieniowego integracji Synapse.</span><span class="sxs-lookup"><span data-stu-id="eb738-130">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="eb738-131">— Status</span><span class="sxs-lookup"><span data-stu-id="eb738-131">-Status</span></span>
<span data-ttu-id="eb738-132">Stan szczegółów środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="eb738-132">The integration runtime detail status.</span></span>

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

### <span data-ttu-id="eb738-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="eb738-133">-WorkspaceName</span></span>
<span data-ttu-id="eb738-134">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="eb738-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="eb738-135">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="eb738-135">-WorkspaceObject</span></span>
<span data-ttu-id="eb738-136">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="eb738-136">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="eb738-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb738-137">CommonParameters</span></span>
<span data-ttu-id="eb738-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb738-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb738-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eb738-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb738-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eb738-140">INPUTS</span></span>

### <span data-ttu-id="eb738-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="eb738-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="eb738-142">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="eb738-142">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="eb738-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eb738-143">OUTPUTS</span></span>

### <span data-ttu-id="eb738-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="eb738-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="eb738-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="eb738-145">NOTES</span></span>

## <span data-ttu-id="eb738-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eb738-146">RELATED LINKS</span></span>
