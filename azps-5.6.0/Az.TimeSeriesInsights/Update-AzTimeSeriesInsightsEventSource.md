---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 7e4063858edaa6180e1f57bc05898ae170284546
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987428"
---
# <span data-ttu-id="42868-101">Update-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="42868-101">Update-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="42868-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42868-102">SYNOPSIS</span></span>
<span data-ttu-id="42868-103">Aktualizuje źródło zdarzeń o określonej nazwie w określonej subskrypcji, grupie zasobów i środowisku.</span><span class="sxs-lookup"><span data-stu-id="42868-103">Updates the event source with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="42868-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="42868-104">SYNTAX</span></span>

### <span data-ttu-id="42868-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="42868-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="42868-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="42868-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="42868-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="42868-107">DESCRIPTION</span></span>
<span data-ttu-id="42868-108">Aktualizuje źródło zdarzeń o określonej nazwie w określonej subskrypcji, grupie zasobów i środowisku.</span><span class="sxs-lookup"><span data-stu-id="42868-108">Updates the event source with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="42868-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="42868-109">EXAMPLES</span></span>

### <span data-ttu-id="42868-110">Przykład 1. Aktualizowanie określonego źródła zdarzeń według nazwy</span><span class="sxs-lookup"><span data-stu-id="42868-110">Example 1: Update a specified event source by name</span></span>
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

<span data-ttu-id="42868-111">To polecenie aktualizuje określone źródło zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="42868-111">This command updates a specific event source.</span></span>

### <span data-ttu-id="42868-112">Przykład 3. Aktualizowanie określonego źródła zdarzeń według obiektu</span><span class="sxs-lookup"><span data-stu-id="42868-112">Example 3: Update a specified event source by object</span></span>
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

<span data-ttu-id="42868-113">To polecenie aktualizuje określone źródło zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="42868-113">This command updates a specific event source.</span></span>

## <span data-ttu-id="42868-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="42868-114">PARAMETERS</span></span>

### <span data-ttu-id="42868-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42868-115">-DefaultProfile</span></span>
<span data-ttu-id="42868-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="42868-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42868-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="42868-117">-EnvironmentName</span></span>
<span data-ttu-id="42868-118">Nazwa środowiska szczegółowych informacji szeregu czasowego skojarzonego z określoną grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="42868-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="42868-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42868-119">-InputObject</span></span>
<span data-ttu-id="42868-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="42868-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="42868-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="42868-121">-Name</span></span>
<span data-ttu-id="42868-122">Nazwa źródła zdarzeń Szczegółowe informacje o seriach czasu skojarzonych z określonym środowiskiem.</span><span class="sxs-lookup"><span data-stu-id="42868-122">The name of the Time Series Insights event source associated with the specified environment.</span></span>

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

### <span data-ttu-id="42868-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42868-123">-ResourceGroupName</span></span>
<span data-ttu-id="42868-124">Nazwa grupy usługi Azure Resource.</span><span class="sxs-lookup"><span data-stu-id="42868-124">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="42868-125">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="42868-125">-SubscriptionId</span></span>
<span data-ttu-id="42868-126">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="42868-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="42868-127">— Tag</span><span class="sxs-lookup"><span data-stu-id="42868-127">-Tag</span></span>
<span data-ttu-id="42868-128">Pary klucz-wartość dodatkowych właściwości źródła zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="42868-128">Key-value pairs of additional properties for the event source.</span></span>

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

### <span data-ttu-id="42868-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="42868-129">-Confirm</span></span>
<span data-ttu-id="42868-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="42868-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42868-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42868-131">-WhatIf</span></span>
<span data-ttu-id="42868-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42868-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42868-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="42868-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42868-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42868-134">CommonParameters</span></span>
<span data-ttu-id="42868-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42868-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42868-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="42868-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42868-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="42868-137">INPUTS</span></span>

### <span data-ttu-id="42868-138">Microsoft.Azure.PowerShell.Cmdlet.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="42868-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="42868-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="42868-139">OUTPUTS</span></span>

### <span data-ttu-id="42868-140">Microsoft.Azure.PowerShell.Cmdlet.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span><span class="sxs-lookup"><span data-stu-id="42868-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="42868-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="42868-141">NOTES</span></span>

<span data-ttu-id="42868-142">ALIASY</span><span class="sxs-lookup"><span data-stu-id="42868-142">ALIASES</span></span>

<span data-ttu-id="42868-143">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="42868-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="42868-144">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="42868-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="42868-145">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="42868-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="42868-146">INPUTOBJECT: <ITimeSeriesInsightsIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="42868-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="42868-147">`[AccessPolicyName <String>]`: nazwa zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="42868-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="42868-148">`[EnvironmentName <String>]`: nazwa środowiska</span><span class="sxs-lookup"><span data-stu-id="42868-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="42868-149">`[EventSourceName <String>]`: nazwa źródła zdarzeń Szczegółowych informacji szeregu czasowego skojarzonego z określonym środowiskiem.</span><span class="sxs-lookup"><span data-stu-id="42868-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="42868-150">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="42868-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="42868-151">`[ReferenceDataSetName <String>]`: nazwa zestawu danych referencyjnych.</span><span class="sxs-lookup"><span data-stu-id="42868-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="42868-152">`[ResourceGroupName <String>]`: nazwa grupy azure resource.</span><span class="sxs-lookup"><span data-stu-id="42868-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="42868-153">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="42868-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="42868-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="42868-154">RELATED LINKS</span></span>

