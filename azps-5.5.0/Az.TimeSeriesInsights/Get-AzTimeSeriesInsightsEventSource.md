---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 5590a89b22c0adc3dfb2df88e6b977dec268a822
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198323"
---
# <span data-ttu-id="f5e35-101">Get-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="f5e35-101">Get-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="f5e35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5e35-102">SYNOPSIS</span></span>
<span data-ttu-id="f5e35-103">Pobiera źródło zdarzeń o określonej nazwie w określonym środowisku.</span><span class="sxs-lookup"><span data-stu-id="f5e35-103">Gets the event source with the specified name in the specified environment.</span></span>

## <span data-ttu-id="f5e35-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f5e35-104">SYNTAX</span></span>

### <span data-ttu-id="f5e35-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="f5e35-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f5e35-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="f5e35-106">Get</span></span>
```
Get-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f5e35-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f5e35-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="f5e35-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="f5e35-108">DESCRIPTION</span></span>
<span data-ttu-id="f5e35-109">Pobiera źródło zdarzeń o określonej nazwie w określonym środowisku.</span><span class="sxs-lookup"><span data-stu-id="f5e35-109">Gets the event source with the specified name in the specified environment.</span></span>

## <span data-ttu-id="f5e35-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f5e35-110">EXAMPLES</span></span>

### <span data-ttu-id="f5e35-111">Przykład 1. Lista wszystkich źródeł zdarzeń w określonym środowisku</span><span class="sxs-lookup"><span data-stu-id="f5e35-111">Example 1: List all event sources under the specified environment</span></span>
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

<span data-ttu-id="f5e35-112">To polecenie wyświetla listę wszystkich źródeł zdarzeń w określonych środowiskach.</span><span class="sxs-lookup"><span data-stu-id="f5e35-112">This command lists all event sources under the specified environments.</span></span>

### <span data-ttu-id="f5e35-113">Przykład 2. Uzyskiwanie określonego źródła zdarzeń według nazwy</span><span class="sxs-lookup"><span data-stu-id="f5e35-113">Example 2: Get a specified event source by name</span></span>
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

<span data-ttu-id="f5e35-114">To polecenie pobiera określone źródło zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="f5e35-114">This command gets a specific event source.</span></span>

### <span data-ttu-id="f5e35-115">Przykład 3. Uzyskiwanie określonego źródła zdarzeń według obiektu</span><span class="sxs-lookup"><span data-stu-id="f5e35-115">Example 3: Get a specified event source by object</span></span>
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

<span data-ttu-id="f5e35-116">To polecenie pobiera określone źródło zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="f5e35-116">This command gets a specific event source.</span></span>

## <span data-ttu-id="f5e35-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5e35-117">PARAMETERS</span></span>

### <span data-ttu-id="f5e35-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5e35-118">-DefaultProfile</span></span>
<span data-ttu-id="f5e35-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f5e35-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5e35-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="f5e35-120">-EnvironmentName</span></span>
<span data-ttu-id="f5e35-121">Nazwa środowiska szczegółowych informacji szeregu czasowego skojarzonego z określoną grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="f5e35-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="f5e35-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5e35-122">-InputObject</span></span>
<span data-ttu-id="f5e35-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="f5e35-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f5e35-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f5e35-124">-Name</span></span>
<span data-ttu-id="f5e35-125">Nazwa źródła zdarzeń Szczegółowe informacje o seriach czasu skojarzonych z określonym środowiskiem.</span><span class="sxs-lookup"><span data-stu-id="f5e35-125">The name of the Time Series Insights event source associated with the specified environment.</span></span>

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

### <span data-ttu-id="f5e35-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5e35-126">-ResourceGroupName</span></span>
<span data-ttu-id="f5e35-127">Nazwa grupy usługi Azure Resource.</span><span class="sxs-lookup"><span data-stu-id="f5e35-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="f5e35-128">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f5e35-128">-SubscriptionId</span></span>
<span data-ttu-id="f5e35-129">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f5e35-129">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="f5e35-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5e35-130">CommonParameters</span></span>
<span data-ttu-id="f5e35-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5e35-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5e35-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f5e35-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5e35-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f5e35-133">INPUTS</span></span>

### <span data-ttu-id="f5e35-134">Microsoft.Azure.PowerShell.Cmdlet.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="f5e35-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="f5e35-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f5e35-135">OUTPUTS</span></span>

### <span data-ttu-id="f5e35-136">Microsoft.Azure.PowerShell.Cmdlet.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span><span class="sxs-lookup"><span data-stu-id="f5e35-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="f5e35-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f5e35-137">NOTES</span></span>

<span data-ttu-id="f5e35-138">ALIASY</span><span class="sxs-lookup"><span data-stu-id="f5e35-138">ALIASES</span></span>

<span data-ttu-id="f5e35-139">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="f5e35-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f5e35-140">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="f5e35-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f5e35-141">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f5e35-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f5e35-142">INPUTOBJECT: <ITimeSeriesInsightsIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="f5e35-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f5e35-143">`[AccessPolicyName <String>]`: nazwa zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="f5e35-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="f5e35-144">`[EnvironmentName <String>]`: nazwa środowiska</span><span class="sxs-lookup"><span data-stu-id="f5e35-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="f5e35-145">`[EventSourceName <String>]`: nazwa źródła zdarzeń Szczegółowych informacji szeregu czasowego skojarzonego z określonym środowiskiem.</span><span class="sxs-lookup"><span data-stu-id="f5e35-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="f5e35-146">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="f5e35-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f5e35-147">`[ReferenceDataSetName <String>]`: nazwa zestawu danych referencyjnych.</span><span class="sxs-lookup"><span data-stu-id="f5e35-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="f5e35-148">`[ResourceGroupName <String>]`: nazwa grupy usługi Azure Resource.</span><span class="sxs-lookup"><span data-stu-id="f5e35-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="f5e35-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span><span class="sxs-lookup"><span data-stu-id="f5e35-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="f5e35-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f5e35-150">RELATED LINKS</span></span>

