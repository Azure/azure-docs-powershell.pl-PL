---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataset.md
ms.openlocfilehash: 8919c554fb32a102991b9c40236e897662709ccb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225466"
---
# <span data-ttu-id="14605-101">Get-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="14605-101">Get-AzSynapseDataset</span></span>

## <span data-ttu-id="14605-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="14605-102">SYNOPSIS</span></span>
<span data-ttu-id="14605-103">Pobiera informacje o zestawach danych w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="14605-103">Gets information about datasets in workspace.</span></span>

## <span data-ttu-id="14605-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="14605-104">SYNTAX</span></span>

### <span data-ttu-id="14605-105">GetByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="14605-105">GetByName (Default)</span></span>
```
Get-AzSynapseDataset -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="14605-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="14605-106">GetByObject</span></span>
```
Get-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14605-107">Opis</span><span class="sxs-lookup"><span data-stu-id="14605-107">DESCRIPTION</span></span>
<span data-ttu-id="14605-108">Polecenie cmdlet **Get-AzSynapseDataset** pobiera informacje o zestawach danych w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="14605-108">The **Get-AzSynapseDataset** cmdlet gets information about datasets in workspace.</span></span>
<span data-ttu-id="14605-109">Jeśli określisz nazwę zestawu danych, to polecenie cmdlet będzie pobierać informacje o tym zestawie danych.</span><span class="sxs-lookup"><span data-stu-id="14605-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="14605-110">Jeśli nie określisz nazwy, to polecenie cmdlet będzie pobierać informacje dotyczące wszystkich zestawów danych w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="14605-110">If you do not specify a name, this cmdlet gets information about all the datasets in the workspace.</span></span>

## <span data-ttu-id="14605-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="14605-111">EXAMPLES</span></span>

### <span data-ttu-id="14605-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="14605-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseDataset -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="14605-113">To polecenie pobiera informacje dotyczące wszystkich zestawów danych w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="14605-113">This command gets information about all datasets in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="14605-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="14605-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset
```

<span data-ttu-id="14605-115">To polecenie pobiera informacje o zestawie danych o nazwie ContosoDataset w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="14605-115">This command gets information about the dataset named ContosoDataset in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="14605-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="14605-116">PARAMETERS</span></span>

### <span data-ttu-id="14605-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14605-117">-DefaultProfile</span></span>
<span data-ttu-id="14605-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="14605-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14605-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="14605-119">-Name</span></span>
<span data-ttu-id="14605-120">Nazwa zestawu danych.</span><span class="sxs-lookup"><span data-stu-id="14605-120">The dataset name.</span></span>

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

### <span data-ttu-id="14605-121">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="14605-121">-WorkspaceName</span></span>
<span data-ttu-id="14605-122">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="14605-122">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="14605-123">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="14605-123">-WorkspaceObject</span></span>
<span data-ttu-id="14605-124">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="14605-124">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="14605-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14605-125">CommonParameters</span></span>
<span data-ttu-id="14605-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14605-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14605-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14605-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14605-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14605-128">INPUTS</span></span>

### <span data-ttu-id="14605-129">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="14605-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="14605-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="14605-130">OUTPUTS</span></span>

### <span data-ttu-id="14605-131">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="14605-131">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="14605-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="14605-132">NOTES</span></span>

## <span data-ttu-id="14605-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="14605-133">RELATED LINKS</span></span>
