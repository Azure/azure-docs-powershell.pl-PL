---
external help file: ''
Module Name: Azs.Commerce.Admin
online version: https://docs.microsoft.com/powershell/module/azs.commerce.admin/get-azssubscriberusage
schema: 2.0.0
ms.openlocfilehash: 9eed3f6f2a4d07bd48136c50ec173f801b30c928
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93894045"
---
# Get-AzsSubscriberUsage

## STRESZCZENIe
Pobiera kolekcję SubscriberUsageAggregates, które są UsageAggregates od użytkowników.

## POLECENIA

```
Get-AzsSubscriberUsage -ReportedEndTime <DateTime> -ReportedStartTime <DateTime> [-SubscriptionId <String[]>]
 [-AggregationGranularity <String>] [-ContinuationToken <String>] [-SubscriberId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## Opis
Pobiera kolekcję SubscriberUsageAggregates, które są UsageAggregates od użytkowników.

## Przykłady

### Przykład 1: pobieranie danych użycia zagregowanych według dni
```powershell
Get-AzsSubscriberUsage -ReportedStartTime "2019-12-30T00:00:00Z" -ReportedEndTime "2019-12-31T00:00:00Z" -AggregationGranularity Daily
```

Pobierz dane dotyczące użycia dla całego dnia 30 grudnia 2019 (czas UTC) dla wszystkich dzierżawców w ramach dostawcy zagregowanego przez dany dzień.
ReportedStartTime i ReportedEndTime muszą być zaokrąglone do dni.
Jeśli jest wywoływana jako administrator usługi, w ten sposób przedstawiane są wszystkie dane dotyczące użycia dla każdej dzierżawy.

### Przykład 2: pobieranie danych użycia zagregowanych o godzinie
```powershell
Get-AzsSubscriberUsage -ReportedStartTime "2019-12-30T00:00:00Z" -ReportedEndTime "2019-12-30T02:00:00Z" -AggregationGranularity Hourly
```

Pobierz dane dotyczące użycia między 12am-2AM w 30 Dec 2019 (czas UTC) zagregowanych o godzinie.
ReportedStartTime i ReportedEndTime muszą być zaokrąglane do godzin.
Podobnie, jeśli jest wywoływana jako administrator usługi, w ten sposób wszystkie dane dotyczące użycia dla każdej dzierżawy są wyświetlane w ten sposób.

## PARAMETRÓW

### -AggregationGranularity
Stopień szczegółowości agregacji.

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

### -ContinuationToken
Token kontynuacji.

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
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -ReportedEndTime
Zgłoszona godzina zakończenia (z wyłączeniem).

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
Zgłoszona godzina rozpoczęcia (włącznie).

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

### -SubscriberId
Identyfikator subskrypcji dzierżawy.

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

### -Subskrypcji
Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure. Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

## WYSYŁA

### Microsoft. Azure. PowerShell. polecenia cmdlet. Commerce. modele. Api20150601Preview. IUsageAggregate



## INFORMACYJN

## LINKI POKREWNE

