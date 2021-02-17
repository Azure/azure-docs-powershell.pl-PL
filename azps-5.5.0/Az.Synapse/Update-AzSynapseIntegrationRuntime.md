---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 31647da87319ca6be90962f34d128f5e2c922d47
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190554"
---
# <span data-ttu-id="db5e5-101">Update-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="db5e5-101">Update-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="db5e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db5e5-102">SYNOPSIS</span></span>
<span data-ttu-id="db5e5-103">Aktualizuje środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="db5e5-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="db5e5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="db5e5-104">SYNTAX</span></span>

### <span data-ttu-id="db5e5-105">UpdateByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="db5e5-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db5e5-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db5e5-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db5e5-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="db5e5-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -ResourceId <String> [-AutoUpdate <String>]
 [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="db5e5-108">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db5e5-108">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-AutoUpdate <String>]
 [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="db5e5-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="db5e5-109">DESCRIPTION</span></span>
<span data-ttu-id="db5e5-110">Polecenie **cmdlet Update-AzSynapseIntegrationRuntime** aktualizuje właściwości środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="db5e5-110">The **Update-AzSynapseIntegrationRuntime** cmdlet updates integration runtime properties.</span></span> <span data-ttu-id="db5e5-111">Obecnie polecenie cmdlet obsługuje tylko aktualizowanie plików "AutoUpdate" i "AutoUpdateDelayOffset" dla środowiska uruchomieniowego integracji samoobsługowej.</span><span class="sxs-lookup"><span data-stu-id="db5e5-111">Currently the cmdlet only supports updating 'AutoUpdate' and 'AutoUpdateDelayOffset' for self-hosted integration runtime.</span></span>

## <span data-ttu-id="db5e5-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="db5e5-112">EXAMPLES</span></span>

### <span data-ttu-id="db5e5-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="db5e5-113">Example 1</span></span>
```powershell
PS C:\> $ts = New-TimeSpan -Hours 3
PS C:\> Update-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -AutoUpdate Off -AutoUpdateDelayOffset $ts
```

<span data-ttu-id="db5e5-114">Polecenie cmdlet aktualizuje środowisko uruchomieniowe integracji z własnym hostem o nazwie "test-selfhost-ir".</span><span class="sxs-lookup"><span data-stu-id="db5e5-114">The cmdlet updates self-hosted integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="db5e5-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db5e5-115">PARAMETERS</span></span>

### <span data-ttu-id="db5e5-116">-AutoUpdate</span><span class="sxs-lookup"><span data-stu-id="db5e5-116">-AutoUpdate</span></span>
<span data-ttu-id="db5e5-117">Włącz lub wyłącz automatyczną aktualizację środowiska uruchomieniowego integracji z własnym środowiskiem uruchomieniowym.</span><span class="sxs-lookup"><span data-stu-id="db5e5-117">Enable or disable the self-hosted integration runtime auto-update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: On, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db5e5-118">-AutoUpdateDelayOffset</span><span class="sxs-lookup"><span data-stu-id="db5e5-118">-AutoUpdateDelayOffset</span></span>
<span data-ttu-id="db5e5-119">Godzina dnia na automatyczną aktualizację środowiska uruchomieniowego integracji z własnym środowiskiem uruchomieniowym.</span><span class="sxs-lookup"><span data-stu-id="db5e5-119">The time of the day for the self-hosted integration runtime auto-update.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db5e5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db5e5-120">-DefaultProfile</span></span>
<span data-ttu-id="db5e5-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="db5e5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db5e5-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db5e5-122">-InputObject</span></span>
<span data-ttu-id="db5e5-123">Obiekt środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="db5e5-123">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db5e5-124">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="db5e5-124">-IntegrationRuntimeName</span></span>
<span data-ttu-id="db5e5-125">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="db5e5-125">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db5e5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db5e5-126">-ResourceGroupName</span></span>
<span data-ttu-id="db5e5-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="db5e5-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db5e5-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db5e5-128">-ResourceId</span></span>
<span data-ttu-id="db5e5-129">Identyfikator zasobu środowiska uruchomieniowego integracji Synapse.</span><span class="sxs-lookup"><span data-stu-id="db5e5-129">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db5e5-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="db5e5-130">-WorkspaceName</span></span>
<span data-ttu-id="db5e5-131">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="db5e5-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db5e5-132">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="db5e5-132">-WorkspaceObject</span></span>
<span data-ttu-id="db5e5-133">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="db5e5-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db5e5-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="db5e5-134">-Confirm</span></span>
<span data-ttu-id="db5e5-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="db5e5-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db5e5-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db5e5-136">-WhatIf</span></span>
<span data-ttu-id="db5e5-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db5e5-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db5e5-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="db5e5-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db5e5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db5e5-139">CommonParameters</span></span>
<span data-ttu-id="db5e5-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db5e5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db5e5-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db5e5-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db5e5-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="db5e5-142">INPUTS</span></span>

### <span data-ttu-id="db5e5-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="db5e5-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="db5e5-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="db5e5-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="db5e5-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="db5e5-145">OUTPUTS</span></span>

### <span data-ttu-id="db5e5-146">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="db5e5-146">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="db5e5-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="db5e5-147">NOTES</span></span>

## <span data-ttu-id="db5e5-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="db5e5-148">RELATED LINKS</span></span>
