---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: f4f42b257c5ce54085214c8cd9d2f79d9e8a6387
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223639"
---
# <span data-ttu-id="5ce86-101">Get-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="5ce86-101">Get-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="5ce86-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5ce86-102">SYNOPSIS</span></span>
<span data-ttu-id="5ce86-103">Pobiera środowisko o określonej nazwie w podanej subskrypcji i grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="5ce86-103">Gets the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="5ce86-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5ce86-104">SYNTAX</span></span>

### <span data-ttu-id="5ce86-105">List1 (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5ce86-105">List1 (Default)</span></span>
```
Get-AzTimeSeriesInsightsEnvironment [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="5ce86-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="5ce86-106">Get</span></span>
```
Get-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5ce86-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5ce86-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-Expand <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5ce86-108">Lista</span><span class="sxs-lookup"><span data-stu-id="5ce86-108">List</span></span>
```
Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5ce86-109">Opis</span><span class="sxs-lookup"><span data-stu-id="5ce86-109">DESCRIPTION</span></span>
<span data-ttu-id="5ce86-110">Pobiera środowisko o określonej nazwie w podanej subskrypcji i grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="5ce86-110">Gets the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="5ce86-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5ce86-111">EXAMPLES</span></span>

### <span data-ttu-id="5ce86-112">Przykład 1: uzyskiwanie środowiska szczegółowego dotyczącego informacji o seriach czasu</span><span class="sxs-lookup"><span data-stu-id="5ce86-112">Example 1: Get a time series insights environment</span></span>
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

<span data-ttu-id="5ce86-113">To polecenie uzyskuje środowisko informacji o seriach czasowych.</span><span class="sxs-lookup"><span data-stu-id="5ce86-113">This command gets a time series insights environment.</span></span>

### <span data-ttu-id="5ce86-114">Przykład 2: wszystkie środowiska szczegółowe dotyczące serii godzin</span><span class="sxs-lookup"><span data-stu-id="5ce86-114">Example 2: List all time series insights environments</span></span>
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

<span data-ttu-id="5ce86-115">W tym poleceniu są wyświetlane wszystkie środowiska informacji o seriach czasu w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="5ce86-115">This command lists all time series insights environments in a resource group.</span></span>

### <span data-ttu-id="5ce86-116">Przykład 3: uzyskiwanie środowiska szczegółowych informacji o seriach czasu według obiektów</span><span class="sxs-lookup"><span data-stu-id="5ce86-116">Example 3: Get a time series insights environment by object</span></span>
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

<span data-ttu-id="5ce86-117">To polecenie umożliwia uzyskiwanie środowisk dotyczących informacji o seriach czasowych.</span><span class="sxs-lookup"><span data-stu-id="5ce86-117">This command gets a time series insights environments.</span></span>

## <span data-ttu-id="5ce86-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5ce86-118">PARAMETERS</span></span>

### <span data-ttu-id="5ce86-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ce86-119">-DefaultProfile</span></span>
<span data-ttu-id="5ce86-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5ce86-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ce86-121">-Expand</span><span class="sxs-lookup"><span data-stu-id="5ce86-121">-Expand</span></span>
<span data-ttu-id="5ce86-122">Ustawienie $expand = status będzie obejmować stan usług wewnętrznych środowiska w usłudze informacji o seriach czasu.</span><span class="sxs-lookup"><span data-stu-id="5ce86-122">Setting $expand=status will include the status of the internal services of the environment in the Time Series Insights service.</span></span>

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

### <span data-ttu-id="5ce86-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5ce86-123">-InputObject</span></span>
<span data-ttu-id="5ce86-124">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="5ce86-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5ce86-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5ce86-125">-Name</span></span>
<span data-ttu-id="5ce86-126">Nazwa środowiska informacji o serii czasowej skojarzonego z określoną grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="5ce86-126">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="5ce86-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ce86-127">-ResourceGroupName</span></span>
<span data-ttu-id="5ce86-128">Nazwa grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5ce86-128">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="5ce86-129">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="5ce86-129">-SubscriptionId</span></span>
<span data-ttu-id="5ce86-130">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5ce86-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="5ce86-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ce86-131">CommonParameters</span></span>
<span data-ttu-id="5ce86-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ce86-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ce86-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ce86-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ce86-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ce86-134">INPUTS</span></span>

### <span data-ttu-id="5ce86-135">Microsoft. Azure. PowerShell. polecenia. TimeSeriesInsights. models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="5ce86-135">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="5ce86-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5ce86-136">OUTPUTS</span></span>

### <span data-ttu-id="5ce86-137">Microsoft. Azure. PowerShell. polecenia. TimeSeriesInsights. models. Api20200515. IEnvironmentResource</span><span class="sxs-lookup"><span data-stu-id="5ce86-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="5ce86-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5ce86-138">NOTES</span></span>

<span data-ttu-id="5ce86-139">PISUJE</span><span class="sxs-lookup"><span data-stu-id="5ce86-139">ALIASES</span></span>

<span data-ttu-id="5ce86-140">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5ce86-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5ce86-141">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="5ce86-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5ce86-142">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5ce86-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5ce86-143">INPUTobject <ITimeSeriesInsightsIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="5ce86-143">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5ce86-144">`[AccessPolicyName <String>]`: Nazwa zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="5ce86-144">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="5ce86-145">`[EnvironmentName <String>]`: Nazwa środowiska</span><span class="sxs-lookup"><span data-stu-id="5ce86-145">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="5ce86-146">`[EventSourceName <String>]`: Nazwa źródła zdarzeń szczegółowych informacji o seriach czasowych skojarzonego z określonym środowiskiem.</span><span class="sxs-lookup"><span data-stu-id="5ce86-146">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="5ce86-147">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="5ce86-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5ce86-148">`[ReferenceDataSetName <String>]`: Nazwa zestawu danych referencyjnych.</span><span class="sxs-lookup"><span data-stu-id="5ce86-148">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="5ce86-149">`[ResourceGroupName <String>]`: Nazwa grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5ce86-149">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="5ce86-150">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5ce86-150">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="5ce86-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ce86-151">RELATED LINKS</span></span>

