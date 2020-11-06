---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: e233c523e5fd9372b1e7dd86b5b5e73eb3f7091e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523413"
---
# Disable-AzureRmDataCollection

## STRESZCZENIe
Nie możesz zbierać danych, aby ulepszyć polecenia cmdlet usługi AzurePowerShell. Dane nie są zbierane, jeśli użytkownik wyraźnie nie zrezygnuje.

## POLECENIA

```
Disable-AzureRmDataCollection [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Możesz ulepszyć środowisko korzystania z usługi Microsoft Cloud i Azure PowerShell, wybierając do kolekcji danych.
Program Azure PowerShell nie gromadzi danych bez zgody użytkownika — należy wyraźnie włączyć, wykonując polecenie Włącz-AzureRmDataCollection lub odpowiedzi tak, gdy program Azure PowerShell wyświetli monit o zbieranie danych przy pierwszym uruchomieniu polecenia cmdlet.
Firma Microsoft gromadzi zebrane dane w celu zidentyfikowania wzorców użytkowania w celu zidentyfikowania typowych problemów i usprawnienia korzystania z usługi Azure PowerShell.
Program Microsoft Azure PowerShell nie gromadzi żadnych danych prywatnych ani żadnych informacji umożliwiających identyfikację użytkownika.

Uruchom polecenie cmdlet Disable-AzureRMDataCollection, aby wyłączyć zbieranie danych dla bieżącego użytkownika.
Zapobiegnie to monitowaniu bieżącego użytkownika o zbieranie danych przy pierwszym uruchomieniu poleceń cmdlet.

Aby włączyć zbieranie danych dla bieżącego użytkownika, uruchom polecenie cmdlet Enable-AzureRmDataCollection.

## Przykłady

### Przykład 1: wyłączanie zbierania danych dla bieżącego użytkownika
```
PS C:\> Disable-AzureRmDataCollection
```

W tym przykładzie pokazano, jak wyłączyć zbieranie danych dla bieżącego użytkownika. 

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

[Enable-AzureRmDataCollection]()

