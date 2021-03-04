---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: 07b1b36222f0d1a31d4a4a7374957336246f0073
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011306"
---
# <span data-ttu-id="e925d-101">Remove-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="e925d-101">Remove-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="e925d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e925d-102">SYNOPSIS</span></span>
<span data-ttu-id="e925d-103">Usuń węzeł o podanej nazwie w środowisku uruchomieniowym integracji.</span><span class="sxs-lookup"><span data-stu-id="e925d-103">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="e925d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e925d-104">SYNTAX</span></span>

### <span data-ttu-id="e925d-105">RemoveByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="e925d-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -NodeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e925d-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e925d-106">RemoveByParentObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -NodeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e925d-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e925d-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -ResourceId <String> -NodeName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e925d-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e925d-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -NodeName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e925d-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="e925d-109">DESCRIPTION</span></span>
<span data-ttu-id="e925d-110">Polecenie **cmdlet Remove-AzSynapseIntegrationRuntimeNode** usuwa węzeł w środowisku uruchomieniowym integracji.</span><span class="sxs-lookup"><span data-stu-id="e925d-110">The **Remove-AzSynapseIntegrationRuntimeNode** cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="e925d-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e925d-111">EXAMPLES</span></span>

### <span data-ttu-id="e925d-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e925d-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -NodeName 'Node_1'
```

<span data-ttu-id="e925d-113">Usuń węzeł o podanej nazwie w środowisku uruchomieniowym integracji.</span><span class="sxs-lookup"><span data-stu-id="e925d-113">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="e925d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e925d-114">PARAMETERS</span></span>

### <span data-ttu-id="e925d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e925d-115">-DefaultProfile</span></span>
<span data-ttu-id="e925d-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e925d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e925d-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="e925d-117">-Force</span></span>
<span data-ttu-id="e925d-118">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e925d-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="e925d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e925d-119">-InputObject</span></span>
<span data-ttu-id="e925d-120">Obiekt środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="e925d-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="e925d-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="e925d-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="e925d-122">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="e925d-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="e925d-123">-NodeName</span><span class="sxs-lookup"><span data-stu-id="e925d-123">-NodeName</span></span>
<span data-ttu-id="e925d-124">Nazwa węzła integracji środowiska uruchomieniowego.</span><span class="sxs-lookup"><span data-stu-id="e925d-124">The integration runtime node name.</span></span>

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

### <span data-ttu-id="e925d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e925d-125">-ResourceGroupName</span></span>
<span data-ttu-id="e925d-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e925d-126">Resource group name.</span></span>

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

### <span data-ttu-id="e925d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e925d-127">-ResourceId</span></span>
<span data-ttu-id="e925d-128">Identyfikator zasobu środowiska uruchomieniowego integracji Synapse.</span><span class="sxs-lookup"><span data-stu-id="e925d-128">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="e925d-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e925d-129">-WorkspaceName</span></span>
<span data-ttu-id="e925d-130">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="e925d-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e925d-131">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e925d-131">-WorkspaceObject</span></span>
<span data-ttu-id="e925d-132">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="e925d-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e925d-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e925d-133">-Confirm</span></span>
<span data-ttu-id="e925d-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e925d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e925d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e925d-135">-WhatIf</span></span>
<span data-ttu-id="e925d-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e925d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e925d-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e925d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e925d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e925d-138">CommonParameters</span></span>
<span data-ttu-id="e925d-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e925d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e925d-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e925d-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e925d-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e925d-141">INPUTS</span></span>

### <span data-ttu-id="e925d-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e925d-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="e925d-143">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e925d-143">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="e925d-144">System.String</span><span class="sxs-lookup"><span data-stu-id="e925d-144">System.String</span></span>

## <span data-ttu-id="e925d-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e925d-145">OUTPUTS</span></span>

### <span data-ttu-id="e925d-146">System.Void</span><span class="sxs-lookup"><span data-stu-id="e925d-146">System.Void</span></span>

## <span data-ttu-id="e925d-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e925d-147">NOTES</span></span>

## <span data-ttu-id="e925d-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e925d-148">RELATED LINKS</span></span>
