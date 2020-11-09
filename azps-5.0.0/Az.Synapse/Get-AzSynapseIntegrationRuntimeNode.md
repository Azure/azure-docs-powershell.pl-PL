---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: 5df58da7ef5fa0829da27f4d6a46372f42bc9dc5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317527"
---
# <span data-ttu-id="6e52a-101">Get-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="6e52a-101">Get-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="6e52a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6e52a-102">SYNOPSIS</span></span>
<span data-ttu-id="6e52a-103">Pobiera informacje o węźle środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="6e52a-103">Gets an integration runtime node information.</span></span>

## <span data-ttu-id="6e52a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6e52a-104">SYNTAX</span></span>

### <span data-ttu-id="6e52a-105">GetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6e52a-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -Name <String> [-IpAddress] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6e52a-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e52a-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -Name <String> [-IpAddress] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e52a-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e52a-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -ResourceId <String> -Name <String> [-IpAddress]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e52a-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e52a-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -Name <String> [-IpAddress]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e52a-109">Opis</span><span class="sxs-lookup"><span data-stu-id="6e52a-109">DESCRIPTION</span></span>
<span data-ttu-id="6e52a-110">Polecenie cmdlet **Get-AzSynapseIntegrationRuntimeNode umożliwia wyświetlenie** szczegółowych informacji dotyczących węzła środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="6e52a-110">The **Get-AzSynapseIntegrationRuntimeNode** cmdlet gets the detail information of an integration runtime node.</span></span>

## <span data-ttu-id="6e52a-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6e52a-111">EXAMPLES</span></span>

### <span data-ttu-id="6e52a-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6e52a-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1'
```

<span data-ttu-id="6e52a-113">Polecenie cmdlet pobiera informacje o węźle o nazwie "Node_1" w obszarze roboczym w środowisku wykonawczym integracji "test-SelfHost-IR" w obszarze roboczym ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="6e52a-113">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="6e52a-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6e52a-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -IpAddress
```

<span data-ttu-id="6e52a-115">Polecenie cmdlet pobiera informacje o węźle o nazwie "Node_1" w ramach programu "test-SelfHost-IR" w obszarze roboczym "test-DF-EU2", łącznie z adresem IP.</span><span class="sxs-lookup"><span data-stu-id="6e52a-115">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in workspace 'test-df-eu2', including the IP address.</span></span>

## <span data-ttu-id="6e52a-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6e52a-116">PARAMETERS</span></span>

### <span data-ttu-id="6e52a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e52a-117">-DefaultProfile</span></span>
<span data-ttu-id="6e52a-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6e52a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e52a-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6e52a-119">-InputObject</span></span>
<span data-ttu-id="6e52a-120">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="6e52a-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="6e52a-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="6e52a-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="6e52a-122">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="6e52a-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="6e52a-123">-Adres_IP</span><span class="sxs-lookup"><span data-stu-id="6e52a-123">-IpAddress</span></span>
<span data-ttu-id="6e52a-124">Adres IP węzła środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="6e52a-124">The IP Address of integration runtime node.</span></span>

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

### <span data-ttu-id="6e52a-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6e52a-125">-Name</span></span>
<span data-ttu-id="6e52a-126">Nazwa węzła środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="6e52a-126">The integration runtime node name.</span></span>

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

### <span data-ttu-id="6e52a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e52a-127">-ResourceGroupName</span></span>
<span data-ttu-id="6e52a-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6e52a-128">Resource group name.</span></span>

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

### <span data-ttu-id="6e52a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6e52a-129">-ResourceId</span></span>
<span data-ttu-id="6e52a-130">Identyfikator zasobu środowiska uruchomieniowego integracji Synapse.</span><span class="sxs-lookup"><span data-stu-id="6e52a-130">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="6e52a-131">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="6e52a-131">-WorkspaceName</span></span>
<span data-ttu-id="6e52a-132">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="6e52a-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="6e52a-133">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="6e52a-133">-WorkspaceObject</span></span>
<span data-ttu-id="6e52a-134">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="6e52a-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="6e52a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e52a-135">CommonParameters</span></span>
<span data-ttu-id="6e52a-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e52a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e52a-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6e52a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e52a-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6e52a-138">INPUTS</span></span>

### <span data-ttu-id="6e52a-139">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6e52a-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="6e52a-140">Microsoft. Azure. Commands. Synapse. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6e52a-140">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="6e52a-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6e52a-141">OUTPUTS</span></span>

### <span data-ttu-id="6e52a-142">Microsoft. Azure. Commands. Synapse. models. PSManagedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="6e52a-142">Microsoft.Azure.Commands.Synapse.Models.PSManagedIntegrationRuntimeNode</span></span>

### <span data-ttu-id="6e52a-143">Microsoft. Azure. Commands. Synapse. models. PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="6e52a-143">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="6e52a-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6e52a-144">NOTES</span></span>

## <span data-ttu-id="6e52a-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6e52a-145">RELATED LINKS</span></span>
