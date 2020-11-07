---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C9E2D9EC-3B6A-492D-B183-9856185548CD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFileContent.md
ms.openlocfilehash: 92c485a743372eff7ddb8725172ac4d9bb030d22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718555"
---
# <span data-ttu-id="1c3ad-101">Get-AzureBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="1c3ad-101">Get-AzureBatchNodeFileContent</span></span>

## <span data-ttu-id="1c3ad-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1c3ad-102">SYNOPSIS</span></span>
<span data-ttu-id="1c3ad-103">Pobiera plik węzła wsadowego.</span><span class="sxs-lookup"><span data-stu-id="1c3ad-103">Gets a Batch node file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c3ad-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1c3ad-104">SYNTAX</span></span>

### <span data-ttu-id="1c3ad-105">Task_Id_Path</span><span class="sxs-lookup"><span data-stu-id="1c3ad-105">Task_Id_Path</span></span>
```
Get-AzureBatchNodeFileContent -JobId <String> -TaskId <String> [-Name] <String> -DestinationPath <String>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c3ad-106">Task_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="1c3ad-106">Task_Id_Stream</span></span>
```
Get-AzureBatchNodeFileContent -JobId <String> -TaskId <String> [-Name] <String> -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c3ad-107">ComputeNode_Id_Path</span><span class="sxs-lookup"><span data-stu-id="1c3ad-107">ComputeNode_Id_Path</span></span>
```
Get-AzureBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -DestinationPath <String> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c3ad-108">ComputeNode_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="1c3ad-108">ComputeNode_Id_Stream</span></span>
```
Get-AzureBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -DestinationStream <Stream> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c3ad-109">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="1c3ad-109">InputObject_Path</span></span>
```
Get-AzureBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationPath <String> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1c3ad-110">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="1c3ad-110">InputObject_Stream</span></span>
```
Get-AzureBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c3ad-111">Opis</span><span class="sxs-lookup"><span data-stu-id="1c3ad-111">DESCRIPTION</span></span>
<span data-ttu-id="1c3ad-112">Polecenie cmdlet **Get-AzureBatchNodeFileContent** pobiera plik węzła usługi Azure Batch i zapisuje go jako plik lub strumień.</span><span class="sxs-lookup"><span data-stu-id="1c3ad-112">The **Get-AzureBatchNodeFileContent** cmdlet gets an Azure Batch node file and saves it as a file or to a stream.</span></span>

## <span data-ttu-id="1c3ad-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1c3ad-113">EXAMPLES</span></span>

