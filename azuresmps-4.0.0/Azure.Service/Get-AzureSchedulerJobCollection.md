---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 89B28B7C-CA61-4CAB-A4DD-69363AB48A65
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a33739cfad37269fc2f91654e82d6ea36eb2336
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054578"
---
# Get-AzureSchedulerJobCollection

## STRESZCZENIe
Pobiera kolekcje zadań harmonogramu.

## POLECENIA

```
Get-AzureSchedulerJobCollection [-Location <String>] [-JobCollectionName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Opis
W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.
Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .

Polecenie cmdlet **Get-AzureSchedulerJobCollection** pobiera co najmniej jedno kolekcje zadań harmonogramu.

## Przykłady

### Przykład 1. Pobierz wszystkie kolekcje
```
PS C:\> Get-AzureSchedulerJobCollection
```

To polecenie pobiera wszystkie kolekcje zadań harmonogramu we wszystkich lokalizacjach w bieżącej subskrypcji.

### Przykład 2: pobieranie wszystkich kolekcji dla lokalizacji
```
PS C:\> Get-AzureSchedulerJobCollection -Location "North Central US"
```

To polecenie pobiera wszystkie kolekcje zadań harmonogramu w lokalizacji o nazwie My Central Północna.

### Przykład 3: uzyskiwanie kolekcji przy użyciu nazwy
```
PS C:\> Get-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01"
```

To polecenie pobiera kolekcję zadań harmonogramu o nazwie JobCollection01.

## PARAMETRÓW

### -JobCollectionName
Określa nazwę kolekcji zadań harmonogramu do pobrania.

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
Prawidłowe wartości: 

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzureSchedulerJobCollection](./New-AzureSchedulerJobCollection.md)

[Remove-AzureSchedulerJobCollection](./Remove-AzureSchedulerJobCollection.md)

[Set-AzureSchedulerJobCollection](./Set-AzureSchedulerJobCollection.md)


