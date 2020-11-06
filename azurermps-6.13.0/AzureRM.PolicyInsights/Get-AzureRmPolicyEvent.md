---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/get-azurermpolicyevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyEvent.md
ms.openlocfilehash: 0c4e4f531dac3f75f0eff69ba1dcfc644473ea06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547359"
---
# Get-AzureRmPolicyEvent

## STRESZCZENIe
Pobiera zdarzenia obliczania zasad generowane po utworzeniu lub zaktualizowaniu zasobów.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### SubscriptionScope (domyślny)
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ManagementGroupScope
```
Get-AzureRmPolicyEvent -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupScope
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PolicySetDefinitionScope
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PolicyDefinitionScope
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SubscriptionLevelPolicyAssignmentScope
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupLevelPolicyAssignmentScope
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceScope
```
Get-AzureRmPolicyEvent -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Pobiera zdarzenia obliczania zasad generowane po utworzeniu lub zaktualizowaniu zasobów. Rekordy zdarzeń zasad mogą być badane w różnych zakresach na podstawie określonego interwału czasu (domyślnie do ostatniego dnia). Wyniki mogą być filtrowane, grupowane, a agregacje grup mogą być obliczane.

## Przykłady

### Przykład 1: pobieranie zdarzeń dotyczących zasad w bieżącym zakresie subskrypcji
```powershell
PS C:\> Get-AzureRmPolicyEvent
```

Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.

### Przykład 2: pobieranie zdarzeń dotyczących zasad w określonym zakresie subskrypcji
```powershell
PS C:\> Get-AzureRmPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach określonej subskrypcji.

### Przykład 3: pobieranie zdarzeń dotyczących zasad w zakresie grupy zarządzania
```powershell
PS C:\> Get-AzureRmPolicyEvent -ManagementGroupName "myManagementGroup"
```

Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w określonej grupie zarządzania.

### Przykład 4: pobieranie zdarzeń dotyczących zasad w zakresie grupy zasobów w bieżącej subskrypcji
```powershell
PS C:\> Get-AzureRmPolicyEvent -ResourceGroupName "myResourceGroup"
```

Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w określonej grupie zasobów (w subskrypcji w bieżącym kontekście sesji).

### Przykład 5: pobieranie zdarzeń zasad w zakresie grupy zasobów w określonej subskrypcji
```powershell
PS C:\> Get-AzureRmPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w określonej grupie zasobów (w określonej subskrypcji).

### Przykład 6: pobieranie zdarzeń dotyczących zasad dla zasobu
```powershell
PS C:\> Get-AzureRmPolicyEvent -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu określonego zasobu.

### Przykład 7: pobieranie zdarzeń dotyczących zasad dla definicji zestawu zasad w bieżącym abonamentzie
```powershell
PS C:\> Get-AzureRmPolicyEvent -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Umożliwia pobieranie rekordów zdarzeń zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) za pomocą określonej definicji zestawu zasad (istniejącej w ramach subskrypcji w bieżącym kontekście sesji).

### Przykład 8: pobieranie zdarzeń dotyczących zasad dla definicji zestawu zasad w określonej subskrypcji
```powershell
PS C:\> Get-AzureRmPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Umożliwia pobieranie rekordów zdarzeń zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) za pomocą określonej definicji zestawu zasad (istniejącej w określonej subskrypcji).

### Przykład 9: pobieranie zdarzeń dotyczących zasad dla definicji zasad w bieżącej subskrypcji
```powershell
PS C:\> Get-AzureRmPolicyEvent -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Umożliwia pobieranie rekordów zdarzeń zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) zgodnie z określoną definicją zasad (istniejącą w ramach subskrypcji w bieżącym kontekście sesji).

