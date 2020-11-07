---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 70d8ded2b2954746a97d6144f33c043c27341da4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710674"
---
# New-AzsScaleUnitNodeObject

## STRESZCZENIe
Dane wejściowe umożliwiające dodanie węzła jednostki skali.

## POLECENIA

```
New-AzsScaleUnitNodeObject [[-BMCIPv4Address] <String>] [[-ComputerName] <String>] [<CommonParameters>]
```

## Opis
Dane wejściowe umożliwiające dodanie węzła jednostki skali.

## Przykłady

### --------------------------PRZYKŁAD 1--------------------------
```
New-AzsScaleUnitNodeObject -BMCIPv4Address 192.168.1.1 -ComputeName 'NodeName'
```

Tworzenie nowego obiektu węzła.

## PARAMETRÓW

### -BMCIPv4Address
Adres BMC komputera fizycznego.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ComputerName
Nazwa komputera fizycznego.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
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

