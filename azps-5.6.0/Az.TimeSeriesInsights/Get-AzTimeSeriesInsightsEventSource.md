---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: c28d33e4da860a68227228564c55a151a3068329
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977617"
---
# <span data-ttu-id="56b09-101">Get-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="56b09-101">Get-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="56b09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56b09-102">SYNOPSIS</span></span>
<span data-ttu-id="56b09-103">Pobiera źródło zdarzeń o określonej nazwie w określonym środowisku.</span><span class="sxs-lookup"><span data-stu-id="56b09-103">Gets the event source with the specified name in the specified environment.</span></span>

## <span data-ttu-id="56b09-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="56b09-104">SYNTAX</span></span>

### <span data-ttu-id="56b09-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="56b09-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="56b09-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="56b09-106">Get</span></span>
```
Get-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="56b09-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="56b09-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="56b09-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="56b09-108">DESCRIPTION</span></span>
<span data-ttu-id="56b09-109">Pobiera źródło zdarzeń o określonej nazwie w określonym środowisku.</span><span class="sxs-lookup"><span data-stu-id="56b09-109">Gets the event source with the specified name in the specified environment.</span></span>

## <span data-ttu-id="56b09-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="56b09-110">EXAMPLES</span></span>

### <span data-ttu-id="56b09-111">Przykład 1. Lista wszystkich źródeł zdarzeń w określonym środowisku</span><span class="sxs-lookup"><span data-stu-id="56b09-111">Example 1: List all event sources under the specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -EnvironmentName tsitest001

ConsumerGroupName     : testgroup2
EventHubName          : hubname001
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.EventHub/namespaces/spacename001/eventhubs/hu 
                        bname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eve 
                        ntsources/estest001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.EventHub
Location              : eastus
Name                  : estest001
ServiceBusNamespace   : spacename001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources

ConsumerGroupName     : testgroup2
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.Devices/IotHubs/iotname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eve 
                        ntsources/iots001
IotHubName            : iotname001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.IoTHub
Location              : eastus
Name                  : iots001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="56b09-112">To polecenie wyświetla listę wszystkich źródeł zdarzeń w określonych środowiskach.</span><span class="sxs-lookup"><span data-stu-id="56b09-112">This command lists all event sources under the specified environments.</span></span>

### <span data-ttu-id="56b09-113">Przykład 2. Uzyskiwanie określonego źródła zdarzeń według nazwy</span><span class="sxs-lookup"><span data-stu-id="56b09-113">Example 2: Get a specified event source by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -EnvironmentName tsitest001 -Name iots001

ConsumerGroupName     : testgroup2
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.Devices/IotHubs/iotname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eve
                        ntsources/iots001
IotHubName            : iotname001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.IoTHub
Location              : eastus
Name                  : iots001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="56b09-114">To polecenie pobiera określone źródło zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="56b09-114">This command gets a specific event source.</span></span>

### <span data-ttu-id="56b09-115">Przykład 3. Uzyskiwanie określonego źródła zdarzeń według obiektu</span><span class="sxs-lookup"><span data-stu-id="56b09-115">Example 3: Get a specified event source by object</span></span>
```powershell
PS C:\> $es = Get-AzTimeSeriesInsightsEventSource -ResourceGroupName tsi-test-i01k5l -EnvironmentName tsi-envv8u56x -Name tsi-esrfyi9h
PS C:\> Get-AzTimeSeriesInsightsEventSource -InputObject $es

ConsumerGroupName     : tsi-test-i01k5l
EventHubName          : eventhubname-d2rvmp
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/tsi-test-i01k5l/providers/Microsoft.EventHub/namespaces/eventhubspace-0t3khp/eventhubs/eventhubname-d2rvmp
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/tsi-test-i01k5l/providers/Microsoft.TimeSeriesInsights/environments/tsi-envv8u56x/eventsources/tsi-esrfyi9h
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.EventHub
Location              : eastus2
Name                  : tsi-esrfyi9h
ServiceBusNamespace   : eventhubspace-0t3khp
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="56b09-116">To polecenie pobiera określone źródło zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="56b09-116">This command gets a specific event source.</span></span>

## <span data-ttu-id="56b09-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56b09-117">PARAMETERS</span></span>

### <span data-ttu-id="56b09-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56b09-118">-DefaultProfile</span></span>
<span data-ttu-id="56b09-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="56b09-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56b09-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="56b09-120">-EnvironmentName</span></span>
<span data-ttu-id="56b09-121">Nazwa środowiska szczegółowych informacji szeregu czasowego skojarzonego z określoną grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="56b09-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="56b09-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56b09-122">-InputObject</span></span>
<span data-ttu-id="56b09-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="56b09-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="56b09-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="56b09-124">-Name</span></span>
<span data-ttu-id="56b09-125">Nazwa źródła zdarzeń Szczegółowe informacje o seriach czasu skojarzonych z określonym środowiskiem.</span><span class="sxs-lookup"><span data-stu-id="56b09-125">The name of the Time Series Insights event source associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: EventSourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56b09-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56b09-126">-ResourceGroupName</span></span>
<span data-ttu-id="56b09-127">Nazwa grupy usługi Azure Resource.</span><span class="sxs-lookup"><span data-stu-id="56b09-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="56b09-128">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="56b09-128">-SubscriptionId</span></span>
<span data-ttu-id="56b09-129">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="56b09-129">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56b09-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56b09-130">CommonParameters</span></span>
<span data-ttu-id="56b09-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56b09-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56b09-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56b09-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56b09-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56b09-133">INPUTS</span></span>

### <span data-ttu-id="56b09-134">Microsoft.Azure.PowerShell.Cmdlet.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="56b09-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="56b09-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56b09-135">OUTPUTS</span></span>

### <span data-ttu-id="56b09-136">Microsoft.Azure.PowerShell.Cmdlet.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span><span class="sxs-lookup"><span data-stu-id="56b09-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="56b09-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="56b09-137">NOTES</span></span>

<span data-ttu-id="56b09-138">ALIASY</span><span class="sxs-lookup"><span data-stu-id="56b09-138">ALIASES</span></span>

<span data-ttu-id="56b09-139">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="56b09-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="56b09-140">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="56b09-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="56b09-141">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="56b09-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="56b09-142">INPUTOBJECT: <ITimeSeriesInsightsIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="56b09-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="56b09-143">`[AccessPolicyName <String>]`: nazwa zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="56b09-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="56b09-144">`[EnvironmentName <String>]`: nazwa środowiska</span><span class="sxs-lookup"><span data-stu-id="56b09-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="56b09-145">`[EventSourceName <String>]`: nazwa źródła zdarzeń Szczegółowych informacji szeregu czasowego skojarzonego z określonym środowiskiem.</span><span class="sxs-lookup"><span data-stu-id="56b09-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="56b09-146">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="56b09-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="56b09-147">`[ReferenceDataSetName <String>]`: nazwa zestawu danych referencyjnych.</span><span class="sxs-lookup"><span data-stu-id="56b09-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="56b09-148">`[ResourceGroupName <String>]`: nazwa grupy azure resource.</span><span class="sxs-lookup"><span data-stu-id="56b09-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="56b09-149">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="56b09-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="56b09-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="56b09-150">RELATED LINKS</span></span>

