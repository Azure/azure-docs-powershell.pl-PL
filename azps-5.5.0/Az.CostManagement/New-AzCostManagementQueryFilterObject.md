---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.CostManagement/new-AzCostManagementQueryFilterObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
ms.openlocfilehash: d2adba5ac5c75745c43e0d1ef62fb39d9b867c5e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196675"
---
# New-AzCostManagementQueryFilterObject

## SYNOPSIS
Tworzenie obiektu w pamięci dla Filtru zapytań

## SKŁADNIA

```
New-AzCostManagementQueryFilterObject [-And <IQueryFilter[]>] [-Dimensions <IQueryComparisonExpression>]
 [-Not <IQueryFilter>] [-Or <IQueryFilter[]>] [-Tag <IQueryComparisonExpression>] [<CommonParameters>]
```

## OPIS
Tworzenie obiektu w pamięci dla Filtru zapytań

## PRZYKŁADY

### Przykład 1. Tworzenie obiektu filtru zapytania do eksportowania zarządzania kosztami
```powershell
PS C:\> $orDimension = New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Value @('East US', 'West Europe')
PS C:\> $orTag = New-AzCostManagementQueryComparisonExpressionObject -Name 'Environment' -Value @('UAT', 'Prod')
PS C:\> New-AzCostManagementQueryFilterObject -or @((New-AzCostManagementQueryFilterObject -Dimension $orDimension), (New-AzCostManagementQueryFilterObject -Tag $orTag))

And       :
Dimension : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
Not       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter
Or        : {Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter, Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter}
Tag       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
```

To polecenie tworzy obiekt filtru zapytania do eksportowania zarządzania kosztami.

## PARAMETERS

### — I
Logiczne wyrażenie "ORAZ".
Musi zawierać co najmniej 2 elementy.
Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach ORAZ i utworzyć tabelę skrótu.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Wymiary
Ma wyrażenie porównania wymiarów.
Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach WYMIARY i utworzyć tabelę skrótu.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryComparisonExpression
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Nie
Logiczne wyrażenie "NOT".
Aby skonstruować, zobacz sekcję NOT properties (NOTATKI) i utwórz tabelę skrótów.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Lub
Logiczne wyrażenie "LUB".
Musi zawierać co najmniej 2 elementy.
Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach LUB i utworzyć tabelę skrótu.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Tag
Zawiera wyrażenie porównania tagu.
Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach tagu i utworzyć tabelę skrótu.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryComparisonExpression
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

## DANE WYJŚCIOWE

### Microsoft.Azure.PowerShell.Cmdlet.CostManagement.Models.Api20200601.QueryFilter

## NOTATKI

ALIASY

COMPLEX PARAMETER PROPERTIES

Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości. Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.


AND <IQueryFilter[]>: Wyrażenie logiczne "AND". Musi zawierać co najmniej 2 elementy.
  - `[And <IQueryFilter[]>]`: wyrażenie logiczne "ORAZ". Musi zawierać co najmniej 2 elementy.
  - `[Dimensions <IQueryComparisonExpression>]`: Ma wyrażenie porównania dla wymiaru
    - `Name <String>`: nazwa kolumny, która ma być porównywana.
    - `Value <String[]>`: tablica wartości do użycia w celu porównania
  - `[Not <IQueryFilter>]`: wyrażenie logiczne "NOT".
  - `[Or <IQueryFilter[]>]`: wyrażenie logiczne "LUB". Musi zawierać co najmniej 2 elementy.
  - `[Tag <IQueryComparisonExpression>]`: zawiera wyrażenie porównania tagu

WYMIARY: <IQueryComparisonExpression> zawiera wyrażenie porównania wymiarów.
  - `Name <String>`: nazwa kolumny, która ma być porównywana.
  - `Value <String[]>`: tablica wartości do użycia w celu porównania

NOT: <IQueryFilter> Wyrażenie logiczne "NOT".
  - `[And <IQueryFilter[]>]`: wyrażenie logiczne "ORAZ". Musi zawierać co najmniej 2 elementy.
  - `[Dimensions <IQueryComparisonExpression>]`: Ma wyrażenie porównania dla wymiaru
    - `Name <String>`: nazwa kolumny, która ma być porównywana.
    - `Value <String[]>`: tablica wartości do użycia w celu porównania
  - `[Not <IQueryFilter>]`: wyrażenie logiczne "NOT".
  - `[Or <IQueryFilter[]>]`: wyrażenie logiczne "LUB". Musi zawierać co najmniej 2 elementy.
  - `[Tag <IQueryComparisonExpression>]`: zawiera wyrażenie porównania tagu

OR <IQueryFilter[]>: Wyrażenie logiczne "OR". Musi zawierać co najmniej 2 elementy.
  - `[And <IQueryFilter[]>]`: wyrażenie logiczne "ORAZ". Musi zawierać co najmniej 2 elementy.
  - `[Dimensions <IQueryComparisonExpression>]`: Ma wyrażenie porównania dla wymiaru
    - `Name <String>`: nazwa kolumny, która ma być porównywana.
    - `Value <String[]>`: tablica wartości do użycia w celu porównania
  - `[Not <IQueryFilter>]`: wyrażenie logiczne "NOT".
  - `[Or <IQueryFilter[]>]`: wyrażenie logiczne "LUB". Musi zawierać co najmniej 2 elementy.
  - `[Tag <IQueryComparisonExpression>]`: zawiera wyrażenie porównania tagu

TAG: <IQueryComparisonExpression> Zawiera wyrażenie porównania tagu.
  - `Name <String>`: nazwa kolumny, która ma być porównywana.
  - `Value <String[]>`: tablica wartości do użycia w celu porównania

## LINKI POKREWNE

