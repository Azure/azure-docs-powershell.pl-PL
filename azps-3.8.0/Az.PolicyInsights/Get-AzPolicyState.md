---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
ms.openlocfilehash: 04600529ded8b95da578d59f0b2f46cd396594ba
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051945"
---
# Get-AzPolicyState

## STRESZCZENIe
Pobiera Stany zgodności z zasadami dotyczącymi zasobów.

## POLECENIA

### SubscriptionScope (domyślny)
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

## Opis
Pobiera Stany zgodności z zasadami dotyczącymi zasobów. Rekordy stanu zasad mogą być badane w różnych zakresach. W zależności od określonego interwału czasu (domyślnie jest to ostatni dzień) można wykonać zapytanie dotyczące najnowszych Stanów zasad lub wszystkich przejść między Stanami zasad. Wyniki mogą być filtrowane, grupowane, a agregacje grup mogą być obliczane.

## Przykłady

### Przykład 1: pobieranie najnowszych Stanów zasad w bieżącym zakresie subskrypcji
```powershell
PS C:\> Get-AzPolicyState
```

Umożliwia pobieranie najnowszych rekordów Stanów zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.

### Przykład 2: Uzyskiwanie najnowszych Stanów zasad w określonym zakresie subskrypcji
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

Umożliwia pobieranie najnowszych rekordów Stanów zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w ramach określonej subskrypcji.

### Przykład 3: uzyskiwanie wszystkich stanów zasad w bieżącym zakresie subskrypcji
```powershell
PS C:\> Get-AzPolicyState -All
```

Pobiera wszystkie historyczne rekordy stanu zasad (w tym najnowsze) generowane w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.

### Przykład 4: pobieranie najnowszych Stanów zasad w zakresie grupy zarządzania
```powershell
PS C:\> Get-AzPolicyState -ManagementGroupName "myManagementGroup"
```

Umożliwia pobieranie najnowszych rekordów Stanów zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w określonej grupie zarządzania.

### Przykład 5: pobieranie najnowszych Stanów zasad w zakresie grupy zasobów w bieżącej subskrypcji
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup"
```

Umożliwia pobieranie najnowszych rekordów Stanów zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów należących do określonej grupy zasobów (w subskrypcji w kontekście bieżącej sesji).

### Przykład 6: pobieranie najnowszych Stanów zasad w zakresie grupy zasobów w określonej subskrypcji
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

Umożliwia pobieranie najnowszych rekordów Stanów zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów należących do określonej grupy zasobów (w określonej subskrypcji).

### Przykład 7: Uzyskiwanie najnowszych Stanów zasad dla zasobu
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

Umożliwia pobieranie najnowszych rekordów Stanów zasad wygenerowanych w ostatnim dniu określonego zasobu.

### Przykład 8: Uzyskiwanie najnowszych Stanów zasad dla definicji zestawu zasad w bieżącej subskrypcji
```powershell
PS C:\> Get-AzPolicyState -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Umożliwia pobieranie najnowszych rekordów Stanów zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) za pomocą określonej definicji zestawu zasad (istniejącej w ramach subskrypcji w bieżącym kontekście sesji).

### Przykład 9: Uzyskiwanie najnowszych Stanów zasad dla definicji zestawu zasad w określonej subskrypcji
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Umożliwia pobieranie najnowszych rekordów Stanów zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) za pomocą określonej definicji zestawu zasad (która istnieje w określonej subskrypcji).

### Przykład 10: Uzyskiwanie najnowszych Stanów zasad dla definicji zasad w bieżącej subskrypcji
```powershell
PS C:\> Get-AzPolicyState -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Umożliwia pobieranie najnowszych rekordów stanu zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) za pomocą określonej definicji zasad (istniejącej w ramach subskrypcji w bieżącym kontekście sesji).

### Przykład 11: pobieranie najnowszych Stanów zasad dla definicji zasad w określonej subskrypcji
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Umożliwia pobieranie najnowszych rekordów Stanów zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) za pomocą określonej definicji zasad (istniejącej w określonej subskrypcji).

### Przykład 12: Uzyskiwanie najnowszych Stanów zasad dla przypisania zasad w bieżącej subskrypcji
```powershell
PS C:\> Get-AzPolicyState -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Umożliwia pobieranie najnowszych rekordów Stanów zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) przez określone przypisanie zasad (istniejące w subskrypcji bieżącego kontekstu sesji).

### Przykład 13: Uzyskiwanie najnowszych Stanów zasad dla przypisania zasad w określonej subskrypcji
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Umożliwia pobieranie najnowszych rekordów Stanów zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) przez określone przypisanie zasad (istniejące w określonej subskrypcji).

### Przykład 14: Uzyskiwanie najnowszych Stanów zasad dla przydziału zasad w określonej grupie zasobów w bieżącej subskrypcji
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Umożliwia pobieranie najnowszych rekordów Stanów zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) przez określone przypisanie zasad (istniejące w grupie zasobów w subskrypcji w bieżącym kontekście sesji).

### Przykład 15: Uzyskiwanie najnowszych Stanów zasad w bieżącym zakresie subskrypcji przy użyciu opcji OrderBy, początek i wybierz zapytanie
```powershell
PS C:\> Get-AzPolicyState -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId, IsCompliant"
```

