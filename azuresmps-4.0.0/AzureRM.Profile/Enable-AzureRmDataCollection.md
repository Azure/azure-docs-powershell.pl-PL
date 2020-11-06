---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 678e08df94d7ea828b04d55892cb66e1c0a62349
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523409"
---
# Enable-AzureRmDataCollection

## STRESZCZENIe
Umożliwia zbieranie danych w celu usprawnienia środowiska użytkownika za pomocą poleceń cmdlet usługi AzurePowerShell.
Wykonanie tego polecenia cmdlet umożliwia zbieranie danych dla bieżącego użytkownika na bieżącym komputerze.
Nie są zbierane żadne dane, o ile użytkownik wyraźnie nie zrezygnuje.

## POLECENIA

```
Enable-AzureRmDataCollection [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Możesz ulepszyć środowisko korzystania z usługi Microsoft Cloud i Azure PowerShell, wybierając do kolekcji danych.
Program Azure PowerShell nie gromadzi danych bez zgody użytkownika — należy wyraźnie włączyć, wykonując polecenie Włącz-AzureRmDataCollection lub odpowiedzi tak, gdy program Azure PowerShell wyświetli monit o zbieranie danych przy pierwszym uruchomieniu polecenia cmdlet.
Firma Microsoft gromadzi zebrane dane w celu zidentyfikowania wzorców użytkowania w celu zidentyfikowania typowych problemów i usprawnienia korzystania z usługi Azure PowerShell.
Program Microsoft Azure PowerShell nie gromadzi żadnych danych prywatnych ani żadnych informacji umożliwiających identyfikację użytkownika.

Uruchom polecenie cmdlet Enable-AzureRMDataCollection, aby włączyć zbieranie danych dla bieżącego użytkownika na bieżącym komputerze.
Zapobiegnie to monitowaniu bieżącego użytkownika o zbieranie danych przy pierwszym uruchomieniu poleceń cmdlet.

Aby wyłączyć zbieranie danych dla bieżącego użytkownika, uruchom polecenie cmdlet Disable-AzureRmDataCollection.

## Przykłady

### Przykład 1: Włączanie zbierania danych dla bieżącego użytkownika
```
PS C:\> Enable-AzureRmDataCollection
```

W tym przykładzie pokazano, jak włączyć zbieranie danych dla bieżącego użytkownika.

## PARAMETRÓW

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet. Polecenie cmdlet nie jest uruchamiane.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### Znaleziono

## INFORMACYJN

## LINKI POKREWNE

[Disable-AzureRmDataCollection]()

