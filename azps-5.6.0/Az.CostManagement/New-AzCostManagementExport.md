---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.costmanagement/new-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementExport.md
ms.openlocfilehash: bc3ff9c6d27cba92cf29090dda988a27f9e8a50b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010673"
---
# <span data-ttu-id="d3840-101">New-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="d3840-101">New-AzCostManagementExport</span></span>

## <span data-ttu-id="d3840-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3840-102">SYNOPSIS</span></span>
<span data-ttu-id="d3840-103">Operacja tworzenia lub aktualizowania eksportu.</span><span class="sxs-lookup"><span data-stu-id="d3840-103">The operation to create or update a export.</span></span>
<span data-ttu-id="d3840-104">Operacja aktualizacji wymaga ustawienia najnowszego tagu eTag w żądaniu.</span><span class="sxs-lookup"><span data-stu-id="d3840-104">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="d3840-105">Możesz uzyskać najnowszy tag eTag, wykonując operację uzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="d3840-105">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="d3840-106">Operacja tworzenia nie wymaga tagu eTag.</span><span class="sxs-lookup"><span data-stu-id="d3840-106">Create operation does not require eTag.</span></span>

## <span data-ttu-id="d3840-107">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d3840-107">SYNTAX</span></span>

```
New-AzCostManagementExport -Name <String> -Scope <String> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d3840-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d3840-108">DESCRIPTION</span></span>
<span data-ttu-id="d3840-109">Operacja tworzenia lub aktualizowania eksportu.</span><span class="sxs-lookup"><span data-stu-id="d3840-109">The operation to create or update a export.</span></span>
<span data-ttu-id="d3840-110">Operacja aktualizacji wymaga ustawienia najnowszego tagu eTag w żądaniu.</span><span class="sxs-lookup"><span data-stu-id="d3840-110">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="d3840-111">Możesz uzyskać najnowszy tag eTag, wykonując operację uzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="d3840-111">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="d3840-112">Operacja tworzenia nie wymaga tagu eTag.</span><span class="sxs-lookup"><span data-stu-id="d3840-112">Create operation does not require eTag.</span></span>

## <span data-ttu-id="d3840-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d3840-113">EXAMPLES</span></span>

### <span data-ttu-id="d3840-114">Przykład 1. Tworzenie an AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="d3840-114">Example 1: Create an AzCostManagementExport</span></span>
```powershell
PS C:\> New-AzCostManagementExport -Scope "subscriptions/***********" -Name "CostManagementExportTest" -ScheduleStatus "Active" -ScheduleRecurrence "Daily" -RecurrencePeriodFrom "2020-10-31T20:00:00Z" -RecurrencePeriodTo "2020-11-30T00:00:00Z" -Format "Csv" -DestinationResourceId "/subscriptions/*************/resourceGroups/ResourceGroupTest/providers/Microsoft.Storage/storageAccounts/storageAccountTest" `  -DestinationContainer "exports" -DestinationRootFolderPath "ad-hoc" -DefinitionType "Usage" -DefinitionTimeframe "MonthToDate" -DatasetGranularity "Daily"

ETag              Name                                      Type
----              ----                                      ----
"********" TestExportDatasetAggregationInfosagdhaghj Microsoft.CostManagement/exports
```

<span data-ttu-id="d3840-115">Tworzenie azCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="d3840-115">Create an AzCostManagementExport</span></span>

## <span data-ttu-id="d3840-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3840-116">PARAMETERS</span></span>

### <span data-ttu-id="d3840-117">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="d3840-117">-ConfigurationColumn</span></span>
<span data-ttu-id="d3840-118">Tablica nazw kolumn do uwzględnionia w eksporcie.</span><span class="sxs-lookup"><span data-stu-id="d3840-118">Array of column names to be included in the export.</span></span>
<span data-ttu-id="d3840-119">Jeśli nie zostanie podany, eksport będzie zawierać wszystkie dostępne kolumny.</span><span class="sxs-lookup"><span data-stu-id="d3840-119">If not provided then the export will include all available columns.</span></span>
<span data-ttu-id="d3840-120">Dostępne kolumny mogą się różnić w zależności od kanału klienta (zobacz przykłady).</span><span class="sxs-lookup"><span data-stu-id="d3840-120">The available columns can vary by customer channel (see examples).</span></span>

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

