---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/update-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Update-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Update-AzCostManagementExport.md
ms.openlocfilehash: 310600555f36fa0f6b129f2cf2a84581ffad044b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323372"
---
# <span data-ttu-id="219ac-101">Update-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="219ac-101">Update-AzCostManagementExport</span></span>

## <span data-ttu-id="219ac-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="219ac-102">SYNOPSIS</span></span>
<span data-ttu-id="219ac-103">Operacja tworzenia lub aktualizowania eksportu.</span><span class="sxs-lookup"><span data-stu-id="219ac-103">The operation to create or update a export.</span></span>
<span data-ttu-id="219ac-104">Operacja aktualizacji wymaga, aby w żądaniu została ustawiona Najnowsza wersja elementu eTag.</span><span class="sxs-lookup"><span data-stu-id="219ac-104">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="219ac-105">Najnowszy element eTag można uzyskać, wykonując operację pobierania.</span><span class="sxs-lookup"><span data-stu-id="219ac-105">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="219ac-106">Operacja tworzenia nie wymaga elementu eTag.</span><span class="sxs-lookup"><span data-stu-id="219ac-106">Create operation does not require eTag.</span></span>

## <span data-ttu-id="219ac-107">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="219ac-107">SYNTAX</span></span>

### <span data-ttu-id="219ac-108">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="219ac-108">UpdateExpanded (Default)</span></span>
```
Update-AzCostManagementExport -Name <String> -Scope <String> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-ETag <String>] [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="219ac-109">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="219ac-109">UpdateViaIdentityExpanded</span></span>
```
Update-AzCostManagementExport -InputObject <ICostManagementIdentity> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-ETag <String>] [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="219ac-110">Opis</span><span class="sxs-lookup"><span data-stu-id="219ac-110">DESCRIPTION</span></span>
<span data-ttu-id="219ac-111">Operacja tworzenia lub aktualizowania eksportu.</span><span class="sxs-lookup"><span data-stu-id="219ac-111">The operation to create or update a export.</span></span>
<span data-ttu-id="219ac-112">Operacja aktualizacji wymaga, aby w żądaniu została ustawiona Najnowsza wersja elementu eTag.</span><span class="sxs-lookup"><span data-stu-id="219ac-112">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="219ac-113">Najnowszy element eTag można uzyskać, wykonując operację pobierania.</span><span class="sxs-lookup"><span data-stu-id="219ac-113">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="219ac-114">Operacja tworzenia nie wymaga elementu eTag.</span><span class="sxs-lookup"><span data-stu-id="219ac-114">Create operation does not require eTag.</span></span>

## <span data-ttu-id="219ac-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="219ac-115">EXAMPLES</span></span>

### <span data-ttu-id="219ac-116">Przykład 1: aktualizowanie AzCostManagementExport według zakresu i nazwy</span><span class="sxs-lookup"><span data-stu-id="219ac-116">Example 1: Update AzCostManagementExport by scope and name</span></span>
```powershell
PS C:\> Update-AzCostManagementExport -Scope "subscriptions//*********" -Name "TestExport" -ScheduleRecurrence 'Weekly'

ETag              Name                                 Type
----              ----                                 ----
"********" TestExportDatasetAggregationInfo Microsoft.CostManagement/exports
```

<span data-ttu-id="219ac-117">Aktualizowanie AzCostManagementExport według zakresu i nazwy</span><span class="sxs-lookup"><span data-stu-id="219ac-117">Update AzCostManagementExport by Scope and name</span></span>

### <span data-ttu-id="219ac-118">Przykład 2: aktualizowanie AzCostManagementExport przez wejście</span><span class="sxs-lookup"><span data-stu-id="219ac-118">Example 2: Update AzCostManagementExport by InputObject</span></span>
```powershell
PS C:\> $oldExport = Get-AzCostManagementExport -Scope "subscriptions/*********" -Name "TestExport"
Update-AzCostManagementExport -InputObject $oldExport -ScheduleRecurrence 'Weekly'

ETag              Name                                 Type
----              ----                                 ----
"********" TestExportDatasetAggregationInfo Microsoft.CostManagement/exports
```

<span data-ttu-id="219ac-119">Aktualizowanie AzCostManagementExport przez wejście</span><span class="sxs-lookup"><span data-stu-id="219ac-119">Update AzCostManagementExport by InputObject</span></span>

## <span data-ttu-id="219ac-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="219ac-120">PARAMETERS</span></span>

### <span data-ttu-id="219ac-121">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="219ac-121">-ConfigurationColumn</span></span>
<span data-ttu-id="219ac-122">Tablica nazw kolumn, które mają zostać uwzględnione w eksporcie.</span><span class="sxs-lookup"><span data-stu-id="219ac-122">Array of column names to be included in the export.</span></span>
<span data-ttu-id="219ac-123">Jeśli nie podano, wówczas eksport będzie obejmował wszystkie dostępne kolumny.</span><span class="sxs-lookup"><span data-stu-id="219ac-123">If not provided then the export will include all available columns.</span></span>
<span data-ttu-id="219ac-124">Dostępne kolumny mogą się różnić w zależności od kanału klienta (Zobacz przykłady).</span><span class="sxs-lookup"><span data-stu-id="219ac-124">The available columns can vary by customer channel (see examples).</span></span>

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

### <span data-ttu-id="219ac-125">-DataSetGranularity</span><span class="sxs-lookup"><span data-stu-id="219ac-125">-DataSetGranularity</span></span>
<span data-ttu-id="219ac-126">Stopień szczegółowości eksportu wierszy.</span><span class="sxs-lookup"><span data-stu-id="219ac-126">The granularity of rows in the export.</span></span>
<span data-ttu-id="219ac-127">Obecnie jest obsługiwana tylko codzienna.</span><span class="sxs-lookup"><span data-stu-id="219ac-127">Currently only 'Daily' is supported.</span></span>

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

### <span data-ttu-id="219ac-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="219ac-128">-DefaultProfile</span></span>
<span data-ttu-id="219ac-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="219ac-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="219ac-130">-DefinitionTimeframe</span><span class="sxs-lookup"><span data-stu-id="219ac-130">-DefinitionTimeframe</span></span>
<span data-ttu-id="219ac-131">Przedział czasu na ściąganie danych do eksportu.</span><span class="sxs-lookup"><span data-stu-id="219ac-131">The time frame for pulling data for the export.</span></span>
<span data-ttu-id="219ac-132">Jeśli jest niestandardowa, należy podać konkretny przedział czasu.</span><span class="sxs-lookup"><span data-stu-id="219ac-132">If custom, then a specific time period must be provided.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.TimeframeType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="219ac-133">-Definitiontype</span><span class="sxs-lookup"><span data-stu-id="219ac-133">-DefinitionType</span></span>
<span data-ttu-id="219ac-134">Typ eksportu.</span><span class="sxs-lookup"><span data-stu-id="219ac-134">The type of the export.</span></span>
<span data-ttu-id="219ac-135">Należy zwrócić uwagę, że "użycie" odpowiada "ActualCost" i dotyczy eksportu, które jeszcze nie udostępniają danych opłat lub umorzenia na potrzeby rezerwacji usług.</span><span class="sxs-lookup"><span data-stu-id="219ac-135">Note that 'Usage' is equivalent to 'ActualCost' and is applicable to exports that do not yet provide data for charges or amortization for service reservations.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.ExportType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="219ac-136">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="219ac-136">-DestinationContainer</span></span>
<span data-ttu-id="219ac-137">Nazwa kontenera, w którym zostanie przekazany wywóz.</span><span class="sxs-lookup"><span data-stu-id="219ac-137">The name of the container where exports will be uploaded.</span></span>

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

### <span data-ttu-id="219ac-138">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="219ac-138">-DestinationResourceId</span></span>
<span data-ttu-id="219ac-139">Identyfikator zasobu konta magazynu, w którym zostanie dostarczony eksport.</span><span class="sxs-lookup"><span data-stu-id="219ac-139">The resource id of the storage account where exports will be delivered.</span></span>

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

### <span data-ttu-id="219ac-140">-DestinationRootFolderPath</span><span class="sxs-lookup"><span data-stu-id="219ac-140">-DestinationRootFolderPath</span></span>
<span data-ttu-id="219ac-141">Nazwa katalogu, w którym będą przekazywane eksportowane.</span><span class="sxs-lookup"><span data-stu-id="219ac-141">The name of the directory where exports will be uploaded.</span></span>

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

### <span data-ttu-id="219ac-142">-ETag</span><span class="sxs-lookup"><span data-stu-id="219ac-142">-ETag</span></span>
<span data-ttu-id="219ac-143">element eTag zasobu.</span><span class="sxs-lookup"><span data-stu-id="219ac-143">eTag of the resource.</span></span>
<span data-ttu-id="219ac-144">W celu obsługi współbieżnych scenariuszy aktualizacji to pole będzie używane do określania, czy użytkownik aktualizuje najnowszą wersję.</span><span class="sxs-lookup"><span data-stu-id="219ac-144">To handle concurrent update scenario, this field will be used to determine whether the user is updating the latest version or not.</span></span>

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

### <span data-ttu-id="219ac-145">-Format</span><span class="sxs-lookup"><span data-stu-id="219ac-145">-Format</span></span>
<span data-ttu-id="219ac-146">Format dostarczanego eksportu.</span><span class="sxs-lookup"><span data-stu-id="219ac-146">The format of the export being delivered.</span></span>
<span data-ttu-id="219ac-147">Obecnie obsługiwane są tylko słowa "CSV".</span><span class="sxs-lookup"><span data-stu-id="219ac-147">Currently only 'Csv' is supported.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.FormatType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="219ac-148">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="219ac-148">-InputObject</span></span>
<span data-ttu-id="219ac-149">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="219ac-149">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="219ac-150">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="219ac-150">-Name</span></span>
<span data-ttu-id="219ac-151">Eksportuj nazwę.</span><span class="sxs-lookup"><span data-stu-id="219ac-151">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ExportName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="219ac-152">-RecurrencePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="219ac-152">-RecurrencePeriodFrom</span></span>
<span data-ttu-id="219ac-153">Data rozpoczęcia cyklu.</span><span class="sxs-lookup"><span data-stu-id="219ac-153">The start date of recurrence.</span></span>

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

### <span data-ttu-id="219ac-154">-RecurrencePeriodTo</span><span class="sxs-lookup"><span data-stu-id="219ac-154">-RecurrencePeriodTo</span></span>
<span data-ttu-id="219ac-155">Data zakończenia cyklu.</span><span class="sxs-lookup"><span data-stu-id="219ac-155">The end date of recurrence.</span></span>

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

### <span data-ttu-id="219ac-156">-ScheduleRecurrence</span><span class="sxs-lookup"><span data-stu-id="219ac-156">-ScheduleRecurrence</span></span>
<span data-ttu-id="219ac-157">Cykl planowania.</span><span class="sxs-lookup"><span data-stu-id="219ac-157">The schedule recurrence.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.RecurrenceType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="219ac-158">-ScheduleStatus</span><span class="sxs-lookup"><span data-stu-id="219ac-158">-ScheduleStatus</span></span>
<span data-ttu-id="219ac-159">Stan harmonogramu eksportu.</span><span class="sxs-lookup"><span data-stu-id="219ac-159">The status of the export's schedule.</span></span>
<span data-ttu-id="219ac-160">Jeśli nie jest aktywny, harmonogram eksportu jest wstrzymany.</span><span class="sxs-lookup"><span data-stu-id="219ac-160">If 'Inactive', the export's schedule is paused.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.StatusType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="219ac-161">-Zakres</span><span class="sxs-lookup"><span data-stu-id="219ac-161">-Scope</span></span>
<span data-ttu-id="219ac-162">Ten parametr definiuje zakres costmanagement z różnych perspektyw "abonament", "Resources" i "świadczenie usługi".</span><span class="sxs-lookup"><span data-stu-id="219ac-162">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="219ac-163">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="219ac-163">-TimePeriodFrom</span></span>
<span data-ttu-id="219ac-164">Data rozpoczęcia eksportowania danych.</span><span class="sxs-lookup"><span data-stu-id="219ac-164">The start date for export data.</span></span>

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

### <span data-ttu-id="219ac-165">-TimePeriodTo</span><span class="sxs-lookup"><span data-stu-id="219ac-165">-TimePeriodTo</span></span>
<span data-ttu-id="219ac-166">Data zakończenia eksportowania danych.</span><span class="sxs-lookup"><span data-stu-id="219ac-166">The end date for export data.</span></span>

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

### <span data-ttu-id="219ac-167">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="219ac-167">-Confirm</span></span>
<span data-ttu-id="219ac-168">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="219ac-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="219ac-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="219ac-169">-WhatIf</span></span>
<span data-ttu-id="219ac-170">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="219ac-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="219ac-171">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="219ac-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="219ac-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="219ac-172">CommonParameters</span></span>
<span data-ttu-id="219ac-173">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="219ac-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="219ac-174">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="219ac-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="219ac-175">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="219ac-175">INPUTS</span></span>

### <span data-ttu-id="219ac-176">Microsoft. Azure. PowerShell. polecenia. CostManagement. models. ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="219ac-176">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="219ac-177">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="219ac-177">OUTPUTS</span></span>

### <span data-ttu-id="219ac-178">Microsoft. Azure. PowerShell. polecenia. CostManagement. models. Api20200601. IExport</span><span class="sxs-lookup"><span data-stu-id="219ac-178">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="219ac-179">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="219ac-179">NOTES</span></span>

<span data-ttu-id="219ac-180">PISUJE</span><span class="sxs-lookup"><span data-stu-id="219ac-180">ALIASES</span></span>

<span data-ttu-id="219ac-181">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="219ac-181">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="219ac-182">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="219ac-182">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="219ac-183">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="219ac-183">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="219ac-184">INPUTobject <ICostManagementIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="219ac-184">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="219ac-185">`[AlertId <String>]`: Identyfikator alertu</span><span class="sxs-lookup"><span data-stu-id="219ac-185">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="219ac-186">`[ExportName <String>]`: Nazwa eksportu.</span><span class="sxs-lookup"><span data-stu-id="219ac-186">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="219ac-187">`[ExternalCloudProviderId <String>]`: Może to być "{externalSubscriptionId}" dla połączonego konta lub "{externalBillingAccountId}" dla konta skonsolidowanego, które jest używane z operacjami wymiaru/kwerendy.</span><span class="sxs-lookup"><span data-stu-id="219ac-187">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="219ac-188">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: Typ zewnętrznego dostawcy chmury skojarzony z operacjami wymiaru/kwerendy.</span><span class="sxs-lookup"><span data-stu-id="219ac-188">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="219ac-189">Obejmuje to "externalSubscriptions" dla połączonego konta, a także "externalBillingAccounts" dla konta skonsolidowanego.</span><span class="sxs-lookup"><span data-stu-id="219ac-189">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="219ac-190">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="219ac-190">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="219ac-191">`[Scope <String>]`: Zakres skojarzony z operacjami wyświetlania.</span><span class="sxs-lookup"><span data-stu-id="219ac-191">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="219ac-192">Obejmuje to "abonament/{subskrypcji}" dla zakresu abonamentu, "abonaments/{Binding}/resourceGroups/{resourceGroupName}" dla zakresu grupy zasobów. Providers/Microsoft. rozliczenia/billingAccounts/{billingAccountId} "dla zakresu kont rozliczeniowych" Providers/Microsoft. rozliczenia/billingAccounts/{billingAccountId}/działy/{departmentId} "dla zakresu działu," Providers/Microsoft. rozliczenia/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId} "dla zakresu EnrollmentAccount," Providers/Microsoft. rozliczenia/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId} "dla zakresu BillingProfile," Providers/Microsoft. rozliczenia/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId} "dla zakresu InvoiceSection," Providers/Microsoft. Management/managementGroups/{managementGroupId} ' dla zakresu grupy zarządzania, "Providers/Microsoft. CostManagement/externalBillingAccounts/{externalBillingAccountName}" dla zewnętrznego zakresu konta rozliczeniowego i "Providers/Microsoft. CostManagement/externalSubscriptions/{externalSubscriptionName}" dla zakresu subskrypcji zewnętrznej.</span><span class="sxs-lookup"><span data-stu-id="219ac-192">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="219ac-193">`[ViewName <String>]`: Nazwa widoku</span><span class="sxs-lookup"><span data-stu-id="219ac-193">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="219ac-194">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="219ac-194">RELATED LINKS</span></span>

