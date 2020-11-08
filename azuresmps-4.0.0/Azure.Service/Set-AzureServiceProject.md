---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D0A2B454-7BFF-4D4D-8A85-FDB47249758F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5f4d1598f17629d178e1feff1b5549631be48c60
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054785"
---
# Set-AzureServiceProject

## STRESZCZENIe
Ustawia domyślną lokalizację, subskrypcję, gniazdo i konto magazynu dla bieżącej usługi.

## POLECENIA

```
Set-AzureServiceProject [-Location <String>] [-Slot <String>] [-Storage <String>] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzureServiceProject** ustawia lokalizację wdrożenia, gniazdo, konto magazynu i abonament dla bieżącej usługi.
Te wartości są używane podczas publikowania usługi w chmurze.

## Przykłady

### Przykład 1: Ustawienia podstawowe
```
PS C:\> Set-AzureServiceProject -Location "North Central US" -Slot Production -Storage myStorageAccount -Subscription myAzureSubscription
```

Ustawia lokalizację wdrożenia usługi na Północno-środkowe region w Stanach Zjednoczonych.
Ustawia miejsce wdrożenia na produkcję. Ustawia konto magazynu, które będzie używane do przemieszczenia definicji usługi na myStorageAccount.
Ustawia subskrypcję, która będzie hostem usługi na stronie Moja subskrypcja.
Po opublikowaniu usługi w chmurze będzie ona hostowana w centrum danych w regionie północ w Stanach Zjednoczonych, a to spowoduje zaktualizowanie miejsca wdrożenia, a następnie użyje określonego konta abonamentu i magazynu.

## PARAMETRÓW

### — Lokalizacja
Region, w którym usługa będzie hostowana.
Ta wartość jest używana podczas publikowania usługi w chmurze.
Możliwe wartości: wszędzie tam, gdzie w Europie, na całym świecie, w Stanach Zjednoczonych, Wschodniej, Wschodniej, północno-zachodnim świecie, na północno-wschodnim świecie, w USA, Azji Południowo – Wschodniej, Europa Zachodnia.

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

### -PassThru
Wskazuje, że to polecenie cmdlet zwraca obiekt reprezentujący element, na którym działa.
Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.

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
Miejsce (produkcja lub przemieszczanie), w którym usługa będzie hostowana.
Ta wartość jest używana podczas publikowania usługi w chmurze.
Możliwe wartości: produkcja, przemieszczanie.

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

### -Storage
Konto magazynu, które ma być używane podczas przekazywania pakietu usługi do chmury.
Jeśli konto magazynu nie istnieje, zostanie utworzone po opublikowaniu usługi w chmurze.

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
* węzły — dev, php — dev, Python — dev

## LINKI POKREWNE

[Nowe — AzureServiceProject](./New-AzureServiceProject.md)

[Publikowanie — AzureServiceProject](./Publish-AzureServiceProject.md)

[Set-AzureServiceProjectRole](./Set-AzureServiceProjectRole.md)


