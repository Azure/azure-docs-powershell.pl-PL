---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azdatalakegen2itemaclobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemACLObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemACLObject.md
ms.openlocfilehash: d16a476bea988afb53ddff7b34a83658e0f274e1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224747"
---
# Set-AzDataLakeGen2ItemAclObject

## STRESZCZENIe
Tworzy/aktualizuje obiekt Gen2 ACL elementu datalake, którego można użyć w Update-AzDataLakeGen2Item polecenia cmdlet.

## POLECENIA

```
Set-AzDataLakeGen2ItemAclObject [-EntityId <String>] [-DefaultScope] -Permission <String>
 [-InputObject <PSPathAccessControlEntry[]>] -AccessControlType <AccessControlType> [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzDataLakeGen2ItemAclObject** tworzy/AKTUALIZUJE obiekt ACL usługi datalake Gen2, który może być wykorzystywany w Update-AzDataLakeGen2Item polecenia cmdlet.
Jeśli nowy wpis ACL o tej samej AccessControlType/EntityId/DefaultScope nie istnieje na liście ACL danych wejściowych, zostanie utworzony nowy wpis ACL, w przeciwnym razie uprawnienia do istniejącego wpisu listy ACL.

## Przykłady

### Przykład 1: Tworzenie obiektu ACL z 3 wpisami ACL i aktualizowanie listy ACL w katalogu
```
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx -DefaultScope
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\>Update-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/dir3" -ACL $acl

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir3            True                         2020-03-23 09:34:31Z rwxrw-rw-+   $superuser           $superuser
```

To polecenie tworzy obiekt ACL z trzema wpisami listy ACL (Use-Inputobject, aby dodać wpis ACL do istniejącego obiektu ACL), i aktualizuje listę ACL w katalogu.

### Przykład 2: Tworzenie obiektu ACL z czterema wpisami list ACL i aktualizowanie uprawnień do istniejącego wpisu listy ACL
```
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx -DefaultScope
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission rwx -InputObject $acl 
PS C:\>$acl

DefaultScope AccessControlType EntityId                             Permissions
------------ ----------------- --------                             -----------
True         User                                                   rwx        
False        Group                                                  rw-        
False        Other                                                  rw-        
False        User              ********-****-****-****-************ rwx        

PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission r-x -InputObject $acl 
PS C:\>$acl  

DefaultScope AccessControlType EntityId                             Permissions
------------ ----------------- --------                             -----------
True         User                                                   rwx        
False        Group                                                  rw-        
False        Other                                                  rw-        
False        User              ********-****-****-****-************ r-x
```

To polecenie najpierw tworzy obiekt ACL z czterema wpisami listy ACL, a następnie ponownie uruchamia polecenie cmdlet z innymi uprawnieniami, ale ten sam AccessControlType/EntityId/DefaultScope z istniejącego wpisu ACL.
Następnie uprawnienie do wpisu listy ACL zostanie zaktualizowane, ale nie zostanie dodany nowy wpis listy ACL.

## PARAMETRÓW

### -AccessControlType
Istnieją cztery typy: "użytkownik" udziela praw właścicielowi lub nazwanemu użytkownikowi, "Group" udziela praw członkowi grupy lub nazwanej grupie, "maska" ogranicza prawa przyznane pozostałym użytkownikom i członkom grup, a "inne" przyznaje prawa wszystkim użytkownikom, których nie ma w żadnym innym wpisie.

```yaml
Type: Azure.Storage.Files.DataLake.Models.AccessControlType
Parameter Sets: (All)
Aliases:
Accepted values: User, Group, Mask, Other

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultScope
Ustaw ten parametr, aby wskazać, że wpis ACE należy do domyślnego ACL dla katalogu. w przeciwnym razie zakres jest niejawny, a wpis ACE należy do listy ACL programu Access.

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

### -EntityId
Identyfikator użytkownika lub grupy.
Jest ona pomijana dla wpisów AccessControlType "maska" i "inne".
Identyfikator użytkownika lub grupy jest również pomijany dla właściciela i grupy będącej właścicielem.

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

### -Inputobject
Jeśli wprowadzasz obiekt PSPathAccessControlEntry, dodamy \[ \] nową listę ACL jako nowy element wejściowego \[ \] obiektu PSPathAccessControlEntry.

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

### -Uprawnienie
Pole uprawnienia jest sekwencją 3-znakową, w której pierwszym znakiem jest "r", aby udzielić dostępu do odczytu, drugi znak jest literą "w", aby uzyskać dostęp do zapisu, a trzeci znak to "x", aby udzielić uprawnienia EXECUTE.
Jeśli nie zostanie udzielony dostęp, znak "-" jest oznaczany brakiem uprawnień.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono

## WYSYŁA

### Microsoft. platformy windowsazure. Commands. Storage. model. ResourceModel. PSPathAccessControlEntry

## INFORMACYJN

## LINKI POKREWNE
