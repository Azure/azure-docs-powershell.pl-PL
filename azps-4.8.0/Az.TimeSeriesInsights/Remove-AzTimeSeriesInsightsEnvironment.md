---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: 8b56475d2510099b7873fa444a0dc78497aeb729
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222115"
---
# <span data-ttu-id="f2966-101">Remove-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="f2966-101">Remove-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="f2966-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f2966-102">SYNOPSIS</span></span>
<span data-ttu-id="f2966-103">Usuwa środowisko o określonej nazwie w określonej grupie subskrypcji i zasobów.</span><span class="sxs-lookup"><span data-stu-id="f2966-103">Deletes the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="f2966-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f2966-104">SYNTAX</span></span>

### <span data-ttu-id="f2966-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="f2966-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f2966-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f2966-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f2966-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f2966-107">DESCRIPTION</span></span>
<span data-ttu-id="f2966-108">Usuwa środowisko o określonej nazwie w określonej grupie subskrypcji i zasobów.</span><span class="sxs-lookup"><span data-stu-id="f2966-108">Deletes the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="f2966-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f2966-109">EXAMPLES</span></span>

### <span data-ttu-id="f2966-110">Przykład 1: usuwanie środowiska informacji o seriach czasu według nazwy</span><span class="sxs-lookup"><span data-stu-id="f2966-110">Example 1: Remove a time series insights environment by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsill

```

<span data-ttu-id="f2966-111">To polecenie usuwa środowisko informacji o seriach czasowych.</span><span class="sxs-lookup"><span data-stu-id="f2966-111">This command removes a time series insights environment.</span></span>

### <span data-ttu-id="f2966-112">Przykład 2: usuwanie środowiska informacji o seriach czasu według obiektów</span><span class="sxs-lookup"><span data-stu-id="f2966-112">Example 2: Remove a time series insights environment by object</span></span>
```powershell
PS C:\> $env = Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsill
PS C:\> Remove-AzTimeSeriesInsightsEnvironment -InputObject $env

```

<span data-ttu-id="f2966-113">To polecenie usuwa środowisko informacji o seriach czasowych.</span><span class="sxs-lookup"><span data-stu-id="f2966-113">This command removes a time series insights environment.</span></span>

## <span data-ttu-id="f2966-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f2966-114">PARAMETERS</span></span>

### <span data-ttu-id="f2966-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2966-115">-DefaultProfile</span></span>
<span data-ttu-id="f2966-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f2966-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2966-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f2966-117">-InputObject</span></span>
<span data-ttu-id="f2966-118">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="f2966-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f2966-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f2966-119">-Name</span></span>
<span data-ttu-id="f2966-120">Nazwa środowiska informacji o serii czasowej skojarzonego z określoną grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="f2966-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2966-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f2966-121">-PassThru</span></span>
<span data-ttu-id="f2966-122">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="f2966-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f2966-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2966-123">-ResourceGroupName</span></span>
<span data-ttu-id="f2966-124">Nazwa grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f2966-124">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="f2966-125">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="f2966-125">-SubscriptionId</span></span>
<span data-ttu-id="f2966-126">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f2966-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="f2966-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f2966-127">-Confirm</span></span>
<span data-ttu-id="f2966-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2966-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2966-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2966-129">-WhatIf</span></span>
<span data-ttu-id="f2966-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2966-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2966-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f2966-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2966-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2966-132">CommonParameters</span></span>
<span data-ttu-id="f2966-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2966-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2966-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f2966-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2966-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2966-135">INPUTS</span></span>

### <span data-ttu-id="f2966-136">Microsoft. Azure. PowerShell. polecenia. TimeSeriesInsights. models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="f2966-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="f2966-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f2966-137">OUTPUTS</span></span>

### <span data-ttu-id="f2966-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f2966-138">System.Boolean</span></span>

## <span data-ttu-id="f2966-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f2966-139">NOTES</span></span>

<span data-ttu-id="f2966-140">PISUJE</span><span class="sxs-lookup"><span data-stu-id="f2966-140">ALIASES</span></span>

<span data-ttu-id="f2966-141">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f2966-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f2966-142">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="f2966-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f2966-143">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f2966-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f2966-144">INPUTobject <ITimeSeriesInsightsIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="f2966-144">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f2966-145">`[AccessPolicyName <String>]`: Nazwa zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="f2966-145">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="f2966-146">`[EnvironmentName <String>]`: Nazwa środowiska</span><span class="sxs-lookup"><span data-stu-id="f2966-146">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="f2966-147">`[EventSourceName <String>]`: Nazwa źródła zdarzeń szczegółowych informacji o seriach czasowych skojarzonego z określonym środowiskiem.</span><span class="sxs-lookup"><span data-stu-id="f2966-147">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="f2966-148">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="f2966-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f2966-149">`[ReferenceDataSetName <String>]`: Nazwa zestawu danych referencyjnych.</span><span class="sxs-lookup"><span data-stu-id="f2966-149">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="f2966-150">`[ResourceGroupName <String>]`: Nazwa grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f2966-150">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="f2966-151">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f2966-151">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="f2966-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f2966-152">RELATED LINKS</span></span>

