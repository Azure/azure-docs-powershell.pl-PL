---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: f4f42b257c5ce54085214c8cd9d2f79d9e8a6387
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241627"
---
# <span data-ttu-id="6b8ae-101">Get-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="6b8ae-101">Get-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="6b8ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b8ae-102">SYNOPSIS</span></span>
<span data-ttu-id="6b8ae-103">Pobiera środowisko o określonej nazwie w określonej grupie subskrypcji i zasobów.</span><span class="sxs-lookup"><span data-stu-id="6b8ae-103">Gets the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="6b8ae-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6b8ae-104">SYNTAX</span></span>

### <span data-ttu-id="6b8ae-105">Lista1 (domyślna)</span><span class="sxs-lookup"><span data-stu-id="6b8ae-105">List1 (Default)</span></span>
```
Get-AzTimeSeriesInsightsEnvironment [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="6b8ae-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="6b8ae-106">Get</span></span>
```
Get-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6b8ae-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6b8ae-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-Expand <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6b8ae-108">Lista</span><span class="sxs-lookup"><span data-stu-id="6b8ae-108">List</span></span>
```
Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="6b8ae-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="6b8ae-109">DESCRIPTION</span></span>
<span data-ttu-id="6b8ae-110">Pobiera środowisko o określonej nazwie w określonej grupie subskrypcji i zasobów.</span><span class="sxs-lookup"><span data-stu-id="6b8ae-110">Gets the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="6b8ae-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6b8ae-111">EXAMPLES</span></span>

### <span data-ttu-id="6b8ae-112">Przykład 1. Uzyskiwanie środowiska szczegółowych informacji z serii czasowej</span><span class="sxs-lookup"><span data-stu-id="6b8ae-112">Example 1: Get a time series insights environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001

DataAccessFqdn               : b6d113a4-0865-405f-b09e-ad4355b5d046.env.timeseries.azure.com
DataAccessId                 : b6d113a4-0865-405f-b09e-ad4355b5d046
DataRetentionTime            : 1.01:25:00
Id                           : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest 
                               001
IngressState                 :
Kind                         : Gen1
Location                     : eastus
Name                         : tsitest001
PartitionKeyProperty         :
PropertyUsageState           :
Sku                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                  : 2
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="6b8ae-113">To polecenie pobiera środowisko szczegółowych informacji z serii czasu.</span><span class="sxs-lookup"><span data-stu-id="6b8ae-113">This command gets a time series insights environment.</span></span>

### <span data-ttu-id="6b8ae-114">Przykład 2. Lista środowisk szczegółowych informacji z serii czasowej</span><span class="sxs-lookup"><span data-stu-id="6b8ae-114">Example 2: List all time series insights environments</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup

DataAccessFqdn                      : 3de1d1e1-4f9b-4bc6-aad3-a835597dcd86.env.timeseries.azure.com
DataAccessId                        : 3de1d1e1-4f9b-4bc6-aad3-a835597dcd86
Id                                  : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/ 
                                      tsill
IngressState                        :
Kind                                : Gen2
Location                            : EastUs
Name                                : tsill
PropertyUsageState                  :
Sku                                 : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                         : 1
SkuName                             : L1
StateDetailCode                     :
StateDetailCurrentCount             :
StateDetailMaxCount                 :
StateDetailMessage                  :
StorageConfigurationAccountName     : cdolauli
Tag                                 : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimeSeriesIdProperty                : {ccc}
Type                                : Microsoft.TimeSeriesInsights/Environments
WarmStoreConfigurationDataRetention : 00:00:00

DataAccessFqdn               : b6d113a4-0865-405f-b09e-ad4355b5d046.env.timeseries.azure.com
DataAccessId                 : b6d113a4-0865-405f-b09e-ad4355b5d046
DataRetentionTime            : 1.01:25:00
Id                           : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest 
                               001
IngressState                 :
Kind                         : Gen1
Location                     : eastus
Name                         : tsitest001
PartitionKeyProperty         :
PropertyUsageState           :
Sku                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                  : 2
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="6b8ae-115">To polecenie zawiera listę wszystkich środowisk szczegółowych informacji szeregu czasowego w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="6b8ae-115">This command lists all time series insights environments in a resource group.</span></span>

### <span data-ttu-id="6b8ae-116">Przykład 3. Uzyskiwanie środowiska szczegółowych informacji z serii czasowej według obiektów</span><span class="sxs-lookup"><span data-stu-id="6b8ae-116">Example 3: Get a time series insights environment by object</span></span>
```powershell
PS C:\> $env = Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName tsi-test-i01k5l -Name tsi-envv8u56x 
PS C:\> Get-AzTimeSeriesInsightsEnvironment -InputObject $env

