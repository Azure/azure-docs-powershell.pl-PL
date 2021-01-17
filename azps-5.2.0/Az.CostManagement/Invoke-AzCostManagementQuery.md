---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/invoke-azcostmanagementquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementQuery.md
ms.openlocfilehash: 1eec241ab9fba3f9e8daa3218b65140d644d56ea
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334654"
---
# <span data-ttu-id="0e5e7-101">Invoke-AzCostManagementQuery</span><span class="sxs-lookup"><span data-stu-id="0e5e7-101">Invoke-AzCostManagementQuery</span></span>

## <span data-ttu-id="0e5e7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0e5e7-102">SYNOPSIS</span></span>
<span data-ttu-id="0e5e7-103">Wykonywanie zapytań dotyczących danych użycia dla określonego zakresu.</span><span class="sxs-lookup"><span data-stu-id="0e5e7-103">Query the usage data for scope defined.</span></span>

## <span data-ttu-id="0e5e7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0e5e7-104">SYNTAX</span></span>

### <span data-ttu-id="0e5e7-105">UsageExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0e5e7-105">UsageExpanded (Default)</span></span>
```
Invoke-AzCostManagementQuery -Scope <String> -Timeframe <TimeframeType> -Type <ExportType>
 [-ConfigurationColumn <String[]>] [-DatasetAggregation <Hashtable>] [-DatasetFilter <IQueryFilter>]
 [-DatasetGranularity <GranularityType>] [-DatasetGrouping <IQueryGrouping[]>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0e5e7-106">UsageExpanded1</span><span class="sxs-lookup"><span data-stu-id="0e5e7-106">UsageExpanded1</span></span>
```
Invoke-AzCostManagementQuery -ExternalCloudProviderId <String>
 -ExternalCloudProviderType <ExternalCloudProviderType> -Timeframe <TimeframeType> -Type <ExportType>
 [-ConfigurationColumn <String[]>] [-DatasetAggregation <Hashtable>] [-DatasetFilter <IQueryFilter>]
 [-DatasetGranularity <GranularityType>] [-DatasetGrouping <IQueryGrouping[]>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0e5e7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0e5e7-107">DESCRIPTION</span></span>
<span data-ttu-id="0e5e7-108">Wykonywanie zapytań dotyczących danych użycia dla określonego zakresu.</span><span class="sxs-lookup"><span data-stu-id="0e5e7-108">Query the usage data for scope defined.</span></span>

## <span data-ttu-id="0e5e7-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0e5e7-109">EXAMPLES</span></span>

### <span data-ttu-id="0e5e7-110">Przykład 1: wywołanie AzCostManagementQuery według zakresu</span><span class="sxs-lookup"><span data-stu-id="0e5e7-110">Example 1: Invoke AzCostManagementQuery by Scope</span></span>
```powershell
PS C:\> Invoke-AzCostManagementQuery -Scope "/subscriptions/***********" -Timeframe MonthToDate -Type Usage -DatasetGranularity 'Daily'

Column                Row
------                ---
{UsageDate, Currency} {20201101 USD, 20201102 USD, 20201103 USD, 20201104 USD…}
```

<span data-ttu-id="0e5e7-111">Wywołanie AzCostManagementQuery według zakresu</span><span class="sxs-lookup"><span data-stu-id="0e5e7-111">Invoke AzCostManagementQuery by Scope</span></span>

### <span data-ttu-id="0e5e7-112">Przykład 2: wywołanie AzCostManagementQuery według zakresu z wymiarami</span><span class="sxs-lookup"><span data-stu-id="0e5e7-112">Example 2: Invoke AzCostManagementQuery by Scope with Dimensions</span></span>
```powershell
PS C:\> $dimensions = New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceGroup' -Operator 'In' -Value 'API'
$filter = New-AzCostManagementQueryFilterObject -Dimensions $dimensions
Invoke-AzCostManagementQuery -Type Usage -Scope "subscriptions/***********" -DatasetGranularity 'Monthly' -DatasetFilter $filter -Timeframe MonthToDate -Debug


Column                   Row
------                   ---
{BillingMonth, Currency} {}
```

<span data-ttu-id="0e5e7-113">Wywołanie AzCostManagementQuery według zakresu z wymiarami</span><span class="sxs-lookup"><span data-stu-id="0e5e7-113">Invoke AzCostManagementQuery by Scope with Dimensions</span></span>

## <span data-ttu-id="0e5e7-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0e5e7-114">PARAMETERS</span></span>

### <span data-ttu-id="0e5e7-115">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="0e5e7-115">-ConfigurationColumn</span></span>
<span data-ttu-id="0e5e7-116">Tablica nazw kolumn, które mają zostać uwzględnione w zapytaniu.</span><span class="sxs-lookup"><span data-stu-id="0e5e7-116">Array of column names to be included in the query.</span></span>

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

### <span data-ttu-id="0e5e7-117">-DatasetAggregation</span><span class="sxs-lookup"><span data-stu-id="0e5e7-117">-DatasetAggregation</span></span>
<span data-ttu-id="0e5e7-118">Słownik wyrażeń agregujących, które mają zostać użyte w zapytaniu.</span><span class="sxs-lookup"><span data-stu-id="0e5e7-118">Dictionary of aggregation expression to use in the query.</span></span>

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

### <span data-ttu-id="0e5e7-119">-DatasetFilter</span><span class="sxs-lookup"><span data-stu-id="0e5e7-119">-DatasetFilter</span></span>
<span data-ttu-id="0e5e7-120">Zawiera wyrażenie filtru, które ma zostać użyte w zapytaniu.</span><span class="sxs-lookup"><span data-stu-id="0e5e7-120">Has filter expression to use in the query.</span></span>
<span data-ttu-id="0e5e7-121">Aby skonstruować, zobacz sekcję notatki dla właściwości DATASETFILTER i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="0e5e7-121">To construct, see NOTES section for DATASETFILTER properties and create a hash table.</span></span>

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

### <span data-ttu-id="0e5e7-122">-DatasetGranularity</span><span class="sxs-lookup"><span data-stu-id="0e5e7-122">-DatasetGranularity</span></span>
<span data-ttu-id="0e5e7-123">Ziarnistość wierszy w zapytaniu.</span><span class="sxs-lookup"><span data-stu-id="0e5e7-123">The granularity of rows in the query.</span></span>

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

### <span data-ttu-id="0e5e7-124">-DatasetGrouping</span><span class="sxs-lookup"><span data-stu-id="0e5e7-124">-DatasetGrouping</span></span>
<span data-ttu-id="0e5e7-125">Tablica wyrażeń Group by, które ma zostać użyte w zapytaniu.</span><span class="sxs-lookup"><span data-stu-id="0e5e7-125">Array of group by expression to use in the query.</span></span>
<span data-ttu-id="0e5e7-126">Aby skonstruować, zobacz sekcję notatki dla właściwości DATASETGROUPING i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="0e5e7-126">To construct, see NOTES section for DATASETGROUPING properties and create a hash table.</span></span>

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

### <span data-ttu-id="0e5e7-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e5e7-127">-DefaultProfile</span></span>
<span data-ttu-id="0e5e7-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0e5e7-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e5e7-129">-ExternalCloudProviderId</span><span class="sxs-lookup"><span data-stu-id="0e5e7-129">-ExternalCloudProviderId</span></span>
<span data-ttu-id="0e5e7-130">Może to być "{externalSubscriptionId}" dla połączonego konta lub "{externalBillingAccountId}" dla konta skonsolidowanego, które jest używane z operacjami wymiaru/kwerendy.</span><span class="sxs-lookup"><span data-stu-id="0e5e7-130">This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>

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

### <span data-ttu-id="0e5e7-131">-ExternalCloudProviderType</span><span class="sxs-lookup"><span data-stu-id="0e5e7-131">-ExternalCloudProviderType</span></span>
<span data-ttu-id="0e5e7-132">Typ dostawcy w chmurze zewnętrznej skojarzony z operacjami wymiaru/kwerendy.</span><span class="sxs-lookup"><span data-stu-id="0e5e7-132">The external cloud provider type associated with dimension/query operations.</span></span>

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

### <span data-ttu-id="0e5e7-133">-Zakres</span><span class="sxs-lookup"><span data-stu-id="0e5e7-133">-Scope</span></span>
<span data-ttu-id="0e5e7-134">Obejmuje to "abonament/{Identyfikator subskrypcji}/" dla zakresu abonamentu, "abonament/{subskrypcji}/resourceGroups/{resourceGroupName}" dla zakresu grupy zasobów. Providers/Microsoft. rozliczenia/billingAccounts/{billingAccountId} "dla zakresu kont rozliczeniowych i" Providers/Microsoft. rozliczenia/billingAccounts/{billingAccountId}/działy/{departmentId} "dla zakresu działów," Providers/Microsoft. rozliczenia/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId} "dla zakresu EnrollmentAccount," Providers/Microsoft Management/managementGroups/{managementGroupId} dla zakresu grupy zarządzania, "Providers/Microsoft. rozliczenia/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}" dla zakresu billingProfile, "Providers/Microsoft. rozliczenia/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}/invoiceSections/{invoiceSectionId}" dla zakresu invoiceSection, a "Providers/Microsoft. rozliczenia/billingAccounts/{billingAccountId}/Customers/{customerId}" specyficzne dla partnerów.</span><span class="sxs-lookup"><span data-stu-id="0e5e7-134">This includes 'subscriptions/{subscriptionId}/' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope and 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId} for Management Group scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for billingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}/invoiceSections/{invoiceSectionId}' for invoiceSection scope, and 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/customers/{customerId}' specific for partners.</span></span>

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

