---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
ms.openlocfilehash: 368ae4ad814c9414ea211ea6e44c2d3fbda005f7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491149"
---
# Get-AzSupportTicket

## STRESZCZENIe
Uzyskaj bilety na pomoc techniczną.

## POLECENIA

### ListParameterSet (domyślny)
```
Get-AzSupportTicket [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### GetByNameParameterSet
```
Get-AzSupportTicket -Name <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## Opis
Pobiera listę biletów pomocy technicznej. Jeśli nie określisz żadnych parametrów, wszystkie bilety pomocy technicznej zostaną pobrane. Możesz również filtrować bilety obsługi według statusu lub polach CreatedDate za pomocą parametru Filter. Poniżej przedstawiono kilka przykładów wartości filtru, które można określić.

| Scenariusz                                                         | Filtru                                           |
|------------------------------------------------------------------|--------------------------------------------------|
| Uzyskiwanie biletów z otwartym stanem                               | "Status eq" Otwórz ""                               |
| Uzyskiwanie biletów w stanie zamkniętym                             | "Stan EQ" zamknięty "                             |
| Pobierz bilety utworzone w dniu 20 grudnia 2019 lub później         | "Polach CreatedDate GE 2019-12-20"                      |
| Pobierz bilety utworzone po 20 grudnia 2019 r.               | "Polach CreatedDate gt 2019-12-20"                      |
| Pobiera bilety utworzone po 20 grudnia 2019ch w stanie Open (Otwórz). | "Polach CreatedDate gt 2019-12-20 and status eq" "Open" |


To polecenie cmdlet obsługuje stronicowanie za pomocą pierwszych i pomijanych parametrów.

Możesz również pobrać jeden bilet pomocy technicznej, podając nazwę biletu. 

## Przykłady

### Przykład 1: Uzyskaj pierwszych 2 bilety
```powershell
PS C:\> Get-AzSupportTicket -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### Przykład 2: Uzyskaj pierwsze 2 bilety po pominięciu pierwszego 2.
```powershell
PS C:\> Get-AzSupportTicket -Skip 2 -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test3 test title3                  150010521000314 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test4 test title4                  150010521000315 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### Przykład 3: uzyskiwanie biletu pomocy technicznej według nazwy
```powershell
PS C:\> Get-AzSupportTicket -Name "test1"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
```

### Przykład 4: Uzyskaj pierwszych 2 bilety pomocy technicznej filtrowane według statusu
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Closed'" -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### Przykład 5: Uzyskaj wszystkie bilety pomocy technicznej, które są w stanie otwartym, i utworzono po 20 grudnia 2019 r.
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Open' and CreatedDate gt 2019-12-20"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test6 test title6                  150010521000311 Minimal  Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
test7 test title7                  150010521000312 Minimal  Billing                       Open   2/5/2020 1:33:53 AM
```

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

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

### -Filter
Filtr, który ma zostać zastosowany do wyników tego polecenia cmdlet.

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Nazwa biletu pomocy technicznej, który jest pobierany przez to polecenie cmdlet.

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeTotalCount
Wyświetla całkowitą liczbę obiektów w zbiorze danych (liczba całkowita), a następnie zaznaczone obiekty.
Jeśli polecenie cmdlet nie może ustalić całkowitej liczby, zostanie wyświetlona "Łączna liczba nieznanych". Liczba całkowita ma właściwość dokładność wskazującą wiarygodność całkowitej wartości licznika.
Wartość zakresu dokładności od 0,0 do 1,0 w przypadku, gdy 0,0 oznacza, że nie można zliczyć obiektów przez polecenie cmdlet, 1,0 oznacza, że liczba jest dokładna, a wartość między 0,0 a 1,0 wskazuje coraz bardziej niezawodny szacunek.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Skip
Ignoruje określoną liczbę obiektów, a następnie pobiera pozostałe obiekty.
Wprowadź liczbę obiektów, które mają zostać pominięte.

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -First
Pobiera tylko określoną liczbę obiektów.
Wprowadź liczbę obiektów do pobrania.

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### Znaleziono

## WYSYŁA

### Microsoft. Azure. Commands. support. models. PSSupportTicket

## INFORMACYJN

## LINKI POKREWNE
