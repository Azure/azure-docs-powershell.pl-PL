---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/get-azstorageblobqueryresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobQueryResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobQueryResult.md
ms.openlocfilehash: fbb1c8e4e2a5421ea7714a0d7a82b1f1cc2567f1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062000"
---
# <span data-ttu-id="60c08-101">Get-AzStorageBlobQueryResult</span><span class="sxs-lookup"><span data-stu-id="60c08-101">Get-AzStorageBlobQueryResult</span></span>

## <span data-ttu-id="60c08-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="60c08-102">SYNOPSIS</span></span>
<span data-ttu-id="60c08-103">Stosuje prostą instrukcję SQL (Structured Query Language) do zawartości obiektu BLOB i zapisuje tylko przeszukiwany podzestaw danych w pliku lokalnym.</span><span class="sxs-lookup"><span data-stu-id="60c08-103">Applies a simple Structured Query Language (SQL) statement on a blob's contents and save only the queried subset of the data to a local file.</span></span>

## <span data-ttu-id="60c08-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="60c08-104">SYNTAX</span></span>

### <span data-ttu-id="60c08-105">NamePipeline (domyślny)</span><span class="sxs-lookup"><span data-stu-id="60c08-105">NamePipeline (Default)</span></span>
```
Get-AzStorageBlobQueryResult [-Blob] <String> [-Container] <String> [-SnapshotTime <DateTimeOffset>]
 [-VersionId <String>] -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="60c08-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="60c08-106">BlobPipeline</span></span>
```
Get-AzStorageBlobQueryResult -BlobBaseClient <BlobBaseClient> -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="60c08-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="60c08-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobQueryResult -BlobContainerClient <BlobContainerClient> [-Blob] <String>
 [-SnapshotTime <DateTimeOffset>] [-VersionId <String>] -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="60c08-108">Opis</span><span class="sxs-lookup"><span data-stu-id="60c08-108">DESCRIPTION</span></span>
<span data-ttu-id="60c08-109">Polecenie cmdlet **Get-AzStorageBlobQueryResult** stosuje prostą instrukcję SQL (Structured Query Language) do zawartości obiektu BLOB i zapisuje poszukiwany podzestaw danych w pliku lokalnym.</span><span class="sxs-lookup"><span data-stu-id="60c08-109">The **Get-AzStorageBlobQueryResult** cmdlet applies a simple Structured Query Language (SQL) statement on a blob's contents and save the queried subset of the data to a local file.</span></span>

## <span data-ttu-id="60c08-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="60c08-110">EXAMPLES</span></span>

### <span data-ttu-id="60c08-111">Przykład 1: kwerenda obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="60c08-111">Example 1: Query a blob</span></span>
```powershell
PS C:\> $inputconfig = New-AzStorageBlobQueryConfig -AsCsv -HasHeader

PS C:\> $outputconfig = New-AzStorageBlobQueryConfig -AsJson

PS C:\> $queryString = "SELECT * FROM BlobStorage WHERE Name = 'a'"

PS C:\> $result = Get-AzStorageBlobQueryResult -Container $containerName -Blob $blobName -QueryString $queryString -ResultFile "c:\resultfile.json" -InputTextConfiguration $inputconfig -OutputTextConfiguration $outputconfig -Context $ctx

PS C:\> $result

BytesScanned FailureCount BlobQueryError
------------ ------------ --------------
         449            0
```

<span data-ttu-id="60c08-112">To polecenie bada działanie obiektu BLOB succsssfully, korzystając z konfiguracji wejściowej jako pliku CSV, oraz konfiguracji wyjściowej w formacie JSON i zapisuje dane wyjściowe w pliku lokalnym "c:\resultfile.json".</span><span class="sxs-lookup"><span data-stu-id="60c08-112">This command querys a blob succsssfully with input config as csv, and output config as json, and save the output to local file "c:\resultfile.json".</span></span>

