---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0fa95e34c6a220a496a79f7a72c65c222f1376f1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055787"
---
# Get-AzsGalleryItem

## STRESZCZENIe
Wyświetla elementy galerii.

## POLECENIA

### Lista (domyślna)
```
Get-AzsGalleryItem [<CommonParameters>]
```

### Pobierz
```
Get-AzsGalleryItem [-Name] <String> [<CommonParameters>]
```

## Opis
Uzyskiwanie listy elementów galerii dostępnych w witrynie Azure Stack platform

## Przykłady

### PRZYKŁAD 1
```
Get-AzsGalleryItem
```

Elementy galerii list.

### PRZYKŁAD 2
```
Get-AzsGalleryItem -Name 'microsoft.vmss.1.3.6'
```

Uzyskaj element galerii według nazwy.

## PARAMETRÓW

### -Name (nazwa)
Tożsamość elementu galerii.
Zawiera nazwę wydawcy, nazwę elementu i może zawierać wersję rozdzieloną znakiem kropki.

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### Microsoft. AzureStack. Management. Gallery. admin. models. GalleryItem

## INFORMACYJN

## LINKI POKREWNE
