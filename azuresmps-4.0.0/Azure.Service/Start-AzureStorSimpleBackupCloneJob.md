---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 403AD2BF-5D03-4B48-A635-E08216FFFC0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 07df96f59b2278d804312d1076965ffed43c2569
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054714"
---
# Start-AzureStorSimpleBackupCloneJob

## STRESZCZENIe
Rozpoczyna zadanie, które powoduje sklonowanie kopii zapasowej na urządzeniu.

## POLECENIA

### Empty (domyślnie)
```
Start-AzureStorSimpleBackupCloneJob -BackupId <String> -Snapshot <Snapshot> -CloneVolumeName <String>
 [-TargetAccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByName
```
Start-AzureStorSimpleBackupCloneJob -SourceDeviceName <String> -TargetDeviceName <String> -BackupId <String>
 -Snapshot <Snapshot> -CloneVolumeName <String>
 [-TargetAccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyById
```
Start-AzureStorSimpleBackupCloneJob -SourceDeviceId <String> -TargetDeviceId <String> -BackupId <String>
 -Snapshot <Snapshot> -CloneVolumeName <String>
 [-TargetAccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Start-AzureStorSimpleBackupCloneJob** rozpoczyna zadanie, które umożliwia sklonowanie istniejącej kopii zapasowej na urządzeniu z systemem StorSimple.

## Przykłady

### Przykład 1: klonowanie kopii zapasowej do innego woluminu przy użyciu nazw urządzeń
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "ContosoDev07" -First 1
PS C:\> $Acrs = Get-AzureStorSimpleAccessControlRecord -ACRName "Acr01"
PS C:\> Start-AzureStorSimpleBackupCloneJob -SourceDeviceName "ContosoDev07 -TargetDeviceName "ContosoDev07" -BackupId $Backup.InstanceId -Snapshot $Backup.Snapshots[0] -CloneVolumeName "cloned_volume11" -TargetAccessControlRecords $Acrs
VERBOSE: ClientRequestId: 43d8b4dc-39da-4ec5-92f6-be1f499155e9_PS
VERBOSE: ClientRequestId: be7a73a7-980c-4ba2-82d4-f6a7ee0eac0a_PS
VERBOSE: ClientRequestId: ee02aaae-d366-43d2-a229-8761d6db39f1_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 9b81d9f9-3e31-49be-a8cd-1b1c6afdb744_PS
bd05baee-36d0-48f4-8b1e-8119c4133446
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId bd05baee-36d0-48f4-8b1e-8119c4133446 for tracking the job's status
```

Pierwsze polecenie pobiera pierwszą kopię zapasową urządzenia o nazwie ContosoDev07 przy użyciu polecenia cmdlet **Get-AzureStorSimpleDeviceBackup** .
Polecenie zapisuje kopię zapasową w zmiennej $Backup.

Drugie polecenie pobiera rekordy kontroli dostępu przy użyciu polecenia cmdlet **Get-AzureStorSimpleAccessControlRecord** .
Polecenie zapisuje wyniki w zmiennej $Acrs.

Polecenie ostatnie rozpoczyna zadanie, które powiela określoną kopię zapasową woluminu na urządzeniu do innego woluminu na tym samym urządzeniu.
W tym przykładzie określono nazwę urządzenia według nazwy.
W poleceniu są używane wartości przechowywane w $Backup i $Acrs.
Polecenie zwraca identyfikator zadania.

### Przykład 2: klonowanie kopii zapasowej do innego woluminu przy użyciu identyfikatorów urządzeń
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName ContosoDev07 -First 1
PS C:\> $Acrs = Get-AzureStorSimpleAccessControlRecord -ACRName "Acr01"
PS C:\> Start-AzureStorSimpleBackupCloneJob -SourceDeviceId "be7a73a7-980c-4ba2-82d4-f6a7ee0eacbb" -TargetDeviceId "be7a73a7-980c-4ba2-82d4-f6a7ee0eacbb" -BackupId $Backup.InstanceId -Snapshot $Backup.Snapshots[0] -CloneVolumeName "cloned_volume11" -TargetAccessControlRecords $Acrs
VERBOSE: ClientRequestId: 43d8b4dc-39da-4ec5-92f6-be1f499155e9_PS
VERBOSE: ClientRequestId: be7a73a7-980c-4ba2-82d4-f6a7ee0eac0a_PS
VERBOSE: ClientRequestId: ee02aaae-d366-43d2-a229-8761d6db39f1_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 9b81d9f9-3e31-49be-a8cd-1b1c6afdb744_PS
bd05baee-36d0-48f4-8b1e-8119c4133446
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId bd05baee-36d0-48f4-8b1e-8119c4133446 for tracking the job's status
```

Pierwsze polecenie pobiera pierwszą kopię zapasową urządzenia o nazwie ContosoDev07 przy użyciu polecenia cmdlet **Get-AzureStorSimpleDeviceBackup** .
Polecenie zapisuje kopię zapasową w zmiennej $Backup.

Drugie polecenie pobiera rekordy kontroli dostępu przy użyciu polecenia cmdlet **Get-AzureStorSimpleAccessControlRecord** .
Polecenie zapisuje wyniki w zmiennej $Acrs.

Polecenie ostatnie rozpoczyna zadanie, które powiela określoną kopię zapasową woluminu na urządzeniu do innego woluminu na tym samym urządzeniu.
W tym przykładzie określono urządzenie według identyfikatora urządzenia.
W poleceniu są używane wartości przechowywane w $Backup i $Acrs.
Polecenie zwraca identyfikator zadania.

### Przykład 3: klonowanie kopii zapasowej do woluminu na innym urządzeniu przy użyciu nazw urządzeń
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "ContosoDev07" -First 1
PS C:\> $Acrs = Get-AzureStorSimpleAccessControlRecord -ACRName "Acr01"
PS C:\> Start-AzureStorSimpleBackupCloneJob -SourceDeviceName "ContosoDev07" -TargetDeviceName "ContosoDev12" -BackupId $Backup.InstanceId -Snapshot $Backup.Snapshots[0] -CloneVolumeName "cloned_volume11" -TargetAccessControlRecords $Acrs
VERBOSE: ClientRequestId: 43d8b4dc-39da-4ec5-92f6-be1f499155e9_PS
VERBOSE: ClientRequestId: be7a73a7-980c-4ba2-82d4-f6a7ee0eac0a_PS
VERBOSE: ClientRequestId: ee02aaae-d366-43d2-a229-8761d6db39f1_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 9b81d9f9-3e31-49be-a8cd-1b1c6afdb744_PS
bd05baee-36d0-48f4-8b1e-8119c4133446
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId bd05baee-36d0-48f4-8b1e-8119c4133446 for tracking the job's status
```

Pierwsze polecenie pobiera pierwszą kopię zapasową urządzenia o nazwie ContosoDev07 przy użyciu polecenia cmdlet **Get-AzureStorSimpleDeviceBackup** .
Polecenie zapisuje kopię zapasową w zmiennej $Backup.

Drugie polecenie pobiera rekordy kontroli dostępu przy użyciu polecenia cmdlet **Get-AzureStorSimpleAccessControlRecord** .
Polecenie zapisuje wyniki w zmiennej $Acrs.

Polecenie ostatnie rozpoczyna zadanie, które powiela określoną kopię zapasową woluminu na urządzeniu na innym urządzeniu.
W tym przykładzie określono urządzenia według nazwy.
W poleceniu są używane wartości przechowywane w $Backup i $Acrs.
Polecenie zwraca identyfikator zadania.

### Przykład 4: klonowanie kopii zapasowej do innego woluminu przy użyciu nazw urządzeń i operatora potoku
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName ContosoDev1 -First 1
PS C:\> Get-AzureStorSimpleAccessControlRecord -ACRName acr1 | Start-AzureStorSimpleBackupCloneJob -SourceDeviceName ContosoDev1 -TargetDeviceName ContosoDev1 -BackupId $backup.InstanceId -Snapshot $backup.Snapshots[0] -CloneVolumeName "cloned_vol1" 
VERBOSE: ClientRequestId: 1183a29d-63a9-408a-9065-032c92d317ee_PS
VERBOSE: ClientRequestId: e195717c-5920-4133-bdf0-c1201ebabf6f_PS
VERBOSE: ClientRequestId: ac16644d-bfd8-4edf-b1ad-f5df4ceb4df7_PS
VERBOSE: ClientRequestId: dcdcab7f-2aaa-496d-8a18-2e7449a70227_PS
VERBOSE: ClientRequestId: 6f92e422-eda9-4087-aefb-2257a49f5beb_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 646b280c-b51c-4812-b5c5-b7ca215f1c90_PS
a747d2dc-2876-474e-aea6-6546b255427e
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId a747d2dc-2876-474e-aea6-6546b255427e for tracking the job's status
VERBOSE: Access Control Record with given name acr11 is found!
```

Pierwsze polecenie pobiera pierwszą kopię zapasową urządzenia o nazwie ContosoDev07 przy użyciu polecenia cmdlet **Get-AzureStorSimpleDeviceBackup** .
Polecenie zapisuje kopię zapasową w zmiennej $Backup.

Drugie polecenie pobiera rekordy kontroli dostępu przy użyciu polecenia cmdlet **Get-AzureStorSimpleAccessControlRecord** .
Polecenie przekazuje wyniki do bieżącego polecenia cmdlet za pomocą operatora potoku.
Bieżące polecenie cmdlet rozpoczyna zadanie, które sklonowa określoną kopię zapasową woluminu na urządzeniu do innego woluminu na tym samym urządzeniu.
W tym przykładzie określono nazwę urządzenia według nazwy.
W poleceniu użyto wartości przechowywanej w $Backup.
Polecenie pobiera wartość parametru *TargetAccessControlRecords* z rurociągu.
Polecenie zwraca identyfikator zadania.

## PARAMETRÓW

### -BackupId
Określa identyfikator wystąpienia kopii zapasowej do sklonowania.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CloneVolumeName
Określa nazwę nowego sklonowanego woluminu na urządzeniu docelowym.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Określa Profil platformy Azure.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Migawka
Określa obiekt migawki, który jest klonem tego polecenia cmdlet.

```yaml
Type: Snapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SourceDeviceId
Określa identyfikator wystąpienia urządzenia źródłowego.
To polecenie cmdlet powoduje klonowanie z powrotem z urządzenia źródłowego.

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceDeviceName
Określa nazwę urządzenia źródłowego.
To polecenie cmdlet powoduje klonowanie z powrotem z urządzenia źródłowego.

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetAccessControlRecords
Określa rekordy kontroli dostępu.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -TargetDeviceId
Określa identyfikator wystąpienia urządzenia docelowego.

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetDeviceName
Określa nazwę urządzenia, do którego to polecenie cmdlet klonuje kopię zapasową.

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Migawka, lista AccessControlRecord
Do tego polecenia cmdlet można potoku obiekty typu **migawka** lub lista obiektów **AccessControlRecord** .

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureStorSimpleDeviceBackup](./Get-AzureStorSimpleDeviceBackup.md)

[Get-AzureStorSimpleAccessControlRecord](./Get-AzureStorSimpleAccessControlRecord.md)


