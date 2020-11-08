---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportticketcommunication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
ms.openlocfilehash: 07a8747f94f9c1fb93bbff06ce855363088a67a0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224132"
---
# Get-AzSupportTicketCommunication

## STRESZCZENIe
Uzyskaj pomoc na temat przekazu biletów pomocy technicznej.

## POLECENIA

### GetByNameParameterSet (domyślny)
```
Get-AzSupportTicketCommunication -SupportTicketName <String> [-Name <String>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

### GetByParentObjectParameterSet
```
Get-AzSupportTicketCommunication [-Name <String>] -SupportTicketObject <PSSupportTicket> [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

## Opis
Pobiera komunikat o pomocy technicznej. Jeśli nie określisz żadnych innych parametrów, otrzymasz całą wiadomość dla biletu. Możesz również filtrować komunikację według polach CreatedDate lub Communicationtype przy użyciu parametru Filter. Poniżej przedstawiono kilka przykładów wartości filtru, które można określić.


| Scenariusz                                                        | Filtru                                                     |
|-----------------------------------------------------------------|------------------------------------------------------------|
| Uzyskiwanie komunikacji w sieci Web                                          | "Internettype EQ" "                               |
| Uzyskiwanie komunikacji telefonicznej                                        | "Telefon komunikacyjny" EQ "                             |
| Uzyskiwanie wiadomości utworzonych w dniu 20 grudnia 2019 lub później | "Polach CreatedDate GE 2019-12-20"                                |
| Pobierz komunikację utworzoną po 20 grudnia 2019 r.       | "Polach CreatedDate gt 2019-12-20"                                |
| Pobiera wiadomości internetowe utworzone po 20 grudnia 2019 r.            | "Polach CreatedDate gt 2019-12-20 and Communicationtype EQ" Web ' " |


To polecenie cmdlet obsługuje stronicowanie za pomocą pierwszych i pomijanych parametrów.

Możesz również pobrać pojedynczą komunikację biletów pomocy technicznej, podając nazwę komunikacji. 

## Przykłady

### Przykład 1: pobieranie całej komunikacji za pomocą biletu pomocy technicznej
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
```

### Przykład 2: pobieranie pojedynczej komunikacji za pomocą nazwy dla biletu pomocy technicznej
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Name "testmessage1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage1 user@contoso.com     test message   2/4/2020 9:38:14 PM
```

### Przykład 3: pobieranie pierwszych 2 wiadomości na bilet pomocy technicznej
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### Przykład 4: pobieranie następnej 2 wiadomości po pominięciu pierwszych 2 wiadomości w przypadku biletu pomocy technicznej
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Skip 2 -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage4 user@contoso.com     test message4  2/4/2020 9:38:14 PM
testmessage5 user@contoso.com     test message5  2/4/2020 9:36:36 PM
```

### Przykład 5: pobieranie wszystkich wiadomości w sieci Web dla biletu pomocy technicznej
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web'"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### Przykład 6: pobieranie wszystkich wiadomości utworzonych w dniu lub po 20 grudnia 2019 dla biletu pomocy technicznej
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### Przykład 7: pobieranie całej komunikacji w sieci Web utworzonej w dniu lub po 20 grudnia 2019 r. na bilet pomocy technicznej
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web' and CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### Przykład 8: pobieranie całej komunikacji dla biletu pomocy technicznej przez obiekt biletu pomocy technicznej dla połączeń rurowych
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Get-AzSupportTicketCommunication

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
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
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Nazwa komunikacji.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SupportTicketName
Nazwa biletu pomocy technicznej.

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

### -SupportTicketObject
Obiekt biletu pomocy technicznej.

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSSupportTicket
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### Microsoft. Azure. Commands. support. models. PSSupportTicket

## WYSYŁA

### Microsoft. Azure. Commands. support. models. PSSupportTicketCommunication

## INFORMACYJN

## LINKI POKREWNE
