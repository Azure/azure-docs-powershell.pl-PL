---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/get-azcostmanagementexportexecutionhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExportExecutionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExportExecutionHistory.md
ms.openlocfilehash: 7bb337837f9bd2be532c4eead8d8379b7cf04fe9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501676"
---
# <span data-ttu-id="7c1ce-101">Get-AzCostManagementExportExecutionHistory</span><span class="sxs-lookup"><span data-stu-id="7c1ce-101">Get-AzCostManagementExportExecutionHistory</span></span>

## <span data-ttu-id="7c1ce-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7c1ce-102">SYNOPSIS</span></span>
<span data-ttu-id="7c1ce-103">Operacja pobierania historii wykonania eksportu dla określonego zakresu i nazwy eksportu.</span><span class="sxs-lookup"><span data-stu-id="7c1ce-103">The operation to get the execution history of an export for the defined scope and export name.</span></span>

## <span data-ttu-id="7c1ce-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7c1ce-104">SYNTAX</span></span>

### <span data-ttu-id="7c1ce-105">Get (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="7c1ce-105">Get (Default)</span></span>
```
Get-AzCostManagementExportExecutionHistory -ExportName <String> -Scope <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="7c1ce-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7c1ce-106">GetViaIdentity</span></span>
```
Get-AzCostManagementExportExecutionHistory -InputObject <ICostManagementIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="7c1ce-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7c1ce-107">DESCRIPTION</span></span>
<span data-ttu-id="7c1ce-108">Operacja pobierania historii wykonania eksportu dla określonego zakresu i nazwy eksportu.</span><span class="sxs-lookup"><span data-stu-id="7c1ce-108">The operation to get the execution history of an export for the defined scope and export name.</span></span>

## <span data-ttu-id="7c1ce-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7c1ce-109">EXAMPLES</span></span>

### <span data-ttu-id="7c1ce-110">Przykład 1: Get AzCostManagementExportExecutionHistory</span><span class="sxs-lookup"><span data-stu-id="7c1ce-110">Example 1: Get AzCostManagementExportExecutionHistory</span></span>
```powershell
PS C:\> Get-AzCostManagementExportExecutionHistory -ExportName 'TestExport' -Scope 'subscriptions/**********'

ExecutionType ProcessingStartTime ProcessingEndTime  Status    FileName
------------- ------------------- -----------------  ------    --------
Scheduled     2020/6/11 12:03:20  2020/6/11 12:03:43 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
Scheduled     2020/6/12 12:03:37  2020/6/12 12:03:48 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
```

<span data-ttu-id="7c1ce-111">Uzyskiwanie AzCostManagementExportExecutionHistory przez Eksportname i zakres</span><span class="sxs-lookup"><span data-stu-id="7c1ce-111">Get AzCostManagementExportExecutionHistory By ExportName and Scope</span></span>

### <span data-ttu-id="7c1ce-112">Przykład 2: Get AzCostManagementExportExecutionHistory przez Inputobject</span><span class="sxs-lookup"><span data-stu-id="7c1ce-112">Example 2: Get AzCostManagementExportExecutionHistory by InputObject</span></span>
```powershell
PS C:\> $getExport = Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'
Get-AzCostManagementExportExecutionHistory -InputObject $getExport

ExecutionType ProcessingStartTime ProcessingEndTime  Status    FileName
------------- ------------------- -----------------  ------    --------
Scheduled     2020/6/11 12:03:20  2020/6/11 12:03:43 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
Scheduled     2020/6/12 12:03:37  2020/6/12 12:03:48 Completed ad-hoc/TestExport/20200601-20200630/
```

<span data-ttu-id="7c1ce-113">Pobierz AzCostManagementExportExecutionHistory przez wejście</span><span class="sxs-lookup"><span data-stu-id="7c1ce-113">Get AzCostManagementExportExecutionHistory By InputObject</span></span>

## <span data-ttu-id="7c1ce-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7c1ce-114">PARAMETERS</span></span>

### <span data-ttu-id="7c1ce-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c1ce-115">-DefaultProfile</span></span>
<span data-ttu-id="7c1ce-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7c1ce-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c1ce-117">-Exportname</span><span class="sxs-lookup"><span data-stu-id="7c1ce-117">-ExportName</span></span>
<span data-ttu-id="7c1ce-118">Eksportuj nazwę.</span><span class="sxs-lookup"><span data-stu-id="7c1ce-118">Export Name.</span></span>

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

