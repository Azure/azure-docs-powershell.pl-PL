---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8EED9813-5106-4D6C-B869-97BCBD7845AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67e354616161ad7f2d2467a37b92c355c7c8c39e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055277"
---
# Get-AzureSchedulerJob

## STRESZCZENIe
Pobiera listę zadań harmonogramu lub określonego zadania harmonogramu.

## POLECENIA

```
Get-AzureSchedulerJob -Location <String> -JobCollectionName <String> [-JobName <String>] [-JobState <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.
Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .

Polecenie cmdlet **Get-AzureSchedulerJobCollection** pobiera listę zadań harmonogramu lub określonego zadania harmonogramu.

## Przykłady

### Przykład 1. pobieranie wszystkich zadań w kolekcji
```
PS C:\> Get-AzureSchedulerJob -Location "North Central US" -JobCollectionName "JobCollection01"
```

To polecenie pobiera zadania harmonogramu, które są częścią kolekcji zadań o nazwie JobCollection01.

### Przykład 2: pobieranie nazwanego zadania
```
PS C:\> Get-AzureSchedulerJob -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job01"
```

To polecenie pobiera zadanie o nazwie Job01 z kolekcji o nazwie JobCollection01 w określonej lokalizacji.

### Przykład 3: uzyskiwanie wyłączonych zadań w kolekcji
```
PS C:\> Get-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01" -JobState "Disabled"
```

To polecenie pobiera wszystkie wyłączone zadania harmonogramu, które są częścią JobCollection01 w określonej lokalizacji.

## PARAMETRÓW

### -JobCollectionName
Określa nazwę kolekcji zawierającej zadanie harmonogramu do pobrania.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -JobName
Określa nazwę zadania harmonogramu, które ma zostać pozyskane.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -JobState
Określa stan zadań harmonogramu do pobrania.
Dopuszczalne wartości tego parametru to:

- Wyłączona
- Łącza
- Błąd
- Zakończyć

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Lokalizacja
Określa nazwę lokalizacji, w której znajduje się usługa chmury.
Dopuszczalne wartości tego parametru to:

- W dowolnym miejscu w Azji
- Dowolne miejsce w Europie
- Dowolne miejsce w USA
- Azja Wschodnia
- Wschodnie USA
- Północno-środkowe USA
- Europa Północna
- Południowa Centrala amerykańska
- Azja Południowo-Wschodnia
- Europa Zachodnia
- Zachodnie USA

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Remove-AzureSchedulerJob](./Remove-AzureSchedulerJob.md)


