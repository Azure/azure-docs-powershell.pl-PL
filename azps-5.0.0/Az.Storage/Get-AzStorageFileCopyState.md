---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C1648DC3-8CFD-4487-A080-D9BE25DAD258
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
ms.openlocfilehash: b87c4169fb2a7d417f56051c4996cf0428ceafe7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225321"
---
# <span data-ttu-id="e1ce4-101">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="e1ce4-101">Get-AzStorageFileCopyState</span></span>

## <span data-ttu-id="e1ce4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e1ce4-102">SYNOPSIS</span></span>
<span data-ttu-id="e1ce4-103">Pobiera stan operacji kopiowania.</span><span class="sxs-lookup"><span data-stu-id="e1ce4-103">Gets the state of a copy operation.</span></span>

## <span data-ttu-id="e1ce4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e1ce4-104">SYNTAX</span></span>

### <span data-ttu-id="e1ce4-105">Nazwaudziału</span><span class="sxs-lookup"><span data-stu-id="e1ce4-105">ShareName</span></span>
```
Get-AzStorageFileCopyState [-ShareName] <String> [-FilePath] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="e1ce4-106">Plik</span><span class="sxs-lookup"><span data-stu-id="e1ce4-106">File</span></span>
```
Get-AzStorageFileCopyState [-File] <CloudFile> [-WaitForComplete] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="e1ce4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e1ce4-107">DESCRIPTION</span></span>
<span data-ttu-id="e1ce4-108">Polecenie cmdlet **Get-AzStorageFileCopyState** Pobiera stan operacji kopiowania plików w usłudze Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="e1ce4-108">The **Get-AzStorageFileCopyState** cmdlet gets the state of an Azure Storage file copy operation.</span></span>
<span data-ttu-id="e1ce4-109">Powinna być uruchamiana w docelowym pliku kopii.</span><span class="sxs-lookup"><span data-stu-id="e1ce4-109">It should run on the copy destination file.</span></span>

## <span data-ttu-id="e1ce4-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e1ce4-110">EXAMPLES</span></span>

### <span data-ttu-id="e1ce4-111">Przykład 1: pobieranie stanu kopiowania według nazwy pliku</span><span class="sxs-lookup"><span data-stu-id="e1ce4-111">Example 1: Get the copy state by file name</span></span>
```
PS C:\>Get-AzStorageFileCopyState -ShareName "ContosoShare" -FilePath "ContosoFile"
```

<span data-ttu-id="e1ce4-112">To polecenie pobiera stan operacji kopiowania pliku o określonej nazwie.</span><span class="sxs-lookup"><span data-stu-id="e1ce4-112">This command gets the state of the copy operation for a file that has the specified name.</span></span>

### <span data-ttu-id="e1ce4-113">Przykład 2: Rozpocznij kopiowanie i potok, aby uzyskać stan kopii</span><span class="sxs-lookup"><span data-stu-id="e1ce4-113">Example 2: Start Copy and pipeline to get the copy status</span></span>
```
C:\PS> $destfile = Start-AzStorageFileCopy -SrcShareName "contososhare" -SrcFilePath "contosofile" -DestShareName "contososhare2" -destfilepath "contosofile_copy"  

C:\PS> $destfile | Get-AzStorageFileCopyState
```

<span data-ttu-id="e1ce4-114">Pierwsze polecenie rozpoczyna kopiowanie pliku "contosofile" do "contosofile_copy", a następnie wyprowadza obiekt plik destiantion.</span><span class="sxs-lookup"><span data-stu-id="e1ce4-114">The first command starts copy file "contosofile" to "contosofile_copy", and output the destiantion file object.</span></span> <span data-ttu-id="e1ce4-115">Drugie polecenie przedestiantiono obiekt pliku w celu uzyskania-AzStorageFileCopyState, aby uzyskać stan kopiowania plików.</span><span class="sxs-lookup"><span data-stu-id="e1ce4-115">The second command pipeline the destiantion file object to Get-AzStorageFileCopyState, to get file copy state.</span></span>

## <span data-ttu-id="e1ce4-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e1ce4-116">PARAMETERS</span></span>

