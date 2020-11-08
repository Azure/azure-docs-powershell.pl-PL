---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: cb2c632b47e512d31a5349be9b6091a9981f5459
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94231613"
---
# <span data-ttu-id="f0b77-101">Remove-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="f0b77-101">Remove-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="f0b77-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f0b77-102">SYNOPSIS</span></span>
<span data-ttu-id="f0b77-103">Usuwanie węzła o podanej nazwie w środowisku wykonawczym integracji.</span><span class="sxs-lookup"><span data-stu-id="f0b77-103">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="f0b77-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f0b77-104">SYNTAX</span></span>

### <span data-ttu-id="f0b77-105">RemoveByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f0b77-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -NodeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0b77-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0b77-106">RemoveByParentObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -NodeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f0b77-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0b77-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -ResourceId <String> -NodeName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0b77-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0b77-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -NodeName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0b77-109">Opis</span><span class="sxs-lookup"><span data-stu-id="f0b77-109">DESCRIPTION</span></span>
<span data-ttu-id="f0b77-110">Polecenie cmdlet **Remove-AzSynapseIntegrationRuntimeNode** usuwa węzeł w środowisku wykonawczym integracji.</span><span class="sxs-lookup"><span data-stu-id="f0b77-110">The **Remove-AzSynapseIntegrationRuntimeNode** cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="f0b77-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f0b77-111">EXAMPLES</span></span>

### <span data-ttu-id="f0b77-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f0b77-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -NodeName 'Node_1'
```

<span data-ttu-id="f0b77-113">Usuwanie węzła o podanej nazwie w środowisku wykonawczym integracji.</span><span class="sxs-lookup"><span data-stu-id="f0b77-113">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="f0b77-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f0b77-114">PARAMETERS</span></span>

### <span data-ttu-id="f0b77-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0b77-115">-DefaultProfile</span></span>
<span data-ttu-id="f0b77-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f0b77-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0b77-117">-Force</span><span class="sxs-lookup"><span data-stu-id="f0b77-117">-Force</span></span>
<span data-ttu-id="f0b77-118">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f0b77-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="f0b77-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f0b77-119">-InputObject</span></span>
<span data-ttu-id="f0b77-120">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="f0b77-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="f0b77-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="f0b77-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="f0b77-122">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="f0b77-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="f0b77-123">-Nodename</span><span class="sxs-lookup"><span data-stu-id="f0b77-123">-NodeName</span></span>
<span data-ttu-id="f0b77-124">Nazwa węzła środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="f0b77-124">The integration runtime node name.</span></span>

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

### <span data-ttu-id="f0b77-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0b77-125">-ResourceGroupName</span></span>
<span data-ttu-id="f0b77-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f0b77-126">Resource group name.</span></span>

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

### <span data-ttu-id="f0b77-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0b77-127">-ResourceId</span></span>
<span data-ttu-id="f0b77-128">Identyfikator zasobu środowiska uruchomieniowego integracji Synapse.</span><span class="sxs-lookup"><span data-stu-id="f0b77-128">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="f0b77-129">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="f0b77-129">-WorkspaceName</span></span>
<span data-ttu-id="f0b77-130">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="f0b77-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f0b77-131">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="f0b77-131">-WorkspaceObject</span></span>
<span data-ttu-id="f0b77-132">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="f0b77-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f0b77-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f0b77-133">-Confirm</span></span>
<span data-ttu-id="f0b77-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0b77-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0b77-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0b77-135">-WhatIf</span></span>
<span data-ttu-id="f0b77-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0b77-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0b77-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f0b77-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0b77-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0b77-138">CommonParameters</span></span>
<span data-ttu-id="f0b77-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0b77-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0b77-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f0b77-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0b77-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f0b77-141">INPUTS</span></span>

### <span data-ttu-id="f0b77-142">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f0b77-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="f0b77-143">Microsoft. Azure. Commands. Synapse. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f0b77-143">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="f0b77-144">System. String</span><span class="sxs-lookup"><span data-stu-id="f0b77-144">System.String</span></span>

## <span data-ttu-id="f0b77-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f0b77-145">OUTPUTS</span></span>

### <span data-ttu-id="f0b77-146">System. void</span><span class="sxs-lookup"><span data-stu-id="f0b77-146">System.Void</span></span>

## <span data-ttu-id="f0b77-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f0b77-147">NOTES</span></span>

## <span data-ttu-id="f0b77-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f0b77-148">RELATED LINKS</span></span>
