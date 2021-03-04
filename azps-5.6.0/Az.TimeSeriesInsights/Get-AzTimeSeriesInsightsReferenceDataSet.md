---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 1fef5f018791fba9369ce7ab18a4b0c3a2440cc6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950826"
---
# <span data-ttu-id="a85bf-101">Get-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="a85bf-101">Get-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="a85bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a85bf-102">SYNOPSIS</span></span>
<span data-ttu-id="a85bf-103">Pobiera zestaw danych odwołania o określonej nazwie w określonym środowisku.</span><span class="sxs-lookup"><span data-stu-id="a85bf-103">Gets the reference data set with the specified name in the specified environment.</span></span>

## <span data-ttu-id="a85bf-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a85bf-104">SYNTAX</span></span>

### <span data-ttu-id="a85bf-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="a85bf-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a85bf-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="a85bf-106">Get</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a85bf-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a85bf-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity>
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a85bf-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a85bf-108">DESCRIPTION</span></span>
<span data-ttu-id="a85bf-109">Pobiera zestaw danych odwołania o określonej nazwie w określonym środowisku.</span><span class="sxs-lookup"><span data-stu-id="a85bf-109">Gets the reference data set with the specified name in the specified environment.</span></span>

## <span data-ttu-id="a85bf-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a85bf-110">EXAMPLES</span></span>

### <span data-ttu-id="a85bf-111">Przykład 1. Lista wszystkich zestawów danych odwoływać się w określonym środowisku</span><span class="sxs-lookup"><span data-stu-id="a85bf-111">Example 1: List all reference data sets under the specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
eastus   dstest002 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="a85bf-112">To polecenie wyświetla listę wszystkich zestawów danych odwoływać się w określonym środowisku.</span><span class="sxs-lookup"><span data-stu-id="a85bf-112">This command lists all reference data sets under the specified environment.</span></span>

### <span data-ttu-id="a85bf-113">Przykład 2. Uzyskiwanie określonego zestawu danych odwołania według nazwy</span><span class="sxs-lookup"><span data-stu-id="a85bf-113">Example 2: Get a specified reference data set by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup -ReferenceDataSetName dstest001

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="a85bf-114">To polecenie otrzymuje określony zestaw danych referencyjnych.</span><span class="sxs-lookup"><span data-stu-id="a85bf-114">This command gets a specified reference data set.</span></span>

### <span data-ttu-id="a85bf-115">Przykład 3. Uzyskiwanie określonego zestawu danych odwołania według obiektu</span><span class="sxs-lookup"><span data-stu-id="a85bf-115">Example 3: Get a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -ResourceGroupName tsi-test-i01k5l -EnvironmentName tsi-envv8u56x -Name tsirdsqwufij 
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds

Location Name         Type
-------- ----         ----
eastus2  tsirdsqwufij Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="a85bf-116">To polecenie otrzymuje określony zestaw danych referencyjnych.</span><span class="sxs-lookup"><span data-stu-id="a85bf-116">This command gets a specified reference data set.</span></span>

## <span data-ttu-id="a85bf-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a85bf-117">PARAMETERS</span></span>

### <span data-ttu-id="a85bf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a85bf-118">-DefaultProfile</span></span>
<span data-ttu-id="a85bf-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a85bf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a85bf-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="a85bf-120">-EnvironmentName</span></span>
<span data-ttu-id="a85bf-121">Nazwa środowiska szczegółowych informacji szeregu czasowego skojarzonego z określoną grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="a85bf-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="a85bf-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a85bf-122">-InputObject</span></span>
<span data-ttu-id="a85bf-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="a85bf-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a85bf-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a85bf-124">-Name</span></span>
<span data-ttu-id="a85bf-125">Nazwa szczegółowych informacji z serii czasowej odwołuje się do zestawu danych skojarzonego z określonym środowiskiem.</span><span class="sxs-lookup"><span data-stu-id="a85bf-125">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ReferenceDataSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a85bf-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a85bf-126">-ResourceGroupName</span></span>
<span data-ttu-id="a85bf-127">Nazwa grupy usługi Azure Resource.</span><span class="sxs-lookup"><span data-stu-id="a85bf-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="a85bf-128">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a85bf-128">-SubscriptionId</span></span>
<span data-ttu-id="a85bf-129">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a85bf-129">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="a85bf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a85bf-130">CommonParameters</span></span>
<span data-ttu-id="a85bf-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a85bf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a85bf-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a85bf-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a85bf-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a85bf-133">INPUTS</span></span>

### <span data-ttu-id="a85bf-134">Microsoft.Azure.PowerShell.Cmdlet.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="a85bf-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="a85bf-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a85bf-135">OUTPUTS</span></span>

### <span data-ttu-id="a85bf-136">Microsoft.Azure.PowerShell.Cmdlet.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span><span class="sxs-lookup"><span data-stu-id="a85bf-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="a85bf-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a85bf-137">NOTES</span></span>

<span data-ttu-id="a85bf-138">ALIASY</span><span class="sxs-lookup"><span data-stu-id="a85bf-138">ALIASES</span></span>

<span data-ttu-id="a85bf-139">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a85bf-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a85bf-140">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="a85bf-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a85bf-141">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a85bf-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a85bf-142">INPUTOBJECT: <ITimeSeriesInsightsIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="a85bf-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a85bf-143">`[AccessPolicyName <String>]`: nazwa zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="a85bf-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="a85bf-144">`[EnvironmentName <String>]`: nazwa środowiska</span><span class="sxs-lookup"><span data-stu-id="a85bf-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="a85bf-145">`[EventSourceName <String>]`: nazwa źródła zdarzeń Szczegółowych informacji szeregu czasowego skojarzonego z określonym środowiskiem.</span><span class="sxs-lookup"><span data-stu-id="a85bf-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="a85bf-146">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="a85bf-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a85bf-147">`[ReferenceDataSetName <String>]`: nazwa zestawu danych referencyjnych.</span><span class="sxs-lookup"><span data-stu-id="a85bf-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="a85bf-148">`[ResourceGroupName <String>]`: nazwa grupy azure resource.</span><span class="sxs-lookup"><span data-stu-id="a85bf-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="a85bf-149">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a85bf-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="a85bf-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a85bf-150">RELATED LINKS</span></span>

