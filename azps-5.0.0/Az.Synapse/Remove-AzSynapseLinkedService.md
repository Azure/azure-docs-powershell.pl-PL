---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseLinkedService.md
ms.openlocfilehash: ca493914cc91d16566fddcebed5367fa81be1d2d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232383"
---
# <span data-ttu-id="99833-101">Remove-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="99833-101">Remove-AzSynapseLinkedService</span></span>

## <span data-ttu-id="99833-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="99833-102">SYNOPSIS</span></span>
<span data-ttu-id="99833-103">Usuwa połączoną usługę z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="99833-103">Removes a linked service from workspace.</span></span>

## <span data-ttu-id="99833-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="99833-104">SYNTAX</span></span>

### <span data-ttu-id="99833-105">RemoveByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="99833-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseLinkedService -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99833-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="99833-106">RemoveByObject</span></span>
```
Remove-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99833-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="99833-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseLinkedService -InputObject <PSLinkedServiceResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99833-108">Opis</span><span class="sxs-lookup"><span data-stu-id="99833-108">DESCRIPTION</span></span>
<span data-ttu-id="99833-109">Polecenie cmdlet **Remove-AzSynapseLinkedService** umożliwia usunięcie połączonej usługi z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="99833-109">The **Remove-AzSynapseLinkedService** cmdlet removes a linked service from workspace.</span></span>

## <span data-ttu-id="99833-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="99833-110">EXAMPLES</span></span>

### <span data-ttu-id="99833-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="99833-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
```

<span data-ttu-id="99833-112">To polecenie powoduje usunięcie połączonej usługi o nazwie ContosoLinkedService z obszaru roboczego o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="99833-112">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="99833-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="99833-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseLinkedService -Name ContosoLinkedService
```

<span data-ttu-id="99833-114">To polecenie powoduje usunięcie połączonej usługi o nazwie ContosoLinkedService z obszaru roboczego o nazwie ContosoWorkspace za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="99833-114">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="99833-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="99833-115">Example 3</span></span>
```powershell
PS C:\> $linkedService = Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
PS C:\> $linkedService | Remove-AzSynapseLinkedService
```

<span data-ttu-id="99833-116">To polecenie powoduje usunięcie połączonej usługi o nazwie ContosoLinkedService z obszaru roboczego o nazwie ContosoWorkspace za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="99833-116">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="99833-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="99833-117">PARAMETERS</span></span>

### <span data-ttu-id="99833-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="99833-118">-AsJob</span></span>
<span data-ttu-id="99833-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="99833-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="99833-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99833-120">-DefaultProfile</span></span>
<span data-ttu-id="99833-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="99833-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99833-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="99833-122">-InputObject</span></span>
<span data-ttu-id="99833-123">Połączony obiekt usługi.</span><span class="sxs-lookup"><span data-stu-id="99833-123">The linked service object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99833-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="99833-124">-Name</span></span>
<span data-ttu-id="99833-125">Nazwa połączonej usługi.</span><span class="sxs-lookup"><span data-stu-id="99833-125">The linked service name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: LinkedServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99833-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="99833-126">-PassThru</span></span>
<span data-ttu-id="99833-127">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="99833-127">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="99833-128">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="99833-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="99833-129">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="99833-129">-WorkspaceName</span></span>
<span data-ttu-id="99833-130">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="99833-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99833-131">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="99833-131">-WorkspaceObject</span></span>
<span data-ttu-id="99833-132">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="99833-132">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99833-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="99833-133">-Confirm</span></span>
<span data-ttu-id="99833-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99833-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99833-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99833-135">-WhatIf</span></span>
<span data-ttu-id="99833-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99833-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="99833-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="99833-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99833-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99833-138">CommonParameters</span></span>
<span data-ttu-id="99833-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99833-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99833-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99833-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99833-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99833-141">INPUTS</span></span>

### <span data-ttu-id="99833-142">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="99833-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="99833-143">Microsoft. Azure. Commands. Synapse. models. PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="99833-143">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="99833-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="99833-144">OUTPUTS</span></span>

### <span data-ttu-id="99833-145">Microsoft. Azure. Commands. Synapse. models. PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="99833-145">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="99833-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="99833-146">NOTES</span></span>

## <span data-ttu-id="99833-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="99833-147">RELATED LINKS</span></span>
