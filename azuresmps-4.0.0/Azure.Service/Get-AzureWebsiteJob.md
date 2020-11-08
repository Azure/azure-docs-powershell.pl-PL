---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6B406310-287F-4BD3-BA38-A9C97E8EDC45
online version: ''
schema: 2.0.0
ms.openlocfilehash: d9f68ca1667e7b028c7646bf5a569e4e467c1b03
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055239"
---
# Get-AzureWebsiteJob

## STRESZCZENIe
Pobiera zadania sieci Web skojarzone z witryną internetową.

## POLECENIA

```
Get-AzureWebsiteJob [-JobName <String>] [-JobType <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Pobiera zadania sieci Web skojarzone z witryną internetową.

## Przykłady

### Przykład 1: uzyskiwanie szczegółowych informacji o zadaniach w sieci Web
```
PS C:\> Get-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob
```

Pobiera zadanie sieci Web o nazwie MyWebJob z gniazda produkcyjnego witryny Moja witryna.

### Przykład 2: pobieranie wszystkich zadań w sieci Web dla witryny sieci Web
```
PS C:\> Get-AzureWebsiteJob -Name MyWebsite
```

Pobiera wszystkie zadania sieci Web skojarzone z miejscem produkcyjnym witryny Moja witryna.

### Przykład 3: pobieranie wszystkich wyzwolonych zadań w sieci Web
```
PS C:\> Get-AzureWebsiteJob -Name MyWebsite -Slot staging -Type Triggered
```

Pobiera wszystkie wyzwolone zadania sieci Web z miejsca przemieszczenia witryny Moja witryna.

## PARAMETRÓW

### -JobName
Nazwa zadania w sieci Web

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

### -JobType
Typ zadania sieci Web.
Dopuszczalne wartości tego parametru to:

- Wyzwolon
- Stałego

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

### -Name (nazwa)
Nazwa witryny sieci Web usługi Azure.

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

### -Slot
Nazwa gniazda witryny sieci Web usługi Azure.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureWebsite](./Get-AzureWebsite.md)

[Nowe — AzureWebsiteJob](./New-AzureWebsiteJob.md)

[Remove-AzureWebsiteJob](./Remove-AzureWebsiteJob.md)

[Start — AzureWebsiteJob](./Start-AzureWebsiteJob.md)

[Zatrzymaj — AzureWebsiteJob](./Stop-AzureWebsiteJob.md)


