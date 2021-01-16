---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: cb2c632b47e512d31a5349be9b6091a9981f5459
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362887"
---
# <span data-ttu-id="6c565-101">Remove-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="6c565-101">Remove-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="6c565-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6c565-102">SYNOPSIS</span></span>
<span data-ttu-id="6c565-103">Usuwanie węzła o podanej nazwie w środowisku wykonawczym integracji.</span><span class="sxs-lookup"><span data-stu-id="6c565-103">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="6c565-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6c565-104">SYNTAX</span></span>

### <span data-ttu-id="6c565-105">RemoveByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6c565-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -NodeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c565-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c565-106">RemoveByParentObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -NodeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6c565-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c565-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -ResourceId <String> -NodeName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c565-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c565-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -NodeName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c565-109">Opis</span><span class="sxs-lookup"><span data-stu-id="6c565-109">DESCRIPTION</span></span>
<span data-ttu-id="6c565-110">Polecenie cmdlet **Remove-AzSynapseIntegrationRuntimeNode** usuwa węzeł w środowisku wykonawczym integracji.</span><span class="sxs-lookup"><span data-stu-id="6c565-110">The **Remove-AzSynapseIntegrationRuntimeNode** cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="6c565-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6c565-111">EXAMPLES</span></span>

### <span data-ttu-id="6c565-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6c565-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -NodeName 'Node_1'
```

<span data-ttu-id="6c565-113">Usuwanie węzła o podanej nazwie w środowisku wykonawczym integracji.</span><span class="sxs-lookup"><span data-stu-id="6c565-113">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="6c565-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6c565-114">PARAMETERS</span></span>

### <span data-ttu-id="6c565-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c565-115">-DefaultProfile</span></span>
<span data-ttu-id="6c565-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6c565-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c565-117">-Force</span><span class="sxs-lookup"><span data-stu-id="6c565-117">-Force</span></span>
<span data-ttu-id="6c565-118">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6c565-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="6c565-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6c565-119">-InputObject</span></span>
<span data-ttu-id="6c565-120">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="6c565-120">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c565-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="6c565-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="6c565-122">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="6c565-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet, RemoveByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c565-123">-Nodename</span><span class="sxs-lookup"><span data-stu-id="6c565-123">-NodeName</span></span>
<span data-ttu-id="6c565-124">Nazwa węzła środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="6c565-124">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c565-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c565-125">-ResourceGroupName</span></span>
<span data-ttu-id="6c565-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6c565-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c565-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c565-127">-ResourceId</span></span>
<span data-ttu-id="6c565-128">Identyfikator zasobu środowiska uruchomieniowego integracji Synapse.</span><span class="sxs-lookup"><span data-stu-id="6c565-128">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c565-129">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="6c565-129">-WorkspaceName</span></span>
<span data-ttu-id="6c565-130">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="6c565-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c565-131">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="6c565-131">-WorkspaceObject</span></span>
<span data-ttu-id="6c565-132">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="6c565-132">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c565-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6c565-133">-Confirm</span></span>
<span data-ttu-id="6c565-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c565-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c565-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c565-135">-WhatIf</span></span>
<span data-ttu-id="6c565-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c565-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c565-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6c565-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c565-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c565-138">CommonParameters</span></span>
<span data-ttu-id="6c565-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c565-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c565-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6c565-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c565-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6c565-141">INPUTS</span></span>

### <span data-ttu-id="6c565-142">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6c565-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="6c565-143">Microsoft. Azure. Commands. Synapse. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6c565-143">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="6c565-144">System. String</span><span class="sxs-lookup"><span data-stu-id="6c565-144">System.String</span></span>

## <span data-ttu-id="6c565-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6c565-145">OUTPUTS</span></span>

### <span data-ttu-id="6c565-146">System. void</span><span class="sxs-lookup"><span data-stu-id="6c565-146">System.Void</span></span>

## <span data-ttu-id="6c565-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6c565-147">NOTES</span></span>

## <span data-ttu-id="6c565-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6c565-148">RELATED LINKS</span></span>
