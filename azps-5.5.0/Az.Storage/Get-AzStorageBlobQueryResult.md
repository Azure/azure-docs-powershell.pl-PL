---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/get-azstorageblobqueryresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobQueryResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobQueryResult.md
ms.openlocfilehash: fbb1c8e4e2a5421ea7714a0d7a82b1f1cc2567f1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195811"
---
# <span data-ttu-id="0ccda-101">Get-AzStorageBlobQueryResult</span><span class="sxs-lookup"><span data-stu-id="0ccda-101">Get-AzStorageBlobQueryResult</span></span>

## <span data-ttu-id="0ccda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ccda-102">SYNOPSIS</span></span>
<span data-ttu-id="0ccda-103">Stosuje prostą instrukcję Sql (Structured Query Language) do zawartości obiektu blob i zapisuje w pliku lokalnym tylko podzbiór danych, do których został zapytany.</span><span class="sxs-lookup"><span data-stu-id="0ccda-103">Applies a simple Structured Query Language (SQL) statement on a blob's contents and save only the queried subset of the data to a local file.</span></span>

## <span data-ttu-id="0ccda-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0ccda-104">SYNTAX</span></span>

### <span data-ttu-id="0ccda-105">NamePipeline (Default)</span><span class="sxs-lookup"><span data-stu-id="0ccda-105">NamePipeline (Default)</span></span>
```
Get-AzStorageBlobQueryResult [-Blob] <String> [-Container] <String> [-SnapshotTime <DateTimeOffset>]
 [-VersionId <String>] -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0ccda-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="0ccda-106">BlobPipeline</span></span>
```
Get-AzStorageBlobQueryResult -BlobBaseClient <BlobBaseClient> -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0ccda-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="0ccda-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobQueryResult -BlobContainerClient <BlobContainerClient> [-Blob] <String>
 [-SnapshotTime <DateTimeOffset>] [-VersionId <String>] -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0ccda-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="0ccda-108">DESCRIPTION</span></span>
<span data-ttu-id="0ccda-109">Polecenie **cmdlet Get-AzStorageBlobQueryResult** powoduje zastosowanie prostej instrukcji SQL (Structured Query Language) do zawartości obiektu blob i zapisanie podzbioru danych, o który zapytano, w pliku lokalnym.</span><span class="sxs-lookup"><span data-stu-id="0ccda-109">The **Get-AzStorageBlobQueryResult** cmdlet applies a simple Structured Query Language (SQL) statement on a blob's contents and save the queried subset of the data to a local file.</span></span>

## <span data-ttu-id="0ccda-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0ccda-110">EXAMPLES</span></span>

### <span data-ttu-id="0ccda-111">Przykład 1. Kwerenda obiektu blob</span><span class="sxs-lookup"><span data-stu-id="0ccda-111">Example 1: Query a blob</span></span>
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

<span data-ttu-id="0ccda-112">To polecenie przekieruje obiekt blob pomyślnie z konfiguracją wejściowym jako plikiem csv i konfiguracją wyjściową jako json, a następnie zapisz dane wyjściowe w pliku lokalnym "c:\resultfile.jssię".</span><span class="sxs-lookup"><span data-stu-id="0ccda-112">This command querys a blob succsssfully with input config as csv, and output config as json, and save the output to local file "c:\resultfile.json".</span></span>

### <span data-ttu-id="0ccda-113">Przykład 2. Tworzenie zapytania migawki obiektu blob</span><span class="sxs-lookup"><span data-stu-id="0ccda-113">Example 2: Query a blob snapshot</span></span>
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

<span data-ttu-id="0ccda-114">To polecenie najpierw pobiera obiekt blob dla migawki obiektów blob, a następnie wysyła zapytanie migawki obiektu blob i wyświetla wynik, w tym błąd zapytania.</span><span class="sxs-lookup"><span data-stu-id="0ccda-114">This command first gets a blob object for blob snapshot, then queries the blob snapshot and show the result include query error.</span></span>

## <span data-ttu-id="0ccda-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ccda-115">PARAMETERS</span></span>

### <span data-ttu-id="0ccda-116">— obiekt blob</span><span class="sxs-lookup"><span data-stu-id="0ccda-116">-Blob</span></span>
<span data-ttu-id="0ccda-117">Nazwa obiektu blob</span><span class="sxs-lookup"><span data-stu-id="0ccda-117">Blob name</span></span>

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

### <span data-ttu-id="0ccda-118">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="0ccda-118">-BlobBaseClient</span></span>
<span data-ttu-id="0ccda-119">Obiekt BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="0ccda-119">BlobBaseClient Object</span></span>

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

### <span data-ttu-id="0ccda-120">-BlobContainerClient</span><span class="sxs-lookup"><span data-stu-id="0ccda-120">-BlobContainerClient</span></span>
<span data-ttu-id="0ccda-121">Obiekt BlobContainerClient</span><span class="sxs-lookup"><span data-stu-id="0ccda-121">BlobContainerClient Object</span></span>

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

### <span data-ttu-id="0ccda-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0ccda-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="0ccda-123">Maksymalny czas wykonywania po stronie klienta dla każdego żądania w sekundach.</span><span class="sxs-lookup"><span data-stu-id="0ccda-123">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="0ccda-124">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="0ccda-124">-ConcurrentTaskCount</span></span>
<span data-ttu-id="0ccda-125">Całkowita ilość jednoczesnych zadań synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="0ccda-125">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="0ccda-126">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="0ccda-126">The default value is 10.</span></span>

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