### <span data-ttu-id="d3840-121">-DataSetGranularity</span><span class="sxs-lookup"><span data-stu-id="d3840-121">-DataSetGranularity</span></span>
<span data-ttu-id="d3840-122">Szczegółowość wierszy w eksporcie.</span><span class="sxs-lookup"><span data-stu-id="d3840-122">The granularity of rows in the export.</span></span>
<span data-ttu-id="d3840-123">Obecnie obsługiwany jest tylko "Dzienny".</span><span class="sxs-lookup"><span data-stu-id="d3840-123">Currently only 'Daily' is supported.</span></span>

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

### <span data-ttu-id="d3840-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3840-124">-DefaultProfile</span></span>
<span data-ttu-id="d3840-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d3840-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3840-126">-DefinitionTimeframe</span><span class="sxs-lookup"><span data-stu-id="d3840-126">-DefinitionTimeframe</span></span>
<span data-ttu-id="d3840-127">Ramy czasowe dla ściągania danych do eksportu.</span><span class="sxs-lookup"><span data-stu-id="d3840-127">The time frame for pulling data for the export.</span></span>
<span data-ttu-id="d3840-128">Jeśli jest to niestandardowe, należy podać określony okres.</span><span class="sxs-lookup"><span data-stu-id="d3840-128">If custom, then a specific time period must be provided.</span></span>

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

### <span data-ttu-id="d3840-129">-DefinitionType</span><span class="sxs-lookup"><span data-stu-id="d3840-129">-DefinitionType</span></span>
<span data-ttu-id="d3840-130">Typ eksportu.</span><span class="sxs-lookup"><span data-stu-id="d3840-130">The type of the export.</span></span>
<span data-ttu-id="d3840-131">Zwróć uwagę, że wartość "Użycie" jest równoważna wartości "Koszt Rzeczywisty" i ma zastosowanie do eksportów, które jeszcze nie zawierają danych dotyczących opłat lub amortowania rezerwacji usług.</span><span class="sxs-lookup"><span data-stu-id="d3840-131">Note that 'Usage' is equivalent to 'ActualCost' and is applicable to exports that do not yet provide data for charges or amortization for service reservations.</span></span>

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

### <span data-ttu-id="d3840-132">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="d3840-132">-DestinationContainer</span></span>
<span data-ttu-id="d3840-133">Nazwa kontenera, do którego zostaną przekazane eksporty.</span><span class="sxs-lookup"><span data-stu-id="d3840-133">The name of the container where exports will be uploaded.</span></span>

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

### <span data-ttu-id="d3840-134">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="d3840-134">-DestinationResourceId</span></span>
<span data-ttu-id="d3840-135">Identyfikator zasobu konta magazynu, do którego będą dostarczane eksporty.</span><span class="sxs-lookup"><span data-stu-id="d3840-135">The resource id of the storage account where exports will be delivered.</span></span>

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

### <span data-ttu-id="d3840-136">-DestinationRootFolderPath</span><span class="sxs-lookup"><span data-stu-id="d3840-136">-DestinationRootFolderPath</span></span>
<span data-ttu-id="d3840-137">Nazwa katalogu, do którego będą przekazywane eksporty.</span><span class="sxs-lookup"><span data-stu-id="d3840-137">The name of the directory where exports will be uploaded.</span></span>

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

### <span data-ttu-id="d3840-138">— Format</span><span class="sxs-lookup"><span data-stu-id="d3840-138">-Format</span></span>
<span data-ttu-id="d3840-139">Format dostarczanego eksportu.</span><span class="sxs-lookup"><span data-stu-id="d3840-139">The format of the export being delivered.</span></span>
<span data-ttu-id="d3840-140">Obecnie jest obsługiwana tylko wartość Csv.</span><span class="sxs-lookup"><span data-stu-id="d3840-140">Currently only 'Csv' is supported.</span></span>

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

