---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
ms.openlocfilehash: e0831e95a5601d3558af7089825684cc48e7838c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062737"
---
# <span data-ttu-id="42cd0-101">Update-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="42cd0-101">Update-AzFunctionAppPlan</span></span>

## <span data-ttu-id="42cd0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="42cd0-102">SYNOPSIS</span></span>
<span data-ttu-id="42cd0-103">Aktualizuje plan usługi App Service.</span><span class="sxs-lookup"><span data-stu-id="42cd0-103">Updates a function app service plan.</span></span>

## <span data-ttu-id="42cd0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="42cd0-104">SYNTAX</span></span>

### <span data-ttu-id="42cd0-105">ByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="42cd0-105">ByName (Default)</span></span>
```
Update-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="42cd0-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="42cd0-106">ByObjectInput</span></span>
```
Update-AzFunctionAppPlan -InputObject <IAppServicePlan> [-MaximumWorkerCount <Int32>]
 [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="42cd0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="42cd0-107">DESCRIPTION</span></span>
<span data-ttu-id="42cd0-108">Aktualizuje plan usługi App Service.</span><span class="sxs-lookup"><span data-stu-id="42cd0-108">Updates a function app service plan.</span></span>

## <span data-ttu-id="42cd0-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="42cd0-109">EXAMPLES</span></span>

### <span data-ttu-id="42cd0-110">Przykład 1: aktualizowanie planu usługi App Service, aby EP2 SKU z 20 maksymalnymi pracownikami.</span><span class="sxs-lookup"><span data-stu-id="42cd0-110">Example 1: Update an app service plan to EP2 sku with twenty maximum workers.</span></span>
```powershell
PS C:\> Update-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                                 -Name MyPremiumPlan `
                                 -MaximumWorkerCount 20 `
                                 -Sku EP2

```

<span data-ttu-id="42cd0-111">To polecenie aktualizuje plan usługi App Service, aby EP2 SKU z 20 maksymalnymi pracownikami.</span><span class="sxs-lookup"><span data-stu-id="42cd0-111">This command updates an app service plan to EP2 sku with twenty maximum workers.</span></span>

## <span data-ttu-id="42cd0-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="42cd0-112">PARAMETERS</span></span>

### <span data-ttu-id="42cd0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="42cd0-113">-AsJob</span></span>
<span data-ttu-id="42cd0-114">Uruchom polecenie jako zadanie.</span><span class="sxs-lookup"><span data-stu-id="42cd0-114">Run the command as a job.</span></span>

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

### <span data-ttu-id="42cd0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42cd0-115">-DefaultProfile</span></span>


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

### <span data-ttu-id="42cd0-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="42cd0-116">-InputObject</span></span>
<span data-ttu-id="42cd0-117">Aby skonstruować, zobacz sekcję notatki dla właściwości INPUTobject i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="42cd0-117">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="42cd0-118">-MaximumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="42cd0-118">-MaximumWorkerCount</span></span>
<span data-ttu-id="42cd0-119">Maksymalna liczba pracowników planu usługi App Service.</span><span class="sxs-lookup"><span data-stu-id="42cd0-119">The maximum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="42cd0-120">-MinimumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="42cd0-120">-MinimumWorkerCount</span></span>
<span data-ttu-id="42cd0-121">Minimalna liczba pracowników planu usługi App Service.</span><span class="sxs-lookup"><span data-stu-id="42cd0-121">The minimum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="42cd0-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="42cd0-122">-Name</span></span>
<span data-ttu-id="42cd0-123">Nazwa planu usługi App Service.</span><span class="sxs-lookup"><span data-stu-id="42cd0-123">Name of the App Service plan.</span></span>

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

### <span data-ttu-id="42cd0-124">-Nowait</span><span class="sxs-lookup"><span data-stu-id="42cd0-124">-NoWait</span></span>
<span data-ttu-id="42cd0-125">Uruchom polecenie asynchronicznie.</span><span class="sxs-lookup"><span data-stu-id="42cd0-125">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="42cd0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42cd0-126">-ResourceGroupName</span></span>
<span data-ttu-id="42cd0-127">Nazwa grupy zasobów, do której należy zasób.</span><span class="sxs-lookup"><span data-stu-id="42cd0-127">Name of the resource group to which the resource belongs.</span></span>

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

### <span data-ttu-id="42cd0-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="42cd0-128">-Sku</span></span>
<span data-ttu-id="42cd0-129">Wersja planu.</span><span class="sxs-lookup"><span data-stu-id="42cd0-129">The plan sku.</span></span>
<span data-ttu-id="42cd0-130">Prawidłowe dane wejściowe to: EP1, EP2, EP3</span><span class="sxs-lookup"><span data-stu-id="42cd0-130">Valid inputs are: EP1, EP2, EP3</span></span>

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

### <span data-ttu-id="42cd0-131">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="42cd0-131">-SubscriptionId</span></span>
<span data-ttu-id="42cd0-132">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="42cd0-132">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="42cd0-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="42cd0-133">-Tag</span></span>
<span data-ttu-id="42cd0-134">Znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="42cd0-134">Resource tags.</span></span>

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

### <span data-ttu-id="42cd0-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="42cd0-135">-Confirm</span></span>
<span data-ttu-id="42cd0-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42cd0-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42cd0-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42cd0-137">-WhatIf</span></span>
<span data-ttu-id="42cd0-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42cd0-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42cd0-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="42cd0-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42cd0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42cd0-140">CommonParameters</span></span>
<span data-ttu-id="42cd0-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42cd0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42cd0-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="42cd0-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42cd0-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="42cd0-143">INPUTS</span></span>

### <span data-ttu-id="42cd0-144">Microsoft. Azure. PowerShell. polecenia. Functions. models. Api20190801. IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="42cd0-144">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="42cd0-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="42cd0-145">OUTPUTS</span></span>

### <span data-ttu-id="42cd0-146">Microsoft. Azure. PowerShell. polecenia. Functions. models. Api20190801. IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="42cd0-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="42cd0-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="42cd0-147">NOTES</span></span>

<span data-ttu-id="42cd0-148">PISUJE</span><span class="sxs-lookup"><span data-stu-id="42cd0-148">ALIASES</span></span>

<span data-ttu-id="42cd0-149">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="42cd0-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="42cd0-150">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="42cd0-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="42cd0-151">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="42cd0-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="42cd0-152">INPUTobject <IAppServicePlan> :</span><span class="sxs-lookup"><span data-stu-id="42cd0-152">INPUTOBJECT <IAppServicePlan>:</span></span> 
  - <span data-ttu-id="42cd0-153">`Location <String>`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="42cd0-153">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="42cd0-154">`[Kind <String>]`: Rodzaj zasobu.</span><span class="sxs-lookup"><span data-stu-id="42cd0-154">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="42cd0-155">`[Tag <IResourceTags>]`: Znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="42cd0-155">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="42cd0-156">`[(Any) <String>]`: Wskazuje, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="42cd0-156">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="42cd0-157">`[Capacity <Int32?>]`: Bieżąca liczba wystąpień przydzielonych do zasobu.</span><span class="sxs-lookup"><span data-stu-id="42cd0-157">`[Capacity <Int32?>]`: Current number of instances assigned to the resource.</span></span>
  - <span data-ttu-id="42cd0-158">`[FreeOfferExpirationTime <DateTime?>]`: Czas wygaśnięcia bezpłatnej oferty farmy serwerów.</span><span class="sxs-lookup"><span data-stu-id="42cd0-158">`[FreeOfferExpirationTime <DateTime?>]`: The time when the server farm free offer expires.</span></span>
  - <span data-ttu-id="42cd0-159">`[HostingEnvironmentProfileId <String>]`: Identyfikator zasobu środowiska App Service Environment.</span><span class="sxs-lookup"><span data-stu-id="42cd0-159">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="42cd0-160">`[HyperV <Boolean?>]`: Jeśli plan usługi App Service kontener funkcji Hyper-V jest <code>true</code> <code>false</code> inny, w przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="42cd0-160">`[HyperV <Boolean?>]`: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="42cd0-161">`[IsSpot <Boolean?>]`: Jeśli <code>true</code> ten plan usługi App Service jest właścicielem wystąpień dodatkowych.</span><span class="sxs-lookup"><span data-stu-id="42cd0-161">`[IsSpot <Boolean?>]`: If <code>true</code>, this App Service Plan owns spot instances.</span></span>
  - <span data-ttu-id="42cd0-162">`[IsXenon <Boolean?>]`: Przestarzałe: Jeśli plan usługi App Service kontener funkcji Hyper-V jest <code>true</code> <code>false</code> inny, w przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="42cd0-162">`[IsXenon <Boolean?>]`: Obsolete: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="42cd0-163">`[MaximumElasticWorkerCount <Int32?>]`: Maksymalna liczba wszystkich pracowników dozwolonych dla tego planu usługi App Service ElasticScaleEnabled</span><span class="sxs-lookup"><span data-stu-id="42cd0-163">`[MaximumElasticWorkerCount <Int32?>]`: Maximum number of total workers allowed for this ElasticScaleEnabled App Service Plan</span></span>
  - <span data-ttu-id="42cd0-164">`[PerSiteScaling <Boolean?>]`: Jeśli <code>true</code> aplikacje przydzielone do tego planu usługi App Service mogą być skalowane niezależnie.</span><span class="sxs-lookup"><span data-stu-id="42cd0-164">`[PerSiteScaling <Boolean?>]`: If <code>true</code>, apps assigned to this App Service plan can be scaled independently.</span></span>         <span data-ttu-id="42cd0-165">Jeśli <code>false</code> aplikacje przydzielone do tego planu usługi App Service będą skalowane do wszystkich wystąpień planu.</span><span class="sxs-lookup"><span data-stu-id="42cd0-165">If <code>false</code>, apps assigned to this App Service plan will scale to all instances of the plan.</span></span>
  - <span data-ttu-id="42cd0-166">`[Reserved <Boolean?>]`: Jeśli plan usługi Linux App Service jest <code>true</code> <code>false</code> inny, w przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="42cd0-166">`[Reserved <Boolean?>]`: If Linux app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="42cd0-167">`[SkuCapability <ICapability[]>]`: Funkcje jednostki SKU, na przykład, są włączone w usłudze Traffic Manager?</span><span class="sxs-lookup"><span data-stu-id="42cd0-167">`[SkuCapability <ICapability[]>]`: Capabilities of the SKU, e.g., is traffic manager enabled?</span></span>
    - <span data-ttu-id="42cd0-168">`[Name <String>]`: Nazwa funkcji SKU.</span><span class="sxs-lookup"><span data-stu-id="42cd0-168">`[Name <String>]`: Name of the SKU capability.</span></span>
    - <span data-ttu-id="42cd0-169">`[Reason <String>]`: Przyczyna funkcji SKU.</span><span class="sxs-lookup"><span data-stu-id="42cd0-169">`[Reason <String>]`: Reason of the SKU capability.</span></span>
    - <span data-ttu-id="42cd0-170">`[Value <String>]`: Wartość funkcji SKU.</span><span class="sxs-lookup"><span data-stu-id="42cd0-170">`[Value <String>]`: Value of the SKU capability.</span></span>
  - <span data-ttu-id="42cd0-171">`[SkuCapacityDefault <Int32?>]`: Domyślna liczba pracowników tej jednostki SKU planu usługi App Service.</span><span class="sxs-lookup"><span data-stu-id="42cd0-171">`[SkuCapacityDefault <Int32?>]`: Default number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="42cd0-172">`[SkuCapacityMaximum <Int32?>]`: Maksymalna liczba pracowników tej jednostki SKU planu usługi App Service.</span><span class="sxs-lookup"><span data-stu-id="42cd0-172">`[SkuCapacityMaximum <Int32?>]`: Maximum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="42cd0-173">`[SkuCapacityMinimum <Int32?>]`: Minimalna liczba pracowników dla tej jednostki SKU planu usługi App Service.</span><span class="sxs-lookup"><span data-stu-id="42cd0-173">`[SkuCapacityMinimum <Int32?>]`: Minimum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="42cd0-174">`[SkuCapacityScaleType <String>]`: Dostępne konfiguracje skali dla planu usługi App Service.</span><span class="sxs-lookup"><span data-stu-id="42cd0-174">`[SkuCapacityScaleType <String>]`: Available scale configurations for an App Service plan.</span></span>
  - <span data-ttu-id="42cd0-175">`[SkuFamily <String>]`: Kod rodziny w wersji SKU zasobu.</span><span class="sxs-lookup"><span data-stu-id="42cd0-175">`[SkuFamily <String>]`: Family code of the resource SKU.</span></span>
  - <span data-ttu-id="42cd0-176">`[SkuLocation <String[]>]`: Lokalizacje jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="42cd0-176">`[SkuLocation <String[]>]`: Locations of the SKU.</span></span>
  - <span data-ttu-id="42cd0-177">`[SkuName <String>]`: Nazwa SKU zasobu.</span><span class="sxs-lookup"><span data-stu-id="42cd0-177">`[SkuName <String>]`: Name of the resource SKU.</span></span>
  - <span data-ttu-id="42cd0-178">`[SkuSize <String>]`: Określenie rozmiaru jednostki SKU zasobu.</span><span class="sxs-lookup"><span data-stu-id="42cd0-178">`[SkuSize <String>]`: Size specifier of the resource SKU.</span></span>
  - <span data-ttu-id="42cd0-179">`[SkuTier <String>]`: Warstwa usługi SKU zasobu.</span><span class="sxs-lookup"><span data-stu-id="42cd0-179">`[SkuTier <String>]`: Service tier of the resource SKU.</span></span>
  - <span data-ttu-id="42cd0-180">`[SpotExpirationTime <DateTime?>]`: Czas wygaśnięcia farmy serwerów.</span><span class="sxs-lookup"><span data-stu-id="42cd0-180">`[SpotExpirationTime <DateTime?>]`: The time when the server farm expires.</span></span> <span data-ttu-id="42cd0-181">Ważne tylko w przypadku, gdy jest to farma serwera dodatkowego.</span><span class="sxs-lookup"><span data-stu-id="42cd0-181">Valid only if it is a spot server farm.</span></span>
  - <span data-ttu-id="42cd0-182">`[TargetWorkerCount <Int32?>]`: Liczba przeskalowania pracownika.</span><span class="sxs-lookup"><span data-stu-id="42cd0-182">`[TargetWorkerCount <Int32?>]`: Scaling worker count.</span></span>
  - <span data-ttu-id="42cd0-183">`[TargetWorkerSizeId <Int32?>]`: Skalowanie rozmiaru pracownika.</span><span class="sxs-lookup"><span data-stu-id="42cd0-183">`[TargetWorkerSizeId <Int32?>]`: Scaling worker size ID.</span></span>
  - <span data-ttu-id="42cd0-184">`[WorkerTierName <String>]`: Warstwa docelowa roboczego przypisana do planu usługi App Service.</span><span class="sxs-lookup"><span data-stu-id="42cd0-184">`[WorkerTierName <String>]`: Target worker tier assigned to the App Service plan.</span></span>

## <span data-ttu-id="42cd0-185">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="42cd0-185">RELATED LINKS</span></span>

