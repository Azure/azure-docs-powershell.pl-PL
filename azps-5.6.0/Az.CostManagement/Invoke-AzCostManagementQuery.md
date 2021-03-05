---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.costmanagement/invoke-azcostmanagementquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementQuery.md
ms.openlocfilehash: c1bc78747807d0f481c35fc75ff6fcfc80a83787
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972881"
---
# <span data-ttu-id="f067b-101">Invoke-AzCostManagementQuery</span><span class="sxs-lookup"><span data-stu-id="f067b-101">Invoke-AzCostManagementQuery</span></span>

## <span data-ttu-id="f067b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f067b-102">SYNOPSIS</span></span>
<span data-ttu-id="f067b-103">Kwerenda danych użycia dla zdefiniowanego zakresu.</span><span class="sxs-lookup"><span data-stu-id="f067b-103">Query the usage data for scope defined.</span></span>

## <span data-ttu-id="f067b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f067b-104">SYNTAX</span></span>

### <span data-ttu-id="f067b-105">UsageExpanded (Default)</span><span class="sxs-lookup"><span data-stu-id="f067b-105">UsageExpanded (Default)</span></span>
```
Invoke-AzCostManagementQuery -Scope <String> -Timeframe <TimeframeType> -Type <ExportType>
 [-ConfigurationColumn <String[]>] [-DatasetAggregation <Hashtable>] [-DatasetFilter <IQueryFilter>]
 [-DatasetGranularity <GranularityType>] [-DatasetGrouping <IQueryGrouping[]>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f067b-106">UsageExpanded1</span><span class="sxs-lookup"><span data-stu-id="f067b-106">UsageExpanded1</span></span>
```
Invoke-AzCostManagementQuery -ExternalCloudProviderId <String>
 -ExternalCloudProviderType <ExternalCloudProviderType> -Timeframe <TimeframeType> -Type <ExportType>
 [-ConfigurationColumn <String[]>] [-DatasetAggregation <Hashtable>] [-DatasetFilter <IQueryFilter>]
 [-DatasetGranularity <GranularityType>] [-DatasetGrouping <IQueryGrouping[]>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f067b-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="f067b-107">DESCRIPTION</span></span>
<span data-ttu-id="f067b-108">Kwerenda danych użycia dla zdefiniowanego zakresu.</span><span class="sxs-lookup"><span data-stu-id="f067b-108">Query the usage data for scope defined.</span></span>

## <span data-ttu-id="f067b-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f067b-109">EXAMPLES</span></span>

### <span data-ttu-id="f067b-110">Przykład 1. Wywoływanie zapytania AzCostManagementQuery według zakresu</span><span class="sxs-lookup"><span data-stu-id="f067b-110">Example 1: Invoke AzCostManagementQuery by Scope</span></span>
```powershell
PS C:\> Invoke-AzCostManagementQuery -Scope "/subscriptions/***********" -Timeframe MonthToDate -Type Usage -DatasetGranularity 'Daily'

Column                Row
------                ---
{UsageDate, Currency} {20201101 USD, 20201102 USD, 20201103 USD, 20201104 USD…}
```

<span data-ttu-id="f067b-111">Invoke AzCostManagementQuery by Scope</span><span class="sxs-lookup"><span data-stu-id="f067b-111">Invoke AzCostManagementQuery by Scope</span></span>

### <span data-ttu-id="f067b-112">Przykład 2. Wywoływanie zapytania AzCostManagementQuery według zakresu z wymiarami</span><span class="sxs-lookup"><span data-stu-id="f067b-112">Example 2: Invoke AzCostManagementQuery by Scope with Dimensions</span></span>
```powershell
PS C:\> $dimensions = New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceGroup' -Value 'API'
$filter = New-AzCostManagementQueryFilterObject -Dimensions $dimensions
Invoke-AzCostManagementQuery -Type Usage -Scope "subscriptions/***********" -DatasetGranularity 'Monthly' -DatasetFilter $filter -Timeframe MonthToDate -Debug


Column                   Row
------                   ---
{BillingMonth, Currency} {}
```

<span data-ttu-id="f067b-113">Invoke AzCostManagementQuery by Scope with Dimensions</span><span class="sxs-lookup"><span data-stu-id="f067b-113">Invoke AzCostManagementQuery by Scope with Dimensions</span></span>

## <span data-ttu-id="f067b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f067b-114">PARAMETERS</span></span>

### <span data-ttu-id="f067b-115">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="f067b-115">-ConfigurationColumn</span></span>
<span data-ttu-id="f067b-116">Tablica nazw kolumn uwzględnianych w zapytaniu.</span><span class="sxs-lookup"><span data-stu-id="f067b-116">Array of column names to be included in the query.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f067b-117">-DatasetAggregation</span><span class="sxs-lookup"><span data-stu-id="f067b-117">-DatasetAggregation</span></span>
<span data-ttu-id="f067b-118">Słownik wyrażenia agregacji do użycia w zapytaniu.</span><span class="sxs-lookup"><span data-stu-id="f067b-118">Dictionary of aggregation expression to use in the query.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f067b-119">-DatasetFilter</span><span class="sxs-lookup"><span data-stu-id="f067b-119">-DatasetFilter</span></span>
<span data-ttu-id="f067b-120">Ma wyrażenie filtru do użycia w zapytaniu.</span><span class="sxs-lookup"><span data-stu-id="f067b-120">Has filter expression to use in the query.</span></span>
<span data-ttu-id="f067b-121">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach FILTR.ZESTAWU DANYCH i utworzyć tabelę skrótów.</span><span class="sxs-lookup"><span data-stu-id="f067b-121">To construct, see NOTES section for DATASETFILTER properties and create a hash table.</span></span>

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

### <span data-ttu-id="f067b-122">- DatasetGranularity</span><span class="sxs-lookup"><span data-stu-id="f067b-122">-DatasetGranularity</span></span>
<span data-ttu-id="f067b-123">Szczegółowość wierszy w zapytaniu.</span><span class="sxs-lookup"><span data-stu-id="f067b-123">The granularity of rows in the query.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.GranularityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f067b-124">-DatasetGrouping</span><span class="sxs-lookup"><span data-stu-id="f067b-124">-DatasetGrouping</span></span>
<span data-ttu-id="f067b-125">Tablica grupowania według wyrażeń do użycia w zapytaniu.</span><span class="sxs-lookup"><span data-stu-id="f067b-125">Array of group by expression to use in the query.</span></span>
<span data-ttu-id="f067b-126">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach GRUPOWANIA ZESTAWÓW DANYCH i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="f067b-126">To construct, see NOTES section for DATASETGROUPING properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryGrouping[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f067b-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f067b-127">-DefaultProfile</span></span>
<span data-ttu-id="f067b-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f067b-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f067b-129">-ExternalCloudProviderId</span><span class="sxs-lookup"><span data-stu-id="f067b-129">-ExternalCloudProviderId</span></span>
<span data-ttu-id="f067b-130">W przypadku konta połączonego może to być wartość "{externalSubscriptionId}" lub "{externalBillingAccountId}" w przypadku skonsolidowanego konta używanego z operacjami wymiaru/zapytania.</span><span class="sxs-lookup"><span data-stu-id="f067b-130">This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>

```yaml
Type: System.String
Parameter Sets: UsageExpanded1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f067b-131">-ExternalCloudProviderType</span><span class="sxs-lookup"><span data-stu-id="f067b-131">-ExternalCloudProviderType</span></span>
<span data-ttu-id="f067b-132">Typ dostawcy chmury zewnętrznej skojarzony z operacjami wymiaru/zapytania.</span><span class="sxs-lookup"><span data-stu-id="f067b-132">The external cloud provider type associated with dimension/query operations.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.ExternalCloudProviderType
Parameter Sets: UsageExpanded1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f067b-133">— Zakres</span><span class="sxs-lookup"><span data-stu-id="f067b-133">-Scope</span></span>
<span data-ttu-id="f067b-134">Obejmuje to "subskrypcje/{subscriptionId}/" dla zakresu subskrypcji, "subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}" dla zakresu resourceGroup, "providers/Microsoft.Billing/billingAccounts/{billingAccountId}" dla zakresu Konta rozliczeniowego oraz "providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}" dla zakresu Dział, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId} dla zakresu EnrollmentAccount, 'providers/Microsoft.Management/managementGroups/{managementGroupId} for Management Group scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' dla zakresu billingProfile, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}/invoiceSections/{invoiceSectionId}' dla zakresu invoiceSection oraz 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/customers/{customerId}' specyficzne dla partnerów.</span><span class="sxs-lookup"><span data-stu-id="f067b-134">This includes 'subscriptions/{subscriptionId}/' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope and 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId} for Management Group scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for billingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}/invoiceSections/{invoiceSectionId}' for invoiceSection scope, and 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/customers/{customerId}' specific for partners.</span></span>

```yaml
Type: System.String
Parameter Sets: UsageExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f067b-135">— Timeframe</span><span class="sxs-lookup"><span data-stu-id="f067b-135">-Timeframe</span></span>
<span data-ttu-id="f067b-136">Ramy czasowe dla wyszukiwania danych do zapytania.</span><span class="sxs-lookup"><span data-stu-id="f067b-136">The time frame for pulling data for the query.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.TimeframeType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f067b-137">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="f067b-137">-TimePeriodFrom</span></span>
<span data-ttu-id="f067b-138">Data rozpoczęcia, z których mają być ciągnięte dane.</span><span class="sxs-lookup"><span data-stu-id="f067b-138">The start date to pull data from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f067b-139">-TimePeriodTo</span><span class="sxs-lookup"><span data-stu-id="f067b-139">-TimePeriodTo</span></span>
<span data-ttu-id="f067b-140">Data zakończenia, do która ma być ciągnięta dane.</span><span class="sxs-lookup"><span data-stu-id="f067b-140">The end date to pull data to.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f067b-141">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="f067b-141">-Type</span></span>
<span data-ttu-id="f067b-142">Typ zapytania.</span><span class="sxs-lookup"><span data-stu-id="f067b-142">The type of the query.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.ExportType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f067b-143">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f067b-143">-Confirm</span></span>
<span data-ttu-id="f067b-144">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f067b-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f067b-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f067b-145">-WhatIf</span></span>
<span data-ttu-id="f067b-146">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f067b-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f067b-147">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f067b-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f067b-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f067b-148">CommonParameters</span></span>
<span data-ttu-id="f067b-149">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f067b-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f067b-150">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f067b-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f067b-151">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f067b-151">INPUTS</span></span>

## <span data-ttu-id="f067b-152">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f067b-152">OUTPUTS</span></span>

### <span data-ttu-id="f067b-153">Microsoft.Azure.PowerShell.Cmdlet.CostManagement.Models.Api20200601.IQueryResult</span><span class="sxs-lookup"><span data-stu-id="f067b-153">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryResult</span></span>

## <span data-ttu-id="f067b-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f067b-154">NOTES</span></span>

<span data-ttu-id="f067b-155">ALIASY</span><span class="sxs-lookup"><span data-stu-id="f067b-155">ALIASES</span></span>

<span data-ttu-id="f067b-156">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f067b-156">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f067b-157">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="f067b-157">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f067b-158">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f067b-158">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f067b-159"><IQueryFilter>FILTR.ZESTAWU DANYCH: zawiera wyrażenie filtru do użycia w zapytaniu.</span><span class="sxs-lookup"><span data-stu-id="f067b-159">DATASETFILTER <IQueryFilter>: Has filter expression to use in the query.</span></span>
  - <span data-ttu-id="f067b-160">`[And <IQueryFilter[]>]`: wyrażenie logiczne "ORAZ".</span><span class="sxs-lookup"><span data-stu-id="f067b-160">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="f067b-161">Musi zawierać co najmniej 2 elementy.</span><span class="sxs-lookup"><span data-stu-id="f067b-161">Must have at least 2 items.</span></span>
  - <span data-ttu-id="f067b-162">`[Dimensions <IQueryComparisonExpression>]`: Ma wyrażenie porównania dla wymiaru</span><span class="sxs-lookup"><span data-stu-id="f067b-162">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="f067b-163">`Name <String>`: nazwa kolumny, która ma być porównywana.</span><span class="sxs-lookup"><span data-stu-id="f067b-163">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="f067b-164">`Value <String[]>`: tablica wartości do użycia w celu porównania</span><span class="sxs-lookup"><span data-stu-id="f067b-164">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="f067b-165">`[Not <IQueryFilter>]`: wyrażenie logiczne "NOT".</span><span class="sxs-lookup"><span data-stu-id="f067b-165">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="f067b-166">`[Or <IQueryFilter[]>]`: wyrażenie logiczne "LUB".</span><span class="sxs-lookup"><span data-stu-id="f067b-166">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="f067b-167">Musi zawierać co najmniej 2 elementy.</span><span class="sxs-lookup"><span data-stu-id="f067b-167">Must have at least 2 items.</span></span>
  - <span data-ttu-id="f067b-168">`[Tag <IQueryComparisonExpression>]`: zawiera wyrażenie porównania tagu</span><span class="sxs-lookup"><span data-stu-id="f067b-168">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="f067b-169">DATASETGROUPING <IQueryGrouping[]>: Tablica grupowania według wyrażeń do użycia w zapytaniu.</span><span class="sxs-lookup"><span data-stu-id="f067b-169">DATASETGROUPING <IQueryGrouping[]>: Array of group by expression to use in the query.</span></span>
  - <span data-ttu-id="f067b-170">`Name <String>`: nazwa kolumny do zgrupowania.</span><span class="sxs-lookup"><span data-stu-id="f067b-170">`Name <String>`: The name of the column to group.</span></span>
  - <span data-ttu-id="f067b-171">`Type <QueryColumnType>`: zawiera typ kolumny do zgrupowania.</span><span class="sxs-lookup"><span data-stu-id="f067b-171">`Type <QueryColumnType>`: Has type of the column to group.</span></span>

## <span data-ttu-id="f067b-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f067b-172">RELATED LINKS</span></span>

