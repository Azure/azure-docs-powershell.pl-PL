---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 7f647da2543a4675dad53f88e2494aa7f6c39419
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182595"
---
# <span data-ttu-id="49bd3-101">Remove-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="49bd3-101">Remove-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="49bd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49bd3-102">SYNOPSIS</span></span>
<span data-ttu-id="49bd3-103">Usuwa źródło zdarzeń o określonej nazwie w określonej subskrypcji, grupie zasobów i środowisku.</span><span class="sxs-lookup"><span data-stu-id="49bd3-103">Deletes the event source with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="49bd3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="49bd3-104">SYNTAX</span></span>

### <span data-ttu-id="49bd3-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="49bd3-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="49bd3-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="49bd3-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="49bd3-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="49bd3-107">DESCRIPTION</span></span>
<span data-ttu-id="49bd3-108">Usuwa źródło zdarzeń o określonej nazwie w określonej subskrypcji, grupie zasobów i środowisku.</span><span class="sxs-lookup"><span data-stu-id="49bd3-108">Deletes the event source with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="49bd3-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="49bd3-109">EXAMPLES</span></span>

### <span data-ttu-id="49bd3-110">Przykład 1. Usuwanie określonego źródła zdarzeń według nazwy</span><span class="sxs-lookup"><span data-stu-id="49bd3-110">Example 1: Remove a specified event source by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -Name iots001 -ResourceGroupName testgroup

```

<span data-ttu-id="49bd3-111">Spowoduje to usunięcie określonego źródła zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="49bd3-111">This removes a specific event source.</span></span>

### <span data-ttu-id="49bd3-112">Przykład 2. Usuwanie określonego źródła zdarzeń przez obiekt</span><span class="sxs-lookup"><span data-stu-id="49bd3-112">Example 2: Remove a specified event source by object</span></span>
```powershell
PS C:\> $es = Get-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name iots001
PS C:\> Remove-AzTimeSeriesInsightsEventSource -InputObject $es

```

<span data-ttu-id="49bd3-113">Spowoduje to usunięcie określonego źródła zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="49bd3-113">This removes a specific event source.</span></span>

## <span data-ttu-id="49bd3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49bd3-114">PARAMETERS</span></span>

### <span data-ttu-id="49bd3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49bd3-115">-DefaultProfile</span></span>
<span data-ttu-id="49bd3-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="49bd3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49bd3-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="49bd3-117">-EnvironmentName</span></span>
<span data-ttu-id="49bd3-118">Nazwa środowiska szczegółowych informacji szeregu czasowego skojarzonego z określoną grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="49bd3-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49bd3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49bd3-119">-InputObject</span></span>
<span data-ttu-id="49bd3-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="49bd3-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49bd3-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="49bd3-121">-Name</span></span>
<span data-ttu-id="49bd3-122">Nazwa źródła zdarzeń Szczegółowe informacje o seriach czasu skojarzonych z określonym środowiskiem.</span><span class="sxs-lookup"><span data-stu-id="49bd3-122">The name of the Time Series Insights event source associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: EventSourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49bd3-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49bd3-123">-PassThru</span></span>
<span data-ttu-id="49bd3-124">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="49bd3-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="49bd3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49bd3-125">-ResourceGroupName</span></span>
<span data-ttu-id="49bd3-126">Nazwa grupy usługi Azure Resource.</span><span class="sxs-lookup"><span data-stu-id="49bd3-126">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49bd3-127">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="49bd3-127">-SubscriptionId</span></span>
<span data-ttu-id="49bd3-128">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="49bd3-128">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49bd3-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="49bd3-129">-Confirm</span></span>
<span data-ttu-id="49bd3-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="49bd3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49bd3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49bd3-131">-WhatIf</span></span>
<span data-ttu-id="49bd3-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49bd3-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49bd3-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="49bd3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49bd3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49bd3-134">CommonParameters</span></span>
<span data-ttu-id="49bd3-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49bd3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49bd3-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49bd3-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49bd3-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49bd3-137">INPUTS</span></span>

### <span data-ttu-id="49bd3-138">Microsoft.Azure.PowerShell.Cmdlet.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="49bd3-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="49bd3-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49bd3-139">OUTPUTS</span></span>

### <span data-ttu-id="49bd3-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="49bd3-140">System.Boolean</span></span>

## <span data-ttu-id="49bd3-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="49bd3-141">NOTES</span></span>

<span data-ttu-id="49bd3-142">ALIASY</span><span class="sxs-lookup"><span data-stu-id="49bd3-142">ALIASES</span></span>

<span data-ttu-id="49bd3-143">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="49bd3-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="49bd3-144">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="49bd3-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="49bd3-145">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="49bd3-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="49bd3-146">INPUTOBJECT: <ITimeSeriesInsightsIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="49bd3-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="49bd3-147">`[AccessPolicyName <String>]`: nazwa zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="49bd3-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="49bd3-148">`[EnvironmentName <String>]`: nazwa środowiska</span><span class="sxs-lookup"><span data-stu-id="49bd3-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="49bd3-149">`[EventSourceName <String>]`: nazwa źródła zdarzeń Szczegółowych informacji szeregu czasowego skojarzonego z określonym środowiskiem.</span><span class="sxs-lookup"><span data-stu-id="49bd3-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="49bd3-150">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="49bd3-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="49bd3-151">`[ReferenceDataSetName <String>]`: nazwa zestawu danych referencyjnych.</span><span class="sxs-lookup"><span data-stu-id="49bd3-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="49bd3-152">`[ResourceGroupName <String>]`: nazwa grupy azure resource.</span><span class="sxs-lookup"><span data-stu-id="49bd3-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="49bd3-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span><span class="sxs-lookup"><span data-stu-id="49bd3-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="49bd3-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="49bd3-154">RELATED LINKS</span></span>

