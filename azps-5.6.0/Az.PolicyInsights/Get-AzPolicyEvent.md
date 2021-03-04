---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/get-azpolicyevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
ms.openlocfilehash: 7c9ee7af59acc90fba6a17e78ffd3dfc4822472d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989171"
---
# Get-AzPolicyEvent

## SYNOPSIS
Pobiera zdarzenia oceny zasad generowane w przypadku tworzenia lub aktualizowania zasobów.

## SKŁADNIA

### SubscriptionScope (domyślne)
```
Get-AzPolicyEvent [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ManagementGroupScope
```
Get-AzPolicyEvent -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupScope
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PolicySetDefinitionScope
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PolicyDefinitionScope
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SubscriptionLevelPolicyAssignmentScope
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupLevelPolicyAssignmentScope
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceScope
```
Get-AzPolicyEvent -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>]
 [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## OPIS
Pobiera zdarzenia oceny zasad generowane w przypadku tworzenia lub aktualizowania zasobów. Zapytania dotyczące rekordów zdarzeń zasad można używać w różnych zakresach w zależności od określonego interwału czasu (domyślne wartością jest ostatni dzień). Wyniki można filtrować, grupować i obliczać agregacje grup.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie zdarzeń zasad w bieżącym zakresie subskrypcji
```powershell
PS C:\> Get-AzPolicyEvent
```

Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.

### Przykład 2. Uzyskiwanie zdarzeń zasad w zakresie określonej subskrypcji
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach określonej subskrypcji.

### Przykład 3. Uzyskiwanie zdarzeń zasad w zakresie grupy zarządzania
```powershell
PS C:\> Get-AzPolicyEvent -ManagementGroupName "myManagementGroup"
```

Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w określonej grupie zarządzania.

### Przykład 4. Uzyskiwanie zdarzeń zasad w zakresie grupy zasobów w bieżącej subskrypcji
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup"
```

Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w określonej grupie zasobów (w ramach subskrypcji w kontekście bieżącej sesji).

### Przykład 5. Uzyskiwanie zdarzeń zasad w zakresie grupy zasobów w określonej subskrypcji
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w określonej grupie zasobów (w określonej subskrypcji).

### Przykład 6. Uzyskiwanie zdarzeń zasad dla zasobu
```powershell
PS C:\> Get-AzPolicyEvent -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla określonego zasobu.

### Przykład 7. Uzyskiwanie zdarzeń zasad dla definicji zestawu zasad w bieżącej subskrypcji
```powershell
PS C:\> Get-AzPolicyEvent -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów (w ramach dzierżawy w bieżącym kontekście sesji) w ramach określonej definicji zestawu zasad (która istnieje w subskrypcji w bieżącym kontekście sesji).

### Przykład 8. Uzyskiwanie zdarzeń zasad dla definicji zestawu zasad w określonej subskrypcji
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów (w ramach dzierżawy w bieżącym kontekście sesji) w ramach określonej definicji zestawu zasad (która istnieje w określonej subskrypcji).

### Przykład 9. Uzyskiwanie zdarzeń zasad dla definicji zasad w bieżącej subskrypcji
```powershell
PS C:\> Get-AzPolicyEvent -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów (w ramach dzierżawy w kontekście bieżącej sesji) w związku z określoną definicją zasad (która istnieje w subskrypcji w bieżącym kontekście sesji).

### Przykład 10. Uzyskiwanie zdarzeń zasad dla definicji zasad w określonej subskrypcji
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów (w ramach dzierżawy w bieżącym kontekście sesji) w związku z określoną definicją zasad (która istnieje w określonej subskrypcji).

### Przykład 11. Uzyskiwanie zdarzeń zasad dla przypisania zasad w bieżącej subskrypcji
```powershell
PS C:\> Get-AzPolicyEvent -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów (w ramach dzierżawy w bieżącym kontekście sesji) w związku z określonym przypisaniem zasad (który istnieje w subskrypcji w bieżącym kontekście sesji).

### Przykład 12. Uzyskiwanie zdarzeń zasad dla przypisania zasad w określonej subskrypcji
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów (w ramach dzierżawy w bieżącym kontekście sesji) określonych przez przypisanie określonych zasad (które istnieje w określonej subskrypcji).

### Przykład 13. Uzyskiwanie zdarzeń zasad dla przydziału zasad w określonej grupie zasobów w bieżącej subskrypcji
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Pobiera rekordy zdarzeń zasad generowane w ostatnim dniu dla wszystkich zasobów (w ramach dzierżawy w bieżącym kontekście sesji) w związku z określonym przydziałem zasad (który istnieje w grupie zasobów w ramach subskrypcji w bieżącym kontekście sesji).

### Przykład 14. Uzyskiwanie zdarzeń zasad w bieżącym zakresie subskrypcji przy użyciu opcji zapytania OrderBy, Top i Select
```powershell
PS C:\> Get-AzPolicyEvent -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId"
```

Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji. Polecenie uporządkuje wyniki według właściwości sygnatury czasowej i nazwy przydziału zasad i przyjmuje tylko 5 z nich wymienionych w tej kolejności.
Wybiera on również, aby wyświetlić tylko podzbiór kolumn dla każdego rekordu.

