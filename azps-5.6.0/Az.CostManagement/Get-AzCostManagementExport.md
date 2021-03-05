---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.costmanagement/get-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExport.md
ms.openlocfilehash: f318fcf3592c0b865684df57230f73a5f22ce024
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996815"
---
# <span data-ttu-id="49d85-101">Get-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="49d85-101">Get-AzCostManagementExport</span></span>

## <span data-ttu-id="49d85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49d85-102">SYNOPSIS</span></span>
<span data-ttu-id="49d85-103">Operacja uzyskania eksportu dla zdefiniowanego zakresu według nazwy eksportu.</span><span class="sxs-lookup"><span data-stu-id="49d85-103">The operation to get the export for the defined scope by export name.</span></span>

## <span data-ttu-id="49d85-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="49d85-104">SYNTAX</span></span>

### <span data-ttu-id="49d85-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="49d85-105">List (Default)</span></span>
```
Get-AzCostManagementExport -Scope <String> [-Expand <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="49d85-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="49d85-106">Get</span></span>
```
Get-AzCostManagementExport -Name <String> -Scope <String> [-Expand <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="49d85-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="49d85-107">GetViaIdentity</span></span>
```
Get-AzCostManagementExport -InputObject <ICostManagementIdentity> [-Expand <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="49d85-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="49d85-108">DESCRIPTION</span></span>
<span data-ttu-id="49d85-109">Operacja uzyskania eksportu dla zdefiniowanego zakresu według nazwy eksportu.</span><span class="sxs-lookup"><span data-stu-id="49d85-109">The operation to get the export for the defined scope by export name.</span></span>

## <span data-ttu-id="49d85-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="49d85-110">EXAMPLES</span></span>

### <span data-ttu-id="49d85-111">Przykład 1. Uzyskiwanie wszystkich azCostManagementExports według zakresu</span><span class="sxs-lookup"><span data-stu-id="49d85-111">Example 1: Get all AzCostManagementExports by scope</span></span>
```powershell
PS C:\> Get-AzCostManagementExport -Scope 'subscriptions/**********'

ETag              Name                               Type
----              ----                               ----
"************" TestExport                         Microsoft.CostManagement/exports
"************" TestExport1                        Microsoft.CostManagement/exports
"************" TestExport2                        Microsoft.CostManagement/exports
```

<span data-ttu-id="49d85-112">Pobierz wszystkie raporty AzCostManagementExports według zakresu</span><span class="sxs-lookup"><span data-stu-id="49d85-112">Get all AzCostManagementExports by Scope</span></span>

### <span data-ttu-id="49d85-113">Przykład 2. Uzyskiwanie azCostManagementExport według nazwy i zakresu</span><span class="sxs-lookup"><span data-stu-id="49d85-113">Example 2: Get AzCostManagementExport by Name and scope</span></span>
```powershell
PS C:\> Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'

ETag              Name       Type
----              ----       ----
"************" TestExport Microsoft.CostManagement/exports
```

<span data-ttu-id="49d85-114">Get AzCostManagementExport by Name and scope</span><span class="sxs-lookup"><span data-stu-id="49d85-114">Get AzCostManagementExport by Name and scope</span></span>

## <span data-ttu-id="49d85-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49d85-115">PARAMETERS</span></span>

### <span data-ttu-id="49d85-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49d85-116">-DefaultProfile</span></span>
<span data-ttu-id="49d85-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="49d85-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49d85-118">— Rozwiń</span><span class="sxs-lookup"><span data-stu-id="49d85-118">-Expand</span></span>
<span data-ttu-id="49d85-119">Może być używany do rozwijania właściwości w ramach eksportu.</span><span class="sxs-lookup"><span data-stu-id="49d85-119">May be used to expand the properties within an export.</span></span>
<span data-ttu-id="49d85-120">Obecnie jest obsługiwana tylko część "runHistory", która zwraca informacje dotyczące ostatnich 10 wykonywania eksportu.</span><span class="sxs-lookup"><span data-stu-id="49d85-120">Currently only 'runHistory' is supported and will return information for the last 10 executions of the export.</span></span>

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

### <span data-ttu-id="49d85-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49d85-121">-InputObject</span></span>
<span data-ttu-id="49d85-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="49d85-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="49d85-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="49d85-123">-Name</span></span>
<span data-ttu-id="49d85-124">Eksportuj nazwę.</span><span class="sxs-lookup"><span data-stu-id="49d85-124">Export Name.</span></span>

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

### <span data-ttu-id="49d85-125">— Zakres</span><span class="sxs-lookup"><span data-stu-id="49d85-125">-Scope</span></span>
<span data-ttu-id="49d85-126">Ten parametr definiuje zakres zarządzania kosztami z różnych perspektyw: "Subskrypcja", "Grupa zasobów" i "Udostępnij usługę".</span><span class="sxs-lookup"><span data-stu-id="49d85-126">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="49d85-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49d85-127">CommonParameters</span></span>
<span data-ttu-id="49d85-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49d85-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49d85-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49d85-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49d85-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49d85-130">INPUTS</span></span>

### <span data-ttu-id="49d85-131">Microsoft.Azure.PowerShell.Cmdlet.CostManagement.Models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="49d85-131">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="49d85-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49d85-132">OUTPUTS</span></span>

### <span data-ttu-id="49d85-133">Microsoft.Azure.PowerShell.cmdlet.costManagement.Models.Api20200601.IExport</span><span class="sxs-lookup"><span data-stu-id="49d85-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="49d85-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="49d85-134">NOTES</span></span>

<span data-ttu-id="49d85-135">ALIASY</span><span class="sxs-lookup"><span data-stu-id="49d85-135">ALIASES</span></span>

<span data-ttu-id="49d85-136">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="49d85-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="49d85-137">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="49d85-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="49d85-138">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="49d85-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="49d85-139">INPUTOBJECT: <ICostManagementIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="49d85-139">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="49d85-140">`[AlertId <String>]`: Identyfikator alertu</span><span class="sxs-lookup"><span data-stu-id="49d85-140">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="49d85-141">`[ExportName <String>]`: Eksportuj nazwę.</span><span class="sxs-lookup"><span data-stu-id="49d85-141">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="49d85-142">`[ExternalCloudProviderId <String>]`: W przypadku konta połączonego może to być wartość "{externalSubscriptionId}" lub "{externalBillingAccountId}" w przypadku skonsolidowanego konta używanego z operacjami wymiaru/zapytania.</span><span class="sxs-lookup"><span data-stu-id="49d85-142">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="49d85-143">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: Typ dostawcy chmury zewnętrznej skojarzony z operacjami wymiar/kwerenda.</span><span class="sxs-lookup"><span data-stu-id="49d85-143">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="49d85-144">Obejmuje to "zewnętrzneSubskrypcje" dla konta połączonego i "externalBillingAccounts" dla skonsolidowanego konta.</span><span class="sxs-lookup"><span data-stu-id="49d85-144">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="49d85-145">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="49d85-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="49d85-146">`[Scope <String>]`: Zakres skojarzony z operacjami wyświetlania.</span><span class="sxs-lookup"><span data-stu-id="49d85-146">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="49d85-147">Obejmuje to "subskrypcje/{subscriptionId}" dla zakresu subskrypcji, "subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}" dla zakresu resourceGroup, "providers/Microsoft.Billing/billingAccounts/{billingAccountId}" dla zakresu Konto rozliczeniowe, "providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}" dla zakresu Dział, "providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}" dla zakresu EnrollmentAccount, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management /managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span><span class="sxs-lookup"><span data-stu-id="49d85-147">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="49d85-148">`[ViewName <String>]`: nazwa widoku</span><span class="sxs-lookup"><span data-stu-id="49d85-148">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="49d85-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="49d85-149">RELATED LINKS</span></span>

