---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C9E2D9EC-3B6A-492D-B183-9856185548CD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchnodefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFileContent.md
ms.openlocfilehash: 534919a404ad415963408816b78e9bbf1f349965
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338770"
---
# <span data-ttu-id="40a4b-101">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="40a4b-101">Get-AzBatchNodeFileContent</span></span>

## <span data-ttu-id="40a4b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="40a4b-102">SYNOPSIS</span></span>
<span data-ttu-id="40a4b-103">Pobiera plik węzła wsadowego.</span><span class="sxs-lookup"><span data-stu-id="40a4b-103">Gets a Batch node file.</span></span>

## <span data-ttu-id="40a4b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="40a4b-104">SYNTAX</span></span>

### <span data-ttu-id="40a4b-105">Task_Id_Path</span><span class="sxs-lookup"><span data-stu-id="40a4b-105">Task_Id_Path</span></span>
```
Get-AzBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationPath <String>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40a4b-106">Task_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="40a4b-106">Task_Id_Stream</span></span>
```
Get-AzBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40a4b-107">ComputeNode_Id_Path</span><span class="sxs-lookup"><span data-stu-id="40a4b-107">ComputeNode_Id_Path</span></span>
```
Get-AzBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationPath <String> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40a4b-108">ComputeNode_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="40a4b-108">ComputeNode_Id_Stream</span></span>
```
Get-AzBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationStream <Stream> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40a4b-109">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="40a4b-109">InputObject_Path</span></span>
```
Get-AzBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationPath <String> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="40a4b-110">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="40a4b-110">InputObject_Stream</span></span>
```
Get-AzBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationStream <Stream> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="40a4b-111">Opis</span><span class="sxs-lookup"><span data-stu-id="40a4b-111">DESCRIPTION</span></span>
<span data-ttu-id="40a4b-112">Polecenie cmdlet **Get-AzBatchNodeFileContent** pobiera plik węzła usługi Azure Batch i zapisuje go jako plik lub strumień.</span><span class="sxs-lookup"><span data-stu-id="40a4b-112">The **Get-AzBatchNodeFileContent** cmdlet gets an Azure Batch node file and saves it as a file or to a stream.</span></span>

## <span data-ttu-id="40a4b-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="40a4b-113">EXAMPLES</span></span>

