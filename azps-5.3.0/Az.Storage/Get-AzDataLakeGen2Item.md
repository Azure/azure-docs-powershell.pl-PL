---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2Item.md
ms.openlocfilehash: edd65cc10ca90592225b6b9deb04167202510a2e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374138"
---
# <span data-ttu-id="34269-101">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="34269-101">Get-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="34269-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="34269-102">SYNOPSIS</span></span>
<span data-ttu-id="34269-103">Pobiera szczegóły pliku lub katalogu w systemie plików.</span><span class="sxs-lookup"><span data-stu-id="34269-103">Gets the details of a file or directory in a filesystem.</span></span>

## <span data-ttu-id="34269-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="34269-104">SYNTAX</span></span>

```
Get-AzDataLakeGen2Item [-FileSystem] <String> [-Path <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34269-105">Opis</span><span class="sxs-lookup"><span data-stu-id="34269-105">DESCRIPTION</span></span>
<span data-ttu-id="34269-106">Polecenie cmdlet **Get-AzDataLakeGen2Item** pobiera szczegóły pliku lub katalogu w systemie plików na koncie usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="34269-106">The **Get-AzDataLakeGen2Item** cmdlet gets the details of a file or directory in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="34269-107">To polecenie cmdlet działa tylko wtedy, gdy dla konta magazynu jest włączone hierarchiczne obszary nazw.</span><span class="sxs-lookup"><span data-stu-id="34269-107">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="34269-108">Ten rodzaj konta można utworzyć, uruchamiając polecenie cmdlet "New-AzStorageAccount" z opcją "-EnableHierarchicalNamespace $true".</span><span class="sxs-lookup"><span data-stu-id="34269-108">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="34269-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="34269-109">EXAMPLES</span></span>

### <span data-ttu-id="34269-110">Przykład 1: uzyskiwanie katalogu z systemu plików i wyświetlanie szczegółów</span><span class="sxs-lookup"><span data-stu-id="34269-110">Example 1: Get a directory from a Filesystem, and show the details</span></span>
```
PS C:\> $dir1 = Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/"
PS C:\> $dir1

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1                 True                         2020-03-23 09:15:56Z rwx---rwx    $superuser           $superuser     
 
PS C:\WINDOWS\system32> $dir1.ACL

DefaultScope AccessControlType EntityId Permissions
------------ ----------------- -------- -----------
False        User                       rwx        
False        Group                      ---        
False        Other                      rwx      

PS C:\WINDOWS\system32> $dir1.Permissions

Owner        : Execute, Write, Read
Group        : None
Other        : Execute, Write, Read
StickyBit    : False
ExtendedAcls : False

PS C:\WINDOWS\system32> $dir1.Properties.Metadata

Key          Value 
---          ----- 
hdi_isfolder true  
tag1         value1
tag2         value2

PS C:\WINDOWS\system32> $dir1.Properties

LastModified          : 3/23/2020 9:15:56 AM +00:00
CreatedOn             : 3/23/2020 9:15:56 AM +00:00
Metadata              : {[hdi_isfolder, true], [tag1, value1], [tag2, value2]}
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
ContentLength         : 0
ContentType           : application/octet-stream
ETag                  : "0x8D7CF0ACBA35FA8"
ContentHash           : 
ContentEncoding       : UDF12
ContentDisposition    : 
ContentLanguage       : 
CacheControl          : READ
AcceptRanges          : bytes
IsServerEncrypted     : True
EncryptionKeySha256   : 
AccessTier            : Cool
ArchiveStatus         : 
AccessTierChangedOn   : 1/1/0001 12:00:00 AM +00:00
```

<span data-ttu-id="34269-111">To polecenie pobiera katalog z systemu plików i pokazuje szczegóły.</span><span class="sxs-lookup"><span data-stu-id="34269-111">This command gets a directory from a Filesystem, and show the details.</span></span>

### <span data-ttu-id="34269-112">Przykład 2: uzyskiwanie pliku z systemu plików</span><span class="sxs-lookup"><span data-stu-id="34269-112">Example 2: Get a file from a Filesystem</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1"

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:20:37Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="34269-113">To polecenie pobiera szczegóły pliku z systemu plików.</span><span class="sxs-lookup"><span data-stu-id="34269-113">This command gets the details of a file from a Filesystem.</span></span> 

## <span data-ttu-id="34269-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="34269-114">PARAMETERS</span></span>

### <span data-ttu-id="34269-115">-Context</span><span class="sxs-lookup"><span data-stu-id="34269-115">-Context</span></span>
<span data-ttu-id="34269-116">Obiekt kontekstu usługi Azure Storage</span><span class="sxs-lookup"><span data-stu-id="34269-116">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="34269-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34269-117">-DefaultProfile</span></span>
<span data-ttu-id="34269-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="34269-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34269-119">— System plików</span><span class="sxs-lookup"><span data-stu-id="34269-119">-FileSystem</span></span>
<span data-ttu-id="34269-120">Nazwa systemu plików</span><span class="sxs-lookup"><span data-stu-id="34269-120">FileSystem name</span></span>

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

### <span data-ttu-id="34269-121">-Path</span><span class="sxs-lookup"><span data-stu-id="34269-121">-Path</span></span>
<span data-ttu-id="34269-122">Ścieżka w określonym systemie plików, który ma zostać pobrany.</span><span class="sxs-lookup"><span data-stu-id="34269-122">The path in the specified Filesystem that should be retrieved.</span></span>
<span data-ttu-id="34269-123">Może to być plik lub katalog w formacie "Directory/file.txt" lub "directory1/Directory2/".</span><span class="sxs-lookup"><span data-stu-id="34269-123">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="34269-124">Nie określaj tego parametru, aby uzyskać katalog główny systemu plików.</span><span class="sxs-lookup"><span data-stu-id="34269-124">Not specify this parameter to get the root directory of the Filesystem.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34269-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34269-125">CommonParameters</span></span>
<span data-ttu-id="34269-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34269-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34269-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34269-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34269-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34269-128">INPUTS</span></span>

### <span data-ttu-id="34269-129">System. String</span><span class="sxs-lookup"><span data-stu-id="34269-129">System.String</span></span>

### <span data-ttu-id="34269-130">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="34269-130">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="34269-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="34269-131">OUTPUTS</span></span>

### <span data-ttu-id="34269-132">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="34269-132">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="34269-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="34269-133">NOTES</span></span>

## <span data-ttu-id="34269-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34269-134">RELATED LINKS</span></span>
