---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 38ED2854-23D0-400E-A5C8-239346B2AF99
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFile.md
ms.openlocfilehash: 0a027bd15d4b207baf9c69fcb9104428c2881872
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718557"
---
# <span data-ttu-id="98bc6-101">Get-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="98bc6-101">Get-AzureBatchNodeFile</span></span>

## <span data-ttu-id="98bc6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="98bc6-102">SYNOPSIS</span></span>
<span data-ttu-id="98bc6-103">Pobiera właściwości plików węzła wsadowego.</span><span class="sxs-lookup"><span data-stu-id="98bc6-103">Gets the properties of Batch node files.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98bc6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="98bc6-104">SYNTAX</span></span>

### <span data-ttu-id="98bc6-105">ComputeNode_Id (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="98bc6-105">ComputeNode_Id (Default)</span></span>
```
Get-AzureBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [[-Name] <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98bc6-106">Task_Id</span><span class="sxs-lookup"><span data-stu-id="98bc6-106">Task_Id</span></span>
```
Get-AzureBatchNodeFile -JobId <String> -TaskId <String> [[-Name] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98bc6-107">Task_ODataFilter</span><span class="sxs-lookup"><span data-stu-id="98bc6-107">Task_ODataFilter</span></span>
```
Get-AzureBatchNodeFile -JobId <String> -TaskId <String> [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98bc6-108">ParentTask</span><span class="sxs-lookup"><span data-stu-id="98bc6-108">ParentTask</span></span>
```
Get-AzureBatchNodeFile [[-Task] <PSCloudTask>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98bc6-109">ComputeNode_ODataFilter</span><span class="sxs-lookup"><span data-stu-id="98bc6-109">ComputeNode_ODataFilter</span></span>
```
Get-AzureBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Recursive] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="98bc6-110">ParentComputeNode</span><span class="sxs-lookup"><span data-stu-id="98bc6-110">ParentComputeNode</span></span>
```
Get-AzureBatchNodeFile [[-ComputeNode] <PSComputeNode>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98bc6-111">Opis</span><span class="sxs-lookup"><span data-stu-id="98bc6-111">DESCRIPTION</span></span>
<span data-ttu-id="98bc6-112">Polecenie cmdlet **Get-AzureBatchNodeFile** pobiera właściwości plików węzłów usługi Azure Batch dotyczących zadania lub węzła obliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="98bc6-112">The **Get-AzureBatchNodeFile** cmdlet gets the properties of the Azure Batch node files of a task or compute node.</span></span>
<span data-ttu-id="98bc6-113">Aby zawęzić wyniki, możesz określić filtr protokołu OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="98bc6-113">To narrow your results, you can specify an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="98bc6-114">Jeśli określisz zadanie, ale nie filtr, to polecenie cmdlet zwróci właściwości dla wszystkich plików węzłów dla tego zadania.</span><span class="sxs-lookup"><span data-stu-id="98bc6-114">If you specify a task, but not a filter, this cmdlet returns properties for all node files for that task.</span></span>
<span data-ttu-id="98bc6-115">Jeśli określisz węzeł obliczeniowy, ale nie filtr, to polecenie cmdlet zwróci właściwości wszystkich plików węzłów dla tego węzła obliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="98bc6-115">If you specify a compute node, but not a filter, this cmdlet returns properties for all node files for that compute node.</span></span>

## <span data-ttu-id="98bc6-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="98bc6-116">EXAMPLES</span></span>

### <span data-ttu-id="98bc6-117">Przykład 1: uzyskiwanie właściwości pliku węzła skojarzonego z zadaniem</span><span class="sxs-lookup"><span data-stu-id="98bc6-117">Example 1: Get the properties of a node file associated with a task</span></span>
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Name "Stdout.txt" -BatchContext $Context
IsDirectory Name          Properties                                      Url

----------- ----          ----------                                      ---

False       StdOut.txt    Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="98bc6-118">To polecenie pobiera właściwości pliku węzła StdOut.txt skojarzonego z zadaniem o IDENTYFIKATORze Task26 w zadaniu, które ma identyfikator zadania ID-000001.</span><span class="sxs-lookup"><span data-stu-id="98bc6-118">This command gets the properties of the StdOut.txt node file associated with the task that has the ID Task26 in the job that has the ID Job-000001.</span></span>
<span data-ttu-id="98bc6-119">Użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby przypisać kontekst do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="98bc6-119">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="98bc6-120">Przykład 2: uzyskiwanie właściwości plików węzłów skojarzonych z zadaniem za pomocą filtru</span><span class="sxs-lookup"><span data-stu-id="98bc6-120">Example 2: Get the properties of node files associated with a task by using a filter</span></span>
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job-00002" -TaskId "Task26" -Filter "startswith(name,'St')" -BatchContext $Context
IsDirectory Name        Properties                                      Url

----------- ----        ----------                                      ---

False       StdErr.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       StdOut.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="98bc6-121">To polecenie pobiera właściwości plików węzłów, których nazwy zaczynają się od St i są skojarzone z zadaniem zawierającym identyfikator Task26 w obszarze zadanie o identyfikatorze ID-00002.</span><span class="sxs-lookup"><span data-stu-id="98bc6-121">This command gets the properties of the node files whose names start with st and are associated with task that has the ID Task26 under job that has the ID Job-00002.</span></span>

### <span data-ttu-id="98bc6-122">Przykład 3: rekursywnie uzyskiwanie właściwości plików węzłów skojarzonych z zadaniem</span><span class="sxs-lookup"><span data-stu-id="98bc6-122">Example 3: Recursively get the properties of node files associated with a task</span></span>
```
PS C:\>Get-AzureBatchTask "Job-00003" "Task31" -BatchContext $Context | Get-AzureBatchNodeFile -Recursive -BatchContext $Context
IsDirectory Name             Properties                                      Url

----------- ----             ----------                                      ---

False       ProcessEnv.cmd   Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       StdErr.txt       Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       StdOut.txt       Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
True        wd                                                               https://cmdletexample.westus.Batch.contoso... 
False       wd\newFile.txt   Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="98bc6-123">To polecenie pobiera właściwości wszystkich plików skojarzonych z zadaniem, które ma identyfikator Task31 w zadaniu zadania-00003.</span><span class="sxs-lookup"><span data-stu-id="98bc6-123">This command gets the properties of all files associated with the task that has the ID Task31 in job Job-00003.</span></span>
<span data-ttu-id="98bc6-124">To polecenie określa parametr *cykliczny* .</span><span class="sxs-lookup"><span data-stu-id="98bc6-124">This command specifies the *Recursive* parameter.</span></span>
<span data-ttu-id="98bc6-125">Polecenie cmdlet wykonuje więc cykliczne wyszukiwanie plików, a następnie zwraca wd\newFile.txt plik węzła.</span><span class="sxs-lookup"><span data-stu-id="98bc6-125">Therefore, the cmdlet performs a recursive file search is performed, and returns the wd\newFile.txt node file.</span></span>

### <span data-ttu-id="98bc6-126">Przykład 4: uzyskiwanie jednego pliku z węzła obliczeniowego</span><span class="sxs-lookup"><span data-stu-id="98bc6-126">Example 4: Get a single file from a compute node</span></span>
```
PS C:\>Get-AzureBatchNodeFile -PoolId "Pool22" -ComputeNodeId "ComputeNode01" -Name "Startup\StdOut.txt" -BatchContext $Context
IsDirectory Name                    Properties                                      Url
----------- ----                    ----------                                      ---
False       startup\stdout.txt      Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="98bc6-127">To polecenie pobiera plik o nazwie Startup\StdOut.txt z węzła obliczeniowego o IDENTYFIKATORze ComputeNode01 w puli o IDENTYFIKATORze Pool22.</span><span class="sxs-lookup"><span data-stu-id="98bc6-127">This command gets the file that is named Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>

### <span data-ttu-id="98bc6-128">Przykład 5: pobieranie wszystkich plików w folderze z węzła obliczeniowego</span><span class="sxs-lookup"><span data-stu-id="98bc6-128">Example 5: Get all files under a folder from a compute node</span></span>
```
PS C:\>Get-AzureBatchNodeFile -PoolId "Pool22" -ComputeNodeId "ComputeNode01" -Filter "startswith(name,'startup')" -Recursive -BatchContext $Context
IsDirectory Name                      Properties                                      Url
----------- ----                      ----------                                      ---
True        startup                                                                   https://cmdletexample.westus.Batch.contoso... 
False       startup\ProcessEnv.cmd    Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       startup\stderr.txt        Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       startup\stdout.txt        Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
True        startup\wd                                                                https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="98bc6-129">To polecenie pobiera wszystkie pliki w folderze Autostart z węzła obliczeniowego o IDENTYFIKATORze ComputeNode01 w puli o IDENTYFIKATORze Pool22.</span><span class="sxs-lookup"><span data-stu-id="98bc6-129">This command gets all the files under the startup folder from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>
<span data-ttu-id="98bc6-130">To polecenie cmdlet określa parametr *cykliczny* .</span><span class="sxs-lookup"><span data-stu-id="98bc6-130">This cmdlet specifies the *Recursive* parameter.</span></span>

### <span data-ttu-id="98bc6-131">Przykład 6: pobieranie plików z folderu głównego węzła obliczeniowego</span><span class="sxs-lookup"><span data-stu-id="98bc6-131">Example 6: Get files from the root folder of a compute node</span></span>
```
PS C:\>Get-AzureBatchComputeNode "Pool22" -Id "ComputeNode01" -BatchContext $Context | Get-AzureBatchNodeFile -BatchContext $Context
IsDirectory Name           Properties       Url
----------- ----           ----------       ---
True        shared                          https://cmdletexample.westus.Batch.contoso... 
True        startup                         https://cmdletexample.westus.Batch.contoso... 
True        workitems                       https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="98bc6-132">To polecenie pobiera wszystkie pliki w folderze głównym węzła obliczeniowego o IDENTYFIKATORze ComputeNode01 w puli o IDENTYFIKATORze Pool22.</span><span class="sxs-lookup"><span data-stu-id="98bc6-132">This command gets all the files at the root folder of the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>

## <span data-ttu-id="98bc6-133">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="98bc6-133">PARAMETERS</span></span>

### <span data-ttu-id="98bc6-134">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="98bc6-134">-BatchContext</span></span>
<span data-ttu-id="98bc6-135">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="98bc6-135">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="98bc6-136">Aby uzyskać obiekt **BatchAccountContext** , który zawiera klucze dostępu dla subskrypcji, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="98bc6-136">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="98bc6-137">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="98bc6-137">-ComputeNode</span></span>
<span data-ttu-id="98bc6-138">Określa węzeł obliczeniowe jako obiekt **PSComputeNode** , który zawiera pliki węzła partii.</span><span class="sxs-lookup"><span data-stu-id="98bc6-138">Specifies the compute node, as a **PSComputeNode** object, that contains the Batch node files.</span></span>
<span data-ttu-id="98bc6-139">Aby uzyskać obiekt węzła obliczeniowego, użyj polecenia cmdlet Get-AzureBatchComputeNode.</span><span class="sxs-lookup"><span data-stu-id="98bc6-139">To obtain a compute node object, use the Get-AzureBatchComputeNode cmdlet.</span></span>

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

### <span data-ttu-id="98bc6-140">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="98bc6-140">-ComputeNodeId</span></span>
<span data-ttu-id="98bc6-141">Określa identyfikator węzła obliczeniowego zawierającego pliki węzła partii.</span><span class="sxs-lookup"><span data-stu-id="98bc6-141">Specifies the ID of the compute node that contains the Batch node files.</span></span>

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

### <span data-ttu-id="98bc6-142">-Filter</span><span class="sxs-lookup"><span data-stu-id="98bc6-142">-Filter</span></span>
<span data-ttu-id="98bc6-143">Określa klauzulę filtru OData.</span><span class="sxs-lookup"><span data-stu-id="98bc6-143">Specifies an OData filter clause.</span></span>
<span data-ttu-id="98bc6-144">To polecenie cmdlet zwraca właściwości plików węzłów, które pasują do filtru, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="98bc6-144">This cmdlet returns properties for node files that match the filter that this parameter specifies.</span></span>

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

### <span data-ttu-id="98bc6-145">-JobId</span><span class="sxs-lookup"><span data-stu-id="98bc6-145">-JobId</span></span>
<span data-ttu-id="98bc6-146">Określa identyfikator zadania zawierającego zadanie docelowe.</span><span class="sxs-lookup"><span data-stu-id="98bc6-146">Specifies the ID of the job that contains the target task.</span></span>

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

### <span data-ttu-id="98bc6-147">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="98bc6-147">-MaxCount</span></span>
<span data-ttu-id="98bc6-148">Określa maksymalną liczbę plików węzłów, dla których to polecenie cmdlet zwraca właściwości.</span><span class="sxs-lookup"><span data-stu-id="98bc6-148">Specifies the maximum number of node files for which this cmdlet returns properties.</span></span>
<span data-ttu-id="98bc6-149">Jeśli określisz wartość zero (0) lub mniejszą, polecenie cmdlet nie używa górnego limitu.</span><span class="sxs-lookup"><span data-stu-id="98bc6-149">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="98bc6-150">Wartość domyślna to 1000.</span><span class="sxs-lookup"><span data-stu-id="98bc6-150">The default value is 1000.</span></span>

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

### <span data-ttu-id="98bc6-151">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="98bc6-151">-Name</span></span>
<span data-ttu-id="98bc6-152">Określa nazwę pliku węzła, dla którego to polecenie cmdlet pobiera właściwości.</span><span class="sxs-lookup"><span data-stu-id="98bc6-152">Specifies the name of the node file for which this cmdlet retrieves properties.</span></span>
<span data-ttu-id="98bc6-153">Nie można określać symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="98bc6-153">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id, Task_Id
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98bc6-154">-PoolId</span><span class="sxs-lookup"><span data-stu-id="98bc6-154">-PoolId</span></span>
<span data-ttu-id="98bc6-155">Określa identyfikator puli zawierającej węzeł obliczeniowy, z którego mają być wyświetlane właściwości plików węzłów.</span><span class="sxs-lookup"><span data-stu-id="98bc6-155">Specifies the ID of the pool that contains the compute node from which to get properties of node files.</span></span>

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

### <span data-ttu-id="98bc6-156">-Rekursywnie</span><span class="sxs-lookup"><span data-stu-id="98bc6-156">-Recursive</span></span>
<span data-ttu-id="98bc6-157">Wskazuje, że to polecenie cmdlet zwraca cykliczną listę plików.</span><span class="sxs-lookup"><span data-stu-id="98bc6-157">Indicates that this cmdlet returns a recursive list of files.</span></span>
<span data-ttu-id="98bc6-158">W przeciwnym razie zwróci tylko pliki w folderze głównym.</span><span class="sxs-lookup"><span data-stu-id="98bc6-158">Otherwise, it returns only the files in the root folder.</span></span>

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

### <span data-ttu-id="98bc6-159">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="98bc6-159">-Task</span></span>
<span data-ttu-id="98bc6-160">Określa zadanie jako obiekt **PSCloudTask** , z którym są skojarzone pliki węzła.</span><span class="sxs-lookup"><span data-stu-id="98bc6-160">Specifies the task, as a **PSCloudTask** object, with which the node files are associated.</span></span>
<span data-ttu-id="98bc6-161">Aby uzyskać obiekt zadania, użyj polecenia cmdlet Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="98bc6-161">To obtain a task object, use the Get-AzureBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="98bc6-162">-TaskId</span><span class="sxs-lookup"><span data-stu-id="98bc6-162">-TaskId</span></span>
<span data-ttu-id="98bc6-163">Określa identyfikator zadania, dla którego to polecenie cmdlet pobiera właściwości plików węzła.</span><span class="sxs-lookup"><span data-stu-id="98bc6-163">Specifies the ID of the task for which this cmdlet gets properties of node files.</span></span>

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

### <span data-ttu-id="98bc6-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98bc6-164">-DefaultProfile</span></span>
<span data-ttu-id="98bc6-165">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="98bc6-165">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98bc6-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98bc6-166">CommonParameters</span></span>
<span data-ttu-id="98bc6-167">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98bc6-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98bc6-168">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98bc6-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98bc6-169">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98bc6-169">INPUTS</span></span>

### <span data-ttu-id="98bc6-170">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="98bc6-170">BatchAccountContext</span></span>
<span data-ttu-id="98bc6-171">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="98bc6-171">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="98bc6-172">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="98bc6-172">PSComputeNode</span></span>
<span data-ttu-id="98bc6-173">Parametr "ComputeNode" akceptuje wartość typu "PSComputeNode" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="98bc6-173">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

### <span data-ttu-id="98bc6-174">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="98bc6-174">PSCloudTask</span></span>
<span data-ttu-id="98bc6-175">Parametr "zadanie" akceptuje wartość typu "PSCloudTask" z potoku.</span><span class="sxs-lookup"><span data-stu-id="98bc6-175">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="98bc6-176">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="98bc6-176">OUTPUTS</span></span>

### <span data-ttu-id="98bc6-177">PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="98bc6-177">PSNodeFile</span></span>

## <span data-ttu-id="98bc6-178">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="98bc6-178">NOTES</span></span>

## <span data-ttu-id="98bc6-179">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="98bc6-179">RELATED LINKS</span></span>

[<span data-ttu-id="98bc6-180">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="98bc6-180">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="98bc6-181">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="98bc6-181">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="98bc6-182">Get-AzureBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="98bc6-182">Get-AzureBatchNodeFileContent</span></span>](./Get-AzureBatchNodeFileContent.md)

[<span data-ttu-id="98bc6-183">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="98bc6-183">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="98bc6-184">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="98bc6-184">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


