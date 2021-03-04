---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataset.md
ms.openlocfilehash: 7d586af76115ddf7cada5a443dd10d51463fe576
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981841"
---
# <span data-ttu-id="b4793-101">Get-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="b4793-101">Get-AzSynapseDataset</span></span>

## <span data-ttu-id="b4793-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4793-102">SYNOPSIS</span></span>
<span data-ttu-id="b4793-103">Pobiera informacje o zestawach danych w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="b4793-103">Gets information about datasets in workspace.</span></span>

## <span data-ttu-id="b4793-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b4793-104">SYNTAX</span></span>

### <span data-ttu-id="b4793-105">GetByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="b4793-105">GetByName (Default)</span></span>
```
Get-AzSynapseDataset -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b4793-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="b4793-106">GetByObject</span></span>
```
Get-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4793-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="b4793-107">DESCRIPTION</span></span>
<span data-ttu-id="b4793-108">Polecenie **cmdlet Get-AzSynapseDataset** pobiera informacje o zestawach danych w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="b4793-108">The **Get-AzSynapseDataset** cmdlet gets information about datasets in workspace.</span></span>
<span data-ttu-id="b4793-109">Jeśli określisz nazwę zestawu danych, to polecenie cmdlet pobiera informacje o tym zestawie danych.</span><span class="sxs-lookup"><span data-stu-id="b4793-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="b4793-110">Jeśli nie określisz nazwy, to polecenie cmdlet pobiera informacje o wszystkich zestawach danych w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="b4793-110">If you do not specify a name, this cmdlet gets information about all the datasets in the workspace.</span></span>

## <span data-ttu-id="b4793-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b4793-111">EXAMPLES</span></span>

### <span data-ttu-id="b4793-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b4793-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseDataset -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="b4793-113">To polecenie pobiera informacje o wszystkich zestawach danych w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="b4793-113">This command gets information about all datasets in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="b4793-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b4793-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset
```

<span data-ttu-id="b4793-115">To polecenie pobiera informacje o zestawie danych ContosoDataset w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="b4793-115">This command gets information about the dataset named ContosoDataset in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="b4793-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4793-116">PARAMETERS</span></span>

### <span data-ttu-id="b4793-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4793-117">-DefaultProfile</span></span>
<span data-ttu-id="b4793-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b4793-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4793-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b4793-119">-Name</span></span>
<span data-ttu-id="b4793-120">Nazwa zestawu danych.</span><span class="sxs-lookup"><span data-stu-id="b4793-120">The dataset name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatasetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4793-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b4793-121">-WorkspaceName</span></span>
<span data-ttu-id="b4793-122">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="b4793-122">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b4793-123">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b4793-123">-WorkspaceObject</span></span>
<span data-ttu-id="b4793-124">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="b4793-124">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b4793-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4793-125">CommonParameters</span></span>
<span data-ttu-id="b4793-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4793-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4793-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b4793-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4793-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4793-128">INPUTS</span></span>

### <span data-ttu-id="b4793-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b4793-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="b4793-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4793-130">OUTPUTS</span></span>

### <span data-ttu-id="b4793-131">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="b4793-131">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="b4793-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b4793-132">NOTES</span></span>

## <span data-ttu-id="b4793-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b4793-133">RELATED LINKS</span></span>
