---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: ed4a3e7c9b53bd481d4d30c4f6a555d8f42c44fd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182611"
---
# <span data-ttu-id="928e5-101">Get-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="928e5-101">Get-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="928e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="928e5-102">SYNOPSIS</span></span>
<span data-ttu-id="928e5-103">Pobiera zestaw danych odwołania o określonej nazwie w określonym środowisku.</span><span class="sxs-lookup"><span data-stu-id="928e5-103">Gets the reference data set with the specified name in the specified environment.</span></span>

## <span data-ttu-id="928e5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="928e5-104">SYNTAX</span></span>

### <span data-ttu-id="928e5-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="928e5-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="928e5-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="928e5-106">Get</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="928e5-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="928e5-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity>
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="928e5-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="928e5-108">DESCRIPTION</span></span>
<span data-ttu-id="928e5-109">Pobiera zestaw danych odwołania o określonej nazwie w określonym środowisku.</span><span class="sxs-lookup"><span data-stu-id="928e5-109">Gets the reference data set with the specified name in the specified environment.</span></span>

## <span data-ttu-id="928e5-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="928e5-110">EXAMPLES</span></span>

### <span data-ttu-id="928e5-111">Przykład 1. Lista wszystkich zestawów danych referencyjnych w określonym środowisku</span><span class="sxs-lookup"><span data-stu-id="928e5-111">Example 1: List all reference data sets under the specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
eastus   dstest002 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="928e5-112">To polecenie wyświetla listę wszystkich zestawów danych odwoływać się w określonym środowisku.</span><span class="sxs-lookup"><span data-stu-id="928e5-112">This command lists all reference data sets under the specified environment.</span></span>

### <span data-ttu-id="928e5-113">Przykład 2. Uzyskiwanie określonego zestawu danych odwołania według nazwy</span><span class="sxs-lookup"><span data-stu-id="928e5-113">Example 2: Get a specified reference data set by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup -ReferenceDataSetName dstest001

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="928e5-114">To polecenie otrzymuje określony zestaw danych referencyjnych.</span><span class="sxs-lookup"><span data-stu-id="928e5-114">This command gets a specified reference data set.</span></span>

### <span data-ttu-id="928e5-115">Przykład 3. Uzyskiwanie określonego zestawu danych odwołania według obiektu</span><span class="sxs-lookup"><span data-stu-id="928e5-115">Example 3: Get a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -ResourceGroupName tsi-test-i01k5l -EnvironmentName tsi-envv8u56x -Name tsirdsqwufij 
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds

Location Name         Type
-------- ----         ----
eastus2  tsirdsqwufij Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="928e5-116">To polecenie otrzymuje określony zestaw danych odwołania.</span><span class="sxs-lookup"><span data-stu-id="928e5-116">This command gets a specified reference data set.</span></span>

## <span data-ttu-id="928e5-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="928e5-117">PARAMETERS</span></span>

### <span data-ttu-id="928e5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="928e5-118">-DefaultProfile</span></span>
<span data-ttu-id="928e5-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="928e5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="928e5-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="928e5-120">-EnvironmentName</span></span>
<span data-ttu-id="928e5-121">Nazwa środowiska szczegółowych informacji szeregu czasowego skojarzonego z określoną grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="928e5-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="928e5-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="928e5-122">-InputObject</span></span>
<span data-ttu-id="928e5-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="928e5-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="928e5-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="928e5-124">-Name</span></span>
<span data-ttu-id="928e5-125">Nazwa szczegółowych informacji z serii czasowej odwołuje się do zestawu danych skojarzonego z określonym środowiskiem.</span><span class="sxs-lookup"><span data-stu-id="928e5-125">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

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

### <span data-ttu-id="928e5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="928e5-126">-ResourceGroupName</span></span>
<span data-ttu-id="928e5-127">Nazwa grupy usługi Azure Resource.</span><span class="sxs-lookup"><span data-stu-id="928e5-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="928e5-128">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="928e5-128">-SubscriptionId</span></span>
<span data-ttu-id="928e5-129">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="928e5-129">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="928e5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="928e5-130">CommonParameters</span></span>
<span data-ttu-id="928e5-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="928e5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="928e5-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="928e5-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="928e5-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="928e5-133">INPUTS</span></span>

### <span data-ttu-id="928e5-134">Microsoft.Azure.PowerShell.Cmdlet.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="928e5-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="928e5-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="928e5-135">OUTPUTS</span></span>

### <span data-ttu-id="928e5-136">Microsoft.Azure.PowerShell.Cmdlet.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span><span class="sxs-lookup"><span data-stu-id="928e5-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="928e5-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="928e5-137">NOTES</span></span>

<span data-ttu-id="928e5-138">ALIASY</span><span class="sxs-lookup"><span data-stu-id="928e5-138">ALIASES</span></span>

<span data-ttu-id="928e5-139">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="928e5-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="928e5-140">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="928e5-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="928e5-141">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="928e5-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="928e5-142">INPUTOBJECT: <ITimeSeriesInsightsIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="928e5-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="928e5-143">`[AccessPolicyName <String>]`: nazwa zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="928e5-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="928e5-144">`[EnvironmentName <String>]`: nazwa środowiska</span><span class="sxs-lookup"><span data-stu-id="928e5-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="928e5-145">`[EventSourceName <String>]`: nazwa źródła zdarzeń Szczegółowych informacji szeregu czasowego skojarzonego z określonym środowiskiem.</span><span class="sxs-lookup"><span data-stu-id="928e5-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="928e5-146">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="928e5-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="928e5-147">`[ReferenceDataSetName <String>]`: nazwa zestawu danych odwołania.</span><span class="sxs-lookup"><span data-stu-id="928e5-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="928e5-148">`[ResourceGroupName <String>]`: nazwa grupy usługi Azure Resource.</span><span class="sxs-lookup"><span data-stu-id="928e5-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="928e5-149">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="928e5-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="928e5-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="928e5-150">RELATED LINKS</span></span>