### <span data-ttu-id="1c3ad-114">Przykład 1: uzyskiwanie pliku węzła partii skojarzonego z zadaniem i zapisywanie pliku</span><span class="sxs-lookup"><span data-stu-id="1c3ad-114">Example 1: Get a Batch node file associated with a task and save the file</span></span>
```
PS C:\>Get-AzureBatchNodeFileContent -JobId "Job01" -TaskId "Task01" -Name "StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="1c3ad-115">To polecenie powoduje wyświetlenie pliku węzła o nazwie StdOut.txt i zapisanie go w E:\PowerShell\StdOut.txt ścieżki pliku na komputerze lokalnym.</span><span class="sxs-lookup"><span data-stu-id="1c3ad-115">This command gets the node file that is named StdOut.txt, and saves it to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="1c3ad-116">Plik węzła StdOut.txt jest skojarzony z zadaniem o IDENTYFIKATORze Task01 dla zadania o IDENTYFIKATORze Job01.</span><span class="sxs-lookup"><span data-stu-id="1c3ad-116">The StdOut.txt node file is associated with task that has the ID Task01 for the job that has the ID Job01.</span></span>
<span data-ttu-id="1c3ad-117">Użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby przypisać kontekst do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="1c3ad-117">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="1c3ad-118">Przykład 2: pobranie pliku węzła partii i zapisanie go w określonej ścieżce pliku za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="1c3ad-118">Example 2: Get a Batch node file and save it to a specified file path using the pipeline</span></span>
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job02" -TaskId "Task02" -Name "StdErr.txt" -BatchContext $Context | Get-AzureBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="1c3ad-119">To polecenie pobiera plik węzła o nazwie StdErr.txt przy użyciu polecenia cmdlet Get-AzureBatchNodeFile.</span><span class="sxs-lookup"><span data-stu-id="1c3ad-119">This command gets the node file that is named StdErr.txt by using the Get-AzureBatchNodeFile cmdlet.</span></span>
<span data-ttu-id="1c3ad-120">Polecenie przekazuje ten plik do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="1c3ad-120">The command passes that file to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1c3ad-121">Bieżące polecenie cmdlet zapisuje ten plik w ścieżce pliku E:\PowerShell\StdOut.txt na komputerze lokalnym.</span><span class="sxs-lookup"><span data-stu-id="1c3ad-121">The current cmdlet saves that file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="1c3ad-122">Plik węzła StdOut.txt jest skojarzony z zadaniem zawierającym identyfikator Task02 dla zadania o IDENTYFIKATORze Job02.</span><span class="sxs-lookup"><span data-stu-id="1c3ad-122">The StdOut.txt node file is associated with the task that has the ID Task02 for the job that has the ID Job02.</span></span>

### <span data-ttu-id="1c3ad-123">Przykład 3: uzyskiwanie pliku węzła partii skojarzonego z zadaniem i kierowanie go do strumienia</span><span class="sxs-lookup"><span data-stu-id="1c3ad-123">Example 3: Get a Batch node file associated with a task and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzureBatchNodeFileContent -JobId "Job03" -TaskId "Task11" -Name "StdOut.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="1c3ad-124">Pierwsze polecenie tworzy strumień za pomocą polecenia cmdlet New-Object, a następnie zapisuje go w zmiennej $Stream.</span><span class="sxs-lookup"><span data-stu-id="1c3ad-124">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>

<span data-ttu-id="1c3ad-125">Drugie polecenie pobiera plik węzła o nazwie StdOut.txt z zadania o IDENTYFIKATORze Task11 dla zadania o IDENTYFIKATORze Job03.</span><span class="sxs-lookup"><span data-stu-id="1c3ad-125">The second command gets the node file that is named StdOut.txt from the task that has the ID Task11 for the job that has the ID Job03.</span></span>
<span data-ttu-id="1c3ad-126">Polecenie kieruje zawartość pliku do strumienia w $Stream.</span><span class="sxs-lookup"><span data-stu-id="1c3ad-126">The command directs file contents to the stream in $Stream.</span></span>

### <span data-ttu-id="1c3ad-127">Przykład 4: Pobieranie pliku węzła z węzła compute i zapisywanie go</span><span class="sxs-lookup"><span data-stu-id="1c3ad-127">Example 4: Get a node file from a compute node and save it</span></span>
```
PS C:\>Get-AzureBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "Startup\StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="1c3ad-128">To polecenie pobiera plik węzła Startup\StdOut.txt z węzła obliczeniowego zawierającego identyfikator ComputeNode01 w puli, która ma identyfikator Pool01.</span><span class="sxs-lookup"><span data-stu-id="1c3ad-128">This command gets the node file Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="1c3ad-129">Polecenie zapisuje plik w ścieżce pliku E:\PowerShell\StdOut.txt na komputerze lokalnym.</span><span class="sxs-lookup"><span data-stu-id="1c3ad-129">The command saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="1c3ad-130">Przykład 5: Pobieranie pliku węzła z węzła compute i zapisywanie go za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="1c3ad-130">Example 5: Get a node file from a compute node and save it by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchNodeFile -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "Startup\StdOut.txt" -BatchContext $Context | Get-AzureBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="1c3ad-131">To polecenie pobiera plik węzła Startup\StdOut.txt przy użyciu Get-AzureBatchNodeFile z węzła obliczeniowego o IDENTYFIKATORze ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="1c3ad-131">This command gets the node file Startup\StdOut.txt by using Get-AzureBatchNodeFile from the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="1c3ad-132">Węzeł obliczeniowy znajduje się w puli o IDENTYFIKATORze Pool01.</span><span class="sxs-lookup"><span data-stu-id="1c3ad-132">The compute node is in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="1c3ad-133">Polecenie przekazuje ten plik węzła do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c3ad-133">The command passes that node file to the current cmdlet.</span></span>
<span data-ttu-id="1c3ad-134">Polecenie cmdlet zapisuje plik w ścieżce pliku E:\PowerShell\StdOut.txt na komputerze lokalnym.</span><span class="sxs-lookup"><span data-stu-id="1c3ad-134">That cmdlet saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="1c3ad-135">Przykład 6: Pobieranie pliku węzła z węzła obliczeniowego i kierowanie go do strumienia</span><span class="sxs-lookup"><span data-stu-id="1c3ad-135">Example 6: Get a node file from a compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzureBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "startup\stdout.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="1c3ad-136">Pierwsze polecenie tworzy strumień za pomocą polecenia cmdlet New-Object, a następnie zapisuje go w zmiennej $Stream.</span><span class="sxs-lookup"><span data-stu-id="1c3ad-136">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>

