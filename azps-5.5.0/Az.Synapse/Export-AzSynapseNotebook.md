---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/export-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Export-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Export-AzSynapseNotebook.md
ms.openlocfilehash: d61038add8ded9f697bfef551e00aec24c8aaf3e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243131"
---
# <span data-ttu-id="76e1f-101">Export-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="76e1f-101">Export-AzSynapseNotebook</span></span>

## <span data-ttu-id="76e1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76e1f-102">SYNOPSIS</span></span>
<span data-ttu-id="76e1f-103">Eksportuje podręczniki.</span><span class="sxs-lookup"><span data-stu-id="76e1f-103">Exports notbooks.</span></span>

## <span data-ttu-id="76e1f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="76e1f-104">SYNTAX</span></span>

### <span data-ttu-id="76e1f-105">ExportByName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="76e1f-105">ExportByName (Default)</span></span>
```
Export-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76e1f-106">ExportByObject</span><span class="sxs-lookup"><span data-stu-id="76e1f-106">ExportByObject</span></span>
```
Export-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76e1f-107">ExportByInputObject</span><span class="sxs-lookup"><span data-stu-id="76e1f-107">ExportByInputObject</span></span>
```
Export-AzSynapseNotebook -InputObject <PSNotebookResource> -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76e1f-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="76e1f-108">DESCRIPTION</span></span>
<span data-ttu-id="76e1f-109">Polecenie **cmdlet Export-AzSynapseNotebook** umożliwia wyeksportowanie notesu Azure Synapse do pliku notesu (ipynb).</span><span class="sxs-lookup"><span data-stu-id="76e1f-109">The **Export-AzSynapseNotebook** cmdlet exports an Azure Synapse notebook to a notebook (.ipynb) file.</span></span> <span data-ttu-id="76e1f-110">Nazwa notesu stanie się nazwą wyeksportowanego pliku.</span><span class="sxs-lookup"><span data-stu-id="76e1f-110">The name of the notebook becomes the name of the exported file.</span></span> <span data-ttu-id="76e1f-111">Jeśli określisz nazwę notesu, polecenie cmdlet wyekeruje ten notes.</span><span class="sxs-lookup"><span data-stu-id="76e1f-111">If you specify the name of a notebook, the cmdlet exports that notebook.</span></span> <span data-ttu-id="76e1f-112">Jeśli nie określisz nazwy, polecenie cmdlet wyeksportuje wszystkie notesy w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="76e1f-112">If you do not specify a name, the cmdlet export all notebooks in the workspace.</span></span>

## <span data-ttu-id="76e1f-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="76e1f-113">EXAMPLES</span></span>

### <span data-ttu-id="76e1f-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="76e1f-114">Example 1</span></span>
```powershell
PS C:\> Export-AzSynapseNotebook -WorkspaceName ContosoWorkspace -OutputFolder "C:\Notebook"
```

<span data-ttu-id="76e1f-115">Eksportuje wszystkie notesy z obszaru roboczego ContosoWorkspace do folderu "C:\Notes".</span><span class="sxs-lookup"><span data-stu-id="76e1f-115">Exports all notebooks in the workspace ContosoWorkspace to the folder "C:\Notebook".</span></span>

### <span data-ttu-id="76e1f-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="76e1f-116">Example 2</span></span>
```powershell
PS C:\> Export-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="76e1f-117">Eksportuje pojedynczy notes o nazwie ContosoNotebook w obszarze roboczym ContosoWorkspace do folderu "C:\Notes".</span><span class="sxs-lookup"><span data-stu-id="76e1f-117">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook".</span></span>

### <span data-ttu-id="76e1f-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="76e1f-118">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Export-AzSynapseNotebook -Name ContosoNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="76e1f-119">Eksportuje pojedynczy notes o nazwie ContosoNotebook w obszarze roboczym ContosoWorkspace do folderu "C:\Notes" za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="76e1f-119">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook" through pipeline.</span></span>

### <span data-ttu-id="76e1f-120">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="76e1f-120">Example 4</span></span>
```powershell
PS C:\> $notebook = Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
PS C:\> $notebook | Export-AzSynapseNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="76e1f-121">Eksportuje pojedynczy notes o nazwie ContosoNotebook w obszarze roboczym ContosoWorkspace do folderu "C:\Notes" za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="76e1f-121">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook" through pipeline.</span></span>

## <span data-ttu-id="76e1f-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76e1f-122">PARAMETERS</span></span>

### <span data-ttu-id="76e1f-123">— AsJob</span><span class="sxs-lookup"><span data-stu-id="76e1f-123">-AsJob</span></span>
<span data-ttu-id="76e1f-124">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="76e1f-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="76e1f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76e1f-125">-DefaultProfile</span></span>
<span data-ttu-id="76e1f-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="76e1f-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76e1f-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76e1f-127">-InputObject</span></span>
<span data-ttu-id="76e1f-128">Obiekt notesu.</span><span class="sxs-lookup"><span data-stu-id="76e1f-128">The notebook object.</span></span>

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

### <span data-ttu-id="76e1f-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="76e1f-129">-Name</span></span>
<span data-ttu-id="76e1f-130">Nazwa notesu.</span><span class="sxs-lookup"><span data-stu-id="76e1f-130">The notebook name.</span></span>

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

### <span data-ttu-id="76e1f-131">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="76e1f-131">-OutputFolder</span></span>
<span data-ttu-id="76e1f-132">Folder, w którym powinien się znaleźć notes.</span><span class="sxs-lookup"><span data-stu-id="76e1f-132">The folder where the notebook should be placed.</span></span>

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

### <span data-ttu-id="76e1f-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="76e1f-133">-WorkspaceName</span></span>
<span data-ttu-id="76e1f-134">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="76e1f-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="76e1f-135">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="76e1f-135">-WorkspaceObject</span></span>
<span data-ttu-id="76e1f-136">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="76e1f-136">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="76e1f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76e1f-137">CommonParameters</span></span>
<span data-ttu-id="76e1f-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76e1f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76e1f-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76e1f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76e1f-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76e1f-140">INPUTS</span></span>

### <span data-ttu-id="76e1f-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="76e1f-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="76e1f-142">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="76e1f-142">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="76e1f-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76e1f-143">OUTPUTS</span></span>

### <span data-ttu-id="76e1f-144">System.IO.FileInfo</span><span class="sxs-lookup"><span data-stu-id="76e1f-144">System.IO.FileInfo</span></span>

## <span data-ttu-id="76e1f-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="76e1f-145">NOTES</span></span>

## <span data-ttu-id="76e1f-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="76e1f-146">RELATED LINKS</span></span>
