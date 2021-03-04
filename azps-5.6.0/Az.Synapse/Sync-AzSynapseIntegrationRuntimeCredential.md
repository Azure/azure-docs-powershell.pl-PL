---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/sync-azsynapseintegrationruntimecredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Sync-AzSynapseIntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Sync-AzSynapseIntegrationRuntimeCredential.md
ms.openlocfilehash: d183506538bb2063a21eaf33df088ba613a2d3ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011265"
---
# <span data-ttu-id="5e959-101">Sync-AzSynapseIntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="5e959-101">Sync-AzSynapseIntegrationRuntimeCredential</span></span>

## <span data-ttu-id="5e959-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e959-102">SYNOPSIS</span></span>
<span data-ttu-id="5e959-103">Synchronizuje poświadczenia między węzłami środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="5e959-103">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="5e959-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5e959-104">SYNTAX</span></span>

### <span data-ttu-id="5e959-105">StopByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="5e959-105">StopByNameParameterSet (Default)</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5e959-106">StopByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e959-106">StopByParentObjectParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -IntegrationRuntimeName <String>
 -WorkspaceObject <PSSynapseWorkspace> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5e959-107">StopByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e959-107">StopByResourceIdParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -ResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e959-108">StopByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e959-108">StopByInputObjectParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -InputObject <PSIntegrationRuntime> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e959-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="5e959-109">DESCRIPTION</span></span>
<span data-ttu-id="5e959-110">Polecenie cmdlet **Sync-AzSynapseIntegrationRuntimeCredential** synchronizuje poświadczenia lokalne między węzłami środowiska uruchomieniowego integracji, co wymusza identyczne poświadczenia we wszystkich węzłach.</span><span class="sxs-lookup"><span data-stu-id="5e959-110">The **Sync-AzSynapseIntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="5e959-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5e959-111">EXAMPLES</span></span>

### <span data-ttu-id="5e959-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5e959-112">Example 1</span></span>
```powershell
PS C:\> Sync-AzSynapseIntegrationRuntimeCredential -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir'
```

<span data-ttu-id="5e959-113">Synchronizuje poświadczenia między węzłami środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="5e959-113">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="5e959-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e959-114">PARAMETERS</span></span>

### <span data-ttu-id="5e959-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e959-115">-DefaultProfile</span></span>
<span data-ttu-id="5e959-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5e959-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e959-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="5e959-117">-Force</span></span>
<span data-ttu-id="5e959-118">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5e959-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="5e959-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e959-119">-InputObject</span></span>
<span data-ttu-id="5e959-120">Obiekt środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="5e959-120">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: StopByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e959-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="5e959-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="5e959-122">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="5e959-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameParameterSet, StopByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e959-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e959-123">-ResourceGroupName</span></span>
<span data-ttu-id="5e959-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5e959-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e959-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e959-125">-ResourceId</span></span>
<span data-ttu-id="5e959-126">Identyfikator zasobu środowiska uruchomieniowego integracji Synapse.</span><span class="sxs-lookup"><span data-stu-id="5e959-126">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e959-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5e959-127">-WorkspaceName</span></span>
<span data-ttu-id="5e959-128">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="5e959-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e959-129">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5e959-129">-WorkspaceObject</span></span>
<span data-ttu-id="5e959-130">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="5e959-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: StopByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e959-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5e959-131">-Confirm</span></span>
<span data-ttu-id="5e959-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5e959-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e959-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e959-133">-WhatIf</span></span>
<span data-ttu-id="5e959-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e959-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e959-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5e959-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e959-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e959-136">CommonParameters</span></span>
<span data-ttu-id="5e959-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e959-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e959-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5e959-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e959-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5e959-139">INPUTS</span></span>

### <span data-ttu-id="5e959-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5e959-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="5e959-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5e959-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="5e959-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5e959-142">OUTPUTS</span></span>

### <span data-ttu-id="5e959-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="5e959-143">System.Void</span></span>

## <span data-ttu-id="5e959-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5e959-144">NOTES</span></span>

## <span data-ttu-id="5e959-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5e959-145">RELATED LINKS</span></span>
