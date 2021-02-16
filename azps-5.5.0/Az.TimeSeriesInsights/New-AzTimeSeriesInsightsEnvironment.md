---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: b4f27c31ebc3eb54727d6df1139409529c20eed9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243010"
---
# <span data-ttu-id="3b41e-101">New-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="3b41e-101">New-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="3b41e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b41e-102">SYNOPSIS</span></span>
<span data-ttu-id="3b41e-103">Tworzenie środowiska w określonej grupie subskrypcji i zasobów.</span><span class="sxs-lookup"><span data-stu-id="3b41e-103">Create an environment in the specified subscription and resource group.</span></span>

## <span data-ttu-id="3b41e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3b41e-104">SYNTAX</span></span>

### <span data-ttu-id="3b41e-105">Gen1 (domyślne)</span><span class="sxs-lookup"><span data-stu-id="3b41e-105">Gen1 (Default)</span></span>
```
New-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> -Capacity <Int32>
 -DataRetentionTime <TimeSpan> -Kind <Kind> -Location <String> -Sku <SkuName> [-SubscriptionId <String>]
 [-PartitionKeyProperty <ITimeSeriesIdProperty[]>] [-StorageLimitExceededBehavior <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3b41e-106">Gen2</span><span class="sxs-lookup"><span data-stu-id="3b41e-106">Gen2</span></span>
```
New-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> -Kind <Kind> -Location <String>
 -Sku <SkuName> -StorageAccountKey <SecureString> -StorageAccountName <String>
 -TimeSeriesIdProperty <ITimeSeriesIdProperty[]> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-WarmStoreDataRetentionTime <TimeSpan>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="3b41e-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="3b41e-107">DESCRIPTION</span></span>
<span data-ttu-id="3b41e-108">Tworzenie środowiska w określonej grupie subskrypcji i zasobów.</span><span class="sxs-lookup"><span data-stu-id="3b41e-108">Create an environment in the specified subscription and resource group.</span></span>

## <span data-ttu-id="3b41e-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3b41e-109">EXAMPLES</span></span>

### <span data-ttu-id="3b41e-110">Przykład 1. Tworzenie środowiska szczegółowych informacji z serii czasowej generacji 1</span><span class="sxs-lookup"><span data-stu-id="3b41e-110">Example 1: Create a Gen1 time series insights environment</span></span>
```powershell
PS C:\> $TimeSpan = New-TimeSpan -Days 1 -Hours 1 -Minutes 25
PS C:\> New-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001 -Kind Gen1 -Location eastus -Sku S1 -DataRetentionTime $TimeSpan -Capacity 2

Kind     Location Name       SkuCapacity SkuName Type
----     -------- ----       ----------- ------- ----
Gen1 eastus   tsitest001 2           S1      Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="3b41e-111">To polecenie tworzy środowisko szczegółowych informacji szeregu czasowego generacji 1.</span><span class="sxs-lookup"><span data-stu-id="3b41e-111">This command creates a Gen1 time series insights environment.</span></span>

### <span data-ttu-id="3b41e-112">Przykład 2. Tworzenie środowiska szczegółowych informacji z serii czasowej gen2</span><span class="sxs-lookup"><span data-stu-id="3b41e-112">Example 2: Create a Gen2 time series insights environment</span></span>
```powershell
PS C:\> $ks = Get-AzStorageAccountKey -ResourceGroupName "testgroup" -Name "staccount001"
PS C:\> $k  = $ks[0].Value | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest002 -Kind Gen2 -Location eastus -Sku L1 -StorageAccountName staccount001 -StorageAccountKey $k -TimeSeriesIdProperty @{name='cdc';type='string'}

Kind     Location Name       SkuCapacity SkuName Type
----     -------- ----       ----------- ------- ----
Gen2 eastus   tsitest002 1           L1      Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="3b41e-113">To polecenie tworzy środowisko szczegółowych informacji szeregu czasowego gen2.</span><span class="sxs-lookup"><span data-stu-id="3b41e-113">This command creates a Gen2 time series insights environment.</span></span>

## <span data-ttu-id="3b41e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b41e-114">PARAMETERS</span></span>

### <span data-ttu-id="3b41e-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="3b41e-115">-AsJob</span></span>
<span data-ttu-id="3b41e-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="3b41e-116">Run the command as a job</span></span>

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

