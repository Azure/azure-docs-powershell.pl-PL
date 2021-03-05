---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: 89fa39a5e6e1bb2ded61c41dd553b6d7d0473d4f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963377"
---
# <span data-ttu-id="5878b-101">Remove-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="5878b-101">Remove-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="5878b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5878b-102">SYNOPSIS</span></span>
<span data-ttu-id="5878b-103">Usuwa środowisko o określonej nazwie w określonej grupie subskrypcji i zasobów.</span><span class="sxs-lookup"><span data-stu-id="5878b-103">Deletes the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="5878b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5878b-104">SYNTAX</span></span>

### <span data-ttu-id="5878b-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="5878b-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5878b-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5878b-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5878b-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="5878b-107">DESCRIPTION</span></span>
<span data-ttu-id="5878b-108">Usuwa środowisko o określonej nazwie w określonej grupie subskrypcji i zasobów.</span><span class="sxs-lookup"><span data-stu-id="5878b-108">Deletes the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="5878b-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5878b-109">EXAMPLES</span></span>

### <span data-ttu-id="5878b-110">Przykład 1. Usuwanie środowiska szczegółowych informacji z serii czasowej według nazwy</span><span class="sxs-lookup"><span data-stu-id="5878b-110">Example 1: Remove a time series insights environment by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsill

```

<span data-ttu-id="5878b-111">To polecenie usuwa środowisko szczegółowych informacji szeregu czasowego.</span><span class="sxs-lookup"><span data-stu-id="5878b-111">This command removes a time series insights environment.</span></span>

### <span data-ttu-id="5878b-112">Przykład 2. Usuwanie środowiska szczegółowych informacji z serii czasowej według obiektu</span><span class="sxs-lookup"><span data-stu-id="5878b-112">Example 2: Remove a time series insights environment by object</span></span>
```powershell
PS C:\> $env = Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsill
PS C:\> Remove-AzTimeSeriesInsightsEnvironment -InputObject $env

```

<span data-ttu-id="5878b-113">To polecenie usuwa środowisko szczegółowych informacji szeregu czasowego.</span><span class="sxs-lookup"><span data-stu-id="5878b-113">This command removes a time series insights environment.</span></span>

## <span data-ttu-id="5878b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5878b-114">PARAMETERS</span></span>

### <span data-ttu-id="5878b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5878b-115">-DefaultProfile</span></span>
<span data-ttu-id="5878b-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5878b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5878b-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5878b-117">-InputObject</span></span>
<span data-ttu-id="5878b-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="5878b-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5878b-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5878b-119">-Name</span></span>
<span data-ttu-id="5878b-120">Nazwa środowiska szczegółowych informacji szeregu czasowego skojarzonego z określoną grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="5878b-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5878b-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5878b-121">-PassThru</span></span>
<span data-ttu-id="5878b-122">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="5878b-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5878b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5878b-123">-ResourceGroupName</span></span>
<span data-ttu-id="5878b-124">Nazwa grupy usługi Azure Resource.</span><span class="sxs-lookup"><span data-stu-id="5878b-124">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="5878b-125">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5878b-125">-SubscriptionId</span></span>
<span data-ttu-id="5878b-126">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5878b-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="5878b-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5878b-127">-Confirm</span></span>
<span data-ttu-id="5878b-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5878b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5878b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5878b-129">-WhatIf</span></span>
<span data-ttu-id="5878b-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5878b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5878b-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5878b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5878b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5878b-132">CommonParameters</span></span>
<span data-ttu-id="5878b-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5878b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5878b-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5878b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5878b-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5878b-135">INPUTS</span></span>

### <span data-ttu-id="5878b-136">Microsoft.Azure.PowerShell.Cmdlet.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="5878b-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="5878b-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5878b-137">OUTPUTS</span></span>

### <span data-ttu-id="5878b-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5878b-138">System.Boolean</span></span>

## <span data-ttu-id="5878b-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5878b-139">NOTES</span></span>

<span data-ttu-id="5878b-140">ALIASY</span><span class="sxs-lookup"><span data-stu-id="5878b-140">ALIASES</span></span>

<span data-ttu-id="5878b-141">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5878b-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5878b-142">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="5878b-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5878b-143">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5878b-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5878b-144">INPUTOBJECT: <ITimeSeriesInsightsIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="5878b-144">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5878b-145">`[AccessPolicyName <String>]`: nazwa zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="5878b-145">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="5878b-146">`[EnvironmentName <String>]`: nazwa środowiska</span><span class="sxs-lookup"><span data-stu-id="5878b-146">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="5878b-147">`[EventSourceName <String>]`: nazwa źródła zdarzeń Szczegółowych informacji szeregu czasowego skojarzonego z określonym środowiskiem.</span><span class="sxs-lookup"><span data-stu-id="5878b-147">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="5878b-148">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="5878b-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5878b-149">`[ReferenceDataSetName <String>]`: nazwa zestawu danych referencyjnych.</span><span class="sxs-lookup"><span data-stu-id="5878b-149">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="5878b-150">`[ResourceGroupName <String>]`: nazwa grupy azure resource.</span><span class="sxs-lookup"><span data-stu-id="5878b-150">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="5878b-151">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5878b-151">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="5878b-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5878b-152">RELATED LINKS</span></span>

