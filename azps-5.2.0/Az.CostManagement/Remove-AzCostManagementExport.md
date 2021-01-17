---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/remove-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Remove-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Remove-AzCostManagementExport.md
ms.openlocfilehash: 75c1f01730d4dfe3e9769a430f874887fd2d2090
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336610"
---
# <span data-ttu-id="ee60c-101">Remove-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="ee60c-101">Remove-AzCostManagementExport</span></span>

## <span data-ttu-id="ee60c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ee60c-102">SYNOPSIS</span></span>
<span data-ttu-id="ee60c-103">Operacja usuwania eksportu.</span><span class="sxs-lookup"><span data-stu-id="ee60c-103">The operation to delete a export.</span></span>

## <span data-ttu-id="ee60c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ee60c-104">SYNTAX</span></span>

### <span data-ttu-id="ee60c-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="ee60c-105">Delete (Default)</span></span>
```
Remove-AzCostManagementExport -Name <String> -Scope <String> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ee60c-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ee60c-106">DeleteViaIdentity</span></span>
```
Remove-AzCostManagementExport -InputObject <ICostManagementIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ee60c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ee60c-107">DESCRIPTION</span></span>
<span data-ttu-id="ee60c-108">Operacja usuwania eksportu.</span><span class="sxs-lookup"><span data-stu-id="ee60c-108">The operation to delete a export.</span></span>

## <span data-ttu-id="ee60c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ee60c-109">EXAMPLES</span></span>

### <span data-ttu-id="ee60c-110">Przykład 1. Usuń AzCostManagementExport według zakresu i nazwy</span><span class="sxs-lookup"><span data-stu-id="ee60c-110">Example 1: Delete the AzCostManagementExport by Scope and Name</span></span>
```powershell
PS C:\> Remove-AzCostManagementExport -Scope 'subscriptions/********' -name 'TestExportDatasetAggregationInfoYouri'


```

<span data-ttu-id="ee60c-111">Usuwanie AzCostManagementExport według zakresu i eksportu</span><span class="sxs-lookup"><span data-stu-id="ee60c-111">Delete the AzCostManagementExport By Scope and ExportName</span></span>

### <span data-ttu-id="ee60c-112">Przykład 2: usuwanie AzCostManagementExport za pomocą obiektu Export</span><span class="sxs-lookup"><span data-stu-id="ee60c-112">Example 2: Delete the AzCostManagementExport by Export Object</span></span>
```powershell
PS C:\> $getExport = Get-AzCostManagementExport -Scope 'subscriptions/*********' -name 'TestExportDatasetAggregationYouori'
Remove-AzCostManagementExport -InputObject $getExport


```

<span data-ttu-id="ee60c-113">Usuwanie AzCostManagementExport przez wejście</span><span class="sxs-lookup"><span data-stu-id="ee60c-113">Delete the AzCostManagementExport By InputObject</span></span>

## <span data-ttu-id="ee60c-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ee60c-114">PARAMETERS</span></span>

### <span data-ttu-id="ee60c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee60c-115">-DefaultProfile</span></span>
<span data-ttu-id="ee60c-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ee60c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee60c-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ee60c-117">-InputObject</span></span>
<span data-ttu-id="ee60c-118">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="ee60c-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ee60c-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ee60c-119">-Name</span></span>
<span data-ttu-id="ee60c-120">Eksportuj nazwę.</span><span class="sxs-lookup"><span data-stu-id="ee60c-120">Export Name.</span></span>

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

### <span data-ttu-id="ee60c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ee60c-121">-PassThru</span></span>
<span data-ttu-id="ee60c-122">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="ee60c-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ee60c-123">-Zakres</span><span class="sxs-lookup"><span data-stu-id="ee60c-123">-Scope</span></span>
<span data-ttu-id="ee60c-124">Ten parametr definiuje zakres costmanagement z różnych perspektyw "abonament", "Resources" i "świadczenie usługi".</span><span class="sxs-lookup"><span data-stu-id="ee60c-124">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="ee60c-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ee60c-125">-Confirm</span></span>
<span data-ttu-id="ee60c-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee60c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee60c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee60c-127">-WhatIf</span></span>
<span data-ttu-id="ee60c-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee60c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee60c-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ee60c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee60c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee60c-130">CommonParameters</span></span>
<span data-ttu-id="ee60c-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee60c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee60c-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ee60c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee60c-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ee60c-133">INPUTS</span></span>

