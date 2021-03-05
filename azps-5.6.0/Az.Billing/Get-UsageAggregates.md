---
external help file: Microsoft.Azure.PowerShell.Cmdlets.UsageAggregates.dll-Help.xml
Module Name: Az.Billing
ms.assetid: 52B3ECCB-80E5-4E16-954A-B83D0BDC7E22
online version: https://docs.microsoft.com/powershell/module/az.billing/get-usageaggregates
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-UsageAggregates.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-UsageAggregates.md
ms.openlocfilehash: 1947b060f6b1d2fcf7e4380d3a1ece808ea29785
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988492"
---
# Get-UsageAggregates

## SYNOPSIS
Otrzymuje zgłoszone szczegóły użycia subskrypcji platformy Azure.

## SKŁADNIA

```
Get-UsageAggregates -ReportedStartTime <DateTime> -ReportedEndTime <DateTime>
 [-AggregationGranularity <AggregationGranularity>] [-ShowDetails <Boolean>] [-ContinuationToken <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-UsageAggregates** pobiera zagregowane dane użycia subskrypcji platformy Azure przez następujące właściwości: 
- Godziny rozpoczęcia i zakończenia zgłoszonych użycia.
- Dokładność agregacji: dzienna lub godzinowa.
- Szczegóły poziomu wystąpienia dla wielu wystąpień tego samego zasobu.
Aby uzyskać spójne wyniki, zwracane dane są oparte na tym, kiedy szczegóły użycia zostały zgłoszone przez zasób platformy Azure.
Aby uzyskać więcej informacji, zobacz informacje dotyczące interfejsu API rest rozliczeń platformy Azure https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) (w bibliotece Microsoft Developer Network).

## PRZYKŁADY

### Przykład 1. Pobieranie danych subskrypcji
```
PS C:\>Get-UsageAggregates -ReportedStartTime "5/2/2015" -ReportedEndTime "5/5/2015"
```

To polecenie pobiera zgłoszone dane użycia dla subskrypcji między 2015-05-02 a 2015-05-05.

## PARAMETERS

### -AggregationGranularity
Określa dokładność agregacji danych.
Prawidłowe wartości to: Codziennie i Co godzinę.
Wartość domyślna to Dzienny.

```yaml
Type: Microsoft.Azure.Commerce.UsageAggregates.Models.AggregationGranularity
Parameter Sets: (All)
Aliases:
Accepted values: Daily, Hourly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContinuationToken
Określa token kontynuacji, który został pobrany z treści odpowiedzi w poprzednim wywołaniu.
W przypadku dużego zestawu wyników odpowiedzi są stronicowane przy użyciu tokenów kontynuacji.
Token kontynuacji służy jako zakładka do postępu.
Jeśli nie określisz tego parametru, dane są pobierane od początku dnia lub godziny określonego w parametrze *ReportedStartTime.*
Zalecamy skorzystanie z następnego linku w odpowiedzi na stronę z danymi.

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

### -ReportedEndTime
Określa zgłoszony czas zakończenia użycia zasobu zarejestrowany w systemie rozliczeń Azure.
Azure to system rozłożony obejmujący wiele centrów danych na całym świecie, dlatego istnieje opóźnienie między rzeczywistym użyciem zasobu, czyli czasem użycia zasobu, a zdarzeniem użycia osiągnięto system rozliczeń, który jest zgłoszonym czasem użycia zasobu.
Aby uzyskać wszystkie zdarzenia użycia dla subskrypcji, które są raportowany za określony czas, należy zapytać o zgłoszony czas.
Mimo że zapytanie jest zwracane według zgłoszonego czasu, polecenie cmdlet agreguje dane odpowiedzi według czasu użycia zasobu.
Dane użycia zasobów są przydatną tabelą przestawną do analizowania danych.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportedStartTime
Określa zgłoszony czas rozpoczęcia użycia zasobu zarejestrowany w systemie rozliczeń Azure.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - ShowDetails
Wskazuje, czy to polecenie cmdlet zwraca szczegóły na poziomie wystąpienia z danymi użycia.
Wartość domyślna to $True.
Jeśli $False, usługa agreguje wyniki po stronie serwera i dlatego zwraca mniej grup zagregowanych.
Jeśli na przykład używasz trzech witryn sieci Web, domyślnie będziesz otrzymać trzy pozycje do użycia w witrynach internetowych.
Jednak gdy ta wartość jest $False, wszystkie dane dla tego samego elementu **subscriptionId,** **meterId,** **usageStartTime** i **usageEndTime** są zwijane w jeden element wiersza.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Brak

## DANE WYJŚCIOWE

### Microsoft.Azure.Commerce.UsageAggregates.Models.UsageAggregationGetResponse

## NOTATKI

## LINKI POKREWNE
