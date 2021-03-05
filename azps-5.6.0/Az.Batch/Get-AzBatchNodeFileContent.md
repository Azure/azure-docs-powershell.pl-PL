---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C9E2D9EC-3B6A-492D-B183-9856185548CD
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchnodefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFileContent.md
ms.openlocfilehash: 5790d217a63b7c2ef3aa7011d5f8a708df1dfbac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983457"
---
# <span data-ttu-id="20068-101">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="20068-101">Get-AzBatchNodeFileContent</span></span>

## <span data-ttu-id="20068-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20068-102">SYNOPSIS</span></span>
<span data-ttu-id="20068-103">Pobiera plik węzła Batch.</span><span class="sxs-lookup"><span data-stu-id="20068-103">Gets a Batch node file.</span></span>

## <span data-ttu-id="20068-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="20068-104">SYNTAX</span></span>

### <span data-ttu-id="20068-105">Task_Id_Path</span><span class="sxs-lookup"><span data-stu-id="20068-105">Task_Id_Path</span></span>
```
Get-AzBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationPath <String>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20068-106">Task_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="20068-106">Task_Id_Stream</span></span>
```
Get-AzBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20068-107">ComputeNode_Id_Path</span><span class="sxs-lookup"><span data-stu-id="20068-107">ComputeNode_Id_Path</span></span>
```
Get-AzBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationPath <String> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20068-108">ComputeNode_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="20068-108">ComputeNode_Id_Stream</span></span>
```
Get-AzBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationStream <Stream> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20068-109">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="20068-109">InputObject_Path</span></span>
```
Get-AzBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationPath <String> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="20068-110">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="20068-110">InputObject_Stream</span></span>
```
Get-AzBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationStream <Stream> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="20068-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="20068-111">DESCRIPTION</span></span>
<span data-ttu-id="20068-112">Polecenie **cmdlet Get-AzBatchNodeFileContent** pobiera plik węzła usługi Azure Batch i zapisuje go jako plik lub w strumieniu.</span><span class="sxs-lookup"><span data-stu-id="20068-112">The **Get-AzBatchNodeFileContent** cmdlet gets an Azure Batch node file and saves it as a file or to a stream.</span></span>

## <span data-ttu-id="20068-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="20068-113">EXAMPLES</span></span>

