---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azdatalakegen2itemaclobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemAclObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemAclObject.md
ms.openlocfilehash: 209cb5ded738faabfdafc113d3d9524f7c01e927
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243178"
---
# Set-AzDataLakeGen2ItemAclObject

## SYNOPSIS
Tworzy/aktualizuje obiekt ACL elementu ACL elementu ACL (dataLake gen2), którego można użyć w Update-AzDataLakeGen2Item cmdlet.

## SKŁADNIA

```
Set-AzDataLakeGen2ItemAclObject [-EntityId <String>] [-DefaultScope] -Permission <String>
 [-InputObject <PSPathAccessControlEntry[]>] -AccessControlType <AccessControlType> [<CommonParameters>]
```

## OPIS
Polecenie cmdlet **Set-AzDataLakeGen2ItemAclObject** tworzy/aktualizuje obiekt ACL elementu ACL elementu DataLake gen2, którego można użyć w Update-AzDataLakeGen2Item cmdlet.
Jeśli nowy wpis ACL z tym samym elementem AccessControlType/EntityId/DefaultScope nie istnieje w wejściowym aclu, utworzy nowy wpis ACL, a w innym przypadku zaktualizuje uprawnienia istniejącego wpisu ACL.

## PRZYKŁADY

### Przykład 1. Tworzenie obiektu ACL z wpisem 3 ACL i aktualizowanie listy ACL w katalogu
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

To polecenie tworzy obiekt ACL z 3 pozycjami ACL (użyj parametru -InputObject, aby dodać wpis acl do istniejącego obiektu acl) i aktualizuje wartość ACL w katalogu.

### Przykład 2. Tworzenie obiektu ACL z 4 pozycjami ACL i aktualizowanie uprawnień istniejącego wpisu ACL
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

To polecenie najpierw tworzy obiekt ACL z 4 pozycjami listy ACL, a następnie ponownie uruchamia polecenie cmdlet z innymi uprawnieniami, ale z tym samym obiektem AccessControlType/EntityId/DefaultScope istniejącego wpisu ACL.
Następnie uprawnienia wpisu listy ACL zostaną zaktualizowane, ale nie zostanie dodany żaden nowy wpis ACL.

## PARAMETERS

### -AccessControlType
Istnieją cztery typy: "użytkownik" udziela praw właścicielowi lub nazwanemu użytkownikowi, "grupa" udziela praw grupie posiadającej lub nazwanej grupie, "maska" ogranicza prawa przyznane nazwanych użytkownikom i członkom grup, a "inne" udziela praw wszystkim użytkownikom, których nie znaleziono w żadnych innych wpisach.

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
Ustaw ten parametr, aby wskazać, że wpis ACE należy do domyślnej listy ACL dla katalogu; w przeciwnym razie zakres jest niejawny, a wpis ACE należy do listy kontroli dostępu.

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
Jest ona pominięta w przypadku wpisów "mask" i "other" programu AccessControlType.
Identyfikator użytkownika lub grupy jest również pominięty dla właściciela i właściciela grupy.

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

### -InputObject
W przypadku wprowadzania obiektu PSPathAccessControlEntry nowy element ACL zostanie dodać jako nowy element obiektu \[ \] wejściowego PSPathAccessControlEntry. \[ \]

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

### — Uprawnienie
Pole uprawnienia to 3-znakowa sekwencja, w której pierwszy znak to "r" w celu udzielenia dostępu do odczytu, drugi znak to "w" w celu udzielenia dostępu do zapisu, a trzeci znak to "x" w celu udzielenia uprawnienia wykonywania.
Jeśli nie udzielono dostępu, znak "-" jest używany do oznaczania, że uprawnienie zostanie odrzucone.

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Brak

## DANE WYJŚCIOWE

### Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry

## NOTATKI

## LINKI POKREWNE
