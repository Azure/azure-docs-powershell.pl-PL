---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/get-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExport.md
ms.openlocfilehash: 269a58e57510f6b0945218645ec079b21b606e44
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196698"
---
# Get-AzCostManagementExport

## SYNOPSIS
Operacja uzyskania eksportu dla zdefiniowanego zakresu według nazwy eksportu.

## SKŁADNIA

### Lista (domyślna)
```
Get-AzCostManagementExport -Scope <String> [-Expand <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### Pobierz
```
Get-AzCostManagementExport -Name <String> -Scope <String> [-Expand <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzCostManagementExport -InputObject <ICostManagementIdentity> [-Expand <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## OPIS
Operacja uzyskania eksportu dla zdefiniowanego zakresu według nazwy eksportu.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie wszystkich azCostManagementExports według zakresu
```powershell
PS C:\> Get-AzCostManagementExport -Scope 'subscriptions/**********'

ETag              Name                               Type
----              ----                               ----
"************" TestExport                         Microsoft.CostManagement/exports
"************" TestExport1                        Microsoft.CostManagement/exports
"************" TestExport2                        Microsoft.CostManagement/exports
```

Pobierz wszystkie raporty AzCostManagementExports według zakresu

### Przykład 2. Pobierz azCostManagementExport według nazwy i zakresu
```powershell
PS C:\> Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'

ETag              Name       Type
----              ----       ----
"************" TestExport Microsoft.CostManagement/exports
```

Get AzCostManagementExport by Name and scope

## PARAMETERS

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Rozwiń
Może być używany do rozwijania właściwości w ramach eksportu.
Obecnie jest obsługiwana tylko część "runHistory", która zwraca informacje dotyczące ostatnich 10 wykonywania eksportu.

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

### -InputObject
Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### — Nazwa
Eksportuj nazwę.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ExportName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Zakres
Ten parametr definiuje zakres zarządzania kosztami z innej perspektywy: "Subskrypcja", "Grupa zasobów" i "Udostępnij usługę".

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Microsoft.Azure.PowerShell.Cmdlet.CostManagement.Models.ICostManagementIdentity

## OUTPUTS

### Microsoft.Azure.PowerShell.Cmdlet.CostManagement.Models.Api20200601.IExport

## NOTATKI

ALIASY

COMPLEX PARAMETER PROPERTIES

Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości. Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.


INPUTOBJECT: <ICostManagementIdentity> Parametr tożsamości
  - `[AlertId <String>]`: Identyfikator alertu
  - `[ExportName <String>]`: Eksportuj nazwę.
  - `[ExternalCloudProviderId <String>]`: W przypadku konta połączonego może to być wartość "{externalSubscriptionId}" lub "{externalBillingAccountId}" w przypadku skonsolidowanego konta używanego z operacjami wymiaru/zapytania.
  - `[ExternalCloudProviderType <ExternalCloudProviderType?>]`: Typ dostawcy chmury zewnętrznej skojarzony z operacjami wymiaru/zapytania. Obejmuje to "zewnętrzneSubskrypcje" dla konta połączonego i "externalBillingAccounts" dla skonsolidowanego konta.
  - `[Id <String>]`: ścieżka tożsamości zasobu
  - `[Scope <String>]`: zakres skojarzony z operacjami wyświetlania. Obejmuje to "subskrypcje/{subscriptionId}" dla zakresu subskrypcji, "subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}" dla zakresu resourceGroup, "providers/Microsoft.Billing/billingAccounts/{billingAccountId}" dla zakresu Konto rozliczeniowe, "providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}" dla zakresu Dział, "providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}" dla zakresu EnrollmentAccount, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management /managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.
  - `[ViewName <String>]`: nazwa widoku

## LINKI POKREWNE