### <span data-ttu-id="20068-114">Przykład 1. Uzyskiwanie pliku węzła wsadowego skojarzonego z zadaniem i zapisywanie pliku</span><span class="sxs-lookup"><span data-stu-id="20068-114">Example 1: Get a Batch node file associated with a task and save the file</span></span>
```
PS C:\>Get-AzBatchNodeFileContent -JobId "Job01" -TaskId "Task01" -Path "StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="20068-115">To polecenie pobiera plik węzła o nazwie StdOut.txt i zapisuje go E:\PowerShell\StdOut.txt ścieżce pliku na komputerze lokalnym.</span><span class="sxs-lookup"><span data-stu-id="20068-115">This command gets the node file that is named StdOut.txt, and saves it to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="20068-116">Plik StdOut.txt jest skojarzony z zadaniem o identyfikatorze Zadanie01 dla zadania o identyfikatorze Zadanie01.</span><span class="sxs-lookup"><span data-stu-id="20068-116">The StdOut.txt node file is associated with task that has the ID Task01 for the job that has the ID Job01.</span></span>
<span data-ttu-id="20068-117">Użyj Get-AzBatchAccountKey cmdlet, aby przypisać kontekst do zmiennej $Context danych.</span><span class="sxs-lookup"><span data-stu-id="20068-117">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="20068-118">Przykład 2. Pobierz plik węzła wsadowy i zapisz go w określonej ścieżce pliku przy użyciu potoku</span><span class="sxs-lookup"><span data-stu-id="20068-118">Example 2: Get a Batch node file and save it to a specified file path using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job02" -TaskId "Task02" -Path "StdErr.txt" -BatchContext $Context | Get-AzBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="20068-119">To polecenie pobiera plik węzła o nazwie StdErr.txt za pomocą Get-AzBatchNodeFile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20068-119">This command gets the node file that is named StdErr.txt by using the Get-AzBatchNodeFile cmdlet.</span></span>
<span data-ttu-id="20068-120">Polecenie przekazuje ten plik do bieżącego polecenia cmdlet przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="20068-120">The command passes that file to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="20068-121">Bieżące polecenie cmdlet zapisuje ten plik w E:\PowerShell\StdOut.txt ścieżce pliku na komputerze lokalnym.</span><span class="sxs-lookup"><span data-stu-id="20068-121">The current cmdlet saves that file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="20068-122">Plik StdOut.txt węzła jest skojarzony z zadaniem, które ma identyfikator Task02 dla zadania o identyfikatorze Zadanie02.</span><span class="sxs-lookup"><span data-stu-id="20068-122">The StdOut.txt node file is associated with the task that has the ID Task02 for the job that has the ID Job02.</span></span>

### <span data-ttu-id="20068-123">Przykład 3. Pobierz plik węzła Batch skojarzony z zadaniem i przekieruj go do strumienia</span><span class="sxs-lookup"><span data-stu-id="20068-123">Example 3: Get a Batch node file associated with a task and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchNodeFileContent -JobId "Job03" -TaskId "Task11" -Path "StdOut.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="20068-124">Pierwsze polecenie tworzy strumień przy użyciu New-Object cmdlet, a następnie zapisuje go w $Stream zmienną.</span><span class="sxs-lookup"><span data-stu-id="20068-124">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="20068-125">Drugie polecenie pobiera plik węzła o nazwie StdOut.txt z zadania o identyfikatorze Zadanie11 dla zadania o identyfikatorze Zadanie03.</span><span class="sxs-lookup"><span data-stu-id="20068-125">The second command gets the node file that is named StdOut.txt from the task that has the ID Task11 for the job that has the ID Job03.</span></span>
<span data-ttu-id="20068-126">Polecenie kieruje zawartość pliku do strumienia w $Stream.</span><span class="sxs-lookup"><span data-stu-id="20068-126">The command directs file contents to the stream in $Stream.</span></span>

### <span data-ttu-id="20068-127">Przykład 4. Pobierz plik węzła z węzła obliczeniowego i zapisz go</span><span class="sxs-lookup"><span data-stu-id="20068-127">Example 4: Get a node file from a compute node and save it</span></span>
```
PS C:\>Get-AzBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="20068-128">To polecenie pobiera plik węzła Startup\StdOut.txt z węzła obliczeniowego o identyfikatorze ComputeNode01 w puli, która ma pulę identyfikatorów 01.</span><span class="sxs-lookup"><span data-stu-id="20068-128">This command gets the node file Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="20068-129">Polecenie zapisze plik w E:\PowerShell\StdOut.txt ścieżki pliku na komputerze lokalnym.</span><span class="sxs-lookup"><span data-stu-id="20068-129">The command saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="20068-130">Przykład 5. Pobierz plik węzła z węzła obliczeniowego i zapisz go przy użyciu potoku</span><span class="sxs-lookup"><span data-stu-id="20068-130">Example 5: Get a node file from a compute node and save it by using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context | Get-AzBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="20068-131">To polecenie pobiera plik węzła Startup\StdOut.txt, używając Get-AzBatchNodeFile z węzła obliczeniowego, który ma identyfikator ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="20068-131">This command gets the node file Startup\StdOut.txt by using Get-AzBatchNodeFile from the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="20068-132">Węzeł obliczeniowy znajduje się w puli, która ma pulę identyfikatorów 01.</span><span class="sxs-lookup"><span data-stu-id="20068-132">The compute node is in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="20068-133">Polecenie przekazuje ten plik węzła do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20068-133">The command passes that node file to the current cmdlet.</span></span>
<span data-ttu-id="20068-134">To polecenie cmdlet zapisuje plik w E:\PowerShell\StdOut.txt ścieżce pliku na komputerze lokalnym.</span><span class="sxs-lookup"><span data-stu-id="20068-134">That cmdlet saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="20068-135">Przykład 6. Pobierz plik węzła z węzła obliczeniowego i przekieruj go do strumienia</span><span class="sxs-lookup"><span data-stu-id="20068-135">Example 6: Get a node file from a compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "startup\stdout.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="20068-136">Pierwsze polecenie tworzy strumień przy użyciu New-Object cmdlet, a następnie zapisuje go w $Stream zmienną.</span><span class="sxs-lookup"><span data-stu-id="20068-136">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="20068-137">Drugie polecenie pobiera plik węzła o nazwie StdOut.txt z węzła obliczeniowego o identyfikatorze ComputeNode01 w puli o identyfikatorze Pool01.</span><span class="sxs-lookup"><span data-stu-id="20068-137">The second command gets the node file that is named StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="20068-138">Polecenie kieruje zawartość pliku do strumienia w $Stream.</span><span class="sxs-lookup"><span data-stu-id="20068-138">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="20068-139">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="20068-139">PARAMETERS</span></span>

### <span data-ttu-id="20068-140">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="20068-140">-BatchContext</span></span>
<span data-ttu-id="20068-141">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="20068-141">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="20068-142">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="20068-142">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="20068-143">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="20068-143">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="20068-144">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="20068-144">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="20068-145">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="20068-145">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="20068-146">-ByteRangeEnd</span><span class="sxs-lookup"><span data-stu-id="20068-146">-ByteRangeEnd</span></span>
<span data-ttu-id="20068-147">Koniec zakresu bajtów do pobrania.</span><span class="sxs-lookup"><span data-stu-id="20068-147">The end of the byte range to be downloaded.</span></span>

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

