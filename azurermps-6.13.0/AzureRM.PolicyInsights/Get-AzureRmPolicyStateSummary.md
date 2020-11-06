---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/get-azurermpolicystatesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyStateSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyStateSummary.md
ms.openlocfilehash: 4b4d45414a9a27561c3be4be195a1e5f77076e6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541599"
---
# Get-AzureRmPolicyStateSummary

## STRESZCZENIe
Pobiera ostatnie podsumowanie stanów zgodności zasad dla zasobów.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### SubscriptionScope (domyślny)
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ManagementGroupScope
```
Get-AzureRmPolicyStateSummary -ManagementGroupName <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupScope
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### PolicySetDefinitionScope
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### PolicyDefinitionScope
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### SubscriptionLevelPolicyAssignmentScope
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceGroupLevelPolicyAssignmentScope
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String>
 -PolicyAssignmentName <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceScope
```
Get-AzureRmPolicyStateSummary -ResourceId <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Umożliwia wyświetlenie podsumowania najnowszych numerów Stanów zgodności zasad w różnych zakresach z podziałem na przypisania zasad i definicje zasad. Obejmuje tylko Stany zasad niezgodne z zasadami.

## Przykłady

### Przykład 1: pobieranie najnowszych niezgodnych Stanów zasad w bieżącym zakresie subskrypcji
```powershell
PS C:\> Get-AzureRmPolicyStateSummary
```

Pobiera Widok podsumowania najnowszych Stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.

### Przykład 2: Uzyskiwanie najnowszych niezgodnych Stanów zasad w określonym zakresie subskrypcji
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

Pobiera Widok podsumowania najnowszych Stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w ramach określonej subskrypcji.

### Przykład 3: pobieranie najnowszych niezgodnych Stanów zasad w zakresie grupy zarządzania
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -ManagementGroupName "myManagementGroup"
```

Pobiera Widok podsumowania najnowszych Stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w określonej grupie zarządzania.

### Przykład 4: pobieranie najnowszych niezgodnych Stanów zasad w zakresie grupy zasobów w bieżącej subskrypcji
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -ResourceGroupName "myResourceGroup"
```

Pobiera Widok podsumowania najnowszych Stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów należących do określonej grupy zasobów (w subskrypcji w kontekście bieżącej sesji).

### Przykład 5: pobieranie najnowszych niezgodnych Stanów zasad w zakresie grupy zasobów w określonej subskrypcji
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

Pobiera Widok podsumowania najnowszych Stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów należących do określonej grupy zasobów (w określonej subskrypcji).

### Przykład 6: uzyskiwanie informacji o najnowszych niezgodnych Stanach zasad dla zasobu
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

Pobiera Widok podsumowania najnowszych Stanów zgodności zasad wygenerowanych w ostatnim dniu określonego zasobu.

### Przykład 7: Pobierz najnowsze niezgodne Stany zasad Podsumowanie dla definicji zestawu zasad w bieżącej subskrypcji
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Pobiera Widok podsumowania najnowszych Stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) realizowanych za pomocą określonej definicji zestawu zasad (która istnieje w kontekście bieżącej sesji).

### Przykład 8: pobieranie najnowszych niezgodnych Stanów zasad dla definicji zestawu zasad w określonej subskrypcji
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Umożliwia wyświetlenie widoku podsumowania najnowszych Stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) za pomocą określonej definicji zestawu zasad (która istnieje w określonej subskrypcji).

### Przykład 9: Pobierz najnowsze niezgodne Stany zasad Podsumowanie dla definicji zasad w bieżącej subskrypcji
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Umożliwia wyświetlenie widoku podsumowania najnowszych Stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) za pomocą określonej definicji zasad (istniejącej w ramach subskrypcji w kontekście bieżącej sesji).

### Przykład 10: pobieranie najnowszych niezgodnych Stanów zasad dla definicji zasad w określonej subskrypcji
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Pobiera Widok podsumowania najnowszych Stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) przeprowadzonych według określonej definicji zasad (która istnieje w określonej subskrypcji).

### Przykład 11: pobieranie najnowszych niezgodnych Stanów zasad dla przypisania zasad w bieżącej subskrypcji
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Pobiera Widok podsumowania najnowszych Stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) realizowanych przez określone przypisanie zasad (istniejące w subskrypcji w bieżącym kontekście sesji).

### Przykład 12: pobieranie najnowszych niezgodnych Stanów zasad dla przypisania zasad w określonej subskrypcji
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Pobiera Widok podsumowania najnowszych Stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) realizowanych przez określone przypisanie zasad (istniejące w określonej subskrypcji).

### Przykład 13: pobieranie najnowszych niezgodnych Stanów zasad dla przydziału zasad w określonej grupie zasobów w bieżącej subskrypcji
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Pobiera Widok podsumowania najnowszych Stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w dzierżawie w bieżącym kontekście sesji) przeprowadzonych przez określone przypisanie zasad (istniejące w grupie zasobów w subskrypcji w bieżącym kontekście sesji).

### Przykład 14: pobieranie najnowszych niezgodnych Stanów zasad w bieżącym zakresie subskrypcji przy użyciu opcji pierwszych kwerend
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -Top 5
```

Pobiera Widok podsumowania najnowszych Stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji. Polecenie porządkuje podsumowania przydziałów w wynikach według liczby niezgodnych zasobów w kolejności malejącej i pobiera tylko 5 najważniejszych podsumowań zadań.

### Przykład 15: Uzyskiwanie najnowszych niezgodnych Stanów zasad w bieżącym zakresie subskrypcji przy użyciu opcji od i do zapytania
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

Pobiera Widok podsumowania najnowszych Stanów zgodności zasad wygenerowanych w zakresie dat określonym dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.

### Przykład 16: pobieranie najnowszych niezgodnych Stanów zasad w bieżącym zakresie subskrypcji za pomocą opcji filtrowania kwerend
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

Pobiera Widok podsumowania najnowszych Stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.
Polecenie ogranicza wyniki zwracane przez filtrowanie na podstawie akcji definicji zasad (obejmuje akcje odmowy lub inspekcji) oraz lokalizację zasobów (z pominięciem lokalizacji wschodniego).

## PARAMETRÓW

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

### Microsoft. Azure. Commands. PolicyInsights. models. PolicyStateSummary

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmPolicyState](./Get-AzureRmPolicyState.md)
