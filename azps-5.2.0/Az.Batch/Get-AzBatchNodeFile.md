---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 38ED2854-23D0-400E-A5C8-239346B2AF99
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchnodefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFile.md
ms.openlocfilehash: db8ef62a158edaa3a697af9f77e7932dfa18c096
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340738"
---
# <span data-ttu-id="3a1c3-101">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="3a1c3-101">Get-AzBatchNodeFile</span></span>

## <span data-ttu-id="3a1c3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3a1c3-102">SYNOPSIS</span></span>
<span data-ttu-id="3a1c3-103">Pobiera właściwości plików węzła wsadowego.</span><span class="sxs-lookup"><span data-stu-id="3a1c3-103">Gets the properties of Batch node files.</span></span>

## <span data-ttu-id="3a1c3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3a1c3-104">SYNTAX</span></span>

### <span data-ttu-id="3a1c3-105">ComputeNode_Id (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="3a1c3-105">ComputeNode_Id (Default)</span></span>
```
Get-AzBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [[-Path] <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a1c3-106">Task_Id</span><span class="sxs-lookup"><span data-stu-id="3a1c3-106">Task_Id</span></span>
```
Get-AzBatchNodeFile -JobId <String> -TaskId <String> [[-Path] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a1c3-107">Task_ODataFilter</span><span class="sxs-lookup"><span data-stu-id="3a1c3-107">Task_ODataFilter</span></span>
```
Get-AzBatchNodeFile -JobId <String> -TaskId <String> [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a1c3-108">ParentTask</span><span class="sxs-lookup"><span data-stu-id="3a1c3-108">ParentTask</span></span>
```
Get-AzBatchNodeFile [[-Task] <PSCloudTask>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a1c3-109">ComputeNode_ODataFilter</span><span class="sxs-lookup"><span data-stu-id="3a1c3-109">ComputeNode_ODataFilter</span></span>
```
Get-AzBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Recursive] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3a1c3-110">ParentComputeNode</span><span class="sxs-lookup"><span data-stu-id="3a1c3-110">ParentComputeNode</span></span>
```
Get-AzBatchNodeFile [[-ComputeNode] <PSComputeNode>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a1c3-111">Opis</span><span class="sxs-lookup"><span data-stu-id="3a1c3-111">DESCRIPTION</span></span>
<span data-ttu-id="3a1c3-112">Polecenie cmdlet **Get-AzBatchNodeFile** pobiera właściwości plików węzłów usługi Azure Batch dotyczących zadania lub węzła obliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="3a1c3-112">The **Get-AzBatchNodeFile** cmdlet gets the properties of the Azure Batch node files of a task or compute node.</span></span>
<span data-ttu-id="3a1c3-113">Aby zawęzić wyniki, możesz określić filtr protokołu OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="3a1c3-113">To narrow your results, you can specify an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="3a1c3-114">Jeśli określisz zadanie, ale nie filtr, to polecenie cmdlet zwróci właściwości dla wszystkich plików węzłów dla tego zadania.</span><span class="sxs-lookup"><span data-stu-id="3a1c3-114">If you specify a task, but not a filter, this cmdlet returns properties for all node files for that task.</span></span>
<span data-ttu-id="3a1c3-115">Jeśli określisz węzeł obliczeniowy, ale nie filtr, to polecenie cmdlet zwróci właściwości wszystkich plików węzłów dla tego węzła obliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="3a1c3-115">If you specify a compute node, but not a filter, this cmdlet returns properties for all node files for that compute node.</span></span>

## <span data-ttu-id="3a1c3-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3a1c3-116">EXAMPLES</span></span>

### <span data-ttu-id="3a1c3-117">Przykład 1: uzyskiwanie właściwości pliku węzła skojarzonego z zadaniem</span><span class="sxs-lookup"><span data-stu-id="3a1c3-117">Example 1: Get the properties of a node file associated with a task</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "Stdout.txt" -BatchContext $Context
IsDirectory Name          Properties                                      Url

----------- ----          ----------                                      ---

False       StdOut.txt    Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="3a1c3-118">To polecenie pobiera właściwości pliku węzła StdOut.txt skojarzonego z zadaniem o IDENTYFIKATORze Task26 w zadaniu, które ma identyfikator zadania ID-000001.</span><span class="sxs-lookup"><span data-stu-id="3a1c3-118">This command gets the properties of the StdOut.txt node file associated with the task that has the ID Task26 in the job that has the ID Job-000001.</span></span>
<span data-ttu-id="3a1c3-119">Użyj polecenia cmdlet Get-AzBatchAccountKey, aby przypisać kontekst do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="3a1c3-119">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="3a1c3-120">Przykład 2: uzyskiwanie właściwości plików węzłów skojarzonych z zadaniem za pomocą filtru</span><span class="sxs-lookup"><span data-stu-id="3a1c3-120">Example 2: Get the properties of node files associated with a task by using a filter</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job-00002" -TaskId "Task26" -Filter "startswith(name,'St')" -BatchContext $Context
IsDirectory Name        Properties                                      Url

----------- ----        ----------                                      ---

False       StdErr.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
False       StdOut.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="3a1c3-121">To polecenie pobiera właściwości plików węzłów, których nazwy zaczynają się od St i są skojarzone z zadaniem zawierającym identyfikator Task26 w obszarze zadanie o identyfikatorze ID-00002.</span><span class="sxs-lookup"><span data-stu-id="3a1c3-121">This command gets the properties of the node files whose names start with st and are associated with task that has the ID Task26 under job that has the ID Job-00002.</span></span>

### <span data-ttu-id="3a1c3-122">Przykład 3: rekursywnie uzyskiwanie właściwości plików węzłów skojarzonych z zadaniem</span><span class="sxs-lookup"><span data-stu-id="3a1c3-122">Example 3: Recursively get the properties of node files associated with a task</span></span>
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

<span data-ttu-id="3a1c3-123">To polecenie pobiera właściwości wszystkich plików skojarzonych z zadaniem, które ma identyfikator Task31 w zadaniu zadania-00003.</span><span class="sxs-lookup"><span data-stu-id="3a1c3-123">This command gets the properties of all files associated with the task that has the ID Task31 in job Job-00003.</span></span>
<span data-ttu-id="3a1c3-124">To polecenie określa parametr *cykliczny* .</span><span class="sxs-lookup"><span data-stu-id="3a1c3-124">This command specifies the *Recursive* parameter.</span></span>
<span data-ttu-id="3a1c3-125">Polecenie cmdlet wykonuje więc cykliczne wyszukiwanie plików, a następnie zwraca wd\newFile.txt plik węzła.</span><span class="sxs-lookup"><span data-stu-id="3a1c3-125">Therefore, the cmdlet performs a recursive file search is performed, and returns the wd\newFile.txt node file.</span></span>

### <span data-ttu-id="3a1c3-126">Przykład 4: uzyskiwanie jednego pliku z węzła obliczeniowego</span><span class="sxs-lookup"><span data-stu-id="3a1c3-126">Example 4: Get a single file from a compute node</span></span>
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool22" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context
IsDirectory Name                    Properties                                      Url
----------- ----                    ----------                                      ---
False       startup\stdout.txt      Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="3a1c3-127">To polecenie pobiera plik o nazwie Startup\StdOut.txt z węzła obliczeniowego o IDENTYFIKATORze ComputeNode01 w puli o IDENTYFIKATORze Pool22.</span><span class="sxs-lookup"><span data-stu-id="3a1c3-127">This command gets the file that is named Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>

### <span data-ttu-id="3a1c3-128">Przykład 5: pobieranie wszystkich plików w folderze z węzła obliczeniowego</span><span class="sxs-lookup"><span data-stu-id="3a1c3-128">Example 5: Get all files under a folder from a compute node</span></span>
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

<span data-ttu-id="3a1c3-129">To polecenie pobiera wszystkie pliki w folderze Autostart z węzła obliczeniowego o IDENTYFIKATORze ComputeNode01 w puli o IDENTYFIKATORze Pool22.</span><span class="sxs-lookup"><span data-stu-id="3a1c3-129">This command gets all the files under the startup folder from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>
<span data-ttu-id="3a1c3-130">To polecenie cmdlet określa parametr *cykliczny* .</span><span class="sxs-lookup"><span data-stu-id="3a1c3-130">This cmdlet specifies the *Recursive* parameter.</span></span>

### <span data-ttu-id="3a1c3-131">Przykład 6: pobieranie plików z folderu głównego węzła obliczeniowego</span><span class="sxs-lookup"><span data-stu-id="3a1c3-131">Example 6: Get files from the root folder of a compute node</span></span>
```
PS C:\>Get-AzBatchComputeNode "Pool22" -Id "ComputeNode01" -BatchContext $Context | Get-AzBatchNodeFile -BatchContext $Context
IsDirectory Name           Properties       Url
----------- ----           ----------       ---
True        shared                          https://cmdletexample.westus.Batch.contoso...
True        startup                         https://cmdletexample.westus.Batch.contoso...
True        workitems                       https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="3a1c3-132">To polecenie pobiera wszystkie pliki w folderze głównym węzła obliczeniowego o IDENTYFIKATORze ComputeNode01 w puli o IDENTYFIKATORze Pool22.</span><span class="sxs-lookup"><span data-stu-id="3a1c3-132">This command gets all the files at the root folder of the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>

## <span data-ttu-id="3a1c3-133">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3a1c3-133">PARAMETERS</span></span>

### <span data-ttu-id="3a1c3-134">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="3a1c3-134">-BatchContext</span></span>
<span data-ttu-id="3a1c3-135">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="3a1c3-135">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="3a1c3-136">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="3a1c3-136">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="3a1c3-137">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKey, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="3a1c3-137">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="3a1c3-138">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="3a1c3-138">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="3a1c3-139">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="3a1c3-139">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="3a1c3-140">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="3a1c3-140">-ComputeNode</span></span>
<span data-ttu-id="3a1c3-141">Określa węzeł obliczeniowe jako obiekt **PSComputeNode** , który zawiera pliki węzła partii.</span><span class="sxs-lookup"><span data-stu-id="3a1c3-141">Specifies the compute node, as a **PSComputeNode** object, that contains the Batch node files.</span></span>
<span data-ttu-id="3a1c3-142">Aby uzyskać obiekt węzła obliczeniowego, użyj polecenia cmdlet Get-AzBatchComputeNode.</span><span class="sxs-lookup"><span data-stu-id="3a1c3-142">To obtain a compute node object, use the Get-AzBatchComputeNode cmdlet.</span></span>

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

### <span data-ttu-id="3a1c3-143">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="3a1c3-143">-ComputeNodeId</span></span>
<span data-ttu-id="3a1c3-144">Określa identyfikator węzła obliczeniowego zawierającego pliki węzła partii.</span><span class="sxs-lookup"><span data-stu-id="3a1c3-144">Specifies the ID of the compute node that contains the Batch node files.</span></span>

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

### <span data-ttu-id="3a1c3-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a1c3-145">-DefaultProfile</span></span>
<span data-ttu-id="3a1c3-146">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3a1c3-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a1c3-147">-Filter</span><span class="sxs-lookup"><span data-stu-id="3a1c3-147">-Filter</span></span>
<span data-ttu-id="3a1c3-148">Określa klauzulę filtru OData.</span><span class="sxs-lookup"><span data-stu-id="3a1c3-148">Specifies an OData filter clause.</span></span>
<span data-ttu-id="3a1c3-149">To polecenie cmdlet zwraca właściwości plików węzłów, które pasują do filtru, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="3a1c3-149">This cmdlet returns properties for node files that match the filter that this parameter specifies.</span></span>

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

### <span data-ttu-id="3a1c3-150">-JobId</span><span class="sxs-lookup"><span data-stu-id="3a1c3-150">-JobId</span></span>
<span data-ttu-id="3a1c3-151">Określa identyfikator zadania zawierającego zadanie docelowe.</span><span class="sxs-lookup"><span data-stu-id="3a1c3-151">Specifies the ID of the job that contains the target task.</span></span>

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

### <span data-ttu-id="3a1c3-152">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="3a1c3-152">-MaxCount</span></span>
<span data-ttu-id="3a1c3-153">Określa maksymalną liczbę plików węzłów, dla których to polecenie cmdlet zwraca właściwości.</span><span class="sxs-lookup"><span data-stu-id="3a1c3-153">Specifies the maximum number of node files for which this cmdlet returns properties.</span></span>
<span data-ttu-id="3a1c3-154">Jeśli określisz wartość zero (0) lub mniejszą, polecenie cmdlet nie używa górnego limitu.</span><span class="sxs-lookup"><span data-stu-id="3a1c3-154">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="3a1c3-155">Wartość domyślna to 1000.</span><span class="sxs-lookup"><span data-stu-id="3a1c3-155">The default value is 1000.</span></span>

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

### <span data-ttu-id="3a1c3-156">-Path</span><span class="sxs-lookup"><span data-stu-id="3a1c3-156">-Path</span></span>
<span data-ttu-id="3a1c3-157">Określa ścieżkę pliku węzła, dla którego to polecenie cmdlet pobiera właściwości.</span><span class="sxs-lookup"><span data-stu-id="3a1c3-157">Specifies the path of the node file for which this cmdlet retrieves properties.</span></span>
<span data-ttu-id="3a1c3-158">Nie można określać symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="3a1c3-158">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="3a1c3-159">-PoolId</span><span class="sxs-lookup"><span data-stu-id="3a1c3-159">-PoolId</span></span>
<span data-ttu-id="3a1c3-160">Określa identyfikator puli zawierającej węzeł obliczeniowy, z którego mają być wyświetlane właściwości plików węzłów.</span><span class="sxs-lookup"><span data-stu-id="3a1c3-160">Specifies the ID of the pool that contains the compute node from which to get properties of node files.</span></span>

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

### <span data-ttu-id="3a1c3-161">-Rekursywnie</span><span class="sxs-lookup"><span data-stu-id="3a1c3-161">-Recursive</span></span>
<span data-ttu-id="3a1c3-162">Wskazuje, że to polecenie cmdlet zwraca cykliczną listę plików.</span><span class="sxs-lookup"><span data-stu-id="3a1c3-162">Indicates that this cmdlet returns a recursive list of files.</span></span>
<span data-ttu-id="3a1c3-163">W przeciwnym razie zwróci tylko pliki w folderze głównym.</span><span class="sxs-lookup"><span data-stu-id="3a1c3-163">Otherwise, it returns only the files in the root folder.</span></span>

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

### <span data-ttu-id="3a1c3-164">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="3a1c3-164">-Task</span></span>
<span data-ttu-id="3a1c3-165">Określa zadanie jako obiekt **PSCloudTask** , z którym są skojarzone pliki węzła.</span><span class="sxs-lookup"><span data-stu-id="3a1c3-165">Specifies the task, as a **PSCloudTask** object, with which the node files are associated.</span></span>
<span data-ttu-id="3a1c3-166">Aby uzyskać obiekt zadania, użyj polecenia cmdlet Get-AzBatchTask.</span><span class="sxs-lookup"><span data-stu-id="3a1c3-166">To obtain a task object, use the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="3a1c3-167">-TaskId</span><span class="sxs-lookup"><span data-stu-id="3a1c3-167">-TaskId</span></span>
<span data-ttu-id="3a1c3-168">Określa identyfikator zadania, dla którego to polecenie cmdlet pobiera właściwości plików węzła.</span><span class="sxs-lookup"><span data-stu-id="3a1c3-168">Specifies the ID of the task for which this cmdlet gets properties of node files.</span></span>

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

### <span data-ttu-id="3a1c3-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a1c3-169">CommonParameters</span></span>
<span data-ttu-id="3a1c3-170">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a1c3-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a1c3-171">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a1c3-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a1c3-172">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a1c3-172">INPUTS</span></span>

### <span data-ttu-id="3a1c3-173">System. String</span><span class="sxs-lookup"><span data-stu-id="3a1c3-173">System.String</span></span>

### <span data-ttu-id="3a1c3-174">Microsoft.Azure.Commands.Batch. Modele. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="3a1c3-174">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="3a1c3-175">Microsoft.Azure.Commands.Batch. Modele. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="3a1c3-175">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="3a1c3-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="3a1c3-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="3a1c3-177">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3a1c3-177">OUTPUTS</span></span>

### <span data-ttu-id="3a1c3-178">Microsoft.Azure.Commands.Batch. Modele. PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="3a1c3-178">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>

## <span data-ttu-id="3a1c3-179">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3a1c3-179">NOTES</span></span>

## <span data-ttu-id="3a1c3-180">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a1c3-180">RELATED LINKS</span></span>

[<span data-ttu-id="3a1c3-181">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="3a1c3-181">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="3a1c3-182">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="3a1c3-182">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="3a1c3-183">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="3a1c3-183">Get-AzBatchNodeFileContent</span></span>](./Get-AzBatchNodeFileContent.md)

[<span data-ttu-id="3a1c3-184">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="3a1c3-184">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="3a1c3-185">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="3a1c3-185">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
