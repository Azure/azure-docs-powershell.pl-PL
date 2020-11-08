---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/export-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Export-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Export-AzSynapseNotebook.md
ms.openlocfilehash: d61038add8ded9f697bfef551e00aec24c8aaf3e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220201"
---
# <span data-ttu-id="8ed9e-101">Export-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="8ed9e-101">Export-AzSynapseNotebook</span></span>

## <span data-ttu-id="8ed9e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8ed9e-102">SYNOPSIS</span></span>
<span data-ttu-id="8ed9e-103">Eksportuje notbooks.</span><span class="sxs-lookup"><span data-stu-id="8ed9e-103">Exports notbooks.</span></span>

## <span data-ttu-id="8ed9e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8ed9e-104">SYNTAX</span></span>

### <span data-ttu-id="8ed9e-105">ExportByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8ed9e-105">ExportByName (Default)</span></span>
```
Export-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ed9e-106">ExportByObject</span><span class="sxs-lookup"><span data-stu-id="8ed9e-106">ExportByObject</span></span>
```
Export-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ed9e-107">ExportByInputObject</span><span class="sxs-lookup"><span data-stu-id="8ed9e-107">ExportByInputObject</span></span>
```
Export-AzSynapseNotebook -InputObject <PSNotebookResource> -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ed9e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8ed9e-108">DESCRIPTION</span></span>
<span data-ttu-id="8ed9e-109">Polecenie cmdlet **Export-AzSynapseNotebook** eksportuje Notes Azure Synapse do pliku notesu (ipynb).</span><span class="sxs-lookup"><span data-stu-id="8ed9e-109">The **Export-AzSynapseNotebook** cmdlet exports an Azure Synapse notebook to a notebook (.ipynb) file.</span></span> <span data-ttu-id="8ed9e-110">Nazwa notesu stanie się nazwą eksportowanego pliku.</span><span class="sxs-lookup"><span data-stu-id="8ed9e-110">The name of the notebook becomes the name of the exported file.</span></span> <span data-ttu-id="8ed9e-111">Jeśli określisz nazwę notesu, polecenie cmdlet wyeksportuj ten Notes.</span><span class="sxs-lookup"><span data-stu-id="8ed9e-111">If you specify the name of a notebook, the cmdlet exports that notebook.</span></span> <span data-ttu-id="8ed9e-112">Jeśli nie określisz nazwy, polecenie cmdlet wyeksportuj wszystkie notesy w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="8ed9e-112">If you do not specify a name, the cmdlet export all notebooks in the workspace.</span></span>

## <span data-ttu-id="8ed9e-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8ed9e-113">EXAMPLES</span></span>

### <span data-ttu-id="8ed9e-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8ed9e-114">Example 1</span></span>
```powershell
PS C:\> Export-AzSynapseNotebook -WorkspaceName ContosoWorkspace -OutputFolder "C:\Notebook"
```

<span data-ttu-id="8ed9e-115">Eksportuje wszystkie notesy w obszarze roboczym ContosoWorkspace do folderu "C:\Notebook".</span><span class="sxs-lookup"><span data-stu-id="8ed9e-115">Exports all notebooks in the workspace ContosoWorkspace to the folder "C:\Notebook".</span></span>

### <span data-ttu-id="8ed9e-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8ed9e-116">Example 2</span></span>
```powershell
PS C:\> Export-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="8ed9e-117">Umożliwia wyeksportowanie pojedynczego notesu o nazwie ContosoNotebook w obszarze roboczym ContosoWorkspace do folderu "C:\Notebook".</span><span class="sxs-lookup"><span data-stu-id="8ed9e-117">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook".</span></span>

### <span data-ttu-id="8ed9e-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="8ed9e-118">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Export-AzSynapseNotebook -Name ContosoNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="8ed9e-119">Umożliwia wyeksportowanie pojedynczego notesu o nazwie ContosoNotebook w obszarze roboczym ContosoWorkspace do folderu "C:\Notebook" za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="8ed9e-119">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook" through pipeline.</span></span>

### <span data-ttu-id="8ed9e-120">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="8ed9e-120">Example 4</span></span>
```powershell
PS C:\> $notebook = Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
PS C:\> $notebook | Export-AzSynapseNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="8ed9e-121">Umożliwia wyeksportowanie pojedynczego notesu o nazwie ContosoNotebook w obszarze roboczym ContosoWorkspace do folderu "C:\Notebook" za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="8ed9e-121">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook" through pipeline.</span></span>

## <span data-ttu-id="8ed9e-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8ed9e-122">PARAMETERS</span></span>

### <span data-ttu-id="8ed9e-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8ed9e-123">-AsJob</span></span>
<span data-ttu-id="8ed9e-124">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="8ed9e-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8ed9e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ed9e-125">-DefaultProfile</span></span>
<span data-ttu-id="8ed9e-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8ed9e-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ed9e-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8ed9e-127">-InputObject</span></span>
<span data-ttu-id="8ed9e-128">Obiekt notesu.</span><span class="sxs-lookup"><span data-stu-id="8ed9e-128">The notebook object.</span></span>

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

### <span data-ttu-id="8ed9e-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8ed9e-129">-Name</span></span>
<span data-ttu-id="8ed9e-130">Nazwa notesu.</span><span class="sxs-lookup"><span data-stu-id="8ed9e-130">The notebook name.</span></span>

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

### <span data-ttu-id="8ed9e-131">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="8ed9e-131">-OutputFolder</span></span>
<span data-ttu-id="8ed9e-132">Folder, w którym ma zostać umieszczony Notes.</span><span class="sxs-lookup"><span data-stu-id="8ed9e-132">The folder where the notebook should be placed.</span></span>

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

### <span data-ttu-id="8ed9e-133">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="8ed9e-133">-WorkspaceName</span></span>
<span data-ttu-id="8ed9e-134">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="8ed9e-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="8ed9e-135">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="8ed9e-135">-WorkspaceObject</span></span>
<span data-ttu-id="8ed9e-136">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="8ed9e-136">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="8ed9e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ed9e-137">CommonParameters</span></span>
<span data-ttu-id="8ed9e-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ed9e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ed9e-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ed9e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ed9e-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ed9e-140">INPUTS</span></span>

### <span data-ttu-id="8ed9e-141">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="8ed9e-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="8ed9e-142">Microsoft. Azure. Commands. Synapse. models. PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="8ed9e-142">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="8ed9e-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8ed9e-143">OUTPUTS</span></span>

### <span data-ttu-id="8ed9e-144">System. IO. FileInfo</span><span class="sxs-lookup"><span data-stu-id="8ed9e-144">System.IO.FileInfo</span></span>

## <span data-ttu-id="8ed9e-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8ed9e-145">NOTES</span></span>

## <span data-ttu-id="8ed9e-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8ed9e-146">RELATED LINKS</span></span>
