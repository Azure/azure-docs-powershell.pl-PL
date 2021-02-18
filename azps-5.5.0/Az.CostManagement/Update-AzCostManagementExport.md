---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/update-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Update-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Update-AzCostManagementExport.md
ms.openlocfilehash: 310600555f36fa0f6b129f2cf2a84581ffad044b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181155"
---
# <span data-ttu-id="4d1e8-101">Update-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="4d1e8-101">Update-AzCostManagementExport</span></span>

## <span data-ttu-id="4d1e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d1e8-102">SYNOPSIS</span></span>
<span data-ttu-id="4d1e8-103">Operacja tworzenia lub aktualizowania eksportu.</span><span class="sxs-lookup"><span data-stu-id="4d1e8-103">The operation to create or update a export.</span></span>
<span data-ttu-id="4d1e8-104">Operacja aktualizacji wymaga ustawienia najnowszego tagu eTag w żądaniu.</span><span class="sxs-lookup"><span data-stu-id="4d1e8-104">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="4d1e8-105">Możesz uzyskać najnowszy tag eTag, wykonując operację uzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="4d1e8-105">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="4d1e8-106">Operacja tworzenia nie wymaga tagu eTag.</span><span class="sxs-lookup"><span data-stu-id="4d1e8-106">Create operation does not require eTag.</span></span>

## <span data-ttu-id="4d1e8-107">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4d1e8-107">SYNTAX</span></span>

