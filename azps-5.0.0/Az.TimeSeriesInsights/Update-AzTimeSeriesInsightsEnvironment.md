---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: e2b7fa000251a12e09dfd7cd345f54f967962839
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224707"
---
# <span data-ttu-id="452c9-101">Update-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="452c9-101">Update-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="452c9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="452c9-102">SYNOPSIS</span></span>
<span data-ttu-id="452c9-103">Umożliwia zaktualizowanie środowiska o określonej nazwie w określonej grupie subskrypcji i zasobów.</span><span class="sxs-lookup"><span data-stu-id="452c9-103">Updates the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="452c9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="452c9-104">SYNTAX</span></span>

### <span data-ttu-id="452c9-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="452c9-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="452c9-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="452c9-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="452c9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="452c9-107">DESCRIPTION</span></span>
<span data-ttu-id="452c9-108">Umożliwia zaktualizowanie środowiska o określonej nazwie w określonej grupie subskrypcji i zasobów.</span><span class="sxs-lookup"><span data-stu-id="452c9-108">Updates the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="452c9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="452c9-109">EXAMPLES</span></span>

### <span data-ttu-id="452c9-110">Przykład 1: aktualizowanie środowiska szczegółowego dotyczącego serii czasu Gen1</span><span class="sxs-lookup"><span data-stu-id="452c9-110">Example 1: Update a Gen1 time series insights environment</span></span>
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

<span data-ttu-id="452c9-111">To polecenie aktualizuje środowisko Gen1 informacji o seriach czasu.</span><span class="sxs-lookup"><span data-stu-id="452c9-111">This command updates a Gen1 time series insights environment.</span></span>

### <span data-ttu-id="452c9-112">Przykład 2: aktualizowanie środowiska informacji o seriach czasu Gen1</span><span class="sxs-lookup"><span data-stu-id="452c9-112">Example 2:  Update a Gen1 time series insights environment</span></span>
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

<span data-ttu-id="452c9-113">To polecenie aktualizuje środowisko Gen1 informacji o seriach czasu.</span><span class="sxs-lookup"><span data-stu-id="452c9-113">This command updates a Gen1 time series insights environment.</span></span>

## <span data-ttu-id="452c9-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="452c9-114">PARAMETERS</span></span>

### <span data-ttu-id="452c9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="452c9-115">-AsJob</span></span>
<span data-ttu-id="452c9-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="452c9-116">Run the command as a job</span></span>

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

### <span data-ttu-id="452c9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="452c9-117">-DefaultProfile</span></span>
<span data-ttu-id="452c9-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="452c9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="452c9-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="452c9-119">-InputObject</span></span>
<span data-ttu-id="452c9-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="452c9-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="452c9-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="452c9-121">-Name</span></span>
<span data-ttu-id="452c9-122">Nazwa środowiska informacji o serii czasowej skojarzonego z określoną grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="452c9-122">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="452c9-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="452c9-123">-NoWait</span></span>
<span data-ttu-id="452c9-124">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="452c9-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="452c9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="452c9-125">-ResourceGroupName</span></span>
<span data-ttu-id="452c9-126">Nazwa grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="452c9-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="452c9-127">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="452c9-127">-SubscriptionId</span></span>
<span data-ttu-id="452c9-128">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="452c9-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="452c9-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="452c9-129">-Tag</span></span>
<span data-ttu-id="452c9-130">Pary klucz-wartość dodatkowych właściwości dla środowiska.</span><span class="sxs-lookup"><span data-stu-id="452c9-130">Key-value pairs of additional properties for the environment.</span></span>

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

### <span data-ttu-id="452c9-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="452c9-131">-Confirm</span></span>
<span data-ttu-id="452c9-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="452c9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="452c9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="452c9-133">-WhatIf</span></span>
<span data-ttu-id="452c9-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="452c9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="452c9-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="452c9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="452c9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="452c9-136">CommonParameters</span></span>
<span data-ttu-id="452c9-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="452c9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="452c9-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="452c9-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="452c9-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="452c9-139">INPUTS</span></span>

### <span data-ttu-id="452c9-140">Microsoft. Azure. PowerShell. polecenia. TimeSeriesInsights. models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="452c9-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="452c9-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="452c9-141">OUTPUTS</span></span>

### <span data-ttu-id="452c9-142">Microsoft. Azure. PowerShell. polecenia. TimeSeriesInsights. models. Api20200515. IEnvironmentResource</span><span class="sxs-lookup"><span data-stu-id="452c9-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="452c9-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="452c9-143">NOTES</span></span>

<span data-ttu-id="452c9-144">PISUJE</span><span class="sxs-lookup"><span data-stu-id="452c9-144">ALIASES</span></span>

<span data-ttu-id="452c9-145">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="452c9-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="452c9-146">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="452c9-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="452c9-147">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="452c9-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="452c9-148">INPUTobject <ITimeSeriesInsightsIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="452c9-148">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="452c9-149">`[AccessPolicyName <String>]`: Nazwa zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="452c9-149">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="452c9-150">`[EnvironmentName <String>]`: Nazwa środowiska</span><span class="sxs-lookup"><span data-stu-id="452c9-150">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="452c9-151">`[EventSourceName <String>]`: Nazwa źródła zdarzeń szczegółowych informacji o seriach czasowych skojarzonego z określonym środowiskiem.</span><span class="sxs-lookup"><span data-stu-id="452c9-151">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="452c9-152">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="452c9-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="452c9-153">`[ReferenceDataSetName <String>]`: Nazwa zestawu danych referencyjnych.</span><span class="sxs-lookup"><span data-stu-id="452c9-153">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="452c9-154">`[ResourceGroupName <String>]`: Nazwa grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="452c9-154">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="452c9-155">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="452c9-155">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="452c9-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="452c9-156">RELATED LINKS</span></span>

