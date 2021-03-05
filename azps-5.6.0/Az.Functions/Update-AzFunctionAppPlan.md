---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/update-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
ms.openlocfilehash: 522de6721d92b76938843b28322b94b5cc6ce481
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963041"
---
# <span data-ttu-id="dd0d1-101">Update-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="dd0d1-101">Update-AzFunctionAppPlan</span></span>

## <span data-ttu-id="dd0d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd0d1-102">SYNOPSIS</span></span>
<span data-ttu-id="dd0d1-103">Aktualizuje plan usługi aplikacji funkcyjnej.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-103">Updates a function app service plan.</span></span>

## <span data-ttu-id="dd0d1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="dd0d1-104">SYNTAX</span></span>

### <span data-ttu-id="dd0d1-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="dd0d1-105">ByName (Default)</span></span>
```
Update-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="dd0d1-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="dd0d1-106">ByObjectInput</span></span>
```
Update-AzFunctionAppPlan -InputObject <IAppServicePlan> [-MaximumWorkerCount <Int32>]
 [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dd0d1-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="dd0d1-107">DESCRIPTION</span></span>
<span data-ttu-id="dd0d1-108">Aktualizuje plan usługi aplikacji funkcyjnej.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-108">Updates a function app service plan.</span></span>

## <span data-ttu-id="dd0d1-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="dd0d1-109">EXAMPLES</span></span>

### <span data-ttu-id="dd0d1-110">Przykład 1. Aktualizowanie planu usługi aplikacji do wersji SKU EP2 z dwudziestoma maksymalnymi pracownikami.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-110">Example 1: Update an app service plan to EP2 sku with twenty maximum workers.</span></span>
```powershell
PS C:\> Update-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                                 -Name MyPremiumPlan `
                                 -MaximumWorkerCount 20 `
                                 -Sku EP2

```

<span data-ttu-id="dd0d1-111">To polecenie aktualizuje plan usługi aplikacji do sKU EP2 z dwudziestoma maksymalnymi pracownikami.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-111">This command updates an app service plan to EP2 sku with twenty maximum workers.</span></span>

## <span data-ttu-id="dd0d1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd0d1-112">PARAMETERS</span></span>

### <span data-ttu-id="dd0d1-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="dd0d1-113">-AsJob</span></span>
<span data-ttu-id="dd0d1-114">Uruchom polecenie jako zadanie.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-114">Run the command as a job.</span></span>

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

### <span data-ttu-id="dd0d1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd0d1-115">-DefaultProfile</span></span>


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

### <span data-ttu-id="dd0d1-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd0d1-116">-InputObject</span></span>
<span data-ttu-id="dd0d1-117">Aby skonstruować, zobacz sekcję NOTES, aby uzyskać informacje o właściwościach INPUTOBJECT i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-117">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan
Parameter Sets: ByObjectInput
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd0d1-118">-MaximumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="dd0d1-118">-MaximumWorkerCount</span></span>
<span data-ttu-id="dd0d1-119">Maksymalna liczba pracowników w planie usług aplikacji.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-119">The maximum number of workers for the app service plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MaxBurst

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd0d1-120">-MinimumLiczbowePracownika</span><span class="sxs-lookup"><span data-stu-id="dd0d1-120">-MinimumWorkerCount</span></span>
<span data-ttu-id="dd0d1-121">Minimalna liczba pracowników w planie usług aplikacji.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-121">The minimum number of workers for the app service plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MinInstances

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd0d1-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="dd0d1-122">-Name</span></span>
<span data-ttu-id="dd0d1-123">Nazwa planu usługi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-123">Name of the App Service plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd0d1-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="dd0d1-124">-NoWait</span></span>
<span data-ttu-id="dd0d1-125">Uruchom polecenie asynchronicznie.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-125">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="dd0d1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd0d1-126">-ResourceGroupName</span></span>
<span data-ttu-id="dd0d1-127">Nazwa grupy zasobów, do której należy zasób.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-127">Name of the resource group to which the resource belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd0d1-128">- SKU</span><span class="sxs-lookup"><span data-stu-id="dd0d1-128">-Sku</span></span>
<span data-ttu-id="dd0d1-129">SKU planu.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-129">The plan sku.</span></span>
<span data-ttu-id="dd0d1-130">Prawidłowe dane wejściowe: EP1, EP2, EP3</span><span class="sxs-lookup"><span data-stu-id="dd0d1-130">Valid inputs are: EP1, EP2, EP3</span></span>

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

### <span data-ttu-id="dd0d1-131">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dd0d1-131">-SubscriptionId</span></span>
<span data-ttu-id="dd0d1-132">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-132">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd0d1-133">— Tag</span><span class="sxs-lookup"><span data-stu-id="dd0d1-133">-Tag</span></span>
<span data-ttu-id="dd0d1-134">Tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-134">Resource tags.</span></span>

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

### <span data-ttu-id="dd0d1-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dd0d1-135">-Confirm</span></span>
<span data-ttu-id="dd0d1-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd0d1-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd0d1-137">-WhatIf</span></span>
<span data-ttu-id="dd0d1-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd0d1-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd0d1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd0d1-140">CommonParameters</span></span>
<span data-ttu-id="dd0d1-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd0d1-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dd0d1-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd0d1-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd0d1-143">INPUTS</span></span>

### <span data-ttu-id="dd0d1-144">Microsoft.Azure.PowerShell.Cmdlet.Functions.Models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="dd0d1-144">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="dd0d1-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd0d1-145">OUTPUTS</span></span>

### <span data-ttu-id="dd0d1-146">Microsoft.Azure.PowerShell.Cmdlet.Functions.Models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="dd0d1-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="dd0d1-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="dd0d1-147">NOTES</span></span>

<span data-ttu-id="dd0d1-148">ALIASY</span><span class="sxs-lookup"><span data-stu-id="dd0d1-148">ALIASES</span></span>

<span data-ttu-id="dd0d1-149">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dd0d1-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dd0d1-150">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dd0d1-151">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dd0d1-152">INPUTOBJECT: <IAppServicePlan></span><span class="sxs-lookup"><span data-stu-id="dd0d1-152">INPUTOBJECT <IAppServicePlan>:</span></span> 
  - <span data-ttu-id="dd0d1-153">`Location <String>`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-153">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="dd0d1-154">`[Kind <String>]`: Rodzaj zasobu.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-154">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="dd0d1-155">`[Tag <IResourceTags>]`: tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-155">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="dd0d1-156">`[(Any) <String>]`: Wskazuje to, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-156">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="dd0d1-157">`[Capacity <Int32?>]`: Bieżąca liczba wystąpień przydzielonych do zasobu.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-157">`[Capacity <Int32?>]`: Current number of instances assigned to the resource.</span></span>
  - <span data-ttu-id="dd0d1-158">`[FreeOfferExpirationTime <DateTime?>]`: czas wygaśnięcia oferty bezpłatnej farmy serwerów.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-158">`[FreeOfferExpirationTime <DateTime?>]`: The time when the server farm free offer expires.</span></span>
  - <span data-ttu-id="dd0d1-159">`[HostingEnvironmentProfileId <String>]`: Identyfikator zasobu w środowisku usługi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-159">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="dd0d1-160">`[HyperV <Boolean?>]`: Jeśli plan usługi aplikacji kontenerowych Hyper-V — w <code>true</code> <code>false</code> przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-160">`[HyperV <Boolean?>]`: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="dd0d1-161">`[IsSpot <Boolean?>]`: Jeśli <code>true</code> ten plan usług aplikacji jest właścicielem wystąpień spotowych.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-161">`[IsSpot <Boolean?>]`: If <code>true</code>, this App Service Plan owns spot instances.</span></span>
  - <span data-ttu-id="dd0d1-162">`[IsXenon <Boolean?>]`: Przestarzałe: Jeśli plan usługi aplikacji kontenerowych Hyper-V <code>true</code> — <code>false</code> w przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-162">`[IsXenon <Boolean?>]`: Obsolete: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="dd0d1-163">`[MaximumElasticWorkerCount <Int32?>]`: Maksymalna liczba pracowników dozwolonych w tym planie usługi aplikacjiScaleEnabled</span><span class="sxs-lookup"><span data-stu-id="dd0d1-163">`[MaximumElasticWorkerCount <Int32?>]`: Maximum number of total workers allowed for this ElasticScaleEnabled App Service Plan</span></span>
  - <span data-ttu-id="dd0d1-164">`[PerSiteScaling <Boolean?>]`: Jeśli aplikacje przypisane do tego planu usługi aplikacji <code>true</code> mogą być skalowane niezależnie.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-164">`[PerSiteScaling <Boolean?>]`: If <code>true</code>, apps assigned to this App Service plan can be scaled independently.</span></span>         <span data-ttu-id="dd0d1-165">Jeśli <code>false</code> aplikacje przypisane do tego planu usługi aplikacji zostaną przeskalowane do wszystkich wystąpień planu.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-165">If <code>false</code>, apps assigned to this App Service plan will scale to all instances of the plan.</span></span>
  - <span data-ttu-id="dd0d1-166">`[Reserved <Boolean?>]`: Jeśli plan usługi aplikacji dla systemu Linux <code>true</code> , <code>false</code> w przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-166">`[Reserved <Boolean?>]`: If Linux app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="dd0d1-167">`[SkuCapability <ICapability[]>]`: Czy włączono możliwości sKU, np. czy włączono Menedżera ruchu?</span><span class="sxs-lookup"><span data-stu-id="dd0d1-167">`[SkuCapability <ICapability[]>]`: Capabilities of the SKU, e.g., is traffic manager enabled?</span></span>
    - <span data-ttu-id="dd0d1-168">`[Name <String>]`: nazwa funkcji SKU.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-168">`[Name <String>]`: Name of the SKU capability.</span></span>
    - <span data-ttu-id="dd0d1-169">`[Reason <String>]`: Przyczyna możliwości SKU.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-169">`[Reason <String>]`: Reason of the SKU capability.</span></span>
    - <span data-ttu-id="dd0d1-170">`[Value <String>]`Wartość funkcji SKU.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-170">`[Value <String>]`: Value of the SKU capability.</span></span>
  - <span data-ttu-id="dd0d1-171">`[SkuCapacityDefault <Int32?>]`: Domyślna liczba pracowników dla tego planu usługi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-171">`[SkuCapacityDefault <Int32?>]`: Default number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="dd0d1-172">`[SkuCapacityMaximum <Int32?>]`: Maksymalna liczba pracowników dla tego planu usługi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-172">`[SkuCapacityMaximum <Int32?>]`: Maximum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="dd0d1-173">`[SkuCapacityMinimum <Int32?>]`: Minimalna liczba pracowników dla tego planu usługi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-173">`[SkuCapacityMinimum <Int32?>]`: Minimum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="dd0d1-174">`[SkuCapacityScaleType <String>]`: Dostępne konfiguracje skali dla planu usługi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-174">`[SkuCapacityScaleType <String>]`: Available scale configurations for an App Service plan.</span></span>
  - <span data-ttu-id="dd0d1-175">`[SkuFamily <String>]`: Kod rodziny sku zasobu.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-175">`[SkuFamily <String>]`: Family code of the resource SKU.</span></span>
  - <span data-ttu-id="dd0d1-176">`[SkuLocation <String[]>]`: lokalizacje sku.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-176">`[SkuLocation <String[]>]`: Locations of the SKU.</span></span>
  - <span data-ttu-id="dd0d1-177">`[SkuName <String>]`: nazwa sku zasobu.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-177">`[SkuName <String>]`: Name of the resource SKU.</span></span>
  - <span data-ttu-id="dd0d1-178">`[SkuSize <String>]`: Specyfikator rozmiaru sku zasobu.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-178">`[SkuSize <String>]`: Size specifier of the resource SKU.</span></span>
  - <span data-ttu-id="dd0d1-179">`[SkuTier <String>]`: Warstwa usługi sku zasobu.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-179">`[SkuTier <String>]`: Service tier of the resource SKU.</span></span>
  - <span data-ttu-id="dd0d1-180">`[SpotExpirationTime <DateTime?>]`: czas wygaśnięcia farmy serwerów.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-180">`[SpotExpirationTime <DateTime?>]`: The time when the server farm expires.</span></span> <span data-ttu-id="dd0d1-181">Prawidłowy tylko w przypadku, gdy jest to farma serwerów spotowych.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-181">Valid only if it is a spot server farm.</span></span>
  - <span data-ttu-id="dd0d1-182">`[TargetWorkerCount <Int32?>]`: skalowanie liczby pracowników.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-182">`[TargetWorkerCount <Int32?>]`: Scaling worker count.</span></span>
  - <span data-ttu-id="dd0d1-183">`[TargetWorkerSizeId <Int32?>]`: skalowanie identyfikatora rozmiaru pracownika.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-183">`[TargetWorkerSizeId <Int32?>]`: Scaling worker size ID.</span></span>
  - <span data-ttu-id="dd0d1-184">`[WorkerTierName <String>]`: Warstwa docelowa pracownika przypisana do planu usługi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-184">`[WorkerTierName <String>]`: Target worker tier assigned to the App Service plan.</span></span>

## <span data-ttu-id="dd0d1-185">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dd0d1-185">RELATED LINKS</span></span>