### <span data-ttu-id="20068-148">-ByteRangeStart</span><span class="sxs-lookup"><span data-stu-id="20068-148">-ByteRangeStart</span></span>
<span data-ttu-id="20068-149">Początek zakresu bajtów do pobrania.</span><span class="sxs-lookup"><span data-stu-id="20068-149">The start of the byte range to be downloaded.</span></span>

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

### <span data-ttu-id="20068-150">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="20068-150">-ComputeNodeId</span></span>
<span data-ttu-id="20068-151">Określa identyfikator węzła obliczeniowego zawierającego plik węzła zwracany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20068-151">Specifies the ID of the compute node that contains the node file that this cmdlet returns.</span></span>

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

### <span data-ttu-id="20068-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20068-152">-DefaultProfile</span></span>
<span data-ttu-id="20068-153">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="20068-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20068-154">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="20068-154">-DestinationPath</span></span>
<span data-ttu-id="20068-155">Określa ścieżkę pliku, w której to polecenie cmdlet zapisuje plik węzła.</span><span class="sxs-lookup"><span data-stu-id="20068-155">Specifies the file path where this cmdlet saves the node file.</span></span>

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

### <span data-ttu-id="20068-156">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="20068-156">-DestinationStream</span></span>
<span data-ttu-id="20068-157">Określa strumień, do którego to polecenie cmdlet zapisuje zawartość pliku węzła.</span><span class="sxs-lookup"><span data-stu-id="20068-157">Specifies the stream into which this cmdlet writes the node file contents.</span></span>
<span data-ttu-id="20068-158">To polecenie cmdlet nie zamyka ani nie przewija tego strumienia.</span><span class="sxs-lookup"><span data-stu-id="20068-158">This cmdlet does not close or rewind this stream.</span></span>

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

### <span data-ttu-id="20068-159">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20068-159">-InputObject</span></span>
<span data-ttu-id="20068-160">Określa plik, który to polecenie cmdlet pobiera jako **obiekt PSNodeFile.**</span><span class="sxs-lookup"><span data-stu-id="20068-160">Specifies the file that this cmdlet gets, as a **PSNodeFile** object.</span></span>
<span data-ttu-id="20068-161">Aby uzyskać obiekt pliku węzła, użyj Get-AzBatchNodeFile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20068-161">To obtain a node file object, use the Get-AzBatchNodeFile cmdlet.</span></span>

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

### <span data-ttu-id="20068-162">- JobId</span><span class="sxs-lookup"><span data-stu-id="20068-162">-JobId</span></span>
<span data-ttu-id="20068-163">Określa identyfikator zadania zawierającego zadanie docelowe.</span><span class="sxs-lookup"><span data-stu-id="20068-163">Specifies the ID of the job that contains the target task.</span></span>

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

### <span data-ttu-id="20068-164">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="20068-164">-Path</span></span>
<span data-ttu-id="20068-165">Ścieżka pliku węzła do pobrania.</span><span class="sxs-lookup"><span data-stu-id="20068-165">The path of the node file to download.</span></span>

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

### <span data-ttu-id="20068-166">- PoolId</span><span class="sxs-lookup"><span data-stu-id="20068-166">-PoolId</span></span>
<span data-ttu-id="20068-167">Określa identyfikator puli zawierającej węzeł obliczeniowy zawierający plik węzła, który pobiera to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20068-167">Specifies the ID of the pool that contains the compute node that contains the node file that this cmdlet gets.</span></span>

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

### <span data-ttu-id="20068-168">- TaskId</span><span class="sxs-lookup"><span data-stu-id="20068-168">-TaskId</span></span>
<span data-ttu-id="20068-169">Określa identyfikator zadania.</span><span class="sxs-lookup"><span data-stu-id="20068-169">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="20068-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20068-170">CommonParameters</span></span>
<span data-ttu-id="20068-171">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20068-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20068-172">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="20068-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20068-173">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="20068-173">INPUTS</span></span>

### <span data-ttu-id="20068-174">System.String</span><span class="sxs-lookup"><span data-stu-id="20068-174">System.String</span></span>

### <span data-ttu-id="20068-175">Microsoft.Azure.Commands.Batch. Models.PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="20068-175">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>

### <span data-ttu-id="20068-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="20068-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="20068-177">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="20068-177">OUTPUTS</span></span>

### <span data-ttu-id="20068-178">System.Void</span><span class="sxs-lookup"><span data-stu-id="20068-178">System.Void</span></span>

## <span data-ttu-id="20068-179">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="20068-179">NOTES</span></span>

## <span data-ttu-id="20068-180">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="20068-180">RELATED LINKS</span></span>

[<span data-ttu-id="20068-181">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="20068-181">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="20068-182">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="20068-182">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="20068-183">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="20068-183">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