### Przykład 10: pobieranie zdarzeń zasad dla definicji zasad w określonej subskrypcji
```powershell
PS C:\> Get-AzureRmPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Umożliwia pobieranie rekordów zdarzeń zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) zgodnie z określoną definicją zasad (istniejącą w określonej subskrypcji).

### Przykład 11: pobieranie zdarzeń dotyczących zasad dla przypisania zasad w bieżącej subskrypcji
```powershell
PS C:\> Get-AzureRmPolicyEvent -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) wykonywane przez określone przypisanie zasad (istniejące w subskrypcji w bieżącym kontekście sesji).

### Przykład 12: pobieranie zdarzeń zasad dla przydziału zasad w określonej subskrypcji
```powershell
PS C:\> Get-AzureRmPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) dokonywanych przez określone przypisanie zasad (istniejące w określonej subskrypcji).

### Przykład 13: pobieranie zdarzeń zasad dla przydziału zasad w określonej grupie zasobów w bieżącej subskrypcji
```powershell
PS C:\> Get-AzureRmPolicyEvent -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) realizowanych przez określone przypisanie zasad (istniejące w grupie zasobów w subskrypcji w bieżącym kontekście sesji).

### Przykład 14: pobieranie zdarzeń dotyczących zasad w bieżącym zakresie subskrypcji przy użyciu opcji OrderBy, początek i wybierz zapytanie
```powershell
PS C:\> Get-AzureRmPolicyEvent -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId"
```

Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji. Polecenie porządkuje wyniki według sygnatury czasowej i właściwości nazw przydziałów, a następnie pobiera tylko 5 najważniejszych osób z listy w tej kolejności.
Wybiera także listę tylko podzestawu kolumn dla każdego rekordu.

### Przykład 15: pobieranie zdarzeń dotyczących zasad w bieżącym zakresie subskrypcji przy użyciu opcji od i do zapytania
```powershell
PS C:\> Get-AzureRmPolicyEvent -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

Pobiera rekordy zdarzeń zasad wygenerowane w zakresie dat określonym dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.

### Przykład 16: pobieranie zdarzeń dotyczących zasad w bieżącym zakresie subskrypcji przy użyciu opcji Filtruj zapytanie
```powershell
PS C:\> Get-AzureRmPolicyEvent -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.
Polecenie ogranicza wyniki zwracane przez filtrowanie na podstawie akcji definicji zasad (dotyczy to odmowy lub akcji inspekcji) oraz lokalizacji zasobów (z pominięciem lokalizacji wschodniego).