### <span data-ttu-id="3b41e-117">— Pojemność</span><span class="sxs-lookup"><span data-stu-id="3b41e-117">-Capacity</span></span>
<span data-ttu-id="3b41e-118">Pojemność tej sku.</span><span class="sxs-lookup"><span data-stu-id="3b41e-118">The capacity of the sku.</span></span>
<span data-ttu-id="3b41e-119">W środowiskach generacji 1 tę wartość można zmienić, aby obsługiwać skalowanie poza środowiska po ich utworzeniu.</span><span class="sxs-lookup"><span data-stu-id="3b41e-119">For Gen1 environments, this value can be changed to support scale out of environments after they have been created.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Gen1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b41e-120">-DataRetentionTime</span><span class="sxs-lookup"><span data-stu-id="3b41e-120">-DataRetentionTime</span></span>
<span data-ttu-id="3b41e-121">Czas przechowywania danych.</span><span class="sxs-lookup"><span data-stu-id="3b41e-121">The data retention time.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Gen1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b41e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b41e-122">-DefaultProfile</span></span>
<span data-ttu-id="3b41e-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3b41e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b41e-124">— Rodzaj</span><span class="sxs-lookup"><span data-stu-id="3b41e-124">-Kind</span></span>
<span data-ttu-id="3b41e-125">Rodzaj środowiska.</span><span class="sxs-lookup"><span data-stu-id="3b41e-125">The kind of the environment.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b41e-126">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3b41e-126">-Location</span></span>
<span data-ttu-id="3b41e-127">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="3b41e-127">The location of the resource.</span></span>

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

### <span data-ttu-id="3b41e-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3b41e-128">-Name</span></span>
<span data-ttu-id="3b41e-129">Nazwa środowiska</span><span class="sxs-lookup"><span data-stu-id="3b41e-129">Name of the environment</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b41e-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3b41e-130">-NoWait</span></span>
<span data-ttu-id="3b41e-131">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="3b41e-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3b41e-132">-PartitionKeyProperty</span><span class="sxs-lookup"><span data-stu-id="3b41e-132">-PartitionKeyProperty</span></span>
<span data-ttu-id="3b41e-133">Lista właściwości zdarzeń, które będą używane do partycjonowania danych w środowisku.</span><span class="sxs-lookup"><span data-stu-id="3b41e-133">The list of event properties which will be used to partition data in the environment.</span></span>
<span data-ttu-id="3b41e-134">Aby skonstruować, zobacz sekcję NOTES dla właściwości PARTITIONKEYPROPERTY i utwórz tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="3b41e-134">To construct, see NOTES section for PARTITIONKEYPROPERTY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.ITimeSeriesIdProperty[]
Parameter Sets: Gen1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b41e-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b41e-135">-ResourceGroupName</span></span>
<span data-ttu-id="3b41e-136">Nazwa grupy usługi Azure Resource.</span><span class="sxs-lookup"><span data-stu-id="3b41e-136">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="3b41e-137">- SKU</span><span class="sxs-lookup"><span data-stu-id="3b41e-137">-Sku</span></span>
<span data-ttu-id="3b41e-138">Nazwa tej sku.</span><span class="sxs-lookup"><span data-stu-id="3b41e-138">The name of this SKU.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.SkuName
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b41e-139">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="3b41e-139">-StorageAccountKey</span></span>
<span data-ttu-id="3b41e-140">Wartość klucza zarządzania, który udziela usłudze Time Series Insights dostępu do zapisu konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="3b41e-140">The value of the management key that grants the Time Series Insights service write access to the storage account.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: Gen2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b41e-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3b41e-141">-StorageAccountName</span></span>
<span data-ttu-id="3b41e-142">Nazwa konta magazynu, które będzie przechowywać dane środowiska przez dłuższy czas.</span><span class="sxs-lookup"><span data-stu-id="3b41e-142">The name of the storage account that will hold the environment's long term data.</span></span>