DataAccessFqdn               : d76a61f2-8a30-41a5-9587-f241eb9b48d9.env.timeseries.azure.com
DataAccessId                 : d76a61f2-8a30-41a5-9587-f241eb9b48d9
DataRetentionTime            : 1.01:25:00
Id                           : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/tsi-test-i01k5l/providers/Microsoft.TimeSeriesInsights/environments/tsi-envv8u56x
IngressState                 :
Kind                         : Gen1
Location                     : eastus2
Name                         : tsi-envv8u56x
PartitionKeyProperty         :
PropertyUsageState           :
Sku                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                  : 1
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="6b8ae-117">To polecenie pobiera środowiska analizy serii czasowej.</span><span class="sxs-lookup"><span data-stu-id="6b8ae-117">This command gets a time series insights environments.</span></span>

## <span data-ttu-id="6b8ae-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b8ae-118">PARAMETERS</span></span>

### <span data-ttu-id="6b8ae-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b8ae-119">-DefaultProfile</span></span>
<span data-ttu-id="6b8ae-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6b8ae-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b8ae-121">— Rozwiń</span><span class="sxs-lookup"><span data-stu-id="6b8ae-121">-Expand</span></span>
<span data-ttu-id="6b8ae-122">Ustawienie $expand=stan będzie uwzględniać stan usług wewnętrznych środowiska w usłudze Time Series Insights.</span><span class="sxs-lookup"><span data-stu-id="6b8ae-122">Setting $expand=status will include the status of the internal services of the environment in the Time Series Insights service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b8ae-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b8ae-123">-InputObject</span></span>
<span data-ttu-id="6b8ae-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="6b8ae-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b8ae-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6b8ae-125">-Name</span></span>
<span data-ttu-id="6b8ae-126">Nazwa środowiska szczegółowych informacji szeregu czasowego skojarzonego z określoną grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="6b8ae-126">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b8ae-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b8ae-127">-ResourceGroupName</span></span>
<span data-ttu-id="6b8ae-128">Nazwa grupy usługi Azure Resource.</span><span class="sxs-lookup"><span data-stu-id="6b8ae-128">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="6b8ae-129">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6b8ae-129">-SubscriptionId</span></span>
<span data-ttu-id="6b8ae-130">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6b8ae-130">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b8ae-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b8ae-131">CommonParameters</span></span>
<span data-ttu-id="6b8ae-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b8ae-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b8ae-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6b8ae-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b8ae-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6b8ae-134">INPUTS</span></span>

### <span data-ttu-id="6b8ae-135">Microsoft.Azure.PowerShell.Cmdlet.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="6b8ae-135">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="6b8ae-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6b8ae-136">OUTPUTS</span></span>

### <span data-ttu-id="6b8ae-137">Microsoft.Azure.PowerShell.Cmdlet.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span><span class="sxs-lookup"><span data-stu-id="6b8ae-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="6b8ae-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6b8ae-138">NOTES</span></span>

<span data-ttu-id="6b8ae-139">ALIASY</span><span class="sxs-lookup"><span data-stu-id="6b8ae-139">ALIASES</span></span>

<span data-ttu-id="6b8ae-140">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="6b8ae-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6b8ae-141">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="6b8ae-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6b8ae-142">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6b8ae-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6b8ae-143">INPUTOBJECT: <ITimeSeriesInsightsIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="6b8ae-143">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6b8ae-144">`[AccessPolicyName <String>]`: nazwa zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="6b8ae-144">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="6b8ae-145">`[EnvironmentName <String>]`: nazwa środowiska</span><span class="sxs-lookup"><span data-stu-id="6b8ae-145">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="6b8ae-146">`[EventSourceName <String>]`: nazwa źródła zdarzeń Szczegółowych informacji szeregu czasowego skojarzonego z określonym środowiskiem.</span><span class="sxs-lookup"><span data-stu-id="6b8ae-146">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="6b8ae-147">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="6b8ae-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6b8ae-148">`[ReferenceDataSetName <String>]`: nazwa zestawu danych odwołania.</span><span class="sxs-lookup"><span data-stu-id="6b8ae-148">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="6b8ae-149">`[ResourceGroupName <String>]`: nazwa grupy usługi Azure Resource.</span><span class="sxs-lookup"><span data-stu-id="6b8ae-149">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="6b8ae-150">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6b8ae-150">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="6b8ae-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6b8ae-151">RELATED LINKS</span></span>