Umożliwia pobieranie najnowszych rekordów Stanów zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji. Polecenie porządkuje wyniki według sygnatury czasowej i właściwości nazw przydziałów, a następnie pobiera tylko 5 najważniejszych osób z listy w tej kolejności.
Wybiera także listę tylko podzestawu kolumn dla każdego rekordu.

### Przykład 16: pobieranie najnowszych Stanów zasad w bieżącym zakresie subskrypcji przy użyciu opcji od i do zapytania
```powershell
PS C:\> Get-AzPolicyState -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

Pobiera najnowsze rekordy Stanów zasad wygenerowane w zakresie dat określonym dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.

### Przykład 17: Uzyskiwanie najnowszych Stanów zasad w bieżącym zakresie subskrypcji za pomocą opcji filtrowania kwerend
```powershell
PS C:\> Get-AzPolicyState -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ComplianceState eq 'NonCompliant' and ResourceLocation ne 'eastus'"
```

Umożliwia pobieranie najnowszych rekordów Stanów zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.
Polecenie ogranicza wyniki zwracane przez filtrowanie na podstawie akcji definicji zasad (obejmuje akcje odmowy lub inspekcji), stan zgodności (dotyczy tylko statusu niezgodnego) i lokalizacji zasobów (z pominięciem lokalizacji wschodniego).

### Przykład 18: pobieranie najnowszych Stanów zasad w bieżącym zakresie subskrypcji z zastosowaniem Określanie agregacji liczby wierszy
```powershell
PS C:\> Get-AzPolicyState -Apply "aggregate(`$count as NumberOfRecords)"
```

Pobiera liczbę najnowszych rekordów Stanów zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.
Polecenie zwraca liczbę tylko rekordów Stanów zasad, która jest zwracana w ramach właściwości AdditionalProperties.

### Przykład 19: pobieranie najnowszych Stanów zasad w bieżącym zakresie subskrypcji przy użyciu Zastosuj Określanie grupowania z agregacją
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumStates))" -OrderBy "NumStates desc" -Top 5
```

Umożliwia pobieranie najnowszych rekordów Stanów zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji. Polecenie ogranicza wyniki zwracane przez filtrowanie na podstawie stanu zgodności (dotyczy tylko statusu niezgodnego).
Umożliwia grupowanie wyników na podstawie przydziałów zasad, definicji zestawu zasad i definicji zasad oraz obliczanie liczby rekordów w każdej grupie, która jest zwracana w ramach właściwości AdditionalProperties.
Wyniki są porządkowane według agregacji zliczania w kolejności malejącej, a w tej kolejności są uwzględniane tylko 5 pierwszych.

### Przykład 20: Uzyskiwanie najnowszych Stanów zasad w bieżącym zakresie subskrypcji z opcją Zastosuj określającą grupowanie bez agregacji
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((ResourceId))"
```

Umożliwia pobieranie najnowszych rekordów Stanów zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji. Polecenie ogranicza wyniki zwracane przez filtrowanie na podstawie stanu zgodności (dotyczy tylko statusu niezgodnego).
Umożliwia grupowanie wyników na podstawie identyfikatora zasobu. Spowoduje to wygenerowanie listy wszystkich zasobów w ramach subskrypcji, które nie są zgodne z co najmniej jednej zasady.

### Przykład 21: Uzyskiwanie najnowszych Stanów zasad w bieżącym zakresie subskrypcji z zastosowaniem Określanie wielu grup
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumNonCompliantResources))" -OrderBy "NumNonCompliantResources desc" -Top 5
```

### Przykład 22: pobieranie najnowszych Stanów zasad, w tym szczegółów oceny zasad dla zasobu
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1" -Expand "PolicyEvaluationDetails"
```

Umożliwia pobieranie najnowszych rekordów Stanów zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji. Polecenie ogranicza wyniki zwracane przez filtrowanie na podstawie stanu zgodności (dotyczy tylko statusu niezgodnego).
Najpierw grupuje wyniki na podstawie przydziału zasad, definicji zestawu zasad, definicji zasad i identyfikatora zasobu. Następnie grupuje wyniki tego zgrupowania, korzystając z tych samych właściwości, z wyjątkiem identyfikatora zasobu, oraz oblicza liczbę rekordów w każdej z tych grup, która jest zwracana w ramach właściwości AdditionalProperties.
Wyniki są porządkowane według agregacji zliczania w kolejności malejącej, a w tej kolejności są uwzględniane tylko 5 pierwszych.
Spowoduje to wygenerowanie pierwszych 5 zasad z największą liczbą niezgodnych zasobów.

## PARAMETRÓW

### -All
W określonym przedziale czasu Uzyskaj wszystkie Stany zasad zamiast tylko najnowsze.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Expand
Wyrażenie rozwijania przy użyciu notacji OData.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### System. String

## WYSYŁA

### Microsoft. Azure. Commands. PolicyInsights. models. PolicyState

## INFORMACYJN

## LINKI POKREWNE

[Get-AzPolicyStateSummary](./Get-AzPolicyStateSummary.md)