<span data-ttu-id="1c3ad-137">Drugie polecenie pobiera plik węzła o nazwie StdOut.txt z węzła obliczeniowego o IDENTYFIKATORze ComputeNode01 w puli o IDENTYFIKATORze Pool01.</span><span class="sxs-lookup"><span data-stu-id="1c3ad-137">The second command gets the node file that is named StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="1c3ad-138">Polecenie kieruje zawartość pliku do strumienia w $Stream.</span><span class="sxs-lookup"><span data-stu-id="1c3ad-138">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="1c3ad-139">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1c3ad-139">PARAMETERS</span></span>

### <span data-ttu-id="1c3ad-140">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="1c3ad-140">-BatchContext</span></span>
<span data-ttu-id="1c3ad-141">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="1c3ad-141">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="1c3ad-142">Aby uzyskać obiekt **BatchAccountContext** , który zawiera klucze dostępu dla subskrypcji, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="1c3ad-142">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="1c3ad-143">-ByteRangeEnd</span><span class="sxs-lookup"><span data-stu-id="1c3ad-143">-ByteRangeEnd</span></span>
<span data-ttu-id="1c3ad-144">Koniec zakresu bajtów, który ma zostać pobrany.</span><span class="sxs-lookup"><span data-stu-id="1c3ad-144">The end of the byte range to be downloaded.</span></span>
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

### <span data-ttu-id="1c3ad-145">-ByteRangeStart</span><span class="sxs-lookup"><span data-stu-id="1c3ad-145">-ByteRangeStart</span></span>
<span data-ttu-id="1c3ad-146">Początek zakresu bajtów, który ma zostać pobrany.</span><span class="sxs-lookup"><span data-stu-id="1c3ad-146">The start of the byte range to be downloaded.</span></span>
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

### <span data-ttu-id="1c3ad-147">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="1c3ad-147">-ComputeNodeId</span></span>
<span data-ttu-id="1c3ad-148">Określa identyfikator węzła obliczeniowego zawierającego plik węzła, który zostanie zwrócony przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c3ad-148">Specifies the ID of the compute node that contains the node file that this cmdlet returns.</span></span>

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

### <span data-ttu-id="1c3ad-149">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="1c3ad-149">-DestinationPath</span></span>
<span data-ttu-id="1c3ad-150">Określa ścieżkę pliku, w którym to polecenie cmdlet zapisuje plik węzła.</span><span class="sxs-lookup"><span data-stu-id="1c3ad-150">Specifies the file path where this cmdlet saves the node file.</span></span>

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

