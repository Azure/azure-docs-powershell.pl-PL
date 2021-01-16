---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 7f647da2543a4675dad53f88e2494aa7f6c39419
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338941"
---
# <span data-ttu-id="a6b26-101">Remove-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="a6b26-101">Remove-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="a6b26-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a6b26-102">SYNOPSIS</span></span>
<span data-ttu-id="a6b26-103">Usuwa źródło zdarzeń o określonej nazwie w określonej subskrypcji, grupie zasobów i środowisku.</span><span class="sxs-lookup"><span data-stu-id="a6b26-103">Deletes the event source with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="a6b26-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a6b26-104">SYNTAX</span></span>

### <span data-ttu-id="a6b26-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="a6b26-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a6b26-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a6b26-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a6b26-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a6b26-107">DESCRIPTION</span></span>
<span data-ttu-id="a6b26-108">Usuwa źródło zdarzeń o określonej nazwie w określonej subskrypcji, grupie zasobów i środowisku.</span><span class="sxs-lookup"><span data-stu-id="a6b26-108">Deletes the event source with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="a6b26-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a6b26-109">EXAMPLES</span></span>

### <span data-ttu-id="a6b26-110">Przykład 1. Usuń określone źródło zdarzeń według nazwy</span><span class="sxs-lookup"><span data-stu-id="a6b26-110">Example 1: Remove a specified event source by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -Name iots001 -ResourceGroupName testgroup

```

<span data-ttu-id="a6b26-111">Spowoduje to usunięcie określonego źródła zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="a6b26-111">This removes a specific event source.</span></span>

### <span data-ttu-id="a6b26-112">Przykład 2: usuwanie określonego źródła zdarzeń przez obiekt</span><span class="sxs-lookup"><span data-stu-id="a6b26-112">Example 2: Remove a specified event source by object</span></span>
```powershell
PS C:\> $es = Get-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name iots001
PS C:\> Remove-AzTimeSeriesInsightsEventSource -InputObject $es

```

<span data-ttu-id="a6b26-113">Spowoduje to usunięcie określonego źródła zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="a6b26-113">This removes a specific event source.</span></span>

## <span data-ttu-id="a6b26-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a6b26-114">PARAMETERS</span></span>

### <span data-ttu-id="a6b26-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6b26-115">-DefaultProfile</span></span>
<span data-ttu-id="a6b26-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a6b26-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6b26-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="a6b26-117">-EnvironmentName</span></span>
<span data-ttu-id="a6b26-118">Nazwa środowiska informacji o serii czasowej skojarzonego z określoną grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="a6b26-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="a6b26-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a6b26-119">-InputObject</span></span>
<span data-ttu-id="a6b26-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="a6b26-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a6b26-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a6b26-121">-Name</span></span>
<span data-ttu-id="a6b26-122">Nazwa źródła zdarzeń szczegółowych informacji o seriach czasowych skojarzonego z określonym środowiskiem.</span><span class="sxs-lookup"><span data-stu-id="a6b26-122">The name of the Time Series Insights event source associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: EventSourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6b26-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6b26-123">-PassThru</span></span>
<span data-ttu-id="a6b26-124">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="a6b26-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a6b26-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6b26-125">-ResourceGroupName</span></span>
<span data-ttu-id="a6b26-126">Nazwa grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a6b26-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="a6b26-127">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="a6b26-127">-SubscriptionId</span></span>
<span data-ttu-id="a6b26-128">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a6b26-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="a6b26-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a6b26-129">-Confirm</span></span>
<span data-ttu-id="a6b26-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6b26-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6b26-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6b26-131">-WhatIf</span></span>
<span data-ttu-id="a6b26-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6b26-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6b26-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a6b26-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6b26-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6b26-134">CommonParameters</span></span>
<span data-ttu-id="a6b26-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6b26-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6b26-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a6b26-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6b26-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a6b26-137">INPUTS</span></span>

### <span data-ttu-id="a6b26-138">Microsoft. Azure. PowerShell. polecenia. TimeSeriesInsights. models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="a6b26-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="a6b26-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a6b26-139">OUTPUTS</span></span>

### <span data-ttu-id="a6b26-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a6b26-140">System.Boolean</span></span>

## <span data-ttu-id="a6b26-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a6b26-141">NOTES</span></span>

<span data-ttu-id="a6b26-142">PISUJE</span><span class="sxs-lookup"><span data-stu-id="a6b26-142">ALIASES</span></span>

<span data-ttu-id="a6b26-143">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a6b26-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a6b26-144">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="a6b26-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a6b26-145">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a6b26-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a6b26-146">INPUTobject <ITimeSeriesInsightsIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="a6b26-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a6b26-147">`[AccessPolicyName <String>]`: Nazwa zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="a6b26-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="a6b26-148">`[EnvironmentName <String>]`: Nazwa środowiska</span><span class="sxs-lookup"><span data-stu-id="a6b26-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="a6b26-149">`[EventSourceName <String>]`: Nazwa źródła zdarzeń szczegółowych informacji o seriach czasowych skojarzonego z określonym środowiskiem.</span><span class="sxs-lookup"><span data-stu-id="a6b26-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="a6b26-150">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="a6b26-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a6b26-151">`[ReferenceDataSetName <String>]`: Nazwa zestawu danych referencyjnych.</span><span class="sxs-lookup"><span data-stu-id="a6b26-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="a6b26-152">`[ResourceGroupName <String>]`: Nazwa grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a6b26-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="a6b26-153">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a6b26-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="a6b26-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a6b26-154">RELATED LINKS</span></span>

