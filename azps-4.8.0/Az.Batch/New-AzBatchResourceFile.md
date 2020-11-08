---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchresourcefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
ms.openlocfilehash: 43cbf86ca473b6984ee2190b1d10df61b6d32e64
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221566"
---
# <span data-ttu-id="bfdb9-101">New-AzBatchResourceFile</span><span class="sxs-lookup"><span data-stu-id="bfdb9-101">New-AzBatchResourceFile</span></span>

## <span data-ttu-id="bfdb9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bfdb9-102">SYNOPSIS</span></span>
<span data-ttu-id="bfdb9-103">Tworzy plik zasobów do użycia przez `New-AzBatchTask` .</span><span class="sxs-lookup"><span data-stu-id="bfdb9-103">Creates a Resource File for usage by `New-AzBatchTask`.</span></span>

## <span data-ttu-id="bfdb9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bfdb9-104">SYNTAX</span></span>

### <span data-ttu-id="bfdb9-105">HttpUrl (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bfdb9-105">HttpUrl (Default)</span></span>
```
New-AzBatchResourceFile -HttpUrl <String> -FilePath <String> [-FileMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bfdb9-106">StorageContainerUrl</span><span class="sxs-lookup"><span data-stu-id="bfdb9-106">StorageContainerUrl</span></span>
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] [-BlobPrefix <String>]
 -StorageContainerUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bfdb9-107">AutoStorageContainerName</span><span class="sxs-lookup"><span data-stu-id="bfdb9-107">AutoStorageContainerName</span></span>
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] -AutoStorageContainerName <String>
 [-BlobPrefix <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bfdb9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="bfdb9-108">DESCRIPTION</span></span>
<span data-ttu-id="bfdb9-109">Tworzy plik zasobów do użycia przez `New-AzBatchTask` .</span><span class="sxs-lookup"><span data-stu-id="bfdb9-109">Creates a Resource File for usage by `New-AzBatchTask`.</span></span>

## <span data-ttu-id="bfdb9-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bfdb9-110">EXAMPLES</span></span>

### <span data-ttu-id="bfdb9-111">Przykład 1. Tworzenie pliku zasobów na podstawie adresu URL HTTP wskazującego jeden plik</span><span class="sxs-lookup"><span data-stu-id="bfdb9-111">Example 1: Create a resource file from an HTTP URL pointing at a single file</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -HttpUrl "https://testacct.blob.core.windows.net/" -FilePath "file1"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="bfdb9-112">Tworzy `PSResourceFile` odwołanie do adresu URL http.</span><span class="sxs-lookup"><span data-stu-id="bfdb9-112">Creates a `PSResourceFile` referencing an HTTP url.</span></span>

### <span data-ttu-id="bfdb9-113">Przykład 2: Tworzenie pliku zasobów na podstawie adresu URL kontenera magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="bfdb9-113">Example 2: Create a resource file from an Azure Storage container URL</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -StorageContainerUrl "https://testacct.blob.core.windows.net/mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="bfdb9-114">Tworzy `PSResourceFile` odwołanie do adresu URL kontenera usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="bfdb9-114">Creates a `PSResourceFile` referencing an Azure Storage container URL.</span></span> <span data-ttu-id="bfdb9-115">Wszystkie pliki w kontenerze zostaną pobrane do określonego folderu.</span><span class="sxs-lookup"><span data-stu-id="bfdb9-115">All files in the container will be downloaded to the specified folder.</span></span>

### <span data-ttu-id="bfdb9-116">Przykład 3: Tworzenie pliku zasobów na podstawie nazwy kontenera automatycznego przechowywania</span><span class="sxs-lookup"><span data-stu-id="bfdb9-116">Example 3: Create a resource file from an Auto Storage container name</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -AutoStorageContainerName "mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="bfdb9-117">Tworzy `PSResourceFile` odwołanie do nazwy kontenera automatycznego przechowywania.</span><span class="sxs-lookup"><span data-stu-id="bfdb9-117">Creates a `PSResourceFile` referencing an Auto Storage container name.</span></span> <span data-ttu-id="bfdb9-118">Wszystkie pliki w kontenerze zostaną pobrane do określonego folderu.</span><span class="sxs-lookup"><span data-stu-id="bfdb9-118">All files in the container will be downloaded to the specified folder.</span></span>

## <span data-ttu-id="bfdb9-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bfdb9-119">PARAMETERS</span></span>

### <span data-ttu-id="bfdb9-120">-AutoStorageContainerName</span><span class="sxs-lookup"><span data-stu-id="bfdb9-120">-AutoStorageContainerName</span></span>
<span data-ttu-id="bfdb9-121">Nazwa kontenera magazynu na koncie Auto-pamięci.</span><span class="sxs-lookup"><span data-stu-id="bfdb9-121">The storage container name in the auto storage account.</span></span>

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

### <span data-ttu-id="bfdb9-122">-BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="bfdb9-122">-BlobPrefix</span></span>
<span data-ttu-id="bfdb9-123">Pobiera prefiks obiektu BLOB, który ma być używany podczas pobierania plików BLOB z kontenera magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bfdb9-123">Gets the blob prefix to use when downloading blobs from an Azure Storage container.</span></span>
<span data-ttu-id="bfdb9-124">Zostaną pobrane tylko te obiekty blob, których nazwy zaczynają się od określonego prefiksu.</span><span class="sxs-lookup"><span data-stu-id="bfdb9-124">Only the blobs whose names begin with the specified prefix will be downloaded.</span></span>
<span data-ttu-id="bfdb9-125">Ten prefiks może być częściową nazwą pliku lub podkatalogiem.</span><span class="sxs-lookup"><span data-stu-id="bfdb9-125">This prefix can be a partial filename or a subdirectory.</span></span>
<span data-ttu-id="bfdb9-126">Jeśli nie podano prefiksu, wszystkie pliki w kontenerze zostaną pobrane.</span><span class="sxs-lookup"><span data-stu-id="bfdb9-126">If a prefix is not specified, all the files in the container will be downloaded.</span></span>

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

### <span data-ttu-id="bfdb9-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfdb9-127">-DefaultProfile</span></span>
<span data-ttu-id="bfdb9-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bfdb9-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfdb9-129">-FileMode</span><span class="sxs-lookup"><span data-stu-id="bfdb9-129">-FileMode</span></span>
<span data-ttu-id="bfdb9-130">Pobiera atrybut tryb uprawnień do pliku w formacie ósemkowym.</span><span class="sxs-lookup"><span data-stu-id="bfdb9-130">Gets the file permission mode attribute in octal format.</span></span>
<span data-ttu-id="bfdb9-131">Ta właściwość jest dostępna tylko w przypadku pobrania pliku zasobu do węzła Linux.</span><span class="sxs-lookup"><span data-stu-id="bfdb9-131">This property is applicable only if the resource file is downloaded to a Linux node.</span></span>
<span data-ttu-id="bfdb9-132">Jeśli ta właściwość nie jest określona dla węzła Linux, wartość domyślna to 0770.</span><span class="sxs-lookup"><span data-stu-id="bfdb9-132">If this property is not specified for a Linux node, then the default value is 0770.</span></span>

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

### <span data-ttu-id="bfdb9-133">-FilePath</span><span class="sxs-lookup"><span data-stu-id="bfdb9-133">-FilePath</span></span>
<span data-ttu-id="bfdb9-134">Lokalizacja w węźle obliczeniowym, do której mają zostać pobrane pliki, względem katalogu roboczego zadania.</span><span class="sxs-lookup"><span data-stu-id="bfdb9-134">The location on the compute node to which to download the file(s), relative to the task's working directory.</span></span> <span data-ttu-id="bfdb9-135">Jeśli parametr HttpUrl jest określony, ścieżka FilePath jest wymagana i zawiera opis ścieżki, do której plik będzie pobierany, łącznie z nazwą pliku.</span><span class="sxs-lookup"><span data-stu-id="bfdb9-135">If the HttpUrl parameter is specified, the FilePath is required and describes the path which the file will be downloaded to, including the filename.</span></span> <span data-ttu-id="bfdb9-136">W przeciwnym razie, jeśli określono parametry AutoStorageContainerName lub StorageContainerUrl, ścieżka FilePath jest opcjonalna i katalog, do którego mają zostać pobrane pliki.</span><span class="sxs-lookup"><span data-stu-id="bfdb9-136">Otherwise, if the AutoStorageContainerName or StorageContainerUrl parameters are specified, FilePath is optional and is the directory to download the files to.</span></span> <span data-ttu-id="bfdb9-137">W przypadku, gdy ścieżka FilePath jest używana jako katalog, każda struktura katalogów już skojarzona z danymi wejściowymi zostanie zachowana w całości i dołączona do określonego katalogu FilePath.</span><span class="sxs-lookup"><span data-stu-id="bfdb9-137">In the case where FilePath is used as a directory, any directory structure already associated with the input data will be retained in full and appended to the specified FilePath directory.</span></span> <span data-ttu-id="bfdb9-138">Określona ścieżka względna nie może być rozdzielona w katalogu roboczym zadania (na przykład przy użyciu '.. ').</span><span class="sxs-lookup"><span data-stu-id="bfdb9-138">The specified relative path cannot break out of the task's working directory (for example by using '..').</span></span>

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

### <span data-ttu-id="bfdb9-139">-HttpUrl</span><span class="sxs-lookup"><span data-stu-id="bfdb9-139">-HttpUrl</span></span>
<span data-ttu-id="bfdb9-140">Adres URL pliku, który ma zostać pobrany.</span><span class="sxs-lookup"><span data-stu-id="bfdb9-140">The URL of the file to download.</span></span>
<span data-ttu-id="bfdb9-141">Jeśli adres URL to usługa Azure Blob Storage, należy ją odczytać za pomocą anonimowego dostępu; oznacza to, że podczas pobierania obiektu BLOB usługa przetwarzania wsadowego nie przedstawia żadnych poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="bfdb9-141">If the URL is Azure Blob Storage, it must be readable using anonymous access; that is, the Batch service does not present any credentials when downloading the blob.</span></span>
<span data-ttu-id="bfdb9-142">Istnieją dwa sposoby uzyskiwania takiego adresu URL dla obiektu BLOB w usłudze Azure Storage: dołączanie do obiektu BLOB uprawnień do odczytu (udostępnionego podpisu dostępu) lub ustawianie listy ACL dla obiektu BLOB lub jego kontenera w celu umożliwienia dostępu publicznego.</span><span class="sxs-lookup"><span data-stu-id="bfdb9-142">There are two ways to get such a URL for a blob in Azure storage: include a Shared Access Signature (SAS) granting read permissions on the blob, or set the ACL for the blob or its container to allow public access.</span></span>

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

### <span data-ttu-id="bfdb9-143">-StorageContainerUrl</span><span class="sxs-lookup"><span data-stu-id="bfdb9-143">-StorageContainerUrl</span></span>
<span data-ttu-id="bfdb9-144">Adres URL kontenera obiektu BLOB w magazynie obiektów blob platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bfdb9-144">The URL of the blob container within Azure Blob Storage.</span></span>
<span data-ttu-id="bfdb9-145">Ten adres URL musi być możliwy do odczytania i może być listowy za pomocą anonimowego dostępu; oznacza to, że usługa przetwarzania wsadowego nie przedstawia żadnych poświadczeń podczas pobierania plików BLOB z kontenera.</span><span class="sxs-lookup"><span data-stu-id="bfdb9-145">This URL must be readable and listable using anonymous access; that is, the Batch service does not present any credentials when downloading blobs from the container.</span></span>
<span data-ttu-id="bfdb9-146">Istnieją dwa sposoby uzyskiwania takiego adresu URL kontenera w usłudze Azure Storage: dołączanie do tego kontenera uprawnień dostępu współużytkowanego (SAS) lub ustawianie listy ACL kontenera, aby umożliwić dostęp publiczny.</span><span class="sxs-lookup"><span data-stu-id="bfdb9-146">There are two ways to get such a URL for a container in Azure storage: include a Shared Access Signature (SAS) granting read permissions on the container, or set the ACL for the container to allow public access.</span></span>

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

### <span data-ttu-id="bfdb9-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfdb9-147">CommonParameters</span></span>
<span data-ttu-id="bfdb9-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfdb9-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfdb9-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bfdb9-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfdb9-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bfdb9-150">INPUTS</span></span>

### <span data-ttu-id="bfdb9-151">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="bfdb9-151">None</span></span>

## <span data-ttu-id="bfdb9-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bfdb9-152">OUTPUTS</span></span>

### <span data-ttu-id="bfdb9-153">Microsoft.Azure.Commands.Batch. Modele. PSResourceFile</span><span class="sxs-lookup"><span data-stu-id="bfdb9-153">Microsoft.Azure.Commands.Batch.Models.PSResourceFile</span></span>

## <span data-ttu-id="bfdb9-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bfdb9-154">NOTES</span></span>

## <span data-ttu-id="bfdb9-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bfdb9-155">RELATED LINKS</span></span>

[<span data-ttu-id="bfdb9-156">Nowe — AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="bfdb9-156">New-AzBatchTask</span></span>](./New-AzBatchTask.md)