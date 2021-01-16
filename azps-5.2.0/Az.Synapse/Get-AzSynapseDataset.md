---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataset.md
ms.openlocfilehash: 8919c554fb32a102991b9c40236e897662709ccb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339277"
---
# <span data-ttu-id="f2be5-101">Get-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="f2be5-101">Get-AzSynapseDataset</span></span>

## <span data-ttu-id="f2be5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f2be5-102">SYNOPSIS</span></span>
<span data-ttu-id="f2be5-103">Pobiera informacje o zestawach danych w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="f2be5-103">Gets information about datasets in workspace.</span></span>

## <span data-ttu-id="f2be5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f2be5-104">SYNTAX</span></span>

### <span data-ttu-id="f2be5-105">GetByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f2be5-105">GetByName (Default)</span></span>
```
Get-AzSynapseDataset -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2be5-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="f2be5-106">GetByObject</span></span>
```
Get-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2be5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f2be5-107">DESCRIPTION</span></span>
<span data-ttu-id="f2be5-108">Polecenie cmdlet **Get-AzSynapseDataset** pobiera informacje o zestawach danych w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="f2be5-108">The **Get-AzSynapseDataset** cmdlet gets information about datasets in workspace.</span></span>
<span data-ttu-id="f2be5-109">Jeśli określisz nazwę zestawu danych, to polecenie cmdlet będzie pobierać informacje o tym zestawie danych.</span><span class="sxs-lookup"><span data-stu-id="f2be5-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="f2be5-110">Jeśli nie określisz nazwy, to polecenie cmdlet będzie pobierać informacje dotyczące wszystkich zestawów danych w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="f2be5-110">If you do not specify a name, this cmdlet gets information about all the datasets in the workspace.</span></span>

## <span data-ttu-id="f2be5-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f2be5-111">EXAMPLES</span></span>

### <span data-ttu-id="f2be5-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f2be5-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseDataset -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="f2be5-113">To polecenie pobiera informacje dotyczące wszystkich zestawów danych w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="f2be5-113">This command gets information about all datasets in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="f2be5-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f2be5-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset
```

<span data-ttu-id="f2be5-115">To polecenie pobiera informacje o zestawie danych o nazwie ContosoDataset w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="f2be5-115">This command gets information about the dataset named ContosoDataset in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="f2be5-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f2be5-116">PARAMETERS</span></span>

### <span data-ttu-id="f2be5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2be5-117">-DefaultProfile</span></span>
<span data-ttu-id="f2be5-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f2be5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2be5-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f2be5-119">-Name</span></span>
<span data-ttu-id="f2be5-120">Nazwa zestawu danych.</span><span class="sxs-lookup"><span data-stu-id="f2be5-120">The dataset name.</span></span>

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

### <span data-ttu-id="f2be5-121">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="f2be5-121">-WorkspaceName</span></span>
<span data-ttu-id="f2be5-122">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="f2be5-122">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f2be5-123">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="f2be5-123">-WorkspaceObject</span></span>
<span data-ttu-id="f2be5-124">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="f2be5-124">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f2be5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2be5-125">CommonParameters</span></span>
<span data-ttu-id="f2be5-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2be5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2be5-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f2be5-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2be5-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2be5-128">INPUTS</span></span>

### <span data-ttu-id="f2be5-129">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f2be5-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="f2be5-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f2be5-130">OUTPUTS</span></span>

### <span data-ttu-id="f2be5-131">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="f2be5-131">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="f2be5-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f2be5-132">NOTES</span></span>

## <span data-ttu-id="f2be5-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f2be5-133">RELATED LINKS</span></span>
