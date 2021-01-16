---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseNotebook.md
ms.openlocfilehash: 28a4742b2e744fb41bca9402a8c48b830554e231
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491093"
---
# <span data-ttu-id="c975d-101">Get-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="c975d-101">Get-AzSynapseNotebook</span></span>

## <span data-ttu-id="c975d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c975d-102">SYNOPSIS</span></span>
<span data-ttu-id="c975d-103">Pobiera informacje o notesach w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="c975d-103">Gets information about notebooks in a workspace.</span></span>

## <span data-ttu-id="c975d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c975d-104">SYNTAX</span></span>

### <span data-ttu-id="c975d-105">GetByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c975d-105">GetByName (Default)</span></span>
```
Get-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c975d-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="c975d-106">GetByObject</span></span>
```
Get-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c975d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c975d-107">DESCRIPTION</span></span>
<span data-ttu-id="c975d-108">Polecenie cmdlet **Get-AzSynapseNotebook** pobiera informacje o notesach w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="c975d-108">The **Get-AzSynapseNotebook** cmdlet gets information about notebooks in a workspace.</span></span> <span data-ttu-id="c975d-109">Jeśli określisz nazwę notesu, polecenie cmdlet pobiera informacje o tym notesie.</span><span class="sxs-lookup"><span data-stu-id="c975d-109">If you specify the name of a notebook, the cmdlet gets information about that notebook.</span></span> <span data-ttu-id="c975d-110">Jeśli nie określisz nazwy, polecenie cmdlet pobiera informacje o wszystkich notesach w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="c975d-110">If you do not specify a name, the cmdlet gets information about all notebooks in the workspace.</span></span>

## <span data-ttu-id="c975d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c975d-111">EXAMPLES</span></span>

### <span data-ttu-id="c975d-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c975d-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace | Format-Table

WorkspaceName    Properties                                         Name
-------------    ----------                                         --
ContosoWorkspace Microsoft.Azure.Commands.Synapse.Models.PSNotebook ContosoNotebook1
ContosoWorkspace Microsoft.Azure.Commands.Synapse.Models.PSNotebook ContosoNotebook2
```

<span data-ttu-id="c975d-113">Pobiera listę wszystkich notesów w obszarze roboczym ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="c975d-113">Gets a list of all notebooks in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="c975d-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c975d-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
```

<span data-ttu-id="c975d-115">Pobiera jeden Notes o nazwie ContosoNotebook w obszarze roboczym ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="c975d-115">Gets a single notebook called ContosoNotebook in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="c975d-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="c975d-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseNotebook -Name ContosoNotebook
```

<span data-ttu-id="c975d-117">Pobiera jeden Notes o nazwie ContosoNotebook w obszarze roboczym ContosoWorkspace za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="c975d-117">Gets a single notebook called ContosoNotebook in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="c975d-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c975d-118">PARAMETERS</span></span>

### <span data-ttu-id="c975d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c975d-119">-DefaultProfile</span></span>
<span data-ttu-id="c975d-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c975d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c975d-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c975d-121">-Name</span></span>
<span data-ttu-id="c975d-122">Nazwa notesu.</span><span class="sxs-lookup"><span data-stu-id="c975d-122">The notebook name.</span></span>

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

### <span data-ttu-id="c975d-123">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="c975d-123">-WorkspaceName</span></span>
<span data-ttu-id="c975d-124">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="c975d-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="c975d-125">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="c975d-125">-WorkspaceObject</span></span>
<span data-ttu-id="c975d-126">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="c975d-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="c975d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c975d-127">CommonParameters</span></span>
<span data-ttu-id="c975d-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c975d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c975d-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c975d-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c975d-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c975d-130">INPUTS</span></span>

### <span data-ttu-id="c975d-131">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c975d-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="c975d-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c975d-132">OUTPUTS</span></span>

### <span data-ttu-id="c975d-133">Microsoft. Azure. Commands. Synapse. models. PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="c975d-133">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="c975d-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c975d-134">NOTES</span></span>

## <span data-ttu-id="c975d-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c975d-135">RELATED LINKS</span></span>
