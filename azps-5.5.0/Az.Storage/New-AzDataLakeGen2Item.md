---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzDataLakeGen2Item.md
ms.openlocfilehash: 26f3dbc3462688458647e2e9676916063ffa3586
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190874"
---
# <span data-ttu-id="2c287-101">New-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="2c287-101">New-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="2c287-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c287-102">SYNOPSIS</span></span>
<span data-ttu-id="2c287-103">Utwórz plik lub katalog w systemie plików.</span><span class="sxs-lookup"><span data-stu-id="2c287-103">Create a file or directory in a filesystem.</span></span>

## <span data-ttu-id="2c287-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2c287-104">SYNTAX</span></span>

### <span data-ttu-id="2c287-105">Plik (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2c287-105">File (Default)</span></span>
```
New-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> -Source <String> [-Umask <String>]
 [-Permission <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c287-106">Katalog</span><span class="sxs-lookup"><span data-stu-id="2c287-106">Directory</span></span>
```
New-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> [-Directory] [-Umask <String>]
 [-Permission <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c287-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="2c287-107">DESCRIPTION</span></span>
<span data-ttu-id="2c287-108">Polecenie **cmdlet New-AzDataLakeGen2Item** tworzy plik lub katalog w systemie plików na koncie magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2c287-108">The **New-AzDataLakeGen2Item** cmdlet creates a file or directory in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="2c287-109">To polecenie cmdlet działa tylko wtedy, gdy dla konta magazynu włączono hierarchiczną przestrzeń nazw.</span><span class="sxs-lookup"><span data-stu-id="2c287-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="2c287-110">Tego rodzaju konto można utworzyć, uruchamiam polecenie cmdlet "New-AzStorageAccount" z poleceniem "-EnableHierarchicalNamespace $true".</span><span class="sxs-lookup"><span data-stu-id="2c287-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="2c287-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2c287-111">EXAMPLES</span></span>

### <span data-ttu-id="2c287-112">Przykład 1. Tworzenie katalogu z określonymi uprawnieniami,maskiem, właściwościami i metadanymi</span><span class="sxs-lookup"><span data-stu-id="2c287-112">Example 1: Create a directory with specified permission, Umask, properties, and metadata</span></span>
```
PS C:\>New-AzDataLakeGen2Item -FileSystem "testfilesystem" -Path "dir1/dir2/" -Directory -Permission rwxrwxrwx -Umask ---rw---- -Property @{"CacheControl" = "READ"; "ContentDisposition" = "True"} -Metadata  @{"tag1" = "value1"; "tag2" = "value2" }

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir2            True                         2020-03-23 09:15:56Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="2c287-113">To polecenie tworzy katalog z określonymi uprawnieniami,maskiem, właściwościami i metadanymi</span><span class="sxs-lookup"><span data-stu-id="2c287-113">This command creates a directory with specified Permission, Umask, properties, and metadata</span></span>

### <span data-ttu-id="2c287-114">Przykład 2. Tworzenie(przekazywanie) pliku jeziora danych z lokalnego pliku źródłowego, a polecenie cmdlet działa w tle</span><span class="sxs-lookup"><span data-stu-id="2c287-114">Example 2: Create(upload) a data lake file from a local source file, and the cmdlet runs in background</span></span>
```
PS C:\> $task = New-AzDataLakeGen2Item  -FileSystem "testfilesystem" -Path "dir1/dir2/file1" -Source "c:\sourcefile.txt" -Force -asjob
PS C:\> $task | Wait-Job
PS C:\> $task.Output

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group                
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir2/file1      False        14400000        2020-03-23 09:19:13Z rw-r-----    $superuser           $superuser
```

<span data-ttu-id="2c287-115">To polecenie tworzy (przekaż) plik jeziora danych z lokalnego pliku źródłowego i polecenie cmdlet działa w tle.</span><span class="sxs-lookup"><span data-stu-id="2c287-115">This command creates(upload) a data lake file from a local source file, and the cmdlet runs in background.</span></span>

## <span data-ttu-id="2c287-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c287-116">PARAMETERS</span></span>

### <span data-ttu-id="2c287-117">— AsJob</span><span class="sxs-lookup"><span data-stu-id="2c287-117">-AsJob</span></span>
<span data-ttu-id="2c287-118">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="2c287-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2c287-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="2c287-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="2c287-120">Całkowita ilość jednoczesnych zadań synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="2c287-120">The total amount of concurrent async tasks.</span></span> <span data-ttu-id="2c287-121">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="2c287-121">The default value is 10.</span></span>

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

### <span data-ttu-id="2c287-122">— kontekst</span><span class="sxs-lookup"><span data-stu-id="2c287-122">-Context</span></span>
<span data-ttu-id="2c287-123">Obiekt kontekstowy magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="2c287-123">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="2c287-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c287-124">-DefaultProfile</span></span>
<span data-ttu-id="2c287-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2c287-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c287-126">— Katalog</span><span class="sxs-lookup"><span data-stu-id="2c287-126">-Directory</span></span>
<span data-ttu-id="2c287-127">Wskazuje, że ten nowy element jest katalogiem, a nie plikiem.</span><span class="sxs-lookup"><span data-stu-id="2c287-127">Indicates that this new item is a directory and not a file.</span></span>

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

### <span data-ttu-id="2c287-128">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="2c287-128">-FileSystem</span></span>
<span data-ttu-id="2c287-129">Nazwa systemu plików</span><span class="sxs-lookup"><span data-stu-id="2c287-129">FileSystem name</span></span>

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

### <span data-ttu-id="2c287-130">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="2c287-130">-Force</span></span>
<span data-ttu-id="2c287-131">Jeśli pomyślnie przekazano, nowy element jest tworzony bez żadnych monitów</span><span class="sxs-lookup"><span data-stu-id="2c287-131">If passed then new item is created without any prompt</span></span>

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

### <span data-ttu-id="2c287-132">— Metadane</span><span class="sxs-lookup"><span data-stu-id="2c287-132">-Metadata</span></span>
<span data-ttu-id="2c287-133">Określa metadane dla utworzonego katalogu lub pliku.</span><span class="sxs-lookup"><span data-stu-id="2c287-133">Specifies metadata for the created directory or file.</span></span>

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

### <span data-ttu-id="2c287-134">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="2c287-134">-Path</span></span>
<span data-ttu-id="2c287-135">Ścieżka w określonym systemie plików, którą należy utworzyć.</span><span class="sxs-lookup"><span data-stu-id="2c287-135">The path in the specified Filesystem that should be create.</span></span>
<span data-ttu-id="2c287-136">Może być plikiem lub katalogiem w formacie "katalog/file.txt" lub "katalog1/katalog2/"</span><span class="sxs-lookup"><span data-stu-id="2c287-136">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

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

### <span data-ttu-id="2c287-137">— Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="2c287-137">-Permission</span></span>
<span data-ttu-id="2c287-138">Ustawia uprawnienia dostępu posix dla właściciela pliku, grupy, która jest właścicielem pliku i innych.</span><span class="sxs-lookup"><span data-stu-id="2c287-138">Sets POSIX access permissions for the file owner, the file owning group, and others.</span></span>
<span data-ttu-id="2c287-139">Każdemu zajęć można przyznać uprawnienie do odczytu, zapisu lub wykonywania.</span><span class="sxs-lookup"><span data-stu-id="2c287-139">Each class may be granted read, write, or execute permission.</span></span>
<span data-ttu-id="2c287-140">Obsługiwane jest symboliczne (rwxrw-rw-).</span><span class="sxs-lookup"><span data-stu-id="2c287-140">Symbolic (rwxrw-rw-) is supported.</span></span>

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

### <span data-ttu-id="2c287-141">- Właściwość</span><span class="sxs-lookup"><span data-stu-id="2c287-141">-Property</span></span>
<span data-ttu-id="2c287-142">Określa właściwości utworzonego katalogu lub pliku.</span><span class="sxs-lookup"><span data-stu-id="2c287-142">Specifies properties for the created directory or file.</span></span> <span data-ttu-id="2c287-143">Obsługiwane właściwości pliku to: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="2c287-143">The supported properties for file are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>
<span data-ttu-id="2c287-144">Obsługiwane właściwości katalogu to: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span><span class="sxs-lookup"><span data-stu-id="2c287-144">The supported properties for directory are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span></span>

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

### <span data-ttu-id="2c287-145">— Źródło</span><span class="sxs-lookup"><span data-stu-id="2c287-145">-Source</span></span>
<span data-ttu-id="2c287-146">Określ lokalną ścieżkę pliku źródłowego, która zostanie przekazać do pliku Datalake Gen2.</span><span class="sxs-lookup"><span data-stu-id="2c287-146">Specify the local source file path which will be upload to a Datalake Gen2 file.</span></span>

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

### <span data-ttu-id="2c287-147">-Umask</span><span class="sxs-lookup"><span data-stu-id="2c287-147">-Umask</span></span>
<span data-ttu-id="2c287-148">Podczas tworzenia nowego elementu i katalogu nadrzędnego nie ma domyślnej listy ACL, maski ograniczają uprawnienia do pliku lub katalogu do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="2c287-148">When creating New Item and the parent directory does not have a default ACL, the umask restricts the permissions of the file or directory to be created.</span></span>
<span data-ttu-id="2c287-149">Uprawnienie wynikowe jest nadane przez p & ^u, gdzie p jest uprawnieniem, a Ty jesteśmaskiem.</span><span class="sxs-lookup"><span data-stu-id="2c287-149">The resulting permission is given by p & ^u, where p is the permission and u is the umask.</span></span>
<span data-ttu-id="2c287-150">Obsługiwane jest symboliczne (rwxrw-rw-).</span><span class="sxs-lookup"><span data-stu-id="2c287-150">Symbolic (rwxrw-rw-) is supported.</span></span>

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

### <span data-ttu-id="2c287-151">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2c287-151">-Confirm</span></span>
<span data-ttu-id="2c287-152">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2c287-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c287-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c287-153">-WhatIf</span></span>
<span data-ttu-id="2c287-154">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c287-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c287-155">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2c287-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c287-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c287-156">CommonParameters</span></span>
<span data-ttu-id="2c287-157">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c287-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c287-158">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c287-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c287-159">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2c287-159">INPUTS</span></span>

### <span data-ttu-id="2c287-160">System.String</span><span class="sxs-lookup"><span data-stu-id="2c287-160">System.String</span></span>

### <span data-ttu-id="2c287-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2c287-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2c287-162">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2c287-162">OUTPUTS</span></span>

### <span data-ttu-id="2c287-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="2c287-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="2c287-164">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2c287-164">NOTES</span></span>

## <span data-ttu-id="2c287-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2c287-165">RELATED LINKS</span></span>