### <span data-ttu-id="e1ce4-117">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e1ce4-117">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="e1ce4-118">Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.</span><span class="sxs-lookup"><span data-stu-id="e1ce4-118">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="e1ce4-119">Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.</span><span class="sxs-lookup"><span data-stu-id="e1ce4-119">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="e1ce4-120">Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="e1ce4-120">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1ce4-121">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="e1ce4-121">-ConcurrentTaskCount</span></span>
<span data-ttu-id="e1ce4-122">Określa maksymalną liczbę współbieżnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="e1ce4-122">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="e1ce4-123">Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="e1ce4-123">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="e1ce4-124">Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.</span><span class="sxs-lookup"><span data-stu-id="e1ce4-124">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="e1ce4-125">Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.</span><span class="sxs-lookup"><span data-stu-id="e1ce4-125">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="e1ce4-126">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="e1ce4-126">The default value is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1ce4-127">-Context</span><span class="sxs-lookup"><span data-stu-id="e1ce4-127">-Context</span></span>
<span data-ttu-id="e1ce4-128">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="e1ce4-128">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="e1ce4-129">Aby uzyskać kontekst, użyj polecenia cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="e1ce4-129">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1ce4-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1ce4-130">-DefaultProfile</span></span>
<span data-ttu-id="e1ce4-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e1ce4-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1ce4-132">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="e1ce4-132">-File</span></span>
<span data-ttu-id="e1ce4-133">Określa obiekt **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="e1ce4-133">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="e1ce4-134">Możesz utworzyć plik w chmurze lub uzyskać go za pomocą polecenia cmdlet Get-AzStorageFile.</span><span class="sxs-lookup"><span data-stu-id="e1ce4-134">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1ce4-135">-FilePath</span><span class="sxs-lookup"><span data-stu-id="e1ce4-135">-FilePath</span></span>
<span data-ttu-id="e1ce4-136">Określa ścieżkę pliku względem udziału usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="e1ce4-136">Specifies the path of the file relative to an Azure Storage share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1ce4-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e1ce4-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="e1ce4-138">Określa długość limitu czasu dla części serwera żądania.</span><span class="sxs-lookup"><span data-stu-id="e1ce4-138">Specifies the length of the time-out period for the server part of a request.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1ce4-139">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="e1ce4-139">-ShareName</span></span>
<span data-ttu-id="e1ce4-140">Określa nazwę udziału.</span><span class="sxs-lookup"><span data-stu-id="e1ce4-140">Specifies the name of a share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1ce4-141">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="e1ce4-141">-WaitForComplete</span></span>
<span data-ttu-id="e1ce4-142">Wskazuje, że to polecenie cmdlet oczekuje na zakończenie kopii.</span><span class="sxs-lookup"><span data-stu-id="e1ce4-142">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="e1ce4-143">Jeśli nie podano tego parametru, to polecenie cmdlet natychmiast zwraca wynik.</span><span class="sxs-lookup"><span data-stu-id="e1ce4-143">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="e1ce4-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1ce4-144">CommonParameters</span></span>
<span data-ttu-id="e1ce4-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1ce4-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1ce4-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1ce4-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1ce4-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e1ce4-147">INPUTS</span></span>

### <span data-ttu-id="e1ce4-148">Microsoft. Azure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="e1ce4-148">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="e1ce4-149">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e1ce4-149">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e1ce4-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e1ce4-150">OUTPUTS</span></span>

### <span data-ttu-id="e1ce4-151">Microsoft. Azure. Storage. File. CopyState</span><span class="sxs-lookup"><span data-stu-id="e1ce4-151">Microsoft.Azure.Storage.File.CopyState</span></span>

## <span data-ttu-id="e1ce4-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e1ce4-152">NOTES</span></span>

## <span data-ttu-id="e1ce4-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e1ce4-153">RELATED LINKS</span></span>

[<span data-ttu-id="e1ce4-154">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="e1ce4-154">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="e1ce4-155">Nowe — AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="e1ce4-155">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="e1ce4-156">Start — AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="e1ce4-156">Start-AzStorageFileCopy</span></span>](./Start-AzStorageFileCopy.md)

[<span data-ttu-id="e1ce4-157">Zatrzymaj — AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="e1ce4-157">Stop-AzStorageFileCopy</span></span>](./Stop-AzStorageFileCopy.md)
