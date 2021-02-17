---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/remove-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
ms.openlocfilehash: 6668952ba07327482da7ed3c274eb003ac61c73c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180610"
---
# <span data-ttu-id="21773-101">Remove-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="21773-101">Remove-AzFunctionAppPlan</span></span>

## <span data-ttu-id="21773-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21773-102">SYNOPSIS</span></span>
<span data-ttu-id="21773-103">Usuwa plan aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="21773-103">Deletes a function app plan.</span></span>

## <span data-ttu-id="21773-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="21773-104">SYNTAX</span></span>

### <span data-ttu-id="21773-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="21773-105">ByName (Default)</span></span>
```
Remove-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="21773-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="21773-106">ByObjectInput</span></span>
```
Remove-AzFunctionAppPlan -InputObject <IAppServicePlan> [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="21773-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="21773-107">DESCRIPTION</span></span>
<span data-ttu-id="21773-108">Usuwa plan aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="21773-108">Deletes a function app plan.</span></span>

## <span data-ttu-id="21773-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="21773-109">EXAMPLES</span></span>

### <span data-ttu-id="21773-110">Przykład 1. Uzyskiwanie planu aplikacji funkcji według nazwy i usuwanie go.</span><span class="sxs-lookup"><span data-stu-id="21773-110">Example 1: Get a function app plan by name and delete it.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName | Remove-AzFunctionAppPlan -Force
```

<span data-ttu-id="21773-111">To polecenie pobiera plan aplikacji funkcji według nazwy i usuwa go.</span><span class="sxs-lookup"><span data-stu-id="21773-111">This command gets a function app plan by name and deletes it.</span></span>

### <span data-ttu-id="21773-112">Przykład 2. Usuwanie planu aplikacji funkcji według nazwy.</span><span class="sxs-lookup"><span data-stu-id="21773-112">Example 2: Delete a function app plan by name.</span></span>
```powershell
PS C:\> Remove-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

<span data-ttu-id="21773-113">To polecenie usuwa plan aplikacji funkcji według nazwy.</span><span class="sxs-lookup"><span data-stu-id="21773-113">This command deletes a function app plan by name.</span></span>

## <span data-ttu-id="21773-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21773-114">PARAMETERS</span></span>

### <span data-ttu-id="21773-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21773-115">-DefaultProfile</span></span>
<span data-ttu-id="21773-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="21773-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21773-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="21773-117">-Force</span></span>
<span data-ttu-id="21773-118">Wymusza usunięcie planu aplikacji funkcji przez polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="21773-118">Forces the cmdlet to remove the function app plan without prompting for confirmation.</span></span>

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

### <span data-ttu-id="21773-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21773-119">-InputObject</span></span>
<span data-ttu-id="21773-120">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach inputOBJECT i utworzyć tabelę skrótów.</span><span class="sxs-lookup"><span data-stu-id="21773-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="21773-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="21773-121">-Name</span></span>
<span data-ttu-id="21773-122">Nazwa aplikacji funkcji.</span><span class="sxs-lookup"><span data-stu-id="21773-122">The name of function app.</span></span>

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

### <span data-ttu-id="21773-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="21773-123">-PassThru</span></span>
<span data-ttu-id="21773-124">Zwraca wartość true, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="21773-124">Returns true when the command succeeds.</span></span>

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

### <span data-ttu-id="21773-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21773-125">-ResourceGroupName</span></span>


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

### <span data-ttu-id="21773-126">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="21773-126">-SubscriptionId</span></span>
<span data-ttu-id="21773-127">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="21773-127">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="21773-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="21773-128">-Confirm</span></span>
<span data-ttu-id="21773-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="21773-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21773-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21773-130">-WhatIf</span></span>
<span data-ttu-id="21773-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21773-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21773-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="21773-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21773-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21773-133">CommonParameters</span></span>
<span data-ttu-id="21773-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21773-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21773-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="21773-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21773-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21773-136">INPUTS</span></span>

### <span data-ttu-id="21773-137">Microsoft.Azure.PowerShell.Cmdlet.Functions.Models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="21773-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="21773-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="21773-138">OUTPUTS</span></span>

### <span data-ttu-id="21773-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="21773-139">System.Boolean</span></span>

## <span data-ttu-id="21773-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="21773-140">NOTES</span></span>

<span data-ttu-id="21773-141">ALIASY</span><span class="sxs-lookup"><span data-stu-id="21773-141">ALIASES</span></span>

<span data-ttu-id="21773-142">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="21773-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="21773-143">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="21773-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="21773-144">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="21773-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="21773-145">INPUTOBJECT: <IAppServicePlan></span><span class="sxs-lookup"><span data-stu-id="21773-145">INPUTOBJECT <IAppServicePlan>:</span></span> 
  - <span data-ttu-id="21773-146">`Location <String>`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="21773-146">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="21773-147">`[Kind <String>]`: Rodzaj zasobu.</span><span class="sxs-lookup"><span data-stu-id="21773-147">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="21773-148">`[Tag <IResourceTags>]`: tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="21773-148">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="21773-149">`[(Any) <String>]`: Wskazuje to, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="21773-149">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="21773-150">`[Capacity <Int32?>]`: Bieżąca liczba wystąpień przydzielonych do zasobu.</span><span class="sxs-lookup"><span data-stu-id="21773-150">`[Capacity <Int32?>]`: Current number of instances assigned to the resource.</span></span>
  - <span data-ttu-id="21773-151">`[FreeOfferExpirationTime <DateTime?>]`: czas wygaśnięcia oferty bezpłatnej farmy serwerów.</span><span class="sxs-lookup"><span data-stu-id="21773-151">`[FreeOfferExpirationTime <DateTime?>]`: The time when the server farm free offer expires.</span></span>
  - <span data-ttu-id="21773-152">`[HostingEnvironmentProfileId <String>]`: Identyfikator zasobu w środowisku usługi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="21773-152">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="21773-153">`[HyperV <Boolean?>]`: Jeśli plan usługi aplikacji kontenerowych Hyper-V — w <code>true</code> <code>false</code> przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="21773-153">`[HyperV <Boolean?>]`: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="21773-154">`[IsSpot <Boolean?>]`: Jeśli <code>true</code> ten plan usług aplikacji jest właścicielem wystąpień spotowych.</span><span class="sxs-lookup"><span data-stu-id="21773-154">`[IsSpot <Boolean?>]`: If <code>true</code>, this App Service Plan owns spot instances.</span></span>
  - <span data-ttu-id="21773-155">`[IsXenon <Boolean?>]`: Przestarzałe: Jeśli plan usługi aplikacji kontenerowych Hyper-V <code>true</code> — <code>false</code> w przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="21773-155">`[IsXenon <Boolean?>]`: Obsolete: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="21773-156">`[MaximumElasticWorkerCount <Int32?>]`: Maksymalna liczba pracowników dozwolonych w tym planie usługi aplikacjiScaleEnabled</span><span class="sxs-lookup"><span data-stu-id="21773-156">`[MaximumElasticWorkerCount <Int32?>]`: Maximum number of total workers allowed for this ElasticScaleEnabled App Service Plan</span></span>
  - <span data-ttu-id="21773-157">`[PerSiteScaling <Boolean?>]`: Jeśli aplikacje przypisane do tego planu usługi aplikacji <code>true</code> mogą być skalowane niezależnie.</span><span class="sxs-lookup"><span data-stu-id="21773-157">`[PerSiteScaling <Boolean?>]`: If <code>true</code>, apps assigned to this App Service plan can be scaled independently.</span></span>         <span data-ttu-id="21773-158">Jeśli aplikacje przypisane do tego planu usługi aplikacji zostaną przeskalowane <code>false</code> do wszystkich wystąpień planu.</span><span class="sxs-lookup"><span data-stu-id="21773-158">If <code>false</code>, apps assigned to this App Service plan will scale to all instances of the plan.</span></span>
  - <span data-ttu-id="21773-159">`[Reserved <Boolean?>]`: Jeśli plan usługi aplikacji dla systemu Linux <code>true</code> , <code>false</code> w przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="21773-159">`[Reserved <Boolean?>]`: If Linux app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="21773-160">`[SkuCapability <ICapability[]>]`: Czy włączono możliwości sKU, np. menedżer ruchu?</span><span class="sxs-lookup"><span data-stu-id="21773-160">`[SkuCapability <ICapability[]>]`: Capabilities of the SKU, e.g., is traffic manager enabled?</span></span>
    - <span data-ttu-id="21773-161">`[Name <String>]`: nazwa funkcji SKU.</span><span class="sxs-lookup"><span data-stu-id="21773-161">`[Name <String>]`: Name of the SKU capability.</span></span>
    - <span data-ttu-id="21773-162">`[Reason <String>]`: Przyczyna możliwości SKU.</span><span class="sxs-lookup"><span data-stu-id="21773-162">`[Reason <String>]`: Reason of the SKU capability.</span></span>
    - <span data-ttu-id="21773-163">`[Value <String>]`Wartość funkcji SKU.</span><span class="sxs-lookup"><span data-stu-id="21773-163">`[Value <String>]`: Value of the SKU capability.</span></span>
  - <span data-ttu-id="21773-164">`[SkuCapacityDefault <Int32?>]`: Domyślna liczba pracowników dla tego planu usługi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="21773-164">`[SkuCapacityDefault <Int32?>]`: Default number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="21773-165">`[SkuCapacityMaximum <Int32?>]`: Maksymalna liczba pracowników dla tego planu usługi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="21773-165">`[SkuCapacityMaximum <Int32?>]`: Maximum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="21773-166">`[SkuCapacityMinimum <Int32?>]`: Minimalna liczba pracowników dla tego planu usługi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="21773-166">`[SkuCapacityMinimum <Int32?>]`: Minimum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="21773-167">`[SkuCapacityScaleType <String>]`: Dostępne konfiguracje skali dla planu usługi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="21773-167">`[SkuCapacityScaleType <String>]`: Available scale configurations for an App Service plan.</span></span>
  - <span data-ttu-id="21773-168">`[SkuFamily <String>]`: Kod rodziny sku zasobu.</span><span class="sxs-lookup"><span data-stu-id="21773-168">`[SkuFamily <String>]`: Family code of the resource SKU.</span></span>
  - <span data-ttu-id="21773-169">`[SkuLocation <String[]>]`: lokalizacje sku.</span><span class="sxs-lookup"><span data-stu-id="21773-169">`[SkuLocation <String[]>]`: Locations of the SKU.</span></span>
  - <span data-ttu-id="21773-170">`[SkuName <String>]`: nazwa sku zasobu.</span><span class="sxs-lookup"><span data-stu-id="21773-170">`[SkuName <String>]`: Name of the resource SKU.</span></span>
  - <span data-ttu-id="21773-171">`[SkuSize <String>]`: Specyfikator rozmiaru sku zasobu.</span><span class="sxs-lookup"><span data-stu-id="21773-171">`[SkuSize <String>]`: Size specifier of the resource SKU.</span></span>
  - <span data-ttu-id="21773-172">`[SkuTier <String>]`: Warstwa usługi sku zasobu.</span><span class="sxs-lookup"><span data-stu-id="21773-172">`[SkuTier <String>]`: Service tier of the resource SKU.</span></span>
  - <span data-ttu-id="21773-173">`[SpotExpirationTime <DateTime?>]`: czas wygaśnięcia farmy serwerów.</span><span class="sxs-lookup"><span data-stu-id="21773-173">`[SpotExpirationTime <DateTime?>]`: The time when the server farm expires.</span></span> <span data-ttu-id="21773-174">Prawidłowy tylko w przypadku, gdy jest to farma serwerów spotowych.</span><span class="sxs-lookup"><span data-stu-id="21773-174">Valid only if it is a spot server farm.</span></span>
  - <span data-ttu-id="21773-175">`[TargetWorkerCount <Int32?>]`: skalowanie liczby pracowników.</span><span class="sxs-lookup"><span data-stu-id="21773-175">`[TargetWorkerCount <Int32?>]`: Scaling worker count.</span></span>
  - <span data-ttu-id="21773-176">`[TargetWorkerSizeId <Int32?>]`: skalowanie identyfikatora rozmiaru pracownika.</span><span class="sxs-lookup"><span data-stu-id="21773-176">`[TargetWorkerSizeId <Int32?>]`: Scaling worker size ID.</span></span>
  - <span data-ttu-id="21773-177">`[WorkerTierName <String>]`: Warstwa docelowa pracownika przypisana do planu usługi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="21773-177">`[WorkerTierName <String>]`: Target worker tier assigned to the App Service plan.</span></span>

## <span data-ttu-id="21773-178">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="21773-178">RELATED LINKS</span></span>

