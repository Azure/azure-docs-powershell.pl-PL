---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 56173c8ca384c817912395a536583fb26e9dfa76
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219684"
---
# <span data-ttu-id="28f32-101">Remove-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="28f32-101">Remove-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="28f32-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="28f32-102">SYNOPSIS</span></span>
<span data-ttu-id="28f32-103">Usuwa zestaw danych źródłowych o określonej nazwie w określonej subskrypcji, grupie zasobów i środowisku.</span><span class="sxs-lookup"><span data-stu-id="28f32-103">Deletes the reference data set with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="28f32-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="28f32-104">SYNTAX</span></span>

### <span data-ttu-id="28f32-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="28f32-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="28f32-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="28f32-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity>
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="28f32-107">Opis</span><span class="sxs-lookup"><span data-stu-id="28f32-107">DESCRIPTION</span></span>
<span data-ttu-id="28f32-108">Usuwa zestaw danych źródłowych o określonej nazwie w określonej subskrypcji, grupie zasobów i środowisku.</span><span class="sxs-lookup"><span data-stu-id="28f32-108">Deletes the reference data set with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="28f32-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="28f32-109">EXAMPLES</span></span>

### <span data-ttu-id="28f32-110">Przykład 1: usuwanie określonego zestawu danych źródłowych według nazwy</span><span class="sxs-lookup"><span data-stu-id="28f32-110">Example 1: Remove a specified reference data set by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup

```

<span data-ttu-id="28f32-111">To polecenie umożliwia usunięcie określonego zestawu danych referencyjnych.</span><span class="sxs-lookup"><span data-stu-id="28f32-111">This command removes a specified reference data set.</span></span>

### <span data-ttu-id="28f32-112">Przykład 2: usuwanie określonych danych referencyjnych ustawionych przez obiekt</span><span class="sxs-lookup"><span data-stu-id="28f32-112">Example 2: Remove a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup
PS C:\> Remove-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds

```

<span data-ttu-id="28f32-113">To polecenie umożliwia usunięcie określonego zestawu danych referencyjnych.</span><span class="sxs-lookup"><span data-stu-id="28f32-113">This command removes a specified reference data set.</span></span>

## <span data-ttu-id="28f32-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="28f32-114">PARAMETERS</span></span>

### <span data-ttu-id="28f32-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28f32-115">-DefaultProfile</span></span>
<span data-ttu-id="28f32-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="28f32-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28f32-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="28f32-117">-EnvironmentName</span></span>
<span data-ttu-id="28f32-118">Nazwa środowiska informacji o serii czasowej skojarzonego z określoną grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="28f32-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="28f32-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="28f32-119">-InputObject</span></span>
<span data-ttu-id="28f32-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="28f32-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="28f32-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="28f32-121">-Name</span></span>
<span data-ttu-id="28f32-122">Nazwa zestawu danych referencyjnych dotyczących szeregu czasowego skojarzonego z określonym środowiskiem.</span><span class="sxs-lookup"><span data-stu-id="28f32-122">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

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

### <span data-ttu-id="28f32-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="28f32-123">-PassThru</span></span>
<span data-ttu-id="28f32-124">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="28f32-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="28f32-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28f32-125">-ResourceGroupName</span></span>
<span data-ttu-id="28f32-126">Nazwa grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="28f32-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="28f32-127">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="28f32-127">-SubscriptionId</span></span>
<span data-ttu-id="28f32-128">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="28f32-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="28f32-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="28f32-129">-Confirm</span></span>
<span data-ttu-id="28f32-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28f32-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28f32-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28f32-131">-WhatIf</span></span>
<span data-ttu-id="28f32-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28f32-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28f32-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="28f32-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28f32-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28f32-134">CommonParameters</span></span>
<span data-ttu-id="28f32-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28f32-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28f32-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28f32-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28f32-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="28f32-137">INPUTS</span></span>

### <span data-ttu-id="28f32-138">Microsoft. Azure. PowerShell. polecenia. TimeSeriesInsights. models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="28f32-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="28f32-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="28f32-139">OUTPUTS</span></span>

### <span data-ttu-id="28f32-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="28f32-140">System.Boolean</span></span>

## <span data-ttu-id="28f32-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="28f32-141">NOTES</span></span>

<span data-ttu-id="28f32-142">PISUJE</span><span class="sxs-lookup"><span data-stu-id="28f32-142">ALIASES</span></span>

<span data-ttu-id="28f32-143">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="28f32-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="28f32-144">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="28f32-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="28f32-145">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="28f32-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="28f32-146">INPUTobject <ITimeSeriesInsightsIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="28f32-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="28f32-147">`[AccessPolicyName <String>]`: Nazwa zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="28f32-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="28f32-148">`[EnvironmentName <String>]`: Nazwa środowiska</span><span class="sxs-lookup"><span data-stu-id="28f32-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="28f32-149">`[EventSourceName <String>]`: Nazwa źródła zdarzeń szczegółowych informacji o seriach czasowych skojarzonego z określonym środowiskiem.</span><span class="sxs-lookup"><span data-stu-id="28f32-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="28f32-150">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="28f32-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="28f32-151">`[ReferenceDataSetName <String>]`: Nazwa zestawu danych referencyjnych.</span><span class="sxs-lookup"><span data-stu-id="28f32-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="28f32-152">`[ResourceGroupName <String>]`: Nazwa grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="28f32-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="28f32-153">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="28f32-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="28f32-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="28f32-154">RELATED LINKS</span></span>