### <span data-ttu-id="d3840-141">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d3840-141">-Name</span></span>
<span data-ttu-id="d3840-142">Eksportuj nazwę.</span><span class="sxs-lookup"><span data-stu-id="d3840-142">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExportName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3840-143">-RecurrencePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="d3840-143">-RecurrencePeriodFrom</span></span>
<span data-ttu-id="d3840-144">Data rozpoczęcia cyklu.</span><span class="sxs-lookup"><span data-stu-id="d3840-144">The start date of recurrence.</span></span>

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

### <span data-ttu-id="d3840-145">-RecurrencePeriodTo</span><span class="sxs-lookup"><span data-stu-id="d3840-145">-RecurrencePeriodTo</span></span>
<span data-ttu-id="d3840-146">Data zakończenia cyklu.</span><span class="sxs-lookup"><span data-stu-id="d3840-146">The end date of recurrence.</span></span>

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

### <span data-ttu-id="d3840-147">-ScheduleRecurrence</span><span class="sxs-lookup"><span data-stu-id="d3840-147">-ScheduleRecurrence</span></span>
<span data-ttu-id="d3840-148">Cykl harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="d3840-148">The schedule recurrence.</span></span>

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

### <span data-ttu-id="d3840-149">-ScheduleStatus</span><span class="sxs-lookup"><span data-stu-id="d3840-149">-ScheduleStatus</span></span>
<span data-ttu-id="d3840-150">Stan harmonogramu eksportu.</span><span class="sxs-lookup"><span data-stu-id="d3840-150">The status of the export's schedule.</span></span>
<span data-ttu-id="d3840-151">Jeśli termin "Nieaktywny" jest wstrzymany, harmonogram eksportu zostanie wstrzymany.</span><span class="sxs-lookup"><span data-stu-id="d3840-151">If 'Inactive', the export's schedule is paused.</span></span>

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

### <span data-ttu-id="d3840-152">— Zakres</span><span class="sxs-lookup"><span data-stu-id="d3840-152">-Scope</span></span>
<span data-ttu-id="d3840-153">Ten parametr definiuje zakres zarządzania kosztami z różnych perspektyw: "Subskrypcja", "Grupa zasobów" i "Udostępnij usługę".</span><span class="sxs-lookup"><span data-stu-id="d3840-153">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3840-154">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="d3840-154">-TimePeriodFrom</span></span>
<span data-ttu-id="d3840-155">Data rozpoczęcia eksportu danych.</span><span class="sxs-lookup"><span data-stu-id="d3840-155">The start date for export data.</span></span>

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

### <span data-ttu-id="d3840-156">-TimePeriodTo</span><span class="sxs-lookup"><span data-stu-id="d3840-156">-TimePeriodTo</span></span>
<span data-ttu-id="d3840-157">Data zakończenia eksportu danych.</span><span class="sxs-lookup"><span data-stu-id="d3840-157">The end date for export data.</span></span>

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

### <span data-ttu-id="d3840-158">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d3840-158">-Confirm</span></span>
<span data-ttu-id="d3840-159">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d3840-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3840-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3840-160">-WhatIf</span></span>
<span data-ttu-id="d3840-161">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3840-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3840-162">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d3840-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3840-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3840-163">CommonParameters</span></span>
<span data-ttu-id="d3840-164">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3840-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3840-165">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d3840-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3840-166">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d3840-166">INPUTS</span></span>

## <span data-ttu-id="d3840-167">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d3840-167">OUTPUTS</span></span>

### <span data-ttu-id="d3840-168">Microsoft.Azure.PowerShell.cmdlet.costManagement.Models.Api20200601.IExport</span><span class="sxs-lookup"><span data-stu-id="d3840-168">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="d3840-169">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d3840-169">NOTES</span></span>

<span data-ttu-id="d3840-170">ALIASY</span><span class="sxs-lookup"><span data-stu-id="d3840-170">ALIASES</span></span>

## <span data-ttu-id="d3840-171">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d3840-171">RELATED LINKS</span></span>

