---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/get-azpolicystatesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
ms.openlocfilehash: 09fce075ae0f6d8c55f5ef18d070a72daafa2cac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989087"
---
# Get-AzPolicyStateSummary

## SYNOPSIS
Pobiera podsumowanie najnowszych stanów zgodności zasad dla zasobów.

## SKŁADNIA

### SubscriptionScope (domyślne)
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ManagementGroupScope
```
Get-AzPolicyStateSummary -ManagementGroupName <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupScope
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### PolicySetDefinitionScope
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### PolicyDefinitionScope
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### SubscriptionLevelPolicyAssignmentScope
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceGroupLevelPolicyAssignmentScope
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceScope
```
Get-AzPolicyStateSummary -ResourceId <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Wyświetla podsumowanie najnowszych numerów stanu zgodności zasad w różnych zakresach, podzielone na przydziały zasad i definicje zasad. Obejmuje ono tylko stany niezgodnych zasad.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie podsumowania najnowszych stanów niezgodnych zasad w bieżącym zakresie subskrypcji
```powershell
PS C:\> Get-AzPolicyStateSummary
```

Pobiera widok podsumowania najnowszych stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.

### Przykład 2. Uzyskiwanie podsumowania najnowszych stanów niezgodnych zasad w określonym zakresie subskrypcji
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

Pobiera widok podsumowania najnowszych stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w ramach określonej subskrypcji.

### Przykład 3. Uzyskiwanie podsumowania najnowszych stanów niezgodnych zasad w zakresie grupy zarządzania
```powershell
PS C:\> Get-AzPolicyStateSummary -ManagementGroupName "myManagementGroup"
```

Pobiera widok podsumowania najnowszych stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w określonej grupie zarządzania.

### Przykład 4. Uzyskiwanie podsumowania najnowszych stanów niezgodnych zasad w zakresie grupy zasobów w bieżącej subskrypcji
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup"
```

Pobiera widok podsumowania najnowszych stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w określonej grupie zasobów (w ramach subskrypcji w bieżącym kontekście sesji).

### Przykład 5. Uzyskiwanie podsumowania najnowszych stanów niezgodnych zasad w zakresie grupy zasobów w określonej subskrypcji
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

Pobiera widok podsumowania najnowszych stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w określonej grupie zasobów (w określonej subskrypcji).

### Przykład 6. Uzyskiwanie podsumowania najnowszych stanów niezgodnych zasad dla zasobu
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

Pobiera widok podsumowania najnowszych stanów zgodności zasad wygenerowanych w ostatnim dniu dla określonego zasobu.

### Przykład 7. Uzyskiwanie podsumowania najnowszych stanów niezgodnych zasad dla definicji zestawu zasad w bieżącej subskrypcji
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Pobiera widok podsumowania najnowszych stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w ramach dzierżawy w bieżącym kontekście sesji), na które wpływa określona definicja zestawu zasad (która istnieje w subskrypcji w bieżącym kontekście sesji).

### Przykład 8. Uzyskiwanie podsumowania najnowszych stanów niezgodnych zasad dla definicji zestawu zasad w określonej subskrypcji
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Pobiera widok podsumowania najnowszych stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w ramach dzierżawy w bieżącym kontekście sesji), na które wpływa określona definicja zestawu zasad (która istnieje w określonej subskrypcji).

### Przykład 9. Uzyskiwanie podsumowania najnowszych stanów niezgodnych zasad dla definicji zasad w bieżącej subskrypcji
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Pobiera widok podsumowania najnowszych stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w ramach dzierżawy w bieżącym kontekście sesji), na które wpływa określona definicja zasad (która istnieje w subskrypcji w bieżącym kontekście sesji).

### Przykład 10. Uzyskiwanie podsumowania najnowszych stanów niezgodnych zasad dla definicji zasad w określonej subskrypcji
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Pobiera widok podsumowania najnowszych stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w ramach dzierżawy w bieżącym kontekście sesji), na które wpływa określona definicja zasad (która istnieje w określonej subskrypcji).

### Przykład 11. Uzyskiwanie podsumowania najnowszych stanów niezgodnych zasad dla przydziału zasad w bieżącej subskrypcji
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Pobiera widok podsumowania najnowszych stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w ramach dzierżawy w bieżącym kontekście sesji), na które wpływa przypisanie określonych zasad (które istnieje w subskrypcji w bieżącym kontekście sesji).

### Przykład 12. Uzyskiwanie podsumowania najnowszych stanów niezgodnych zasad dla przypisania zasad w określonej subskrypcji
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Pobiera widok podsumowania najnowszych stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów (w ramach dzierżawy w bieżącym kontekście sesji), na które wpływa przypisanie określonych zasad (istnieje w określonej subskrypcji).

### Przykład 13. Uzyskiwanie podsumowania najnowszych stanów niezgodnych zasad dla przydziału zasad w określonej grupie zasobów w bieżącej subskrypcji
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Pobiera widok podsumowania najnowszych stanów zgodności zasad wygenerowany w ostatnim dniu dla wszystkich zasobów (w ramach dzierżawy w bieżącym kontekście sesji), na które wpływa przypisanie określonych zasad (które istnieje w grupie zasobów w ramach subskrypcji w bieżącym kontekście sesji).

### Przykład 14. Uzyskiwanie podsumowania najnowszych stanów niezgodnych zasad w bieżącym zakresie subskrypcji z opcją Zapytanie najlepsze
```powershell
PS C:\> Get-AzPolicyStateSummary -Top 5
```

Pobiera widok podsumowania najnowszych stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji. Polecenie uporządkuje podsumowania przydziałów zasad w wynikach według niezgodnych liczników zasobów w kolejności malejącej i przyjmuje tylko 5 najwyższych sum tych podsumowań przydziałów zasad.

### Przykład 15. Uzyskiwanie podsumowania najnowszych stanów niezgodnych zasad w bieżącym zakresie subskrypcji z opcjami zapytania Od i Do
```powershell
PS C:\> Get-AzPolicyStateSummary -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

Pobiera widok podsumowania najnowszych stanów zgodności zasad generowanych w zakresie dat określonym dla wszystkich zasobów w ramach subskrypcji w kontekście bieżącej sesji.

### Przykład 16. Uzyskiwanie podsumowania najnowszych niezgodnych stanów zasad w bieżącym zakresie subskrypcji z opcją zapytania filtru
```powershell
PS C:\> Get-AzPolicyStateSummary -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

Pobiera widok podsumowania najnowszych stanów zgodności zasad wygenerowanych w ostatnim dniu dla wszystkich zasobów w ramach subskrypcji w bieżącym kontekście sesji.
To polecenie ogranicza wyniki zwracane przez filtrowanie na podstawie akcji definicji zasad (obejmuje akcje odmawiania lub inspekcji) i lokalizację zasobu (z wyłączeniem lokalizacji na wschód).

## PARAMETERS

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

### Microsoft.Azure.Commands.PolicyInsights.Models.PolicyStateSummary

## NOTATKI

## LINKI POKREWNE

[Get-AzPolicyState](./Get-AzPolicyState.md)
