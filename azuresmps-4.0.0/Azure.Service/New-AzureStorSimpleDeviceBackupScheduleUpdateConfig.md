---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 22C6845E-D7BD-4BBC-B373-394A23488A94
online version: ''
schema: 2.0.0
ms.openlocfilehash: a0695dc42d9c540e30ddf9ac55bd6fc136c84bff
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054490"
---
# New-AzureStorSimpleDeviceBackupScheduleUpdateConfig

## STRESZCZENIe
Umożliwia utworzenie obiektu konfiguracji Planowanie kopii zapasowej.

## POLECENIA

```
New-AzureStorSimpleDeviceBackupScheduleUpdateConfig -Id <String> -BackupType <String> -RecurrenceType <String>
 -RecurrenceValue <Int32> -RetentionCount <Int64> [-StartFromDateTime <String>] [-Enabled <Boolean>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** tworzy obiekt konfiguracji **BackupScheduleUpdateRequest** .
Ten obiekt konfiguracji służy do aktualizowania zasad tworzenia kopii zapasowych przy użyciu polecenia cmdlet **Set-AzureStorSimpleDeviceBackupPolicy** .

## Przykłady

### Przykład 1: Tworzenie żądania aktualizacji harmonogramu
```
PS C:\>New-AzureStorSimpleDeviceBackupScheduleUpdateConfig -Id "147f734d-a31a-4473-8501-6ba38be2cb30" -BackupType CloudSnapshot -RecurrenceType Hourly -RecurrenceValue 1 -RetentionCount 50 -Enabled $True
VERBOSE: ClientRequestId: ef346641-54b4-4273-8898-7f863e7c5b7e_PS


BackupType     : CloudSnapshot
Id             : 147f734d-a31a-4473-8501-6ba38be2cb30
Recurrence     : Microsoft.WindowsAzure.Management.StorSimple.Models.ScheduleRecurrence
RetentionCount : 50
StartTime      : 2014-12-16T00:39:32+05:30
Status         : Enabled
```

To polecenie tworzy żądanie aktualizacji harmonogramu kopii zapasowej dla harmonogramu o określonym IDENTYFIKATORze.
Żądanie polega na zapełnieniu harmonogramu kopii zapasowej migawki w chmurze, która powtarza się co godzinę.
Kopie zapasowe są zachowywane przez 50 dni.
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

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Określa identyfikator wystąpienia harmonogramu kopii zapasowych do zaktualizowania.

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

### BackupScheduleUpdateRequest
To polecenie cmdlet zwraca obiekt **BackupScheduleUpdateRequest** , który zawiera informacje o zaktualizowanych harmonogramach kopii zapasowych.

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzureStorSimpleDeviceBackupScheduleAddConfig](./New-AzureStorSimpleDeviceBackupScheduleAddConfig.md)

[Set-AzureStorSimpleDeviceBackupPolicy](./Set-AzureStorSimpleDeviceBackupPolicy.md)


