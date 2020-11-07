---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
ms.openlocfilehash: 1a68b5ca391e6c09673f07f0469035e0f96c1562
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704771"
---
# Enable-AzDataCollection

## STRESZCZENIe
Umożliwia zbieranie danych w celu usprawnienia środowiska użytkownika za pomocą poleceń cmdlet usługi AzurePowerShell.
Wykonanie tego polecenia cmdlet umożliwia zbieranie danych dla bieżącego użytkownika na bieżącym komputerze.
Nie są zbierane żadne dane, o ile użytkownik wyraźnie nie zrezygnuje.

## POLECENIA

```
Enable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Możesz ulepszyć środowisko korzystania z usługi Microsoft Cloud i Azure PowerShell, wybierając do kolekcji danych.
Program Azure PowerShell nie gromadzi danych bez zgody użytkownika — należy wyraźnie włączyć, wykonując polecenie Włącz-AzDataCollection lub odpowiedzi tak, gdy program Azure PowerShell wyświetli monit o zbieranie danych przy pierwszym uruchomieniu polecenia cmdlet.
Firma Microsoft gromadzi zebrane dane w celu zidentyfikowania wzorców użytkowania w celu zidentyfikowania typowych problemów i usprawnienia korzystania z usługi Azure PowerShell.
Program Microsoft Azure PowerShell nie gromadzi żadnych danych prywatnych ani żadnych informacji umożliwiających identyfikację użytkownika.
Uruchom polecenie cmdlet Enable-AzDataCollection, aby włączyć zbieranie danych dla bieżącego użytkownika na bieżącym komputerze.
Zapobiegnie to monitowaniu bieżącego użytkownika o zbieranie danych przy pierwszym uruchomieniu poleceń cmdlet.
Aby wyłączyć zbieranie danych dla bieżącego użytkownika, uruchom polecenie cmdlet Disable-AzDataCollection.

## Przykłady

### Przykład 1: Włączanie zbierania danych dla bieżącego użytkownika
```
PS C:\> Enable-AzDataCollection
```

W tym przykładzie pokazano, jak włączyć zbieranie danych dla bieżącego użytkownika.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawca i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
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

### Znaleziono

## WYSYŁA

### System. void

## INFORMACYJN

## LINKI POKREWNE

[Disable-AzDataCollection](./Disable-AzDataCollection.md)

