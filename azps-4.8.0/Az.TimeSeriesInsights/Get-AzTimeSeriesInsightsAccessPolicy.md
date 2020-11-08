---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: c7d8f46f42b1b42e4831540f5c68706c61ff78cf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063805"
---
# <span data-ttu-id="35a80-101">Get-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="35a80-101">Get-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="35a80-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="35a80-102">SYNOPSIS</span></span>
<span data-ttu-id="35a80-103">Pobiera zasady dostępu o określonej nazwie w określonym środowisku.</span><span class="sxs-lookup"><span data-stu-id="35a80-103">Gets the access policy with the specified name in the specified environment.</span></span>

## <span data-ttu-id="35a80-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="35a80-104">SYNTAX</span></span>

### <span data-ttu-id="35a80-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="35a80-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="35a80-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="35a80-106">Get</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="35a80-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="35a80-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="35a80-108">Opis</span><span class="sxs-lookup"><span data-stu-id="35a80-108">DESCRIPTION</span></span>
<span data-ttu-id="35a80-109">Pobiera zasady dostępu o określonej nazwie w określonym środowisku.</span><span class="sxs-lookup"><span data-stu-id="35a80-109">Gets the access policy with the specified name in the specified environment.</span></span>

## <span data-ttu-id="35a80-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="35a80-110">EXAMPLES</span></span>

### <span data-ttu-id="35a80-111">Przykład 1: wyświetlanie wszystkich zasad dostępu w określonym środowisku</span><span class="sxs-lookup"><span data-stu-id="35a80-111">Example 1: List all access policies under a specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
policy002 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="35a80-112">To polecenie wyświetla listę wszystkich zasad dostępu w określonym środowisku.</span><span class="sxs-lookup"><span data-stu-id="35a80-112">This command lists all access policies under a specified environment.</span></span>

### <span data-ttu-id="35a80-113">Przykład 2: uzyskiwanie określonych zasad dostępu według nazwy</span><span class="sxs-lookup"><span data-stu-id="35a80-113">Example 2: Get a specified access policy by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name policy001

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="35a80-114">To polecenie pobiera określone zasady dostępu.</span><span class="sxs-lookup"><span data-stu-id="35a80-114">This command gets a specified access policy.</span></span>

### <span data-ttu-id="35a80-115">Przykład 3: uzyskiwanie określonych zasad dostępu według obiektów</span><span class="sxs-lookup"><span data-stu-id="35a80-115">Example 3: Get a specified access policy by object</span></span>
```powershell
PS C:\>$ap = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsi-envv8u56x -ResourceGroupName tsi-test-i01k5l -Name tsi-apilgj5y 
PS C:\>Get-AzTimeSeriesInsightsAccessPolicy -InputObject $ap

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="35a80-116">To polecenie pobiera określone zasady dostępu.</span><span class="sxs-lookup"><span data-stu-id="35a80-116">This command gets a specified access policy.</span></span>

## <span data-ttu-id="35a80-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="35a80-117">PARAMETERS</span></span>

### <span data-ttu-id="35a80-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35a80-118">-DefaultProfile</span></span>
<span data-ttu-id="35a80-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="35a80-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35a80-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="35a80-120">-EnvironmentName</span></span>
<span data-ttu-id="35a80-121">Nazwa środowiska informacji o serii czasowej skojarzonego z określoną grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="35a80-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="35a80-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="35a80-122">-InputObject</span></span>
<span data-ttu-id="35a80-123">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="35a80-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="35a80-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="35a80-124">-Name</span></span>
<span data-ttu-id="35a80-125">Nazwa zasad dostępu usługi Insights w ramach sekwencji czasu skojarzonych z określonym środowiskiem.</span><span class="sxs-lookup"><span data-stu-id="35a80-125">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

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

### <span data-ttu-id="35a80-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35a80-126">-ResourceGroupName</span></span>
<span data-ttu-id="35a80-127">Nazwa grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="35a80-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="35a80-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="35a80-128">-SubscriptionId</span></span>
<span data-ttu-id="35a80-129">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="35a80-129">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="35a80-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35a80-130">CommonParameters</span></span>
<span data-ttu-id="35a80-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35a80-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35a80-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35a80-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35a80-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="35a80-133">INPUTS</span></span>

### <span data-ttu-id="35a80-134">Microsoft. Azure. PowerShell. polecenia. TimeSeriesInsights. models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="35a80-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="35a80-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="35a80-135">OUTPUTS</span></span>

### <span data-ttu-id="35a80-136">Microsoft. Azure. PowerShell. polecenia. TimeSeriesInsights. models. Api20200515. IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="35a80-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="35a80-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="35a80-137">NOTES</span></span>

<span data-ttu-id="35a80-138">PISUJE</span><span class="sxs-lookup"><span data-stu-id="35a80-138">ALIASES</span></span>

<span data-ttu-id="35a80-139">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="35a80-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="35a80-140">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="35a80-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="35a80-141">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="35a80-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="35a80-142">INPUTobject <ITimeSeriesInsightsIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="35a80-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="35a80-143">`[AccessPolicyName <String>]`: Nazwa zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="35a80-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="35a80-144">`[EnvironmentName <String>]`: Nazwa środowiska</span><span class="sxs-lookup"><span data-stu-id="35a80-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="35a80-145">`[EventSourceName <String>]`: Nazwa źródła zdarzeń szczegółowych informacji o seriach czasowych skojarzonego z określonym środowiskiem.</span><span class="sxs-lookup"><span data-stu-id="35a80-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="35a80-146">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="35a80-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="35a80-147">`[ReferenceDataSetName <String>]`: Nazwa zestawu danych referencyjnych.</span><span class="sxs-lookup"><span data-stu-id="35a80-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="35a80-148">`[ResourceGroupName <String>]`: Nazwa grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="35a80-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="35a80-149">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="35a80-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="35a80-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="35a80-150">RELATED LINKS</span></span>

