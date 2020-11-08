---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2Item.md
ms.openlocfilehash: ffbfad973e881c3ae88e961517d097d7c8d6cedd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051271"
---
# Get-AzDataLakeGen2Item

## STRESZCZENIe
Pobiera szczegóły pliku lub katalogu w systemie plików.

## POLECENIA

```
Get-AzDataLakeGen2Item [-FileSystem] <String> [-Path <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzDataLakeGen2Item** pobiera szczegóły pliku lub katalogu w systemie plików na koncie usługi Azure Storage.
To polecenie cmdlet działa tylko wtedy, gdy dla konta magazynu jest włączone hierarchiczne obszary nazw. Ten rodzaj konta można utworzyć, uruchamiając polecenie cmdlet "New-AzStorageAccount" z opcją "-EnableHierarchicalNamespace $true".

## Przykłady

### Przykład 1: uzyskiwanie katalogu z systemu plików i wyświetlanie szczegółów
```
PS C:\> $dir1 = Get-AzDataLakeGen2tem -FileSystem "filesystem1" -Path "dir1/"
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

To polecenie pobiera katalog z systemu plików i pokazuje szczegóły.

### Przykład 2: uzyskiwanie pliku z systemu plików
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1"

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:20:37Z rwx---rwx    $superuser           $superuser
```

To polecenie pobiera szczegóły pliku z systemu plików. 

## PARAMETRÓW

### -Context
Obiekt kontekstu usługi Azure Storage

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

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

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

### — System plików
Nazwa systemu plików

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

### -Path
Ścieżka w określonym systemie plików, który ma zostać pobrany.
Może to być plik lub katalog w formacie "Directory/file.txt" lub "directory1/Directory2/".
Nie określaj tego parametru, aby uzyskać katalog główny systemu plików.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

### Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext

## WYSYŁA

### Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item

## INFORMACYJN

## LINKI POKREWNE
