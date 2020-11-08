---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/sync-azsynapseintegrationruntimecredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Sync-AzSynapseIntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Sync-AzSynapseIntegrationRuntimeCredential.md
ms.openlocfilehash: feb9d74cf49dfa8ae5455b303ee78f443a08e942
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94061932"
---
# <span data-ttu-id="8002e-101">Sync-AzSynapseIntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="8002e-101">Sync-AzSynapseIntegrationRuntimeCredential</span></span>

## <span data-ttu-id="8002e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8002e-102">SYNOPSIS</span></span>
<span data-ttu-id="8002e-103">Synchronizuje poświadczenia między węzłami w środowisku wykonawczym integracji.</span><span class="sxs-lookup"><span data-stu-id="8002e-103">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="8002e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8002e-104">SYNTAX</span></span>

### <span data-ttu-id="8002e-105">StopByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8002e-105">StopByNameParameterSet (Default)</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8002e-106">StopByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8002e-106">StopByParentObjectParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -IntegrationRuntimeName <String>
 -WorkspaceObject <PSSynapseWorkspace> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8002e-107">StopByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8002e-107">StopByResourceIdParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -ResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8002e-108">StopByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8002e-108">StopByInputObjectParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -InputObject <PSIntegrationRuntime> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8002e-109">Opis</span><span class="sxs-lookup"><span data-stu-id="8002e-109">DESCRIPTION</span></span>
<span data-ttu-id="8002e-110">Polecenie cmdlet **Sync-AzSynapseIntegrationRuntimeCredential** synchronizuje poświadczenia lokalne między węzłami środowiska wykonawczego programu integracyjnego, które wymuszają identyczne poświadczenia we wszystkich węzłach.</span><span class="sxs-lookup"><span data-stu-id="8002e-110">The **Sync-AzSynapseIntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="8002e-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8002e-111">EXAMPLES</span></span>

### <span data-ttu-id="8002e-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8002e-112">Example 1</span></span>
```powershell
PS C:\> Sync-AzSynapseIntegrationRuntimeCredential -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir'
```

<span data-ttu-id="8002e-113">Synchronizuje poświadczenia między węzłami w środowisku wykonawczym integracji.</span><span class="sxs-lookup"><span data-stu-id="8002e-113">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="8002e-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8002e-114">PARAMETERS</span></span>

### <span data-ttu-id="8002e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8002e-115">-DefaultProfile</span></span>
<span data-ttu-id="8002e-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8002e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8002e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="8002e-117">-Force</span></span>
<span data-ttu-id="8002e-118">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8002e-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="8002e-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8002e-119">-InputObject</span></span>
<span data-ttu-id="8002e-120">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="8002e-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="8002e-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="8002e-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="8002e-122">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="8002e-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="8002e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8002e-123">-ResourceGroupName</span></span>
<span data-ttu-id="8002e-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8002e-124">Resource group name.</span></span>

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

### <span data-ttu-id="8002e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8002e-125">-ResourceId</span></span>
<span data-ttu-id="8002e-126">Identyfikator zasobu środowiska uruchomieniowego integracji Synapse.</span><span class="sxs-lookup"><span data-stu-id="8002e-126">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="8002e-127">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="8002e-127">-WorkspaceName</span></span>
<span data-ttu-id="8002e-128">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="8002e-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="8002e-129">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="8002e-129">-WorkspaceObject</span></span>
<span data-ttu-id="8002e-130">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="8002e-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="8002e-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8002e-131">-Confirm</span></span>
<span data-ttu-id="8002e-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8002e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8002e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8002e-133">-WhatIf</span></span>
<span data-ttu-id="8002e-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8002e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8002e-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8002e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8002e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8002e-136">CommonParameters</span></span>
<span data-ttu-id="8002e-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8002e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8002e-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8002e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8002e-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8002e-139">INPUTS</span></span>

### <span data-ttu-id="8002e-140">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="8002e-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="8002e-141">Microsoft. Azure. Commands. Synapse. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="8002e-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="8002e-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8002e-142">OUTPUTS</span></span>

### <span data-ttu-id="8002e-143">System. void</span><span class="sxs-lookup"><span data-stu-id="8002e-143">System.Void</span></span>

## <span data-ttu-id="8002e-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8002e-144">NOTES</span></span>

## <span data-ttu-id="8002e-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8002e-145">RELATED LINKS</span></span>
