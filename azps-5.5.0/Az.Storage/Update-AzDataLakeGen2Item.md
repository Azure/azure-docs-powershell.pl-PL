---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2Item.md
ms.openlocfilehash: 6af68da41e1d5ea212d23d0cbc2296a68a6fa7e5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190698"
---
# <span data-ttu-id="9eb30-101">Update-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="9eb30-101">Update-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="9eb30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9eb30-102">SYNOPSIS</span></span>
<span data-ttu-id="9eb30-103">Aktualizowanie pliku lub katalogu na właściwości, metadane, uprawnienia, acl i właściciela.</span><span class="sxs-lookup"><span data-stu-id="9eb30-103">Update a file or directory on properties, metadata, permission, ACL, and owner.</span></span>

## <span data-ttu-id="9eb30-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9eb30-104">SYNTAX</span></span>

### <span data-ttu-id="9eb30-105">ReceiveManual (Default)</span><span class="sxs-lookup"><span data-stu-id="9eb30-105">ReceiveManual (Default)</span></span>
```
Update-AzDataLakeGen2Item [-FileSystem] <String> [-Path <String>] [-Permission <String>] [-Owner <String>]
 [-Group <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Acl <PSPathAccessControlEntry[]>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9eb30-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="9eb30-106">ItemPipeline</span></span>
```
Update-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> [-Permission <String>] [-Owner <String>]
 [-Group <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Acl <PSPathAccessControlEntry[]>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9eb30-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="9eb30-107">DESCRIPTION</span></span>
<span data-ttu-id="9eb30-108">Polecenie **cmdlet Update-AzDataLakeGen2Item** aktualizuje plik lub katalog na podstawie właściwości, metadanych, uprawnień, listy ACL i właściciela.</span><span class="sxs-lookup"><span data-stu-id="9eb30-108">The **Update-AzDataLakeGen2Item** cmdlet updates a file or directory on properties, metadata, permission, ACL, and owner.</span></span>
<span data-ttu-id="9eb30-109">To polecenie cmdlet działa tylko wtedy, gdy dla konta magazynu włączono hierarchiczną przestrzeń nazw.</span><span class="sxs-lookup"><span data-stu-id="9eb30-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="9eb30-110">Tego rodzaju konto można utworzyć, uruchamiam polecenie cmdlet "New-AzStorageAccount" z poleceniem "-EnableHierarchicalNamespace $true".</span><span class="sxs-lookup"><span data-stu-id="9eb30-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="9eb30-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9eb30-111">EXAMPLES</span></span>

### <span data-ttu-id="9eb30-112">Przykład 1. Tworzenie obiektu ACL z wpisem 3 ACL i aktualizowanie listy ACL do wszystkich elementów w systemie plików cyklicznie</span><span class="sxs-lookup"><span data-stu-id="9eb30-112">Example 1: Create an ACL object with 3 ACL entry, and update ACL to all items in a Filesystem recursively</span></span>
```
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" -Recurse | Update-AzDataLakeGen2Item -ACL $acl

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1                 True                         2020-03-13 13:07:34Z rwxrw-rw-    $superuser           $superuser           
dir1/file1           False        1024            2020-03-23 09:29:18Z rwxrw-rw-    $superuser           $superuser          
dir2                 True                         2020-03-23 09:28:36Z rwxrw-rw-    $superuser           $superuser
```

<span data-ttu-id="9eb30-113">To polecenie najpierw tworzy obiekt ACL z wpisem 3 acl (użyj parametru -InputObject, aby dodać wpis acl do istniejącego obiektu acl), a następnie pobierz wszystkie elementy w systemie plików i zaktualizuj wartość ACL elementów.</span><span class="sxs-lookup"><span data-stu-id="9eb30-113">This command first creates an ACL object with 3 acl entry (use -InputObject parameter to add acl entry to existing acl object), then get all items in a filesystem and update acl on the items.</span></span>

### <span data-ttu-id="9eb30-114">Przykład 2. Aktualizowanie wszystkich właściwości pliku i wyświetlanie ich</span><span class="sxs-lookup"><span data-stu-id="9eb30-114">Example 2: Update all properties on a file, and show them</span></span>
```
PS C:\> $file = Update-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1" `
                 -Acl $acl `
                 -Property @{"ContentType" = "image/jpeg"; "ContentMD5" = "i727sP7HigloQDsqadNLHw=="; "ContentEncoding" = "UDF8"; "CacheControl" = "READ"; "ContentDisposition" = "True"; "ContentLanguage" = "EN-US"} `
                 -Metadata  @{"tag1" = "value1"; "tag2" = "value2" } `
                 -Permission rw-rw-rwx `
                 -Owner '$superuser' `
                 -Group '$superuser'

PS C:\> $file

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:57:33Z rwxrw-rw-    $superuser           $superuser          

PS C:\> $file.ACL

DefaultScope AccessControlType EntityId Permissions
------------ ----------------- -------- -----------
False        User                       rwx        
False        Group                      rw-        
False        Other                      rw-        

PS C:\> $file.Permissions

Owner        : Execute, Write, Read
Group        : Write, Read
Other        : Write, Read
StickyBit    : False
ExtendedAcls : False

PS C:\> $file.Properties.Metadata

Key  Value 
---  ----- 
tag2 value2
tag1 value1

PS C:\> $file.Properties


LastModified          : 3/23/2020 9:57:33 AM +00:00
CreatedOn             : 3/23/2020 9:29:18 AM +00:00
Metadata              : {[tag2, value2], [tag1, value1]}
CopyCompletedOn       : 1/1/0001 12:00:00 AM +00:00
CopyStatusDescription : 
CopyId                : 
CopyProgress          : 
CopySource            : 
CopyStatus            : Pending
IsIncrementalCopy     : False
LeaseDuration         : Infinite
LeaseState            : Available
LeaseStatus           : Unlocked
ContentLength         : 1024
ContentType           : image/jpeg
ETag                  : "0x8D7CF109B9878CC"
ContentHash           : {139, 189, 187, 176...}
ContentEncoding       : UDF8
ContentDisposition    : True
ContentLanguage       : EN-US
CacheControl          : READ
AcceptRanges          : bytes
IsServerEncrypted     : True
EncryptionKeySha256   : 
AccessTier            : Cool
ArchiveStatus         : 
AccessTierChangedOn   : 1/1/0001 12:00:00 AM +00:00
```

<span data-ttu-id="9eb30-115">To polecenie aktualizuje wszystkie właściwości pliku (ACL, permission, owner, group, metadata, property can be updated with any conbination) i wyświetla je w konsoli programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9eb30-115">This command updates all properties on a file (ACL, permission,owner, group, metadata, property can be updated with any conbination), and show them in Powershell console.</span></span>

### <span data-ttu-id="9eb30-116">Przykład 3. Dodawanie wpisu listy ACL do katalogu</span><span class="sxs-lookup"><span data-stu-id="9eb30-116">Example 3: Add an ACL entry to a directory</span></span>
```
## Get the origin ACL
PS C:\> $acl = (Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path 'dir1/dir3/').ACL

# Update permission of a new ACL entry (if ACL entry with same AccessControlType/EntityId/DefaultScope not exist, will add a new ACL entry, else update permission of existing ACL entry)
PS C:\> $acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission rw- -InputObject $acl  

# set the new acl to the directory
PS C:\> update-AzDataLakeGen2Item -FileSystem "filesystem1" -Path 'dir1/dir3/' -ACL $acl

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir3            True                         2020-03-23 09:34:31Z rwxrw-rw-+   $superuser           $superuser
```

<span data-ttu-id="9eb30-117">To polecenie pobiera pozycję ACL z katalogu, aktualizuje/dodaje pozycję ACL i wraca do katalogu.</span><span class="sxs-lookup"><span data-stu-id="9eb30-117">This command gets ACL from a directory, updates/adds an ACL entry, and sets back to the directory.</span></span>
<span data-ttu-id="9eb30-118">Jeśli wpis ACL z tym samym elementem AccessControlType/EntityId/DefaultScope nie istnieje, spowoduje dodanie nowego wpisu ACL, a w innym przypadku zaktualizowanie uprawnienia istniejącego wpisu ACL.</span><span class="sxs-lookup"><span data-stu-id="9eb30-118">If ACL entry with same AccessControlType/EntityId/DefaultScope not exist, will add a new ACL entry, else update permission of existing ACL entry.</span></span>

## <span data-ttu-id="9eb30-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9eb30-119">PARAMETERS</span></span>

### <span data-ttu-id="9eb30-120">—Acl</span><span class="sxs-lookup"><span data-stu-id="9eb30-120">-Acl</span></span>
<span data-ttu-id="9eb30-121">Ustawia prawa kontroli dostępu posix w plikach i katalogach.</span><span class="sxs-lookup"><span data-stu-id="9eb30-121">Sets POSIX access control rights on files and directories.</span></span>
<span data-ttu-id="9eb30-122">Utwórz ten obiekt za pomocą obiektu New-AzDataLakeGen2ItemAclObject.</span><span class="sxs-lookup"><span data-stu-id="9eb30-122">Create this object with New-AzDataLakeGen2ItemAclObject.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eb30-123">— kontekst</span><span class="sxs-lookup"><span data-stu-id="9eb30-123">-Context</span></span>
<span data-ttu-id="9eb30-124">Obiekt kontekstowy magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="9eb30-124">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="9eb30-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eb30-125">-DefaultProfile</span></span>
<span data-ttu-id="9eb30-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9eb30-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9eb30-127">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="9eb30-127">-FileSystem</span></span>
<span data-ttu-id="9eb30-128">Nazwa systemu plików</span><span class="sxs-lookup"><span data-stu-id="9eb30-128">FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9eb30-129">— Grupowanie</span><span class="sxs-lookup"><span data-stu-id="9eb30-129">-Group</span></span>
<span data-ttu-id="9eb30-130">Ustawia grupę, która jest właścicielem obiektu blob.</span><span class="sxs-lookup"><span data-stu-id="9eb30-130">Sets the owning group of the blob.</span></span>

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

### <span data-ttu-id="9eb30-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9eb30-131">-InputObject</span></span>
<span data-ttu-id="9eb30-132">Obiekt elementu Platformy Azure Datalake Gen2 do aktualizacji</span><span class="sxs-lookup"><span data-stu-id="9eb30-132">Azure Datalake Gen2 Item Object to update</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item
Parameter Sets: ItemPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9eb30-133">— Metadane</span><span class="sxs-lookup"><span data-stu-id="9eb30-133">-Metadata</span></span>
<span data-ttu-id="9eb30-134">Określa metadane dla katalogu lub pliku.</span><span class="sxs-lookup"><span data-stu-id="9eb30-134">Specifies metadata for the directory or file.</span></span>

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

### <span data-ttu-id="9eb30-135">— Właściciel</span><span class="sxs-lookup"><span data-stu-id="9eb30-135">-Owner</span></span>
<span data-ttu-id="9eb30-136">Ustawia właściciela obiektu blob.</span><span class="sxs-lookup"><span data-stu-id="9eb30-136">Sets the owner of the blob.</span></span>

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

### <span data-ttu-id="9eb30-137">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="9eb30-137">-Path</span></span>
<span data-ttu-id="9eb30-138">Ścieżka w określonym systemie plików, która powinna zostać zaktualizowana.</span><span class="sxs-lookup"><span data-stu-id="9eb30-138">The path in the specified Filesystem that should be updated.</span></span>
<span data-ttu-id="9eb30-139">Może być plikiem lub katalogiem w formacie "katalog/file.txt" lub "katalog1/katalog2/".</span><span class="sxs-lookup"><span data-stu-id="9eb30-139">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="9eb30-140">Nie określ tego parametru zaktualizuje katalog główny systemu plików.</span><span class="sxs-lookup"><span data-stu-id="9eb30-140">Not specify this parameter will update the root directory of the Filesystem.</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9eb30-141">— Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="9eb30-141">-Permission</span></span>
<span data-ttu-id="9eb30-142">Ustawia uprawnienia dostępu posix dla właściciela pliku, grupy, która jest właścicielem pliku i innych.</span><span class="sxs-lookup"><span data-stu-id="9eb30-142">Sets POSIX access permissions for the file owner, the file owning group, and others.</span></span>
<span data-ttu-id="9eb30-143">Każdemu zajęć można przyznać uprawnienie do odczytu, zapisu lub wykonywania.</span><span class="sxs-lookup"><span data-stu-id="9eb30-143">Each class may be granted read, write, or execute permission.</span></span>
<span data-ttu-id="9eb30-144">Obsługiwane jest symboliczne (rwxrw-rw-).</span><span class="sxs-lookup"><span data-stu-id="9eb30-144">Symbolic (rwxrw-rw-) is supported.</span></span>
<span data-ttu-id="9eb30-145">Nieprawidłowe w połączeniu z Acl.</span><span class="sxs-lookup"><span data-stu-id="9eb30-145">Invalid in conjunction with Acl.</span></span>

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

### <span data-ttu-id="9eb30-146">- Właściwość</span><span class="sxs-lookup"><span data-stu-id="9eb30-146">-Property</span></span>
<span data-ttu-id="9eb30-147">Określa właściwości katalogu lub pliku.</span><span class="sxs-lookup"><span data-stu-id="9eb30-147">Specifies properties for the directory or file.</span></span> <span data-ttu-id="9eb30-148">Obsługiwane właściwości pliku to: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="9eb30-148">The supported properties for file are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>
<span data-ttu-id="9eb30-149">Obsługiwane właściwości katalogu to: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span><span class="sxs-lookup"><span data-stu-id="9eb30-149">The supported properties for directory are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span></span>

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

### <span data-ttu-id="9eb30-150">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9eb30-150">-Confirm</span></span>
<span data-ttu-id="9eb30-151">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9eb30-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9eb30-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9eb30-152">-WhatIf</span></span>
<span data-ttu-id="9eb30-153">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9eb30-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9eb30-154">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9eb30-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9eb30-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eb30-155">CommonParameters</span></span>
<span data-ttu-id="9eb30-156">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9eb30-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eb30-157">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9eb30-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eb30-158">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9eb30-158">INPUTS</span></span>

### <span data-ttu-id="9eb30-159">System.String</span><span class="sxs-lookup"><span data-stu-id="9eb30-159">System.String</span></span>

### <span data-ttu-id="9eb30-160">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="9eb30-160">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="9eb30-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9eb30-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9eb30-162">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9eb30-162">OUTPUTS</span></span>

### <span data-ttu-id="9eb30-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="9eb30-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="9eb30-164">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9eb30-164">NOTES</span></span>

## <span data-ttu-id="9eb30-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9eb30-165">RELATED LINKS</span></span>