### <span data-ttu-id="1c3ad-151">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="1c3ad-151">-DestinationStream</span></span>
<span data-ttu-id="1c3ad-152">Określa strumień, w którym polecenie cmdlet zapisuje zawartość pliku węzła.</span><span class="sxs-lookup"><span data-stu-id="1c3ad-152">Specifies the stream into which this cmdlet writes the node file contents.</span></span>
<span data-ttu-id="1c3ad-153">To polecenie cmdlet nie zamyka ani nie Przewija tego strumienia.</span><span class="sxs-lookup"><span data-stu-id="1c3ad-153">This cmdlet does not close or rewind this stream.</span></span>

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

### <span data-ttu-id="1c3ad-154">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1c3ad-154">-InputObject</span></span>
<span data-ttu-id="1c3ad-155">Określa plik, który jest pobierany przez to polecenie cmdlet, jako obiekt **PSNodeFile** .</span><span class="sxs-lookup"><span data-stu-id="1c3ad-155">Specifies the file that this cmdlet gets, as a **PSNodeFile** object.</span></span>
<span data-ttu-id="1c3ad-156">Aby uzyskać obiekt pliku węzła, użyj polecenia cmdlet Get-AzureBatchNodeFile.</span><span class="sxs-lookup"><span data-stu-id="1c3ad-156">To obtain a node file object, use the Get-AzureBatchNodeFile cmdlet.</span></span>

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

### <span data-ttu-id="1c3ad-157">-JobId</span><span class="sxs-lookup"><span data-stu-id="1c3ad-157">-JobId</span></span>
<span data-ttu-id="1c3ad-158">Określa identyfikator zadania zawierającego zadanie docelowe.</span><span class="sxs-lookup"><span data-stu-id="1c3ad-158">Specifies the ID of the job that contains the target task.</span></span>

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

### <span data-ttu-id="1c3ad-159">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1c3ad-159">-Name</span></span>
<span data-ttu-id="1c3ad-160">Określa nazwę pliku węzła, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c3ad-160">Specifies the name of the node file that this cmdlet retrieves.</span></span>
<span data-ttu-id="1c3ad-161">Nie można określać symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="1c3ad-161">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream, ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c3ad-162">-PoolId</span><span class="sxs-lookup"><span data-stu-id="1c3ad-162">-PoolId</span></span>
<span data-ttu-id="1c3ad-163">Określa identyfikator puli zawierającej węzeł obliczeniowy, który zawiera plik węzła, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c3ad-163">Specifies the ID of the pool that contains the compute node that contains the node file that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1c3ad-164">-TaskId</span><span class="sxs-lookup"><span data-stu-id="1c3ad-164">-TaskId</span></span>
<span data-ttu-id="1c3ad-165">Określa identyfikator zadania.</span><span class="sxs-lookup"><span data-stu-id="1c3ad-165">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="1c3ad-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c3ad-166">-DefaultProfile</span></span>
<span data-ttu-id="1c3ad-167">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1c3ad-167">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c3ad-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c3ad-168">CommonParameters</span></span>
<span data-ttu-id="1c3ad-169">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c3ad-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c3ad-170">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c3ad-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c3ad-171">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1c3ad-171">INPUTS</span></span>

### <span data-ttu-id="1c3ad-172">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="1c3ad-172">BatchAccountContext</span></span>
<span data-ttu-id="1c3ad-173">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="1c3ad-173">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="1c3ad-174">PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="1c3ad-174">PSNodeFile</span></span>
<span data-ttu-id="1c3ad-175">Parametr "Inputobject" przyjmuje wartość typu "PSNodeFile" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="1c3ad-175">Parameter 'InputObject' accepts value of type 'PSNodeFile' from the pipeline</span></span>

## <span data-ttu-id="1c3ad-176">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1c3ad-176">OUTPUTS</span></span>

## <span data-ttu-id="1c3ad-177">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1c3ad-177">NOTES</span></span>

## <span data-ttu-id="1c3ad-178">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1c3ad-178">RELATED LINKS</span></span>

[<span data-ttu-id="1c3ad-179">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="1c3ad-179">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="1c3ad-180">Get-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="1c3ad-180">Get-AzureBatchNodeFile</span></span>](./Get-AzureBatchNodeFile.md)

[<span data-ttu-id="1c3ad-181">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="1c3ad-181">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