### <span data-ttu-id="60c08-113">Przykład 2: zapytanie do migawki obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="60c08-113">Example 2: Query a blob snapshot</span></span>
```powershell
PS C:\> $blob = Get-AzStorageBlob -Container $containerName -Blob $blobName -SnapshotTime "2020-07-29T11:08:21.1097874Z" -Context $ctx

PS C:\> $inputconfig = New-AzStorageBlobQueryConfig -AsCsv -ColumnSeparator "," -QuotationCharacter """" -EscapeCharacter "\" -RecordSeparator "`n" -HasHeader

PS C:\> $outputconfig = New-AzStorageBlobQueryConfig -AsJson -RecordSeparator "`n" 

PS C:\> $queryString = "SELECT * FROM BlobStorage WHERE _1 LIKE '1%%'"

PS C:\> $result = $blob | Get-AzStorageBlobQueryResult -QueryString $queryString -ResultFile $localFilePath -InputTextConfiguration $inputconfig -OutputTextConfiguration $outputconfig

PS C:\> $result

BytesScanned FailureCount BlobQueryError
------------ ------------ --------------
   187064971            1 {ParseError}  



PS C:\> $result.BlobQueryError

Name       Description                                                   IsFatal Position
----       -----------                                                   ------- --------
ParseError Unexpected token '1' at [byte: 3077737]. Expecting token ','.    True  7270632
```

<span data-ttu-id="60c08-114">To polecenie po raz pierwszy uzyskuje obiekt BLOB na potrzeby migawki obiektu BLOB, a następnie wysyła zapytanie do migawki obiektu BLOB i pokaże wynik błąd zapytania.</span><span class="sxs-lookup"><span data-stu-id="60c08-114">This command first gets a blob object for blob snapshot, then queries the blob snapshot and show the result include query error.</span></span>

## <span data-ttu-id="60c08-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="60c08-115">PARAMETERS</span></span>

### <span data-ttu-id="60c08-116">-Obiekt BLOB</span><span class="sxs-lookup"><span data-stu-id="60c08-116">-Blob</span></span>
<span data-ttu-id="60c08-117">Nazwa obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="60c08-117">Blob name</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60c08-118">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="60c08-118">-BlobBaseClient</span></span>
<span data-ttu-id="60c08-119">Obiekt BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="60c08-119">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60c08-120">-BlobContainerClient</span><span class="sxs-lookup"><span data-stu-id="60c08-120">-BlobContainerClient</span></span>
<span data-ttu-id="60c08-121">Obiekt BlobContainerClient</span><span class="sxs-lookup"><span data-stu-id="60c08-121">BlobContainerClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.BlobContainerClient
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60c08-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="60c08-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="60c08-123">Maksymalny czas wykonywania wszystkich żądań po stronie klienta (w sekundach).</span><span class="sxs-lookup"><span data-stu-id="60c08-123">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="60c08-124">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="60c08-124">-ConcurrentTaskCount</span></span>
<span data-ttu-id="60c08-125">Całkowita liczba współbieżnych zadań asynchronicznych.</span><span class="sxs-lookup"><span data-stu-id="60c08-125">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="60c08-126">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="60c08-126">The default value is 10.</span></span>

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

### <span data-ttu-id="60c08-127">-Kontener</span><span class="sxs-lookup"><span data-stu-id="60c08-127">-Container</span></span>
<span data-ttu-id="60c08-128">Nazwa kontenera</span><span class="sxs-lookup"><span data-stu-id="60c08-128">Container name</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60c08-129">-Context</span><span class="sxs-lookup"><span data-stu-id="60c08-129">-Context</span></span>
<span data-ttu-id="60c08-130">Obiekt kontekstu usługi Azure Storage</span><span class="sxs-lookup"><span data-stu-id="60c08-130">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60c08-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60c08-131">-DefaultProfile</span></span>
<span data-ttu-id="60c08-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="60c08-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60c08-133">-Force</span><span class="sxs-lookup"><span data-stu-id="60c08-133">-Force</span></span>
<span data-ttu-id="60c08-134">Wymuś zastąpienie istniejącego pliku.</span><span class="sxs-lookup"><span data-stu-id="60c08-134">Force to overwrite the existing file.</span></span>

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

### <span data-ttu-id="60c08-135">-InputTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="60c08-135">-InputTextConfiguration</span></span>
<span data-ttu-id="60c08-136">Konfiguracja używana do obsługi tekstu wejściowego zapytania.</span><span class="sxs-lookup"><span data-stu-id="60c08-136">The configuration used to handled the query input text.</span></span> <span data-ttu-id="60c08-137">Tworzenie obiektu konfiguracji z nowymi — AzStorageBlobQueryConfig.</span><span class="sxs-lookup"><span data-stu-id="60c08-137">Create configuration object the with New-AzStorageBlobQueryConfig.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60c08-138">-OutputTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="60c08-138">-OutputTextConfiguration</span></span>
<span data-ttu-id="60c08-139">Konfiguracja używana do obsługi tekstu wyjściowego kwerendy.</span><span class="sxs-lookup"><span data-stu-id="60c08-139">The configuration used to handled the query output text.</span></span> <span data-ttu-id="60c08-140">Tworzenie obiektu konfiguracji z nowymi — AzStorageBlobQueryConfig.</span><span class="sxs-lookup"><span data-stu-id="60c08-140">Create configuration object the with New-AzStorageBlobQueryConfig.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60c08-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="60c08-141">-PassThru</span></span>
<span data-ttu-id="60c08-142">Zwraca, czy pomyślnie zbadano zapytanie określonego obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="60c08-142">Return whether the specified blob is successfully queried.</span></span>

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

### <span data-ttu-id="60c08-143">-QueryString</span><span class="sxs-lookup"><span data-stu-id="60c08-143">-QueryString</span></span>
<span data-ttu-id="60c08-144">Ciąg zapytania, Zobacz więcej szczegółów w: https://docs.microsoft.com/en-us/azure/storage/blobs/query-acceleration-sql-reference</span><span class="sxs-lookup"><span data-stu-id="60c08-144">Query string, see more details in: https://docs.microsoft.com/en-us/azure/storage/blobs/query-acceleration-sql-reference</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60c08-145">-ResultFile</span><span class="sxs-lookup"><span data-stu-id="60c08-145">-ResultFile</span></span>
<span data-ttu-id="60c08-146">Lokalna ścieżka pliku służąca do zapisania wyniku zapytania.</span><span class="sxs-lookup"><span data-stu-id="60c08-146">Local file path to save the query result.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60c08-147">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="60c08-147">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="60c08-148">Upłynął limit czasu serwera dla każdego żądania (w sekundach).</span><span class="sxs-lookup"><span data-stu-id="60c08-148">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="60c08-149">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="60c08-149">-SnapshotTime</span></span>
<span data-ttu-id="60c08-150">Obiekt BLOB SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="60c08-150">Blob SnapshotTime</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60c08-151">-VersionId</span><span class="sxs-lookup"><span data-stu-id="60c08-151">-VersionId</span></span>
<span data-ttu-id="60c08-152">Obiekt BLOB VersionId</span><span class="sxs-lookup"><span data-stu-id="60c08-152">Blob VersionId</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60c08-153">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="60c08-153">-Confirm</span></span>
<span data-ttu-id="60c08-154">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60c08-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60c08-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60c08-155">-WhatIf</span></span>
<span data-ttu-id="60c08-156">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60c08-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60c08-157">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="60c08-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60c08-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60c08-158">CommonParameters</span></span>
<span data-ttu-id="60c08-159">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60c08-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60c08-160">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60c08-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60c08-161">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="60c08-161">INPUTS</span></span>

### <span data-ttu-id="60c08-162">Azure. Storage. blob. specjalizowane. BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="60c08-162">Azure.Storage.Blobs.Specialized.BlobBaseClient</span></span>

### <span data-ttu-id="60c08-163">Azure. Storage. blob. BlobContainerClient</span><span class="sxs-lookup"><span data-stu-id="60c08-163">Azure.Storage.Blobs.BlobContainerClient</span></span>

### <span data-ttu-id="60c08-164">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="60c08-164">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="60c08-165">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="60c08-165">OUTPUTS</span></span>

### <span data-ttu-id="60c08-166">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="60c08-166">System.Boolean</span></span>

## <span data-ttu-id="60c08-167">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="60c08-167">NOTES</span></span>

## <span data-ttu-id="60c08-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="60c08-168">RELATED LINKS</span></span>
