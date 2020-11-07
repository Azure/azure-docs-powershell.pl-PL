---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d3c564a004c006a9fd77c6fb5cef034b402b0b1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888234"
---
# Get-AzsNetworkAdminOverview

## STRESZCZENIe
Zapoznaj się z omówieniem stanu dostawcy zasobów sieciowych.

## POLECENIA

```
Get-AzsNetworkAdminOverview [<CommonParameters>]
```

## Opis
Zapoznaj się z omówieniem stanu dostawcy zasobów sieciowych. Poszczególne właściwości zapewniają szczegółowe zliczanie użycia zasobów i kondycji według składników.

## Przykłady

### --------------------------PRZYKŁAD 1--------------------------
```
Get-AzsNetworkAdminOverview
```

Zapoznanie się z omówieniem administratora sieci.

### --------------------------PRZYKŁAD 2--------------------------
```
(Get-AzsNetworkAdminOverview).PublicIpAddressUsage
```

Uzyskaj publiczne użycie adresu IP.

## PARAMETRÓW

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### Microsoft. AzureStack. Management. Network. admin. models. AdminOverview

## INFORMACYJN

## LINKI POKREWNE

