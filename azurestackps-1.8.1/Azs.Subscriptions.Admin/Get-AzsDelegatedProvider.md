---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: afc99afebed095da96d826918cc6912f197d1899
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93890026"
---
# Get-AzsDelegatedProvider

## STRESZCZENIe
Pobierz listę delegatedProviders.

## POLECENIA

### Lista (domyślna)
```
Get-AzsDelegatedProvider [<CommonParameters>]
```

### Pobierz
```
Get-AzsDelegatedProvider [-DelegatedProviderId] <Guid> [<CommonParameters>]
```

## Opis
Pobierz listę delegatedProviders.

## Przykłady

### --------------------------PRZYKŁAD 1--------------------------
```
Get-AzsDelegatedProvider
```

Uzyskaj listę dostawców delegowanych.

### --------------------------PRZYKŁAD 2--------------------------
```
Get-AzsDelegatedProvider -DelegatedProviderId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

Uzyskiwanie określonego dostawcy delegowanego.

## PARAMETRÓW

### -DelegatedProviderId
{{Fill DelegatedProviderId Description}}

```yaml
Type: Guid
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

### Microsoft. AzureStack. Management. Subscriptions. admin. modele. Subscription

## INFORMACYJN

## LINKI POKREWNE

