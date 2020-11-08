---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D4349562-1392-44B6-9353-6231F0CB5C51
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66618c0a684a8e54d41bbe4014ee1e6c893acdbf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055094"
---
# Remove-AzureSchedulerJobCollection

## STRESZCZENIe
Usuwa kolekcję zadań harmonogramu.

## POLECENIA

```
Remove-AzureSchedulerJobCollection [-Force] [-Location <String>] -JobCollectionName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.
Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .

Polecenie cmdlet **Remove-AzureSchedulerJobCollection** usuwa kolekcję zadań harmonogramu i wszystkie zadania w ramach tej kolekcji.

## Przykłady

### Przykład 1: usuwanie kolekcji zadań dla lokalizacji
```
PS C:\> Remove-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01"
```

To polecenie usuwa kolekcję zadań harmonogramu o nazwie JobCollection01 w Północnej, centralnej lokalizacji.
Polecenie usuwa również zadania w obszarze JobCollection01.

### Przykład 2: usuwanie lokalizacji zadania
```
PS C:\> Remove-AzureSchedulerJobCollection -JobCollectionName "JobCollection02"
```

To polecenie usuwa kolekcję zadań harmonogramu o nazwie JobCollection02.
Polecenie usuwa również zadania w obszarze JobCollection02.

## PARAMETRÓW

### -Force
Wskazuje, że to polecenie cmdlet usunie kolekcję zadań harmonogramu bez monitowania o potwierdzenie.

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

### -JobCollectionName
Określa nazwę kolekcji zadań harmonogramu do usunięcia.

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

[Nowe — AzureSchedulerJobCollection](./New-AzureSchedulerJobCollection.md)

[Set-AzureSchedulerJobCollection](./Set-AzureSchedulerJobCollection.md)


