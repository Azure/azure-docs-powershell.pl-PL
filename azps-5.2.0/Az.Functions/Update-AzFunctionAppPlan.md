---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
ms.openlocfilehash: e0831e95a5601d3558af7089825684cc48e7838c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345250"
---
# <span data-ttu-id="bee04-101">Update-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="bee04-101">Update-AzFunctionAppPlan</span></span>

## <span data-ttu-id="bee04-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bee04-102">SYNOPSIS</span></span>
<span data-ttu-id="bee04-103">Aktualizuje plan usługi App Service.</span><span class="sxs-lookup"><span data-stu-id="bee04-103">Updates a function app service plan.</span></span>

## <span data-ttu-id="bee04-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bee04-104">SYNTAX</span></span>

### <span data-ttu-id="bee04-105">ByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bee04-105">ByName (Default)</span></span>
```
Update-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bee04-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="bee04-106">ByObjectInput</span></span>
```
Update-AzFunctionAppPlan -InputObject <IAppServicePlan> [-MaximumWorkerCount <Int32>]
 [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bee04-107">Opis</span><span class="sxs-lookup"><span data-stu-id="bee04-107">DESCRIPTION</span></span>
<span data-ttu-id="bee04-108">Aktualizuje plan usługi App Service.</span><span class="sxs-lookup"><span data-stu-id="bee04-108">Updates a function app service plan.</span></span>

## <span data-ttu-id="bee04-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bee04-109">EXAMPLES</span></span>

### <span data-ttu-id="bee04-110">Przykład 1: aktualizowanie planu usługi App Service, aby EP2 SKU z 20 maksymalnymi pracownikami.</span><span class="sxs-lookup"><span data-stu-id="bee04-110">Example 1: Update an app service plan to EP2 sku with twenty maximum workers.</span></span>
```powershell
PS C:\> Update-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                                 -Name MyPremiumPlan `
                                 -MaximumWorkerCount 20 `
                                 -Sku EP2

```

<span data-ttu-id="bee04-111">To polecenie aktualizuje plan usługi App Service, aby EP2 SKU z 20 maksymalnymi pracownikami.</span><span class="sxs-lookup"><span data-stu-id="bee04-111">This command updates an app service plan to EP2 sku with twenty maximum workers.</span></span>

## <span data-ttu-id="bee04-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bee04-112">PARAMETERS</span></span>

### <span data-ttu-id="bee04-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bee04-113">-AsJob</span></span>
<span data-ttu-id="bee04-114">Uruchom polecenie jako zadanie.</span><span class="sxs-lookup"><span data-stu-id="bee04-114">Run the command as a job.</span></span>

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

### <span data-ttu-id="bee04-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bee04-115">-DefaultProfile</span></span>


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

### <span data-ttu-id="bee04-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bee04-116">-InputObject</span></span>
<span data-ttu-id="bee04-117">Aby skonstruować, zobacz sekcję notatki dla właściwości INPUTobject i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="bee04-117">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bee04-118">-MaximumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="bee04-118">-MaximumWorkerCount</span></span>
<span data-ttu-id="bee04-119">Maksymalna liczba pracowników planu usługi App Service.</span><span class="sxs-lookup"><span data-stu-id="bee04-119">The maximum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="bee04-120">-MinimumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="bee04-120">-MinimumWorkerCount</span></span>
<span data-ttu-id="bee04-121">Minimalna liczba pracowników planu usługi App Service.</span><span class="sxs-lookup"><span data-stu-id="bee04-121">The minimum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="bee04-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bee04-122">-Name</span></span>
<span data-ttu-id="bee04-123">Nazwa planu usługi App Service.</span><span class="sxs-lookup"><span data-stu-id="bee04-123">Name of the App Service plan.</span></span>

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

### <span data-ttu-id="bee04-124">-Nowait</span><span class="sxs-lookup"><span data-stu-id="bee04-124">-NoWait</span></span>
<span data-ttu-id="bee04-125">Uruchom polecenie asynchronicznie.</span><span class="sxs-lookup"><span data-stu-id="bee04-125">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="bee04-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bee04-126">-ResourceGroupName</span></span>
<span data-ttu-id="bee04-127">Nazwa grupy zasobów, do której należy zasób.</span><span class="sxs-lookup"><span data-stu-id="bee04-127">Name of the resource group to which the resource belongs.</span></span>

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

### <span data-ttu-id="bee04-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="bee04-128">-Sku</span></span>
<span data-ttu-id="bee04-129">Wersja planu.</span><span class="sxs-lookup"><span data-stu-id="bee04-129">The plan sku.</span></span>
<span data-ttu-id="bee04-130">Prawidłowe dane wejściowe to: EP1, EP2, EP3</span><span class="sxs-lookup"><span data-stu-id="bee04-130">Valid inputs are: EP1, EP2, EP3</span></span>

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

### <span data-ttu-id="bee04-131">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="bee04-131">-SubscriptionId</span></span>
<span data-ttu-id="bee04-132">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bee04-132">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="bee04-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="bee04-133">-Tag</span></span>
<span data-ttu-id="bee04-134">Znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="bee04-134">Resource tags.</span></span>

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

### <span data-ttu-id="bee04-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bee04-135">-Confirm</span></span>
<span data-ttu-id="bee04-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bee04-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bee04-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bee04-137">-WhatIf</span></span>
<span data-ttu-id="bee04-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bee04-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bee04-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bee04-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bee04-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bee04-140">CommonParameters</span></span>
<span data-ttu-id="bee04-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bee04-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bee04-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bee04-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bee04-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bee04-143">INPUTS</span></span>

### <span data-ttu-id="bee04-144">Microsoft. Azure. PowerShell. polecenia. Functions. models. Api20190801. IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="bee04-144">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="bee04-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bee04-145">OUTPUTS</span></span>

### <span data-ttu-id="bee04-146">Microsoft. Azure. PowerShell. polecenia. Functions. models. Api20190801. IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="bee04-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="bee04-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bee04-147">NOTES</span></span>

<span data-ttu-id="bee04-148">PISUJE</span><span class="sxs-lookup"><span data-stu-id="bee04-148">ALIASES</span></span>

<span data-ttu-id="bee04-149">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bee04-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bee04-150">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="bee04-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bee04-151">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bee04-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bee04-152">INPUTobject <IAppServicePlan> :</span><span class="sxs-lookup"><span data-stu-id="bee04-152">INPUTOBJECT <IAppServicePlan>:</span></span> 
  - <span data-ttu-id="bee04-153">`Location <String>`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="bee04-153">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="bee04-154">`[Kind <String>]`: Rodzaj zasobu.</span><span class="sxs-lookup"><span data-stu-id="bee04-154">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="bee04-155">`[Tag <IResourceTags>]`: Znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="bee04-155">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="bee04-156">`[(Any) <String>]`: Wskazuje, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="bee04-156">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="bee04-157">`[Capacity <Int32?>]`: Bieżąca liczba wystąpień przydzielonych do zasobu.</span><span class="sxs-lookup"><span data-stu-id="bee04-157">`[Capacity <Int32?>]`: Current number of instances assigned to the resource.</span></span>
  - <span data-ttu-id="bee04-158">`[FreeOfferExpirationTime <DateTime?>]`: Czas wygaśnięcia bezpłatnej oferty farmy serwerów.</span><span class="sxs-lookup"><span data-stu-id="bee04-158">`[FreeOfferExpirationTime <DateTime?>]`: The time when the server farm free offer expires.</span></span>
  - <span data-ttu-id="bee04-159">`[HostingEnvironmentProfileId <String>]`: Identyfikator zasobu środowiska App Service Environment.</span><span class="sxs-lookup"><span data-stu-id="bee04-159">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="bee04-160">`[HyperV <Boolean?>]`: Jeśli plan usługi App Service kontener funkcji Hyper-V jest <code>true</code> <code>false</code> inny, w przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="bee04-160">`[HyperV <Boolean?>]`: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="bee04-161">`[IsSpot <Boolean?>]`: Jeśli <code>true</code> ten plan usługi App Service jest właścicielem wystąpień dodatkowych.</span><span class="sxs-lookup"><span data-stu-id="bee04-161">`[IsSpot <Boolean?>]`: If <code>true</code>, this App Service Plan owns spot instances.</span></span>
  - <span data-ttu-id="bee04-162">`[IsXenon <Boolean?>]`: Przestarzałe: Jeśli plan usługi App Service kontener funkcji Hyper-V jest <code>true</code> <code>false</code> inny, w przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="bee04-162">`[IsXenon <Boolean?>]`: Obsolete: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="bee04-163">`[MaximumElasticWorkerCount <Int32?>]`: Maksymalna liczba wszystkich pracowników dozwolonych dla tego planu usługi App Service ElasticScaleEnabled</span><span class="sxs-lookup"><span data-stu-id="bee04-163">`[MaximumElasticWorkerCount <Int32?>]`: Maximum number of total workers allowed for this ElasticScaleEnabled App Service Plan</span></span>
  - <span data-ttu-id="bee04-164">`[PerSiteScaling <Boolean?>]`: Jeśli <code>true</code> aplikacje przydzielone do tego planu usługi App Service mogą być skalowane niezależnie.</span><span class="sxs-lookup"><span data-stu-id="bee04-164">`[PerSiteScaling <Boolean?>]`: If <code>true</code>, apps assigned to this App Service plan can be scaled independently.</span></span>         <span data-ttu-id="bee04-165">Jeśli <code>false</code> aplikacje przydzielone do tego planu usługi App Service będą skalowane do wszystkich wystąpień planu.</span><span class="sxs-lookup"><span data-stu-id="bee04-165">If <code>false</code>, apps assigned to this App Service plan will scale to all instances of the plan.</span></span>
  - <span data-ttu-id="bee04-166">`[Reserved <Boolean?>]`: Jeśli plan usługi Linux App Service jest <code>true</code> <code>false</code> inny, w przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="bee04-166">`[Reserved <Boolean?>]`: If Linux app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="bee04-167">`[SkuCapability <ICapability[]>]`: Funkcje jednostki SKU, na przykład, są włączone w usłudze Traffic Manager?</span><span class="sxs-lookup"><span data-stu-id="bee04-167">`[SkuCapability <ICapability[]>]`: Capabilities of the SKU, e.g., is traffic manager enabled?</span></span>
    - <span data-ttu-id="bee04-168">`[Name <String>]`: Nazwa funkcji SKU.</span><span class="sxs-lookup"><span data-stu-id="bee04-168">`[Name <String>]`: Name of the SKU capability.</span></span>
    - <span data-ttu-id="bee04-169">`[Reason <String>]`: Przyczyna funkcji SKU.</span><span class="sxs-lookup"><span data-stu-id="bee04-169">`[Reason <String>]`: Reason of the SKU capability.</span></span>
    - <span data-ttu-id="bee04-170">`[Value <String>]`: Wartość funkcji SKU.</span><span class="sxs-lookup"><span data-stu-id="bee04-170">`[Value <String>]`: Value of the SKU capability.</span></span>
  - <span data-ttu-id="bee04-171">`[SkuCapacityDefault <Int32?>]`: Domyślna liczba pracowników tej jednostki SKU planu usługi App Service.</span><span class="sxs-lookup"><span data-stu-id="bee04-171">`[SkuCapacityDefault <Int32?>]`: Default number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="bee04-172">`[SkuCapacityMaximum <Int32?>]`: Maksymalna liczba pracowników tej jednostki SKU planu usługi App Service.</span><span class="sxs-lookup"><span data-stu-id="bee04-172">`[SkuCapacityMaximum <Int32?>]`: Maximum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="bee04-173">`[SkuCapacityMinimum <Int32?>]`: Minimalna liczba pracowników dla tej jednostki SKU planu usługi App Service.</span><span class="sxs-lookup"><span data-stu-id="bee04-173">`[SkuCapacityMinimum <Int32?>]`: Minimum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="bee04-174">`[SkuCapacityScaleType <String>]`: Dostępne konfiguracje skali dla planu usługi App Service.</span><span class="sxs-lookup"><span data-stu-id="bee04-174">`[SkuCapacityScaleType <String>]`: Available scale configurations for an App Service plan.</span></span>
  - <span data-ttu-id="bee04-175">`[SkuFamily <String>]`: Kod rodziny w wersji SKU zasobu.</span><span class="sxs-lookup"><span data-stu-id="bee04-175">`[SkuFamily <String>]`: Family code of the resource SKU.</span></span>
  - <span data-ttu-id="bee04-176">`[SkuLocation <String[]>]`: Lokalizacje jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="bee04-176">`[SkuLocation <String[]>]`: Locations of the SKU.</span></span>
  - <span data-ttu-id="bee04-177">`[SkuName <String>]`: Nazwa SKU zasobu.</span><span class="sxs-lookup"><span data-stu-id="bee04-177">`[SkuName <String>]`: Name of the resource SKU.</span></span>
  - <span data-ttu-id="bee04-178">`[SkuSize <String>]`: Określenie rozmiaru jednostki SKU zasobu.</span><span class="sxs-lookup"><span data-stu-id="bee04-178">`[SkuSize <String>]`: Size specifier of the resource SKU.</span></span>
  - <span data-ttu-id="bee04-179">`[SkuTier <String>]`: Warstwa usługi SKU zasobu.</span><span class="sxs-lookup"><span data-stu-id="bee04-179">`[SkuTier <String>]`: Service tier of the resource SKU.</span></span>
  - <span data-ttu-id="bee04-180">`[SpotExpirationTime <DateTime?>]`: Czas wygaśnięcia farmy serwerów.</span><span class="sxs-lookup"><span data-stu-id="bee04-180">`[SpotExpirationTime <DateTime?>]`: The time when the server farm expires.</span></span> <span data-ttu-id="bee04-181">Ważne tylko w przypadku, gdy jest to farma serwera dodatkowego.</span><span class="sxs-lookup"><span data-stu-id="bee04-181">Valid only if it is a spot server farm.</span></span>
  - <span data-ttu-id="bee04-182">`[TargetWorkerCount <Int32?>]`: Liczba przeskalowania pracownika.</span><span class="sxs-lookup"><span data-stu-id="bee04-182">`[TargetWorkerCount <Int32?>]`: Scaling worker count.</span></span>
  - <span data-ttu-id="bee04-183">`[TargetWorkerSizeId <Int32?>]`: Skalowanie rozmiaru pracownika.</span><span class="sxs-lookup"><span data-stu-id="bee04-183">`[TargetWorkerSizeId <Int32?>]`: Scaling worker size ID.</span></span>
  - <span data-ttu-id="bee04-184">`[WorkerTierName <String>]`: Warstwa docelowa roboczego przypisana do planu usługi App Service.</span><span class="sxs-lookup"><span data-stu-id="bee04-184">`[WorkerTierName <String>]`: Target worker tier assigned to the App Service plan.</span></span>

## <span data-ttu-id="bee04-185">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bee04-185">RELATED LINKS</span></span>

