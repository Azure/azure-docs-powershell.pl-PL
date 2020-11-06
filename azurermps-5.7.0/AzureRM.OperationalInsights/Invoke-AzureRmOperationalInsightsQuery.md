---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/invoke-azurermoperationalinsightsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Invoke-AzureRmOperationalInsightsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Invoke-AzureRmOperationalInsightsQuery.md
ms.openlocfilehash: e3bfdd771413f17d4dd560a350d45fdb3f47c5a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527994"
---
# Invoke-AzureRmOperationalInsightsQuery

## STRESZCZENIe
Zwraca wyniki wyszukiwania na podstawie określonych parametrów.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### ByWorkspaceId (domyślny)
```
Invoke-AzureRmOperationalInsightsQuery -WorkspaceId <String> -Query <String> [-Timespan <TimeSpan>]
 [-Wait <Int32>] [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByWorkspaceObject
```
Invoke-AzureRmOperationalInsightsQuery -Workspace <PSWorkspace> -Query <String> [-Timespan <TimeSpan>]
 [-Wait <Int32>] [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Invoke-AzureRmOperationalInsightsQuery** zwraca wyniki wyszukiwania na podstawie określonych parametrów.

Możesz uzyskać dostęp do stanu wyszukiwania we właściwości Metadata zwracanego obiektu.
Jeśli stan jest oczekujący, wyszukiwanie nie zostało wykonane, a wyniki będą pochodzić z archiwum.

Wyniki wyszukiwania można pobrać z właściwości Value zwróconego obiektu.

## Przykłady

### Przykład 1: uzyskiwanie wyników wyszukiwania za pomocą kwerendy
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $queryResults.Results
...
```

Po wywołaniu $queryResults. wyniki będą zawierać wszystkie wiersze wynikowe z zapytania.

### Przykład 2: konwertowanie $results. Wyniki IEnumberable do tablicy
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $resultsArray = [System.Linq.Enumerable]::ToArray($results.Results)
...
```

Niektóre kwerendy mogą powodować zwracanie bardzo dużych zestawów danych. W związku z tym domyślnym zachowaniem polecenia cmdlet jest zwrócenie interfejsu IEnumerable w celu zmniejszenia kosztów pamięci. Jeśli wolisz uzyskać tablicę wyników, możesz użyć metody rozszerzenia wyliczalna Metoda LINQ. ToArray () w celu przekonwertowania interfejsu IEnumerable na tablicę.

### Przykład 3: uzyskiwanie wyników wyszukiwania przy użyciu zapytania w określonym przedziale czasu
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -Timespan (New-TimeSpan -Hours 24)
PS C:\> $queryResults.Results
...
```

Wyniki z tego zapytania będą ograniczone do ciągu 24 godzin.

### Przykład 4: uwzględnianie statystyk & renderowania w wynikach zapytania
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -IncludeRender -IncludeStatistics
PS C:\> $queryResults.Results
...
PS C:\> $queryResults.Render
...
PS C:\> $queryResults.Statistics
...
```

[https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions)Aby uzyskać szczegółowe informacje, zobacz informacje dotyczące renderowania i statystyk.

## PARAMETRÓW

### -AsJob
Uruchom polecenie cmdlet w tle
```yaml
Type: SwitchParameter
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeRender
Jeśli ta wartość jest określona, w odpowiedzi zostaną uwzględnione informacje dotyczące renderowania zapytań metrycznych.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeStatistics
Jeśli ta argument jest określona, statystyki kwerend zostaną uwzględnione w odpowiedzi.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Query
Kwerenda do wykonania.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TimeSpan
Obiekt TimeSpan, według którego ma zostać powiązany kwerenda.

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Czekaj
Umieszcza górną granicę czasu, jaki serwer będzie poświęcał na przetwarzanie kwerendy.
Widz https://dev.loganalytics.io/documentation/Using-the-API/Timeouts

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Obszar roboczy
Obszar roboczy

```yaml
Type: PSWorkspace
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
Type: String
Parameter Sets: ByWorkspaceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace
Jeśli potoku, identyfikator obszaru roboczego zostanie wyodrębniony z PSWorkspace. W przeciwnym razie za pomocą parametru workspaceId można ręcznie określić identyfikator obszaru roboczego.

## WYSYŁA

### Microsoft. Azure. Commands. OperationalInsights. models. PSQueryResponse
***PSQueryResponse*** zawiera wyniki, Renderuj & statystykę zapytania.

## INFORMACYJN

## LINKI POKREWNE

