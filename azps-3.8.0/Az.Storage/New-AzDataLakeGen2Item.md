---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzDataLakeGen2Item.md
ms.openlocfilehash: 26f3dbc3462688458647e2e9676916063ffa3586
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052120"
---
# <span data-ttu-id="eb8df-101">New-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="eb8df-101">New-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="eb8df-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eb8df-102">SYNOPSIS</span></span>
<span data-ttu-id="eb8df-103">Tworzenie pliku lub katalogu w systemie plików.</span><span class="sxs-lookup"><span data-stu-id="eb8df-103">Create a file or directory in a filesystem.</span></span>

## <span data-ttu-id="eb8df-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eb8df-104">SYNTAX</span></span>

### <span data-ttu-id="eb8df-105">Plik (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="eb8df-105">File (Default)</span></span>
```
New-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> -Source <String> [-Umask <String>]
 [-Permission <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb8df-106">Directory</span><span class="sxs-lookup"><span data-stu-id="eb8df-106">Directory</span></span>
```
New-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> [-Directory] [-Umask <String>]
 [-Permission <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb8df-107">Opis</span><span class="sxs-lookup"><span data-stu-id="eb8df-107">DESCRIPTION</span></span>
<span data-ttu-id="eb8df-108">Polecenie cmdlet **New-AzDataLakeGen2Item** tworzy plik lub katalog w systemie plików na koncie usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="eb8df-108">The **New-AzDataLakeGen2Item** cmdlet creates a file or directory in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="eb8df-109">To polecenie cmdlet działa tylko wtedy, gdy dla konta magazynu jest włączone hierarchiczne obszary nazw.</span><span class="sxs-lookup"><span data-stu-id="eb8df-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="eb8df-110">Ten rodzaj konta można utworzyć, uruchamiając polecenie cmdlet "New-AzStorageAccount" z opcją "-EnableHierarchicalNamespace $true".</span><span class="sxs-lookup"><span data-stu-id="eb8df-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="eb8df-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eb8df-111">EXAMPLES</span></span>

### <span data-ttu-id="eb8df-112">Przykład 1. Tworzenie katalogu z określonymi uprawnieniami, umask, właściwościami i metadanymi</span><span class="sxs-lookup"><span data-stu-id="eb8df-112">Example 1: Create a directory with specified permission, Umask, properties, and metadata</span></span>
```
PS C:\>New-AzDataLakeGen2Item -FileSystem "testfilesystem" -Path "dir1/dir2/" -Directory -Permission rwxrwxrwx -Umask ---rw---- -Property @{"CacheControl" = "READ"; "ContentDisposition" = "True"} -Metadata  @{"tag1" = "value1"; "tag2" = "value2" }

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir2            True                         2020-03-23 09:15:56Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="eb8df-113">To polecenie tworzy katalog z określonymi uprawnieniami, umask, właściwościami i metadanymi.</span><span class="sxs-lookup"><span data-stu-id="eb8df-113">This command creates a directory with specified Permission, Umask, properties, and metadata</span></span>

### <span data-ttu-id="eb8df-114">Przykład 2: Tworzenie (przekazywanie) pliku Data Lake z lokalnego pliku źródłowego, a polecenie cmdlet działa w tle</span><span class="sxs-lookup"><span data-stu-id="eb8df-114">Example 2: Create(upload) a data lake file from a local source file, and the cmdlet runs in background</span></span>
```
PS C:\> $task = New-AzDataLakeGen2Item  -FileSystem "testfilesystem" -Path "dir1/dir2/file1" -Source "c:\sourcefile.txt" -Force -asjob
PS C:\> $task | Wait-Job
PS C:\> $task.Output

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group                
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir2/file1      False        14400000        2020-03-23 09:19:13Z rw-r-----    $superuser           $superuser
```

<span data-ttu-id="eb8df-115">To polecenie tworzy (przekazuje) plik Data Lake z lokalnego pliku źródłowego, a polecenie cmdlet jest uruchamiane w tle.</span><span class="sxs-lookup"><span data-stu-id="eb8df-115">This command creates(upload) a data lake file from a local source file, and the cmdlet runs in background.</span></span>

## <span data-ttu-id="eb8df-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eb8df-116">PARAMETERS</span></span>

### <span data-ttu-id="eb8df-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eb8df-117">-AsJob</span></span>
<span data-ttu-id="eb8df-118">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="eb8df-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eb8df-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="eb8df-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="eb8df-120">Całkowita liczba współbieżnych zadań asynchronicznych.</span><span class="sxs-lookup"><span data-stu-id="eb8df-120">The total amount of concurrent async tasks.</span></span> <span data-ttu-id="eb8df-121">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="eb8df-121">The default value is 10.</span></span>

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

### <span data-ttu-id="eb8df-122">-Context</span><span class="sxs-lookup"><span data-stu-id="eb8df-122">-Context</span></span>
<span data-ttu-id="eb8df-123">Obiekt kontekstu usługi Azure Storage</span><span class="sxs-lookup"><span data-stu-id="eb8df-123">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="eb8df-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb8df-124">-DefaultProfile</span></span>
<span data-ttu-id="eb8df-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="eb8df-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb8df-126">-Directory</span><span class="sxs-lookup"><span data-stu-id="eb8df-126">-Directory</span></span>
<span data-ttu-id="eb8df-127">Wskazuje, że nowy element jest katalogiem, a nie plikiem.</span><span class="sxs-lookup"><span data-stu-id="eb8df-127">Indicates that this new item is a directory and not a file.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Directory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb8df-128">— System plików</span><span class="sxs-lookup"><span data-stu-id="eb8df-128">-FileSystem</span></span>
<span data-ttu-id="eb8df-129">Nazwa systemu plików</span><span class="sxs-lookup"><span data-stu-id="eb8df-129">FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb8df-130">-Force</span><span class="sxs-lookup"><span data-stu-id="eb8df-130">-Force</span></span>
<span data-ttu-id="eb8df-131">Jeśli przekazano, zostanie utworzony nowy element bez żadnego monitu</span><span class="sxs-lookup"><span data-stu-id="eb8df-131">If passed then new item is created without any prompt</span></span>

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

### <span data-ttu-id="eb8df-132">-Metadata</span><span class="sxs-lookup"><span data-stu-id="eb8df-132">-Metadata</span></span>
<span data-ttu-id="eb8df-133">Określa metadane dla utworzonego katalogu lub pliku.</span><span class="sxs-lookup"><span data-stu-id="eb8df-133">Specifies metadata for the created directory or file.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb8df-134">-Path</span><span class="sxs-lookup"><span data-stu-id="eb8df-134">-Path</span></span>
<span data-ttu-id="eb8df-135">Ścieżka w określonym systemie plików, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="eb8df-135">The path in the specified Filesystem that should be create.</span></span>
<span data-ttu-id="eb8df-136">Może to być plik lub katalog w formacie "Directory/file.txt" lub "directory1/Directory2/"</span><span class="sxs-lookup"><span data-stu-id="eb8df-136">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb8df-137">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="eb8df-137">-Permission</span></span>
<span data-ttu-id="eb8df-138">Umożliwia ustawianie uprawnień dostępu do POSIX dla właściciela pliku, grupy będącej właścicielem i innych.</span><span class="sxs-lookup"><span data-stu-id="eb8df-138">Sets POSIX access permissions for the file owner, the file owning group, and others.</span></span>
<span data-ttu-id="eb8df-139">Każdej klasie można udzielić uprawnień Odczyt, zapis lub wykonywanie.</span><span class="sxs-lookup"><span data-stu-id="eb8df-139">Each class may be granted read, write, or execute permission.</span></span>
<span data-ttu-id="eb8df-140">Obsługa symboliczna (rwxrw-RW-).</span><span class="sxs-lookup"><span data-stu-id="eb8df-140">Symbolic (rwxrw-rw-) is supported.</span></span>

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

### <span data-ttu-id="eb8df-141">-Property</span><span class="sxs-lookup"><span data-stu-id="eb8df-141">-Property</span></span>
<span data-ttu-id="eb8df-142">Określa właściwości utworzonego katalogu lub pliku.</span><span class="sxs-lookup"><span data-stu-id="eb8df-142">Specifies properties for the created directory or file.</span></span> <span data-ttu-id="eb8df-143">Obsługiwane właściwości pliku to: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="eb8df-143">The supported properties for file are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>
<span data-ttu-id="eb8df-144">Obsługiwane właściwości katalogu to: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span><span class="sxs-lookup"><span data-stu-id="eb8df-144">The supported properties for directory are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb8df-145">-Source</span><span class="sxs-lookup"><span data-stu-id="eb8df-145">-Source</span></span>
<span data-ttu-id="eb8df-146">Określ ścieżkę lokalnego pliku źródłowego, który zostanie przekazany do pliku datalake Gen2.</span><span class="sxs-lookup"><span data-stu-id="eb8df-146">Specify the local source file path which will be upload to a Datalake Gen2 file.</span></span>

```yaml
Type: System.String
Parameter Sets: File
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb8df-147">-Umask</span><span class="sxs-lookup"><span data-stu-id="eb8df-147">-Umask</span></span>
<span data-ttu-id="eb8df-148">Podczas tworzenia nowego elementu, a katalog nadrzędny nie ma domyślnej listy ACL, umask ogranicza uprawnienia do tworzenia plików lub katalogów.</span><span class="sxs-lookup"><span data-stu-id="eb8df-148">When creating New Item and the parent directory does not have a default ACL, the umask restricts the permissions of the file or directory to be created.</span></span>
<span data-ttu-id="eb8df-149">Wynikowa zgoda jest udzielana przez p & ^ u, gdzie p jest uprawnieniem, a użytkownik jest umask.</span><span class="sxs-lookup"><span data-stu-id="eb8df-149">The resulting permission is given by p & ^u, where p is the permission and u is the umask.</span></span>
<span data-ttu-id="eb8df-150">Obsługa symboliczna (rwxrw-RW-).</span><span class="sxs-lookup"><span data-stu-id="eb8df-150">Symbolic (rwxrw-rw-) is supported.</span></span>

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

### <span data-ttu-id="eb8df-151">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="eb8df-151">-Confirm</span></span>
<span data-ttu-id="eb8df-152">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb8df-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb8df-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb8df-153">-WhatIf</span></span>
<span data-ttu-id="eb8df-154">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb8df-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb8df-155">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="eb8df-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb8df-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb8df-156">CommonParameters</span></span>
<span data-ttu-id="eb8df-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb8df-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb8df-158">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb8df-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb8df-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eb8df-159">INPUTS</span></span>

### <span data-ttu-id="eb8df-160">System. String</span><span class="sxs-lookup"><span data-stu-id="eb8df-160">System.String</span></span>

### <span data-ttu-id="eb8df-161">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="eb8df-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="eb8df-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eb8df-162">OUTPUTS</span></span>

### <span data-ttu-id="eb8df-163">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="eb8df-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="eb8df-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eb8df-164">NOTES</span></span>

## <span data-ttu-id="eb8df-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eb8df-165">RELATED LINKS</span></span>
