---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/remove-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
ms.openlocfilehash: 6668952ba07327482da7ed3c274eb003ac61c73c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326774"
---
# <span data-ttu-id="0b9be-101">Remove-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="0b9be-101">Remove-AzFunctionAppPlan</span></span>

## <span data-ttu-id="0b9be-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0b9be-102">SYNOPSIS</span></span>
<span data-ttu-id="0b9be-103">Usuwa plan aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="0b9be-103">Deletes a function app plan.</span></span>

## <span data-ttu-id="0b9be-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0b9be-104">SYNTAX</span></span>

### <span data-ttu-id="0b9be-105">ByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0b9be-105">ByName (Default)</span></span>
```
Remove-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0b9be-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="0b9be-106">ByObjectInput</span></span>
```
Remove-AzFunctionAppPlan -InputObject <IAppServicePlan> [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0b9be-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0b9be-107">DESCRIPTION</span></span>
<span data-ttu-id="0b9be-108">Usuwa plan aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="0b9be-108">Deletes a function app plan.</span></span>

## <span data-ttu-id="0b9be-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0b9be-109">EXAMPLES</span></span>

### <span data-ttu-id="0b9be-110">Przykład 1: Uzyskaj plan aplikacji funkcji według nazwy i usuń go.</span><span class="sxs-lookup"><span data-stu-id="0b9be-110">Example 1: Get a function app plan by name and delete it.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName | Remove-AzFunctionAppPlan -Force
```

<span data-ttu-id="0b9be-111">To polecenie pobiera plan aplikacji o nazwie i usuwa go.</span><span class="sxs-lookup"><span data-stu-id="0b9be-111">This command gets a function app plan by name and deletes it.</span></span>

### <span data-ttu-id="0b9be-112">Przykład 2: usuwanie planu aplikacji funkcji według nazwy.</span><span class="sxs-lookup"><span data-stu-id="0b9be-112">Example 2: Delete a function app plan by name.</span></span>
```powershell
PS C:\> Remove-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

<span data-ttu-id="0b9be-113">To polecenie usuwa plan aplikacji funkcji według nazwy.</span><span class="sxs-lookup"><span data-stu-id="0b9be-113">This command deletes a function app plan by name.</span></span>

## <span data-ttu-id="0b9be-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0b9be-114">PARAMETERS</span></span>

### <span data-ttu-id="0b9be-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b9be-115">-DefaultProfile</span></span>
<span data-ttu-id="0b9be-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0b9be-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b9be-117">-Force</span><span class="sxs-lookup"><span data-stu-id="0b9be-117">-Force</span></span>
<span data-ttu-id="0b9be-118">Wymusza usunięcie funkcji polecenia cmdlet z planu aplikacji bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0b9be-118">Forces the cmdlet to remove the function app plan without prompting for confirmation.</span></span>

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

### <span data-ttu-id="0b9be-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0b9be-119">-InputObject</span></span>
<span data-ttu-id="0b9be-120">Aby skonstruować, zobacz sekcję notatki dla właściwości INPUTobject i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="0b9be-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0b9be-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0b9be-121">-Name</span></span>
<span data-ttu-id="0b9be-122">Nazwa aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="0b9be-122">The name of function app.</span></span>

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

### <span data-ttu-id="0b9be-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0b9be-123">-PassThru</span></span>
<span data-ttu-id="0b9be-124">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="0b9be-124">Returns true when the command succeeds.</span></span>

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

### <span data-ttu-id="0b9be-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b9be-125">-ResourceGroupName</span></span>


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

### <span data-ttu-id="0b9be-126">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="0b9be-126">-SubscriptionId</span></span>
<span data-ttu-id="0b9be-127">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0b9be-127">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="0b9be-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0b9be-128">-Confirm</span></span>
<span data-ttu-id="0b9be-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b9be-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b9be-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b9be-130">-WhatIf</span></span>
<span data-ttu-id="0b9be-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b9be-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b9be-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0b9be-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b9be-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b9be-133">CommonParameters</span></span>
<span data-ttu-id="0b9be-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b9be-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b9be-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b9be-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b9be-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0b9be-136">INPUTS</span></span>

### <span data-ttu-id="0b9be-137">Microsoft. Azure. PowerShell. polecenia. Functions. models. Api20190801. IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0b9be-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="0b9be-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0b9be-138">OUTPUTS</span></span>

### <span data-ttu-id="0b9be-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0b9be-139">System.Boolean</span></span>

## <span data-ttu-id="0b9be-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0b9be-140">NOTES</span></span>

<span data-ttu-id="0b9be-141">PISUJE</span><span class="sxs-lookup"><span data-stu-id="0b9be-141">ALIASES</span></span>

<span data-ttu-id="0b9be-142">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0b9be-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0b9be-143">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="0b9be-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0b9be-144">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0b9be-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0b9be-145">INPUTobject <IAppServicePlan> :</span><span class="sxs-lookup"><span data-stu-id="0b9be-145">INPUTOBJECT <IAppServicePlan>:</span></span> 
  - <span data-ttu-id="0b9be-146">`Location <String>`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="0b9be-146">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="0b9be-147">`[Kind <String>]`: Rodzaj zasobu.</span><span class="sxs-lookup"><span data-stu-id="0b9be-147">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="0b9be-148">`[Tag <IResourceTags>]`: Znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="0b9be-148">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="0b9be-149">`[(Any) <String>]`: Wskazuje, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="0b9be-149">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="0b9be-150">`[Capacity <Int32?>]`: Bieżąca liczba wystąpień przydzielonych do zasobu.</span><span class="sxs-lookup"><span data-stu-id="0b9be-150">`[Capacity <Int32?>]`: Current number of instances assigned to the resource.</span></span>
  - <span data-ttu-id="0b9be-151">`[FreeOfferExpirationTime <DateTime?>]`: Czas wygaśnięcia bezpłatnej oferty farmy serwerów.</span><span class="sxs-lookup"><span data-stu-id="0b9be-151">`[FreeOfferExpirationTime <DateTime?>]`: The time when the server farm free offer expires.</span></span>
  - <span data-ttu-id="0b9be-152">`[HostingEnvironmentProfileId <String>]`: Identyfikator zasobu środowiska App Service Environment.</span><span class="sxs-lookup"><span data-stu-id="0b9be-152">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="0b9be-153">`[HyperV <Boolean?>]`: Jeśli plan usługi App Service kontener funkcji Hyper-V jest <code>true</code> <code>false</code> inny, w przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="0b9be-153">`[HyperV <Boolean?>]`: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="0b9be-154">`[IsSpot <Boolean?>]`: Jeśli <code>true</code> ten plan usługi App Service jest właścicielem wystąpień dodatkowych.</span><span class="sxs-lookup"><span data-stu-id="0b9be-154">`[IsSpot <Boolean?>]`: If <code>true</code>, this App Service Plan owns spot instances.</span></span>
  - <span data-ttu-id="0b9be-155">`[IsXenon <Boolean?>]`: Przestarzałe: Jeśli plan usługi App Service kontener funkcji Hyper-V jest <code>true</code> <code>false</code> inny, w przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="0b9be-155">`[IsXenon <Boolean?>]`: Obsolete: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="0b9be-156">`[MaximumElasticWorkerCount <Int32?>]`: Maksymalna liczba wszystkich pracowników dozwolonych dla tego planu usługi App Service ElasticScaleEnabled</span><span class="sxs-lookup"><span data-stu-id="0b9be-156">`[MaximumElasticWorkerCount <Int32?>]`: Maximum number of total workers allowed for this ElasticScaleEnabled App Service Plan</span></span>
  - <span data-ttu-id="0b9be-157">`[PerSiteScaling <Boolean?>]`: Jeśli <code>true</code> aplikacje przydzielone do tego planu usługi App Service mogą być skalowane niezależnie.</span><span class="sxs-lookup"><span data-stu-id="0b9be-157">`[PerSiteScaling <Boolean?>]`: If <code>true</code>, apps assigned to this App Service plan can be scaled independently.</span></span>         <span data-ttu-id="0b9be-158">Jeśli <code>false</code> aplikacje przydzielone do tego planu usługi App Service będą skalowane do wszystkich wystąpień planu.</span><span class="sxs-lookup"><span data-stu-id="0b9be-158">If <code>false</code>, apps assigned to this App Service plan will scale to all instances of the plan.</span></span>
  - <span data-ttu-id="0b9be-159">`[Reserved <Boolean?>]`: Jeśli plan usługi Linux App Service jest <code>true</code> <code>false</code> inny, w przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="0b9be-159">`[Reserved <Boolean?>]`: If Linux app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="0b9be-160">`[SkuCapability <ICapability[]>]`: Funkcje jednostki SKU, na przykład, są włączone w usłudze Traffic Manager?</span><span class="sxs-lookup"><span data-stu-id="0b9be-160">`[SkuCapability <ICapability[]>]`: Capabilities of the SKU, e.g., is traffic manager enabled?</span></span>
    - <span data-ttu-id="0b9be-161">`[Name <String>]`: Nazwa funkcji SKU.</span><span class="sxs-lookup"><span data-stu-id="0b9be-161">`[Name <String>]`: Name of the SKU capability.</span></span>
    - <span data-ttu-id="0b9be-162">`[Reason <String>]`: Przyczyna funkcji SKU.</span><span class="sxs-lookup"><span data-stu-id="0b9be-162">`[Reason <String>]`: Reason of the SKU capability.</span></span>
    - <span data-ttu-id="0b9be-163">`[Value <String>]`: Wartość funkcji SKU.</span><span class="sxs-lookup"><span data-stu-id="0b9be-163">`[Value <String>]`: Value of the SKU capability.</span></span>
  - <span data-ttu-id="0b9be-164">`[SkuCapacityDefault <Int32?>]`: Domyślna liczba pracowników tej jednostki SKU planu usługi App Service.</span><span class="sxs-lookup"><span data-stu-id="0b9be-164">`[SkuCapacityDefault <Int32?>]`: Default number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="0b9be-165">`[SkuCapacityMaximum <Int32?>]`: Maksymalna liczba pracowników tej jednostki SKU planu usługi App Service.</span><span class="sxs-lookup"><span data-stu-id="0b9be-165">`[SkuCapacityMaximum <Int32?>]`: Maximum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="0b9be-166">`[SkuCapacityMinimum <Int32?>]`: Minimalna liczba pracowników dla tej jednostki SKU planu usługi App Service.</span><span class="sxs-lookup"><span data-stu-id="0b9be-166">`[SkuCapacityMinimum <Int32?>]`: Minimum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="0b9be-167">`[SkuCapacityScaleType <String>]`: Dostępne konfiguracje skali dla planu usługi App Service.</span><span class="sxs-lookup"><span data-stu-id="0b9be-167">`[SkuCapacityScaleType <String>]`: Available scale configurations for an App Service plan.</span></span>
  - <span data-ttu-id="0b9be-168">`[SkuFamily <String>]`: Kod rodziny w wersji SKU zasobu.</span><span class="sxs-lookup"><span data-stu-id="0b9be-168">`[SkuFamily <String>]`: Family code of the resource SKU.</span></span>
  - <span data-ttu-id="0b9be-169">`[SkuLocation <String[]>]`: Lokalizacje jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="0b9be-169">`[SkuLocation <String[]>]`: Locations of the SKU.</span></span>
  - <span data-ttu-id="0b9be-170">`[SkuName <String>]`: Nazwa SKU zasobu.</span><span class="sxs-lookup"><span data-stu-id="0b9be-170">`[SkuName <String>]`: Name of the resource SKU.</span></span>
  - <span data-ttu-id="0b9be-171">`[SkuSize <String>]`: Określenie rozmiaru jednostki SKU zasobu.</span><span class="sxs-lookup"><span data-stu-id="0b9be-171">`[SkuSize <String>]`: Size specifier of the resource SKU.</span></span>
  - <span data-ttu-id="0b9be-172">`[SkuTier <String>]`: Warstwa usługi SKU zasobu.</span><span class="sxs-lookup"><span data-stu-id="0b9be-172">`[SkuTier <String>]`: Service tier of the resource SKU.</span></span>
  - <span data-ttu-id="0b9be-173">`[SpotExpirationTime <DateTime?>]`: Czas wygaśnięcia farmy serwerów.</span><span class="sxs-lookup"><span data-stu-id="0b9be-173">`[SpotExpirationTime <DateTime?>]`: The time when the server farm expires.</span></span> <span data-ttu-id="0b9be-174">Ważne tylko w przypadku, gdy jest to farma serwera dodatkowego.</span><span class="sxs-lookup"><span data-stu-id="0b9be-174">Valid only if it is a spot server farm.</span></span>
  - <span data-ttu-id="0b9be-175">`[TargetWorkerCount <Int32?>]`: Liczba przeskalowania pracownika.</span><span class="sxs-lookup"><span data-stu-id="0b9be-175">`[TargetWorkerCount <Int32?>]`: Scaling worker count.</span></span>
  - <span data-ttu-id="0b9be-176">`[TargetWorkerSizeId <Int32?>]`: Skalowanie rozmiaru pracownika.</span><span class="sxs-lookup"><span data-stu-id="0b9be-176">`[TargetWorkerSizeId <Int32?>]`: Scaling worker size ID.</span></span>
  - <span data-ttu-id="0b9be-177">`[WorkerTierName <String>]`: Warstwa docelowa roboczego przypisana do planu usługi App Service.</span><span class="sxs-lookup"><span data-stu-id="0b9be-177">`[WorkerTierName <String>]`: Target worker tier assigned to the App Service plan.</span></span>

## <span data-ttu-id="0b9be-178">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0b9be-178">RELATED LINKS</span></span>

