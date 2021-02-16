---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 57b6c6619a45e515c7aff2e30edc346ff39af9ac
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243091"
---
# <span data-ttu-id="68ae5-101">Remove-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="68ae5-101">Remove-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="68ae5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68ae5-102">SYNOPSIS</span></span>
<span data-ttu-id="68ae5-103">Usuwa środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="68ae5-103">Removes an integration runtime.</span></span>

## <span data-ttu-id="68ae5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="68ae5-104">SYNTAX</span></span>

### <span data-ttu-id="68ae5-105">RemoveByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="68ae5-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68ae5-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="68ae5-106">RemoveByParentObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68ae5-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="68ae5-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -ResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68ae5-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="68ae5-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68ae5-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="68ae5-109">DESCRIPTION</span></span>
<span data-ttu-id="68ae5-110">Polecenie **cmdlet Remove-AzSynapseIntegrationRuntime** usuwa środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="68ae5-110">The **Remove-AzSynapseIntegrationRuntime** cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="68ae5-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="68ae5-111">EXAMPLES</span></span>

### <span data-ttu-id="68ae5-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="68ae5-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="68ae5-113">To polecenie usuwa środowisko uruchomieniowe integracji o nazwie "test-reserved-ir" z obszaru roboczego o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="68ae5-113">This command removes the integration runtime named 'test-reserved-ir' from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="68ae5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="68ae5-114">PARAMETERS</span></span>

### <span data-ttu-id="68ae5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68ae5-115">-DefaultProfile</span></span>
<span data-ttu-id="68ae5-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="68ae5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68ae5-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="68ae5-117">-Force</span></span>
<span data-ttu-id="68ae5-118">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="68ae5-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="68ae5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68ae5-119">-InputObject</span></span>
<span data-ttu-id="68ae5-120">Obiekt środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="68ae5-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="68ae5-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="68ae5-121">-Name</span></span>
<span data-ttu-id="68ae5-122">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="68ae5-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet, RemoveByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68ae5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68ae5-123">-ResourceGroupName</span></span>
<span data-ttu-id="68ae5-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="68ae5-124">Resource group name.</span></span>

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

### <span data-ttu-id="68ae5-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="68ae5-125">-ResourceId</span></span>
<span data-ttu-id="68ae5-126">Identyfikator zasobu środowiska uruchomieniowego integracji Synapse.</span><span class="sxs-lookup"><span data-stu-id="68ae5-126">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="68ae5-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="68ae5-127">-WorkspaceName</span></span>
<span data-ttu-id="68ae5-128">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="68ae5-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="68ae5-129">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="68ae5-129">-WorkspaceObject</span></span>
<span data-ttu-id="68ae5-130">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="68ae5-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="68ae5-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="68ae5-131">-Confirm</span></span>
<span data-ttu-id="68ae5-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="68ae5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68ae5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68ae5-133">-WhatIf</span></span>
<span data-ttu-id="68ae5-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68ae5-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68ae5-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="68ae5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68ae5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68ae5-136">CommonParameters</span></span>
<span data-ttu-id="68ae5-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68ae5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68ae5-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="68ae5-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68ae5-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="68ae5-139">INPUTS</span></span>

### <span data-ttu-id="68ae5-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="68ae5-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="68ae5-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="68ae5-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="68ae5-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="68ae5-142">OUTPUTS</span></span>

### <span data-ttu-id="68ae5-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="68ae5-143">System.Void</span></span>

## <span data-ttu-id="68ae5-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="68ae5-144">NOTES</span></span>

## <span data-ttu-id="68ae5-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="68ae5-145">RELATED LINKS</span></span>
