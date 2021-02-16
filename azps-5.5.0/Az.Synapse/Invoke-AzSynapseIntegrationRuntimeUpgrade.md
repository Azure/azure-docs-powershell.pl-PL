---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/invoke-azsynapseintegrationruntimeupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseIntegrationRuntimeUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseIntegrationRuntimeUpgrade.md
ms.openlocfilehash: 59630bd0ffcf5bebfc68f647cff444466727a990
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243098"
---
# <span data-ttu-id="d9ffd-101">Invoke-AzSynapseIntegrationRuntimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="d9ffd-101">Invoke-AzSynapseIntegrationRuntimeUpgrade</span></span>

## <span data-ttu-id="d9ffd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9ffd-102">SYNOPSIS</span></span>
<span data-ttu-id="d9ffd-103">Uaktualnienie środowiska integracji samoobsługowej.</span><span class="sxs-lookup"><span data-stu-id="d9ffd-103">Upgrades self-hosted integration runtime.</span></span>

## <span data-ttu-id="d9ffd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d9ffd-104">SYNTAX</span></span>

### <span data-ttu-id="d9ffd-105">InvokeByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="d9ffd-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9ffd-106">InvokeByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9ffd-106">InvokeByParentObjectParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9ffd-107">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9ffd-107">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9ffd-108">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9ffd-108">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9ffd-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="d9ffd-109">DESCRIPTION</span></span>
<span data-ttu-id="d9ffd-110">Polecenie cmdlet **Invoke-AzSynapseIntegrationRuntimeUpgrade** uaktualnia środowisko integracji samoobsługowej, jeśli jest dostępna nowa wersja.</span><span class="sxs-lookup"><span data-stu-id="d9ffd-110">The **Invoke-AzSynapseIntegrationRuntimeUpgrade** cmdlet upgrades self-hosted integration runtime if the new version is available.</span></span>

## <span data-ttu-id="d9ffd-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d9ffd-111">EXAMPLES</span></span>

### <span data-ttu-id="d9ffd-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d9ffd-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSynapseIntegrationRuntimeUpgrade -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="d9ffd-113">Polecenie cmdlet uaktualnia środowisko uruchomieniowe integracji z własnym hostem o nazwie "test-selfhost-ir" w obszarze roboczym ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="d9ffd-113">The cmdlet upgrades self-hosted integration runtime named 'test-selfhost-ir' in workspace ContosoWorkspace.</span></span>

## <span data-ttu-id="d9ffd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9ffd-114">PARAMETERS</span></span>

### <span data-ttu-id="d9ffd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9ffd-115">-DefaultProfile</span></span>
<span data-ttu-id="d9ffd-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d9ffd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9ffd-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9ffd-117">-InputObject</span></span>
<span data-ttu-id="d9ffd-118">Obiekt środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="d9ffd-118">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: InvokeByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9ffd-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d9ffd-119">-Name</span></span>
<span data-ttu-id="d9ffd-120">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="d9ffd-120">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet, InvokeByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9ffd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9ffd-121">-ResourceGroupName</span></span>
<span data-ttu-id="d9ffd-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d9ffd-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9ffd-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9ffd-123">-ResourceId</span></span>
<span data-ttu-id="d9ffd-124">Identyfikator zasobu środowiska uruchomieniowego integracji Synapse.</span><span class="sxs-lookup"><span data-stu-id="d9ffd-124">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9ffd-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d9ffd-125">-WorkspaceName</span></span>
<span data-ttu-id="d9ffd-126">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="d9ffd-126">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9ffd-127">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d9ffd-127">-WorkspaceObject</span></span>
<span data-ttu-id="d9ffd-128">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="d9ffd-128">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: InvokeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9ffd-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d9ffd-129">-Confirm</span></span>
<span data-ttu-id="d9ffd-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d9ffd-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9ffd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9ffd-131">-WhatIf</span></span>
<span data-ttu-id="d9ffd-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9ffd-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9ffd-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d9ffd-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9ffd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9ffd-134">CommonParameters</span></span>
<span data-ttu-id="d9ffd-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9ffd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9ffd-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d9ffd-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9ffd-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9ffd-137">INPUTS</span></span>

### <span data-ttu-id="d9ffd-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d9ffd-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="d9ffd-139">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="d9ffd-139">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="d9ffd-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9ffd-140">OUTPUTS</span></span>

### <span data-ttu-id="d9ffd-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="d9ffd-141">System.Void</span></span>

## <span data-ttu-id="d9ffd-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d9ffd-142">NOTES</span></span>

## <span data-ttu-id="d9ffd-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d9ffd-143">RELATED LINKS</span></span>
