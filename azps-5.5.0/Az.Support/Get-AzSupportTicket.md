---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
ms.openlocfilehash: 368ae4ad814c9414ea211ea6e44c2d3fbda005f7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182835"
---
# Get-AzSupportTicket

## SYNOPSIS
Uzyskaj bilety pomocy technicznej.

## SKŁADNIA

### ListParameterSet (domyślne)
```
Get-AzSupportTicket [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### GetByNameParameterSet
```
Get-AzSupportTicket -Name <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## OPIS
Pobiera listę biletów pomocy technicznej. Jeśli nie określisz żadnych parametrów, zostaną pobrane wszystkie bilety pomocy technicznej. Możesz również filtrować bilety pomocy technicznej według stanu lub wartości CreatedDate, używając parametru Filtruj. Poniżej przedstawiono kilka przykładów wartości filtru, które można określić.

| Scenariusz                                                         | Filtr                                           |
|------------------------------------------------------------------|--------------------------------------------------|
| Uzyskaj bilety, które są w stanie otwartym                               | "Status eq 'Open'"                               |
| Uzyskaj bilety, które są w stanie zamkniętym                             | "Status eq 'Closed'"                             |
| Uzyskaj bilety utworzone 20 grudnia 2019 r. lub później         | "CreatedDate ge 2019-12-20"                      |
| Uzyskaj bilety utworzone po 20 grudnia 2019 r.               | "CreatedDate gt 2019-12-20"                      |
| Pobiera bilety utworzone po 20 grudnia 2019 r. w stanie otwartym | "CreatedDate gt 2019-12-20 and Status eq 'Open'" |


To polecenie cmdlet obsługuje stronicowanie za pomocą parametrów First (Pierwszy) i Skip (Pomiń).

Możesz również pobrać pojedynczy bilet pomocy technicznej, określając nazwę biletu. 

## PRZYKŁADY

### Przykład 1. Uzyskaj pierwsze 2 bilety
```powershell
PS C:\> Get-AzSupportTicket -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### Przykład 2. Uzyskiwanie pierwszych 2 biletów po pominięciem pierwszych 2 biletów
```powershell
PS C:\> Get-AzSupportTicket -Skip 2 -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test3 test title3                  150010521000314 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test4 test title4                  150010521000315 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### Przykład 3. Uzyskiwanie zgłoszenia do pomocy technicznej według nazwy
```powershell
PS C:\> Get-AzSupportTicket -Name "test1"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
```

### Przykład 4. Uzyskaj pierwsze 2 bilety pomocy technicznej filtrowane według stanu
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Closed'" -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### Przykład 5. Uzyskaj wszystkie bilety pomocy technicznej, które znajdują się w stanie otwartym i zostały utworzone po 20 grudnia 2019 r.
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Open' and CreatedDate gt 2019-12-20"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test6 test title6                  150010521000311 Minimal  Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
test7 test title7                  150010521000312 Minimal  Billing                       Open   2/5/2020 1:33:53 AM
```

## PARAMETERS

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

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

### — Filtr
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

### — Nazwa
Nazwa biletu pomocy technicznej, które otrzymuje to polecenie cmdlet.

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

### - IncludeTotalCount
Raportuje całkowitą liczbę obiektów w zestawie danych (liczbę całkowitą), a po niej zaznaczone obiekty.
Jeśli polecenie cmdlet nie może ustalić łącznej liczby, wyświetla komunikat "Nieznana liczba sum". Liczba całkowita ma właściwość Dokładność, która wskazuje niezawodność wartości łącznej liczby.
Wartość zakresu dokładności wynosi od 0,0 do 1,0, gdzie 0,0 oznacza, że nie można zliczyć obiektów za pomocą polecenia cmdlet, wartość 1,0 oznacza, że liczba jest dokładna, a wartość z przedziału od 0,0 do 1,0 oznacza coraz bardziej niezawodne oszacowanie.

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

### — Pomiń
Ignoruje określoną liczbę obiektów, a następnie pobiera pozostałe obiekty.
Wprowadź liczbę obiektów do pominięcia.

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

### — najpierw
Pobiera tylko określoną liczbę obiektów.
Wprowadź liczbę obiektów do uzyskania.

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Brak

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Support.Models.PSSupportTicket

## NOTATKI

## LINKI POKREWNE
