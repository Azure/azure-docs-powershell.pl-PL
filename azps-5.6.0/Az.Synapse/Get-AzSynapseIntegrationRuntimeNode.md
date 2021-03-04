---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: dbd791b3ab77889e8c78279b576b614c4d86b4b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994736"
---
# <span data-ttu-id="48597-101">Get-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="48597-101">Get-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="48597-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48597-102">SYNOPSIS</span></span>
<span data-ttu-id="48597-103">Pobiera informacje o węźle środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="48597-103">Gets an integration runtime node information.</span></span>

## <span data-ttu-id="48597-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="48597-104">SYNTAX</span></span>

### <span data-ttu-id="48597-105">GetByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="48597-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -Name <String> [-IpAddress] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="48597-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="48597-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -Name <String> [-IpAddress] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48597-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="48597-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -ResourceId <String> -Name <String> [-IpAddress]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48597-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="48597-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -Name <String> [-IpAddress]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48597-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="48597-109">DESCRIPTION</span></span>
<span data-ttu-id="48597-110">Polecenie **cmdlet Get-AzSynapseIntegrationRuntimeNode** pobiera szczegółowe informacje węzła środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="48597-110">The **Get-AzSynapseIntegrationRuntimeNode** cmdlet gets the detail information of an integration runtime node.</span></span>

## <span data-ttu-id="48597-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="48597-111">EXAMPLES</span></span>

### <span data-ttu-id="48597-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="48597-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1'
```

<span data-ttu-id="48597-113">Polecenie cmdlet pobiera informacje o węźle o nazwie "Node_1" w środowisku integracji samoobsługowej "test-selfhost-ir" w obszarze roboczym ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="48597-113">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="48597-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="48597-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -IpAddress
```

<span data-ttu-id="48597-115">Polecenie cmdlet pobiera informacje o węźle o nazwie "Node_1" w środowisku integracji samoobsługowej "test-selfhost-ir" w obszarze roboczym "test-df-eu2", łącznie z adresem IP.</span><span class="sxs-lookup"><span data-stu-id="48597-115">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in workspace 'test-df-eu2', including the IP address.</span></span>

## <span data-ttu-id="48597-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48597-116">PARAMETERS</span></span>

### <span data-ttu-id="48597-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48597-117">-DefaultProfile</span></span>
<span data-ttu-id="48597-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="48597-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48597-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48597-119">-InputObject</span></span>
<span data-ttu-id="48597-120">Obiekt środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="48597-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="48597-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="48597-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="48597-122">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="48597-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48597-123">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="48597-123">-IpAddress</span></span>
<span data-ttu-id="48597-124">Adres IP węzła środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="48597-124">The IP Address of integration runtime node.</span></span>

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

### <span data-ttu-id="48597-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="48597-125">-Name</span></span>
<span data-ttu-id="48597-126">Nazwa węzła integracji środowiska uruchomieniowego.</span><span class="sxs-lookup"><span data-stu-id="48597-126">The integration runtime node name.</span></span>

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

### <span data-ttu-id="48597-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48597-127">-ResourceGroupName</span></span>
<span data-ttu-id="48597-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="48597-128">Resource group name.</span></span>

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

### <span data-ttu-id="48597-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48597-129">-ResourceId</span></span>
<span data-ttu-id="48597-130">Identyfikator zasobu środowiska uruchomieniowego integracji Synapse.</span><span class="sxs-lookup"><span data-stu-id="48597-130">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="48597-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="48597-131">-WorkspaceName</span></span>
<span data-ttu-id="48597-132">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="48597-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="48597-133">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="48597-133">-WorkspaceObject</span></span>
<span data-ttu-id="48597-134">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="48597-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="48597-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48597-135">CommonParameters</span></span>
<span data-ttu-id="48597-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48597-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48597-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="48597-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48597-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="48597-138">INPUTS</span></span>

### <span data-ttu-id="48597-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="48597-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="48597-140">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="48597-140">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="48597-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="48597-141">OUTPUTS</span></span>

### <span data-ttu-id="48597-142">Microsoft.Azure.Commands.Synapse.Models.PSManagedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="48597-142">Microsoft.Azure.Commands.Synapse.Models.PSManagedIntegrationRuntimeNode</span></span>

### <span data-ttu-id="48597-143">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="48597-143">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="48597-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="48597-144">NOTES</span></span>

## <span data-ttu-id="48597-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="48597-145">RELATED LINKS</span></span>
