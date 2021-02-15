---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/invoke-azcostmanagementexecuteexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementExecuteExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementExecuteExport.md
ms.openlocfilehash: 752af43a72151296c4c90ecc32923a786c7b4081
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196691"
---
# Invoke-AzCostManagementExecuteExport

## SYNOPSIS
Operacja wykonywania eksportu.

## SKŁADNIA

### Wykonywanie (domyślne)
```
Invoke-AzCostManagementExecuteExport -ExportName <String> -Scope <String> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ExecuteViaIdentity
```
Invoke-AzCostManagementExecuteExport -InputObject <ICostManagementIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## OPIS
Operacja wykonywania eksportu.

## PRZYKŁADY

### Przykład 1. Wywoływanie eksportowania według wartości ExportName i Scope
```powershell
PS C:\> Invoke-AzCostManagementExecuteExport -ExportName 'TestExport' -Scope 'subscriptions/**********'

```

Wywoływanie eksportowania według nazwa_eksportu i zakresu

### Przykład 2. Wywoływanie eksportowania przez inputObject
```powershell
PS C:\> $getExport = Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'
Invoke-AzCostManagementExecuteExport -InputObject $getExport

```

Invoke Export by InputObject

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

### -ExportName
Eksportuj nazwę.

```yaml
Type: System.String
Parameter Sets: Execute
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity
Parameter Sets: ExecuteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PassThru
Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.

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

### — Zakres
Ten parametr definiuje zakres zarządzania kosztami z innej perspektywy: "Subskrypcja", "Grupa zasobów" i "Udostępnij usługę".

```yaml
Type: System.String
Parameter Sets: Execute
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Potwierdź
Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.
Polecenie cmdlet nie zostanie uruchomione.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Microsoft.Azure.PowerShell.Cmdlet.CostManagement.Models.ICostManagementIdentity

## DANE WYJŚCIOWE

### System.Boolean

## NOTATKI

ALIASY

COMPLEX PARAMETER PROPERTIES

Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości. Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.


INPUTOBJECT: <ICostManagementIdentity> Parametr tożsamości
  - `[AlertId <String>]`: Identyfikator alertu
  - `[ExportName <String>]`: Eksportuj nazwę.
  - `[ExternalCloudProviderId <String>]`: W przypadku konta połączonego może to być wartość "{externalSubscriptionId}" lub "{externalBillingAccountId}" w przypadku skonsolidowanego konta używanego z operacjami wymiaru/zapytania.
  - `[ExternalCloudProviderType <ExternalCloudProviderType?>]`: Typ dostawcy chmury zewnętrznej skojarzony z operacjami wymiar/kwerenda. Obejmuje to "zewnętrzneSubskrypcje" dla konta połączonego i "externalBillingAccounts" dla skonsolidowanego konta.
  - `[Id <String>]`: ścieżka tożsamości zasobu
  - `[Scope <String>]`: Zakres skojarzony z operacjami wyświetlania. Obejmuje to "subskrypcje/{subscriptionId}" dla zakresu subskrypcji, "subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}" dla zakresu resourceGroup, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' dla zakresu Konto rozliczeniowe, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' dla zakresu Dział, "providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}" dla zakresu EnrollmentAccount, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management /managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.
  - `[ViewName <String>]`: nazwa widoku

## LINKI POKREWNE

