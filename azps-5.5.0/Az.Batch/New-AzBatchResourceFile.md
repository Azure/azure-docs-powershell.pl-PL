---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchresourcefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
ms.openlocfilehash: 43cbf86ca473b6984ee2190b1d10df61b6d32e64
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239250"
---
# <span data-ttu-id="12c27-101">New-AzBatchResourceFile</span><span class="sxs-lookup"><span data-stu-id="12c27-101">New-AzBatchResourceFile</span></span>

## <span data-ttu-id="12c27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12c27-102">SYNOPSIS</span></span>
<span data-ttu-id="12c27-103">Tworzy plik zasobu do użycia `New-AzBatchTask` według.</span><span class="sxs-lookup"><span data-stu-id="12c27-103">Creates a Resource File for usage by `New-AzBatchTask`.</span></span>

## <span data-ttu-id="12c27-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="12c27-104">SYNTAX</span></span>

### <span data-ttu-id="12c27-105">HttpUrl (domyślne)</span><span class="sxs-lookup"><span data-stu-id="12c27-105">HttpUrl (Default)</span></span>
```
New-AzBatchResourceFile -HttpUrl <String> -FilePath <String> [-FileMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12c27-106">StorageContainerUrl</span><span class="sxs-lookup"><span data-stu-id="12c27-106">StorageContainerUrl</span></span>
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] [-BlobPrefix <String>]
 -StorageContainerUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12c27-107">AutoStorageContainerName</span><span class="sxs-lookup"><span data-stu-id="12c27-107">AutoStorageContainerName</span></span>
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] -AutoStorageContainerName <String>
 [-BlobPrefix <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12c27-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="12c27-108">DESCRIPTION</span></span>
<span data-ttu-id="12c27-109">Tworzy plik zasobu do użycia `New-AzBatchTask` według.</span><span class="sxs-lookup"><span data-stu-id="12c27-109">Creates a Resource File for usage by `New-AzBatchTask`.</span></span>

## <span data-ttu-id="12c27-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="12c27-110">EXAMPLES</span></span>

### <span data-ttu-id="12c27-111">Przykład 1. Tworzenie pliku zasobu za pomocą adresu URL HTTP, który wskaże pojedynczy plik</span><span class="sxs-lookup"><span data-stu-id="12c27-111">Example 1: Create a resource file from an HTTP URL pointing at a single file</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -HttpUrl "https://testacct.blob.core.windows.net/" -FilePath "file1"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="12c27-112">Tworzy odwołanie `PSResourceFile` do adresu URL HTTP.</span><span class="sxs-lookup"><span data-stu-id="12c27-112">Creates a `PSResourceFile` referencing an HTTP url.</span></span>

### <span data-ttu-id="12c27-113">Przykład 2. Tworzenie pliku zasobu z adresu URL kontenera magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="12c27-113">Example 2: Create a resource file from an Azure Storage container URL</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -StorageContainerUrl "https://testacct.blob.core.windows.net/mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="12c27-114">Tworzy odwołanie `PSResourceFile` do adresu URL kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="12c27-114">Creates a `PSResourceFile` referencing an Azure Storage container URL.</span></span> <span data-ttu-id="12c27-115">Wszystkie pliki w kontenerze zostaną pobrane do określonego folderu.</span><span class="sxs-lookup"><span data-stu-id="12c27-115">All files in the container will be downloaded to the specified folder.</span></span>

### <span data-ttu-id="12c27-116">Przykład 3. Tworzenie pliku zasobu z nazwy kontenera autowy magazynowania</span><span class="sxs-lookup"><span data-stu-id="12c27-116">Example 3: Create a resource file from an Auto Storage container name</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -AutoStorageContainerName "mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="12c27-117">Tworzy odwołanie `PSResourceFile` do nazwy kontenera autowy magazynowania.</span><span class="sxs-lookup"><span data-stu-id="12c27-117">Creates a `PSResourceFile` referencing an Auto Storage container name.</span></span> <span data-ttu-id="12c27-118">Wszystkie pliki w kontenerze zostaną pobrane do określonego folderu.</span><span class="sxs-lookup"><span data-stu-id="12c27-118">All files in the container will be downloaded to the specified folder.</span></span>

## <span data-ttu-id="12c27-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12c27-119">PARAMETERS</span></span>

### <span data-ttu-id="12c27-120">-AutoStorageContainerName</span><span class="sxs-lookup"><span data-stu-id="12c27-120">-AutoStorageContainerName</span></span>
<span data-ttu-id="12c27-121">Nazwa kontenera magazynu na koncie automatycznego magazynu.</span><span class="sxs-lookup"><span data-stu-id="12c27-121">The storage container name in the auto storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: AutoStorageContainerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c27-122">-BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="12c27-122">-BlobPrefix</span></span>
<span data-ttu-id="12c27-123">Pobiera prefiks obiektu blob do użycia podczas pobierania obiektów blob z kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="12c27-123">Gets the blob prefix to use when downloading blobs from an Azure Storage container.</span></span>
<span data-ttu-id="12c27-124">Zostaną pobrane tylko obiekty blob, których nazwy zaczynają się od określonego prefiksu.</span><span class="sxs-lookup"><span data-stu-id="12c27-124">Only the blobs whose names begin with the specified prefix will be downloaded.</span></span>
<span data-ttu-id="12c27-125">Ten prefiks może być częściową nazwą pliku lub podkategoriam.</span><span class="sxs-lookup"><span data-stu-id="12c27-125">This prefix can be a partial filename or a subdirectory.</span></span>
<span data-ttu-id="12c27-126">Jeśli nie określono prefiksu, zostaną pobrane wszystkie pliki w kontenerze.</span><span class="sxs-lookup"><span data-stu-id="12c27-126">If a prefix is not specified, all the files in the container will be downloaded.</span></span>

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl, AutoStorageContainerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c27-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12c27-127">-DefaultProfile</span></span>
<span data-ttu-id="12c27-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="12c27-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12c27-129">-FileMode</span><span class="sxs-lookup"><span data-stu-id="12c27-129">-FileMode</span></span>
<span data-ttu-id="12c27-130">Pobiera atrybut trybu uprawnień pliku w formacie ósemkowym.</span><span class="sxs-lookup"><span data-stu-id="12c27-130">Gets the file permission mode attribute in octal format.</span></span>
<span data-ttu-id="12c27-131">Ta właściwość ma zastosowanie tylko wtedy, gdy plik zasobu zostanie pobrany do węzła systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="12c27-131">This property is applicable only if the resource file is downloaded to a Linux node.</span></span>
<span data-ttu-id="12c27-132">Jeśli ta właściwość nie jest określona dla węzła systemu Linux, wartość domyślna to 0770.</span><span class="sxs-lookup"><span data-stu-id="12c27-132">If this property is not specified for a Linux node, then the default value is 0770.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c27-133">- FilePath</span><span class="sxs-lookup"><span data-stu-id="12c27-133">-FilePath</span></span>
<span data-ttu-id="12c27-134">Lokalizacja w węźle obliczeniowym, do której należy pobrać pliki, względem katalogu roboczego zadania.</span><span class="sxs-lookup"><span data-stu-id="12c27-134">The location on the compute node to which to download the file(s), relative to the task's working directory.</span></span> <span data-ttu-id="12c27-135">Jeśli parametr HttpUrl jest określony, wymagany jest program FilePath i opisuje ścieżkę, do której zostanie pobrany plik, wraz z nazwą pliku.</span><span class="sxs-lookup"><span data-stu-id="12c27-135">If the HttpUrl parameter is specified, the FilePath is required and describes the path which the file will be downloaded to, including the filename.</span></span> <span data-ttu-id="12c27-136">W przeciwnym razie, jeśli określono parametry AutoStorageContainerName lub StorageContainerUrl, program FilePath jest opcjonalny i jest katalogiem do pobierania plików.</span><span class="sxs-lookup"><span data-stu-id="12c27-136">Otherwise, if the AutoStorageContainerName or StorageContainerUrl parameters are specified, FilePath is optional and is the directory to download the files to.</span></span> <span data-ttu-id="12c27-137">W przypadku użycia programu FilePath jako katalogu każda struktura katalogu już skojarzona z danymi wejściowymi zostanie zachowana w pełni i dołączona do określonego katalogu FilePath.</span><span class="sxs-lookup"><span data-stu-id="12c27-137">In the case where FilePath is used as a directory, any directory structure already associated with the input data will be retained in full and appended to the specified FilePath directory.</span></span> <span data-ttu-id="12c27-138">Określona ścieżka względna nie może wychodzić z katalogu roboczego zadania (na przykład za pomocą ".").</span><span class="sxs-lookup"><span data-stu-id="12c27-138">The specified relative path cannot break out of the task's working directory (for example by using '..').</span></span>

```yaml
Type: System.String
Parameter Sets: HttpUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl, AutoStorageContainerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c27-139">- HttpUrl</span><span class="sxs-lookup"><span data-stu-id="12c27-139">-HttpUrl</span></span>
<span data-ttu-id="12c27-140">Adres URL pliku do pobrania.</span><span class="sxs-lookup"><span data-stu-id="12c27-140">The URL of the file to download.</span></span>
<span data-ttu-id="12c27-141">Jeśli adres URL to magazyn obiektów blob platformy Azure, musi być czytelny przy użyciu dostępu anonimowego; oznacza to, że usługa wsadowa nie prezentuje żadnych poświadczeń podczas pobierania obiektu blob.</span><span class="sxs-lookup"><span data-stu-id="12c27-141">If the URL is Azure Blob Storage, it must be readable using anonymous access; that is, the Batch service does not present any credentials when downloading the blob.</span></span>
<span data-ttu-id="12c27-142">Istnieją dwa sposoby uzyskiwania takiego adresu URL dla obiektu blob w magazynie platformy Azure: obejmują podpis dostępu udostępnionego (SAS, Shared Access Signature), który udziela uprawnień do odczytu obiektu blob, lub ustaw wartość ACL dla obiektu blob lub jego kontenera, aby zezwolić na dostęp publiczny.</span><span class="sxs-lookup"><span data-stu-id="12c27-142">There are two ways to get such a URL for a blob in Azure storage: include a Shared Access Signature (SAS) granting read permissions on the blob, or set the ACL for the blob or its container to allow public access.</span></span>

