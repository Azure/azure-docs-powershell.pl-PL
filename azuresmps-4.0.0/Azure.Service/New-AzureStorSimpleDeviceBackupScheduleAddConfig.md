---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: EE7EC812-640B-4672-B23C-673F912F0EDC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 945d06ddc1be6d2b0864b0421a5a087e14d98218
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054494"
---
# New-AzureStorSimpleDeviceBackupScheduleAddConfig

## STRESZCZENIe
Tworzy obiekt konfiguracji Harmonogram kopii zapasowych.

## POLECENIA

```
New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType <String> -RecurrenceType <String>
 -RecurrenceValue <Int32> -RetentionCount <Int64> [-StartFromDateTime <String>] -Enabled <Boolean>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureStorSimpleDeviceBackupScheduleAddConfig** tworzy obiekt konfiguracji **BackupScheduleBase** .
Ten obiekt konfiguracji służy do tworzenia nowych zasad tworzenia kopii zapasowych przy użyciu polecenia cmdlet **New-AzureStorSimpleDeviceBackupPolicy** .

## Przykłady

### Przykład 1. Tworzenie kopii zapasowej obiektu konfiguracji
```
PS C:\>New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType CloudSnapshot -RecurrenceType Daily -RecurrenceValue 1 -RetentionCount 100 -Enabled $True
VERBOSE: ClientRequestId: 426a79ee-fed3-4d3d-9123-e371f83222b3_PS


BackupType     : CloudSnapshot
Recurrence     : Microsoft.WindowsAzure.Management.StorSimple.Models.ScheduleRecurrence
RetentionCount : 100
StartTime      : 2014-12-16T00:37:19+05:30
Status         : Enabled
```

To polecenie tworzy obiekt bazowy harmonogramu kopii zapasowej dla kopii zapasowych migawek w chmurze.
Kopia zapasowa jest wykonywana codziennie, a kopie zapasowe są zachowywane przez 100 dni.
Ten harmonogram jest włączony od domyślnego czasu, który jest bieżącą godziną.

## PARAMETRÓW

### -Backuptype
Określa typ kopii zapasowej.
Prawidłowe wartości to: LocalSnapshot oraz CloudSnapshot.

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

### -Enabled
Wskazuje, czy włączyć harmonogram wykonywania kopii zapasowych.

```yaml
Type: Boolean
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

### -Recurrencetypetype
Określa typ cyklu dla tego harmonogramu kopii zapasowej.
Prawidłowe wartości: 

- Minut
- Godzinowego
- Dobow
- Weekly

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

### -RecurrenceValue
Określa, jak często ma być wykonywane wykonywanie kopii zapasowej.
W tym parametrze jest używana jednostka określona przez parametr *cykliczntype* .

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RetentionCount
Określa liczbę dni, przez które mają być zachowywane kopie zapasowe.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartFromDateTime
Określa datę, od której należy zacząć tworzenie kopii zapasowych.
Wartość domyślna to bieżąca godzina.

```yaml
Type: String
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

### BackupScheduleBase
To polecenie cmdlet zwraca obiekt **BackupScheduleBase** .
Utwórz nowe zasady tworzenia kopii zapasowych przy użyciu **BackupScheduleBase** .

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzureStorSimpleDeviceBackupScheduleUpdateConfig](./New-AzureStorSimpleDeviceBackupScheduleUpdateConfig.md)

[Nowe — AzureStorSimpleDeviceBackupPolicy](./New-AzureStorSimpleDeviceBackupPolicy.md)


