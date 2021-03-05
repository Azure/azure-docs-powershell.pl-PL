---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/new-azsynapseintegrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseIntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseIntegrationRuntimeKey.md
ms.openlocfilehash: 143238bfcc8dffc209150a675af0a982d20663bb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976081"
---
# <span data-ttu-id="e716c-101">New-AzSynapseIntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="e716c-101">New-AzSynapseIntegrationRuntimeKey</span></span>

## <span data-ttu-id="e716c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e716c-102">SYNOPSIS</span></span>
<span data-ttu-id="e716c-103">Generuj samodzielnie hostowany klucz środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="e716c-103">Regenerate self-hosted integration runtime key.</span></span>

## <span data-ttu-id="e716c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e716c-104">SYNTAX</span></span>

### <span data-ttu-id="e716c-105">NewByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="e716c-105">NewByNameParameterSet (Default)</span></span>
```
New-AzSynapseIntegrationRuntimeKey [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -KeyName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e716c-106">NewByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e716c-106">NewByParentObjectParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -Name <String> -WorkspaceObject <PSSynapseWorkspace> -KeyName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e716c-107">NewByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e716c-107">NewByResourceIdParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -ResourceId <String> -KeyName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e716c-108">NewByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e716c-108">NewByInputObjectParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -InputObject <PSIntegrationRuntime> -KeyName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e716c-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="e716c-109">DESCRIPTION</span></span>
<span data-ttu-id="e716c-110">Polecenie cmdlet **New-AzSynapseIntegrationRuntimeKey** ponownie generuje klucz środowiska uruchomieniowego integracji przy użyciu nazwy klucza określonej przez parametr "KeyName".</span><span class="sxs-lookup"><span data-stu-id="e716c-110">The cmdlet **New-AzSynapseIntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="e716c-111">Poprzedni klucz jest nieprawidłowy.</span><span class="sxs-lookup"><span data-stu-id="e716c-111">The previous key will is invalid.</span></span>

## <span data-ttu-id="e716c-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e716c-112">EXAMPLES</span></span>

### <span data-ttu-id="e716c-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e716c-113">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseIntegrationRuntimeKey -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -KeyName authKey2
```

<span data-ttu-id="e716c-114">Polecenie cmdlet ponownie generuje klucz "authKey2" dla środowiska uruchomieniowego integracji o nazwie "test-selfhost-ir".</span><span class="sxs-lookup"><span data-stu-id="e716c-114">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="e716c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e716c-115">PARAMETERS</span></span>

### <span data-ttu-id="e716c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e716c-116">-DefaultProfile</span></span>
<span data-ttu-id="e716c-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e716c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e716c-118">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="e716c-118">-Force</span></span>
<span data-ttu-id="e716c-119">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e716c-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="e716c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e716c-120">-InputObject</span></span>
<span data-ttu-id="e716c-121">Obiekt środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="e716c-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="e716c-122">-KeyName</span><span class="sxs-lookup"><span data-stu-id="e716c-122">-KeyName</span></span>
<span data-ttu-id="e716c-123">Nazwa klucza uwierzytelniania środowiska integracji samoobsługowej.</span><span class="sxs-lookup"><span data-stu-id="e716c-123">The authentication key name of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="e716c-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e716c-124">-Name</span></span>
<span data-ttu-id="e716c-125">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="e716c-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="e716c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e716c-126">-ResourceGroupName</span></span>
<span data-ttu-id="e716c-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e716c-127">Resource group name.</span></span>

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

### <span data-ttu-id="e716c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e716c-128">-ResourceId</span></span>
<span data-ttu-id="e716c-129">Identyfikator zasobu środowiska uruchomieniowego integracji Synapse.</span><span class="sxs-lookup"><span data-stu-id="e716c-129">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="e716c-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e716c-130">-WorkspaceName</span></span>
<span data-ttu-id="e716c-131">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="e716c-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e716c-132">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e716c-132">-WorkspaceObject</span></span>
<span data-ttu-id="e716c-133">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="e716c-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e716c-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e716c-134">-Confirm</span></span>
<span data-ttu-id="e716c-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e716c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e716c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e716c-136">-WhatIf</span></span>
<span data-ttu-id="e716c-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e716c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e716c-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e716c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e716c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e716c-139">CommonParameters</span></span>
<span data-ttu-id="e716c-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e716c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e716c-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e716c-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e716c-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e716c-142">INPUTS</span></span>

### <span data-ttu-id="e716c-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e716c-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="e716c-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e716c-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="e716c-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e716c-145">OUTPUTS</span></span>

### <span data-ttu-id="e716c-146">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="e716c-146">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="e716c-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e716c-147">NOTES</span></span>

## <span data-ttu-id="e716c-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e716c-148">RELATED LINKS</span></span>
