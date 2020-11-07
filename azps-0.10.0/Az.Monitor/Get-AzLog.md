---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzLog.md
ms.openlocfilehash: f6000574313942c774c9243d9a4d4a42caa28820
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891194"
---
# Get-AzLog

## STRESZCZENIe
Pobieranie zdarzeń dziennika aktywności.

## POLECENIA

### GetByCorrelationId
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceId
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceGroup
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-ResourceGroupName] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByResourceProvider
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetBySubscription
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzLog** pobiera zdarzenia dziennika aktywności.
Zdarzenia można kojarzyć z bieżącym IDENTYFIKATORem subskrypcji, IDENTYFIKATORem korelacji, grupą zasobów, IDENTYFIKATORem zasobu lub dostawcą zasobów.

## Przykłady

### Przykład 1: uzyskiwanie dziennika zdarzeń według identyfikatora subskrypcji
```
PS C:\>Get-AzLog
```

To polecenie zawiera listę najwyżej 1000 zdarzeń skojarzonych z IDENTYFIKATORem abonamentu użytkownika, który nastąpił 7 dni od bieżącej daty/godziny.

### Przykład 2: uzyskiwanie dziennika zdarzeń według identyfikatora subskrypcji z maksymalną liczbą zdarzeń
```
PS C:\>Get-AzLog -MaxRecord 100
```

To polecenie zawiera listę najwyżej 100 zdarzeń skojarzonych z IDENTYFIKATORem abonamentu użytkownika, który nastąpił 7 dni od bieżącej daty/godziny.

### Przykład 3: uzyskiwanie dziennika zdarzeń według identyfikatora subskrypcji z godziną rozpoczęcia.
```
PS C:\>Get-AzLog -StartTime 2017-06-01T10:30
```

To polecenie wyświetla listę najwyżej 1000 zdarzeń skojarzonych z IDENTYFIKATORem abonamentu użytkownika, który miał miejsce w dniu lub po cenie 2017 – 06-01T10:30 czas lokalny, jeśli ta data/godzina nie jest starsza niż 90 dni od bieżącej daty/godziny.

### Przykład 4: uzyskiwanie dziennika zdarzeń według identyfikatora abonamentu z godziną rozpoczęcia i godziną zakończenia.
```
PS C:\>Get-AzLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

To polecenie wyświetla najwyżej 1000 zdarzeń skojarzonych z IDENTYFIKATORem abonamentu użytkownika, który miał miejsce w dniu lub po dniu 2017 – 04 – 01T10:30 czas lokalny, a przed 2017em – 04 – 14T11:30 czas lokalny, jeśli cały zakres daty/godziny nie jest wcześniejszy niż 90 dni od bieżącej daty/godziny, czyli okres przechowywania.

### Przykład 5: uzyskiwanie dziennika zdarzeń według identyfikatora korelacji
```
PS C:\>Get-AzLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

To polecenie wyświetla listę najwyżej 1000 zdarzeń skojarzonych z określonym IDENTYFIKATORem korelacji, który nastąpił 7 dni od bieżącej daty/godziny. 
**Uwaga** : jest to zwykle tylko jedno zdarzenie.

### Przykład 6: uzyskiwanie dziennika zdarzeń według identyfikatora korelacji z maksymalną liczbą zdarzeń
```
PS C:\>Get-AzLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxRecord 100
```

To polecenie wyświetla listę najwyżej 100 zdarzeń skojarzonych z określonym IDENTYFIKATORem korelacji, który nastąpił 7 dni od bieżącej daty/godziny. 
**Uwaga** : jest to zwykle tylko jedno zdarzenie.

### Przykład 7: uzyskiwanie dziennika zdarzeń według identyfikatora korelacji i godziny rozpoczęcia
```
PS C:\>Get-AzLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

To polecenie wyświetla listę najwyżej 1000 zdarzeń skojarzonych z określonym IDENTYFIKATORem korelacji, który miał miejsce w dniu lub po cenie 2017-05-22T04:30:00 czas lokalny, jeśli godzina rozpoczęcia nie jest wcześniejsza niż 90 dni od bieżącej daty/godziny.
**Uwaga** : jest to zwykle tylko jedno zdarzenie.

### Przykład 8: uzyskiwanie dziennika zdarzeń według identyfikatora korelacji z godziną rozpoczęcia i godziną zakończenia
```
PS C:\>Get-AzLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