### Przykład 15. Uzyskiwanie zdarzeń zasad w bieżącym zakresie subskrypcji z opcjami zapytania Od i Do
```powershell
PS C:\> Get-AzPolicyEvent -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

Pobiera rekordy zdarzeń zasad generowane w zakresie dat określonym dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.

### Przykład 16. Uzyskiwanie zdarzeń zasad w bieżącym zakresie subskrypcji z opcją zapytania filtru
```powershell
PS C:\> Get-AzPolicyEvent -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.
To polecenie ogranicza wyniki zwracane przez filtrowanie na podstawie akcji definicji zasad (obejmuje akcje odrzucania lub inspekcji) i lokalizacji zasobów (z wyłączeniem lokalizacji regionu wschodniego).

### Przykład 17. Uzyskiwanie zdarzeń zasad w bieżącym zakresie subskrypcji z ustawieniem agregacji Zastosuj do liczby wierszy
```powershell
PS C:\> Get-AzPolicyEvent -Apply "aggregate(`$count as NumberOfRecords)"
```

Pobiera liczbę rekordów zdarzeń zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w kontekście bieżącej sesji.
To polecenie zwraca tylko liczbę rekordów zdarzeń zasad, która jest zwracana wewnątrz właściwości AdditionalProperties.

### Przykład 18. Uzyskiwanie zdarzeń zasad w bieżącym zakresie subskrypcji z ustawieniem Zastosuj grupowanie z agregacją
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, PolicyDefinitionAction, ResourceId), aggregate(`$count as NumEvents))" -OrderBy "NumEvents desc" -Top 5
```

Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji. To polecenie ogranicza wyniki zwracane przez filtrowanie na podstawie akcji definicji zasad (obejmuje tylko inspekcję i odrzucanie zdarzeń).
Grupuje wyniki na podstawie przypisania zasad, definicji zasad, akcji definicji zasad i identyfikatora zasobu, a następnie oblicza liczbę rekordów w każdej grupie, która jest zwracana we właściwości AdditionalProperties.
Wyniki są uporządkowane według agregacji licznika w kolejności malejącej i przyjmuje tylko 5 z nich wymienionych w tej kolejności.

### Przykład 19. Uzyskiwanie zdarzeń zasad w bieżącym zakresie subskrypcji z ustawieniem Zastosuj grupowanie bez agregacji
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((ResourceId))"
```

Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji. To polecenie ogranicza wyniki zwracane przez filtrowanie na podstawie akcji definicji zasad (obejmuje tylko inspekcję i odrzucanie zdarzeń).
Grupuje wyniki na podstawie identyfikatora zasobu. W wyniku tego zostanie wygenerowana lista wszystkich zasobów w ramach subskrypcji, które wygenerują zdarzenie zasad dla co najmniej jednej inspekcji lub odmów zasad.

### Przykład 20. Uzyskiwanie zdarzeń zasad w bieżącym zakresie subskrypcji z polem Zastosuj określającą wiele grup
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicyDefinitionId), aggregate(`$count as NumDeniedResources))" -OrderBy "NumDeniedResources desc" -Top 5
```

Pobiera rekordy zdarzeń zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji. To polecenie ogranicza wyniki zwracane przez filtrowanie na podstawie akcji definicji zasad (obejmuje tylko odrzucanie zdarzeń).
Najpierw grupuje wyniki na podstawie przydziałów zasad, definicji zasad i identyfikatora zasobu. Następnie grupuje wyniki tej grupowania o tych samych właściwościach z wyjątkiem identyfikatora zasobu i oblicza liczbę rekordów w każdej z tych grup, która jest zwracana we właściwości AdditionalProperties.
Wyniki są uporządkowane według agregacji licznika w kolejności malejącej i przyjmuje tylko 5 z nich wymienionych w tej kolejności.
W ten sposób jest generowanych 5 najważniejszych zasad odmów z najwięcej odrzuconych zasobów.

## PARAMETERS

### — Zastosuj
Zastosuj wyrażenie dla agregacji przy użyciu notacji OData.

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

### — Filtr
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

### — Od
Sygnatura czasowa w formacie ISO 8601 określająca czas rozpoczęcia interwału dla zapytania.
Jeśli nie jest określona, wartość parametru "To" jest domyślnie określana jako minus 1 dzień.

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
Wyrażenie kolejności przy użyciu notacji OData.
Co najmniej jedna nazwa kolumny rozdzielona przecinkami z opcjonalnym "desc" (ustawieniem domyślnym) lub "asc".

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
Nazwa przydziału zasad.

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

### — Wybierz
Zaznacz wyrażenie przy użyciu notacji OData.
Co najmniej jedna nazwa kolumn rozdzielanych przecinkami.
Ogranicza kolumny w każdym rekordzie tylko do tych, o które proszono.

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

### - SubscriptionId
Identyfikator subskrypcji.

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

### — Do
Sygnatura czasowa w formacie ISO 8601 określająca czas zakończenia interwału dla zapytania.
Jeśli nie zostanie określona, domyślnie jest określana godzina żądania.

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

### — Na górze
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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.PolicyInsights.Models.PolicyEvent

## NOTATKI

## LINKI POKREWNE
