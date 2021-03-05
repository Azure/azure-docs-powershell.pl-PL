---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseNotebook.md
ms.openlocfilehash: 9b960c3b671ecada8f4f24e1b5a8897de7004440
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007441"
---
# <span data-ttu-id="1944c-101">Set-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="1944c-101">Set-AzSynapseNotebook</span></span>

## <span data-ttu-id="1944c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1944c-102">SYNOPSIS</span></span>
<span data-ttu-id="1944c-103">Tworzy lub aktualizuje notes w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="1944c-103">Creates or updates a notebook in a workspace.</span></span>

## <span data-ttu-id="1944c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1944c-104">SYNTAX</span></span>

### <span data-ttu-id="1944c-105">SetByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="1944c-105">SetByName (Default)</span></span>
```
Set-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1944c-106">SetByNameAndSparkPool</span><span class="sxs-lookup"><span data-stu-id="1944c-106">SetByNameAndSparkPool</span></span>
```
Set-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -SparkPoolName <String> [-ExecutorSize <String>]
 -ExecutorCount <Int32> -DefinitionFile <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1944c-107">SetByObject</span><span class="sxs-lookup"><span data-stu-id="1944c-107">SetByObject</span></span>
```
Set-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1944c-108">SetByObjectAndSparkPool</span><span class="sxs-lookup"><span data-stu-id="1944c-108">SetByObjectAndSparkPool</span></span>
```
Set-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -SparkPoolName <String>
 [-ExecutorSize <String>] -ExecutorCount <Int32> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1944c-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="1944c-109">DESCRIPTION</span></span>
<span data-ttu-id="1944c-110">Polecenie **cmdlet Set-AzSynapseNotebook** tworzy lub aktualizuje notes w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="1944c-110">The **Set-AzSynapseNotebook** cmdlet creates or updates a notebook in a workspace.</span></span>

## <span data-ttu-id="1944c-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1944c-111">EXAMPLES</span></span>

### <span data-ttu-id="1944c-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1944c-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseNotebook -WorkspaceName ContosoWorkspace -DefinitionFile "C:\\samples\\notebook.ipynb"

    WorkspaceName : ContosoWorkspace
    Properties    : Microsoft.Azure.Commands.Synapse.Models.PSNotebook
    Name          : notebook
```

<span data-ttu-id="1944c-113">To polecenie tworzy lub aktualizuje notes z pliku notesu notebook.ipynb w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="1944c-113">This command creates or updates a notebook from notebook file notebook.ipynb in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="1944c-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="1944c-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseNotebook -DefinitionFile "C:\\samples\\notebook.ipynb"
```

<span data-ttu-id="1944c-115">To polecenie tworzy lub aktualizuje notes z pliku notesu notebook.ipynb w obszarze roboczym o nazwie ContosoWorkspace za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="1944c-115">This command creates or updates a notebook from notebook file notebook.ipynb in the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="1944c-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="1944c-116">Example 3</span></span>
```powershell
PS C:\> Set-AzSynapseNotebook -WorkspaceName ContosoWorkspace -DefinitionFile "C:\\samples\\notebook.ipynb" -SparkPoolName ContosoSparkPool -ExecutorCount 2
```

<span data-ttu-id="1944c-117">To polecenie tworzy lub aktualizuje notes z pliku notesu notebook notebook.ipynb, który jest dołączany do pliku ContosoSparkPool i używa 2 plików wykonywających w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="1944c-117">This command creates or updates a notebook from notebook file notebook.ipynb which attaches to ContosoSparkPool and uses 2 executors in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="1944c-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1944c-118">PARAMETERS</span></span>

### <span data-ttu-id="1944c-119">— AsJob</span><span class="sxs-lookup"><span data-stu-id="1944c-119">-AsJob</span></span>
<span data-ttu-id="1944c-120">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1944c-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1944c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1944c-121">-DefaultProfile</span></span>
<span data-ttu-id="1944c-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1944c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1944c-123">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="1944c-123">-DefinitionFile</span></span>
<span data-ttu-id="1944c-124">Ścieżka pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="1944c-124">The JSON file path.</span></span>

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

### <span data-ttu-id="1944c-125">-ExecutorCount</span><span class="sxs-lookup"><span data-stu-id="1944c-125">-ExecutorCount</span></span>
<span data-ttu-id="1944c-126">Liczba executorów, którzy mają zostać przydzieleni w określonej puli przebiegu w czasie dla zadania.</span><span class="sxs-lookup"><span data-stu-id="1944c-126">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="1944c-127">-ExecutorSize</span><span class="sxs-lookup"><span data-stu-id="1944c-127">-ExecutorSize</span></span>
<span data-ttu-id="1944c-128">Liczba rdzeni i pamięci, które mają być używane dla executorów przydzielonych do określonej puli przebiegu w czasie dla zadania.</span><span class="sxs-lookup"><span data-stu-id="1944c-128">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="1944c-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1944c-129">-Name</span></span>
<span data-ttu-id="1944c-130">Nazwa notesu.</span><span class="sxs-lookup"><span data-stu-id="1944c-130">The notebook name.</span></span>

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

### <span data-ttu-id="1944c-131">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="1944c-131">-SparkPoolName</span></span>
<span data-ttu-id="1944c-132">Nazwa puli przebiegu w czasie synpsy.</span><span class="sxs-lookup"><span data-stu-id="1944c-132">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="1944c-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1944c-133">-WorkspaceName</span></span>
<span data-ttu-id="1944c-134">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="1944c-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="1944c-135">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="1944c-135">-WorkspaceObject</span></span>
<span data-ttu-id="1944c-136">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="1944c-136">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="1944c-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1944c-137">-Confirm</span></span>
<span data-ttu-id="1944c-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1944c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1944c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1944c-139">-WhatIf</span></span>
<span data-ttu-id="1944c-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1944c-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1944c-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1944c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1944c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1944c-142">CommonParameters</span></span>
<span data-ttu-id="1944c-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1944c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1944c-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1944c-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1944c-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1944c-145">INPUTS</span></span>

### <span data-ttu-id="1944c-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1944c-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="1944c-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1944c-147">OUTPUTS</span></span>

### <span data-ttu-id="1944c-148">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="1944c-148">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="1944c-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1944c-149">NOTES</span></span>

## <span data-ttu-id="1944c-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1944c-150">RELATED LINKS</span></span>
