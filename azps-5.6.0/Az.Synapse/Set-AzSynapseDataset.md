---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataset.md
ms.openlocfilehash: 1001aa2f282ab59e6ddc9e3e1ecc654950d8e30e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952970"
---
# <span data-ttu-id="3df90-101">Set-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="3df90-101">Set-AzSynapseDataset</span></span>

## <span data-ttu-id="3df90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3df90-102">SYNOPSIS</span></span>
<span data-ttu-id="3df90-103">Tworzy lub aktualizuje zestaw danych w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="3df90-103">Creates or updates a dataset in workspace.</span></span>

## <span data-ttu-id="3df90-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3df90-104">SYNTAX</span></span>

### <span data-ttu-id="3df90-105">SetByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="3df90-105">SetByName (Default)</span></span>
```
Set-AzSynapseDataset -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3df90-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="3df90-106">SetByObject</span></span>
```
Set-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3df90-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="3df90-107">DESCRIPTION</span></span>
<span data-ttu-id="3df90-108">Polecenie **cmdlet Set-AzSynapseDataset** tworzy zestaw danych lub aktualizuje istniejący zestaw danych w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="3df90-108">The **Set-AzSynapseDataset** cmdlet creates a dataset or updates an existing dataset in workspace.</span></span>

## <span data-ttu-id="3df90-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3df90-109">EXAMPLES</span></span>

### <span data-ttu-id="3df90-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3df90-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset -DefinitionFile "C:\\samples\\Dataset.json"
```

<span data-ttu-id="3df90-111">To polecenie tworzy w obszarze roboczym zestaw danych ContosoDataset o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="3df90-111">This command creates a dataset named ContosoDataset in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="3df90-112">Polecenie bazuje na danych w pliku danych Dataset.jspliku.</span><span class="sxs-lookup"><span data-stu-id="3df90-112">The command bases the dataset on information in the Dataset.json file.</span></span>

## <span data-ttu-id="3df90-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3df90-113">PARAMETERS</span></span>

### <span data-ttu-id="3df90-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="3df90-114">-AsJob</span></span>
<span data-ttu-id="3df90-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="3df90-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3df90-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3df90-116">-DefaultProfile</span></span>
<span data-ttu-id="3df90-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3df90-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3df90-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="3df90-118">-DefinitionFile</span></span>
<span data-ttu-id="3df90-119">Ścieżka pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="3df90-119">The JSON file path.</span></span>

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

### <span data-ttu-id="3df90-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3df90-120">-Name</span></span>
<span data-ttu-id="3df90-121">Nazwa zestawu danych.</span><span class="sxs-lookup"><span data-stu-id="3df90-121">The dataset name.</span></span>

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

### <span data-ttu-id="3df90-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3df90-122">-WorkspaceName</span></span>
<span data-ttu-id="3df90-123">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="3df90-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="3df90-124">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3df90-124">-WorkspaceObject</span></span>
<span data-ttu-id="3df90-125">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="3df90-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="3df90-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3df90-126">-Confirm</span></span>
<span data-ttu-id="3df90-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3df90-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3df90-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3df90-128">-WhatIf</span></span>
<span data-ttu-id="3df90-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3df90-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3df90-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3df90-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3df90-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3df90-131">CommonParameters</span></span>
<span data-ttu-id="3df90-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3df90-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3df90-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3df90-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3df90-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3df90-134">INPUTS</span></span>

### <span data-ttu-id="3df90-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3df90-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="3df90-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3df90-136">OUTPUTS</span></span>

### <span data-ttu-id="3df90-137">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="3df90-137">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="3df90-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3df90-138">NOTES</span></span>

## <span data-ttu-id="3df90-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3df90-139">RELATED LINKS</span></span>
