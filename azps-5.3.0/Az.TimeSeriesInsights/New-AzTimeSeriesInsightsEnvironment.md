---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: b4f27c31ebc3eb54727d6df1139409529c20eed9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98498190"
---
# <span data-ttu-id="741dd-101">New-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="741dd-101">New-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="741dd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="741dd-102">SYNOPSIS</span></span>
<span data-ttu-id="741dd-103">Utwórz środowisko w określonej grupie subskrypcji i zasobów.</span><span class="sxs-lookup"><span data-stu-id="741dd-103">Create an environment in the specified subscription and resource group.</span></span>

## <span data-ttu-id="741dd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="741dd-104">SYNTAX</span></span>

### <span data-ttu-id="741dd-105">Gen1 (domyślny)</span><span class="sxs-lookup"><span data-stu-id="741dd-105">Gen1 (Default)</span></span>
```
New-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> -Capacity <Int32>
 -DataRetentionTime <TimeSpan> -Kind <Kind> -Location <String> -Sku <SkuName> [-SubscriptionId <String>]
 [-PartitionKeyProperty <ITimeSeriesIdProperty[]>] [-StorageLimitExceededBehavior <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="741dd-106">Gen2</span><span class="sxs-lookup"><span data-stu-id="741dd-106">Gen2</span></span>
```
New-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> -Kind <Kind> -Location <String>
 -Sku <SkuName> -StorageAccountKey <SecureString> -StorageAccountName <String>
 -TimeSeriesIdProperty <ITimeSeriesIdProperty[]> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-WarmStoreDataRetentionTime <TimeSpan>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="741dd-107">Opis</span><span class="sxs-lookup"><span data-stu-id="741dd-107">DESCRIPTION</span></span>
<span data-ttu-id="741dd-108">Utwórz środowisko w określonej grupie subskrypcji i zasobów.</span><span class="sxs-lookup"><span data-stu-id="741dd-108">Create an environment in the specified subscription and resource group.</span></span>

## <span data-ttu-id="741dd-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="741dd-109">EXAMPLES</span></span>

### <span data-ttu-id="741dd-110">Przykład 1. Tworzenie środowiska informacji o serii czasu Gen1</span><span class="sxs-lookup"><span data-stu-id="741dd-110">Example 1: Create a Gen1 time series insights environment</span></span>
```powershell
PS C:\> $TimeSpan = New-TimeSpan -Days 1 -Hours 1 -Minutes 25
PS C:\> New-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001 -Kind Gen1 -Location eastus -Sku S1 -DataRetentionTime $TimeSpan -Capacity 2

Kind     Location Name       SkuCapacity SkuName Type
----     -------- ----       ----------- ------- ----
Gen1 eastus   tsitest001 2           S1      Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="741dd-111">To polecenie tworzy środowisko informacji o seriach czasu Gen1.</span><span class="sxs-lookup"><span data-stu-id="741dd-111">This command creates a Gen1 time series insights environment.</span></span>

### <span data-ttu-id="741dd-112">Przykład 2: Tworzenie środowiska szczegółowego dotyczącego serii godzin Gen2</span><span class="sxs-lookup"><span data-stu-id="741dd-112">Example 2: Create a Gen2 time series insights environment</span></span>
```powershell
PS C:\> $ks = Get-AzStorageAccountKey -ResourceGroupName "testgroup" -Name "staccount001"
PS C:\> $k  = $ks[0].Value | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest002 -Kind Gen2 -Location eastus -Sku L1 -StorageAccountName staccount001 -StorageAccountKey $k -TimeSeriesIdProperty @{name='cdc';type='string'}

Kind     Location Name       SkuCapacity SkuName Type
----     -------- ----       ----------- ------- ----
Gen2 eastus   tsitest002 1           L1      Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="741dd-113">To polecenie tworzy środowisko informacji o seriach czasu Gen2.</span><span class="sxs-lookup"><span data-stu-id="741dd-113">This command creates a Gen2 time series insights environment.</span></span>

## <span data-ttu-id="741dd-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="741dd-114">PARAMETERS</span></span>

### <span data-ttu-id="741dd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="741dd-115">-AsJob</span></span>
<span data-ttu-id="741dd-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="741dd-116">Run the command as a job</span></span>

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

