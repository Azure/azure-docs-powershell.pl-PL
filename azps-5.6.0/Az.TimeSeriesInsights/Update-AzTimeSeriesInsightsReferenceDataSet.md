---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 956e7a1a2fd0917dd3b647ef547eec165c1cd5ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987414"
---
# <span data-ttu-id="e6f52-101">Update-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="e6f52-101">Update-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="e6f52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6f52-102">SYNOPSIS</span></span>
<span data-ttu-id="e6f52-103">Aktualizuje zestaw danych referencyjnych o określonej nazwie w określonej subskrypcji, grupie zasobów i środowisku.</span><span class="sxs-lookup"><span data-stu-id="e6f52-103">Updates the reference data set with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="e6f52-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e6f52-104">SYNTAX</span></span>

### <span data-ttu-id="e6f52-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="e6f52-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e6f52-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e6f52-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e6f52-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="e6f52-107">DESCRIPTION</span></span>
<span data-ttu-id="e6f52-108">Aktualizuje zestaw danych referencyjnych o określonej nazwie w określonej subskrypcji, grupie zasobów i środowisku.</span><span class="sxs-lookup"><span data-stu-id="e6f52-108">Updates the reference data set with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="e6f52-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e6f52-109">EXAMPLES</span></span>

### <span data-ttu-id="e6f52-110">Przykład 1. Aktualizowanie określonego zestawu danych odwołania według nazwy</span><span class="sxs-lookup"><span data-stu-id="e6f52-110">Example 1: Update a specified reference data set by name</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup -Tag @{"tstg"="lb001"}

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="e6f52-111">To polecenie aktualizuje określony zestaw danych referencyjnych.</span><span class="sxs-lookup"><span data-stu-id="e6f52-111">This command updates a specified reference data set.</span></span>

### <span data-ttu-id="e6f52-112">Przykład 2. Aktualizowanie określonego zestawu danych odwołania według obiektu</span><span class="sxs-lookup"><span data-stu-id="e6f52-112">Example 2: Update a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup -ReferenceDataSetName dstest001
PS C:\> Update-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds -Tag @{"tstg"="lb001"}

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="e6f52-113">To polecenie aktualizuje określony zestaw danych referencyjnych.</span><span class="sxs-lookup"><span data-stu-id="e6f52-113">This command updates a specified reference data set.</span></span>

## <span data-ttu-id="e6f52-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6f52-114">PARAMETERS</span></span>

### <span data-ttu-id="e6f52-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6f52-115">-DefaultProfile</span></span>
<span data-ttu-id="e6f52-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e6f52-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6f52-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="e6f52-117">-EnvironmentName</span></span>
<span data-ttu-id="e6f52-118">Nazwa środowiska szczegółowych informacji szeregu czasowego skojarzonego z określoną grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="e6f52-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="e6f52-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6f52-119">-InputObject</span></span>
<span data-ttu-id="e6f52-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="e6f52-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e6f52-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e6f52-121">-Name</span></span>
<span data-ttu-id="e6f52-122">Nazwa szczegółowych informacji z serii czasowej odwołuje się do zestawu danych skojarzonego z określonym środowiskiem.</span><span class="sxs-lookup"><span data-stu-id="e6f52-122">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ReferenceDataSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6f52-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6f52-123">-ResourceGroupName</span></span>
<span data-ttu-id="e6f52-124">Nazwa grupy usługi Azure Resource.</span><span class="sxs-lookup"><span data-stu-id="e6f52-124">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="e6f52-125">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e6f52-125">-SubscriptionId</span></span>
<span data-ttu-id="e6f52-126">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e6f52-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="e6f52-127">— Tag</span><span class="sxs-lookup"><span data-stu-id="e6f52-127">-Tag</span></span>
<span data-ttu-id="e6f52-128">Pary klucz-wartość dodatkowych właściwości dla odwołania do zestawu danych.</span><span class="sxs-lookup"><span data-stu-id="e6f52-128">Key-value pairs of additional properties for the reference data set.</span></span>

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

### <span data-ttu-id="e6f52-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e6f52-129">-Confirm</span></span>
<span data-ttu-id="e6f52-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e6f52-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6f52-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6f52-131">-WhatIf</span></span>
<span data-ttu-id="e6f52-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6f52-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6f52-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e6f52-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6f52-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6f52-134">CommonParameters</span></span>
<span data-ttu-id="e6f52-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6f52-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6f52-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6f52-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6f52-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e6f52-137">INPUTS</span></span>

### <span data-ttu-id="e6f52-138">Microsoft.Azure.PowerShell.Cmdlet.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="e6f52-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="e6f52-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e6f52-139">OUTPUTS</span></span>

### <span data-ttu-id="e6f52-140">Microsoft.Azure.PowerShell.Cmdlet.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span><span class="sxs-lookup"><span data-stu-id="e6f52-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="e6f52-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e6f52-141">NOTES</span></span>

<span data-ttu-id="e6f52-142">ALIASY</span><span class="sxs-lookup"><span data-stu-id="e6f52-142">ALIASES</span></span>

<span data-ttu-id="e6f52-143">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e6f52-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e6f52-144">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="e6f52-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e6f52-145">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e6f52-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e6f52-146">INPUTOBJECT: <ITimeSeriesInsightsIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="e6f52-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e6f52-147">`[AccessPolicyName <String>]`: nazwa zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="e6f52-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="e6f52-148">`[EnvironmentName <String>]`: nazwa środowiska</span><span class="sxs-lookup"><span data-stu-id="e6f52-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="e6f52-149">`[EventSourceName <String>]`: nazwa źródła zdarzeń Szczegółowych informacji szeregu czasowego skojarzonego z określonym środowiskiem.</span><span class="sxs-lookup"><span data-stu-id="e6f52-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="e6f52-150">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="e6f52-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e6f52-151">`[ReferenceDataSetName <String>]`: nazwa zestawu danych referencyjnych.</span><span class="sxs-lookup"><span data-stu-id="e6f52-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="e6f52-152">`[ResourceGroupName <String>]`: nazwa grupy azure resource.</span><span class="sxs-lookup"><span data-stu-id="e6f52-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="e6f52-153">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e6f52-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="e6f52-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e6f52-154">RELATED LINKS</span></span>