```yaml
Type: System.String
Parameter Sets: HttpUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c27-143">- StorageContainerUrl</span><span class="sxs-lookup"><span data-stu-id="12c27-143">-StorageContainerUrl</span></span>
<span data-ttu-id="12c27-144">Adres URL kontenera obiektów blob w magazynie obiektów blob platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="12c27-144">The URL of the blob container within Azure Blob Storage.</span></span>
<span data-ttu-id="12c27-145">Ten adres URL musi być czytelny i dostępny do listy przy użyciu dostępu anonimowego; oznacza to, że usługa wsadowa nie prezentuje żadnych poświadczeń podczas pobierania obiektów blob z kontenera.</span><span class="sxs-lookup"><span data-stu-id="12c27-145">This URL must be readable and listable using anonymous access; that is, the Batch service does not present any credentials when downloading blobs from the container.</span></span>
<span data-ttu-id="12c27-146">Istnieją dwa sposoby uzyskiwania takiego adresu URL dla kontenera w magazynie platformy Azure: obejmują podpis dostępu udostępnionego (SAS, Shared Access Signature) udzielanie uprawnień do odczytu kontenera lub ustawienie listy ACL dla kontenera, aby zezwolić na dostęp publiczny.</span><span class="sxs-lookup"><span data-stu-id="12c27-146">There are two ways to get such a URL for a container in Azure storage: include a Shared Access Signature (SAS) granting read permissions on the container, or set the ACL for the container to allow public access.</span></span>

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c27-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12c27-147">CommonParameters</span></span>
<span data-ttu-id="12c27-148">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12c27-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12c27-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="12c27-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12c27-150">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="12c27-150">INPUTS</span></span>

### <span data-ttu-id="12c27-151">Brak</span><span class="sxs-lookup"><span data-stu-id="12c27-151">None</span></span>

## <span data-ttu-id="12c27-152">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="12c27-152">OUTPUTS</span></span>

### <span data-ttu-id="12c27-153">Microsoft.Azure.Commands.Batch. Models.PSResourceFile</span><span class="sxs-lookup"><span data-stu-id="12c27-153">Microsoft.Azure.Commands.Batch.Models.PSResourceFile</span></span>

## <span data-ttu-id="12c27-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="12c27-154">NOTES</span></span>

## <span data-ttu-id="12c27-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="12c27-155">RELATED LINKS</span></span>

[<span data-ttu-id="12c27-156">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="12c27-156">New-AzBatchTask</span></span>](./New-AzBatchTask.md)