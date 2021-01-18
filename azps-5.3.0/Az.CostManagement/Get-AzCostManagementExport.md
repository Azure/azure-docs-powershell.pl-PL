---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/get-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExport.md
ms.openlocfilehash: 269a58e57510f6b0945218645ec079b21b606e44
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503771"
---
# <span data-ttu-id="537f6-101">Get-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="537f6-101">Get-AzCostManagementExport</span></span>

## <span data-ttu-id="537f6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="537f6-102">SYNOPSIS</span></span>
<span data-ttu-id="537f6-103">Operacja uzyskiwania eksportu dla zdefiniowanego zakresu przez eksportowanie nazwy.</span><span class="sxs-lookup"><span data-stu-id="537f6-103">The operation to get the export for the defined scope by export name.</span></span>

## <span data-ttu-id="537f6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="537f6-104">SYNTAX</span></span>

### <span data-ttu-id="537f6-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="537f6-105">List (Default)</span></span>
```
Get-AzCostManagementExport -Scope <String> [-Expand <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="537f6-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="537f6-106">Get</span></span>
```
Get-AzCostManagementExport -Name <String> -Scope <String> [-Expand <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="537f6-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="537f6-107">GetViaIdentity</span></span>
```
Get-AzCostManagementExport -InputObject <ICostManagementIdentity> [-Expand <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="537f6-108">Opis</span><span class="sxs-lookup"><span data-stu-id="537f6-108">DESCRIPTION</span></span>
<span data-ttu-id="537f6-109">Operacja uzyskiwania eksportu dla zdefiniowanego zakresu przez eksportowanie nazwy.</span><span class="sxs-lookup"><span data-stu-id="537f6-109">The operation to get the export for the defined scope by export name.</span></span>

## <span data-ttu-id="537f6-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="537f6-110">EXAMPLES</span></span>

### <span data-ttu-id="537f6-111">Przykład 1. Pobierz wszystkie AzCostManagementExports według zakresu</span><span class="sxs-lookup"><span data-stu-id="537f6-111">Example 1: Get all AzCostManagementExports by scope</span></span>
```powershell
PS C:\> Get-AzCostManagementExport -Scope 'subscriptions/**********'

ETag              Name                               Type
----              ----                               ----
"************" TestExport                         Microsoft.CostManagement/exports
"************" TestExport1                        Microsoft.CostManagement/exports
"************" TestExport2                        Microsoft.CostManagement/exports
```

<span data-ttu-id="537f6-112">Pobierz wszystkie AzCostManagementExports według zakresu</span><span class="sxs-lookup"><span data-stu-id="537f6-112">Get all AzCostManagementExports by Scope</span></span>

### <span data-ttu-id="537f6-113">Przykład 2: Uzyskaj AzCostManagementExport według nazwy i zakresu</span><span class="sxs-lookup"><span data-stu-id="537f6-113">Example 2: Get AzCostManagementExport by Name and scope</span></span>
```powershell
PS C:\> Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'

ETag              Name       Type
----              ----       ----
"************" TestExport Microsoft.CostManagement/exports
```

<span data-ttu-id="537f6-114">Uzyskaj AzCostManagementExport według nazwy i zakresu</span><span class="sxs-lookup"><span data-stu-id="537f6-114">Get AzCostManagementExport by Name and scope</span></span>

## <span data-ttu-id="537f6-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="537f6-115">PARAMETERS</span></span>

### <span data-ttu-id="537f6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="537f6-116">-DefaultProfile</span></span>
<span data-ttu-id="537f6-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="537f6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="537f6-118">-Expand</span><span class="sxs-lookup"><span data-stu-id="537f6-118">-Expand</span></span>
<span data-ttu-id="537f6-119">Może służyć do rozszerzania właściwości w ramach eksportu.</span><span class="sxs-lookup"><span data-stu-id="537f6-119">May be used to expand the properties within an export.</span></span>
<span data-ttu-id="537f6-120">Obecnie jest obsługiwana tylko "runHistory" i zostaną zwrócone informacje dotyczące ostatnich 10 wykonania eksportu.</span><span class="sxs-lookup"><span data-stu-id="537f6-120">Currently only 'runHistory' is supported and will return information for the last 10 executions of the export.</span></span>

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

### <span data-ttu-id="537f6-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="537f6-121">-InputObject</span></span>
<span data-ttu-id="537f6-122">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="537f6-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="537f6-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="537f6-123">-Name</span></span>
<span data-ttu-id="537f6-124">Eksportuj nazwę.</span><span class="sxs-lookup"><span data-stu-id="537f6-124">Export Name.</span></span>

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

### <span data-ttu-id="537f6-125">-Zakres</span><span class="sxs-lookup"><span data-stu-id="537f6-125">-Scope</span></span>
<span data-ttu-id="537f6-126">Ten parametr definiuje zakres costmanagement z różnych perspektyw "abonament", "Resources" i "świadczenie usługi".</span><span class="sxs-lookup"><span data-stu-id="537f6-126">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="537f6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="537f6-127">CommonParameters</span></span>
<span data-ttu-id="537f6-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="537f6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="537f6-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="537f6-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="537f6-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="537f6-130">INPUTS</span></span>

### <span data-ttu-id="537f6-131">Microsoft. Azure. PowerShell. polecenia. CostManagement. models. ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="537f6-131">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="537f6-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="537f6-132">OUTPUTS</span></span>

### <span data-ttu-id="537f6-133">Microsoft. Azure. PowerShell. polecenia. CostManagement. models. Api20200601. IExport</span><span class="sxs-lookup"><span data-stu-id="537f6-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="537f6-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="537f6-134">NOTES</span></span>

<span data-ttu-id="537f6-135">PISUJE</span><span class="sxs-lookup"><span data-stu-id="537f6-135">ALIASES</span></span>

<span data-ttu-id="537f6-136">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="537f6-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="537f6-137">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="537f6-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="537f6-138">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="537f6-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="537f6-139">INPUTobject <ICostManagementIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="537f6-139">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="537f6-140">`[AlertId <String>]`: Identyfikator alertu</span><span class="sxs-lookup"><span data-stu-id="537f6-140">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="537f6-141">`[ExportName <String>]`: Nazwa eksportu.</span><span class="sxs-lookup"><span data-stu-id="537f6-141">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="537f6-142">`[ExternalCloudProviderId <String>]`: Może to być "{externalSubscriptionId}" dla połączonego konta lub "{externalBillingAccountId}" dla konta skonsolidowanego, które jest używane z operacjami wymiaru/kwerendy.</span><span class="sxs-lookup"><span data-stu-id="537f6-142">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="537f6-143">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: Typ zewnętrznego dostawcy chmury skojarzony z operacjami wymiaru/kwerendy.</span><span class="sxs-lookup"><span data-stu-id="537f6-143">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="537f6-144">Obejmuje to "externalSubscriptions" dla połączonego konta, a także "externalBillingAccounts" dla konta skonsolidowanego.</span><span class="sxs-lookup"><span data-stu-id="537f6-144">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="537f6-145">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="537f6-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="537f6-146">`[Scope <String>]`: Zakres skojarzony z operacjami wyświetlania.</span><span class="sxs-lookup"><span data-stu-id="537f6-146">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="537f6-147">Obejmuje to "abonament/{subskrypcji}" dla zakresu abonamentu, "abonaments/{Binding}/resourceGroups/{resourceGroupName}" dla zakresu grupy zasobów. Providers/Microsoft. rozliczenia/billingAccounts/{billingAccountId} "dla zakresu kont rozliczeniowych" Providers/Microsoft. rozliczenia/billingAccounts/{billingAccountId}/działy/{departmentId} "dla zakresu działu," Providers/Microsoft. rozliczenia/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId} "dla zakresu EnrollmentAccount," Providers/Microsoft. rozliczenia/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId} "dla zakresu BillingProfile," Providers/Microsoft. rozliczenia/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId} "dla zakresu InvoiceSection," Providers/Microsoft. Management/managementGroups/{managementGroupId} ' dla zakresu grupy zarządzania, "Providers/Microsoft. CostManagement/externalBillingAccounts/{externalBillingAccountName}" dla zewnętrznego zakresu konta rozliczeniowego i "Providers/Microsoft. CostManagement/externalSubscriptions/{externalSubscriptionName}" dla zakresu subskrypcji zewnętrznej.</span><span class="sxs-lookup"><span data-stu-id="537f6-147">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="537f6-148">`[ViewName <String>]`: Nazwa widoku</span><span class="sxs-lookup"><span data-stu-id="537f6-148">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="537f6-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="537f6-149">RELATED LINKS</span></span>

