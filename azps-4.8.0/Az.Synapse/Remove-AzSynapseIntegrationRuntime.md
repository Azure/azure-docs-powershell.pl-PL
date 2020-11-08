---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 57b6c6619a45e515c7aff2e30edc346ff39af9ac
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064383"
---
# <span data-ttu-id="f9084-101">Remove-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f9084-101">Remove-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="f9084-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f9084-102">SYNOPSIS</span></span>
<span data-ttu-id="f9084-103">Usuwa środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="f9084-103">Removes an integration runtime.</span></span>

## <span data-ttu-id="f9084-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f9084-104">SYNTAX</span></span>

### <span data-ttu-id="f9084-105">RemoveByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f9084-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9084-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9084-106">RemoveByParentObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9084-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9084-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -ResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9084-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9084-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9084-109">Opis</span><span class="sxs-lookup"><span data-stu-id="f9084-109">DESCRIPTION</span></span>
<span data-ttu-id="f9084-110">Polecenie cmdlet **Remove-AzSynapseIntegrationRuntime** usuwa środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="f9084-110">The **Remove-AzSynapseIntegrationRuntime** cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="f9084-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f9084-111">EXAMPLES</span></span>

### <span data-ttu-id="f9084-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f9084-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="f9084-113">To polecenie usuwa środowisko uruchomieniowe integracji o nazwie "Tested-zastrzeżonym-IR" z obszaru roboczego o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="f9084-113">This command removes the integration runtime named 'test-reserved-ir' from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="f9084-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f9084-114">PARAMETERS</span></span>

### <span data-ttu-id="f9084-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9084-115">-DefaultProfile</span></span>
<span data-ttu-id="f9084-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f9084-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9084-117">-Force</span><span class="sxs-lookup"><span data-stu-id="f9084-117">-Force</span></span>
<span data-ttu-id="f9084-118">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f9084-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="f9084-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f9084-119">-InputObject</span></span>
<span data-ttu-id="f9084-120">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="f9084-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="f9084-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f9084-121">-Name</span></span>
<span data-ttu-id="f9084-122">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="f9084-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="f9084-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9084-123">-ResourceGroupName</span></span>
<span data-ttu-id="f9084-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f9084-124">Resource group name.</span></span>

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

### <span data-ttu-id="f9084-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9084-125">-ResourceId</span></span>
<span data-ttu-id="f9084-126">Identyfikator zasobu środowiska uruchomieniowego integracji Synapse.</span><span class="sxs-lookup"><span data-stu-id="f9084-126">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="f9084-127">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="f9084-127">-WorkspaceName</span></span>
<span data-ttu-id="f9084-128">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="f9084-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f9084-129">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="f9084-129">-WorkspaceObject</span></span>
<span data-ttu-id="f9084-130">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="f9084-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f9084-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f9084-131">-Confirm</span></span>
<span data-ttu-id="f9084-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9084-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9084-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9084-133">-WhatIf</span></span>
<span data-ttu-id="f9084-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9084-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9084-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f9084-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9084-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9084-136">CommonParameters</span></span>
<span data-ttu-id="f9084-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9084-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9084-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f9084-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9084-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f9084-139">INPUTS</span></span>

### <span data-ttu-id="f9084-140">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f9084-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="f9084-141">Microsoft. Azure. Commands. Synapse. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f9084-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="f9084-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f9084-142">OUTPUTS</span></span>

### <span data-ttu-id="f9084-143">System. void</span><span class="sxs-lookup"><span data-stu-id="f9084-143">System.Void</span></span>

## <span data-ttu-id="f9084-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f9084-144">NOTES</span></span>

## <span data-ttu-id="f9084-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f9084-145">RELATED LINKS</span></span>