### <span data-ttu-id="4d1e8-108">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="4d1e8-108">UpdateExpanded (Default)</span></span>
```
Update-AzCostManagementExport -Name <String> -Scope <String> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-ETag <String>] [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4d1e8-109">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="4d1e8-109">UpdateViaIdentityExpanded</span></span>
```
Update-AzCostManagementExport -InputObject <ICostManagementIdentity> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-ETag <String>] [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4d1e8-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="4d1e8-110">DESCRIPTION</span></span>
<span data-ttu-id="4d1e8-111">Operacja tworzenia lub aktualizowania eksportu.</span><span class="sxs-lookup"><span data-stu-id="4d1e8-111">The operation to create or update a export.</span></span>
<span data-ttu-id="4d1e8-112">Operacja aktualizacji wymaga ustawienia najnowszego tagu eTag w żądaniu.</span><span class="sxs-lookup"><span data-stu-id="4d1e8-112">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="4d1e8-113">Możesz uzyskać najnowszy tag eTag, wykonując operację uzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="4d1e8-113">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="4d1e8-114">Operacja tworzenia nie wymaga tagu eTag.</span><span class="sxs-lookup"><span data-stu-id="4d1e8-114">Create operation does not require eTag.</span></span>

## <span data-ttu-id="4d1e8-115">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4d1e8-115">EXAMPLES</span></span>

### <span data-ttu-id="4d1e8-116">Przykład 1. Aktualizowanie pola AzCostManagementExport według zakresu i nazwy</span><span class="sxs-lookup"><span data-stu-id="4d1e8-116">Example 1: Update AzCostManagementExport by scope and name</span></span>
```powershell
PS C:\> Update-AzCostManagementExport -Scope "subscriptions//*********" -Name "TestExport" -ScheduleRecurrence 'Weekly'

ETag              Name                                 Type
----              ----                                 ----
"********" TestExportDatasetAggregationInfo Microsoft.CostManagement/exports
```

<span data-ttu-id="4d1e8-117">Aktualizowanie pliku AzCostManagementExport według zakresu i nazwy</span><span class="sxs-lookup"><span data-stu-id="4d1e8-117">Update AzCostManagementExport by Scope and name</span></span>

### <span data-ttu-id="4d1e8-118">Przykład 2. Aktualizacja azCostManagementExport przez InputObject</span><span class="sxs-lookup"><span data-stu-id="4d1e8-118">Example 2: Update AzCostManagementExport by InputObject</span></span>
```powershell
PS C:\> $oldExport = Get-AzCostManagementExport -Scope "subscriptions/*********" -Name "TestExport"
Update-AzCostManagementExport -InputObject $oldExport -ScheduleRecurrence 'Weekly'

ETag              Name                                 Type
----              ----                                 ----
"********" TestExportDatasetAggregationInfo Microsoft.CostManagement/exports
```

<span data-ttu-id="4d1e8-119">Aktualizuj azCostManagementExport by InputObject</span><span class="sxs-lookup"><span data-stu-id="4d1e8-119">Update AzCostManagementExport by InputObject</span></span>

## <span data-ttu-id="4d1e8-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d1e8-120">PARAMETERS</span></span>

### <span data-ttu-id="4d1e8-121">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="4d1e8-121">-ConfigurationColumn</span></span>
<span data-ttu-id="4d1e8-122">Tablica nazw kolumn do uwzględnionia w eksporcie.</span><span class="sxs-lookup"><span data-stu-id="4d1e8-122">Array of column names to be included in the export.</span></span>
<span data-ttu-id="4d1e8-123">Jeśli nie zostanie podany, eksport będzie zawierać wszystkie dostępne kolumny.</span><span class="sxs-lookup"><span data-stu-id="4d1e8-123">If not provided then the export will include all available columns.</span></span>
<span data-ttu-id="4d1e8-124">Dostępne kolumny mogą się różnić w zależności od kanału klienta (zobacz przykłady).</span><span class="sxs-lookup"><span data-stu-id="4d1e8-124">The available columns can vary by customer channel (see examples).</span></span>

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

### <span data-ttu-id="4d1e8-125">-DataSetGranularity</span><span class="sxs-lookup"><span data-stu-id="4d1e8-125">-DataSetGranularity</span></span>
<span data-ttu-id="4d1e8-126">Szczegółowość wierszy w eksporcie.</span><span class="sxs-lookup"><span data-stu-id="4d1e8-126">The granularity of rows in the export.</span></span>
<span data-ttu-id="4d1e8-127">Obecnie obsługiwany jest tylko "Dzienny".</span><span class="sxs-lookup"><span data-stu-id="4d1e8-127">Currently only 'Daily' is supported.</span></span>

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

### <span data-ttu-id="4d1e8-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d1e8-128">-DefaultProfile</span></span>
<span data-ttu-id="4d1e8-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4d1e8-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d1e8-130">-DefinitionTimeframe</span><span class="sxs-lookup"><span data-stu-id="4d1e8-130">-DefinitionTimeframe</span></span>
<span data-ttu-id="4d1e8-131">Ramy czasowe dla ściągania danych do eksportu.</span><span class="sxs-lookup"><span data-stu-id="4d1e8-131">The time frame for pulling data for the export.</span></span>
<span data-ttu-id="4d1e8-132">Jeśli jest to niestandardowe, należy podać określony okres.</span><span class="sxs-lookup"><span data-stu-id="4d1e8-132">If custom, then a specific time period must be provided.</span></span>

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

### <span data-ttu-id="4d1e8-133">-DefinitionType</span><span class="sxs-lookup"><span data-stu-id="4d1e8-133">-DefinitionType</span></span>
<span data-ttu-id="4d1e8-134">Typ eksportu.</span><span class="sxs-lookup"><span data-stu-id="4d1e8-134">The type of the export.</span></span>
<span data-ttu-id="4d1e8-135">Zwróć uwagę, że wartość "Użycie" jest równoważna wartości "Koszt Rzeczywisty" i ma zastosowanie do eksportów, które jeszcze nie zawierają danych dotyczących opłat lub amortowania rezerwacji usług.</span><span class="sxs-lookup"><span data-stu-id="4d1e8-135">Note that 'Usage' is equivalent to 'ActualCost' and is applicable to exports that do not yet provide data for charges or amortization for service reservations.</span></span>

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

### <span data-ttu-id="4d1e8-136">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="4d1e8-136">-DestinationContainer</span></span>
<span data-ttu-id="4d1e8-137">Nazwa kontenera, do którego zostaną przekazane eksporty.</span><span class="sxs-lookup"><span data-stu-id="4d1e8-137">The name of the container where exports will be uploaded.</span></span>

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

### <span data-ttu-id="4d1e8-138">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="4d1e8-138">-DestinationResourceId</span></span>
<span data-ttu-id="4d1e8-139">Identyfikator zasobu konta magazynu, do którego będą dostarczane eksporty.</span><span class="sxs-lookup"><span data-stu-id="4d1e8-139">The resource id of the storage account where exports will be delivered.</span></span>

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

### <span data-ttu-id="4d1e8-140">-DestinationRootFolderPath</span><span class="sxs-lookup"><span data-stu-id="4d1e8-140">-DestinationRootFolderPath</span></span>
<span data-ttu-id="4d1e8-141">Nazwa katalogu, do którego będą przekazywane eksporty.</span><span class="sxs-lookup"><span data-stu-id="4d1e8-141">The name of the directory where exports will be uploaded.</span></span>

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

### <span data-ttu-id="4d1e8-142">— ETag</span><span class="sxs-lookup"><span data-stu-id="4d1e8-142">-ETag</span></span>
<span data-ttu-id="4d1e8-143">Tag eTag zasobu.</span><span class="sxs-lookup"><span data-stu-id="4d1e8-143">eTag of the resource.</span></span>
<span data-ttu-id="4d1e8-144">Do obsługi scenariusza jednoczesnej aktualizacji to pole służy do określania, czy użytkownik aktualizuje najnowszą wersję.</span><span class="sxs-lookup"><span data-stu-id="4d1e8-144">To handle concurrent update scenario, this field will be used to determine whether the user is updating the latest version or not.</span></span>

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

### <span data-ttu-id="4d1e8-145">— Format</span><span class="sxs-lookup"><span data-stu-id="4d1e8-145">-Format</span></span>
<span data-ttu-id="4d1e8-146">Format dostarczanego eksportu.</span><span class="sxs-lookup"><span data-stu-id="4d1e8-146">The format of the export being delivered.</span></span>
<span data-ttu-id="4d1e8-147">Obecnie jest obsługiwana tylko wartość Csv.</span><span class="sxs-lookup"><span data-stu-id="4d1e8-147">Currently only 'Csv' is supported.</span></span>

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

### <span data-ttu-id="4d1e8-148">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d1e8-148">-InputObject</span></span>
<span data-ttu-id="4d1e8-149">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="4d1e8-149">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4d1e8-150">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4d1e8-150">-Name</span></span>
<span data-ttu-id="4d1e8-151">Eksportuj nazwę.</span><span class="sxs-lookup"><span data-stu-id="4d1e8-151">Export Name.</span></span>

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

### <span data-ttu-id="4d1e8-152">-RecurrencePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="4d1e8-152">-RecurrencePeriodFrom</span></span>
<span data-ttu-id="4d1e8-153">Data rozpoczęcia cyklu.</span><span class="sxs-lookup"><span data-stu-id="4d1e8-153">The start date of recurrence.</span></span>

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

### <span data-ttu-id="4d1e8-154">-RecurrencePeriodTo</span><span class="sxs-lookup"><span data-stu-id="4d1e8-154">-RecurrencePeriodTo</span></span>
<span data-ttu-id="4d1e8-155">Data zakończenia cyklu.</span><span class="sxs-lookup"><span data-stu-id="4d1e8-155">The end date of recurrence.</span></span>

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

### <span data-ttu-id="4d1e8-156">-ScheduleRecurrence</span><span class="sxs-lookup"><span data-stu-id="4d1e8-156">-ScheduleRecurrence</span></span>
<span data-ttu-id="4d1e8-157">Cykl harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="4d1e8-157">The schedule recurrence.</span></span>

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

### <span data-ttu-id="4d1e8-158">-ScheduleStatus</span><span class="sxs-lookup"><span data-stu-id="4d1e8-158">-ScheduleStatus</span></span>
<span data-ttu-id="4d1e8-159">Stan harmonogramu eksportu.</span><span class="sxs-lookup"><span data-stu-id="4d1e8-159">The status of the export's schedule.</span></span>
<span data-ttu-id="4d1e8-160">Jeśli termin "Nieaktywny" jest wstrzymany, harmonogram eksportu zostanie wstrzymany.</span><span class="sxs-lookup"><span data-stu-id="4d1e8-160">If 'Inactive', the export's schedule is paused.</span></span>

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

### <span data-ttu-id="4d1e8-161">— Zakres</span><span class="sxs-lookup"><span data-stu-id="4d1e8-161">-Scope</span></span>
<span data-ttu-id="4d1e8-162">Ten parametr definiuje zakres zarządzania kosztami z innej perspektywy: "Subskrypcja", "Grupa zasobów" i "Udostępnij usługę".</span><span class="sxs-lookup"><span data-stu-id="4d1e8-162">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="4d1e8-163">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="4d1e8-163">-TimePeriodFrom</span></span>
<span data-ttu-id="4d1e8-164">Data rozpoczęcia eksportu danych.</span><span class="sxs-lookup"><span data-stu-id="4d1e8-164">The start date for export data.</span></span>

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

### <span data-ttu-id="4d1e8-165">-TimePeriodTo</span><span class="sxs-lookup"><span data-stu-id="4d1e8-165">-TimePeriodTo</span></span>
<span data-ttu-id="4d1e8-166">Data zakończenia eksportu danych.</span><span class="sxs-lookup"><span data-stu-id="4d1e8-166">The end date for export data.</span></span>

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

### <span data-ttu-id="4d1e8-167">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4d1e8-167">-Confirm</span></span>
<span data-ttu-id="4d1e8-168">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4d1e8-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d1e8-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d1e8-169">-WhatIf</span></span>
<span data-ttu-id="4d1e8-170">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d1e8-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d1e8-171">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4d1e8-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d1e8-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d1e8-172">CommonParameters</span></span>
<span data-ttu-id="4d1e8-173">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d1e8-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d1e8-174">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4d1e8-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d1e8-175">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d1e8-175">INPUTS</span></span>

### <span data-ttu-id="4d1e8-176">Microsoft.Azure.PowerShell.Cmdlet.CostManagement.Models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="4d1e8-176">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="4d1e8-177">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d1e8-177">OUTPUTS</span></span>

### <span data-ttu-id="4d1e8-178">Microsoft.Azure.PowerShell.Cmdlet.CostManagement.Models.Api20200601.IExport</span><span class="sxs-lookup"><span data-stu-id="4d1e8-178">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="4d1e8-179">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4d1e8-179">NOTES</span></span>

<span data-ttu-id="4d1e8-180">ALIASY</span><span class="sxs-lookup"><span data-stu-id="4d1e8-180">ALIASES</span></span>

<span data-ttu-id="4d1e8-181">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4d1e8-181">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4d1e8-182">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="4d1e8-182">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4d1e8-183">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4d1e8-183">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4d1e8-184">INPUTOBJECT: <ICostManagementIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="4d1e8-184">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4d1e8-185">`[AlertId <String>]`: Identyfikator alertu</span><span class="sxs-lookup"><span data-stu-id="4d1e8-185">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="4d1e8-186">`[ExportName <String>]`: Eksportuj nazwę.</span><span class="sxs-lookup"><span data-stu-id="4d1e8-186">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="4d1e8-187">`[ExternalCloudProviderId <String>]`: W przypadku konta połączonego może to być wartość "{externalSubscriptionId}" lub "{externalBillingAccountId}" w przypadku skonsolidowanego konta używanego z operacjami wymiaru/zapytania.</span><span class="sxs-lookup"><span data-stu-id="4d1e8-187">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="4d1e8-188">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: Typ dostawcy chmury zewnętrznej skojarzony z operacjami wymiar/kwerenda.</span><span class="sxs-lookup"><span data-stu-id="4d1e8-188">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="4d1e8-189">Obejmuje to "zewnętrzneSubskrypcje" dla konta połączonego i "externalBillingAccounts" dla skonsolidowanego konta.</span><span class="sxs-lookup"><span data-stu-id="4d1e8-189">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="4d1e8-190">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="4d1e8-190">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4d1e8-191">`[Scope <String>]`: zakres skojarzony z operacjami wyświetlania.</span><span class="sxs-lookup"><span data-stu-id="4d1e8-191">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="4d1e8-192">Obejmuje to "subskrypcje/{subscriptionId}" dla zakresu subskrypcji, "subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}" dla zakresu resourceGroup, "providers/Microsoft.Billing/billingAccounts/{billingAccountId}" dla zakresu Konto rozliczeniowe, "providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}" dla zakresu Dział, "providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}" dla zakresu EnrollmentAccount, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management /managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span><span class="sxs-lookup"><span data-stu-id="4d1e8-192">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="4d1e8-193">`[ViewName <String>]`: nazwa widoku</span><span class="sxs-lookup"><span data-stu-id="4d1e8-193">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="4d1e8-194">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4d1e8-194">RELATED LINKS</span></span>

