---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: e776b0e11fedd0b2903135b9b640c3b704706027
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224961"
---
# <span data-ttu-id="515da-101">Update-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="515da-101">Update-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="515da-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="515da-102">SYNOPSIS</span></span>
<span data-ttu-id="515da-103">Aktualizuje zasady dostępu o określonej nazwie w określonej subskrypcji, grupie zasobów i środowisku.</span><span class="sxs-lookup"><span data-stu-id="515da-103">Updates the access policy with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="515da-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="515da-104">SYNTAX</span></span>

### <span data-ttu-id="515da-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="515da-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-Role <AccessPolicyRole[]>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="515da-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="515da-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity> [-Description <String>]
 [-Role <AccessPolicyRole[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="515da-107">Opis</span><span class="sxs-lookup"><span data-stu-id="515da-107">DESCRIPTION</span></span>
<span data-ttu-id="515da-108">Aktualizuje zasady dostępu o określonej nazwie w określonej subskrypcji, grupie zasobów i środowisku.</span><span class="sxs-lookup"><span data-stu-id="515da-108">Updates the access policy with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="515da-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="515da-109">EXAMPLES</span></span>

### <span data-ttu-id="515da-110">Przykład 1: aktualizowanie określonych zasad dostępu według nazwy</span><span class="sxs-lookup"><span data-stu-id="515da-110">Example 1: Update a specified access policy by name</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup -Role Contributor,Reader

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="515da-111">To polecenie aktualizuje określone zasady dostępu.</span><span class="sxs-lookup"><span data-stu-id="515da-111">This command updates a specified access policy.</span></span>

### <span data-ttu-id="515da-112">Przykład 2: aktualizowanie określonych zasad dostępu według obiektów</span><span class="sxs-lookup"><span data-stu-id="515da-112">Example 2: Update a specified access policy by object</span></span>
```powershell
PS C:\> $policy = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name policy001
PS C:\> Update-AzTimeSeriesInsightsAccessPolicy -InputObject $policy -Role Contributor

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="515da-113">To polecenie aktualizuje określone zasady dostępu.</span><span class="sxs-lookup"><span data-stu-id="515da-113">This command updates a specified access policy.</span></span>

## <span data-ttu-id="515da-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="515da-114">PARAMETERS</span></span>

### <span data-ttu-id="515da-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="515da-115">-DefaultProfile</span></span>
<span data-ttu-id="515da-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="515da-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="515da-117">— Opis</span><span class="sxs-lookup"><span data-stu-id="515da-117">-Description</span></span>
<span data-ttu-id="515da-118">Opis zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="515da-118">An description of the access policy.</span></span>

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

### <span data-ttu-id="515da-119">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="515da-119">-EnvironmentName</span></span>
<span data-ttu-id="515da-120">Nazwa środowiska informacji o serii czasowej skojarzonego z określoną grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="515da-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="515da-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="515da-121">-InputObject</span></span>
<span data-ttu-id="515da-122">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="515da-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="515da-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="515da-123">-Name</span></span>
<span data-ttu-id="515da-124">Nazwa zasad dostępu usługi Insights w ramach sekwencji czasu skojarzonych z określonym środowiskiem.</span><span class="sxs-lookup"><span data-stu-id="515da-124">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

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

### <span data-ttu-id="515da-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="515da-125">-ResourceGroupName</span></span>
<span data-ttu-id="515da-126">Nazwa grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="515da-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="515da-127">-Rola</span><span class="sxs-lookup"><span data-stu-id="515da-127">-Role</span></span>
<span data-ttu-id="515da-128">Lista ról, do których podmiot zabezpieczeń jest przydzielony w środowisku.</span><span class="sxs-lookup"><span data-stu-id="515da-128">The list of roles the principal is assigned on the environment.</span></span>

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

### <span data-ttu-id="515da-129">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="515da-129">-SubscriptionId</span></span>
<span data-ttu-id="515da-130">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="515da-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="515da-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="515da-131">-Confirm</span></span>
<span data-ttu-id="515da-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="515da-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="515da-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="515da-133">-WhatIf</span></span>
<span data-ttu-id="515da-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="515da-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="515da-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="515da-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="515da-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="515da-136">CommonParameters</span></span>
<span data-ttu-id="515da-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="515da-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="515da-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="515da-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="515da-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="515da-139">INPUTS</span></span>

### <span data-ttu-id="515da-140">Microsoft. Azure. PowerShell. polecenia. TimeSeriesInsights. models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="515da-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="515da-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="515da-141">OUTPUTS</span></span>

### <span data-ttu-id="515da-142">Microsoft. Azure. PowerShell. polecenia. TimeSeriesInsights. models. Api20200515. IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="515da-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="515da-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="515da-143">NOTES</span></span>

<span data-ttu-id="515da-144">PISUJE</span><span class="sxs-lookup"><span data-stu-id="515da-144">ALIASES</span></span>

<span data-ttu-id="515da-145">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="515da-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="515da-146">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="515da-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="515da-147">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="515da-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="515da-148">INPUTobject <ITimeSeriesInsightsIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="515da-148">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="515da-149">`[AccessPolicyName <String>]`: Nazwa zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="515da-149">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="515da-150">`[EnvironmentName <String>]`: Nazwa środowiska</span><span class="sxs-lookup"><span data-stu-id="515da-150">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="515da-151">`[EventSourceName <String>]`: Nazwa źródła zdarzeń szczegółowych informacji o seriach czasowych skojarzonego z określonym środowiskiem.</span><span class="sxs-lookup"><span data-stu-id="515da-151">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="515da-152">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="515da-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="515da-153">`[ReferenceDataSetName <String>]`: Nazwa zestawu danych referencyjnych.</span><span class="sxs-lookup"><span data-stu-id="515da-153">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="515da-154">`[ResourceGroupName <String>]`: Nazwa grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="515da-154">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="515da-155">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="515da-155">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="515da-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="515da-156">RELATED LINKS</span></span>

