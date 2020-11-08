---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: e87487e55ce285aa5c430dabaa274ee70c34ba00
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219683"
---
# <span data-ttu-id="0fbfc-101">Update-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="0fbfc-101">Update-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="0fbfc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0fbfc-102">SYNOPSIS</span></span>
<span data-ttu-id="0fbfc-103">Umożliwia zaktualizowanie źródła zdarzeń o określonej nazwie w określonej subskrypcji, grupie zasobów i środowisku.</span><span class="sxs-lookup"><span data-stu-id="0fbfc-103">Updates the event source with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="0fbfc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0fbfc-104">SYNTAX</span></span>

### <span data-ttu-id="0fbfc-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0fbfc-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="0fbfc-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="0fbfc-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0fbfc-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0fbfc-107">DESCRIPTION</span></span>
<span data-ttu-id="0fbfc-108">Umożliwia zaktualizowanie źródła zdarzeń o określonej nazwie w określonej subskrypcji, grupie zasobów i środowisku.</span><span class="sxs-lookup"><span data-stu-id="0fbfc-108">Updates the event source with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="0fbfc-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0fbfc-109">EXAMPLES</span></span>

### <span data-ttu-id="0fbfc-110">Przykład 1: aktualizowanie określonego źródła zdarzeń według nazwy</span><span class="sxs-lookup"><span data-stu-id="0fbfc-110">Example 1: Update a specified event source by name</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -Name iots001 -ResourceGroupName testgroup -Tag @{"tgk"="001"}

ConsumerGroupName     : testgroup2
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.Devices/IotHubs/iotname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eventsources/iots001
IotHubName            : iotname001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.IoTHub
Location              : eastus
Name                  : iots001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="0fbfc-111">To polecenie aktualizuje określone źródło zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="0fbfc-111">This command updates a specific event source.</span></span>

### <span data-ttu-id="0fbfc-112">Przykład 3: aktualizowanie określonego źródła zdarzeń przez obiekt</span><span class="sxs-lookup"><span data-stu-id="0fbfc-112">Example 3: Update a specified event source by object</span></span>
```powershell
PS C:\> $es = Get-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name iots001
PS C:\> Update-AzTimeSeriesInsightsEventSource -InputObject $es -Tag @{"tgb"="002"}

ConsumerGroupName     : testgroup2
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.Devices/IotHubs/iotname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eventsources/iots001
IotHubName            : iotname001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.IoTHub
Location              : eastus
Name                  : iots001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="0fbfc-113">To polecenie aktualizuje określone źródło zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="0fbfc-113">This command updates a specific event source.</span></span>

## <span data-ttu-id="0fbfc-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0fbfc-114">PARAMETERS</span></span>

### <span data-ttu-id="0fbfc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fbfc-115">-DefaultProfile</span></span>
<span data-ttu-id="0fbfc-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0fbfc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fbfc-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="0fbfc-117">-EnvironmentName</span></span>
<span data-ttu-id="0fbfc-118">Nazwa środowiska informacji o serii czasowej skojarzonego z określoną grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="0fbfc-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="0fbfc-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0fbfc-119">-InputObject</span></span>
<span data-ttu-id="0fbfc-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="0fbfc-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0fbfc-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0fbfc-121">-Name</span></span>
<span data-ttu-id="0fbfc-122">Nazwa źródła zdarzeń szczegółowych informacji o seriach czasowych skojarzonego z określonym środowiskiem.</span><span class="sxs-lookup"><span data-stu-id="0fbfc-122">The name of the Time Series Insights event source associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: EventSourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fbfc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fbfc-123">-ResourceGroupName</span></span>
<span data-ttu-id="0fbfc-124">Nazwa grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0fbfc-124">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="0fbfc-125">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="0fbfc-125">-SubscriptionId</span></span>
<span data-ttu-id="0fbfc-126">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0fbfc-126">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fbfc-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="0fbfc-127">-Tag</span></span>
<span data-ttu-id="0fbfc-128">Pary klucz-wartość dodatkowych właściwości źródła zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="0fbfc-128">Key-value pairs of additional properties for the event source.</span></span>

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

### <span data-ttu-id="0fbfc-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0fbfc-129">-Confirm</span></span>
<span data-ttu-id="0fbfc-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0fbfc-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fbfc-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fbfc-131">-WhatIf</span></span>
<span data-ttu-id="0fbfc-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0fbfc-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fbfc-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0fbfc-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fbfc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fbfc-134">CommonParameters</span></span>
<span data-ttu-id="0fbfc-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fbfc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fbfc-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0fbfc-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fbfc-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0fbfc-137">INPUTS</span></span>

### <span data-ttu-id="0fbfc-138">Microsoft. Azure. PowerShell. polecenia. TimeSeriesInsights. models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="0fbfc-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="0fbfc-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0fbfc-139">OUTPUTS</span></span>

### <span data-ttu-id="0fbfc-140">Microsoft. Azure. PowerShell. polecenia. TimeSeriesInsights. models. Api20200515. IEventSourceResource</span><span class="sxs-lookup"><span data-stu-id="0fbfc-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="0fbfc-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0fbfc-141">NOTES</span></span>

<span data-ttu-id="0fbfc-142">PISUJE</span><span class="sxs-lookup"><span data-stu-id="0fbfc-142">ALIASES</span></span>

<span data-ttu-id="0fbfc-143">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0fbfc-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0fbfc-144">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="0fbfc-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0fbfc-145">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0fbfc-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0fbfc-146">INPUTobject <ITimeSeriesInsightsIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="0fbfc-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0fbfc-147">`[AccessPolicyName <String>]`: Nazwa zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="0fbfc-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="0fbfc-148">`[EnvironmentName <String>]`: Nazwa środowiska</span><span class="sxs-lookup"><span data-stu-id="0fbfc-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="0fbfc-149">`[EventSourceName <String>]`: Nazwa źródła zdarzeń szczegółowych informacji o seriach czasowych skojarzonego z określonym środowiskiem.</span><span class="sxs-lookup"><span data-stu-id="0fbfc-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="0fbfc-150">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="0fbfc-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0fbfc-151">`[ReferenceDataSetName <String>]`: Nazwa zestawu danych referencyjnych.</span><span class="sxs-lookup"><span data-stu-id="0fbfc-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="0fbfc-152">`[ResourceGroupName <String>]`: Nazwa grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0fbfc-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="0fbfc-153">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0fbfc-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="0fbfc-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0fbfc-154">RELATED LINKS</span></span>

