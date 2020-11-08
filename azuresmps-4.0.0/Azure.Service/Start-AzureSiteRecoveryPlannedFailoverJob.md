---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2575F5C4-A276-49CE-AB0C-726F359DA6F9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7f71138e47c851097fe36ca294784fc571b6369f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054717"
---
# Start-AzureSiteRecoveryPlannedFailoverJob

## STRESZCZENIe
Rozpoczyna operację planowanej pracy awaryjnej odzyskiwania witryny.

## POLECENIA

### ByRPId (domyślny)
```
Start-AzureSiteRecoveryPlannedFailoverJob -RPId <String> -Direction <String> [-WaitForCompletion]
 [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByPEId
```
Start-AzureSiteRecoveryPlannedFailoverJob -ProtectionEntityId <String> -ProtectionContainerId <String>
 -Direction <String> [-WaitForCompletion] [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByRPObject
```
Start-AzureSiteRecoveryPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-WaitForCompletion] [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByPEObject
```
Start-AzureSiteRecoveryPlannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-WaitForCompletion] [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Start-AzureSiteRecoveryPlannedFailoverJob** rozpoczyna planowaną pracę w trybie failover dla jednostki ochrony usługi Azure Site Recovery lub planu odzyskiwania.
Możesz sprawdzić, czy zadanie powiodło się przy użyciu polecenia cmdlet **Get-AzureSiteRecoveryJob** .

## Przykłady

### Przykład 1. uruchomienie planowanego zadania w trybie failover
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer 
PS C:\> $Protected = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container 
PS C:\> Start-AzureSiteRecoveryPlannedFailoverJob -Direction PrimaryToRecovery -ProtectionEntity $Protected -Optimize ForDowntime
ID               : c38eecdc-731c-405b-a61c-08db99aae2fe
ClientRequestId  : 32ace403-0916-4967-83a1-529176bd6e88-2014-49-06 15:49:24Z-P
State            : NotStarted
StateDescription : NotStarted
StartTime        : 
EndTime          : 
AllowedActions   : {}
Name             : 
Tasks            : {}
Errors           : {}
```

Pierwsze polecenie pobiera wszystkie chronione kontenery w bieżącym magazynie usługi Azure Site Recovery, korzystając z polecenia cmdlet **Get-AzureSiteRecoveryProtectionContainer** , a następnie zapisuje wyniki w zmiennej $Container.
W tym przykładzie istnieje jeden kontener.

Drugie polecenie pobiera chronione maszyny wirtualne należące do kontenera przechowywanego w $Container przy użyciu polecenia cmdlet **Get-AzureSiteRecoveryProtectionEntity** .
Polecenie zapisuje wyniki w zmiennej $Protected.

Ostatnie polecenie uruchamia zadanie przejęcia awaryjnego w kierunku PrimaryToRecovery dla chronionych maszyn wirtualnych przechowywanych w $Protected.

## PARAMETRÓW

### -Direction
Określa kierunek pracy awaryjnej.
Dopuszczalne wartości tego parametru to:

- PrimaryToRecovery
- RecoveryToPrimary

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

### — Optymalizuj
Określa, do czego należy zoptymalizować.
Ten parametr dotyczy trybu failover z witryny platformy Azure w witrynie lokalnej, która wymaga znacznej synchronizacji danych.
Dopuszczalne wartości tego parametru to:

- ForDowntime
- ForSynchronization

Gdy jest określony **ForDowntime** , oznacza to, że dane są synchronizowane przed przejściem w tryb pracy awaryjnej w celu zminimalizowania przestojów.
Synchronizacja jest przeprowadzana bez zamykania maszyny wirtualnej.
Po zakończeniu synchronizacji zadanie zostaje zawieszone.
Wznów zadanie, aby wykonać dodatkową operację synchronizacji, która zamyka maszynę wirtualną.

Gdy jest określony **ForSynchronization** , oznacza to, że dane są synchronizowane podczas pracy awaryjnej tylko wtedy, gdy synchronizacja danych jest zminimalizowana.
Ponieważ to ustawienie jest włączone, maszyna wirtualna jest natychmiast zamykana.
Synchronizacja rozpoczyna się po zamknięciu, aby ukończyć operację przełączania awaryjnego.

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

### -ProtectionContainerId
Określa identyfikator chronionego kontenera, dla którego ma zostać uruchomione zadanie.

```yaml
Type: String
Parameter Sets: ByPEId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProtectionEntity
Określa obiekt jednostki ochrony przed odzyskiwaniem witryny.

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ProtectionEntityId
Określa obiekt **ASRProtectionEntity** , dla którego ma zostać uruchomione zadanie.
Aby uzyskać obiekt **ASRProtectionEntity** , użyj polecenia cmdlet **Get-AzureSiteRecoveryProtectionEntity** .

```yaml
Type: String
Parameter Sets: ByPEId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryPlan
Określa obiekt planu odzyskiwania.

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RPId
Określa identyfikator planu odzyskiwania, dla którego ma zostać uruchomione zadanie.

```yaml
Type: String
Parameter Sets: ByRPId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WaitForCompletion
Wskazuje, że polecenie cmdlet oczekuje na zakończenie operacji przed zwróceniem sterowania do konsoli programu Windows PowerShell.

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

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureSiteRecoveryProtectionContainer](./Get-AzureSiteRecoveryProtectionContainer.md)

[Get-AzureSiteRecoveryProtectionEntity](./Get-AzureSiteRecoveryProtectionEntity.md)


