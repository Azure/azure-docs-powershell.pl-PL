---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: c7d8f46f42b1b42e4831540f5c68706c61ff78cf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182619"
---
# <span data-ttu-id="b0909-101">Get-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b0909-101">Get-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="b0909-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0909-102">SYNOPSIS</span></span>
<span data-ttu-id="b0909-103">Pobiera zasady dostępu o określonej nazwie w określonym środowisku.</span><span class="sxs-lookup"><span data-stu-id="b0909-103">Gets the access policy with the specified name in the specified environment.</span></span>

## <span data-ttu-id="b0909-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b0909-104">SYNTAX</span></span>

### <span data-ttu-id="b0909-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="b0909-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b0909-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="b0909-106">Get</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b0909-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b0909-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b0909-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="b0909-108">DESCRIPTION</span></span>
<span data-ttu-id="b0909-109">Pobiera zasady dostępu o określonej nazwie w określonym środowisku.</span><span class="sxs-lookup"><span data-stu-id="b0909-109">Gets the access policy with the specified name in the specified environment.</span></span>

## <span data-ttu-id="b0909-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b0909-110">EXAMPLES</span></span>

### <span data-ttu-id="b0909-111">Przykład 1. Lista wszystkich zasad dostępu w określonym środowisku</span><span class="sxs-lookup"><span data-stu-id="b0909-111">Example 1: List all access policies under a specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
policy002 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="b0909-112">To polecenie zawiera listę wszystkich zasad dostępu w określonym środowisku.</span><span class="sxs-lookup"><span data-stu-id="b0909-112">This command lists all access policies under a specified environment.</span></span>

### <span data-ttu-id="b0909-113">Przykład 2. Uzyskiwanie określonych zasad dostępu według nazwy</span><span class="sxs-lookup"><span data-stu-id="b0909-113">Example 2: Get a specified access policy by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name policy001

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="b0909-114">To polecenie otrzymuje określone zasady dostępu.</span><span class="sxs-lookup"><span data-stu-id="b0909-114">This command gets a specified access policy.</span></span>

### <span data-ttu-id="b0909-115">Przykład 3. Uzyskiwanie określonych zasad dostępu według obiektu</span><span class="sxs-lookup"><span data-stu-id="b0909-115">Example 3: Get a specified access policy by object</span></span>
```powershell
PS C:\>$ap = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsi-envv8u56x -ResourceGroupName tsi-test-i01k5l -Name tsi-apilgj5y 
PS C:\>Get-AzTimeSeriesInsightsAccessPolicy -InputObject $ap

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="b0909-116">To polecenie otrzymuje określone zasady dostępu.</span><span class="sxs-lookup"><span data-stu-id="b0909-116">This command gets a specified access policy.</span></span>

## <span data-ttu-id="b0909-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0909-117">PARAMETERS</span></span>

### <span data-ttu-id="b0909-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0909-118">-DefaultProfile</span></span>
<span data-ttu-id="b0909-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b0909-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0909-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="b0909-120">-EnvironmentName</span></span>
<span data-ttu-id="b0909-121">Nazwa środowiska szczegółowych informacji szeregu czasowego skojarzonego z określoną grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="b0909-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0909-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0909-122">-InputObject</span></span>
<span data-ttu-id="b0909-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="b0909-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0909-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b0909-124">-Name</span></span>
<span data-ttu-id="b0909-125">Nazwa zasad dostępu Szczegółowych informacji szeregu czasowego skojarzonych z określonym środowiskiem.</span><span class="sxs-lookup"><span data-stu-id="b0909-125">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AccessPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0909-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0909-126">-ResourceGroupName</span></span>
<span data-ttu-id="b0909-127">Nazwa grupy usługi Azure Resource.</span><span class="sxs-lookup"><span data-stu-id="b0909-127">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0909-128">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b0909-128">-SubscriptionId</span></span>
<span data-ttu-id="b0909-129">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b0909-129">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0909-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0909-130">CommonParameters</span></span>
<span data-ttu-id="b0909-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0909-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0909-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0909-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0909-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b0909-133">INPUTS</span></span>

### <span data-ttu-id="b0909-134">Microsoft.Azure.PowerShell.Cmdlet.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="b0909-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="b0909-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b0909-135">OUTPUTS</span></span>

### <span data-ttu-id="b0909-136">Microsoft.Azure.PowerShell.Cmdlet.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="b0909-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="b0909-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b0909-137">NOTES</span></span>

<span data-ttu-id="b0909-138">ALIASY</span><span class="sxs-lookup"><span data-stu-id="b0909-138">ALIASES</span></span>

<span data-ttu-id="b0909-139">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b0909-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b0909-140">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="b0909-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b0909-141">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b0909-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b0909-142">INPUTOBJECT: <ITimeSeriesInsightsIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="b0909-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b0909-143">`[AccessPolicyName <String>]`: nazwa zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="b0909-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="b0909-144">`[EnvironmentName <String>]`: nazwa środowiska</span><span class="sxs-lookup"><span data-stu-id="b0909-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="b0909-145">`[EventSourceName <String>]`: nazwa źródła zdarzeń Szczegółowych informacji szeregu czasowego skojarzonego z określonym środowiskiem.</span><span class="sxs-lookup"><span data-stu-id="b0909-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="b0909-146">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="b0909-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b0909-147">`[ReferenceDataSetName <String>]`: nazwa zestawu danych referencyjnych.</span><span class="sxs-lookup"><span data-stu-id="b0909-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="b0909-148">`[ResourceGroupName <String>]`: nazwa grupy azure resource.</span><span class="sxs-lookup"><span data-stu-id="b0909-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="b0909-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span><span class="sxs-lookup"><span data-stu-id="b0909-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="b0909-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b0909-150">RELATED LINKS</span></span>