### <span data-ttu-id="40a4b-114">Przykład 1: uzyskiwanie pliku węzła partii skojarzonego z zadaniem i zapisywanie pliku</span><span class="sxs-lookup"><span data-stu-id="40a4b-114">Example 1: Get a Batch node file associated with a task and save the file</span></span>
```
PS C:\>Get-AzBatchNodeFileContent -JobId "Job01" -TaskId "Task01" -Path "StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="40a4b-115">To polecenie powoduje wyświetlenie pliku węzła o nazwie StdOut.txt i zapisanie go w E:\PowerShell\StdOut.txt ścieżki pliku na komputerze lokalnym.</span><span class="sxs-lookup"><span data-stu-id="40a4b-115">This command gets the node file that is named StdOut.txt, and saves it to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="40a4b-116">Plik węzła StdOut.txt jest skojarzony z zadaniem o IDENTYFIKATORze Task01 dla zadania o IDENTYFIKATORze Job01.</span><span class="sxs-lookup"><span data-stu-id="40a4b-116">The StdOut.txt node file is associated with task that has the ID Task01 for the job that has the ID Job01.</span></span>
<span data-ttu-id="40a4b-117">Użyj polecenia cmdlet Get-AzBatchAccountKey, aby przypisać kontekst do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="40a4b-117">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="40a4b-118">Przykład 2: pobranie pliku węzła partii i zapisanie go w określonej ścieżce pliku za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="40a4b-118">Example 2: Get a Batch node file and save it to a specified file path using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job02" -TaskId "Task02" -Path "StdErr.txt" -BatchContext $Context | Get-AzBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="40a4b-119">To polecenie pobiera plik węzła o nazwie StdErr.txt przy użyciu polecenia cmdlet Get-AzBatchNodeFile.</span><span class="sxs-lookup"><span data-stu-id="40a4b-119">This command gets the node file that is named StdErr.txt by using the Get-AzBatchNodeFile cmdlet.</span></span>
<span data-ttu-id="40a4b-120">Polecenie przekazuje ten plik do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="40a4b-120">The command passes that file to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="40a4b-121">Bieżące polecenie cmdlet zapisuje ten plik w ścieżce pliku E:\PowerShell\StdOut.txt na komputerze lokalnym.</span><span class="sxs-lookup"><span data-stu-id="40a4b-121">The current cmdlet saves that file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="40a4b-122">Plik węzła StdOut.txt jest skojarzony z zadaniem zawierającym identyfikator Task02 dla zadania o IDENTYFIKATORze Job02.</span><span class="sxs-lookup"><span data-stu-id="40a4b-122">The StdOut.txt node file is associated with the task that has the ID Task02 for the job that has the ID Job02.</span></span>

### <span data-ttu-id="40a4b-123">Przykład 3: uzyskiwanie pliku węzła partii skojarzonego z zadaniem i kierowanie go do strumienia</span><span class="sxs-lookup"><span data-stu-id="40a4b-123">Example 3: Get a Batch node file associated with a task and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchNodeFileContent -JobId "Job03" -TaskId "Task11" -Path "StdOut.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="40a4b-124">Pierwsze polecenie tworzy strumień za pomocą polecenia cmdlet New-Object, a następnie zapisuje go w zmiennej $Stream.</span><span class="sxs-lookup"><span data-stu-id="40a4b-124">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="40a4b-125">Drugie polecenie pobiera plik węzła o nazwie StdOut.txt z zadania o IDENTYFIKATORze Task11 dla zadania o IDENTYFIKATORze Job03.</span><span class="sxs-lookup"><span data-stu-id="40a4b-125">The second command gets the node file that is named StdOut.txt from the task that has the ID Task11 for the job that has the ID Job03.</span></span>
<span data-ttu-id="40a4b-126">Polecenie kieruje zawartość pliku do strumienia w $Stream.</span><span class="sxs-lookup"><span data-stu-id="40a4b-126">The command directs file contents to the stream in $Stream.</span></span>

### <span data-ttu-id="40a4b-127">Przykład 4: Pobieranie pliku węzła z węzła compute i zapisywanie go</span><span class="sxs-lookup"><span data-stu-id="40a4b-127">Example 4: Get a node file from a compute node and save it</span></span>
```
PS C:\>Get-AzBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="40a4b-128">To polecenie pobiera plik węzła Startup\StdOut.txt z węzła obliczeniowego zawierającego identyfikator ComputeNode01 w puli, która ma identyfikator Pool01.</span><span class="sxs-lookup"><span data-stu-id="40a4b-128">This command gets the node file Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="40a4b-129">Polecenie zapisuje plik w ścieżce pliku E:\PowerShell\StdOut.txt na komputerze lokalnym.</span><span class="sxs-lookup"><span data-stu-id="40a4b-129">The command saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="40a4b-130">Przykład 5: Pobieranie pliku węzła z węzła compute i zapisywanie go za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="40a4b-130">Example 5: Get a node file from a compute node and save it by using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context | Get-AzBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="40a4b-131">To polecenie pobiera plik węzła Startup\StdOut.txt przy użyciu Get-AzBatchNodeFile z węzła obliczeniowego o IDENTYFIKATORze ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="40a4b-131">This command gets the node file Startup\StdOut.txt by using Get-AzBatchNodeFile from the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="40a4b-132">Węzeł obliczeniowy znajduje się w puli o IDENTYFIKATORze Pool01.</span><span class="sxs-lookup"><span data-stu-id="40a4b-132">The compute node is in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="40a4b-133">Polecenie przekazuje ten plik węzła do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40a4b-133">The command passes that node file to the current cmdlet.</span></span>
<span data-ttu-id="40a4b-134">Polecenie cmdlet zapisuje plik w ścieżce pliku E:\PowerShell\StdOut.txt na komputerze lokalnym.</span><span class="sxs-lookup"><span data-stu-id="40a4b-134">That cmdlet saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="40a4b-135">Przykład 6: Pobieranie pliku węzła z węzła obliczeniowego i kierowanie go do strumienia</span><span class="sxs-lookup"><span data-stu-id="40a4b-135">Example 6: Get a node file from a compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "startup\stdout.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="40a4b-136">Pierwsze polecenie tworzy strumień za pomocą polecenia cmdlet New-Object, a następnie zapisuje go w zmiennej $Stream.</span><span class="sxs-lookup"><span data-stu-id="40a4b-136">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="40a4b-137">Drugie polecenie pobiera plik węzła o nazwie StdOut.txt z węzła obliczeniowego o IDENTYFIKATORze ComputeNode01 w puli o IDENTYFIKATORze Pool01.</span><span class="sxs-lookup"><span data-stu-id="40a4b-137">The second command gets the node file that is named StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="40a4b-138">Polecenie kieruje zawartość pliku do strumienia w $Stream.</span><span class="sxs-lookup"><span data-stu-id="40a4b-138">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="40a4b-139">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="40a4b-139">PARAMETERS</span></span>

