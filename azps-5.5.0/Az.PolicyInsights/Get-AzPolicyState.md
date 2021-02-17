---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
ms.openlocfilehash: 04600529ded8b95da578d59f0b2f46cd396594ba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240339"
---
# Get-AzPolicyState

## SYNOPSIS
Pobiera stany zgodności zasad dla zasobów.

## SKŁADNIA

### SubscriptionScope (domyślne)
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ManagementGroupScope
```
Get-AzPolicyState [-All] -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupScope
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceScope
```
Get-AzPolicyState [-All] -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-Expand <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PolicySetDefinitionScope
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PolicyDefinitionScope
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SubscriptionLevelPolicyAssignmentScope
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupLevelPolicyAssignmentScope
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Pobiera stany zgodności zasad dla zasobów. Zapytania dotyczące rekordów stanu zasad można używać w różnych zakresach. W zależności od określonego interwału czasu (domyślnie do ostatniego dnia) można utworzyć zapytanie dotyczące najnowszych stanów zasad lub wszystkich przejść stanów zasad. Wyniki można filtrować, grupować i obliczać agregacje grup.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie najnowszych stanów zasad w bieżącym zakresie subskrypcji
```powershell
PS C:\> Get-AzPolicyState
```

Pobiera najnowsze rekordy stanu zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.

### Przykład 2. Uzyskiwanie najnowszych stanów zasad w zakresie określonej subskrypcji
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

Pobiera rekordy stanu najnowszych zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach określonej subskrypcji.

### Przykład 3. Uzyskiwanie wszystkich stanów zasad w bieżącym zakresie subskrypcji
```powershell
PS C:\> Get-AzPolicyState -All
```

Pobiera wszystkie historyczne rekordy stanu zasad (w tym najnowsze) wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.

### Przykład 4. Uzyskiwanie najnowszych stanów zasad w zakresie grupy zarządzania
```powershell
PS C:\> Get-AzPolicyState -ManagementGroupName "myManagementGroup"
```

Pobiera najnowsze rekordy stanu zasad generowane w ostatnim dniu dla wszystkich zasobów w określonej grupie zarządzania.

### Przykład 5. Uzyskiwanie najnowszych stanów zasad w zakresie grupy zasobów w bieżącej subskrypcji
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup"
```

Pobiera rekordy stanu najnowszych zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach określonej grupy zasobów (w ramach subskrypcji w bieżącym kontekście sesji).

### Przykład 6. Uzyskiwanie najnowszych stanów zasad w zakresie grupy zasobów w określonej subskrypcji
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

Pobiera rekordy stanu najnowszych zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w określonej grupie zasobów (w określonej subskrypcji).

### Przykład 7. Uzyskiwanie najnowszych stanów zasad dla zasobu
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

Pobiera rekordy stanu najnowszych zasad wygenerowane w ostatnim dniu dla określonego zasobu.

### Przykład 8. Uzyskiwanie najnowszych stanów zasad dla definicji zestawu zasad w bieżącej subskrypcji
```powershell
PS C:\> Get-AzPolicyState -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Pobiera rekordy stanu najnowszych zasad generowane w ostatnim dniu dla wszystkich zasobów (w ramach dzierżawy w bieżącym kontekście sesji) określonych definicji zestawu zasad (która istnieje w subskrypcji w bieżącym kontekście sesji).

### Przykład 9. Uzyskiwanie najnowszych stanów zasad dla definicji zestawu zasad w określonej subskrypcji
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Pobiera rekordy stanu najnowszych zasad generowane w ostatnim dniu dla wszystkich zasobów (w ramach dzierżawy w bieżącym kontekście sesji) określonych na podstawie definicji zestawu określonych zasad (która istnieje w określonej subskrypcji).

### Przykład 10. Uzyskiwanie najnowszych stanów zasad dla definicji zasad w bieżącej subskrypcji
```powershell
PS C:\> Get-AzPolicyState -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Pobiera rekordy stanu najnowszych zasad generowane w ostatnim dniu dla wszystkich zasobów (w ramach dzierżawy w bieżącym kontekście sesji) w ramach określonej definicji zasad (która istnieje w subskrypcji w bieżącym kontekście sesji).

### Przykład 11. Uzyskiwanie najnowszych stanów zasad dla definicji zasad w określonej subskrypcji
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Pobiera rekordy stanu najnowszych zasad generowane w ostatnim dniu dla wszystkich zasobów (w ramach dzierżawy w bieżącym kontekście sesji) w ramach określonej definicji zasad (która istnieje w określonej subskrypcji).

### Przykład 12. Uzyskiwanie najnowszych stanów zasad dla przypisania zasad w bieżącej subskrypcji
```powershell
PS C:\> Get-AzPolicyState -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Pobiera rekordy stanu najnowszych zasad generowane w ostatnim dniu dla wszystkich zasobów (w ramach dzierżawy w bieżącym kontekście sesji) określonych przez przypisanie określonych zasad (które istnieje w subskrypcji w bieżącym kontekście sesji).

### Przykład 13. Uzyskiwanie najnowszych stanów zasad dla przypisania zasad w określonej subskrypcji
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Pobiera rekordy stanu najnowszych zasad generowane w ostatnim dniu dla wszystkich zasobów (w ramach dzierżawy w bieżącym kontekście sesji) określonych przez przypisanie określonych zasad (które istnieje w określonej subskrypcji).

