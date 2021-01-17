---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2Item.md
ms.openlocfilehash: 6af68da41e1d5ea212d23d0cbc2296a68a6fa7e5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335161"
---
# <span data-ttu-id="5b8b6-101">Update-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="5b8b6-101">Update-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="5b8b6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5b8b6-102">SYNOPSIS</span></span>
<span data-ttu-id="5b8b6-103">Aktualizowanie pliku lub katalogu na właściwościach, metadanych, uprawnieniach, listach ACL i właścicielu.</span><span class="sxs-lookup"><span data-stu-id="5b8b6-103">Update a file or directory on properties, metadata, permission, ACL, and owner.</span></span>

## <span data-ttu-id="5b8b6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5b8b6-104">SYNTAX</span></span>

### <span data-ttu-id="5b8b6-105">ReceiveManual (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5b8b6-105">ReceiveManual (Default)</span></span>
```
Update-AzDataLakeGen2Item [-FileSystem] <String> [-Path <String>] [-Permission <String>] [-Owner <String>]
 [-Group <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Acl <PSPathAccessControlEntry[]>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5b8b6-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="5b8b6-106">ItemPipeline</span></span>
```
Update-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> [-Permission <String>] [-Owner <String>]
 [-Group <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Acl <PSPathAccessControlEntry[]>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5b8b6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5b8b6-107">DESCRIPTION</span></span>
<span data-ttu-id="5b8b6-108">Polecenie cmdlet **Update-AzDataLakeGen2Item** aktualizuje plik lub katalog na właściwościach, metadanych, uprawnieniach, listach ACL i właścicielu.</span><span class="sxs-lookup"><span data-stu-id="5b8b6-108">The **Update-AzDataLakeGen2Item** cmdlet updates a file or directory on properties, metadata, permission, ACL, and owner.</span></span>
<span data-ttu-id="5b8b6-109">To polecenie cmdlet działa tylko wtedy, gdy dla konta magazynu jest włączone hierarchiczne obszary nazw.</span><span class="sxs-lookup"><span data-stu-id="5b8b6-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="5b8b6-110">Ten rodzaj konta można utworzyć, uruchamiając polecenie cmdlet "New-AzStorageAccount" z opcją "-EnableHierarchicalNamespace $true".</span><span class="sxs-lookup"><span data-stu-id="5b8b6-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="5b8b6-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5b8b6-111">EXAMPLES</span></span>

### <span data-ttu-id="5b8b6-112">Przykład 1: Tworzenie obiektu ACL z 3 wpisami ACL i aktualizowanie listy ACL do wszystkich elementów w systemie plików cyklicznie</span><span class="sxs-lookup"><span data-stu-id="5b8b6-112">Example 1: Create an ACL object with 3 ACL entry, and update ACL to all items in a Filesystem recursively</span></span>
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

<span data-ttu-id="5b8b6-113">To polecenie najpierw tworzy obiekt ACL z 3 wpisami ACL (Use-Inputobject), aby dodać wpis ACL do istniejącego obiektu ACL, a następnie uzyskać wszystkie elementy w systemie plików i zaktualizować listę ACL elementów.</span><span class="sxs-lookup"><span data-stu-id="5b8b6-113">This command first creates an ACL object with 3 acl entry (use -InputObject parameter to add acl entry to existing acl object), then get all items in a filesystem and update acl on the items.</span></span>

### <span data-ttu-id="5b8b6-114">Przykład 2: aktualizowanie wszystkich właściwości pliku i wyświetlenie ich</span><span class="sxs-lookup"><span data-stu-id="5b8b6-114">Example 2: Update all properties on a file, and show them</span></span>
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

<span data-ttu-id="5b8b6-115">To polecenie aktualizuje wszystkie właściwości pliku (ACL, uprawnienie, właściciel, Grupa, metadane, właściwość może zostać zaktualizowana o dowolne conbination) i pokazywanie ich w konsoli programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5b8b6-115">This command updates all properties on a file (ACL, permission,owner, group, metadata, property can be updated with any conbination), and show them in Powershell console.</span></span>

### <span data-ttu-id="5b8b6-116">Przykład 3: Dodawanie wpisu ACL do katalogu</span><span class="sxs-lookup"><span data-stu-id="5b8b6-116">Example 3: Add an ACL entry to a directory</span></span>
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

<span data-ttu-id="5b8b6-117">To polecenie pobiera listę ACL z katalogu, aktualizuje/dodaje wpis listy ACL, a następnie przywraca go do katalogu.</span><span class="sxs-lookup"><span data-stu-id="5b8b6-117">This command gets ACL from a directory, updates/adds an ACL entry, and sets back to the directory.</span></span>
<span data-ttu-id="5b8b6-118">Jeśli wpis ACL o tej samej AccessControlType/EntityId/DefaultScope nie istnieje, zostanie dodany nowy wpis ACL, w przeciwnym razie uprawnienia do istniejącego wpisu listy ACL.</span><span class="sxs-lookup"><span data-stu-id="5b8b6-118">If ACL entry with same AccessControlType/EntityId/DefaultScope not exist, will add a new ACL entry, else update permission of existing ACL entry.</span></span>

## <span data-ttu-id="5b8b6-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5b8b6-119">PARAMETERS</span></span>

### <span data-ttu-id="5b8b6-120">-ACL</span><span class="sxs-lookup"><span data-stu-id="5b8b6-120">-Acl</span></span>
<span data-ttu-id="5b8b6-121">Ustawia prawa kontroli dostępu POSIX do plików i katalogów.</span><span class="sxs-lookup"><span data-stu-id="5b8b6-121">Sets POSIX access control rights on files and directories.</span></span>
<span data-ttu-id="5b8b6-122">Utwórz ten obiekt, używając nowego-AzDataLakeGen2ItemAclObject.</span><span class="sxs-lookup"><span data-stu-id="5b8b6-122">Create this object with New-AzDataLakeGen2ItemAclObject.</span></span>

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

### <span data-ttu-id="5b8b6-123">-Context</span><span class="sxs-lookup"><span data-stu-id="5b8b6-123">-Context</span></span>
<span data-ttu-id="5b8b6-124">Obiekt kontekstu usługi Azure Storage</span><span class="sxs-lookup"><span data-stu-id="5b8b6-124">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="5b8b6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b8b6-125">-DefaultProfile</span></span>
<span data-ttu-id="5b8b6-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5b8b6-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b8b6-127">— System plików</span><span class="sxs-lookup"><span data-stu-id="5b8b6-127">-FileSystem</span></span>
<span data-ttu-id="5b8b6-128">Nazwa systemu plików</span><span class="sxs-lookup"><span data-stu-id="5b8b6-128">FileSystem name</span></span>

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

### <span data-ttu-id="5b8b6-129">-Group</span><span class="sxs-lookup"><span data-stu-id="5b8b6-129">-Group</span></span>
<span data-ttu-id="5b8b6-130">Ustawia grupę będącą właścicielem obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="5b8b6-130">Sets the owning group of the blob.</span></span>

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

### <span data-ttu-id="5b8b6-131">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5b8b6-131">-InputObject</span></span>
<span data-ttu-id="5b8b6-132">Obiekt usługi Azure datalake Gen2 do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="5b8b6-132">Azure Datalake Gen2 Item Object to update</span></span>

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

### <span data-ttu-id="5b8b6-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="5b8b6-133">-Metadata</span></span>
<span data-ttu-id="5b8b6-134">Określa metadane katalogu lub pliku.</span><span class="sxs-lookup"><span data-stu-id="5b8b6-134">Specifies metadata for the directory or file.</span></span>

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

### <span data-ttu-id="5b8b6-135">-Właściciel</span><span class="sxs-lookup"><span data-stu-id="5b8b6-135">-Owner</span></span>
<span data-ttu-id="5b8b6-136">Ustawia właściciela obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="5b8b6-136">Sets the owner of the blob.</span></span>

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

### <span data-ttu-id="5b8b6-137">-Path</span><span class="sxs-lookup"><span data-stu-id="5b8b6-137">-Path</span></span>
<span data-ttu-id="5b8b6-138">Ścieżka w określonym systemie plików, która powinna zostać zaktualizowana.</span><span class="sxs-lookup"><span data-stu-id="5b8b6-138">The path in the specified Filesystem that should be updated.</span></span>
<span data-ttu-id="5b8b6-139">Może to być plik lub katalog w formacie "Directory/file.txt" lub "directory1/Directory2/".</span><span class="sxs-lookup"><span data-stu-id="5b8b6-139">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="5b8b6-140">Nieokreślenie tego parametru spowoduje zaktualizowanie katalogu głównego systemu plików.</span><span class="sxs-lookup"><span data-stu-id="5b8b6-140">Not specify this parameter will update the root directory of the Filesystem.</span></span>

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

### <span data-ttu-id="5b8b6-141">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="5b8b6-141">-Permission</span></span>
<span data-ttu-id="5b8b6-142">Umożliwia ustawianie uprawnień dostępu do POSIX dla właściciela pliku, grupy będącej właścicielem i innych.</span><span class="sxs-lookup"><span data-stu-id="5b8b6-142">Sets POSIX access permissions for the file owner, the file owning group, and others.</span></span>
<span data-ttu-id="5b8b6-143">Każdej klasie można udzielić uprawnień Odczyt, zapis lub wykonywanie.</span><span class="sxs-lookup"><span data-stu-id="5b8b6-143">Each class may be granted read, write, or execute permission.</span></span>
<span data-ttu-id="5b8b6-144">Obsługa symboliczna (rwxrw-RW-).</span><span class="sxs-lookup"><span data-stu-id="5b8b6-144">Symbolic (rwxrw-rw-) is supported.</span></span>
<span data-ttu-id="5b8b6-145">Nieprawidłowy w połączeniu z listą ACL.</span><span class="sxs-lookup"><span data-stu-id="5b8b6-145">Invalid in conjunction with Acl.</span></span>

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

### <span data-ttu-id="5b8b6-146">-Property</span><span class="sxs-lookup"><span data-stu-id="5b8b6-146">-Property</span></span>
<span data-ttu-id="5b8b6-147">Określa właściwości katalogu lub pliku.</span><span class="sxs-lookup"><span data-stu-id="5b8b6-147">Specifies properties for the directory or file.</span></span> <span data-ttu-id="5b8b6-148">Obsługiwane właściwości pliku to: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="5b8b6-148">The supported properties for file are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>
<span data-ttu-id="5b8b6-149">Obsługiwane właściwości katalogu to: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span><span class="sxs-lookup"><span data-stu-id="5b8b6-149">The supported properties for directory are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span></span>

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

### <span data-ttu-id="5b8b6-150">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5b8b6-150">-Confirm</span></span>
<span data-ttu-id="5b8b6-151">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b8b6-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b8b6-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b8b6-152">-WhatIf</span></span>
<span data-ttu-id="5b8b6-153">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b8b6-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b8b6-154">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5b8b6-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b8b6-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b8b6-155">CommonParameters</span></span>
<span data-ttu-id="5b8b6-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b8b6-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b8b6-157">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b8b6-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b8b6-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5b8b6-158">INPUTS</span></span>

### <span data-ttu-id="5b8b6-159">System. String</span><span class="sxs-lookup"><span data-stu-id="5b8b6-159">System.String</span></span>

### <span data-ttu-id="5b8b6-160">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="5b8b6-160">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="5b8b6-161">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="5b8b6-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="5b8b6-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5b8b6-162">OUTPUTS</span></span>

### <span data-ttu-id="5b8b6-163">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="5b8b6-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="5b8b6-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5b8b6-164">NOTES</span></span>

## <span data-ttu-id="5b8b6-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5b8b6-165">RELATED LINKS</span></span>
