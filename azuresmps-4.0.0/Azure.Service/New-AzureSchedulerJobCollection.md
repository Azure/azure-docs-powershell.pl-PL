---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: DF12406D-894C-4732-95EE-D75524023B82
online version: ''
schema: 2.0.0
ms.openlocfilehash: c2e6596c0de702175927f51bfd70fc5271b13bfd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054946"
---
# New-AzureSchedulerJobCollection

## STRESZCZENIe
Tworzy kolekcję zadań harmonogramu.

## POLECENIA

```
New-AzureSchedulerJobCollection -Location <String> -JobCollectionName <String> [-Plan <String>]
 [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Opis
W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.
Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .

Polecenie cmdlet **New-AzureSchedulerJobCollection** tworzy kolekcję zadań harmonogramu.
Jeśli nie określisz wartości parametru *Plan* , polecenie cmdlet utworzy standardową kolekcję zadań.

## Przykłady

### Przykład 1. Tworzenie kolekcji zadań harmonogramu zawierającej wartości domyślne
```
PS C:\> New-AzureSchedulerJobCollection -JobCollectionName "JobCollection01" -Location "North Central US" -Plan "Standard"
```

To polecenie tworzy standardową kolekcję zadań harmonogramu o nazwie JobCollection01.
Nowa kolekcja zawiera domyślną liczbę zadań i maksymalny cykl dla kolekcji zadań harmonogramu standardowego.

### Przykład 2: Tworzenie kolekcji zadań harmonogramu z określonymi wartościami
```
PS C:\> New-AzureSchedulerJobCollection -JobCollectionName "JobCollection02" -Location "North Central US" -Frequency "Hour" -Interval 12 -MaxJobCount 30 -Plan "Standard"
```

To polecenie tworzy standardową kolekcję zadań harmonogramu o nazwie JobCollection02.
Nowa kolekcja zawiera maksymalną liczbę zadań 30 i maksymalnie 12 godzin.

## PARAMETRÓW

### -Częstotliwość
Określa maksymalną częstotliwość, jaką można określić na dowolnym stanowisku w tej kolekcji zadań harmonogramu.

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

### -Interval
Określa interwał cyklu z częstotliwością określoną przy użyciu parametru *częstotliwości* .

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

### -JobCollectionName
Określa nazwę nowej kolekcji zadań harmonogramu.

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

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxJobCount
Określa maksymalną liczbę zadań, które można utworzyć w kolekcji zadań harmonogramu.

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

### -Plan
Określa plan kolekcji zadań harmonogramu.

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

[Get-AzureSchedulerJobCollection](./Get-AzureSchedulerJobCollection.md)

[Remove-AzureSchedulerJobCollection](./Remove-AzureSchedulerJobCollection.md)

[Set-AzureSchedulerJobCollection](./Set-AzureSchedulerJobCollection.md)