### Przykład 14. Uzyskiwanie najnowszych stanów zasad dla przydziału zasad w określonej grupie zasobów w bieżącej subskrypcji
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Pobiera rekordy stanu najnowszych zasad generowane w ostatnim dniu dla wszystkich zasobów (w ramach dzierżawy w bieżącym kontekście sesji) w związku z określonym przydziałem zasad (który istnieje w grupie zasobów w ramach subskrypcji w bieżącym kontekście sesji).

### Przykład 15. Uzyskiwanie najnowszych stanów zasad w bieżącym zakresie subskrypcji za pomocą opcji zapytania OrderBy, Top i Select
```powershell
PS C:\> Get-AzPolicyState -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId, IsCompliant"
```

Pobiera najnowsze rekordy stanu zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji. Polecenie uporządkuje wyniki według właściwości sygnatury czasowej i nazwy przydziału zasad i przyjmuje tylko 5 z nich wymienionych w tej kolejności.
Wybiera on również, aby wyświetlić tylko podzbiór kolumn dla każdego rekordu.

### Przykład 16. Uzyskiwanie najnowszych stanów zasad w bieżącym zakresie subskrypcji z opcjami zapytania Od i Do
```powershell
PS C:\> Get-AzPolicyState -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

Pobiera najnowsze rekordy stanu zasad generowane w zakresie dat określonym dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.

### Przykład 17. Uzyskiwanie najnowszych stanów zasad w bieżącym zakresie subskrypcji z opcją zapytania filtru
```powershell
PS C:\> Get-AzPolicyState -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ComplianceState eq 'NonCompliant' and ResourceLocation ne 'eastus'"
```

Pobiera najnowsze rekordy stanu zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.
To polecenie ogranicza wyniki zwracane przez filtrowanie na podstawie akcji definicji zasad (obejmuje akcje odrzucania lub inspekcji), stanu zgodności (obejmuje tylko stan niezgodny) i lokalizacji zasobów (z wyłączeniem lokalizacji regionu wschodniego).

### Przykład 18. Uzyskiwanie najnowszych stanów zasad w bieżącym zakresie subskrypcji z ustawieniem Zastosuj określającą agregację liczby wierszy
```powershell
PS C:\> Get-AzPolicyState -Apply "aggregate(`$count as NumberOfRecords)"
```

Pobiera liczbę rekordów stanu najnowszych zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.
To polecenie zwraca liczbę tylko rekordów stanu zasad, zwracanych wewnątrz właściwości AdditionalProperties.

### Przykład 19. Uzyskiwanie najnowszych stanów zasad w bieżącym zakresie subskrypcji z zastosowaniem określania grupowania z agregacją
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumStates))" -OrderBy "NumStates desc" -Top 5
```

Pobiera najnowsze rekordy stanu zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji. To polecenie ogranicza wyniki zwracane przez filtrowanie na podstawie stanu zgodności (obejmuje tylko stan niezgodności).
Grupuje wyniki na podstawie przypisania zasad, definicji zestawu zasad i definicji zasad, a następnie oblicza liczbę rekordów w każdej grupie, która jest zwracana wewnątrz właściwości AdditionalProperties.
Wyniki są uporządkowane według agregacji licznika w kolejności malejącej i przyjmuje tylko 5 z nich wymienionych w tej kolejności.

### Przykład 20. Uzyskiwanie najnowszych stanów zasad w bieżącym zakresie subskrypcji z ustawieniem Zastosuj grupowanie bez agregacji
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((ResourceId))"
```

Pobiera najnowsze rekordy stanu zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji. To polecenie ogranicza wyniki zwracane przez filtrowanie na podstawie stanu zgodności (obejmuje tylko stan niezgodności).
Grupuje wyniki na podstawie identyfikatora zasobu. W ten sposób zostanie wygenerowana lista wszystkich zasobów w ramach subskrypcji, które są niezgodne z co najmniej jedną zasadą.

### Przykład 21. Uzyskiwanie najnowszych stanów zasad w bieżącym zakresie subskrypcji z polem Zastosuj określającą wiele grupowania
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumNonCompliantResources))" -OrderBy "NumNonCompliantResources desc" -Top 5
```

### Przykład 22. Uzyskiwanie najnowszych stanów zasad wraz ze szczegółami oceny zasad dla zasobu
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1" -Expand "PolicyEvaluationDetails"
```

Pobiera najnowsze rekordy stanu zasad wygenerowane w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji. To polecenie ogranicza wyniki zwracane przez filtrowanie na podstawie stanu zgodności (obejmuje tylko stan niezgodności).
Najpierw grupuje wyniki na podstawie przypisania zasad, definicji zestawu zasad, definicji zasad i identyfikatora zasobu. Następnie grupuje wyniki tej grupowania o tych samych właściwościach z wyjątkiem identyfikatora zasobu i oblicza liczbę rekordów w każdej z tych grup, która jest zwracana we właściwości AdditionalProperties.
Wyniki są uporządkowane według agregacji licznika w kolejności malejącej i przyjmuje tylko 5 z nich wymienionych w tej kolejności.
W ten sposób jest generowanych 5 najważniejszych zasad z najwięcej niezgodnych zasobów.

## PARAMETERS

### — Wszystko
W określonym interwale czasu pobierz wszystkie stany zasad, a nie tylko najnowsze.

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

### — Rozwiń
Rozwijanie wyrażenia przy użyciu notacji OData.

```yaml
Type: System.String
Parameter Sets: ResourceScope
Aliases:

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
Co najmniej jedna nazwa kolumny rozdzielona przecinkami.
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

### Microsoft.Azure.Commands.PolicyInsights.Models.PolicyState

## NOTATKI

## LINKI POKREWNE

[Get-AzPolicyStateSummary](./Get-AzPolicyStateSummary.md)
