---
external help file: Microsoft.Azure.PowerShell.Cmdlets.UsageAggregates.dll-Help.xml
Module Name: Az.Billing
ms.assetid: 52B3ECCB-80E5-4E16-954A-B83D0BDC7E22
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-usageaggregates
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Billing/Billing/help/Get-UsageAggregates.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Billing/Billing/help/Get-UsageAggregates.md
ms.openlocfilehash: 510d0ee001e4c291dad3cc024f593d1f29c7ddca
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890137"
---
# Get-UsageAggregates

## STRESZCZENIe
Pobiera zgłoszone dane dotyczące użycia subskrypcji usługi Azure.

## POLECENIA

```
Get-UsageAggregates -ReportedStartTime <DateTime> -ReportedEndTime <DateTime>
 [-AggregationGranularity <AggregationGranularity>] [-ShowDetails <Boolean>] [-ContinuationToken <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-UsageAggregates** pobiera zagregowane dane użycia subskrypcji platformy Azure według następujących właściwości: 
- Godziny rozpoczęcia i zakończenia użytkowania, które zostały zgłoszone.
- Precyzja agregacji — codziennie lub co godzinę.
- Szczegóły poziomu wystąpienia dla wielu wystąpień tego samego zasobu.
W przypadku spójnych wyników zwracanych danych zależy od tego, kiedy dane o użyciu zostały zgłoszone przez zasób platformy Azure.
Aby uzyskać więcej informacji, zobacz informacje o interfejsie API usługi zaliczenia Azure https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c ( https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) w bibliotece Microsoft Developer Network).

## Przykłady

### Przykład 1: pobieranie danych subskrypcji
```
PS C:\>Get-UsageAggregates -ReportedStartTime "5/2/2015" -ReportedEndTime "5/5/2015"
```

To polecenie pobiera zgłoszone dane dotyczące użycia subskrypcji między 5/2/2015 a 5/5/2015.

## PARAMETRÓW

### -AggregationGranularity
Określa dokładność agregacji danych.
Prawidłowe wartości to: codziennie i co godzinę.
Wartość domyślna to codziennie.

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
Określa token kontynuacji, który został pobrany z treści odpowiedzi w poprzedniej rozmowie.
W przypadku dużego zestawu wyników odpowiedzi są stronicowane przy użyciu tokenów kontynuacji.
Token kontynuacji służy jako Zakładka do postępu.
Jeśli ten parametr nie jest określony, dane są pobierane od początku dnia lub godziny określonej w *ReportedStartTime*.
Zalecamy, aby w przypadku tych danych obserwować łącze dalej na stronie Odpowiedz na.

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

### -ReportedEndTime
Określa raportowaną godzinę zakończenia użycia zasobów w systemie rozliczeń Azure.
Platforma Azure jest systemem rozproszonym, obejmującym wiele centrów danych na całym świecie, dlatego istnieje opóźnienie między rzeczywistym użyciem zasobu, czyli czasem użycia zasobów, a kiedy zdarzenie użycia osiągnęło system rozliczeń, czyli czas raportowania użycia zasobów.
W celu uzyskania wszystkich zdarzeń użycia dla subskrypcji zgłaszanych przez okres, zbadasz zapytanie według zgłoszonego czasu.
Mimo że kwerenda została zgłoszona przez zgłoszony czas, polecenie cmdlet agreguje dane odpowiedzi przez czas użycia zasobów.
Dane dotyczące użycia zasobów to przydatny sposób na analizowanie danych.

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
Określa zgłoszony czas rozpoczęcia, po zapisaniu użycia zasobów w systemie rozliczeń Azure.

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

### -ShowDetails
Wskazuje, czy to polecenie cmdlet zwraca szczegóły na poziomie wystąpienia przy użyciu danych użycia.
Wartość domyślna to $True.
Jeśli $False, usługa agreguje wyniki po stronie serwera i w związku z tym zwraca mniej grup agregacji.
Jeśli na przykład korzystasz z trzech witryn internetowych, domyślnie otrzymasz trzy elementy wiersza, aby można było skorzystać z witryny sieci Web.
Jeśli jednak wartość jest $False, wszystkie dane dla tego samego identyfikatora **subskrypcji** , **meterId** , **usageStartTime** i **usageEndTime** są zwijane w jeden element linii.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono

## WYSYŁA

### Microsoft. Azure. Commerce. UsageAggregates. MODELES. UsageAggregationGetResponse

## INFORMACYJN

## LINKI POKREWNE