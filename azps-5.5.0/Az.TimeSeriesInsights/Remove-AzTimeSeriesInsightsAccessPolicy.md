---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: 2a6c58729d08c5bd060434c7a21720f87a3f7de3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190546"
---
# <span data-ttu-id="71fe6-101">Remove-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="71fe6-101">Remove-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="71fe6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71fe6-102">SYNOPSIS</span></span>
<span data-ttu-id="71fe6-103">Usuwa zasady dostępu o określonej nazwie w określonej subskrypcji, grupie zasobów i środowisku.</span><span class="sxs-lookup"><span data-stu-id="71fe6-103">Deletes the access policy with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="71fe6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="71fe6-104">SYNTAX</span></span>

### <span data-ttu-id="71fe6-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="71fe6-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="71fe6-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="71fe6-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity>
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="71fe6-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="71fe6-107">DESCRIPTION</span></span>
<span data-ttu-id="71fe6-108">Usuwa zasady dostępu o określonej nazwie w określonej subskrypcji, grupie zasobów i środowisku.</span><span class="sxs-lookup"><span data-stu-id="71fe6-108">Deletes the access policy with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="71fe6-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="71fe6-109">EXAMPLES</span></span>

### <span data-ttu-id="71fe6-110">Przykład 1. Usuwanie określonych zasad dostępu według nazwy</span><span class="sxs-lookup"><span data-stu-id="71fe6-110">Example 1: Remove a specified access policy by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup

```

<span data-ttu-id="71fe6-111">To polecenie usuwa określone zasady dostępu.</span><span class="sxs-lookup"><span data-stu-id="71fe6-111">This command removes a specified access policy.</span></span>

### <span data-ttu-id="71fe6-112">Przykład 2. Usuwanie określonych zasad dostępu z obiektu</span><span class="sxs-lookup"><span data-stu-id="71fe6-112">Example 2: Remove a specified access policy by object</span></span>
```powershell
PS C:\> $policy = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup
PS C:\> Remove-AzTimeSeriesInsightsAccessPolicy -InputObject $policy

```

<span data-ttu-id="71fe6-113">To polecenie usuwa określone zasady dostępu.</span><span class="sxs-lookup"><span data-stu-id="71fe6-113">This command removes a specified access policy.</span></span>

## <span data-ttu-id="71fe6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71fe6-114">PARAMETERS</span></span>

### <span data-ttu-id="71fe6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71fe6-115">-DefaultProfile</span></span>
<span data-ttu-id="71fe6-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="71fe6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71fe6-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="71fe6-117">-EnvironmentName</span></span>
<span data-ttu-id="71fe6-118">Nazwa środowiska szczegółowych informacji szeregu czasowego skojarzonego z określoną grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="71fe6-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="71fe6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71fe6-119">-InputObject</span></span>
<span data-ttu-id="71fe6-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="71fe6-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="71fe6-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="71fe6-121">-Name</span></span>
<span data-ttu-id="71fe6-122">Nazwa zasad dostępu Szczegółowych informacji szeregu czasowego skojarzonych z określonym środowiskiem.</span><span class="sxs-lookup"><span data-stu-id="71fe6-122">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AccessPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71fe6-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71fe6-123">-PassThru</span></span>
<span data-ttu-id="71fe6-124">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="71fe6-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="71fe6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71fe6-125">-ResourceGroupName</span></span>
<span data-ttu-id="71fe6-126">Nazwa grupy usługi Azure Resource.</span><span class="sxs-lookup"><span data-stu-id="71fe6-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="71fe6-127">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="71fe6-127">-SubscriptionId</span></span>
<span data-ttu-id="71fe6-128">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="71fe6-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="71fe6-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="71fe6-129">-Confirm</span></span>
<span data-ttu-id="71fe6-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="71fe6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71fe6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71fe6-131">-WhatIf</span></span>
<span data-ttu-id="71fe6-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71fe6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71fe6-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="71fe6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71fe6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71fe6-134">CommonParameters</span></span>
<span data-ttu-id="71fe6-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71fe6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71fe6-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71fe6-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71fe6-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="71fe6-137">INPUTS</span></span>

### <span data-ttu-id="71fe6-138">Microsoft.Azure.PowerShell.Cmdlet.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="71fe6-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="71fe6-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="71fe6-139">OUTPUTS</span></span>

### <span data-ttu-id="71fe6-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="71fe6-140">System.Boolean</span></span>

## <span data-ttu-id="71fe6-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="71fe6-141">NOTES</span></span>

<span data-ttu-id="71fe6-142">ALIASY</span><span class="sxs-lookup"><span data-stu-id="71fe6-142">ALIASES</span></span>

<span data-ttu-id="71fe6-143">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="71fe6-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="71fe6-144">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="71fe6-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="71fe6-145">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="71fe6-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="71fe6-146">INPUTOBJECT: <ITimeSeriesInsightsIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="71fe6-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="71fe6-147">`[AccessPolicyName <String>]`: nazwa zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="71fe6-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="71fe6-148">`[EnvironmentName <String>]`: nazwa środowiska</span><span class="sxs-lookup"><span data-stu-id="71fe6-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="71fe6-149">`[EventSourceName <String>]`: nazwa źródła zdarzeń Szczegółowych informacji szeregu czasowego skojarzonego z określonym środowiskiem.</span><span class="sxs-lookup"><span data-stu-id="71fe6-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="71fe6-150">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="71fe6-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="71fe6-151">`[ReferenceDataSetName <String>]`: nazwa zestawu danych odwołania.</span><span class="sxs-lookup"><span data-stu-id="71fe6-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="71fe6-152">`[ResourceGroupName <String>]`: nazwa grupy usługi Azure Resource.</span><span class="sxs-lookup"><span data-stu-id="71fe6-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="71fe6-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span><span class="sxs-lookup"><span data-stu-id="71fe6-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="71fe6-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="71fe6-154">RELATED LINKS</span></span>

