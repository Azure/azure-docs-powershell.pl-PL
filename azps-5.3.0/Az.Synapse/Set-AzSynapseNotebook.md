---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseNotebook.md
ms.openlocfilehash: da4907200bef198afa1d57b51069c6379d28c8f1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501298"
---
# <span data-ttu-id="6d263-101">Set-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="6d263-101">Set-AzSynapseNotebook</span></span>

## <span data-ttu-id="6d263-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6d263-102">SYNOPSIS</span></span>
<span data-ttu-id="6d263-103">Umożliwia utworzenie lub zaktualizowanie notesu w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="6d263-103">Creates or updates a notebook in a workspace.</span></span>

## <span data-ttu-id="6d263-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6d263-104">SYNTAX</span></span>

### <span data-ttu-id="6d263-105">SetByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6d263-105">SetByName (Default)</span></span>
```
Set-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d263-106">SetByNameAndSparkPool</span><span class="sxs-lookup"><span data-stu-id="6d263-106">SetByNameAndSparkPool</span></span>
```
Set-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -SparkPoolName <String> [-ExecutorSize <String>]
 -ExecutorCount <Int32> -DefinitionFile <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d263-107">SetByObject</span><span class="sxs-lookup"><span data-stu-id="6d263-107">SetByObject</span></span>
```
Set-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d263-108">SetByObjectAndSparkPool</span><span class="sxs-lookup"><span data-stu-id="6d263-108">SetByObjectAndSparkPool</span></span>
```
Set-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -SparkPoolName <String>
 [-ExecutorSize <String>] -ExecutorCount <Int32> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d263-109">Opis</span><span class="sxs-lookup"><span data-stu-id="6d263-109">DESCRIPTION</span></span>
<span data-ttu-id="6d263-110">Polecenie cmdlet **Set-AzSynapseNotebook** umożliwia utworzenie lub zaktualizowanie notesu w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="6d263-110">The **Set-AzSynapseNotebook** cmdlet creates or updates a notebook in a workspace.</span></span>

## <span data-ttu-id="6d263-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6d263-111">EXAMPLES</span></span>

### <span data-ttu-id="6d263-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6d263-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseNotebook -WorkspaceName ContosoWorkspace -DefinitionFile "C:\\samples\\notebook.ipynb"

    WorkspaceName : ContosoWorkspace
    Properties    : Microsoft.Azure.Commands.Synapse.Models.PSNotebook
    Name          : notebook
```

<span data-ttu-id="6d263-113">To polecenie umożliwia utworzenie lub zaktualizowanie notesu z notesu pliku notesu. ipynb w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="6d263-113">This command creates or updates a notebook from notebook file notebook.ipynb in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="6d263-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6d263-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseNotebook -DefinitionFile "C:\\samples\\notebook.ipynb"
```

<span data-ttu-id="6d263-115">To polecenie umożliwia utworzenie lub zaktualizowanie notesu z notesu pliku notesu. ipynb w obszarze roboczym o nazwie ContosoWorkspace za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="6d263-115">This command creates or updates a notebook from notebook file notebook.ipynb in the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="6d263-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="6d263-116">Example 3</span></span>
```powershell
PS C:\> Set-AzSynapseNotebook -WorkspaceName ContosoWorkspace -DefinitionFile "C:\\samples\\notebook.ipynb" -SparkPoolName ContosoSparkPool -ExecutorCount 2
```

<span data-ttu-id="6d263-117">To polecenie umożliwia utworzenie lub zaktualizowanie notesu z notesu pliku notesu. ipynb, który dołącza do ContosoSparkPool i używa 2 modułów wykonujących w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="6d263-117">This command creates or updates a notebook from notebook file notebook.ipynb which attaches to ContosoSparkPool and uses 2 executors in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="6d263-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6d263-118">PARAMETERS</span></span>

### <span data-ttu-id="6d263-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d263-119">-AsJob</span></span>
<span data-ttu-id="6d263-120">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6d263-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6d263-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d263-121">-DefaultProfile</span></span>
<span data-ttu-id="6d263-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6d263-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d263-123">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="6d263-123">-DefinitionFile</span></span>
<span data-ttu-id="6d263-124">Ścieżka pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="6d263-124">The JSON file path.</span></span>

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

### <span data-ttu-id="6d263-125">-ExecutorCount</span><span class="sxs-lookup"><span data-stu-id="6d263-125">-ExecutorCount</span></span>
<span data-ttu-id="6d263-126">Liczba wykonawców, które mają zostać przydzielone w określonej puli platformy Spark dla zadania.</span><span class="sxs-lookup"><span data-stu-id="6d263-126">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByNameAndSparkPool, SetByObjectAndSparkPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d263-127">-ExecutorSize</span><span class="sxs-lookup"><span data-stu-id="6d263-127">-ExecutorSize</span></span>
<span data-ttu-id="6d263-128">Liczba podstawowych i pamięci, które mają być używane w przypadku modułów wykonujących zadania, przydzielonych w określonej puli platformy Spark.</span><span class="sxs-lookup"><span data-stu-id="6d263-128">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndSparkPool, SetByObjectAndSparkPool
Aliases:
Accepted values: Small, Medium, Large

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d263-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6d263-129">-Name</span></span>
<span data-ttu-id="6d263-130">Nazwa notesu.</span><span class="sxs-lookup"><span data-stu-id="6d263-130">The notebook name.</span></span>

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

### <span data-ttu-id="6d263-131">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="6d263-131">-SparkPoolName</span></span>
<span data-ttu-id="6d263-132">Nazwa puli Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="6d263-132">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndSparkPool, SetByObjectAndSparkPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d263-133">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="6d263-133">-WorkspaceName</span></span>
<span data-ttu-id="6d263-134">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="6d263-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByNameAndSparkPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d263-135">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="6d263-135">-WorkspaceObject</span></span>
<span data-ttu-id="6d263-136">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="6d263-136">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject, SetByObjectAndSparkPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d263-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6d263-137">-Confirm</span></span>
<span data-ttu-id="6d263-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d263-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d263-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d263-139">-WhatIf</span></span>
<span data-ttu-id="6d263-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d263-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d263-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6d263-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d263-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d263-142">CommonParameters</span></span>
<span data-ttu-id="6d263-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d263-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d263-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d263-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d263-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6d263-145">INPUTS</span></span>

### <span data-ttu-id="6d263-146">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6d263-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="6d263-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6d263-147">OUTPUTS</span></span>

### <span data-ttu-id="6d263-148">Microsoft. Azure. Commands. Synapse. models. PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="6d263-148">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="6d263-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6d263-149">NOTES</span></span>

## <span data-ttu-id="6d263-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6d263-150">RELATED LINKS</span></span>