### Przykład 17: pobieranie zdarzeń dotyczących zasad w bieżącym zakresie subskrypcji przy użyciu Zastosuj Określanie agregacji liczby wierszy
```powershell
PS C:\> Get-AzureRmPolicyEvent -Apply "aggregate(`$count as NumberOfRecords)"
```

Pobiera liczbę rekordów zdarzeń zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.
Polecenie zwraca liczbę tylko rekordów zdarzeń zasad, które są zwracane w ramach właściwości AdditionalProperties.

### Przykład 18: pobieranie zdarzeń dotyczących zasad w bieżącym zakresie subskrypcji przy użyciu Zastosuj Określanie grupowania z agregacją
```powershell
PS C:\> Get-AzureRmPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, PolicyDefinitionAction, ResourceId), aggregate(`$count as NumEvents))" -OrderBy "NumEvents desc" -Top 5
```

Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji. Polecenie ogranicza wyniki zwracane przez filtrowanie na podstawie akcji definicji zasad (obejmuje tylko zdarzenia inspekcji i Odmów).
Umożliwia grupowanie wyników na podstawie przydziału zasad, definicji zasad, akcji definicji zasad i identyfikatora zasobu oraz obliczanie liczby rekordów w każdej grupie, która jest zwracana w ramach właściwości AdditionalProperties.
Wyniki są porządkowane według agregacji zliczania w kolejności malejącej, a w tej kolejności są uwzględniane tylko 5 pierwszych.

### Przykład 19: pobieranie zdarzeń dotyczących zasad w bieżącym zakresie subskrypcji z zastosowaniem Określanie grupowania bez agregacji
```powershell
PS C:\> Get-AzureRmPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((ResourceId))"
```

Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji. Polecenie ogranicza wyniki zwracane przez filtrowanie na podstawie akcji definicji zasad (obejmuje tylko zdarzenia inspekcji i Odmów).
Umożliwia grupowanie wyników na podstawie identyfikatora zasobu. Spowoduje to wygenerowanie listy wszystkich zasobów w ramach subskrypcji, które wygenerowały zdarzenie zasad dla co najmniej jednej inspekcji lub zasady odmowy.

### Przykład 20: pobieranie zdarzeń dotyczących zasad w bieżącym zakresie subskrypcji z zastosowaniem Określanie wielu grup
```powershell
PS C:\> Get-AzureRmPolicyEvent -Filter "PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicyDefinitionId), aggregate(`$count as NumDeniedResources))" -OrderBy "NumDeniedResources desc" -Top 5
```

Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji. Polecenie ogranicza wyniki zwracane przez filtrowanie na podstawie akcji definicji zasad (dotyczy tylko zdarzeń Odmów).
Najpierw grupuje wyniki na podstawie przydziału zasad, definicji zasad i identyfikatora zasobu. Następnie grupuje wyniki tego zgrupowania, korzystając z tych samych właściwości, z wyjątkiem identyfikatora zasobu, oraz oblicza liczbę rekordów w każdej z tych grup, która jest zwracana w ramach właściwości AdditionalProperties.
Wyniki są porządkowane według agregacji zliczania w kolejności malejącej, a w tej kolejności są uwzględniane tylko 5 pierwszych.
Spowoduje to wygenerowanie pierwszych 5 zasad odmowy, które mają najwięcej odmówionych zasobów.

## PARAMETRÓW

### -Apply
Stosowanie wyrażenia agregacji przy użyciu notacji OData.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Filter
Wyrażenie filtru przy użyciu notacji OData.

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

### -Od
ISO 8601 sformatowana sygnatura czasowa określająca czas rozpoczęcia interwału do kwerendy.
Jeśli nie określono tej wartości, domyślnie przyjmowana jest wartość parametru "to" pomniejszona o 1 dzień.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagementGroupName
Nazwa grupy zarządzania.

```yaml
Type: System.String
Parameter Sets: ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OrderBy
Wyrażenie porządkowania przy użyciu notacji OData.
Jedna lub więcej nazw kolumn rozdzielanych przecinkami z opcjonalną wartością DESC (domyślnie) lub "ASC".

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

### -PolicyAssignmentName
Nazwa zadania w zasadach.

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelPolicyAssignmentScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicyDefinitionName
Nazwa definicji zasad.

```yaml
Type: System.String
Parameter Sets: PolicyDefinitionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicySetDefinitionName
Nazwa definicji zestawu zasad.

```yaml
Type: System.String
Parameter Sets: PolicySetDefinitionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów.

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Identyfikator zasobu.

```yaml
Type: System.String
Parameter Sets: ResourceScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Wybierz pozycję
Wybierz wyrażenie przy użyciu notacji OData.
Jedna lub więcej nazw kolumn rozdzielanych przecinkami.
Ogranicza liczbę kolumn w każdym rekordzie do żądanych wartości.

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
Identyfikator abonamentu.

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, ResourceGroupScope, PolicySetDefinitionScope, PolicyDefinitionScope, SubscriptionLevelPolicyAssignmentScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -To
ISO 8601 sformatowana sygnatura czasowa określająca czas zakończenia interwału do kwerendy.
Jeśli nie określono tego parametru, domyślną wartością jest czas żądania.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Początek
Maksymalna liczba rekordów do zwrócenia.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

## WYSYŁA

### Microsoft. Azure. Commands. PolicyInsights. models. PolicyEvent

## INFORMACYJN

## LINKI POKREWNE