### <span data-ttu-id="0ccda-127">— Kontener</span><span class="sxs-lookup"><span data-stu-id="0ccda-127">-Container</span></span>
<span data-ttu-id="0ccda-128">Nazwa kontenera</span><span class="sxs-lookup"><span data-stu-id="0ccda-128">Container name</span></span>

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

### <span data-ttu-id="0ccda-129">— kontekst</span><span class="sxs-lookup"><span data-stu-id="0ccda-129">-Context</span></span>
<span data-ttu-id="0ccda-130">Obiekt kontekstowy magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="0ccda-130">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="0ccda-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ccda-131">-DefaultProfile</span></span>
<span data-ttu-id="0ccda-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0ccda-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ccda-133">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="0ccda-133">-Force</span></span>
<span data-ttu-id="0ccda-134">Wymusz zastąpienie istniejącego pliku.</span><span class="sxs-lookup"><span data-stu-id="0ccda-134">Force to overwrite the existing file.</span></span>

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

### <span data-ttu-id="0ccda-135">-InputTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="0ccda-135">-InputTextConfiguration</span></span>
<span data-ttu-id="0ccda-136">Konfiguracja używana do obsługi tekstu wejściowego zapytania.</span><span class="sxs-lookup"><span data-stu-id="0ccda-136">The configuration used to handled the query input text.</span></span> <span data-ttu-id="0ccda-137">Utwórz obiekt konfiguracji za pomocą new-azstorageBlobQueryConfig.</span><span class="sxs-lookup"><span data-stu-id="0ccda-137">Create configuration object the with New-AzStorageBlobQueryConfig.</span></span>

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

### <span data-ttu-id="0ccda-138">-OutputTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="0ccda-138">-OutputTextConfiguration</span></span>
<span data-ttu-id="0ccda-139">Konfiguracja używana do obsługi tekstu wyjściowego zapytania.</span><span class="sxs-lookup"><span data-stu-id="0ccda-139">The configuration used to handled the query output text.</span></span> <span data-ttu-id="0ccda-140">Utwórz obiekt konfiguracji za pomocą new-azstorageBlobQueryConfig.</span><span class="sxs-lookup"><span data-stu-id="0ccda-140">Create configuration object the with New-AzStorageBlobQueryConfig.</span></span>

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

### <span data-ttu-id="0ccda-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0ccda-141">-PassThru</span></span>
<span data-ttu-id="0ccda-142">Sprawdź, czy określony obiekt blob został pomyślnie zwrócony.</span><span class="sxs-lookup"><span data-stu-id="0ccda-142">Return whether the specified blob is successfully queried.</span></span>

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

### <span data-ttu-id="0ccda-143">-QueryString</span><span class="sxs-lookup"><span data-stu-id="0ccda-143">-QueryString</span></span>
<span data-ttu-id="0ccda-144">Ciąg zapytania, zobacz więcej szczegółów w: https://docs.microsoft.com/en-us/azure/storage/blobs/query-acceleration-sql-reference</span><span class="sxs-lookup"><span data-stu-id="0ccda-144">Query string, see more details in: https://docs.microsoft.com/en-us/azure/storage/blobs/query-acceleration-sql-reference</span></span>

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

### <span data-ttu-id="0ccda-145">-ResultFile</span><span class="sxs-lookup"><span data-stu-id="0ccda-145">-ResultFile</span></span>
<span data-ttu-id="0ccda-146">Lokalna ścieżka pliku do zapisania wyniku zapytania.</span><span class="sxs-lookup"><span data-stu-id="0ccda-146">Local file path to save the query result.</span></span>

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

### <span data-ttu-id="0ccda-147">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0ccda-147">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="0ccda-148">Czas poszczególnych żądań w sekundach dla serwera jest uy czasowy.</span><span class="sxs-lookup"><span data-stu-id="0ccda-148">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="0ccda-149">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="0ccda-149">-SnapshotTime</span></span>
<span data-ttu-id="0ccda-150">Migawka obiektów blob</span><span class="sxs-lookup"><span data-stu-id="0ccda-150">Blob SnapshotTime</span></span>

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

### <span data-ttu-id="0ccda-151">-VersionId</span><span class="sxs-lookup"><span data-stu-id="0ccda-151">-VersionId</span></span>
<span data-ttu-id="0ccda-152">Blob VersionId</span><span class="sxs-lookup"><span data-stu-id="0ccda-152">Blob VersionId</span></span>

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

### <span data-ttu-id="0ccda-153">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0ccda-153">-Confirm</span></span>
<span data-ttu-id="0ccda-154">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0ccda-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ccda-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ccda-155">-WhatIf</span></span>
<span data-ttu-id="0ccda-156">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ccda-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ccda-157">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0ccda-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ccda-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ccda-158">CommonParameters</span></span>
<span data-ttu-id="0ccda-159">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ccda-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ccda-160">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ccda-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ccda-161">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0ccda-161">INPUTS</span></span>

### <span data-ttu-id="0ccda-162">Azure.Storage.Blobs.Specialized.BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="0ccda-162">Azure.Storage.Blobs.Specialized.BlobBaseClient</span></span>

### <span data-ttu-id="0ccda-163">Azure.Storage.Blobs.BlobContainerClient</span><span class="sxs-lookup"><span data-stu-id="0ccda-163">Azure.Storage.Blobs.BlobContainerClient</span></span>

### <span data-ttu-id="0ccda-164">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0ccda-164">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0ccda-165">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0ccda-165">OUTPUTS</span></span>

### <span data-ttu-id="0ccda-166">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0ccda-166">System.Boolean</span></span>

## <span data-ttu-id="0ccda-167">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0ccda-167">NOTES</span></span>

## <span data-ttu-id="0ccda-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0ccda-168">RELATED LINKS</span></span>
