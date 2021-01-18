---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/new-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementExport.md
ms.openlocfilehash: edc0475a9d4299e1bd7346ab441a78b09905d59c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503765"
---
# <span data-ttu-id="e9cc9-101">New-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="e9cc9-101">New-AzCostManagementExport</span></span>

## <span data-ttu-id="e9cc9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e9cc9-102">SYNOPSIS</span></span>
<span data-ttu-id="e9cc9-103">Operacja tworzenia lub aktualizowania eksportu.</span><span class="sxs-lookup"><span data-stu-id="e9cc9-103">The operation to create or update a export.</span></span>
<span data-ttu-id="e9cc9-104">Operacja aktualizacji wymaga, aby w żądaniu została ustawiona Najnowsza wersja elementu eTag.</span><span class="sxs-lookup"><span data-stu-id="e9cc9-104">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="e9cc9-105">Najnowszy element eTag można uzyskać, wykonując operację pobierania.</span><span class="sxs-lookup"><span data-stu-id="e9cc9-105">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="e9cc9-106">Operacja tworzenia nie wymaga elementu eTag.</span><span class="sxs-lookup"><span data-stu-id="e9cc9-106">Create operation does not require eTag.</span></span>

## <span data-ttu-id="e9cc9-107">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e9cc9-107">SYNTAX</span></span>

```
New-AzCostManagementExport -Name <String> -Scope <String> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e9cc9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e9cc9-108">DESCRIPTION</span></span>
<span data-ttu-id="e9cc9-109">Operacja tworzenia lub aktualizowania eksportu.</span><span class="sxs-lookup"><span data-stu-id="e9cc9-109">The operation to create or update a export.</span></span>
<span data-ttu-id="e9cc9-110">Operacja aktualizacji wymaga, aby w żądaniu została ustawiona Najnowsza wersja elementu eTag.</span><span class="sxs-lookup"><span data-stu-id="e9cc9-110">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="e9cc9-111">Najnowszy element eTag można uzyskać, wykonując operację pobierania.</span><span class="sxs-lookup"><span data-stu-id="e9cc9-111">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="e9cc9-112">Operacja tworzenia nie wymaga elementu eTag.</span><span class="sxs-lookup"><span data-stu-id="e9cc9-112">Create operation does not require eTag.</span></span>

## <span data-ttu-id="e9cc9-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e9cc9-113">EXAMPLES</span></span>

### <span data-ttu-id="e9cc9-114">Przykład 1. Tworzenie AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="e9cc9-114">Example 1: Create an AzCostManagementExport</span></span>
```powershell
PS C:\> New-AzCostManagementExport -Scope "subscriptions/***********" -Name "CostManagementExportTest" -ScheduleStatus "Active" -ScheduleRecurrence "Daily" -RecurrencePeriodFrom "2020-10-31T20:00:00Z" -RecurrencePeriodTo "2020-11-30T00:00:00Z" -Format "Csv" -DestinationResourceId "/subscriptions/*************/resourceGroups/ResourceGroupTest/providers/Microsoft.Storage/storageAccounts/storageAccountTest" `  -DestinationContainer "exports" -DestinationRootFolderPath "ad-hoc" -DefinitionType "Usage" -DefinitionTimeframe "MonthToDate" -DatasetGranularity "Daily"

ETag              Name                                      Type
----              ----                                      ----
"********" TestExportDatasetAggregationInfosagdhaghj Microsoft.CostManagement/exports
```

<span data-ttu-id="e9cc9-115">Tworzenie AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="e9cc9-115">Create an AzCostManagementExport</span></span>

## <span data-ttu-id="e9cc9-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e9cc9-116">PARAMETERS</span></span>

### <span data-ttu-id="e9cc9-117">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="e9cc9-117">-ConfigurationColumn</span></span>
<span data-ttu-id="e9cc9-118">Tablica nazw kolumn, które mają zostać uwzględnione w eksporcie.</span><span class="sxs-lookup"><span data-stu-id="e9cc9-118">Array of column names to be included in the export.</span></span>
<span data-ttu-id="e9cc9-119">Jeśli nie podano, wówczas eksport będzie obejmował wszystkie dostępne kolumny.</span><span class="sxs-lookup"><span data-stu-id="e9cc9-119">If not provided then the export will include all available columns.</span></span>
<span data-ttu-id="e9cc9-120">Dostępne kolumny mogą się różnić w zależności od kanału klienta (Zobacz przykłady).</span><span class="sxs-lookup"><span data-stu-id="e9cc9-120">The available columns can vary by customer channel (see examples).</span></span>

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