### <span data-ttu-id="741dd-117">-Pojemność</span><span class="sxs-lookup"><span data-stu-id="741dd-117">-Capacity</span></span>
<span data-ttu-id="741dd-118">Pojemność jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="741dd-118">The capacity of the sku.</span></span>
<span data-ttu-id="741dd-119">W przypadku środowisk Gen1 wartość tę można zmienić w celu obsługi skalowania poza środowiskami po ich utworzeniu.</span><span class="sxs-lookup"><span data-stu-id="741dd-119">For Gen1 environments, this value can be changed to support scale out of environments after they have been created.</span></span>

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

### <span data-ttu-id="741dd-120">-DataRetentionTime</span><span class="sxs-lookup"><span data-stu-id="741dd-120">-DataRetentionTime</span></span>
<span data-ttu-id="741dd-121">Czas przechowywania danych.</span><span class="sxs-lookup"><span data-stu-id="741dd-121">The data retention time.</span></span>

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

### <span data-ttu-id="741dd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="741dd-122">-DefaultProfile</span></span>
<span data-ttu-id="741dd-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="741dd-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="741dd-124">-Kind</span><span class="sxs-lookup"><span data-stu-id="741dd-124">-Kind</span></span>
<span data-ttu-id="741dd-125">Rodzaj środowiska.</span><span class="sxs-lookup"><span data-stu-id="741dd-125">The kind of the environment.</span></span>

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

### <span data-ttu-id="741dd-126">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="741dd-126">-Location</span></span>
<span data-ttu-id="741dd-127">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="741dd-127">The location of the resource.</span></span>

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

### <span data-ttu-id="741dd-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="741dd-128">-Name</span></span>
<span data-ttu-id="741dd-129">Nazwa środowiska</span><span class="sxs-lookup"><span data-stu-id="741dd-129">Name of the environment</span></span>

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

### <span data-ttu-id="741dd-130">-Nowait</span><span class="sxs-lookup"><span data-stu-id="741dd-130">-NoWait</span></span>
<span data-ttu-id="741dd-131">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="741dd-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="741dd-132">-PartitionKeyProperty</span><span class="sxs-lookup"><span data-stu-id="741dd-132">-PartitionKeyProperty</span></span>
<span data-ttu-id="741dd-133">Lista właściwości zdarzeń, które będą używane do dzielenia danych w środowisku.</span><span class="sxs-lookup"><span data-stu-id="741dd-133">The list of event properties which will be used to partition data in the environment.</span></span>
<span data-ttu-id="741dd-134">Aby skonstruować, zobacz sekcję notatki dla właściwości PARTITIONKEYPROPERTY i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="741dd-134">To construct, see NOTES section for PARTITIONKEYPROPERTY properties and create a hash table.</span></span>

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

### <span data-ttu-id="741dd-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="741dd-135">-ResourceGroupName</span></span>
<span data-ttu-id="741dd-136">Nazwa grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="741dd-136">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="741dd-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="741dd-137">-Sku</span></span>
<span data-ttu-id="741dd-138">Nazwa tej jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="741dd-138">The name of this SKU.</span></span>

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

### <span data-ttu-id="741dd-139">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="741dd-139">-StorageAccountKey</span></span>
<span data-ttu-id="741dd-140">Wartość klucza zarządzania zapewniającego dostęp usługi gromadzenia danych w ramach szeregu czasowego do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="741dd-140">The value of the management key that grants the Time Series Insights service write access to the storage account.</span></span>

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

### <span data-ttu-id="741dd-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="741dd-141">-StorageAccountName</span></span>
<span data-ttu-id="741dd-142">Nazwa konta magazynu, które będzie zawierać dane o długim czasie długoterminowym środowiska.</span><span class="sxs-lookup"><span data-stu-id="741dd-142">The name of the storage account that will hold the environment's long term data.</span></span>

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

### <span data-ttu-id="741dd-143">-StorageLimitExceededBehavior</span><span class="sxs-lookup"><span data-stu-id="741dd-143">-StorageLimitExceededBehavior</span></span>
<span data-ttu-id="741dd-144">Zachowanie w przypadku przekroczenia pojemności środowiska usługa informacji o serii czasowej powinna trwać</span><span class="sxs-lookup"><span data-stu-id="741dd-144">The behavior the Time Series Insights service should take when the environment's capacity has been exceeded</span></span>

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