To polecenie wyświetla listę najwyżej 1000 zdarzeń skojarzonych z określonym IDENTYFIKATORem korelacji, który miał miejsce w dniu lub po cenie 2017 – 04 – 15T04:30 czas lokalny, ale przed 2017-04 – 25T12:30 czas lokalny, jeśli cały zakres daty/godziny nie jest wcześniejszy niż 90 dni od bieżącej daty/godziny, czyli okres przechowywania.

### Przykład 9: uzyskiwanie dziennika zdarzeń dla grupy zasobów
```
PS C:\>Get-AzLog -ResourceGroupName "Contoso-Web-CentralUS"
```

To polecenie wyświetla najwyżej 1000 zdarzeń skojarzonych z określoną grupą zasobów, które miały miejsce w ciągu 7 dni od bieżącej daty/godziny.

### Przykład 10: uzyskiwanie dziennika zdarzeń dla grupy zasobów z maksymalną liczbą zdarzeń
```
PS C:\>Get-AzLog -ResourceGroup "Contoso-Web-CentralUS" -MaxRecord 100
```

To polecenie wyświetla listę najwyżej 100 zdarzeń skojarzonych z określoną grupą zasobów, które miały miejsce 7 dni od bieżącej daty/godziny.

### Przykład 11: pobieranie dziennika zdarzeń dla grupy zasobów według czasu rozpoczęcia
```
PS C:\>Get-AzLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

To polecenie wyświetla listę najwyżej 1000 zdarzeń skojarzonych z określoną grupą zasobów, które miały miejsce w dniu lub po cenie 2017-05-22T04:30:00 czas lokalny, jeśli godzina rozpoczęcia nie jest wcześniejsza niż 90 dni od bieżącej daty/godziny.

### Przykład 12: pobieranie dziennika zdarzeń dla grupy zasobów z godziną rozpoczęcia i godziną zakończenia
```
PS C:\>Get-AzLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

To polecenie wyświetla listę najwyżej 1000 zdarzeń skojarzonych z określoną grupą zasobów, które miały miejsce w dniu lub po cenie 2017 – 04 – 15T04:30 czas lokalny, ale przed 2017em – 04 – 25T12:30 czas lokalny, jeśli cały zakres dat/godzin nie jest wcześniejszy niż 90 dni od bieżącej daty/godziny, czyli okres przechowywania.

### Przykład 13: uzyskiwanie dziennika zdarzeń według identyfikatora zasobu
```
PS C:\>Get-AzLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

To polecenie wyświetla listę najwyżej 1000 zdarzeń skojarzonych z określonym IDENTYFIKATORem zasobu, który miał miejsce 7 dni od bieżącej daty/godziny.

### Przykład 14: uzyskiwanie dziennika zdarzeń według identyfikatora zasobu z maksymalną liczbą zdarzeń
```
PS C:\>Get-AzLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxRecord 100
```

To polecenie wyświetla listę najwyżej 100 zdarzeń skojarzonych z określonym IDENTYFIKATORem zasobu, który miał miejsce 7 dni od bieżącej daty/godziny.

### Przykład 15: uzyskiwanie dziennika zdarzeń według identyfikatora zasobu z godziną rozpoczęcia
```
PS C:\>Get-AzLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

To polecenie wyświetla listę najwyżej 1000 zdarzeń skojarzonych z określonym IDENTYFIKATORem zasobu, który miał miejsce w dniu lub po cenie 2017-05-22T04:30:00 czas lokalny, jeśli godzina rozpoczęcia nie jest wcześniejsza niż 90 dni od bieżącej daty/godziny.