### <span data-ttu-id="ee60c-134">Microsoft. Azure. PowerShell. polecenia. CostManagement. models. ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="ee60c-134">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="ee60c-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ee60c-135">OUTPUTS</span></span>

### <span data-ttu-id="ee60c-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ee60c-136">System.Boolean</span></span>

## <span data-ttu-id="ee60c-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ee60c-137">NOTES</span></span>

<span data-ttu-id="ee60c-138">PISUJE</span><span class="sxs-lookup"><span data-stu-id="ee60c-138">ALIASES</span></span>

<span data-ttu-id="ee60c-139">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ee60c-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ee60c-140">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="ee60c-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ee60c-141">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ee60c-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ee60c-142">INPUTobject <ICostManagementIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="ee60c-142">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ee60c-143">`[AlertId <String>]`: Identyfikator alertu</span><span class="sxs-lookup"><span data-stu-id="ee60c-143">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="ee60c-144">`[ExportName <String>]`: Nazwa eksportu.</span><span class="sxs-lookup"><span data-stu-id="ee60c-144">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="ee60c-145">`[ExternalCloudProviderId <String>]`: Może to być "{externalSubscriptionId}" dla połączonego konta lub "{externalBillingAccountId}" dla konta skonsolidowanego, które jest używane z operacjami wymiaru/kwerendy.</span><span class="sxs-lookup"><span data-stu-id="ee60c-145">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="ee60c-146">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: Typ zewnętrznego dostawcy chmury skojarzony z operacjami wymiaru/kwerendy.</span><span class="sxs-lookup"><span data-stu-id="ee60c-146">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="ee60c-147">Obejmuje to "externalSubscriptions" dla połączonego konta, a także "externalBillingAccounts" dla konta skonsolidowanego.</span><span class="sxs-lookup"><span data-stu-id="ee60c-147">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="ee60c-148">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="ee60c-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ee60c-149">`[Scope <String>]`: Zakres skojarzony z operacjami wyświetlania.</span><span class="sxs-lookup"><span data-stu-id="ee60c-149">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="ee60c-150">Obejmuje to "abonament/{subskrypcji}" dla zakresu abonamentu, "abonaments/{Binding}/resourceGroups/{resourceGroupName}" dla zakresu grupy zasobów. Providers/Microsoft. rozliczenia/billingAccounts/{billingAccountId} "dla zakresu kont rozliczeniowych" Providers/Microsoft. rozliczenia/billingAccounts/{billingAccountId}/działy/{departmentId} "dla zakresu działu," Providers/Microsoft. rozliczenia/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId} "dla zakresu EnrollmentAccount," Providers/Microsoft. rozliczenia/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId} "dla zakresu BillingProfile," Providers/Microsoft. rozliczenia/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId} "dla zakresu InvoiceSection," Providers/Microsoft. Management/managementGroups/{managementGroupId} ' dla zakresu grupy zarządzania, "Providers/Microsoft. CostManagement/externalBillingAccounts/{externalBillingAccountName}" dla zewnętrznego zakresu konta rozliczeniowego i "Providers/Microsoft. CostManagement/externalSubscriptions/{externalSubscriptionName}" dla zakresu subskrypcji zewnętrznej.</span><span class="sxs-lookup"><span data-stu-id="ee60c-150">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="ee60c-151">`[ViewName <String>]`: Nazwa widoku</span><span class="sxs-lookup"><span data-stu-id="ee60c-151">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="ee60c-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ee60c-152">RELATED LINKS</span></span>

