---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/export-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Export-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Export-AzSynapseNotebook.md
ms.openlocfilehash: 110d72f0a73a6a710e014a08c64cadf3b8be7d0e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981866"
---
# <span data-ttu-id="75b82-101">Export-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="75b82-101">Export-AzSynapseNotebook</span></span>

## <span data-ttu-id="75b82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75b82-102">SYNOPSIS</span></span>
<span data-ttu-id="75b82-103">Eksportuje podręczniki.</span><span class="sxs-lookup"><span data-stu-id="75b82-103">Exports notbooks.</span></span>

## <span data-ttu-id="75b82-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="75b82-104">SYNTAX</span></span>

### <span data-ttu-id="75b82-105">ExportByName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="75b82-105">ExportByName (Default)</span></span>
```
Export-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75b82-106">ExportByObject</span><span class="sxs-lookup"><span data-stu-id="75b82-106">ExportByObject</span></span>
```
Export-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75b82-107">ExportByInputObject</span><span class="sxs-lookup"><span data-stu-id="75b82-107">ExportByInputObject</span></span>
```
Export-AzSynapseNotebook -InputObject <PSNotebookResource> -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75b82-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="75b82-108">DESCRIPTION</span></span>
<span data-ttu-id="75b82-109">Polecenie **cmdlet Export-AzSynapseNotebook** umożliwia wyeksportowanie notesu Azure Synapse do pliku notesu (ipynb).</span><span class="sxs-lookup"><span data-stu-id="75b82-109">The **Export-AzSynapseNotebook** cmdlet exports an Azure Synapse notebook to a notebook (.ipynb) file.</span></span> <span data-ttu-id="75b82-110">Nazwa notesu stanie się nazwą wyeksportowanego pliku.</span><span class="sxs-lookup"><span data-stu-id="75b82-110">The name of the notebook becomes the name of the exported file.</span></span> <span data-ttu-id="75b82-111">Jeśli określisz nazwę notesu, polecenie cmdlet wyekeruje ten notes.</span><span class="sxs-lookup"><span data-stu-id="75b82-111">If you specify the name of a notebook, the cmdlet exports that notebook.</span></span> <span data-ttu-id="75b82-112">Jeśli nie określisz nazwy, polecenie cmdlet wyeksportuje wszystkie notesy w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="75b82-112">If you do not specify a name, the cmdlet export all notebooks in the workspace.</span></span>

## <span data-ttu-id="75b82-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="75b82-113">EXAMPLES</span></span>

### <span data-ttu-id="75b82-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="75b82-114">Example 1</span></span>
```powershell
PS C:\> Export-AzSynapseNotebook -WorkspaceName ContosoWorkspace -OutputFolder "C:\Notebook"
```

<span data-ttu-id="75b82-115">Eksportuje wszystkie notesy z obszaru roboczego ContosoWorkspace do folderu "C:\Notes".</span><span class="sxs-lookup"><span data-stu-id="75b82-115">Exports all notebooks in the workspace ContosoWorkspace to the folder "C:\Notebook".</span></span>

### <span data-ttu-id="75b82-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="75b82-116">Example 2</span></span>
```powershell
PS C:\> Export-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="75b82-117">Eksportuje pojedynczy notes o nazwie ContosoNotebook w obszarze roboczym ContosoWorkspace do folderu "C:\Notes".</span><span class="sxs-lookup"><span data-stu-id="75b82-117">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook".</span></span>

### <span data-ttu-id="75b82-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="75b82-118">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Export-AzSynapseNotebook -Name ContosoNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="75b82-119">Eksportuje pojedynczy notes o nazwie ContosoNotebook w obszarze roboczym ContosoWorkspace do folderu "C:\Notes" za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="75b82-119">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook" through pipeline.</span></span>

### <span data-ttu-id="75b82-120">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="75b82-120">Example 4</span></span>
```powershell
PS C:\> $notebook = Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
PS C:\> $notebook | Export-AzSynapseNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="75b82-121">Eksportuje pojedynczy notes o nazwie ContosoNotebook w obszarze roboczym ContosoWorkspace do folderu "C:\Notes" za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="75b82-121">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook" through pipeline.</span></span>

## <span data-ttu-id="75b82-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75b82-122">PARAMETERS</span></span>

### <span data-ttu-id="75b82-123">— AsJob</span><span class="sxs-lookup"><span data-stu-id="75b82-123">-AsJob</span></span>
<span data-ttu-id="75b82-124">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="75b82-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="75b82-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75b82-125">-DefaultProfile</span></span>
<span data-ttu-id="75b82-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="75b82-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75b82-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75b82-127">-InputObject</span></span>
<span data-ttu-id="75b82-128">Obiekt notesu.</span><span class="sxs-lookup"><span data-stu-id="75b82-128">The notebook object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource
Parameter Sets: ExportByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75b82-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="75b82-129">-Name</span></span>
<span data-ttu-id="75b82-130">Nazwa notesu.</span><span class="sxs-lookup"><span data-stu-id="75b82-130">The notebook name.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByName, ExportByObject
Aliases: NotebookName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75b82-131">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="75b82-131">-OutputFolder</span></span>
<span data-ttu-id="75b82-132">Folder, w którym powinien się znaleźć notes.</span><span class="sxs-lookup"><span data-stu-id="75b82-132">The folder where the notebook should be placed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75b82-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="75b82-133">-WorkspaceName</span></span>
<span data-ttu-id="75b82-134">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="75b82-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75b82-135">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="75b82-135">-WorkspaceObject</span></span>
<span data-ttu-id="75b82-136">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="75b82-136">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: ExportByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75b82-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75b82-137">CommonParameters</span></span>
<span data-ttu-id="75b82-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75b82-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75b82-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="75b82-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75b82-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="75b82-140">INPUTS</span></span>

### <span data-ttu-id="75b82-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="75b82-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="75b82-142">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="75b82-142">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="75b82-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="75b82-143">OUTPUTS</span></span>

### <span data-ttu-id="75b82-144">System.IO.FileInfo</span><span class="sxs-lookup"><span data-stu-id="75b82-144">System.IO.FileInfo</span></span>

## <span data-ttu-id="75b82-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="75b82-145">NOTES</span></span>

## <span data-ttu-id="75b82-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="75b82-146">RELATED LINKS</span></span>
