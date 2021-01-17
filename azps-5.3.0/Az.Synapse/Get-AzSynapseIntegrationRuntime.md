---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 285c0877441cabf51c723a472208cc002867fa7a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491106"
---
# <span data-ttu-id="2dd73-101">Get-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2dd73-101">Get-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="2dd73-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2dd73-102">SYNOPSIS</span></span>
<span data-ttu-id="2dd73-103">Pobiera informacje o zasobach w czasie wykonywania integracji.</span><span class="sxs-lookup"><span data-stu-id="2dd73-103">Gets information about integration runtime resources.</span></span>

## <span data-ttu-id="2dd73-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2dd73-104">SYNTAX</span></span>

### <span data-ttu-id="2dd73-105">GetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2dd73-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2dd73-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2dd73-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime [-Name <String>] -WorkspaceObject <PSSynapseWorkspace> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2dd73-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2dd73-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime -ResourceId <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2dd73-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2dd73-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2dd73-109">Opis</span><span class="sxs-lookup"><span data-stu-id="2dd73-109">DESCRIPTION</span></span>
<span data-ttu-id="2dd73-110">Polecenie cmdlet **Get-AzSynapseIntegrationRuntime** pobiera informacje o środowiskach integracji w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="2dd73-110">The **Get-AzSynapseIntegrationRuntime** cmdlet gets information about integration runtimes in a workspace.</span></span>
<span data-ttu-id="2dd73-111">Jeśli określisz nazwę środowiska wykonawczego integracji, to polecenie cmdlet spowoduje wyświetlenie informacji o tym czasie wykonywania integracji.</span><span class="sxs-lookup"><span data-stu-id="2dd73-111">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="2dd73-112">Jeśli nie określisz nazwy, to polecenie cmdlet będzie pobierać informacje o wszystkich środowiskach uruchomieniowych integracji w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="2dd73-112">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a workspace.</span></span>

## <span data-ttu-id="2dd73-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2dd73-113">EXAMPLES</span></span>

### <span data-ttu-id="2dd73-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2dd73-114">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="2dd73-115">Lista wszystkich programów obsługi środowiska integracji w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="2dd73-115">List all integration runtimes in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="2dd73-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="2dd73-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="2dd73-117">To polecenie wyświetla informacje o środowisku wykonawczym integracji o nazwie test-SelfHost-IR ' w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="2dd73-117">This command displays information about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="2dd73-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="2dd73-118">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -Status
```

<span data-ttu-id="2dd73-119">To polecenie wyświetla szczegółowy stan środowiska uruchomieniowego integracji o nazwie "test-SelfHost-IR" w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="2dd73-119">This command displays detail status about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="2dd73-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2dd73-120">PARAMETERS</span></span>

### <span data-ttu-id="2dd73-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dd73-121">-DefaultProfile</span></span>
<span data-ttu-id="2dd73-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2dd73-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2dd73-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2dd73-123">-InputObject</span></span>
<span data-ttu-id="2dd73-124">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="2dd73-124">The integration runtime object.</span></span>

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

### <span data-ttu-id="2dd73-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2dd73-125">-Name</span></span>
<span data-ttu-id="2dd73-126">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="2dd73-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="2dd73-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dd73-127">-ResourceGroupName</span></span>
<span data-ttu-id="2dd73-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2dd73-128">Resource group name.</span></span>

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

### <span data-ttu-id="2dd73-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2dd73-129">-ResourceId</span></span>
<span data-ttu-id="2dd73-130">Identyfikator zasobu środowiska uruchomieniowego integracji Synapse.</span><span class="sxs-lookup"><span data-stu-id="2dd73-130">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="2dd73-131">-Status</span><span class="sxs-lookup"><span data-stu-id="2dd73-131">-Status</span></span>
<span data-ttu-id="2dd73-132">Stan szczegółów środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="2dd73-132">The integration runtime detail status.</span></span>

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

### <span data-ttu-id="2dd73-133">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="2dd73-133">-WorkspaceName</span></span>
<span data-ttu-id="2dd73-134">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="2dd73-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="2dd73-135">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="2dd73-135">-WorkspaceObject</span></span>
<span data-ttu-id="2dd73-136">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="2dd73-136">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="2dd73-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dd73-137">CommonParameters</span></span>
<span data-ttu-id="2dd73-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dd73-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dd73-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2dd73-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dd73-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2dd73-140">INPUTS</span></span>

### <span data-ttu-id="2dd73-141">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2dd73-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="2dd73-142">Microsoft. Azure. Commands. Synapse. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2dd73-142">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="2dd73-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2dd73-143">OUTPUTS</span></span>

### <span data-ttu-id="2dd73-144">Microsoft. Azure. Commands. Synapse. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2dd73-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="2dd73-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2dd73-145">NOTES</span></span>

## <span data-ttu-id="2dd73-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2dd73-146">RELATED LINKS</span></span>
