---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 5590a89b22c0adc3dfb2df88e6b977dec268a822
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232376"
---
# <span data-ttu-id="add2d-101">Get-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="add2d-101">Get-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="add2d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="add2d-102">SYNOPSIS</span></span>
<span data-ttu-id="add2d-103">Pobiera źródło zdarzeń o określonej nazwie w określonym środowisku.</span><span class="sxs-lookup"><span data-stu-id="add2d-103">Gets the event source with the specified name in the specified environment.</span></span>

## <span data-ttu-id="add2d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="add2d-104">SYNTAX</span></span>

### <span data-ttu-id="add2d-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="add2d-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="add2d-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="add2d-106">Get</span></span>
```
Get-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="add2d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="add2d-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="add2d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="add2d-108">DESCRIPTION</span></span>
<span data-ttu-id="add2d-109">Pobiera źródło zdarzeń o określonej nazwie w określonym środowisku.</span><span class="sxs-lookup"><span data-stu-id="add2d-109">Gets the event source with the specified name in the specified environment.</span></span>

## <span data-ttu-id="add2d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="add2d-110">EXAMPLES</span></span>

### <span data-ttu-id="add2d-111">Przykład 1: wyświetlanie wszystkich źródeł zdarzeń w ramach określonego środowiska</span><span class="sxs-lookup"><span data-stu-id="add2d-111">Example 1: List all event sources under the specified environment</span></span>
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

<span data-ttu-id="add2d-112">To polecenie wyświetla listę wszystkich źródeł zdarzeń w określonych środowiskach.</span><span class="sxs-lookup"><span data-stu-id="add2d-112">This command lists all event sources under the specified environments.</span></span>

### <span data-ttu-id="add2d-113">Przykład 2: uzyskiwanie określonego źródła zdarzeń według nazwy</span><span class="sxs-lookup"><span data-stu-id="add2d-113">Example 2: Get a specified event source by name</span></span>
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

<span data-ttu-id="add2d-114">To polecenie pobiera określone źródło zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="add2d-114">This command gets a specific event source.</span></span>

### <span data-ttu-id="add2d-115">Przykład 3: uzyskiwanie określonego źródła zdarzeń według obiektu</span><span class="sxs-lookup"><span data-stu-id="add2d-115">Example 3: Get a specified event source by object</span></span>
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

<span data-ttu-id="add2d-116">To polecenie pobiera określone źródło zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="add2d-116">This command gets a specific event source.</span></span>

## <span data-ttu-id="add2d-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="add2d-117">PARAMETERS</span></span>

### <span data-ttu-id="add2d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="add2d-118">-DefaultProfile</span></span>
<span data-ttu-id="add2d-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="add2d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="add2d-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="add2d-120">-EnvironmentName</span></span>
<span data-ttu-id="add2d-121">Nazwa środowiska informacji o serii czasowej skojarzonego z określoną grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="add2d-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="add2d-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="add2d-122">-InputObject</span></span>
<span data-ttu-id="add2d-123">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="add2d-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="add2d-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="add2d-124">-Name</span></span>
<span data-ttu-id="add2d-125">Nazwa źródła zdarzeń szczegółowych informacji o seriach czasowych skojarzonego z określonym środowiskiem.</span><span class="sxs-lookup"><span data-stu-id="add2d-125">The name of the Time Series Insights event source associated with the specified environment.</span></span>

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

### <span data-ttu-id="add2d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="add2d-126">-ResourceGroupName</span></span>
<span data-ttu-id="add2d-127">Nazwa grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="add2d-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="add2d-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="add2d-128">-SubscriptionId</span></span>
<span data-ttu-id="add2d-129">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="add2d-129">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="add2d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="add2d-130">CommonParameters</span></span>
<span data-ttu-id="add2d-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="add2d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="add2d-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="add2d-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="add2d-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="add2d-133">INPUTS</span></span>

### <span data-ttu-id="add2d-134">Microsoft. Azure. PowerShell. polecenia. TimeSeriesInsights. models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="add2d-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="add2d-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="add2d-135">OUTPUTS</span></span>

### <span data-ttu-id="add2d-136">Microsoft. Azure. PowerShell. polecenia. TimeSeriesInsights. models. Api20200515. IEventSourceResource</span><span class="sxs-lookup"><span data-stu-id="add2d-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="add2d-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="add2d-137">NOTES</span></span>

<span data-ttu-id="add2d-138">PISUJE</span><span class="sxs-lookup"><span data-stu-id="add2d-138">ALIASES</span></span>

<span data-ttu-id="add2d-139">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="add2d-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="add2d-140">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="add2d-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="add2d-141">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="add2d-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="add2d-142">INPUTobject <ITimeSeriesInsightsIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="add2d-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="add2d-143">`[AccessPolicyName <String>]`: Nazwa zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="add2d-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="add2d-144">`[EnvironmentName <String>]`: Nazwa środowiska</span><span class="sxs-lookup"><span data-stu-id="add2d-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="add2d-145">`[EventSourceName <String>]`: Nazwa źródła zdarzeń szczegółowych informacji o seriach czasowych skojarzonego z określonym środowiskiem.</span><span class="sxs-lookup"><span data-stu-id="add2d-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="add2d-146">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="add2d-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="add2d-147">`[ReferenceDataSetName <String>]`: Nazwa zestawu danych referencyjnych.</span><span class="sxs-lookup"><span data-stu-id="add2d-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="add2d-148">`[ResourceGroupName <String>]`: Nazwa grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="add2d-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="add2d-149">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="add2d-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="add2d-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="add2d-150">RELATED LINKS</span></span>