### <span data-ttu-id="0e5e7-135">— Przedział czasu</span><span class="sxs-lookup"><span data-stu-id="0e5e7-135">-Timeframe</span></span>
<span data-ttu-id="0e5e7-136">Przedział czasu umożliwiający ściąganie danych w zapytaniu.</span><span class="sxs-lookup"><span data-stu-id="0e5e7-136">The time frame for pulling data for the query.</span></span>

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

### <span data-ttu-id="0e5e7-137">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="0e5e7-137">-TimePeriodFrom</span></span>
<span data-ttu-id="0e5e7-138">Data rozpoczęcia ściągania danych.</span><span class="sxs-lookup"><span data-stu-id="0e5e7-138">The start date to pull data from.</span></span>

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

### <span data-ttu-id="0e5e7-139">-TimePeriodTo</span><span class="sxs-lookup"><span data-stu-id="0e5e7-139">-TimePeriodTo</span></span>
<span data-ttu-id="0e5e7-140">Data zakończenia ściągania danych.</span><span class="sxs-lookup"><span data-stu-id="0e5e7-140">The end date to pull data to.</span></span>

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

### <span data-ttu-id="0e5e7-141">-Type</span><span class="sxs-lookup"><span data-stu-id="0e5e7-141">-Type</span></span>
<span data-ttu-id="0e5e7-142">Typ zapytania.</span><span class="sxs-lookup"><span data-stu-id="0e5e7-142">The type of the query.</span></span>

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