### <span data-ttu-id="e9cc9-121">-DataSetGranularity</span><span class="sxs-lookup"><span data-stu-id="e9cc9-121">-DataSetGranularity</span></span>
<span data-ttu-id="e9cc9-122">Stopień szczegółowości eksportu wierszy.</span><span class="sxs-lookup"><span data-stu-id="e9cc9-122">The granularity of rows in the export.</span></span>
<span data-ttu-id="e9cc9-123">Obecnie jest obsługiwana tylko codzienna.</span><span class="sxs-lookup"><span data-stu-id="e9cc9-123">Currently only 'Daily' is supported.</span></span>

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

### <span data-ttu-id="e9cc9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9cc9-124">-DefaultProfile</span></span>
<span data-ttu-id="e9cc9-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e9cc9-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9cc9-126">-DefinitionTimeframe</span><span class="sxs-lookup"><span data-stu-id="e9cc9-126">-DefinitionTimeframe</span></span>
<span data-ttu-id="e9cc9-127">Przedział czasu na ściąganie danych do eksportu.</span><span class="sxs-lookup"><span data-stu-id="e9cc9-127">The time frame for pulling data for the export.</span></span>
<span data-ttu-id="e9cc9-128">Jeśli jest niestandardowa, należy podać konkretny przedział czasu.</span><span class="sxs-lookup"><span data-stu-id="e9cc9-128">If custom, then a specific time period must be provided.</span></span>

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

### <span data-ttu-id="e9cc9-129">-Definitiontype</span><span class="sxs-lookup"><span data-stu-id="e9cc9-129">-DefinitionType</span></span>
<span data-ttu-id="e9cc9-130">Typ eksportu.</span><span class="sxs-lookup"><span data-stu-id="e9cc9-130">The type of the export.</span></span>
<span data-ttu-id="e9cc9-131">Należy zwrócić uwagę, że "użycie" odpowiada "ActualCost" i dotyczy eksportu, które jeszcze nie udostępniają danych opłat lub umorzenia na potrzeby rezerwacji usług.</span><span class="sxs-lookup"><span data-stu-id="e9cc9-131">Note that 'Usage' is equivalent to 'ActualCost' and is applicable to exports that do not yet provide data for charges or amortization for service reservations.</span></span>

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

### <span data-ttu-id="e9cc9-132">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="e9cc9-132">-DestinationContainer</span></span>
<span data-ttu-id="e9cc9-133">Nazwa kontenera, w którym zostanie przekazany wywóz.</span><span class="sxs-lookup"><span data-stu-id="e9cc9-133">The name of the container where exports will be uploaded.</span></span>

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

### <span data-ttu-id="e9cc9-134">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="e9cc9-134">-DestinationResourceId</span></span>
<span data-ttu-id="e9cc9-135">Identyfikator zasobu konta magazynu, w którym zostanie dostarczony eksport.</span><span class="sxs-lookup"><span data-stu-id="e9cc9-135">The resource id of the storage account where exports will be delivered.</span></span>

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

### <span data-ttu-id="e9cc9-136">-DestinationRootFolderPath</span><span class="sxs-lookup"><span data-stu-id="e9cc9-136">-DestinationRootFolderPath</span></span>
<span data-ttu-id="e9cc9-137">Nazwa katalogu, w którym będą przekazywane eksportowane.</span><span class="sxs-lookup"><span data-stu-id="e9cc9-137">The name of the directory where exports will be uploaded.</span></span>

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

### <span data-ttu-id="e9cc9-138">-Format</span><span class="sxs-lookup"><span data-stu-id="e9cc9-138">-Format</span></span>
<span data-ttu-id="e9cc9-139">Format dostarczanego eksportu.</span><span class="sxs-lookup"><span data-stu-id="e9cc9-139">The format of the export being delivered.</span></span>
<span data-ttu-id="e9cc9-140">Obecnie obsługiwane są tylko słowa "CSV".</span><span class="sxs-lookup"><span data-stu-id="e9cc9-140">Currently only 'Csv' is supported.</span></span>

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

