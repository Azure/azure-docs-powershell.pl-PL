---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 38ED2854-23D0-400E-A5C8-239346B2AF99
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchnodefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFile.md
ms.openlocfilehash: db8ef62a158edaa3a697af9f77e7932dfa18c096
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239339"
---
# <span data-ttu-id="70015-101">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="70015-101">Get-AzBatchNodeFile</span></span>

## <span data-ttu-id="70015-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70015-102">SYNOPSIS</span></span>
<span data-ttu-id="70015-103">Pobiera właściwości plików węzła partii.</span><span class="sxs-lookup"><span data-stu-id="70015-103">Gets the properties of Batch node files.</span></span>

## <span data-ttu-id="70015-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="70015-104">SYNTAX</span></span>

### <span data-ttu-id="70015-105">ComputeNode_Id (domyślne)</span><span class="sxs-lookup"><span data-stu-id="70015-105">ComputeNode_Id (Default)</span></span>
```
Get-AzBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [[-Path] <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70015-106">Task_Id</span><span class="sxs-lookup"><span data-stu-id="70015-106">Task_Id</span></span>
```
Get-AzBatchNodeFile -JobId <String> -TaskId <String> [[-Path] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70015-107">Task_ODataFilter</span><span class="sxs-lookup"><span data-stu-id="70015-107">Task_ODataFilter</span></span>
```
Get-AzBatchNodeFile -JobId <String> -TaskId <String> [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70015-108">ParentTask</span><span class="sxs-lookup"><span data-stu-id="70015-108">ParentTask</span></span>
```
Get-AzBatchNodeFile [[-Task] <PSCloudTask>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70015-109">ComputeNode_ODataFilter</span><span class="sxs-lookup"><span data-stu-id="70015-109">ComputeNode_ODataFilter</span></span>
```
Get-AzBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Recursive] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="70015-110">ParentComputeNode</span><span class="sxs-lookup"><span data-stu-id="70015-110">ParentComputeNode</span></span>
```
Get-AzBatchNodeFile [[-ComputeNode] <PSComputeNode>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70015-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="70015-111">DESCRIPTION</span></span>
<span data-ttu-id="70015-112">Polecenie **cmdlet Get-AzBatchNodeFile** pobiera właściwości plików węzła usługi Azure Batch zadania lub węzła obliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="70015-112">The **Get-AzBatchNodeFile** cmdlet gets the properties of the Azure Batch node files of a task or compute node.</span></span>
<span data-ttu-id="70015-113">Aby zawęzić wyniki, możesz określić filtr protokołu Open Data (OData).</span><span class="sxs-lookup"><span data-stu-id="70015-113">To narrow your results, you can specify an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="70015-114">Jeśli określisz zadanie, ale nie filtr, to polecenie cmdlet zwróci właściwości wszystkich plików węzła dla tego zadania.</span><span class="sxs-lookup"><span data-stu-id="70015-114">If you specify a task, but not a filter, this cmdlet returns properties for all node files for that task.</span></span>
<span data-ttu-id="70015-115">Jeśli określisz węzeł obliczeniowy, ale nie filtr, to polecenie cmdlet zwróci właściwości wszystkich plików węzła dla tego węzła obliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="70015-115">If you specify a compute node, but not a filter, this cmdlet returns properties for all node files for that compute node.</span></span>

## <span data-ttu-id="70015-116">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="70015-116">EXAMPLES</span></span>

### <span data-ttu-id="70015-117">Przykład 1. Uzyskiwanie właściwości pliku węzła skojarzonego z zadaniem</span><span class="sxs-lookup"><span data-stu-id="70015-117">Example 1: Get the properties of a node file associated with a task</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "Stdout.txt" -BatchContext $Context
IsDirectory Name          Properties                                      Url

----------- ----          ----------                                      ---

False       StdOut.txt    Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="70015-118">To polecenie pobiera właściwości pliku węzła StdOut.txt skojarzonego z zadaniem, które ma identyfikator Zadanie26 w zadaniu, które ma identyfikator Zadanie-000001.</span><span class="sxs-lookup"><span data-stu-id="70015-118">This command gets the properties of the StdOut.txt node file associated with the task that has the ID Task26 in the job that has the ID Job-000001.</span></span>
<span data-ttu-id="70015-119">Użyj Get-AzBatchAccountKey cmdlet, aby przypisać kontekst do zmiennej $Context danych.</span><span class="sxs-lookup"><span data-stu-id="70015-119">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="70015-120">Przykład 2. Uzyskiwanie właściwości plików węzła skojarzonych z zadaniem przy użyciu filtru</span><span class="sxs-lookup"><span data-stu-id="70015-120">Example 2: Get the properties of node files associated with a task by using a filter</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job-00002" -TaskId "Task26" -Filter "startswith(name,'St')" -BatchContext $Context
IsDirectory Name        Properties                                      Url

----------- ----        ----------                                      ---

False       StdErr.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
False       StdOut.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="70015-121">To polecenie pobiera właściwości plików węzła, których nazwy zaczynają się od st i są skojarzone z zadaniem o identyfikatorze Zadanie26 w zadaniu o identyfikatorze Zadanie-00002.</span><span class="sxs-lookup"><span data-stu-id="70015-121">This command gets the properties of the node files whose names start with st and are associated with task that has the ID Task26 under job that has the ID Job-00002.</span></span>

### <span data-ttu-id="70015-122">Przykład 3. Cykliczne uzyskiwanie właściwości plików węzła skojarzonych z zadaniem</span><span class="sxs-lookup"><span data-stu-id="70015-122">Example 3: Recursively get the properties of node files associated with a task</span></span>
```
PS C:\>Get-AzBatchTask "Job-00003" "Task31" -BatchContext $Context | Get-AzBatchNodeFile -Recursive -BatchContext $Context
IsDirectory Name             Properties                                      Url

----------- ----             ----------                                      ---

False       ProcessEnv.cmd   Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
False       StdErr.txt       Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
False       StdOut.txt       Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
True        wd                                                               https://cmdletexample.westus.Batch.contoso...
False       wd\newFile.txt   Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="70015-123">To polecenie pobiera właściwości wszystkich plików skojarzonych z zadaniem o identyfikatorze Zadanie31 w zadaniu 00003.</span><span class="sxs-lookup"><span data-stu-id="70015-123">This command gets the properties of all files associated with the task that has the ID Task31 in job Job-00003.</span></span>
<span data-ttu-id="70015-124">To polecenie określa parametr *Rekurencyjny.*</span><span class="sxs-lookup"><span data-stu-id="70015-124">This command specifies the *Recursive* parameter.</span></span>
<span data-ttu-id="70015-125">Dlatego polecenie cmdlet wykonuje wyszukiwanie rekurentywne pliku i zwraca wd\newFile.txt pliku węzła.</span><span class="sxs-lookup"><span data-stu-id="70015-125">Therefore, the cmdlet performs a recursive file search is performed, and returns the wd\newFile.txt node file.</span></span>

### <span data-ttu-id="70015-126">Przykład 4. Uzyskiwanie pojedynczego pliku z węzła obliczeniowego</span><span class="sxs-lookup"><span data-stu-id="70015-126">Example 4: Get a single file from a compute node</span></span>
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool22" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context
IsDirectory Name                    Properties                                      Url
----------- ----                    ----------                                      ---
False       startup\stdout.txt      Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="70015-127">To polecenie pobiera plik o nazwie Startup\StdOut.txt z węzła obliczeniowego, który ma identyfikator ComputeNode01 w puli, która ma pulę identyfikatorów 22.</span><span class="sxs-lookup"><span data-stu-id="70015-127">This command gets the file that is named Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>

### <span data-ttu-id="70015-128">Przykład 5. Pobierz wszystkie pliki poniżej folderu z węzła obliczeniowego</span><span class="sxs-lookup"><span data-stu-id="70015-128">Example 5: Get all files under a folder from a compute node</span></span>
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool22" -ComputeNodeId "ComputeNode01" -Filter "startswith(name,'startup')" -Recursive -BatchContext $Context
IsDirectory Name                      Properties                                      Url
----------- ----                      ----------                                      ---
True        startup                                                                   https://cmdletexample.westus.Batch.contoso...
False       startup\ProcessEnv.cmd    Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
False       startup\stderr.txt        Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
False       startup\stdout.txt        Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
True        startup\wd                                                                https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="70015-129">To polecenie pobiera wszystkie pliki w folderze startowym z węzła obliczeniowego zawierającego identyfikator ComputeNode01 w puli zawierającej pulę identyfikatorów 22.</span><span class="sxs-lookup"><span data-stu-id="70015-129">This command gets all the files under the startup folder from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>
<span data-ttu-id="70015-130">To polecenie cmdlet określa parametr *rekurencyjny.*</span><span class="sxs-lookup"><span data-stu-id="70015-130">This cmdlet specifies the *Recursive* parameter.</span></span>

### <span data-ttu-id="70015-131">Przykład 6. Uzyskiwanie plików z folderu głównego węzła obliczeniowego</span><span class="sxs-lookup"><span data-stu-id="70015-131">Example 6: Get files from the root folder of a compute node</span></span>
```
PS C:\>Get-AzBatchComputeNode "Pool22" -Id "ComputeNode01" -BatchContext $Context | Get-AzBatchNodeFile -BatchContext $Context
IsDirectory Name           Properties       Url
----------- ----           ----------       ---
True        shared                          https://cmdletexample.westus.Batch.contoso...
True        startup                         https://cmdletexample.westus.Batch.contoso...
True        workitems                       https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="70015-132">To polecenie pobiera wszystkie pliki w folderze głównym węzła obliczeniowego, który ma identyfikator ComputeNode01 w puli zawierającej pulę identyfikatorów 22.</span><span class="sxs-lookup"><span data-stu-id="70015-132">This command gets all the files at the root folder of the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>

## <span data-ttu-id="70015-133">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70015-133">PARAMETERS</span></span>

### <span data-ttu-id="70015-134">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="70015-134">-BatchContext</span></span>
<span data-ttu-id="70015-135">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="70015-135">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="70015-136">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="70015-136">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="70015-137">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="70015-137">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="70015-138">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="70015-138">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="70015-139">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="70015-139">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70015-140">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="70015-140">-ComputeNode</span></span>
<span data-ttu-id="70015-141">Określa węzeł obliczeniowy, jako **obiekt PSComputeNode,** zawierający pliki węzła Batch.</span><span class="sxs-lookup"><span data-stu-id="70015-141">Specifies the compute node, as a **PSComputeNode** object, that contains the Batch node files.</span></span>
<span data-ttu-id="70015-142">Aby uzyskać obiekt węzła obliczeniowego, użyj Get-AzBatchComputeNode cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70015-142">To obtain a compute node object, use the Get-AzBatchComputeNode cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: ParentComputeNode
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70015-143">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="70015-143">-ComputeNodeId</span></span>
<span data-ttu-id="70015-144">Określa identyfikator węzła obliczeniowego zawierającego pliki węzła Partii.</span><span class="sxs-lookup"><span data-stu-id="70015-144">Specifies the ID of the compute node that contains the Batch node files.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id, ComputeNode_ODataFilter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70015-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70015-145">-DefaultProfile</span></span>
<span data-ttu-id="70015-146">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="70015-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70015-147">— Filtr</span><span class="sxs-lookup"><span data-stu-id="70015-147">-Filter</span></span>
<span data-ttu-id="70015-148">Określa klauzulę filtru OData.</span><span class="sxs-lookup"><span data-stu-id="70015-148">Specifies an OData filter clause.</span></span>
<span data-ttu-id="70015-149">To polecenie cmdlet zwraca właściwości plików węzła, które są zgodne z filtrem, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="70015-149">This cmdlet returns properties for node files that match the filter that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_ODataFilter, ParentTask, ComputeNode_ODataFilter, ParentComputeNode
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70015-150">- JobId</span><span class="sxs-lookup"><span data-stu-id="70015-150">-JobId</span></span>
<span data-ttu-id="70015-151">Określa identyfikator zadania zawierającego zadanie docelowe.</span><span class="sxs-lookup"><span data-stu-id="70015-151">Specifies the ID of the job that contains the target task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id, Task_ODataFilter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70015-152">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="70015-152">-MaxCount</span></span>
<span data-ttu-id="70015-153">Określa maksymalną liczbę plików węzła, dla których to polecenie cmdlet zwraca właściwości.</span><span class="sxs-lookup"><span data-stu-id="70015-153">Specifies the maximum number of node files for which this cmdlet returns properties.</span></span>
<span data-ttu-id="70015-154">Jeśli określisz wartość zero (0) lub mniejszą, polecenie cmdlet nie użyje górnego limitu.</span><span class="sxs-lookup"><span data-stu-id="70015-154">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="70015-155">Wartość domyślna to 1000.</span><span class="sxs-lookup"><span data-stu-id="70015-155">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Task_ODataFilter, ParentTask, ComputeNode_ODataFilter, ParentComputeNode
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70015-156">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="70015-156">-Path</span></span>
<span data-ttu-id="70015-157">Określa ścieżkę pliku węzła, dla którego to polecenie cmdlet pobiera właściwości.</span><span class="sxs-lookup"><span data-stu-id="70015-157">Specifies the path of the node file for which this cmdlet retrieves properties.</span></span>
<span data-ttu-id="70015-158">Nie można określić symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="70015-158">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id, Task_Id
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70015-159">- PoolId</span><span class="sxs-lookup"><span data-stu-id="70015-159">-PoolId</span></span>
<span data-ttu-id="70015-160">Określa identyfikator puli zawierającej węzeł obliczeniowy, z którego mają być właściwości plików węzła.</span><span class="sxs-lookup"><span data-stu-id="70015-160">Specifies the ID of the pool that contains the compute node from which to get properties of node files.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id, ComputeNode_ODataFilter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70015-161">- Rekurencyjna</span><span class="sxs-lookup"><span data-stu-id="70015-161">-Recursive</span></span>
<span data-ttu-id="70015-162">Wskazuje, że to polecenie cmdlet zwraca listę rekurencyjną plików.</span><span class="sxs-lookup"><span data-stu-id="70015-162">Indicates that this cmdlet returns a recursive list of files.</span></span>
<span data-ttu-id="70015-163">W przeciwnym razie zwraca tylko pliki z folderu głównego.</span><span class="sxs-lookup"><span data-stu-id="70015-163">Otherwise, it returns only the files in the root folder.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Task_ODataFilter, ParentTask, ComputeNode_ODataFilter, ParentComputeNode
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70015-164">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="70015-164">-Task</span></span>
<span data-ttu-id="70015-165">Określa zadanie jako obiekt **PSCloudTask,** z którym są skojarzone pliki węzła.</span><span class="sxs-lookup"><span data-stu-id="70015-165">Specifies the task, as a **PSCloudTask** object, with which the node files are associated.</span></span>
<span data-ttu-id="70015-166">Aby uzyskać obiekt zadania, użyj Get-AzBatchTask cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70015-166">To obtain a task object, use the Get-AzBatchTask cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: ParentTask
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70015-167">- TaskId</span><span class="sxs-lookup"><span data-stu-id="70015-167">-TaskId</span></span>
<span data-ttu-id="70015-168">Określa identyfikator zadania, dla którego to polecenie cmdlet pobiera właściwości plików węzła.</span><span class="sxs-lookup"><span data-stu-id="70015-168">Specifies the ID of the task for which this cmdlet gets properties of node files.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id, Task_ODataFilter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70015-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70015-169">CommonParameters</span></span>
<span data-ttu-id="70015-170">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70015-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70015-171">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="70015-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70015-172">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="70015-172">INPUTS</span></span>

### <span data-ttu-id="70015-173">System.String</span><span class="sxs-lookup"><span data-stu-id="70015-173">System.String</span></span>

### <span data-ttu-id="70015-174">Microsoft.Azure.Commands.Batch. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="70015-174">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="70015-175">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="70015-175">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="70015-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="70015-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="70015-177">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="70015-177">OUTPUTS</span></span>

### <span data-ttu-id="70015-178">Microsoft.Azure.Commands.Batch. Models.PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="70015-178">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>

## <span data-ttu-id="70015-179">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="70015-179">NOTES</span></span>

## <span data-ttu-id="70015-180">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="70015-180">RELATED LINKS</span></span>

[<span data-ttu-id="70015-181">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="70015-181">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="70015-182">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="70015-182">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="70015-183">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="70015-183">Get-AzBatchNodeFileContent</span></span>](./Get-AzBatchNodeFileContent.md)

[<span data-ttu-id="70015-184">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="70015-184">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="70015-185">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="70015-185">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