### <span data-ttu-id="7c1ce-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7c1ce-119">-InputObject</span></span>
<span data-ttu-id="7c1ce-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="7c1ce-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7c1ce-121">-Zakres</span><span class="sxs-lookup"><span data-stu-id="7c1ce-121">-Scope</span></span>
<span data-ttu-id="7c1ce-122">Ten parametr definiuje zakres costmanagement z różnych perspektyw "abonament", "Resources" i "świadczenie usługi".</span><span class="sxs-lookup"><span data-stu-id="7c1ce-122">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="7c1ce-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c1ce-123">CommonParameters</span></span>
<span data-ttu-id="7c1ce-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c1ce-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c1ce-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7c1ce-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c1ce-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7c1ce-126">INPUTS</span></span>

### <span data-ttu-id="7c1ce-127">Microsoft. Azure. PowerShell. polecenia. CostManagement. models. ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="7c1ce-127">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="7c1ce-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7c1ce-128">OUTPUTS</span></span>

### <span data-ttu-id="7c1ce-129">Microsoft. Azure. PowerShell. polecenia. CostManagement. models. Api20200601. IExportExecution</span><span class="sxs-lookup"><span data-stu-id="7c1ce-129">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExportExecution</span></span>

## <span data-ttu-id="7c1ce-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7c1ce-130">NOTES</span></span>

<span data-ttu-id="7c1ce-131">PISUJE</span><span class="sxs-lookup"><span data-stu-id="7c1ce-131">ALIASES</span></span>

<span data-ttu-id="7c1ce-132">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7c1ce-132">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7c1ce-133">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="7c1ce-133">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7c1ce-134">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7c1ce-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7c1ce-135">INPUTobject <ICostManagementIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="7c1ce-135">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7c1ce-136">`[AlertId <String>]`: Identyfikator alertu</span><span class="sxs-lookup"><span data-stu-id="7c1ce-136">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="7c1ce-137">`[ExportName <String>]`: Nazwa eksportu.</span><span class="sxs-lookup"><span data-stu-id="7c1ce-137">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="7c1ce-138">`[ExternalCloudProviderId <String>]`: Może to być "{externalSubscriptionId}" dla połączonego konta lub "{externalBillingAccountId}" dla konta skonsolidowanego, które jest używane z operacjami wymiaru/kwerendy.</span><span class="sxs-lookup"><span data-stu-id="7c1ce-138">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="7c1ce-139">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: Typ zewnętrznego dostawcy chmury skojarzony z operacjami wymiaru/kwerendy.</span><span class="sxs-lookup"><span data-stu-id="7c1ce-139">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="7c1ce-140">Obejmuje to "externalSubscriptions" dla połączonego konta, a także "externalBillingAccounts" dla konta skonsolidowanego.</span><span class="sxs-lookup"><span data-stu-id="7c1ce-140">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="7c1ce-141">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="7c1ce-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7c1ce-142">`[Scope <String>]`: Zakres skojarzony z operacjami wyświetlania.</span><span class="sxs-lookup"><span data-stu-id="7c1ce-142">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="7c1ce-143">Obejmuje to "abonament/{subskrypcji}" dla zakresu abonamentu, "abonaments/{Binding}/resourceGroups/{resourceGroupName}" dla zakresu grupy zasobów. Providers/Microsoft. rozliczenia/billingAccounts/{billingAccountId} "dla zakresu kont rozliczeniowych" Providers/Microsoft. rozliczenia/billingAccounts/{billingAccountId}/działy/{departmentId} "dla zakresu działu," Providers/Microsoft. rozliczenia/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId} "dla zakresu EnrollmentAccount," Providers/Microsoft. rozliczenia/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId} "dla zakresu BillingProfile," Providers/Microsoft. rozliczenia/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId} "dla zakresu InvoiceSection," Providers/Microsoft. Management/managementGroups/{managementGroupId} ' dla zakresu grupy zarządzania, "Providers/Microsoft. CostManagement/externalBillingAccounts/{externalBillingAccountName}" dla zewnętrznego zakresu konta rozliczeniowego i "Providers/Microsoft. CostManagement/externalSubscriptions/{externalSubscriptionName}" dla zakresu subskrypcji zewnętrznej.</span><span class="sxs-lookup"><span data-stu-id="7c1ce-143">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="7c1ce-144">`[ViewName <String>]`: Nazwa widoku</span><span class="sxs-lookup"><span data-stu-id="7c1ce-144">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="7c1ce-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7c1ce-145">RELATED LINKS</span></span>

