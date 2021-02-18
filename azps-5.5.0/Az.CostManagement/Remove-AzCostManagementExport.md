---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/remove-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Remove-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Remove-AzCostManagementExport.md
ms.openlocfilehash: 75c1f01730d4dfe3e9769a430f874887fd2d2090
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181163"
---
# <span data-ttu-id="fcc36-101">Remove-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="fcc36-101">Remove-AzCostManagementExport</span></span>

## <span data-ttu-id="fcc36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcc36-102">SYNOPSIS</span></span>
<span data-ttu-id="fcc36-103">Operacja usunięcia eksportu.</span><span class="sxs-lookup"><span data-stu-id="fcc36-103">The operation to delete a export.</span></span>

## <span data-ttu-id="fcc36-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fcc36-104">SYNTAX</span></span>

### <span data-ttu-id="fcc36-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="fcc36-105">Delete (Default)</span></span>
```
Remove-AzCostManagementExport -Name <String> -Scope <String> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fcc36-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fcc36-106">DeleteViaIdentity</span></span>
```
Remove-AzCostManagementExport -InputObject <ICostManagementIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fcc36-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="fcc36-107">DESCRIPTION</span></span>
<span data-ttu-id="fcc36-108">Operacja usunięcia eksportu.</span><span class="sxs-lookup"><span data-stu-id="fcc36-108">The operation to delete a export.</span></span>

## <span data-ttu-id="fcc36-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fcc36-109">EXAMPLES</span></span>

### <span data-ttu-id="fcc36-110">Przykład 1. Usunięcie pola AzCostManagementExport według zakresu i nazwy</span><span class="sxs-lookup"><span data-stu-id="fcc36-110">Example 1: Delete the AzCostManagementExport by Scope and Name</span></span>
```powershell
PS C:\> Remove-AzCostManagementExport -Scope 'subscriptions/********' -name 'TestExportDatasetAggregationInfoYouri'


```

<span data-ttu-id="fcc36-111">Usuwanie parametru AzCostManagementExport By Scope i ExportName</span><span class="sxs-lookup"><span data-stu-id="fcc36-111">Delete the AzCostManagementExport By Scope and ExportName</span></span>

### <span data-ttu-id="fcc36-112">Przykład 2. Usuwanie obiektu AzCostManagementExport przez obiekt Export</span><span class="sxs-lookup"><span data-stu-id="fcc36-112">Example 2: Delete the AzCostManagementExport by Export Object</span></span>
```powershell
PS C:\> $getExport = Get-AzCostManagementExport -Scope 'subscriptions/*********' -name 'TestExportDatasetAggregationYouori'
Remove-AzCostManagementExport -InputObject $getExport


```

<span data-ttu-id="fcc36-113">Usuwanie pola AzCostManagementExport by InputObject</span><span class="sxs-lookup"><span data-stu-id="fcc36-113">Delete the AzCostManagementExport By InputObject</span></span>

## <span data-ttu-id="fcc36-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fcc36-114">PARAMETERS</span></span>

### <span data-ttu-id="fcc36-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcc36-115">-DefaultProfile</span></span>
<span data-ttu-id="fcc36-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fcc36-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcc36-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fcc36-117">-InputObject</span></span>
<span data-ttu-id="fcc36-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="fcc36-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fcc36-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fcc36-119">-Name</span></span>
<span data-ttu-id="fcc36-120">Eksportuj nazwę.</span><span class="sxs-lookup"><span data-stu-id="fcc36-120">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ExportName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcc36-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fcc36-121">-PassThru</span></span>
<span data-ttu-id="fcc36-122">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="fcc36-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="fcc36-123">— Zakres</span><span class="sxs-lookup"><span data-stu-id="fcc36-123">-Scope</span></span>
<span data-ttu-id="fcc36-124">Ten parametr definiuje zakres zarządzania kosztami z różnych perspektyw: "Subskrypcja", "Grupa zasobów" i "Udostępnij usługę".</span><span class="sxs-lookup"><span data-stu-id="fcc36-124">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcc36-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fcc36-125">-Confirm</span></span>
<span data-ttu-id="fcc36-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fcc36-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcc36-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcc36-127">-WhatIf</span></span>
<span data-ttu-id="fcc36-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fcc36-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcc36-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="fcc36-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcc36-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcc36-130">CommonParameters</span></span>
<span data-ttu-id="fcc36-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcc36-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcc36-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fcc36-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcc36-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fcc36-133">INPUTS</span></span>

### <span data-ttu-id="fcc36-134">Microsoft.Azure.PowerShell.Cmdlet.CostManagement.Models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="fcc36-134">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="fcc36-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fcc36-135">OUTPUTS</span></span>

### <span data-ttu-id="fcc36-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fcc36-136">System.Boolean</span></span>

## <span data-ttu-id="fcc36-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fcc36-137">NOTES</span></span>

<span data-ttu-id="fcc36-138">ALIASY</span><span class="sxs-lookup"><span data-stu-id="fcc36-138">ALIASES</span></span>

<span data-ttu-id="fcc36-139">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="fcc36-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fcc36-140">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="fcc36-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fcc36-141">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fcc36-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fcc36-142">INPUTOBJECT: <ICostManagementIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="fcc36-142">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fcc36-143">`[AlertId <String>]`: Identyfikator alertu</span><span class="sxs-lookup"><span data-stu-id="fcc36-143">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="fcc36-144">`[ExportName <String>]`: Eksportuj nazwę.</span><span class="sxs-lookup"><span data-stu-id="fcc36-144">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="fcc36-145">`[ExternalCloudProviderId <String>]`: W przypadku konta połączonego może to być wartość "{externalSubscriptionId}" lub "{externalBillingAccountId}" w przypadku skonsolidowanego konta używanego z operacjami wymiaru/zapytania.</span><span class="sxs-lookup"><span data-stu-id="fcc36-145">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="fcc36-146">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: Typ dostawcy chmury zewnętrznej skojarzony z operacjami wymiaru/zapytania.</span><span class="sxs-lookup"><span data-stu-id="fcc36-146">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="fcc36-147">Obejmuje to "zewnętrzneSubskrypcje" dla konta połączonego i "externalBillingAccounts" dla skonsolidowanego konta.</span><span class="sxs-lookup"><span data-stu-id="fcc36-147">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="fcc36-148">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="fcc36-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fcc36-149">`[Scope <String>]`: Zakres skojarzony z operacjami wyświetlania.</span><span class="sxs-lookup"><span data-stu-id="fcc36-149">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="fcc36-150">Obejmuje to "subskrypcje/{subscriptionId}" dla zakresu subskrypcji, "subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}" dla zakresu resourceGroup, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' dla zakresu Konto rozliczeniowe, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' dla zakresu Dział, "providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}" dla zakresu EnrollmentAccount, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management /managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span><span class="sxs-lookup"><span data-stu-id="fcc36-150">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="fcc36-151">`[ViewName <String>]`: nazwa widoku</span><span class="sxs-lookup"><span data-stu-id="fcc36-151">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="fcc36-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fcc36-152">RELATED LINKS</span></span>