### <span data-ttu-id="0e5e7-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0e5e7-143">-Confirm</span></span>
<span data-ttu-id="0e5e7-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e5e7-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e5e7-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e5e7-145">-WhatIf</span></span>
<span data-ttu-id="0e5e7-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e5e7-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e5e7-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0e5e7-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e5e7-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e5e7-148">CommonParameters</span></span>
<span data-ttu-id="0e5e7-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e5e7-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e5e7-150">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0e5e7-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e5e7-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e5e7-151">INPUTS</span></span>

## <span data-ttu-id="0e5e7-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0e5e7-152">OUTPUTS</span></span>

### <span data-ttu-id="0e5e7-153">Microsoft. Azure. PowerShell. polecenia. CostManagement. models. Api20200601. IQueryResult</span><span class="sxs-lookup"><span data-stu-id="0e5e7-153">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryResult</span></span>

## <span data-ttu-id="0e5e7-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0e5e7-154">NOTES</span></span>

<span data-ttu-id="0e5e7-155">PISUJE</span><span class="sxs-lookup"><span data-stu-id="0e5e7-155">ALIASES</span></span>

<span data-ttu-id="0e5e7-156">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0e5e7-156">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0e5e7-157">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="0e5e7-157">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0e5e7-158">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0e5e7-158">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0e5e7-159">DATASETFILTER <IQueryFilter> : zawiera wyrażenie filtru, które ma zostać użyte w zapytaniu.</span><span class="sxs-lookup"><span data-stu-id="0e5e7-159">DATASETFILTER <IQueryFilter>: Has filter expression to use in the query.</span></span>
  - <span data-ttu-id="0e5e7-160">`[And <IQueryFilter[]>]`: Wyrażenie logiczne "AND".</span><span class="sxs-lookup"><span data-stu-id="0e5e7-160">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="0e5e7-161">Musi zawierać co najmniej 2 elementy.</span><span class="sxs-lookup"><span data-stu-id="0e5e7-161">Must have at least 2 items.</span></span>
  - <span data-ttu-id="0e5e7-162">`[Dimensions <IQueryComparisonExpression>]`: Zawiera wyrażenie porównania dla wymiaru</span><span class="sxs-lookup"><span data-stu-id="0e5e7-162">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="0e5e7-163">`Name <String>`: Nazwa kolumny, która ma być używana w porównaniu.</span><span class="sxs-lookup"><span data-stu-id="0e5e7-163">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="0e5e7-164">`Operator <OperatorType>`: Operator używany do porównywania.</span><span class="sxs-lookup"><span data-stu-id="0e5e7-164">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="0e5e7-165">`Value <String[]>`: Tablica wartości do użycia w porównaniu</span><span class="sxs-lookup"><span data-stu-id="0e5e7-165">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="0e5e7-166">`[Not <IQueryFilter>]`: Logiczne wyrażenie "NOT".</span><span class="sxs-lookup"><span data-stu-id="0e5e7-166">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="0e5e7-167">`[Or <IQueryFilter[]>]`: Wyrażenie logiczne "OR".</span><span class="sxs-lookup"><span data-stu-id="0e5e7-167">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="0e5e7-168">Musi zawierać co najmniej 2 elementy.</span><span class="sxs-lookup"><span data-stu-id="0e5e7-168">Must have at least 2 items.</span></span>
  - <span data-ttu-id="0e5e7-169">`[Tag <IQueryComparisonExpression>]`: Zawiera wyrażenie porównania dla znacznika</span><span class="sxs-lookup"><span data-stu-id="0e5e7-169">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="0e5e7-170">DATASETGROUPING <IQueryGrouping [] >: tablica wyrażeń Group by, które mają zostać użyte w zapytaniu.</span><span class="sxs-lookup"><span data-stu-id="0e5e7-170">DATASETGROUPING <IQueryGrouping[]>: Array of group by expression to use in the query.</span></span>
  - <span data-ttu-id="0e5e7-171">`Name <String>`: Nazwa kolumny do grupowania.</span><span class="sxs-lookup"><span data-stu-id="0e5e7-171">`Name <String>`: The name of the column to group.</span></span>
  - <span data-ttu-id="0e5e7-172">`Type <QueryColumnType>`: Typ kolumny do grupowania.</span><span class="sxs-lookup"><span data-stu-id="0e5e7-172">`Type <QueryColumnType>`: Has type of the column to group.</span></span>

## <span data-ttu-id="0e5e7-173">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0e5e7-173">RELATED LINKS</span></span>