### <span data-ttu-id="741dd-145">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="741dd-145">-SubscriptionId</span></span>
<span data-ttu-id="741dd-146">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="741dd-146">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="741dd-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="741dd-147">-Tag</span></span>
<span data-ttu-id="741dd-148">Pary klucz-wartość dodatkowych właściwości zasobu.</span><span class="sxs-lookup"><span data-stu-id="741dd-148">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="741dd-149">-TimeSeriesIdProperty</span><span class="sxs-lookup"><span data-stu-id="741dd-149">-TimeSeriesIdProperty</span></span>
<span data-ttu-id="741dd-150">Lista właściwości zdarzeń, które zostaną użyte do zdefiniowania identyfikatora szeregu czasowego środowiska. Aby skonstruować, zobacz sekcję notatki dla właściwości TIMESERIESIDPROPERTY i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="741dd-150">The list of event properties which will be used to define the environment's time series id. To construct, see NOTES section for TIMESERIESIDPROPERTY properties and create a hash table.</span></span>

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

### <span data-ttu-id="741dd-151">-WarmStoreDataRetentionTime</span><span class="sxs-lookup"><span data-stu-id="741dd-151">-WarmStoreDataRetentionTime</span></span>
<span data-ttu-id="741dd-152">ISO8601 TimeSpan określający liczbę dni, przez które zdarzenia środowiska będą dostępne w kwerendach w sklepie ciepłym.</span><span class="sxs-lookup"><span data-stu-id="741dd-152">ISO8601 timespan specifying the number of days the environment's events will be available for query from the warm store.</span></span>

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

### <span data-ttu-id="741dd-153">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="741dd-153">-Confirm</span></span>
<span data-ttu-id="741dd-154">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="741dd-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="741dd-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="741dd-155">-WhatIf</span></span>
<span data-ttu-id="741dd-156">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="741dd-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="741dd-157">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="741dd-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="741dd-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="741dd-158">CommonParameters</span></span>
<span data-ttu-id="741dd-159">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="741dd-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="741dd-160">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="741dd-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="741dd-161">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="741dd-161">INPUTS</span></span>

## <span data-ttu-id="741dd-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="741dd-162">OUTPUTS</span></span>

### <span data-ttu-id="741dd-163">Microsoft. Azure. PowerShell. polecenia. TimeSeriesInsights. models. Api20200515. IEnvironmentResource</span><span class="sxs-lookup"><span data-stu-id="741dd-163">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="741dd-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="741dd-164">NOTES</span></span>

<span data-ttu-id="741dd-165">PISUJE</span><span class="sxs-lookup"><span data-stu-id="741dd-165">ALIASES</span></span>

<span data-ttu-id="741dd-166">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="741dd-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="741dd-167">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="741dd-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="741dd-168">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="741dd-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="741dd-169">PARTITIONKEYPROPERTY <ITimeSeriesIdProperty [] >: Lista właściwości zdarzeń, które będą używane do dzielenia danych w środowisku.</span><span class="sxs-lookup"><span data-stu-id="741dd-169">PARTITIONKEYPROPERTY <ITimeSeriesIdProperty[]>: The list of event properties which will be used to partition data in the environment.</span></span>
  - <span data-ttu-id="741dd-170">`[Name <String>]`: Nazwa właściwości.</span><span class="sxs-lookup"><span data-stu-id="741dd-170">`[Name <String>]`: The name of the property.</span></span>
  - <span data-ttu-id="741dd-171">`[Type <PropertyType?>]`: Typ właściwości.</span><span class="sxs-lookup"><span data-stu-id="741dd-171">`[Type <PropertyType?>]`: The type of the property.</span></span>

<span data-ttu-id="741dd-172">TIMESERIESIDPROPERTY <ITimeSeriesIdProperty [] >: Lista właściwości zdarzeń, które zostaną użyte do zdefiniowania identyfikatora serii czasu dla środowiska.</span><span class="sxs-lookup"><span data-stu-id="741dd-172">TIMESERIESIDPROPERTY <ITimeSeriesIdProperty[]>: The list of event properties which will be used to define the environment's time series id.</span></span>
  - <span data-ttu-id="741dd-173">`[Name <String>]`: Nazwa właściwości.</span><span class="sxs-lookup"><span data-stu-id="741dd-173">`[Name <String>]`: The name of the property.</span></span>
  - <span data-ttu-id="741dd-174">`[Type <PropertyType?>]`: Typ właściwości.</span><span class="sxs-lookup"><span data-stu-id="741dd-174">`[Type <PropertyType?>]`: The type of the property.</span></span>

## <span data-ttu-id="741dd-175">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="741dd-175">RELATED LINKS</span></span>

