---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapseintegrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseIntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseIntegrationRuntimeKey.md
ms.openlocfilehash: 836dcabaa190b66daf5a4f3f2fdaf300fe47ccdf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219687"
---
# <span data-ttu-id="65d25-101">New-AzSynapseIntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="65d25-101">New-AzSynapseIntegrationRuntimeKey</span></span>

## <span data-ttu-id="65d25-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="65d25-102">SYNOPSIS</span></span>
<span data-ttu-id="65d25-103">Ponowne generowanie klucza środowiska uruchomieniowego w ramach samodzielnej integracji.</span><span class="sxs-lookup"><span data-stu-id="65d25-103">Regenerate self-hosted integration runtime key.</span></span>

## <span data-ttu-id="65d25-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="65d25-104">SYNTAX</span></span>

### <span data-ttu-id="65d25-105">NewByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="65d25-105">NewByNameParameterSet (Default)</span></span>
```
New-AzSynapseIntegrationRuntimeKey [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -KeyName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="65d25-106">NewByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="65d25-106">NewByParentObjectParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -Name <String> -WorkspaceObject <PSSynapseWorkspace> -KeyName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65d25-107">NewByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="65d25-107">NewByResourceIdParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -ResourceId <String> -KeyName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65d25-108">NewByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="65d25-108">NewByInputObjectParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -InputObject <PSIntegrationRuntime> -KeyName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65d25-109">Opis</span><span class="sxs-lookup"><span data-stu-id="65d25-109">DESCRIPTION</span></span>
<span data-ttu-id="65d25-110">Polecenie cmdlet **New-AzSynapseIntegrationRuntimeKey** generuje ponownie klucz środowiska uruchomieniowego integracji z nazwą klucza określoną przez parametr "KeyName".</span><span class="sxs-lookup"><span data-stu-id="65d25-110">The cmdlet **New-AzSynapseIntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="65d25-111">Poprzedni klucz będzie nieprawidłowy.</span><span class="sxs-lookup"><span data-stu-id="65d25-111">The previous key will is invalid.</span></span>

## <span data-ttu-id="65d25-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="65d25-112">EXAMPLES</span></span>

### <span data-ttu-id="65d25-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="65d25-113">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseIntegrationRuntimeKey -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -KeyName authKey2
```

<span data-ttu-id="65d25-114">Polecenie cmdlet regeneruje klucz "authKey2" dla środowiska uruchomieniowego integracji o nazwie "test-SelfHost-IR".</span><span class="sxs-lookup"><span data-stu-id="65d25-114">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="65d25-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="65d25-115">PARAMETERS</span></span>

### <span data-ttu-id="65d25-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65d25-116">-DefaultProfile</span></span>
<span data-ttu-id="65d25-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="65d25-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65d25-118">-Force</span><span class="sxs-lookup"><span data-stu-id="65d25-118">-Force</span></span>
<span data-ttu-id="65d25-119">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="65d25-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="65d25-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="65d25-120">-InputObject</span></span>
<span data-ttu-id="65d25-121">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="65d25-121">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: NewByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65d25-122">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="65d25-122">-KeyName</span></span>
<span data-ttu-id="65d25-123">Nazwa klucza uwierzytelniania w ramach samodzielnego środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="65d25-123">The authentication key name of the self-hosted integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AuthKey1, AuthKey2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d25-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="65d25-124">-Name</span></span>
<span data-ttu-id="65d25-125">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="65d25-125">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByNameParameterSet, NewByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d25-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65d25-126">-ResourceGroupName</span></span>
<span data-ttu-id="65d25-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="65d25-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d25-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65d25-128">-ResourceId</span></span>
<span data-ttu-id="65d25-129">Identyfikator zasobu środowiska uruchomieniowego integracji Synapse.</span><span class="sxs-lookup"><span data-stu-id="65d25-129">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d25-130">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="65d25-130">-WorkspaceName</span></span>
<span data-ttu-id="65d25-131">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="65d25-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d25-132">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="65d25-132">-WorkspaceObject</span></span>
<span data-ttu-id="65d25-133">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="65d25-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: NewByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65d25-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="65d25-134">-Confirm</span></span>
<span data-ttu-id="65d25-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65d25-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65d25-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65d25-136">-WhatIf</span></span>
<span data-ttu-id="65d25-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65d25-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65d25-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="65d25-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65d25-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65d25-139">CommonParameters</span></span>
<span data-ttu-id="65d25-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65d25-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65d25-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65d25-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65d25-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="65d25-142">INPUTS</span></span>

### <span data-ttu-id="65d25-143">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="65d25-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="65d25-144">Microsoft. Azure. Commands. Synapse. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="65d25-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="65d25-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="65d25-145">OUTPUTS</span></span>

### <span data-ttu-id="65d25-146">Microsoft. Azure. Commands. Synapse. models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="65d25-146">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="65d25-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="65d25-147">NOTES</span></span>

## <span data-ttu-id="65d25-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="65d25-148">RELATED LINKS</span></span>
