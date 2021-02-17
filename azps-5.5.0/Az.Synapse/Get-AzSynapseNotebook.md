---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseNotebook.md
ms.openlocfilehash: 28a4742b2e744fb41bca9402a8c48b830554e231
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241747"
---
# <span data-ttu-id="a4e05-101">Get-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="a4e05-101">Get-AzSynapseNotebook</span></span>

## <span data-ttu-id="a4e05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4e05-102">SYNOPSIS</span></span>
<span data-ttu-id="a4e05-103">Pobiera informacje o notesach w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="a4e05-103">Gets information about notebooks in a workspace.</span></span>

## <span data-ttu-id="a4e05-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a4e05-104">SYNTAX</span></span>

### <span data-ttu-id="a4e05-105">GetByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="a4e05-105">GetByName (Default)</span></span>
```
Get-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a4e05-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="a4e05-106">GetByObject</span></span>
```
Get-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4e05-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="a4e05-107">DESCRIPTION</span></span>
<span data-ttu-id="a4e05-108">Polecenie **cmdlet Get-AzSynapseNotebook** pobiera informacje o notesach w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="a4e05-108">The **Get-AzSynapseNotebook** cmdlet gets information about notebooks in a workspace.</span></span> <span data-ttu-id="a4e05-109">Jeśli określisz nazwę notesu, polecenie cmdlet pobiera informacje o tym notesie.</span><span class="sxs-lookup"><span data-stu-id="a4e05-109">If you specify the name of a notebook, the cmdlet gets information about that notebook.</span></span> <span data-ttu-id="a4e05-110">Jeśli nie określisz nazwy, polecenie cmdlet pobiera informacje o wszystkich notesach w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="a4e05-110">If you do not specify a name, the cmdlet gets information about all notebooks in the workspace.</span></span>

## <span data-ttu-id="a4e05-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a4e05-111">EXAMPLES</span></span>

### <span data-ttu-id="a4e05-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a4e05-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace | Format-Table

WorkspaceName    Properties                                         Name
-------------    ----------                                         --
ContosoWorkspace Microsoft.Azure.Commands.Synapse.Models.PSNotebook ContosoNotebook1
ContosoWorkspace Microsoft.Azure.Commands.Synapse.Models.PSNotebook ContosoNotebook2
```

<span data-ttu-id="a4e05-113">Pobiera listę wszystkich notesów w obszarze roboczym ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a4e05-113">Gets a list of all notebooks in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="a4e05-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a4e05-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
```

<span data-ttu-id="a4e05-115">Pobiera jeden notes o nazwie ContosoNotebook w obszarze roboczym ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a4e05-115">Gets a single notebook called ContosoNotebook in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="a4e05-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="a4e05-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseNotebook -Name ContosoNotebook
```

<span data-ttu-id="a4e05-117">Pobiera jeden notes o nazwie ContosoNotebook w obszarze roboczym ContosoWorkspace za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="a4e05-117">Gets a single notebook called ContosoNotebook in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="a4e05-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4e05-118">PARAMETERS</span></span>

### <span data-ttu-id="a4e05-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4e05-119">-DefaultProfile</span></span>
<span data-ttu-id="a4e05-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a4e05-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4e05-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a4e05-121">-Name</span></span>
<span data-ttu-id="a4e05-122">Nazwa notesu.</span><span class="sxs-lookup"><span data-stu-id="a4e05-122">The notebook name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NotebookName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4e05-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a4e05-123">-WorkspaceName</span></span>
<span data-ttu-id="a4e05-124">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="a4e05-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4e05-125">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a4e05-125">-WorkspaceObject</span></span>
<span data-ttu-id="a4e05-126">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="a4e05-126">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4e05-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4e05-127">CommonParameters</span></span>
<span data-ttu-id="a4e05-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4e05-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4e05-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a4e05-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4e05-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4e05-130">INPUTS</span></span>

### <span data-ttu-id="a4e05-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a4e05-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a4e05-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a4e05-132">OUTPUTS</span></span>

### <span data-ttu-id="a4e05-133">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="a4e05-133">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="a4e05-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a4e05-134">NOTES</span></span>

## <span data-ttu-id="a4e05-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a4e05-135">RELATED LINKS</span></span>
