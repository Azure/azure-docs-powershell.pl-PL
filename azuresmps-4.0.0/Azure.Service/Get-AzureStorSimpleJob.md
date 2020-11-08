---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 2001E040-5551-40C3-81D2-9A8334DE02BF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7692d4407df8fb4af8647ee0b4490abe73b2c937
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054524"
---
# Get-AzureStorSimpleJob

## STRESZCZENIe
Pobiera zadania StorSimple.

## POLECENIA

```
Get-AzureStorSimpleJob [-DeviceName <String>] [-InstanceId <String>] [-Status <String>] [-Type <String>]
 [-From <DateTime>] [-To <DateTime>] [-Skip <Int32>] [-First <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureStorSimpleJob** pobiera zadania usługi Azure StorSimple.
Określ identyfikator wystąpienia, aby uzyskać określone zadanie.
Określ inne parametry, aby ograniczyć zadania, które są pobierane przez to polecenie cmdlet.

To polecenie cmdlet zwraca maksymalnie 200 zadań.
Jeśli istnieje więcej niż 200 zadań, Pobierz pozostałe zadania przy użyciu parametrów *pierwszy* i *Pomiń* .
Jeśli określisz wartość 100 dla pozycji *Pomiń* i 50 dla *pierwszego* , to polecenie cmdlet nie zwróci pierwszych 100 wyników.
Zwraca następne 50 wyników po 100, które pominie.

## Przykłady

### Przykład 1: uzyskiwanie zadania przy użyciu identyfikatora
```
PS C:\>Get-AzureStorSimpleJob -InstanceId "574f47e0-44e9-495c-b8a5-0203c57ebf6d"
BackupPolicy             : 
BackupTimeStamp          : 1/1/0001 12:00:00 AM
BackupType               : CloudSnapshot
DataStats                : Microsoft.WindowsAzure.Management.StorSimple.Models.DataStatistics
Device                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
Entity                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
ErrorDetails             : {}
HideProgressDetails      : False
InstanceId               : 574f47e0-44e9-495c-b8a5-0203c57ebf6d
IsInstantRestoreComplete : False
IsJobCancellable         : True
JobDetails               : Microsoft.WindowsAzure.Management.StorSimple.Models.JobStatusInfo
Name                     : 26447caf-59bb-41c9-a028-3224d296c7dc
Progress                 : 100
SourceDevice             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
SourceEntity             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
SourceVolume             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
Status                   : Completed
TimeStats                : Microsoft.WindowsAzure.Management.StorSimple.Models.TimeStatistics
Type                     : Backup
Volume                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
```

To polecenie pobiera informacje dotyczące zadania o określonym IDENTYFIKATORze.

### Przykład 2: pobieranie zadań przy użyciu nazwy urządzenia
```
PS C:\>Get-AzureStorSimpleJob -DeviceName "8600-Bravo 001" -First 2
InstanceId                           Type                         Status                                          DeviceName                                      StartTime                                       Progress                                       
----------                           ----                         ------                                          ----------                                      ---------                                       --------                                       
1997c33f-bfcc-4d08-9aba-28068340a1f9 Backup                       Running                                         8600-Bravo 001                                  4/15/2015 1:30:02 PM                            92                                             
85074062-ef6a-408a-b6c9-2a0904bb99ca Backup                       Completed                                       8600-Bravo 001                                  4/15/2015 1:30:02 PM                            100
```

To polecenie pobiera informacje dotyczące zadań związanych z urządzeniem o nazwie 8600 – Bravo 001.
Polecenie pobiera pierwsze dwa zadania dla urządzenia.

### Przykład 3: pobieranie ukończonych zadań
```
PS C:\>Get-AzureStorSimpleJob -Status "Completed" -Skip 10 -First 2
```

To polecenie pobiera ukończone zadania.
Polecenie pobiera tylko dwa pierwsze zadania po pominięciu pierwszych dziesięciu zadań.

### Przykład 4: pobieranie ręcznych zadań kopii zapasowej
```
PS C:\>Get-AzureStorSimpleJob -Type "ManualBackup"
```

To polecenie pobiera zadania ręcznego typu kopii zapasowej.

### Przykład 5: pobieranie zadań między określonymi godzinami
```
PS C:\>$StartTime = Get-Date -Year 2015 -Month 3 -Day 10
PS C:\> $EndTime = Get-Date -Year 2015 -Month 3 -Day 11 -Hour 12 -Minute 15
PS C:\>Get-AzureStorSimpleJob -DeviceName "Device07" -From $StartTime -To $EndTime
```

Dwa pierwsze polecenia tworzą obiekty **DateTime** przy użyciu Get-Date polecenia cmdlet.
Nowe godziny w $StartTime i $EndTime zmiennych są zapisywane w tych poleceniach.
Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Date` .

Polecenie ostatnie pobiera zadania dla urządzenia o nazwie Device07 między godzinami przechowywanymi w $StartTime i $EndTime.

## PARAMETRÓW

### -DeviceName
Określa nazwę urządzenia StorSimple.

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

### -First
Pobiera tylko określoną liczbę obiektów.
Wprowadź liczbę obiektów do pobrania.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Od
Określa datę i godzinę rozpoczęcia zadań, które są pobierane przez to polecenie cmdlet.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstanceId
Określa identyfikator zadania do pobrania.

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

### -Profile
Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.
Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.

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

### -Skip
Ignoruje określoną liczbę obiektów, a następnie pobiera pozostałe obiekty.
Wprowadź liczbę obiektów, które mają zostać pominięte.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Status
Określa stan.
Dopuszczalne wartości tego parametru to:

- Wykonywania
- Zakończyć
- Anulowania
- Nie powiodło się
- Redukcji
- CompletedWithErrors

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

### -To
Określa datę i godzinę zakończenia zadań, które są pobierane przez to polecenie cmdlet.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type
Określa typ zadania.
Dopuszczalne wartości tego parametru to:

- Wykonania
- ManualBackup
- Przywrócenie
- CloneWorkflow
- DeviceRestore
- Aktualizowane
- SupportPackage
- VirtualApplianceProvisioning

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
Nie możesz popotokować danych wejściowych tego polecenia cmdlet.

## WYSYŁA

### IList \<DeviceJobDetails\> , DeviceJobDetails
To polecenie cmdlet zwraca listę obiektów szczegółów zadania lub, jeśli określisz parametr *InstanceId* , zwróci jeden obiekt szczegółów zadania.

## INFORMACYJN

## LINKI POKREWNE

[Zatrzymaj — AzureStorSimpleJob](./Stop-AzureStorSimpleJob.md)


