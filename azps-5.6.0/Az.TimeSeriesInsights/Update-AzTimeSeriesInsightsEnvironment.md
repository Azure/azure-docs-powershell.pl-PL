---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: 86e143455f287bef8bff4b391f7f40aa01fba99b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987435"
---
# <span data-ttu-id="80b4a-101">Update-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="80b4a-101">Update-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="80b4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80b4a-102">SYNOPSIS</span></span>
<span data-ttu-id="80b4a-103">Aktualizuje środowisko o określonej nazwie w określonej grupie subskrypcji i zasobów.</span><span class="sxs-lookup"><span data-stu-id="80b4a-103">Updates the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="80b4a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="80b4a-104">SYNTAX</span></span>

### <span data-ttu-id="80b4a-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="80b4a-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="80b4a-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="80b4a-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="80b4a-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="80b4a-107">DESCRIPTION</span></span>
<span data-ttu-id="80b4a-108">Aktualizuje środowisko o określonej nazwie w określonej grupie subskrypcji i zasobów.</span><span class="sxs-lookup"><span data-stu-id="80b4a-108">Updates the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="80b4a-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="80b4a-109">EXAMPLES</span></span>

### <span data-ttu-id="80b4a-110">Przykład 1. Aktualizowanie środowiska szczegółowych informacji szeregu czasowego generacji 1</span><span class="sxs-lookup"><span data-stu-id="80b4a-110">Example 1: Update a Gen1 time series insights environment</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001 -Tag @{'key1'='val1'}

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
SkuCapacity                  : 5
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="80b4a-111">To polecenie aktualizuje środowisko szczegółowych informacji szeregu czasowego generacji 1.</span><span class="sxs-lookup"><span data-stu-id="80b4a-111">This command updates a Gen1 time series insights environment.</span></span>

### <span data-ttu-id="80b4a-112">Przykład 2. Aktualizowanie środowiska szczegółowych informacji szeregu czasowego generacji 1</span><span class="sxs-lookup"><span data-stu-id="80b4a-112">Example 2:  Update a Gen1 time series insights environment</span></span>
```powershell
PS C:\> $env = Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001
PS C:\> Update-AzTimeSeriesInsightsEnvironment -InputObject $env -Tag @{'key2'='val2'}

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
SkuCapacity                  : 5
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="80b4a-113">To polecenie aktualizuje środowisko szczegółowych informacji szeregu czasowego generacji 1.</span><span class="sxs-lookup"><span data-stu-id="80b4a-113">This command updates a Gen1 time series insights environment.</span></span>

## <span data-ttu-id="80b4a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80b4a-114">PARAMETERS</span></span>

### <span data-ttu-id="80b4a-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="80b4a-115">-AsJob</span></span>
<span data-ttu-id="80b4a-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="80b4a-116">Run the command as a job</span></span>

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

### <span data-ttu-id="80b4a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80b4a-117">-DefaultProfile</span></span>
<span data-ttu-id="80b4a-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="80b4a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80b4a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80b4a-119">-InputObject</span></span>
<span data-ttu-id="80b4a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="80b4a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="80b4a-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="80b4a-121">-Name</span></span>
<span data-ttu-id="80b4a-122">Nazwa środowiska szczegółowych informacji szeregu czasowego skojarzonego z określoną grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="80b4a-122">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80b4a-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="80b4a-123">-NoWait</span></span>
<span data-ttu-id="80b4a-124">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="80b4a-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="80b4a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80b4a-125">-ResourceGroupName</span></span>
<span data-ttu-id="80b4a-126">Nazwa grupy usługi Azure Resource.</span><span class="sxs-lookup"><span data-stu-id="80b4a-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="80b4a-127">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="80b4a-127">-SubscriptionId</span></span>
<span data-ttu-id="80b4a-128">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="80b4a-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="80b4a-129">— Tag</span><span class="sxs-lookup"><span data-stu-id="80b4a-129">-Tag</span></span>
<span data-ttu-id="80b4a-130">Pary klucz-wartość dodatkowych właściwości środowiska.</span><span class="sxs-lookup"><span data-stu-id="80b4a-130">Key-value pairs of additional properties for the environment.</span></span>

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

### <span data-ttu-id="80b4a-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="80b4a-131">-Confirm</span></span>
<span data-ttu-id="80b4a-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="80b4a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80b4a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80b4a-133">-WhatIf</span></span>
<span data-ttu-id="80b4a-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80b4a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80b4a-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="80b4a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80b4a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80b4a-136">CommonParameters</span></span>
<span data-ttu-id="80b4a-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80b4a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80b4a-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80b4a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80b4a-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="80b4a-139">INPUTS</span></span>

### <span data-ttu-id="80b4a-140">Microsoft.Azure.PowerShell.Cmdlet.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="80b4a-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="80b4a-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="80b4a-141">OUTPUTS</span></span>

### <span data-ttu-id="80b4a-142">Microsoft.Azure.PowerShell.Cmdlet.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span><span class="sxs-lookup"><span data-stu-id="80b4a-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="80b4a-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="80b4a-143">NOTES</span></span>

<span data-ttu-id="80b4a-144">ALIASY</span><span class="sxs-lookup"><span data-stu-id="80b4a-144">ALIASES</span></span>

<span data-ttu-id="80b4a-145">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="80b4a-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="80b4a-146">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="80b4a-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="80b4a-147">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="80b4a-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="80b4a-148">INPUTOBJECT: <ITimeSeriesInsightsIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="80b4a-148">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="80b4a-149">`[AccessPolicyName <String>]`: nazwa zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="80b4a-149">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="80b4a-150">`[EnvironmentName <String>]`: nazwa środowiska</span><span class="sxs-lookup"><span data-stu-id="80b4a-150">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="80b4a-151">`[EventSourceName <String>]`: nazwa źródła zdarzeń Szczegółowych informacji szeregu czasowego skojarzonego z określonym środowiskiem.</span><span class="sxs-lookup"><span data-stu-id="80b4a-151">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="80b4a-152">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="80b4a-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="80b4a-153">`[ReferenceDataSetName <String>]`: nazwa zestawu danych referencyjnych.</span><span class="sxs-lookup"><span data-stu-id="80b4a-153">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="80b4a-154">`[ResourceGroupName <String>]`: nazwa grupy azure resource.</span><span class="sxs-lookup"><span data-stu-id="80b4a-154">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="80b4a-155">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="80b4a-155">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="80b4a-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="80b4a-156">RELATED LINKS</span></span>

