---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
ms.openlocfilehash: 6203143eb2d386b627d0208730987709b1dd68c4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983946"
---
# <span data-ttu-id="9ac4d-101">Remove-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="9ac4d-101">Remove-AzSynapseNotebook</span></span>

## <span data-ttu-id="9ac4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ac4d-102">SYNOPSIS</span></span>
<span data-ttu-id="9ac4d-103">Usuwa notes z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="9ac4d-103">Removes a notebook from a workspace.</span></span>

## <span data-ttu-id="9ac4d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9ac4d-104">SYNTAX</span></span>

### <span data-ttu-id="9ac4d-105">RemoveByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="9ac4d-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseNotebook -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ac4d-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="9ac4d-106">RemoveByObject</span></span>
```
Remove-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ac4d-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="9ac4d-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseNotebook -InputObject <PSNotebookResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ac4d-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="9ac4d-108">DESCRIPTION</span></span>
<span data-ttu-id="9ac4d-109">Polecenie **cmdlet Remove-AzSynapseNotebook** usuwa notes z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="9ac4d-109">The **Remove-AzSynapseNotebook** cmdlet removes a notebook from a workspace.</span></span>

## <span data-ttu-id="9ac4d-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9ac4d-110">EXAMPLES</span></span>

### <span data-ttu-id="9ac4d-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9ac4d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
```

<span data-ttu-id="9ac4d-112">Usuń notes o nazwie ContosoNotebook z obszaru roboczego ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="9ac4d-112">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="9ac4d-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="9ac4d-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseNotebook -Name ContosoNotebook
```

<span data-ttu-id="9ac4d-114">Usuń notes o nazwie ContosoNotebook z obszaru roboczego ContosoWorkspace z potoku.</span><span class="sxs-lookup"><span data-stu-id="9ac4d-114">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="9ac4d-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="9ac4d-115">Example 3</span></span>
```powershell
PS C:\> $notebook = Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
PS C:\> $notebook | Remove-AzSynapseNotebook
```

<span data-ttu-id="9ac4d-116">Usuń notes o nazwie ContosoNotebook z obszaru roboczego ContosoWorkspace z potoku.</span><span class="sxs-lookup"><span data-stu-id="9ac4d-116">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="9ac4d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ac4d-117">PARAMETERS</span></span>

### <span data-ttu-id="9ac4d-118">— AsJob</span><span class="sxs-lookup"><span data-stu-id="9ac4d-118">-AsJob</span></span>
<span data-ttu-id="9ac4d-119">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9ac4d-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9ac4d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ac4d-120">-DefaultProfile</span></span>
<span data-ttu-id="9ac4d-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9ac4d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ac4d-122">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="9ac4d-122">-Force</span></span>
<span data-ttu-id="9ac4d-123">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9ac4d-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9ac4d-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ac4d-124">-InputObject</span></span>
<span data-ttu-id="9ac4d-125">Obiekt notesu.</span><span class="sxs-lookup"><span data-stu-id="9ac4d-125">The notebook object.</span></span>

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

### <span data-ttu-id="9ac4d-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9ac4d-126">-Name</span></span>
<span data-ttu-id="9ac4d-127">Nazwa notesu.</span><span class="sxs-lookup"><span data-stu-id="9ac4d-127">The notebook name.</span></span>

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

### <span data-ttu-id="9ac4d-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ac4d-128">-PassThru</span></span>
<span data-ttu-id="9ac4d-129">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="9ac4d-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="9ac4d-130">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="9ac4d-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="9ac4d-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9ac4d-131">-WorkspaceName</span></span>
<span data-ttu-id="9ac4d-132">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="9ac4d-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="9ac4d-133">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9ac4d-133">-WorkspaceObject</span></span>
<span data-ttu-id="9ac4d-134">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="9ac4d-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="9ac4d-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9ac4d-135">-Confirm</span></span>
<span data-ttu-id="9ac4d-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9ac4d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ac4d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ac4d-137">-WhatIf</span></span>
<span data-ttu-id="9ac4d-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ac4d-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9ac4d-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9ac4d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ac4d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ac4d-140">CommonParameters</span></span>
<span data-ttu-id="9ac4d-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ac4d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ac4d-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9ac4d-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ac4d-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9ac4d-143">INPUTS</span></span>

### <span data-ttu-id="9ac4d-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="9ac4d-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="9ac4d-145">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="9ac4d-145">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="9ac4d-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9ac4d-146">OUTPUTS</span></span>

### <span data-ttu-id="9ac4d-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9ac4d-147">System.Boolean</span></span>

## <span data-ttu-id="9ac4d-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9ac4d-148">NOTES</span></span>

## <span data-ttu-id="9ac4d-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9ac4d-149">RELATED LINKS</span></span>
