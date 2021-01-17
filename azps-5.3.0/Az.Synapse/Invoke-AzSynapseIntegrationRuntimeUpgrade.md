---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/invoke-azsynapseintegrationruntimeupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseIntegrationRuntimeUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseIntegrationRuntimeUpgrade.md
ms.openlocfilehash: 59630bd0ffcf5bebfc68f647cff444466727a990
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383686"
---
# <span data-ttu-id="10a89-101">Invoke-AzSynapseIntegrationRuntimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="10a89-101">Invoke-AzSynapseIntegrationRuntimeUpgrade</span></span>

## <span data-ttu-id="10a89-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="10a89-102">SYNOPSIS</span></span>
<span data-ttu-id="10a89-103">Uaktualnia środowisko uruchomieniowe integracji na samym własnym poziomie.</span><span class="sxs-lookup"><span data-stu-id="10a89-103">Upgrades self-hosted integration runtime.</span></span>

## <span data-ttu-id="10a89-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="10a89-104">SYNTAX</span></span>

### <span data-ttu-id="10a89-105">InvokeByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="10a89-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10a89-106">InvokeByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="10a89-106">InvokeByParentObjectParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10a89-107">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="10a89-107">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10a89-108">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="10a89-108">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10a89-109">Opis</span><span class="sxs-lookup"><span data-stu-id="10a89-109">DESCRIPTION</span></span>
<span data-ttu-id="10a89-110">Polecenie cmdlet **Invoke-AzSynapseIntegrationRuntimeUpgrade** umożliwia uaktualnienie programu obsługi integracji obsługiwanego automatycznie, jeśli jest dostępna nowa wersja.</span><span class="sxs-lookup"><span data-stu-id="10a89-110">The **Invoke-AzSynapseIntegrationRuntimeUpgrade** cmdlet upgrades self-hosted integration runtime if the new version is available.</span></span>

## <span data-ttu-id="10a89-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="10a89-111">EXAMPLES</span></span>

### <span data-ttu-id="10a89-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="10a89-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSynapseIntegrationRuntimeUpgrade -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="10a89-113">Polecenie cmdlet uaktualnia w obszarze roboczym programu SelfHost o nazwie "test--IR".</span><span class="sxs-lookup"><span data-stu-id="10a89-113">The cmdlet upgrades self-hosted integration runtime named 'test-selfhost-ir' in workspace ContosoWorkspace.</span></span>

## <span data-ttu-id="10a89-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="10a89-114">PARAMETERS</span></span>

### <span data-ttu-id="10a89-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10a89-115">-DefaultProfile</span></span>
<span data-ttu-id="10a89-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="10a89-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10a89-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="10a89-117">-InputObject</span></span>
<span data-ttu-id="10a89-118">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="10a89-118">The integration runtime object.</span></span>

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

### <span data-ttu-id="10a89-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="10a89-119">-Name</span></span>
<span data-ttu-id="10a89-120">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="10a89-120">The integration runtime name.</span></span>

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

### <span data-ttu-id="10a89-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10a89-121">-ResourceGroupName</span></span>
<span data-ttu-id="10a89-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="10a89-122">Resource group name.</span></span>

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

### <span data-ttu-id="10a89-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10a89-123">-ResourceId</span></span>
<span data-ttu-id="10a89-124">Identyfikator zasobu środowiska uruchomieniowego integracji Synapse.</span><span class="sxs-lookup"><span data-stu-id="10a89-124">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="10a89-125">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="10a89-125">-WorkspaceName</span></span>
<span data-ttu-id="10a89-126">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="10a89-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="10a89-127">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="10a89-127">-WorkspaceObject</span></span>
<span data-ttu-id="10a89-128">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="10a89-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="10a89-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="10a89-129">-Confirm</span></span>
<span data-ttu-id="10a89-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10a89-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10a89-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10a89-131">-WhatIf</span></span>
<span data-ttu-id="10a89-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10a89-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10a89-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="10a89-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10a89-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10a89-134">CommonParameters</span></span>
<span data-ttu-id="10a89-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10a89-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10a89-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="10a89-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10a89-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10a89-137">INPUTS</span></span>

### <span data-ttu-id="10a89-138">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="10a89-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="10a89-139">Microsoft. Azure. Commands. Synapse. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="10a89-139">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="10a89-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="10a89-140">OUTPUTS</span></span>

### <span data-ttu-id="10a89-141">System. void</span><span class="sxs-lookup"><span data-stu-id="10a89-141">System.Void</span></span>

## <span data-ttu-id="10a89-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="10a89-142">NOTES</span></span>

## <span data-ttu-id="10a89-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="10a89-143">RELATED LINKS</span></span>