### Przykład 16: uzyskiwanie dziennika zdarzeń według identyfikatora zasobu z godziną rozpoczęcia i godziną zakończenia
```
PS C:\>Get-AzLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

To polecenie wyświetla listę najwyżej 1000 zdarzeń skojarzonych z określonym IDENTYFIKATORem zasobu, który miał miejsce w dniu lub po dniu 2017 – 04 – 15T04:30 czas lokalny, ale przed 2017-04 – 25T12:30 czas lokalny, jeśli cały zakres dat/godzin nie jest wcześniejszy niż 90 dni od bieżącej daty/godziny, czyli okres przechowywania.

### Przykład 17: uzyskiwanie dziennika zdarzeń według dostawcy zasobów
```
PS C:\>Get-AzLog -ResourceProvider "Microsoft.Web"
```

To polecenie wyświetla listę najwyżej 1000 zdarzeń skojarzonych z określonym dostawcą zasobów, który miał miejsce 7 dni od bieżącej daty/godziny.

### Przykład 18: uzyskiwanie dziennika zdarzeń przez dostawcę zasobów z maksymalną liczbą zdarzeń
```
PS C:\>Get-AzLog -ResourceProvider "Microsoft.Web" -MaxRecord 100
```

To polecenie wyświetla listę najwyżej 100 zdarzeń skojarzonych z określonym dostawcą zasobów, który miał miejsce 7 dni od bieżącej daty/godziny.

### Przykład 19: uzyskiwanie dziennika zdarzeń przez dostawcę zasobów przy użyciu godziny rozpoczęcia
```
PS C:\>Get-AzLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

To polecenie wyświetla listę najwyżej 1000 zdarzeń skojarzonych z określonym dostawcą zasobów, który miał miejsce w dniu lub po cenie 2017-05-22T04:30:00 czas lokalny, jeśli godzina rozpoczęcia nie jest wcześniejsza niż 90 dni od bieżącej daty/godziny.

### Przykład 20: uzyskiwanie dziennika zdarzeń przez dostawcę zasobów z godziną rozpoczęcia i godziną zakończenia
```
PS C:\>Get-AzLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

To polecenie wyświetla listę najwyżej 1000 zdarzeń skojarzonych z określonym dostawcą zasobów, który miał miejsce w dniu lub po dniu 2017 – 04 – 15T04:30 czas lokalny, ale przed 2017-04 – 25T12:30 czas lokalny, jeśli cały zakres dat/godzin nie jest wcześniejszy niż 90 dni od bieżącej daty/godziny, czyli okres przechowywania.

## PARAMETRÓW

### — Rozmówca
Określa rozmówcę.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Identyfikator korelacji
Określa identyfikator korelacji.
Ten parametr jest wymagany.

```yaml
Type: System.String
Parameter Sets: GetByCorrelationId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

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

### -DetailedOutput
Wskazuje, że w tym poleceniu cmdlet są wyświetlane szczegółowe dane wyjściowe.
Domyślnie dane wyjściowe są sumowane.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Switch not present = False, i.e. output summarized
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EndTime
Określa godzinę zakończenia kwerendy w czasie lokalnym.
Wartość domyślna to bieżąca godzina.
Wartość musi być późniejsza niż czas *rozpoczęcia*.
Możesz użyć polecenia cmdlet Get-Date, aby uzyskać obiekt **DateTime** .

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Current date (time: 00:00:00 AM) + 1 day
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxRecord
Określa całkowitą liczbę rekordów do pobrania dla określonego filtru.
Wartość domyślna to 1000, a maksymalna akceptowana wartość to 100000. Wartości ujemne i 0 są ignorowane i zostanie wykorzystana wartość domyślna.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1000
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Określa identyfikator zasobu.

```yaml
Type: System.String
Parameter Sets: GetByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceProvider
Określa filtr według dostawcy zasobów.

```yaml
Type: System.String
Parameter Sets: GetByResourceProvider
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StartTime
Określa godzinę rozpoczęcia kwerendy w czasie lokalnym.
Wartość domyślna to *Endtime* minus siedem dni.
Możesz użyć polecenia cmdlet Get-Date, aby uzyskać obiekt **DateTime** .

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: EndTime - 7 days
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Status
Określa stan.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### System. Nullable "1 [[System. DateTime, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]

### System. String

### System. Management. Automation. SwitchParameter

### System. Int32

## WYSYŁA

### Microsoft. Azure. Commands. Insights. OutputClasses. PSEventData

## INFORMACYJN

## LINKI POKREWNE
