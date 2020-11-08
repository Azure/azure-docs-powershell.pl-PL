---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: EFAE7117-9B8B-4CB9-B4D9-3F08DCE1816E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 405b9d427c7e59dfb3628806a878d57a281a6b4e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055174"
---
# New-AzureStorSimpleDeviceBackupPolicy

## STRESZCZENIe
Tworzy zasady tworzenia kopii zapasowych.

## POLECENIA

```
New-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicyName <String>
 -BackupSchedulesToAdd <PSObject[]> -VolumeIdsToAdd <PSObject[]> [-WaitForComplete] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureStorSimpleDeviceBackupPolicy** tworzy zasady tworzenia kopii zapasowych.
Zasady tworzenia kopii zapasowej zawierają co najmniej jeden harmonogram kopii zapasowych, który może być uruchomiony w jednym lub większej liczbie woluminów.
Aby utworzyć harmonogram wykonywania kopii zapasowych, użyj polecenia cmdlet **New-AzureStorSimpleDeviceBackupScheduleAddConfig** .

## Przykłady

### Przykład 1. Tworzenie zasad tworzenia kopii zapasowych
```
PS C:\>$Schedule01 = New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType LocalSnapshot -RecurrenceType Daily -RecurrenceValue 10 -RetentionCount 5 -Enabled $True
PS C:\> $Schedule02 = New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType CloudSnapshot -RecurrenceType Hourly -RecurrenceValue 1 -RetentionCount 5 -Enabled $True
PS C:\> $ScheduleArray = @()
PS C:\> $ScheduleArray += $Schedule01
PS C:\> $ScheduleArray += $Schedule02
PS C:\> $DeviceContainer = Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm"
PS C:\> $Volume = $(Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeContainer $DeviceContainer[0])
PS C:\> $VolumeArray = @()
PS C:\> $VolumeArray += $Volume[0].InstanceId
PS C:\> New-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyName "GeneralPolicy07" -BackupSchedulesToAdd $ScheduleArray -VolumeIdsToAdd $VolumeArray
VERBOSE: ClientRequestId: e9d6771e-c323-47b9-b424-cb98f8ed0273_PS
VERBOSE: ClientRequestId: db0e7c86-d0d2-4a5a-b1cb-182494cba027_PS
VERBOSE: ClientRequestId: 77708dfd-a386-4999-b7ed-5d53e288ae83_PS


JobId        : d4ce5340-d5d1-4471-9cc8-013193f021b3
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your add operation has completed successfully. 
VERBOSE: ClientRequestId: bbf7e9b9-b493-40b3-8348-f15bcfc4da8a_PS
BackupSchedules          : {36d21096-bbd1-47b7-91b5-40ad1792d992, 505fc91f-deb5-4dca-bfcb-98c20b75ebcc}
Volumes                  : {volume03}
BackupPolicyCreationType : BySaaS
LastBackup               : 01-01-2010 05:30:00
NextBackup               : 16-12-2014 01:13:43
SchedulesCount           : 2
SSMHostName              : 
VolumesCount             : 1
InstanceId               : 8799c2f0-8850-4e91-aa23-ee18c67da8bd
Name                     : GeneralPolicy07
OperationInProgress      : None
```

Pierwsze polecenie tworzy obiekt konfiguracji Harmonogram kopii zapasowych przy użyciu polecenia cmdlet **New-AzureStorSimpleDeviceBackupScheduleAddConfig** , a następnie zapisuje ten obiekt w zmiennej $Schedule 01.

Drugie polecenie tworzy inny obiekt konfiguracji kopii zapasowej przy użyciu polecenia **New-AzureStorSimpleDeviceBackupScheduleAddConfig** , a następnie zapisuje ten obiekt w zmiennej $Schedule 02.

W trzecim poleceniu jest tworzona pusta zmienna tablicowa o nazwie $ScheduleArray.
Następne dwa polecenia dodają obiekty utworzone w pierwszych dwóch poleceniach do $ScheduleArray.

Szóste polecenie pobiera kontener woluminowy dla urządzenia o nazwie Contoso63-AppVm przy użyciu polecenia cmdlet **Get-AzureStorSimpleDeviceVolumeContainer** , a następnie zapisuje ten obiekt kontenera w zmiennej $DeviceContainer.

Po siódmym poleceniu jest pobierany wolumin kontenera woluminu przechowywanego w pierwszym członku $DeviceContainer przy użyciu polecenia cmdlet **Get-AzureStorSimpleDeviceVolume** , a następnie zapisanie tego woluminu w zmiennej $Volume.

W przypadku ósmego polecenia zostanie utworzona pusta zmienna tablicowa o nazwie $VolumeArray.
Polecenie Next (następne) dodaje identyfikator woluminu do $VolumeArray.
Ta wartość identyfikuje wolumin przechowywany w $Volume, na którym są uruchamiane zasady tworzenia kopii zapasowych.
Możesz dodać kolejne identyfikatory woluminów do $VolumeArray.

Ostatnie polecenie tworzy zasady tworzenia kopii zapasowych o nazwie GeneralPolicy07 dla urządzenia o nazwie Contoso63-AppVm.
To polecenie Określa obiekty konfiguracji harmonogramu przechowywane w $ScheduleArray.
Polecenie określa wolumin lub woluminy, do których mają być stosowane zasady, w $VolumeArray.
Zasady tworzenia kopii zapasowych można zweryfikować przy użyciu polecenia cmdlet **Get-AzureStorSimpleDeviceBackupPolicy** .

## PARAMETRÓW

### -BackupPolicyName
Określa nazwę zasad tworzenia kopii zapasowych.

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

### -BackupSchedulesToAdd
Określa tablicę obiektów **BackupScheduleBase** , które należy dodać do zasad.
Każdy obiekt przedstawia harmonogram.
Zasady tworzenia kopii zapasowej zawierają jeden lub więcej harmonogramów.
Aby uzyskać obiekt **BackupScheduleBase** , użyj polecenia cmdlet **New-AzureStorSimpleDeviceBackupScheduleAddConfig** .

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName
Określa nazwę urządzenia StorSimple, na którym należy utworzyć zasady tworzenia kopii zapasowych.

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

### -VolumeIdsToAdd
Określa tablicę identyfikatorów woluminów dodawanych do zasad tworzenia kopii zapasowych.

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WaitForComplete
Wskazuje, że przed zwróceniem kontroli na konsolę programu Windows PowerShell to polecenie cmdlet oczekuje na ukończenie operacji.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono

## WYSYŁA

### BackupPolicy
To polecenie cmdlet zwraca obiekt **BackupPolicy** , który zawiera nowe harmonogramy i woluminy.

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureStorSimpleDeviceBackupPolicy](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[Get-AzureStorSimpleDeviceVolume](./Get-AzureStorSimpleDeviceVolume.md)

[Get-AzureStorSimpleDeviceVolumeContainer](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[Remove-AzureStorSimpleDeviceBackupPolicy](./Remove-AzureStorSimpleDeviceBackupPolicy.md)

[Set-AzureStorSimpleDeviceBackupPolicy](./Set-AzureStorSimpleDeviceBackupPolicy.md)

[Nowe — AzureStorSimpleDeviceBackupScheduleAddConfig](./New-AzureStorSimpleDeviceBackupScheduleAddConfig.md)


