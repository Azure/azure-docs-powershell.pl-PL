---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/new-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
ms.openlocfilehash: 7f91fee2e8cc772be291662af325fd87edebdfd9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181154"
---
# <span data-ttu-id="7a358-101">New-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="7a358-101">New-AzCustomProvider</span></span>

## <span data-ttu-id="7a358-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a358-102">SYNOPSIS</span></span>
<span data-ttu-id="7a358-103">Tworzy lub aktualizuje niestandardowego dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="7a358-103">Creates or updates the custom resource provider.</span></span>

## <span data-ttu-id="7a358-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7a358-104">SYNTAX</span></span>

```
New-AzCustomProvider -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Action <ICustomRpActionRouteDefinition[]>] [-ResourceType <ICustomRpResourceTypeRouteDefinition[]>]
 [-Tag <Hashtable>] [-Validation <ICustomRpValidations[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7a358-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="7a358-105">DESCRIPTION</span></span>
<span data-ttu-id="7a358-106">Tworzy lub aktualizuje niestandardowego dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="7a358-106">Creates or updates the custom resource provider.</span></span>

## <span data-ttu-id="7a358-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7a358-107">EXAMPLES</span></span>

### <span data-ttu-id="7a358-108">Przykład 1. Tworzenie dostawcy niestandardowego</span><span class="sxs-lookup"><span data-stu-id="7a358-108">Example 1: Create a custom provider</span></span>
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}


Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="7a358-109">Tworzenie niestandardowego dostawcy zasobów</span><span class="sxs-lookup"><span data-stu-id="7a358-109">Create a custom resource provider</span></span>

### <span data-ttu-id="7a358-110">Przykład 2. Tworzenie dostawcy niestandardowego ze skojarzeniami</span><span class="sxs-lookup"><span data-stu-id="7a358-110">Example 2: Create a custom provider with associations</span></span>
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace2.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}, @{Name="Associations"; Endpoint="https://contoso.com/myService", RoutingType="Proxy,Cache,Extension"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace2.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="7a358-111">Utwórz dostawcę niestandardowego z trasą dla niestandardowych skojarzeń dostawców.</span><span class="sxs-lookup"><span data-stu-id="7a358-111">Create a custom provider, with a route for Custom provider associations.</span></span>

## <span data-ttu-id="7a358-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a358-112">PARAMETERS</span></span>

### <span data-ttu-id="7a358-113">— akcja</span><span class="sxs-lookup"><span data-stu-id="7a358-113">-Action</span></span>
<span data-ttu-id="7a358-114">Lista akcji implementnych przez dostawcę zasobów niestandardowych.</span><span class="sxs-lookup"><span data-stu-id="7a358-114">A list of actions that the custom resource provider implements.</span></span>
<span data-ttu-id="7a358-115">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach AKCJI i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="7a358-115">To construct, see NOTES section for ACTION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpActionRouteDefinition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a358-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="7a358-116">-AsJob</span></span>
<span data-ttu-id="7a358-117">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="7a358-117">Run the command as a job</span></span>

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

### <span data-ttu-id="7a358-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a358-118">-DefaultProfile</span></span>
<span data-ttu-id="7a358-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7a358-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a358-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="7a358-120">-Location</span></span>
<span data-ttu-id="7a358-121">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="7a358-121">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a358-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7a358-122">-Name</span></span>
<span data-ttu-id="7a358-123">Nazwa dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7a358-123">The name of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a358-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7a358-124">-NoWait</span></span>
<span data-ttu-id="7a358-125">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="7a358-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7a358-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a358-126">-ResourceGroupName</span></span>
<span data-ttu-id="7a358-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7a358-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a358-128">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="7a358-128">-ResourceType</span></span>
<span data-ttu-id="7a358-129">Lista typów zasobów zaimplementowanych przez niestandardowego dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="7a358-129">A list of resource types that the custom resource provider implements.</span></span>
<span data-ttu-id="7a358-130">Aby skonstruować, zobacz sekcję NOTES, aby uzyskać informacje o właściwościach RESOURCETYPE i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="7a358-130">To construct, see NOTES section for RESOURCETYPE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpResourceTypeRouteDefinition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a358-131">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7a358-131">-SubscriptionId</span></span>
<span data-ttu-id="7a358-132">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7a358-132">The Azure subscription ID.</span></span>
<span data-ttu-id="7a358-133">Jest to ciąg w formacie GUID (np. 000000000-0000-0000-0000-0000000000000)</span><span class="sxs-lookup"><span data-stu-id="7a358-133">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a358-134">— Tag</span><span class="sxs-lookup"><span data-stu-id="7a358-134">-Tag</span></span>
<span data-ttu-id="7a358-135">Tagi zasobów</span><span class="sxs-lookup"><span data-stu-id="7a358-135">Resource tags</span></span>

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

### <span data-ttu-id="7a358-136">— Sprawdzanie poprawności</span><span class="sxs-lookup"><span data-stu-id="7a358-136">-Validation</span></span>
<span data-ttu-id="7a358-137">Lista sprawdzania poprawności, które mają być uruchamiane na żądaniach niestandardowego dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7a358-137">A list of validations to run on the custom resource provider's requests.</span></span>
<span data-ttu-id="7a358-138">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach sprawdzania poprawności i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="7a358-138">To construct, see NOTES section for VALIDATION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpValidations[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a358-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7a358-139">-Confirm</span></span>
<span data-ttu-id="7a358-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7a358-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a358-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a358-141">-WhatIf</span></span>
<span data-ttu-id="7a358-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a358-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a358-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7a358-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a358-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a358-144">CommonParameters</span></span>
<span data-ttu-id="7a358-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a358-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a358-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a358-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a358-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a358-147">INPUTS</span></span>

## <span data-ttu-id="7a358-148">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a358-148">OUTPUTS</span></span>

### <span data-ttu-id="7a358-149">Microsoft.Azure.PowerShell.cmdlet.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="7a358-149">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="7a358-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7a358-150">NOTES</span></span>

<span data-ttu-id="7a358-151">ALIASY</span><span class="sxs-lookup"><span data-stu-id="7a358-151">ALIASES</span></span>

<span data-ttu-id="7a358-152">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7a358-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7a358-153">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="7a358-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7a358-154">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7a358-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7a358-155">ACTION <ICustomRpActionRouteDefinition[]>: lista akcji implementowania przez dostawcę zasobów niestandardowych.</span><span class="sxs-lookup"><span data-stu-id="7a358-155">ACTION <ICustomRpActionRouteDefinition[]>: A list of actions that the custom resource provider implements.</span></span>
  - <span data-ttu-id="7a358-156">`Endpoint <String>`: URI punktu końcowego definicji trasy, do których dostawca zasobów niestandardowych będzie żądał serwera proxy.</span><span class="sxs-lookup"><span data-stu-id="7a358-156">`Endpoint <String>`: The route definition endpoint URI that the custom resource provider will proxy requests to.</span></span> <span data-ttu-id="7a358-157">Może to być w postaci płaskiego URI (np. ' ') lub określić trasę za pomocą ścieżki https://testendpoint/ (np. ' https://testendpoint/{requestPath} ')</span><span class="sxs-lookup"><span data-stu-id="7a358-157">This can be in the form of a flat URI (e.g. 'https://testendpoint/') or can specify to route via a path (e.g. 'https://testendpoint/{requestPath}')</span></span>
  - <span data-ttu-id="7a358-158">`Name <String>`: nazwa definicji trasy.</span><span class="sxs-lookup"><span data-stu-id="7a358-158">`Name <String>`: The name of the route definition.</span></span> <span data-ttu-id="7a358-159">Stanie się to nazwą rozszerzenia ARM (np. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span><span class="sxs-lookup"><span data-stu-id="7a358-159">This becomes the name for the ARM extension (e.g. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span></span>
  - <span data-ttu-id="7a358-160">`[RoutingType <ActionRouting?>]`: Typy routingu obsługiwane w żądaniach akcji.</span><span class="sxs-lookup"><span data-stu-id="7a358-160">`[RoutingType <ActionRouting?>]`: The routing types that are supported for action requests.</span></span>

<span data-ttu-id="7a358-161">RESOURCETYPE <ICustomRpResourceTypeRouteDefinition[]>: lista typów zasobów implementowania przez niestandardowego dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="7a358-161">RESOURCETYPE <ICustomRpResourceTypeRouteDefinition[]>: A list of resource types that the custom resource provider implements.</span></span>
  - <span data-ttu-id="7a358-162">`Endpoint <String>`: URI punktu końcowego definicji trasy, do których dostawca zasobów niestandardowych będzie żądał serwera proxy.</span><span class="sxs-lookup"><span data-stu-id="7a358-162">`Endpoint <String>`: The route definition endpoint URI that the custom resource provider will proxy requests to.</span></span> <span data-ttu-id="7a358-163">Może to być w postaci płaskiego URI (np. ' ') lub określić trasę za pomocą ścieżki https://testendpoint/ (np. ' https://testendpoint/{requestPath} ')</span><span class="sxs-lookup"><span data-stu-id="7a358-163">This can be in the form of a flat URI (e.g. 'https://testendpoint/') or can specify to route via a path (e.g. 'https://testendpoint/{requestPath}')</span></span>
  - <span data-ttu-id="7a358-164">`Name <String>`: nazwa definicji trasy.</span><span class="sxs-lookup"><span data-stu-id="7a358-164">`Name <String>`: The name of the route definition.</span></span> <span data-ttu-id="7a358-165">Stanie się to nazwą rozszerzenia ARM (np. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span><span class="sxs-lookup"><span data-stu-id="7a358-165">This becomes the name for the ARM extension (e.g. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span></span>
  - <span data-ttu-id="7a358-166">`[RoutingType <ResourceTypeRouting?>]`: Typy routingu obsługiwane dla żądań zasobów.</span><span class="sxs-lookup"><span data-stu-id="7a358-166">`[RoutingType <ResourceTypeRouting?>]`: The routing types that are supported for resource requests.</span></span>

<span data-ttu-id="7a358-167">SPRAWDZANIE <ICustomRpValidations[]>: lista sprawdzania poprawności, które mają być uruchamiane na żądaniach niestandardowego dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7a358-167">VALIDATION <ICustomRpValidations[]>: A list of validations to run on the custom resource provider's requests.</span></span>
  - <span data-ttu-id="7a358-168">`Specification <String>`: Link do specyfikacji sprawdzania poprawności.</span><span class="sxs-lookup"><span data-stu-id="7a358-168">`Specification <String>`: A link to the validation specification.</span></span> <span data-ttu-id="7a358-169">Specyfikacja musi być hostowana w raw.githubusercontent.com.</span><span class="sxs-lookup"><span data-stu-id="7a358-169">The specification must be hosted on raw.githubusercontent.com.</span></span>
  - <span data-ttu-id="7a358-170">`[ValidationType <ValidationType?>]`: typ sprawdzania poprawności, który ma być uruchamiany względem zgodnego żądania.</span><span class="sxs-lookup"><span data-stu-id="7a358-170">`[ValidationType <ValidationType?>]`: The type of validation to run against a matching request.</span></span>

## <span data-ttu-id="7a358-171">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7a358-171">RELATED LINKS</span></span>

