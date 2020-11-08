---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
ms.openlocfilehash: 22570fa8d236675a8ad2acd712e1ff66c1bc5049
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064380"
---
# <span data-ttu-id="e62d6-101">Remove-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="e62d6-101">Remove-AzSynapseNotebook</span></span>

## <span data-ttu-id="e62d6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e62d6-102">SYNOPSIS</span></span>
<span data-ttu-id="e62d6-103">Usuwanie notesu z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="e62d6-103">Removes a notebook from a workspace.</span></span>

## <span data-ttu-id="e62d6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e62d6-104">SYNTAX</span></span>

### <span data-ttu-id="e62d6-105">RemoveByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e62d6-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseNotebook -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e62d6-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="e62d6-106">RemoveByObject</span></span>
```
Remove-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e62d6-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="e62d6-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseNotebook -InputObject <PSNotebookResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e62d6-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e62d6-108">DESCRIPTION</span></span>
<span data-ttu-id="e62d6-109">Polecenie cmdlet **Remove-AzSynapseNotebook** umożliwia usunięcie notesu z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="e62d6-109">The **Remove-AzSynapseNotebook** cmdlet removes a notebook from a workspace.</span></span>

## <span data-ttu-id="e62d6-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e62d6-110">EXAMPLES</span></span>

### <span data-ttu-id="e62d6-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e62d6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
```

<span data-ttu-id="e62d6-112">Usuwanie notesu o nazwie ContosoNotebook z obszaru roboczego ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="e62d6-112">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="e62d6-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e62d6-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseNotebook -Name ContosoNotebook
```

<span data-ttu-id="e62d6-114">Usuwanie notesu o nazwie ContosoNotebook z obszaru roboczego ContosoWorkspace za pomocą rurociągu.</span><span class="sxs-lookup"><span data-stu-id="e62d6-114">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="e62d6-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="e62d6-115">Example 3</span></span>
```powershell
PS C:\> $notebook = Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
PS C:\> $notebook | Remove-AzSynapseNotebook
```

<span data-ttu-id="e62d6-116">Usuwanie notesu o nazwie ContosoNotebook z obszaru roboczego ContosoWorkspace za pomocą rurociągu.</span><span class="sxs-lookup"><span data-stu-id="e62d6-116">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="e62d6-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e62d6-117">PARAMETERS</span></span>

### <span data-ttu-id="e62d6-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e62d6-118">-AsJob</span></span>
<span data-ttu-id="e62d6-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e62d6-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e62d6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e62d6-120">-DefaultProfile</span></span>
<span data-ttu-id="e62d6-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e62d6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e62d6-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e62d6-122">-InputObject</span></span>
<span data-ttu-id="e62d6-123">Obiekt notesu.</span><span class="sxs-lookup"><span data-stu-id="e62d6-123">The notebook object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e62d6-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e62d6-124">-Name</span></span>
<span data-ttu-id="e62d6-125">Nazwa notesu.</span><span class="sxs-lookup"><span data-stu-id="e62d6-125">The notebook name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: NotebookName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62d6-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e62d6-126">-PassThru</span></span>
<span data-ttu-id="e62d6-127">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="e62d6-127">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="e62d6-128">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="e62d6-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="e62d6-129">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="e62d6-129">-WorkspaceName</span></span>
<span data-ttu-id="e62d6-130">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="e62d6-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e62d6-131">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="e62d6-131">-WorkspaceObject</span></span>
<span data-ttu-id="e62d6-132">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="e62d6-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e62d6-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e62d6-133">-Confirm</span></span>
<span data-ttu-id="e62d6-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e62d6-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e62d6-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e62d6-135">-WhatIf</span></span>
<span data-ttu-id="e62d6-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e62d6-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e62d6-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e62d6-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e62d6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e62d6-138">CommonParameters</span></span>
<span data-ttu-id="e62d6-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e62d6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e62d6-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e62d6-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e62d6-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e62d6-141">INPUTS</span></span>

### <span data-ttu-id="e62d6-142">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e62d6-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="e62d6-143">Microsoft. Azure. Commands. Synapse. models. PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="e62d6-143">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="e62d6-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e62d6-144">OUTPUTS</span></span>

### <span data-ttu-id="e62d6-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e62d6-145">System.Boolean</span></span>

## <span data-ttu-id="e62d6-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e62d6-146">NOTES</span></span>

## <span data-ttu-id="e62d6-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e62d6-147">RELATED LINKS</span></span>