### <span data-ttu-id="40a4b-140">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="40a4b-140">-BatchContext</span></span>
<span data-ttu-id="40a4b-141">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="40a4b-141">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="40a4b-142">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="40a4b-142">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="40a4b-143">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKey, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="40a4b-143">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="40a4b-144">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="40a4b-144">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="40a4b-145">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="40a4b-145">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="40a4b-146">-ByteRangeEnd</span><span class="sxs-lookup"><span data-stu-id="40a4b-146">-ByteRangeEnd</span></span>
<span data-ttu-id="40a4b-147">Koniec zakresu bajtów, który ma zostać pobrany.</span><span class="sxs-lookup"><span data-stu-id="40a4b-147">The end of the byte range to be downloaded.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40a4b-148">-ByteRangeStart</span><span class="sxs-lookup"><span data-stu-id="40a4b-148">-ByteRangeStart</span></span>
<span data-ttu-id="40a4b-149">Początek zakresu bajtów, który ma zostać pobrany.</span><span class="sxs-lookup"><span data-stu-id="40a4b-149">The start of the byte range to be downloaded.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40a4b-150">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="40a4b-150">-ComputeNodeId</span></span>
<span data-ttu-id="40a4b-151">Określa identyfikator węzła obliczeniowego zawierającego plik węzła, który zostanie zwrócony przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40a4b-151">Specifies the ID of the compute node that contains the node file that this cmdlet returns.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40a4b-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40a4b-152">-DefaultProfile</span></span>
<span data-ttu-id="40a4b-153">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="40a4b-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40a4b-154">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="40a4b-154">-DestinationPath</span></span>
<span data-ttu-id="40a4b-155">Określa ścieżkę pliku, w którym to polecenie cmdlet zapisuje plik węzła.</span><span class="sxs-lookup"><span data-stu-id="40a4b-155">Specifies the file path where this cmdlet saves the node file.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, ComputeNode_Id_Path, InputObject_Path
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40a4b-156">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="40a4b-156">-DestinationStream</span></span>
<span data-ttu-id="40a4b-157">Określa strumień, w którym polecenie cmdlet zapisuje zawartość pliku węzła.</span><span class="sxs-lookup"><span data-stu-id="40a4b-157">Specifies the stream into which this cmdlet writes the node file contents.</span></span>
<span data-ttu-id="40a4b-158">To polecenie cmdlet nie zamyka ani nie Przewija tego strumienia.</span><span class="sxs-lookup"><span data-stu-id="40a4b-158">This cmdlet does not close or rewind this stream.</span></span>

```yaml
Type: System.IO.Stream
Parameter Sets: Task_Id_Stream, ComputeNode_Id_Stream, InputObject_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40a4b-159">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="40a4b-159">-InputObject</span></span>
<span data-ttu-id="40a4b-160">Określa plik, który jest pobierany przez to polecenie cmdlet, jako obiekt **PSNodeFile** .</span><span class="sxs-lookup"><span data-stu-id="40a4b-160">Specifies the file that this cmdlet gets, as a **PSNodeFile** object.</span></span>
<span data-ttu-id="40a4b-161">Aby uzyskać obiekt pliku węzła, użyj polecenia cmdlet Get-AzBatchNodeFile.</span><span class="sxs-lookup"><span data-stu-id="40a4b-161">To obtain a node file object, use the Get-AzBatchNodeFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSNodeFile
Parameter Sets: InputObject_Path, InputObject_Stream
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40a4b-162">-JobId</span><span class="sxs-lookup"><span data-stu-id="40a4b-162">-JobId</span></span>
<span data-ttu-id="40a4b-163">Określa identyfikator zadania zawierającego zadanie docelowe.</span><span class="sxs-lookup"><span data-stu-id="40a4b-163">Specifies the ID of the job that contains the target task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40a4b-164">-Path</span><span class="sxs-lookup"><span data-stu-id="40a4b-164">-Path</span></span>
<span data-ttu-id="40a4b-165">Ścieżka pliku węzła do pobrania.</span><span class="sxs-lookup"><span data-stu-id="40a4b-165">The path of the node file to download.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream, ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40a4b-166">-PoolId</span><span class="sxs-lookup"><span data-stu-id="40a4b-166">-PoolId</span></span>
<span data-ttu-id="40a4b-167">Określa identyfikator puli zawierającej węzeł obliczeniowy, który zawiera plik węzła, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40a4b-167">Specifies the ID of the pool that contains the compute node that contains the node file that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40a4b-168">-TaskId</span><span class="sxs-lookup"><span data-stu-id="40a4b-168">-TaskId</span></span>
<span data-ttu-id="40a4b-169">Określa identyfikator zadania.</span><span class="sxs-lookup"><span data-stu-id="40a4b-169">Specifies the ID of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40a4b-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40a4b-170">CommonParameters</span></span>
<span data-ttu-id="40a4b-171">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40a4b-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40a4b-172">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40a4b-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40a4b-173">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="40a4b-173">INPUTS</span></span>

### <span data-ttu-id="40a4b-174">System. String</span><span class="sxs-lookup"><span data-stu-id="40a4b-174">System.String</span></span>

### <span data-ttu-id="40a4b-175">Microsoft.Azure.Commands.Batch. Modele. PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="40a4b-175">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>

### <span data-ttu-id="40a4b-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="40a4b-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="40a4b-177">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="40a4b-177">OUTPUTS</span></span>

### <span data-ttu-id="40a4b-178">System. void</span><span class="sxs-lookup"><span data-stu-id="40a4b-178">System.Void</span></span>

## <span data-ttu-id="40a4b-179">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="40a4b-179">NOTES</span></span>

## <span data-ttu-id="40a4b-180">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="40a4b-180">RELATED LINKS</span></span>

[<span data-ttu-id="40a4b-181">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="40a4b-181">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="40a4b-182">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="40a4b-182">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="40a4b-183">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="40a4b-183">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
