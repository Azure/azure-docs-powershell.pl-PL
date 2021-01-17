---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
ms.openlocfilehash: 23bd6186f31199ab9387df5ee78ce3fdbe89032e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383462"
---
# <span data-ttu-id="b4491-101">Remove-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="b4491-101">Remove-AzSynapseNotebook</span></span>

## <span data-ttu-id="b4491-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b4491-102">SYNOPSIS</span></span>
<span data-ttu-id="b4491-103">Usuwanie notesu z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="b4491-103">Removes a notebook from a workspace.</span></span>

## <span data-ttu-id="b4491-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b4491-104">SYNTAX</span></span>

### <span data-ttu-id="b4491-105">RemoveByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b4491-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseNotebook -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4491-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="b4491-106">RemoveByObject</span></span>
```
Remove-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4491-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="b4491-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseNotebook -InputObject <PSNotebookResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4491-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b4491-108">DESCRIPTION</span></span>
<span data-ttu-id="b4491-109">Polecenie cmdlet **Remove-AzSynapseNotebook** umożliwia usunięcie notesu z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="b4491-109">The **Remove-AzSynapseNotebook** cmdlet removes a notebook from a workspace.</span></span>

## <span data-ttu-id="b4491-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b4491-110">EXAMPLES</span></span>

### <span data-ttu-id="b4491-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b4491-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
```

<span data-ttu-id="b4491-112">Usuwanie notesu o nazwie ContosoNotebook z obszaru roboczego ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="b4491-112">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="b4491-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b4491-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseNotebook -Name ContosoNotebook
```

<span data-ttu-id="b4491-114">Usuwanie notesu o nazwie ContosoNotebook z obszaru roboczego ContosoWorkspace za pomocą rurociągu.</span><span class="sxs-lookup"><span data-stu-id="b4491-114">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="b4491-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="b4491-115">Example 3</span></span>
```powershell
PS C:\> $notebook = Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
PS C:\> $notebook | Remove-AzSynapseNotebook
```

<span data-ttu-id="b4491-116">Usuwanie notesu o nazwie ContosoNotebook z obszaru roboczego ContosoWorkspace za pomocą rurociągu.</span><span class="sxs-lookup"><span data-stu-id="b4491-116">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="b4491-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b4491-117">PARAMETERS</span></span>

### <span data-ttu-id="b4491-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4491-118">-AsJob</span></span>
<span data-ttu-id="b4491-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b4491-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b4491-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4491-120">-DefaultProfile</span></span>
<span data-ttu-id="b4491-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b4491-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4491-122">-Force</span><span class="sxs-lookup"><span data-stu-id="b4491-122">-Force</span></span>
<span data-ttu-id="b4491-123">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b4491-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b4491-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b4491-124">-InputObject</span></span>
<span data-ttu-id="b4491-125">Obiekt notesu.</span><span class="sxs-lookup"><span data-stu-id="b4491-125">The notebook object.</span></span>

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

### <span data-ttu-id="b4491-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b4491-126">-Name</span></span>
<span data-ttu-id="b4491-127">Nazwa notesu.</span><span class="sxs-lookup"><span data-stu-id="b4491-127">The notebook name.</span></span>

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

### <span data-ttu-id="b4491-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b4491-128">-PassThru</span></span>
<span data-ttu-id="b4491-129">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="b4491-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="b4491-130">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="b4491-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="b4491-131">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="b4491-131">-WorkspaceName</span></span>
<span data-ttu-id="b4491-132">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="b4491-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b4491-133">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="b4491-133">-WorkspaceObject</span></span>
<span data-ttu-id="b4491-134">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="b4491-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b4491-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b4491-135">-Confirm</span></span>
<span data-ttu-id="b4491-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4491-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4491-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4491-137">-WhatIf</span></span>
<span data-ttu-id="b4491-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4491-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b4491-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b4491-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4491-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4491-140">CommonParameters</span></span>
<span data-ttu-id="b4491-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4491-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4491-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4491-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4491-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4491-143">INPUTS</span></span>

### <span data-ttu-id="b4491-144">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b4491-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="b4491-145">Microsoft. Azure. Commands. Synapse. models. PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="b4491-145">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="b4491-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b4491-146">OUTPUTS</span></span>

### <span data-ttu-id="b4491-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b4491-147">System.Boolean</span></span>

## <span data-ttu-id="b4491-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b4491-148">NOTES</span></span>

## <span data-ttu-id="b4491-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b4491-149">RELATED LINKS</span></span>
