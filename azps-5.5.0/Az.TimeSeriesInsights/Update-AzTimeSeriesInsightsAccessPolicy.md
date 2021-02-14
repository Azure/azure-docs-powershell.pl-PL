---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: e776b0e11fedd0b2903135b9b640c3b704706027
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197275"
---
# <span data-ttu-id="13c1b-101">Update-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="13c1b-101">Update-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="13c1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13c1b-102">SYNOPSIS</span></span>
<span data-ttu-id="13c1b-103">Aktualizuje zasady dostępu o określonej nazwie w określonej subskrypcji, grupie zasobów i środowisku.</span><span class="sxs-lookup"><span data-stu-id="13c1b-103">Updates the access policy with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="13c1b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="13c1b-104">SYNTAX</span></span>

### <span data-ttu-id="13c1b-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="13c1b-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-Role <AccessPolicyRole[]>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="13c1b-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="13c1b-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity> [-Description <String>]
 [-Role <AccessPolicyRole[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="13c1b-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="13c1b-107">DESCRIPTION</span></span>
<span data-ttu-id="13c1b-108">Aktualizuje zasady dostępu o określonej nazwie w określonej subskrypcji, grupie zasobów i środowisku.</span><span class="sxs-lookup"><span data-stu-id="13c1b-108">Updates the access policy with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="13c1b-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="13c1b-109">EXAMPLES</span></span>

### <span data-ttu-id="13c1b-110">Przykład 1. Aktualizowanie określonych zasad dostępu według nazwy</span><span class="sxs-lookup"><span data-stu-id="13c1b-110">Example 1: Update a specified access policy by name</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup -Role Contributor,Reader

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="13c1b-111">To polecenie aktualizuje określone zasady dostępu.</span><span class="sxs-lookup"><span data-stu-id="13c1b-111">This command updates a specified access policy.</span></span>

### <span data-ttu-id="13c1b-112">Przykład 2. Aktualizowanie określonych zasad dostępu według obiektu</span><span class="sxs-lookup"><span data-stu-id="13c1b-112">Example 2: Update a specified access policy by object</span></span>
```powershell
PS C:\> $policy = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name policy001
PS C:\> Update-AzTimeSeriesInsightsAccessPolicy -InputObject $policy -Role Contributor

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="13c1b-113">To polecenie aktualizuje określone zasady dostępu.</span><span class="sxs-lookup"><span data-stu-id="13c1b-113">This command updates a specified access policy.</span></span>

## <span data-ttu-id="13c1b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13c1b-114">PARAMETERS</span></span>

### <span data-ttu-id="13c1b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13c1b-115">-DefaultProfile</span></span>
<span data-ttu-id="13c1b-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="13c1b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13c1b-117">— Opis</span><span class="sxs-lookup"><span data-stu-id="13c1b-117">-Description</span></span>
<span data-ttu-id="13c1b-118">Opis zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="13c1b-118">An description of the access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13c1b-119">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="13c1b-119">-EnvironmentName</span></span>
<span data-ttu-id="13c1b-120">Nazwa środowiska szczegółowych informacji szeregu czasowego skojarzonego z określoną grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="13c1b-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="13c1b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13c1b-121">-InputObject</span></span>
<span data-ttu-id="13c1b-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="13c1b-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="13c1b-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="13c1b-123">-Name</span></span>
<span data-ttu-id="13c1b-124">Nazwa zasad dostępu Szczegółowych informacji szeregu czasowego skojarzonych z określonym środowiskiem.</span><span class="sxs-lookup"><span data-stu-id="13c1b-124">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: AccessPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13c1b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13c1b-125">-ResourceGroupName</span></span>
<span data-ttu-id="13c1b-126">Nazwa grupy usługi Azure Resource.</span><span class="sxs-lookup"><span data-stu-id="13c1b-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="13c1b-127">— Rola</span><span class="sxs-lookup"><span data-stu-id="13c1b-127">-Role</span></span>
<span data-ttu-id="13c1b-128">Lista ról przypisanych do środowiska przez podmiot zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="13c1b-128">The list of roles the principal is assigned on the environment.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.AccessPolicyRole[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13c1b-129">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="13c1b-129">-SubscriptionId</span></span>
<span data-ttu-id="13c1b-130">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="13c1b-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="13c1b-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="13c1b-131">-Confirm</span></span>
<span data-ttu-id="13c1b-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="13c1b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13c1b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13c1b-133">-WhatIf</span></span>
<span data-ttu-id="13c1b-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13c1b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13c1b-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="13c1b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13c1b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13c1b-136">CommonParameters</span></span>
<span data-ttu-id="13c1b-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13c1b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13c1b-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="13c1b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13c1b-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13c1b-139">INPUTS</span></span>

### <span data-ttu-id="13c1b-140">Microsoft.Azure.PowerShell.Cmdlet.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="13c1b-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="13c1b-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13c1b-141">OUTPUTS</span></span>

### <span data-ttu-id="13c1b-142">Microsoft.Azure.PowerShell.Cmdlet.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="13c1b-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="13c1b-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="13c1b-143">NOTES</span></span>

<span data-ttu-id="13c1b-144">ALIASY</span><span class="sxs-lookup"><span data-stu-id="13c1b-144">ALIASES</span></span>

<span data-ttu-id="13c1b-145">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="13c1b-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="13c1b-146">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="13c1b-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="13c1b-147">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="13c1b-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="13c1b-148">INPUTOBJECT: <ITimeSeriesInsightsIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="13c1b-148">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="13c1b-149">`[AccessPolicyName <String>]`: nazwa zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="13c1b-149">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="13c1b-150">`[EnvironmentName <String>]`: nazwa środowiska</span><span class="sxs-lookup"><span data-stu-id="13c1b-150">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="13c1b-151">`[EventSourceName <String>]`: nazwa źródła zdarzeń Szczegółowych informacji szeregu czasowego skojarzonego z określonym środowiskiem.</span><span class="sxs-lookup"><span data-stu-id="13c1b-151">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="13c1b-152">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="13c1b-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="13c1b-153">`[ReferenceDataSetName <String>]`: nazwa zestawu danych odwołania.</span><span class="sxs-lookup"><span data-stu-id="13c1b-153">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="13c1b-154">`[ResourceGroupName <String>]`: nazwa grupy azure resource.</span><span class="sxs-lookup"><span data-stu-id="13c1b-154">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="13c1b-155">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="13c1b-155">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="13c1b-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="13c1b-156">RELATED LINKS</span></span>

