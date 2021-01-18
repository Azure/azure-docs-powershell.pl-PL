---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 31647da87319ca6be90962f34d128f5e2c922d47
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500618"
---
# <span data-ttu-id="43a30-101">Update-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="43a30-101">Update-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="43a30-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="43a30-102">SYNOPSIS</span></span>
<span data-ttu-id="43a30-103">Aktualizuje środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="43a30-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="43a30-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="43a30-104">SYNTAX</span></span>

### <span data-ttu-id="43a30-105">UpdateByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="43a30-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43a30-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="43a30-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43a30-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="43a30-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -ResourceId <String> [-AutoUpdate <String>]
 [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="43a30-108">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="43a30-108">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-AutoUpdate <String>]
 [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="43a30-109">Opis</span><span class="sxs-lookup"><span data-stu-id="43a30-109">DESCRIPTION</span></span>
<span data-ttu-id="43a30-110">Polecenie cmdlet **Update-AzSynapseIntegrationRuntime** umożliwia aktualizowanie właściwości środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="43a30-110">The **Update-AzSynapseIntegrationRuntime** cmdlet updates integration runtime properties.</span></span> <span data-ttu-id="43a30-111">Obecnie polecenie cmdlet obsługuje tylko aktualizowanie "Autoaktualizacja" i "AutoUpdateDelayOffset" w przypadku środowiska uruchomieniowego integracji samodzielnego.</span><span class="sxs-lookup"><span data-stu-id="43a30-111">Currently the cmdlet only supports updating 'AutoUpdate' and 'AutoUpdateDelayOffset' for self-hosted integration runtime.</span></span>

## <span data-ttu-id="43a30-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="43a30-112">EXAMPLES</span></span>

### <span data-ttu-id="43a30-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="43a30-113">Example 1</span></span>
```powershell
PS C:\> $ts = New-TimeSpan -Hours 3
PS C:\> Update-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -AutoUpdate Off -AutoUpdateDelayOffset $ts
```

<span data-ttu-id="43a30-114">Polecenie cmdlet aktualizuje samowyodrębniający się środowisko uruchomieniowe integracji o nazwie "test-SelfHost-IR".</span><span class="sxs-lookup"><span data-stu-id="43a30-114">The cmdlet updates self-hosted integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="43a30-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="43a30-115">PARAMETERS</span></span>

### <span data-ttu-id="43a30-116">-Aktualizacje automatyczne</span><span class="sxs-lookup"><span data-stu-id="43a30-116">-AutoUpdate</span></span>
<span data-ttu-id="43a30-117">Włączanie lub wyłączanie automatycznej aktualizacji funkcji automatycznego aktualizowania środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="43a30-117">Enable or disable the self-hosted integration runtime auto-update.</span></span>

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

### <span data-ttu-id="43a30-118">-AutoUpdateDelayOffset</span><span class="sxs-lookup"><span data-stu-id="43a30-118">-AutoUpdateDelayOffset</span></span>
<span data-ttu-id="43a30-119">Godzina, o której ma zostać zawarta automatyczna aktualizacja automatycznej aktualizacji w czasie wykonywania integracji.</span><span class="sxs-lookup"><span data-stu-id="43a30-119">The time of the day for the self-hosted integration runtime auto-update.</span></span>

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

### <span data-ttu-id="43a30-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43a30-120">-DefaultProfile</span></span>
<span data-ttu-id="43a30-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="43a30-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43a30-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="43a30-122">-InputObject</span></span>
<span data-ttu-id="43a30-123">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="43a30-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="43a30-124">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="43a30-124">-IntegrationRuntimeName</span></span>
<span data-ttu-id="43a30-125">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="43a30-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="43a30-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43a30-126">-ResourceGroupName</span></span>
<span data-ttu-id="43a30-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="43a30-127">Resource group name.</span></span>

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

### <span data-ttu-id="43a30-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43a30-128">-ResourceId</span></span>
<span data-ttu-id="43a30-129">Identyfikator zasobu środowiska uruchomieniowego integracji Synapse.</span><span class="sxs-lookup"><span data-stu-id="43a30-129">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="43a30-130">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="43a30-130">-WorkspaceName</span></span>
<span data-ttu-id="43a30-131">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="43a30-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="43a30-132">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="43a30-132">-WorkspaceObject</span></span>
<span data-ttu-id="43a30-133">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="43a30-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="43a30-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="43a30-134">-Confirm</span></span>
<span data-ttu-id="43a30-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43a30-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43a30-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43a30-136">-WhatIf</span></span>
<span data-ttu-id="43a30-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43a30-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43a30-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="43a30-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43a30-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43a30-139">CommonParameters</span></span>
<span data-ttu-id="43a30-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43a30-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43a30-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43a30-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43a30-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="43a30-142">INPUTS</span></span>

### <span data-ttu-id="43a30-143">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="43a30-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="43a30-144">Microsoft. Azure. Commands. Synapse. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="43a30-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="43a30-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="43a30-145">OUTPUTS</span></span>

### <span data-ttu-id="43a30-146">Microsoft. Azure. Commands. Synapse. models. PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="43a30-146">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="43a30-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="43a30-147">NOTES</span></span>

## <span data-ttu-id="43a30-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="43a30-148">RELATED LINKS</span></span>
