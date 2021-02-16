---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 285c0877441cabf51c723a472208cc002867fa7a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195635"
---
# <span data-ttu-id="fd1bb-101">Get-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="fd1bb-101">Get-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="fd1bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd1bb-102">SYNOPSIS</span></span>
<span data-ttu-id="fd1bb-103">Pobiera informacje o zasobach środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="fd1bb-103">Gets information about integration runtime resources.</span></span>

## <span data-ttu-id="fd1bb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fd1bb-104">SYNTAX</span></span>

### <span data-ttu-id="fd1bb-105">GetByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="fd1bb-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd1bb-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd1bb-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime [-Name <String>] -WorkspaceObject <PSSynapseWorkspace> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd1bb-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd1bb-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime -ResourceId <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fd1bb-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd1bb-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd1bb-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="fd1bb-109">DESCRIPTION</span></span>
<span data-ttu-id="fd1bb-110">Polecenie **cmdlet Get-AzSynapseIntegrationRuntime** pobiera informacje o środowiskach uruchomieniowych integracji w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="fd1bb-110">The **Get-AzSynapseIntegrationRuntime** cmdlet gets information about integration runtimes in a workspace.</span></span>
<span data-ttu-id="fd1bb-111">Jeśli określisz nazwę środowiska uruchomieniowego integracji, to polecenie cmdlet pobiera informacje o tym środowisku uruchomieniowym integracji.</span><span class="sxs-lookup"><span data-stu-id="fd1bb-111">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="fd1bb-112">Jeśli nie określisz nazwy, to polecenie cmdlet pobiera informacje o wszystkich środowiskach uruchomieniowych integracji w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="fd1bb-112">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a workspace.</span></span>

## <span data-ttu-id="fd1bb-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fd1bb-113">EXAMPLES</span></span>

### <span data-ttu-id="fd1bb-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fd1bb-114">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="fd1bb-115">Lista wszystkich środowisk uruchomieniowych integracji w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="fd1bb-115">List all integration runtimes in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="fd1bb-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="fd1bb-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="fd1bb-117">To polecenie wyświetla informacje o środowisku uruchomieniowym integracji o nazwie "test-selfhost-ir" w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="fd1bb-117">This command displays information about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="fd1bb-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="fd1bb-118">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -Status
```

<span data-ttu-id="fd1bb-119">To polecenie wyświetla stan szczegółów środowiska uruchomieniowego integracji o nazwie "test-selfhost-ir" w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="fd1bb-119">This command displays detail status about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="fd1bb-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd1bb-120">PARAMETERS</span></span>

### <span data-ttu-id="fd1bb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd1bb-121">-DefaultProfile</span></span>
<span data-ttu-id="fd1bb-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fd1bb-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd1bb-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd1bb-123">-InputObject</span></span>
<span data-ttu-id="fd1bb-124">Obiekt środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="fd1bb-124">The integration runtime object.</span></span>

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

### <span data-ttu-id="fd1bb-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fd1bb-125">-Name</span></span>
<span data-ttu-id="fd1bb-126">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="fd1bb-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="fd1bb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd1bb-127">-ResourceGroupName</span></span>
<span data-ttu-id="fd1bb-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fd1bb-128">Resource group name.</span></span>

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

### <span data-ttu-id="fd1bb-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd1bb-129">-ResourceId</span></span>
<span data-ttu-id="fd1bb-130">Identyfikator zasobu środowiska uruchomieniowego integracji Synapse.</span><span class="sxs-lookup"><span data-stu-id="fd1bb-130">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="fd1bb-131">— Status</span><span class="sxs-lookup"><span data-stu-id="fd1bb-131">-Status</span></span>
<span data-ttu-id="fd1bb-132">Stan szczegółów środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="fd1bb-132">The integration runtime detail status.</span></span>

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

### <span data-ttu-id="fd1bb-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fd1bb-133">-WorkspaceName</span></span>
<span data-ttu-id="fd1bb-134">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="fd1bb-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="fd1bb-135">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="fd1bb-135">-WorkspaceObject</span></span>
<span data-ttu-id="fd1bb-136">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="fd1bb-136">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="fd1bb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd1bb-137">CommonParameters</span></span>
<span data-ttu-id="fd1bb-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd1bb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd1bb-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd1bb-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd1bb-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fd1bb-140">INPUTS</span></span>

### <span data-ttu-id="fd1bb-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="fd1bb-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="fd1bb-142">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="fd1bb-142">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="fd1bb-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fd1bb-143">OUTPUTS</span></span>

### <span data-ttu-id="fd1bb-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="fd1bb-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="fd1bb-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fd1bb-145">NOTES</span></span>

## <span data-ttu-id="fd1bb-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fd1bb-146">RELATED LINKS</span></span>
