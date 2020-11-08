---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7317DAC1-B535-4650-86BF-73E96F61EECD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 23bb8e09fac8ec4fe0e8ff5b3c23ab995f03694c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055157"
---
# New-AzureVMSqlServerAutoPatchingConfig

## STRESZCZENIe
Tworzy obiekt konfiguracji do automatycznego tworzenia poprawek maszyny wirtualnej.

## POLECENIA

```
New-AzureVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureVMSqlServerAutoPatchingConfig** tworzy obiekt konfiguracji do automatycznego tworzenia poprawek maszyny wirtualnej.

## Przykłady

### Przykład 1. Tworzenie obiektu konfiguracji w celu skonfigurowania automatycznej poprawki
```
PS C:\> $APS = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
          Enable                        : True
          DayOfWeek                     : Thursday
          MaintenanceWindowStartingHour : 11
          MaintenanceWindowDuration     : 120
          PatchCategory                 : Important
```

To polecenie tworzy obiekt konfiguracji, którego można użyć w celu skonfigurowania automatycznej poprawki za pomocą polecenia Set-AzureVMSqlServerExtension.

## PARAMETRÓW

### -DayOfWeek
Określa dzień tygodnia, w którym powinny być instalowane aktualizacje.

Dopuszczalne wartości tego parametru to:

- Niedziele
- Poniedziałek
- Wtorku
- Środa
- Czwartek
- Poniedziałek
- Sobota
- Codzienne

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

### -Enable
Wskazuje, że automatyczne poprawianie maszyny wirtualnej jest włączone.
Jeśli włączysz automatyczne poprawianie, polecenie cmdlet spowoduje przejście systemu Windows do trybu interakcyjnego.
Jeśli wyłączysz automatyczne stosowanie, ustawienia Windows Update nie zmienią się.

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

### -InformationAction
Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.

Dopuszczalne wartości tego parametru to:

- Kontynuacj
- Ignorować
- Inquire
- SilentlyContinue
- Przestaw
- Wykonywanie

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Określa zmienną informacyjną.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaintenanceWindowDuration
Określa czas trwania okna obsługi.
Automatyczne poprawianie spowoduje uniknięcie wykonania akcji, która może wpływać na dostępność maszyny wirtualnej poza tym oknem.
Dozwolone są tylko 30 minut.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaintenanceWindowStartingHour
Określa godzinę dnia, kiedy zostanie uruchomione okno konserwacja.
Ten czas określa, kiedy aktualizacje rozpoczynają instalację i są zaokrąglane do godziny.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PatchCategory
Określa, czy należy uwzględnić ważne aktualizacje.

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

## WYSYŁA

### AutoPatchingSettings
To polecenie cmdlet zwraca obiekt zawiera ustawienia automatycznej poprawki.

## INFORMACYJN

## LINKI POKREWNE

[Set-AzureVMSqlServerExtension](./Set-AzureVMSqlServerExtension.md)

[Remove-AzureVMSqlServerExtension](./Remove-AzureVMSqlServerExtension.md)

[Set-AzureVMSqlServerExtension](./Set-AzureVMSqlServerExtension.md)