```yaml
Type: System.String
Parameter Sets: Gen2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b41e-143">-StorageLimitExceededBehavior</span><span class="sxs-lookup"><span data-stu-id="3b41e-143">-StorageLimitExceededBehavior</span></span>
<span data-ttu-id="3b41e-144">Działanie usługi Time Series Insights powinno zostać podjęcia w przypadku przekroczenia pojemności środowiska</span><span class="sxs-lookup"><span data-stu-id="3b41e-144">The behavior the Time Series Insights service should take when the environment's capacity has been exceeded</span></span>

```yaml
Type: System.String
Parameter Sets: Gen1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b41e-145">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3b41e-145">-SubscriptionId</span></span>
<span data-ttu-id="3b41e-146">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3b41e-146">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b41e-147">— Tag</span><span class="sxs-lookup"><span data-stu-id="3b41e-147">-Tag</span></span>
<span data-ttu-id="3b41e-148">Pary klucz-wartość dodatkowych właściwości zasobu.</span><span class="sxs-lookup"><span data-stu-id="3b41e-148">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="3b41e-149">-TimeSeriesIdProperty</span><span class="sxs-lookup"><span data-stu-id="3b41e-149">-TimeSeriesIdProperty</span></span>
<span data-ttu-id="3b41e-150">Lista właściwości zdarzeń, które będą używane do definiowania identyfikatora szeregu czasowego środowiska. Aby skonstruować, zobacz sekcję NOTATEK, aby uzyskać informacje o właściwościach TIMESERIESIDPROPERTY i utworzyć tabelę skrótów.</span><span class="sxs-lookup"><span data-stu-id="3b41e-150">The list of event properties which will be used to define the environment's time series id. To construct, see NOTES section for TIMESERIESIDPROPERTY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.ITimeSeriesIdProperty[]
Parameter Sets: Gen2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b41e-151">-WarmStoreDataRetentionTime</span><span class="sxs-lookup"><span data-stu-id="3b41e-151">-WarmStoreDataRetentionTime</span></span>
<span data-ttu-id="3b41e-152">Zakres czasu ISO8601 określający liczbę dni, przez które zdarzenia środowiska będą dostępne dla zapytania z ciepłego magazynu.</span><span class="sxs-lookup"><span data-stu-id="3b41e-152">ISO8601 timespan specifying the number of days the environment's events will be available for query from the warm store.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Gen2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b41e-153">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3b41e-153">-Confirm</span></span>
<span data-ttu-id="3b41e-154">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3b41e-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b41e-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b41e-155">-WhatIf</span></span>
<span data-ttu-id="3b41e-156">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b41e-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b41e-157">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3b41e-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b41e-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b41e-158">CommonParameters</span></span>
<span data-ttu-id="3b41e-159">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b41e-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b41e-160">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3b41e-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b41e-161">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3b41e-161">INPUTS</span></span>

## <span data-ttu-id="3b41e-162">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3b41e-162">OUTPUTS</span></span>

### <span data-ttu-id="3b41e-163">Microsoft.Azure.PowerShell.Cmdlet.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span><span class="sxs-lookup"><span data-stu-id="3b41e-163">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="3b41e-164">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3b41e-164">NOTES</span></span>

<span data-ttu-id="3b41e-165">ALIASY</span><span class="sxs-lookup"><span data-stu-id="3b41e-165">ALIASES</span></span>

<span data-ttu-id="3b41e-166">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3b41e-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3b41e-167">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="3b41e-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3b41e-168">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3b41e-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3b41e-169">PARTITIONKEYPROPERTY <ITimeSeriesIdProperty[]>: Lista właściwości zdarzeń, które będą używane do partycjonowania danych w środowisku.</span><span class="sxs-lookup"><span data-stu-id="3b41e-169">PARTITIONKEYPROPERTY <ITimeSeriesIdProperty[]>: The list of event properties which will be used to partition data in the environment.</span></span>
  - <span data-ttu-id="3b41e-170">`[Name <String>]`: nazwa właściwości.</span><span class="sxs-lookup"><span data-stu-id="3b41e-170">`[Name <String>]`: The name of the property.</span></span>
  - <span data-ttu-id="3b41e-171">`[Type <PropertyType?>]`: typ właściwości.</span><span class="sxs-lookup"><span data-stu-id="3b41e-171">`[Type <PropertyType?>]`: The type of the property.</span></span>

<span data-ttu-id="3b41e-172">TIMESERIESIDPROPERTY <ITimeSeriesIdProperty[]>: Lista właściwości zdarzeń, które będą używane do definiowania identyfikatora serii czasowej środowiska.</span><span class="sxs-lookup"><span data-stu-id="3b41e-172">TIMESERIESIDPROPERTY <ITimeSeriesIdProperty[]>: The list of event properties which will be used to define the environment's time series id.</span></span>
  - <span data-ttu-id="3b41e-173">`[Name <String>]`: nazwa właściwości.</span><span class="sxs-lookup"><span data-stu-id="3b41e-173">`[Name <String>]`: The name of the property.</span></span>
  - <span data-ttu-id="3b41e-174">`[Type <PropertyType?>]`: typ właściwości.</span><span class="sxs-lookup"><span data-stu-id="3b41e-174">`[Type <PropertyType?>]`: The type of the property.</span></span>

## <span data-ttu-id="3b41e-175">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3b41e-175">RELATED LINKS</span></span>

