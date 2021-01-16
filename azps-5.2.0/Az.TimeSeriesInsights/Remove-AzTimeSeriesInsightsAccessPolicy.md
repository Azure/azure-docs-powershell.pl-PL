---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: 2a6c58729d08c5bd060434c7a21720f87a3f7de3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349078"
---
# <span data-ttu-id="9a94e-101">Remove-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9a94e-101">Remove-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="9a94e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9a94e-102">SYNOPSIS</span></span>
<span data-ttu-id="9a94e-103">Usuwa zasady dostępu o określonej nazwie w określonej subskrypcji, grupie zasobów i środowisku.</span><span class="sxs-lookup"><span data-stu-id="9a94e-103">Deletes the access policy with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="9a94e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9a94e-104">SYNTAX</span></span>

### <span data-ttu-id="9a94e-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="9a94e-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9a94e-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9a94e-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity>
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9a94e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9a94e-107">DESCRIPTION</span></span>
<span data-ttu-id="9a94e-108">Usuwa zasady dostępu o określonej nazwie w określonej subskrypcji, grupie zasobów i środowisku.</span><span class="sxs-lookup"><span data-stu-id="9a94e-108">Deletes the access policy with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="9a94e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9a94e-109">EXAMPLES</span></span>

### <span data-ttu-id="9a94e-110">Przykład 1: usunięcie określonych zasad dostępu według nazwy</span><span class="sxs-lookup"><span data-stu-id="9a94e-110">Example 1: Remove a specified access policy by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup

```

<span data-ttu-id="9a94e-111">To polecenie usuwa określone zasady dostępu.</span><span class="sxs-lookup"><span data-stu-id="9a94e-111">This command removes a specified access policy.</span></span>

### <span data-ttu-id="9a94e-112">Przykład 2: usuwanie określonych zasad dostępu według obiektów</span><span class="sxs-lookup"><span data-stu-id="9a94e-112">Example 2: Remove a specified access policy by object</span></span>
```powershell
PS C:\> $policy = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup
PS C:\> Remove-AzTimeSeriesInsightsAccessPolicy -InputObject $policy

```

<span data-ttu-id="9a94e-113">To polecenie usuwa określone zasady dostępu.</span><span class="sxs-lookup"><span data-stu-id="9a94e-113">This command removes a specified access policy.</span></span>

## <span data-ttu-id="9a94e-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9a94e-114">PARAMETERS</span></span>

### <span data-ttu-id="9a94e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a94e-115">-DefaultProfile</span></span>
<span data-ttu-id="9a94e-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9a94e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a94e-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="9a94e-117">-EnvironmentName</span></span>
<span data-ttu-id="9a94e-118">Nazwa środowiska informacji o serii czasowej skojarzonego z określoną grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="9a94e-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="9a94e-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9a94e-119">-InputObject</span></span>
<span data-ttu-id="9a94e-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="9a94e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9a94e-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9a94e-121">-Name</span></span>
<span data-ttu-id="9a94e-122">Nazwa zasad dostępu usługi Insights w ramach sekwencji czasu skojarzonych z określonym środowiskiem.</span><span class="sxs-lookup"><span data-stu-id="9a94e-122">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

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

### <span data-ttu-id="9a94e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a94e-123">-PassThru</span></span>
<span data-ttu-id="9a94e-124">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="9a94e-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9a94e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a94e-125">-ResourceGroupName</span></span>
<span data-ttu-id="9a94e-126">Nazwa grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9a94e-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="9a94e-127">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="9a94e-127">-SubscriptionId</span></span>
<span data-ttu-id="9a94e-128">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9a94e-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="9a94e-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9a94e-129">-Confirm</span></span>
<span data-ttu-id="9a94e-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a94e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a94e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a94e-131">-WhatIf</span></span>
<span data-ttu-id="9a94e-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a94e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a94e-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9a94e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a94e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a94e-134">CommonParameters</span></span>
<span data-ttu-id="9a94e-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a94e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a94e-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9a94e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a94e-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9a94e-137">INPUTS</span></span>

### <span data-ttu-id="9a94e-138">Microsoft. Azure. PowerShell. polecenia. TimeSeriesInsights. models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="9a94e-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="9a94e-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9a94e-139">OUTPUTS</span></span>

### <span data-ttu-id="9a94e-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9a94e-140">System.Boolean</span></span>

## <span data-ttu-id="9a94e-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9a94e-141">NOTES</span></span>

<span data-ttu-id="9a94e-142">PISUJE</span><span class="sxs-lookup"><span data-stu-id="9a94e-142">ALIASES</span></span>

<span data-ttu-id="9a94e-143">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9a94e-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9a94e-144">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="9a94e-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9a94e-145">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9a94e-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9a94e-146">INPUTobject <ITimeSeriesInsightsIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="9a94e-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9a94e-147">`[AccessPolicyName <String>]`: Nazwa zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="9a94e-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="9a94e-148">`[EnvironmentName <String>]`: Nazwa środowiska</span><span class="sxs-lookup"><span data-stu-id="9a94e-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="9a94e-149">`[EventSourceName <String>]`: Nazwa źródła zdarzeń szczegółowych informacji o seriach czasowych skojarzonego z określonym środowiskiem.</span><span class="sxs-lookup"><span data-stu-id="9a94e-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="9a94e-150">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="9a94e-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9a94e-151">`[ReferenceDataSetName <String>]`: Nazwa zestawu danych referencyjnych.</span><span class="sxs-lookup"><span data-stu-id="9a94e-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="9a94e-152">`[ResourceGroupName <String>]`: Nazwa grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9a94e-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="9a94e-153">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9a94e-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="9a94e-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9a94e-154">RELATED LINKS</span></span>

