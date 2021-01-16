---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataset.md
ms.openlocfilehash: d2471320a27b1af96dba6b5e2b552a01ff5b50e3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383229"
---
# <span data-ttu-id="1c183-101">Set-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="1c183-101">Set-AzSynapseDataset</span></span>

## <span data-ttu-id="1c183-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1c183-102">SYNOPSIS</span></span>
<span data-ttu-id="1c183-103">Tworzenie lub aktualizowanie zestawu danych w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="1c183-103">Creates or updates a dataset in workspace.</span></span>

## <span data-ttu-id="1c183-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1c183-104">SYNTAX</span></span>

### <span data-ttu-id="1c183-105">SetByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1c183-105">SetByName (Default)</span></span>
```
Set-AzSynapseDataset -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c183-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="1c183-106">SetByObject</span></span>
```
Set-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c183-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1c183-107">DESCRIPTION</span></span>
<span data-ttu-id="1c183-108">Polecenie cmdlet **Set-AzSynapseDataset** umożliwia utworzenie zestawu danych lub zaktualizowanie istniejącego zestawu danych w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="1c183-108">The **Set-AzSynapseDataset** cmdlet creates a dataset or updates an existing dataset in workspace.</span></span>

## <span data-ttu-id="1c183-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1c183-109">EXAMPLES</span></span>

### <span data-ttu-id="1c183-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1c183-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset -DefinitionFile "C:\\samples\\Dataset.json"
```

<span data-ttu-id="1c183-111">To polecenie tworzy zestaw danych o nazwie ContosoDataset w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="1c183-111">This command creates a dataset named ContosoDataset in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="1c183-112">Polecenie opiera się na zestawie danych na temat informacji zawartych w Dataset.jspliku.</span><span class="sxs-lookup"><span data-stu-id="1c183-112">The command bases the dataset on information in the Dataset.json file.</span></span>

## <span data-ttu-id="1c183-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1c183-113">PARAMETERS</span></span>

### <span data-ttu-id="1c183-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1c183-114">-AsJob</span></span>
<span data-ttu-id="1c183-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1c183-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1c183-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c183-116">-DefaultProfile</span></span>
<span data-ttu-id="1c183-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1c183-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c183-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="1c183-118">-DefinitionFile</span></span>
<span data-ttu-id="1c183-119">Ścieżka pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="1c183-119">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c183-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1c183-120">-Name</span></span>
<span data-ttu-id="1c183-121">Nazwa zestawu danych.</span><span class="sxs-lookup"><span data-stu-id="1c183-121">The dataset name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatasetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c183-122">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="1c183-122">-WorkspaceName</span></span>
<span data-ttu-id="1c183-123">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="1c183-123">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c183-124">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="1c183-124">-WorkspaceObject</span></span>
<span data-ttu-id="1c183-125">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="1c183-125">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c183-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1c183-126">-Confirm</span></span>
<span data-ttu-id="1c183-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c183-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c183-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c183-128">-WhatIf</span></span>
<span data-ttu-id="1c183-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c183-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c183-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1c183-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c183-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c183-131">CommonParameters</span></span>
<span data-ttu-id="1c183-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c183-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c183-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c183-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c183-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1c183-134">INPUTS</span></span>

### <span data-ttu-id="1c183-135">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1c183-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="1c183-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1c183-136">OUTPUTS</span></span>

### <span data-ttu-id="1c183-137">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="1c183-137">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="1c183-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1c183-138">NOTES</span></span>

## <span data-ttu-id="1c183-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1c183-139">RELATED LINKS</span></span>
