---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 004cfc8e0bd22be1f57a320cf10aa7d7f53cbb0e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990711"
---
# <span data-ttu-id="9e12f-101">Update-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="9e12f-101">Update-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="9e12f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e12f-102">SYNOPSIS</span></span>
<span data-ttu-id="9e12f-103">Aktualizuje środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="9e12f-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="9e12f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9e12f-104">SYNTAX</span></span>

### <span data-ttu-id="9e12f-105">UpdateByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="9e12f-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e12f-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e12f-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e12f-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e12f-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -ResourceId <String> [-AutoUpdate <String>]
 [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9e12f-108">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e12f-108">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-AutoUpdate <String>]
 [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9e12f-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="9e12f-109">DESCRIPTION</span></span>
<span data-ttu-id="9e12f-110">Polecenie **cmdlet Update-AzSynapseIntegrationRuntime** aktualizuje właściwości środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="9e12f-110">The **Update-AzSynapseIntegrationRuntime** cmdlet updates integration runtime properties.</span></span> <span data-ttu-id="9e12f-111">Obecnie polecenie cmdlet obsługuje tylko aktualizowanie "AutoUpdate" i "AutoUpdateDelayOffset" dla środowiska uruchomieniowego integracji z własnym hostem.</span><span class="sxs-lookup"><span data-stu-id="9e12f-111">Currently the cmdlet only supports updating 'AutoUpdate' and 'AutoUpdateDelayOffset' for self-hosted integration runtime.</span></span>

## <span data-ttu-id="9e12f-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9e12f-112">EXAMPLES</span></span>

### <span data-ttu-id="9e12f-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9e12f-113">Example 1</span></span>
```powershell
PS C:\> $ts = New-TimeSpan -Hours 3
PS C:\> Update-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -AutoUpdate Off -AutoUpdateDelayOffset $ts
```

<span data-ttu-id="9e12f-114">Polecenie cmdlet aktualizuje środowisko uruchomieniowe integracji samoobsługowej o nazwie "test-selfhost-ir".</span><span class="sxs-lookup"><span data-stu-id="9e12f-114">The cmdlet updates self-hosted integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="9e12f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e12f-115">PARAMETERS</span></span>

### <span data-ttu-id="9e12f-116">-AutoUpdate</span><span class="sxs-lookup"><span data-stu-id="9e12f-116">-AutoUpdate</span></span>
<span data-ttu-id="9e12f-117">Włącz lub wyłącz automatyczną aktualizację środowiska integracji z własnym środowiskiem uruchomieniowym.</span><span class="sxs-lookup"><span data-stu-id="9e12f-117">Enable or disable the self-hosted integration runtime auto-update.</span></span>

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

### <span data-ttu-id="9e12f-118">-AutoUpdateDelayOffset</span><span class="sxs-lookup"><span data-stu-id="9e12f-118">-AutoUpdateDelayOffset</span></span>
<span data-ttu-id="9e12f-119">Godzina dnia na automatyczną aktualizację środowiska integracji z własnym środowiskiem uruchomieniowym.</span><span class="sxs-lookup"><span data-stu-id="9e12f-119">The time of the day for the self-hosted integration runtime auto-update.</span></span>

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

### <span data-ttu-id="9e12f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e12f-120">-DefaultProfile</span></span>
<span data-ttu-id="9e12f-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9e12f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e12f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e12f-122">-InputObject</span></span>
<span data-ttu-id="9e12f-123">Obiekt środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="9e12f-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="9e12f-124">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="9e12f-124">-IntegrationRuntimeName</span></span>
<span data-ttu-id="9e12f-125">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="9e12f-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="9e12f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e12f-126">-ResourceGroupName</span></span>
<span data-ttu-id="9e12f-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9e12f-127">Resource group name.</span></span>

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

### <span data-ttu-id="9e12f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e12f-128">-ResourceId</span></span>
<span data-ttu-id="9e12f-129">Identyfikator zasobu środowiska uruchomieniowego integracji Synapse.</span><span class="sxs-lookup"><span data-stu-id="9e12f-129">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="9e12f-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9e12f-130">-WorkspaceName</span></span>
<span data-ttu-id="9e12f-131">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="9e12f-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="9e12f-132">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9e12f-132">-WorkspaceObject</span></span>
<span data-ttu-id="9e12f-133">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="9e12f-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="9e12f-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9e12f-134">-Confirm</span></span>
<span data-ttu-id="9e12f-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9e12f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e12f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e12f-136">-WhatIf</span></span>
<span data-ttu-id="9e12f-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e12f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e12f-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9e12f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e12f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e12f-139">CommonParameters</span></span>
<span data-ttu-id="9e12f-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e12f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e12f-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9e12f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e12f-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e12f-142">INPUTS</span></span>

### <span data-ttu-id="9e12f-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="9e12f-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="9e12f-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="9e12f-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="9e12f-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e12f-145">OUTPUTS</span></span>

### <span data-ttu-id="9e12f-146">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="9e12f-146">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="9e12f-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9e12f-147">NOTES</span></span>

## <span data-ttu-id="9e12f-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9e12f-148">RELATED LINKS</span></span>
