---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 7dbced00ee2e39c536765bd16a19fbe7a66e291b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219682"
---
# <span data-ttu-id="1790a-101">Update-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="1790a-101">Update-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="1790a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1790a-102">SYNOPSIS</span></span>
<span data-ttu-id="1790a-103">Aktualizuje zestaw danych źródłowych o określonej nazwie w określonej subskrypcji, grupie zasobów i środowisku.</span><span class="sxs-lookup"><span data-stu-id="1790a-103">Updates the reference data set with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="1790a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1790a-104">SYNTAX</span></span>

### <span data-ttu-id="1790a-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1790a-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1790a-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="1790a-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1790a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1790a-107">DESCRIPTION</span></span>
<span data-ttu-id="1790a-108">Aktualizuje zestaw danych źródłowych o określonej nazwie w określonej subskrypcji, grupie zasobów i środowisku.</span><span class="sxs-lookup"><span data-stu-id="1790a-108">Updates the reference data set with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="1790a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1790a-109">EXAMPLES</span></span>

### <span data-ttu-id="1790a-110">Przykład 1: aktualizowanie określonego zestawu danych referencyjnych według nazwy</span><span class="sxs-lookup"><span data-stu-id="1790a-110">Example 1: Update a specified reference data set by name</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup -Tag @{"tstg"="lb001"}

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="1790a-111">To polecenie umożliwia zaktualizowanie określonego zestawu danych referencyjnych.</span><span class="sxs-lookup"><span data-stu-id="1790a-111">This command updates a specified reference data set.</span></span>

### <span data-ttu-id="1790a-112">Przykład 2: aktualizowanie określonych danych referencyjnych ustawionych według obiektów</span><span class="sxs-lookup"><span data-stu-id="1790a-112">Example 2: Update a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup -ReferenceDataSetName dstest001
PS C:\> Update-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds -Tag @{"tstg"="lb001"}

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="1790a-113">To polecenie umożliwia zaktualizowanie określonego zestawu danych referencyjnych.</span><span class="sxs-lookup"><span data-stu-id="1790a-113">This command updates a specified reference data set.</span></span>

## <span data-ttu-id="1790a-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1790a-114">PARAMETERS</span></span>

### <span data-ttu-id="1790a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1790a-115">-DefaultProfile</span></span>
<span data-ttu-id="1790a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1790a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1790a-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="1790a-117">-EnvironmentName</span></span>
<span data-ttu-id="1790a-118">Nazwa środowiska informacji o serii czasowej skojarzonego z określoną grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="1790a-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="1790a-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1790a-119">-InputObject</span></span>
<span data-ttu-id="1790a-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="1790a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1790a-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1790a-121">-Name</span></span>
<span data-ttu-id="1790a-122">Nazwa zestawu danych referencyjnych dotyczących szeregu czasowego skojarzonego z określonym środowiskiem.</span><span class="sxs-lookup"><span data-stu-id="1790a-122">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

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

### <span data-ttu-id="1790a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1790a-123">-ResourceGroupName</span></span>
<span data-ttu-id="1790a-124">Nazwa grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1790a-124">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="1790a-125">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="1790a-125">-SubscriptionId</span></span>
<span data-ttu-id="1790a-126">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1790a-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="1790a-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="1790a-127">-Tag</span></span>
<span data-ttu-id="1790a-128">Pary klucz-wartość dodatkowych właściwości dla zestawu danych źródłowych.</span><span class="sxs-lookup"><span data-stu-id="1790a-128">Key-value pairs of additional properties for the reference data set.</span></span>

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

### <span data-ttu-id="1790a-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1790a-129">-Confirm</span></span>
<span data-ttu-id="1790a-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1790a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1790a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1790a-131">-WhatIf</span></span>
<span data-ttu-id="1790a-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1790a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1790a-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1790a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1790a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1790a-134">CommonParameters</span></span>
<span data-ttu-id="1790a-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1790a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1790a-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1790a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1790a-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1790a-137">INPUTS</span></span>

### <span data-ttu-id="1790a-138">Microsoft. Azure. PowerShell. polecenia. TimeSeriesInsights. models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="1790a-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="1790a-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1790a-139">OUTPUTS</span></span>

### <span data-ttu-id="1790a-140">Microsoft. Azure. PowerShell. polecenia. TimeSeriesInsights. models. Api20200515. IReferenceDataSetResource</span><span class="sxs-lookup"><span data-stu-id="1790a-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="1790a-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1790a-141">NOTES</span></span>

<span data-ttu-id="1790a-142">PISUJE</span><span class="sxs-lookup"><span data-stu-id="1790a-142">ALIASES</span></span>

<span data-ttu-id="1790a-143">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1790a-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1790a-144">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="1790a-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1790a-145">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1790a-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1790a-146">INPUTobject <ITimeSeriesInsightsIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="1790a-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1790a-147">`[AccessPolicyName <String>]`: Nazwa zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="1790a-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="1790a-148">`[EnvironmentName <String>]`: Nazwa środowiska</span><span class="sxs-lookup"><span data-stu-id="1790a-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="1790a-149">`[EventSourceName <String>]`: Nazwa źródła zdarzeń szczegółowych informacji o seriach czasowych skojarzonego z określonym środowiskiem.</span><span class="sxs-lookup"><span data-stu-id="1790a-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="1790a-150">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="1790a-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1790a-151">`[ReferenceDataSetName <String>]`: Nazwa zestawu danych referencyjnych.</span><span class="sxs-lookup"><span data-stu-id="1790a-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="1790a-152">`[ResourceGroupName <String>]`: Nazwa grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1790a-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="1790a-153">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1790a-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="1790a-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1790a-154">RELATED LINKS</span></span>

