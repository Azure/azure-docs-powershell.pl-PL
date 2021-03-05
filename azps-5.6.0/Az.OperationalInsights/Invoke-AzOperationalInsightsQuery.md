---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/invoke-azoperationalinsightsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Invoke-AzOperationalInsightsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Invoke-AzOperationalInsightsQuery.md
ms.openlocfilehash: bdba6d4da6df49d1975e2cfd1cc6e47f6ce6d776
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010289"
---
# Invoke-AzOperationalInsightsQuery

## SYNOPSIS
Zwraca wyniki wyszukiwania na podstawie określonych parametrów.

## SKŁADNIA

### ByWorkspaceId (Domyślna)
```
Invoke-AzOperationalInsightsQuery -WorkspaceId <String> -Query <String> [-Timespan <TimeSpan>] [-Wait <Int32>]
 [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByWorkspaceObject
```
Invoke-AzOperationalInsightsQuery -Workspace <PSWorkspace> -Query <String> [-Timespan <TimeSpan>]
 [-Wait <Int32>] [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## OPIS
Polecenie cmdlet **Invoke-AzOperationalInsightsQuery** zwraca wyniki wyszukiwania na podstawie określonych parametrów.
Stan wyszukiwania można uzyskać we właściwości Metadane zwróconego obiektu.
Jeśli stan to Oczekiwanie, wyszukiwanie nie zostało ukończone, a wyniki zostaną z archiwum.
Wyniki wyszukiwania można pobrać z właściwości Wartość zwróconego obiektu.
Tutaj możesz sprawdzić szczegółowe informacje dotyczące ogólnych limitów https://docs.microsoft.com/azure/azure-monitor/service-limits#log-queries-and-language zapytań:

## PRZYKŁADY

### Przykład 1. Uzyskiwanie wyników wyszukiwania przy użyciu zapytania
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $queryResults.Results
...
```

Po wywołaniu funkcja $queryResults.Results będzie zawierać wszystkie wiersze wynikowe z zapytania.

### Przykład 2. Konwertowanie $results. Wynik IEnumerable do tablicy
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $resultsArray = [System.Linq.Enumerable]::ToArray($queryResults.Results)
...
```

Niektóre zapytania mogą powodować zwracanie bardzo dużych zestawów danych. Z tego powodu domyślnym zachowaniem polecenia cmdlet jest zwracanie wartości IEnumerable w celu zmniejszenia kosztów pamięci. Jeśli wolisz uzyskać tablicę wyników, możesz użyć metody rozszerzenia LINQ enumerable.ToArray() w celu przekonwertowania wartości IEnumerable na tablicę.

### Przykład 3. Uzyskiwanie wyników wyszukiwania przy użyciu zapytania w określonym czasie
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -Timespan (New-TimeSpan -Hours 24)
PS C:\> $queryResults.Results
...
```

Wyniki tego zapytania będą ograniczone do ostatnich 24 godzin.

### Przykład 4. Uwzględnianie & renderowania w wynikach zapytania
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -IncludeRender -IncludeStatistics
PS C:\> $queryResults.Results
...
PS C:\> $queryResults.Render
...
PS C:\> $queryResults.Statistics
...
```

Aby [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) uzyskać szczegółowe informacje na temat renderowania i statystyki, zobacz te informacje.

## PARAMETERS

### — AsJob
Uruchamianie polecenia cmdlet w tle

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

### - IncludeRender
Jeśli zostanie określona, informacje o renderowaniu dla zapytań metrycznych będą uwzględniane w odpowiedzi.

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

### — IncludeStatistics
Jeśli zostanie określona, w odpowiedzi zostaną uwzględnione statystyki zapytań.

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

### — zapytanie
Kwerenda do wykonania.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - Timespan
Czas, przez który zapytanie jest powiązane.

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Czekanie
Dodaje górną granicę czasu przetwarzania zapytania przez serwer.
Zobacz: https://dev.loganalytics.io/documentation/Using-the-API/Timeouts

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Obszar roboczy
Obszar roboczy

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WorkspaceId
Identyfikator obszaru roboczego.

```yaml
Type: System.String
Parameter Sets: ByWorkspaceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.OperationalInsights.Models.PSQueryResponse

## NOTATKI

## LINKI POKREWNE
