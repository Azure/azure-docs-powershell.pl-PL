---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.CostManagement/new-AzCostManagementQueryFilterObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
ms.openlocfilehash: e7b5c605af531bd1c1251a1c615da9498059d43d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336613"
---
# New-AzCostManagementQueryFilterObject

## STRESZCZENIe
Tworzenie obiektu w pamięci dla QueryFilter

## POLECENIA

```
New-AzCostManagementQueryFilterObject [-And <IQueryFilter[]>] [-Dimensions <IQueryComparisonExpression>]
 [-Not <IQueryFilter>] [-Or <IQueryFilter[]>] [-Tag <IQueryComparisonExpression>] [<CommonParameters>]
```

## Opis
Tworzenie obiektu w pamięci dla QueryFilter

## Przykłady

### Przykład 1. Tworzenie obiektu filtru zapytania na potrzeby eksportu zarządzania kosztami
```powershell
PS C:\> $orDimension = New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Operator In -Value @('East US', 'West Europe')
PS C:\> $orTag = New-AzCostManagementQueryComparisonExpressionObject -Name 'Environment' -Operator In -Value @('UAT', 'Prod')
PS C:\> New-AzCostManagementQueryFilterObject -or @((New-AzCostManagementQueryFilterObject -Dimension $orDimension), (New-AzCostManagementQueryFilterObject -Tag $orTag))

And       :
Dimension : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
Not       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter
Or        : {Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter, Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter}
Tag       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
```

to polecenie tworzy obiekt Filter zapytania na potrzeby eksportu zarządzania kosztami.

## PARAMETRÓW

### -And
Wyrażenie logiczne "AND".
Musi zawierać co najmniej 2 elementy.
Aby skonstruować, zobacz sekcję notatki i właściwości i Utwórz tablicę skrótów.

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

### -Dimensions
Zawiera wyrażenie porównania wymiarów.
Aby skonstruować, zobacz sekcję notatki dla właściwości wymiarów i Utwórz tablicę skrótów.

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

### -Not
Logiczne wyrażenie "NOT".
Aby skonstruować, zobacz sekcję notatki dla właściwości NOT Properties i Utwórz tablicę skrótów.

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

### -Or
Wyrażenie logiczne "OR".
Musi zawierać co najmniej 2 elementy.
Aby skonstruować, zobacz sekcję notatek dla lub właściwości i Utwórz tablicę skrótów.

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

### -Tag
Zawiera wyrażenie porównania dla znacznika.
Aby skonstruować, zobacz sekcję notatki dla właściwości ZNACZNIKÓW i Utwórz tablicę skrótów.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

## WYSYŁA

### Microsoft. Azure. PowerShell. polecenia. CostManagement. models. Api20200601. QueryFilter

## INFORMACYJN

PISUJE

ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW

Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości. Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.


I <IQueryFilter [] >: wyrażenie logiczne "AND". Musi zawierać co najmniej 2 elementy.
  - `[And <IQueryFilter[]>]`: Wyrażenie logiczne "AND". Musi zawierać co najmniej 2 elementy.
  - `[Dimensions <IQueryComparisonExpression>]`: Zawiera wyrażenie porównania dla wymiaru
    - `Name <String>`: Nazwa kolumny, która ma być używana w porównaniu.
    - `Operator <OperatorType>`: Operator używany do porównywania.
    - `Value <String[]>`: Tablica wartości do użycia w porównaniu
  - `[Not <IQueryFilter>]`: Logiczne wyrażenie "NOT".
  - `[Or <IQueryFilter[]>]`: Wyrażenie logiczne "OR". Musi zawierać co najmniej 2 elementy.
  - `[Tag <IQueryComparisonExpression>]`: Zawiera wyrażenie porównania dla znacznika

Wymiary <IQueryComparisonExpression> : zawiera wyrażenie porównawcze dla wymiarów.
  - `Name <String>`: Nazwa kolumny, która ma być używana w porównaniu.
  - `Operator <OperatorType>`: Operator używany do porównywania.
  - `Value <String[]>`: Tablica wartości do użycia w porównaniu

NOT <IQueryFilter> : logiczne wyrażenie "not".
  - `[And <IQueryFilter[]>]`: Wyrażenie logiczne "AND". Musi zawierać co najmniej 2 elementy.
  - `[Dimensions <IQueryComparisonExpression>]`: Zawiera wyrażenie porównania dla wymiaru
    - `Name <String>`: Nazwa kolumny, która ma być używana w porównaniu.
    - `Operator <OperatorType>`: Operator używany do porównywania.
    - `Value <String[]>`: Tablica wartości do użycia w porównaniu
  - `[Not <IQueryFilter>]`: Logiczne wyrażenie "NOT".
  - `[Or <IQueryFilter[]>]`: Wyrażenie logiczne "OR". Musi zawierać co najmniej 2 elementy.
  - `[Tag <IQueryComparisonExpression>]`: Zawiera wyrażenie porównania dla znacznika

LUB <IQueryFilter [] >: wyrażenie logiczne "OR". Musi zawierać co najmniej 2 elementy.
  - `[And <IQueryFilter[]>]`: Wyrażenie logiczne "AND". Musi zawierać co najmniej 2 elementy.
  - `[Dimensions <IQueryComparisonExpression>]`: Zawiera wyrażenie porównania dla wymiaru
    - `Name <String>`: Nazwa kolumny, która ma być używana w porównaniu.
    - `Operator <OperatorType>`: Operator używany do porównywania.
    - `Value <String[]>`: Tablica wartości do użycia w porównaniu
  - `[Not <IQueryFilter>]`: Logiczne wyrażenie "NOT".
  - `[Or <IQueryFilter[]>]`: Wyrażenie logiczne "OR". Musi zawierać co najmniej 2 elementy.
  - `[Tag <IQueryComparisonExpression>]`: Zawiera wyrażenie porównania dla znacznika

TAG <IQueryComparisonExpression> : zawiera wyrażenie porównania dla znacznika.
  - `Name <String>`: Nazwa kolumny, która ma być używana w porównaniu.
  - `Operator <OperatorType>`: Operator używany do porównywania.
  - `Value <String[]>`: Tablica wartości do użycia w porównaniu

## LINKI POKREWNE