### <span data-ttu-id="e9cc9-141">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e9cc9-141">-Name</span></span>
<span data-ttu-id="e9cc9-142">Eksportuj nazwę.</span><span class="sxs-lookup"><span data-stu-id="e9cc9-142">Export Name.</span></span>

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

### <span data-ttu-id="e9cc9-143">-RecurrencePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="e9cc9-143">-RecurrencePeriodFrom</span></span>
<span data-ttu-id="e9cc9-144">Data rozpoczęcia cyklu.</span><span class="sxs-lookup"><span data-stu-id="e9cc9-144">The start date of recurrence.</span></span>

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

### <span data-ttu-id="e9cc9-145">-RecurrencePeriodTo</span><span class="sxs-lookup"><span data-stu-id="e9cc9-145">-RecurrencePeriodTo</span></span>
<span data-ttu-id="e9cc9-146">Data zakończenia cyklu.</span><span class="sxs-lookup"><span data-stu-id="e9cc9-146">The end date of recurrence.</span></span>

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

### <span data-ttu-id="e9cc9-147">-ScheduleRecurrence</span><span class="sxs-lookup"><span data-stu-id="e9cc9-147">-ScheduleRecurrence</span></span>
<span data-ttu-id="e9cc9-148">Cykl planowania.</span><span class="sxs-lookup"><span data-stu-id="e9cc9-148">The schedule recurrence.</span></span>

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

### <span data-ttu-id="e9cc9-149">-ScheduleStatus</span><span class="sxs-lookup"><span data-stu-id="e9cc9-149">-ScheduleStatus</span></span>
<span data-ttu-id="e9cc9-150">Stan harmonogramu eksportu.</span><span class="sxs-lookup"><span data-stu-id="e9cc9-150">The status of the export's schedule.</span></span>
<span data-ttu-id="e9cc9-151">Jeśli nie jest aktywny, harmonogram eksportu jest wstrzymany.</span><span class="sxs-lookup"><span data-stu-id="e9cc9-151">If 'Inactive', the export's schedule is paused.</span></span>

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

### <span data-ttu-id="e9cc9-152">-Zakres</span><span class="sxs-lookup"><span data-stu-id="e9cc9-152">-Scope</span></span>
<span data-ttu-id="e9cc9-153">Ten parametr definiuje zakres costmanagement z różnych perspektyw "abonament", "Resources" i "świadczenie usługi".</span><span class="sxs-lookup"><span data-stu-id="e9cc9-153">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="e9cc9-154">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="e9cc9-154">-TimePeriodFrom</span></span>
<span data-ttu-id="e9cc9-155">Data rozpoczęcia eksportowania danych.</span><span class="sxs-lookup"><span data-stu-id="e9cc9-155">The start date for export data.</span></span>

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

### <span data-ttu-id="e9cc9-156">-TimePeriodTo</span><span class="sxs-lookup"><span data-stu-id="e9cc9-156">-TimePeriodTo</span></span>
<span data-ttu-id="e9cc9-157">Data zakończenia eksportowania danych.</span><span class="sxs-lookup"><span data-stu-id="e9cc9-157">The end date for export data.</span></span>

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

### <span data-ttu-id="e9cc9-158">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e9cc9-158">-Confirm</span></span>
<span data-ttu-id="e9cc9-159">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9cc9-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9cc9-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9cc9-160">-WhatIf</span></span>
<span data-ttu-id="e9cc9-161">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9cc9-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9cc9-162">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e9cc9-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9cc9-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9cc9-163">CommonParameters</span></span>
<span data-ttu-id="e9cc9-164">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9cc9-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9cc9-165">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e9cc9-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9cc9-166">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e9cc9-166">INPUTS</span></span>

## <span data-ttu-id="e9cc9-167">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e9cc9-167">OUTPUTS</span></span>

### <span data-ttu-id="e9cc9-168">Microsoft. Azure. PowerShell. polecenia. CostManagement. models. Api20200601. IExport</span><span class="sxs-lookup"><span data-stu-id="e9cc9-168">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="e9cc9-169">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e9cc9-169">NOTES</span></span>

<span data-ttu-id="e9cc9-170">PISUJE</span><span class="sxs-lookup"><span data-stu-id="e9cc9-170">ALIASES</span></span>

## <span data-ttu-id="e9cc9-171">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e9cc9-171">RELATED LINKS</span></span>

