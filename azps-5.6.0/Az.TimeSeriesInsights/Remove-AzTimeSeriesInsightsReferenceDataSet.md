---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 99271e0933662df4789338bcdcacc5a278fa3b4c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991859"
---
# <span data-ttu-id="6fe9e-101">Remove-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="6fe9e-101">Remove-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="6fe9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fe9e-102">SYNOPSIS</span></span>
<span data-ttu-id="6fe9e-103">Usuwa zestaw danych referencyjnych o określonej nazwie w określonej subskrypcji, grupie zasobów i środowisku.</span><span class="sxs-lookup"><span data-stu-id="6fe9e-103">Deletes the reference data set with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="6fe9e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6fe9e-104">SYNTAX</span></span>

### <span data-ttu-id="6fe9e-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="6fe9e-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6fe9e-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6fe9e-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity>
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6fe9e-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="6fe9e-107">DESCRIPTION</span></span>
<span data-ttu-id="6fe9e-108">Usuwa zestaw danych referencyjnych o określonej nazwie w określonej subskrypcji, grupie zasobów i środowisku.</span><span class="sxs-lookup"><span data-stu-id="6fe9e-108">Deletes the reference data set with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="6fe9e-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6fe9e-109">EXAMPLES</span></span>

### <span data-ttu-id="6fe9e-110">Przykład 1. Usuwanie określonego zestawu danych odwołania według nazwy</span><span class="sxs-lookup"><span data-stu-id="6fe9e-110">Example 1: Remove a specified reference data set by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup

```

<span data-ttu-id="6fe9e-111">To polecenie usuwa określony zestaw danych odwołania.</span><span class="sxs-lookup"><span data-stu-id="6fe9e-111">This command removes a specified reference data set.</span></span>

### <span data-ttu-id="6fe9e-112">Przykład 2. Usuwanie określonego zestawu danych odwołania z obiektu</span><span class="sxs-lookup"><span data-stu-id="6fe9e-112">Example 2: Remove a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup
PS C:\> Remove-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds

```

<span data-ttu-id="6fe9e-113">To polecenie usuwa określony zestaw danych odwołania.</span><span class="sxs-lookup"><span data-stu-id="6fe9e-113">This command removes a specified reference data set.</span></span>

## <span data-ttu-id="6fe9e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6fe9e-114">PARAMETERS</span></span>

### <span data-ttu-id="6fe9e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fe9e-115">-DefaultProfile</span></span>
<span data-ttu-id="6fe9e-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6fe9e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fe9e-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="6fe9e-117">-EnvironmentName</span></span>
<span data-ttu-id="6fe9e-118">Nazwa środowiska szczegółowych informacji szeregu czasowego skojarzonego z określoną grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="6fe9e-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="6fe9e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6fe9e-119">-InputObject</span></span>
<span data-ttu-id="6fe9e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="6fe9e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6fe9e-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6fe9e-121">-Name</span></span>
<span data-ttu-id="6fe9e-122">Nazwa szczegółowych informacji z serii czasowej odwołuje się do zestawu danych skojarzonego z określonym środowiskiem.</span><span class="sxs-lookup"><span data-stu-id="6fe9e-122">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ReferenceDataSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fe9e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6fe9e-123">-PassThru</span></span>
<span data-ttu-id="6fe9e-124">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="6fe9e-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6fe9e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fe9e-125">-ResourceGroupName</span></span>
<span data-ttu-id="6fe9e-126">Nazwa grupy usługi Azure Resource.</span><span class="sxs-lookup"><span data-stu-id="6fe9e-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="6fe9e-127">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6fe9e-127">-SubscriptionId</span></span>
<span data-ttu-id="6fe9e-128">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6fe9e-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="6fe9e-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6fe9e-129">-Confirm</span></span>
<span data-ttu-id="6fe9e-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6fe9e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fe9e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fe9e-131">-WhatIf</span></span>
<span data-ttu-id="6fe9e-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6fe9e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fe9e-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6fe9e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fe9e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fe9e-134">CommonParameters</span></span>
<span data-ttu-id="6fe9e-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fe9e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fe9e-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6fe9e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fe9e-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6fe9e-137">INPUTS</span></span>

### <span data-ttu-id="6fe9e-138">Microsoft.Azure.PowerShell.Cmdlet.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="6fe9e-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="6fe9e-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6fe9e-139">OUTPUTS</span></span>

### <span data-ttu-id="6fe9e-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6fe9e-140">System.Boolean</span></span>

## <span data-ttu-id="6fe9e-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6fe9e-141">NOTES</span></span>

<span data-ttu-id="6fe9e-142">ALIASY</span><span class="sxs-lookup"><span data-stu-id="6fe9e-142">ALIASES</span></span>

<span data-ttu-id="6fe9e-143">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6fe9e-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6fe9e-144">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="6fe9e-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6fe9e-145">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6fe9e-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6fe9e-146">INPUTOBJECT: <ITimeSeriesInsightsIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="6fe9e-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6fe9e-147">`[AccessPolicyName <String>]`: nazwa zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="6fe9e-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="6fe9e-148">`[EnvironmentName <String>]`: nazwa środowiska</span><span class="sxs-lookup"><span data-stu-id="6fe9e-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="6fe9e-149">`[EventSourceName <String>]`: nazwa źródła zdarzeń Szczegółowych informacji szeregu czasowego skojarzonego z określonym środowiskiem.</span><span class="sxs-lookup"><span data-stu-id="6fe9e-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="6fe9e-150">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="6fe9e-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6fe9e-151">`[ReferenceDataSetName <String>]`: nazwa zestawu danych referencyjnych.</span><span class="sxs-lookup"><span data-stu-id="6fe9e-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="6fe9e-152">`[ResourceGroupName <String>]`: nazwa grupy azure resource.</span><span class="sxs-lookup"><span data-stu-id="6fe9e-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="6fe9e-153">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6fe9e-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="6fe9e-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6fe9e-154">RELATED LINKS</span></span>

