---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/get-azcostmanagementexportexecutionhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExportExecutionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExportExecutionHistory.md
ms.openlocfilehash: 7bb337837f9bd2be532c4eead8d8379b7cf04fe9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181211"
---
# <span data-ttu-id="d4763-101">Get-AzCostManagementExportExecutionHistory</span><span class="sxs-lookup"><span data-stu-id="d4763-101">Get-AzCostManagementExportExecutionHistory</span></span>

## <span data-ttu-id="d4763-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4763-102">SYNOPSIS</span></span>
<span data-ttu-id="d4763-103">Operacja w celu uzyskania historii wykonywania eksportu dla zdefiniowanego zakresu i nazwy eksportu.</span><span class="sxs-lookup"><span data-stu-id="d4763-103">The operation to get the execution history of an export for the defined scope and export name.</span></span>

## <span data-ttu-id="d4763-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d4763-104">SYNTAX</span></span>

### <span data-ttu-id="d4763-105">Pobierz (domyślne)</span><span class="sxs-lookup"><span data-stu-id="d4763-105">Get (Default)</span></span>
```
Get-AzCostManagementExportExecutionHistory -ExportName <String> -Scope <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="d4763-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d4763-106">GetViaIdentity</span></span>
```
Get-AzCostManagementExportExecutionHistory -InputObject <ICostManagementIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="d4763-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d4763-107">DESCRIPTION</span></span>
<span data-ttu-id="d4763-108">Operacja w celu uzyskania historii wykonywania eksportu dla zdefiniowanego zakresu i nazwy eksportu.</span><span class="sxs-lookup"><span data-stu-id="d4763-108">The operation to get the execution history of an export for the defined scope and export name.</span></span>

## <span data-ttu-id="d4763-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d4763-109">EXAMPLES</span></span>

### <span data-ttu-id="d4763-110">Przykład 1. Pobierz azCostManagementExportExecutionHistory</span><span class="sxs-lookup"><span data-stu-id="d4763-110">Example 1: Get AzCostManagementExportExecutionHistory</span></span>
```powershell
PS C:\> Get-AzCostManagementExportExecutionHistory -ExportName 'TestExport' -Scope 'subscriptions/**********'

ExecutionType ProcessingStartTime ProcessingEndTime  Status    FileName
------------- ------------------- -----------------  ------    --------
Scheduled     2020/6/11 12:03:20  2020/6/11 12:03:43 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
Scheduled     2020/6/12 12:03:37  2020/6/12 12:03:48 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
```

<span data-ttu-id="d4763-111">Get AzCostManagementExportExecutionHistory By ExportName and Scope</span><span class="sxs-lookup"><span data-stu-id="d4763-111">Get AzCostManagementExportExecutionHistory By ExportName and Scope</span></span>

### <span data-ttu-id="d4763-112">Przykład 2. Pobierz azCostManagementExportExecutionHistory by InputObject</span><span class="sxs-lookup"><span data-stu-id="d4763-112">Example 2: Get AzCostManagementExportExecutionHistory by InputObject</span></span>
```powershell
PS C:\> $getExport = Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'
Get-AzCostManagementExportExecutionHistory -InputObject $getExport

ExecutionType ProcessingStartTime ProcessingEndTime  Status    FileName
------------- ------------------- -----------------  ------    --------
Scheduled     2020/6/11 12:03:20  2020/6/11 12:03:43 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
Scheduled     2020/6/12 12:03:37  2020/6/12 12:03:48 Completed ad-hoc/TestExport/20200601-20200630/
```

<span data-ttu-id="d4763-113">Pobierz azCostManagementExportExecutionHistory by InputObject</span><span class="sxs-lookup"><span data-stu-id="d4763-113">Get AzCostManagementExportExecutionHistory By InputObject</span></span>

## <span data-ttu-id="d4763-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4763-114">PARAMETERS</span></span>

### <span data-ttu-id="d4763-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4763-115">-DefaultProfile</span></span>
<span data-ttu-id="d4763-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d4763-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4763-117">-ExportName</span><span class="sxs-lookup"><span data-stu-id="d4763-117">-ExportName</span></span>
<span data-ttu-id="d4763-118">Eksportuj nazwę.</span><span class="sxs-lookup"><span data-stu-id="d4763-118">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4763-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4763-119">-InputObject</span></span>
<span data-ttu-id="d4763-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="d4763-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d4763-121">— Zakres</span><span class="sxs-lookup"><span data-stu-id="d4763-121">-Scope</span></span>
<span data-ttu-id="d4763-122">Ten parametr definiuje zakres zarządzania kosztami z innej perspektywy: "Subskrypcja", "Grupa zasobów" i "Udostępnij usługę".</span><span class="sxs-lookup"><span data-stu-id="d4763-122">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4763-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4763-123">CommonParameters</span></span>
<span data-ttu-id="d4763-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4763-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4763-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d4763-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4763-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d4763-126">INPUTS</span></span>

### <span data-ttu-id="d4763-127">Microsoft.Azure.PowerShell.Cmdlet.CostManagement.Models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="d4763-127">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="d4763-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d4763-128">OUTPUTS</span></span>

### <span data-ttu-id="d4763-129">Microsoft.Azure.PowerShell.Cmdlet.CostManagement.Models.Api20200601.IExportExecution</span><span class="sxs-lookup"><span data-stu-id="d4763-129">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExportExecution</span></span>

## <span data-ttu-id="d4763-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d4763-130">NOTES</span></span>

<span data-ttu-id="d4763-131">ALIASY</span><span class="sxs-lookup"><span data-stu-id="d4763-131">ALIASES</span></span>

<span data-ttu-id="d4763-132">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="d4763-132">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d4763-133">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="d4763-133">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d4763-134">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d4763-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d4763-135">INPUTOBJECT: <ICostManagementIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="d4763-135">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d4763-136">`[AlertId <String>]`: Identyfikator alertu</span><span class="sxs-lookup"><span data-stu-id="d4763-136">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="d4763-137">`[ExportName <String>]`: Eksportuj nazwę.</span><span class="sxs-lookup"><span data-stu-id="d4763-137">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="d4763-138">`[ExternalCloudProviderId <String>]`: W przypadku konta połączonego może to być wartość "{externalSubscriptionId}" lub "{externalBillingAccountId}" w przypadku skonsolidowanego konta używanego z operacjami wymiaru/zapytania.</span><span class="sxs-lookup"><span data-stu-id="d4763-138">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="d4763-139">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: Typ dostawcy chmury zewnętrznej skojarzony z operacjami wymiar/kwerenda.</span><span class="sxs-lookup"><span data-stu-id="d4763-139">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="d4763-140">Obejmuje to "zewnętrzneSubskrypcje" dla konta połączonego i "externalBillingAccounts" dla skonsolidowanego konta.</span><span class="sxs-lookup"><span data-stu-id="d4763-140">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="d4763-141">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="d4763-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d4763-142">`[Scope <String>]`: zakres skojarzony z operacjami wyświetlania.</span><span class="sxs-lookup"><span data-stu-id="d4763-142">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="d4763-143">Obejmuje to "subskrypcje/{subscriptionId}" dla zakresu subskrypcji, "subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}" dla zakresu resourceGroup, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' dla zakresu Konto rozliczeniowe, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' dla zakresu Dział, "providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}" dla zakresu EnrollmentAccount, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management /managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span><span class="sxs-lookup"><span data-stu-id="d4763-143">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="d4763-144">`[ViewName <String>]`: nazwa widoku</span><span class="sxs-lookup"><span data-stu-id="d4763-144">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="d4763-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d4763-145">RELATED LINKS</span></span>

