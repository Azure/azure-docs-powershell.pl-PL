---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/new-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
ms.openlocfilehash: 7f91fee2e8cc772be291662af325fd87edebdfd9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94306697"
---
# <span data-ttu-id="4cf67-101">New-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="4cf67-101">New-AzCustomProvider</span></span>

## <span data-ttu-id="4cf67-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4cf67-102">SYNOPSIS</span></span>
<span data-ttu-id="4cf67-103">Umożliwia utworzenie lub zaktualizowanie niestandardowego dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4cf67-103">Creates or updates the custom resource provider.</span></span>

## <span data-ttu-id="4cf67-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4cf67-104">SYNTAX</span></span>

```
New-AzCustomProvider -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Action <ICustomRpActionRouteDefinition[]>] [-ResourceType <ICustomRpResourceTypeRouteDefinition[]>]
 [-Tag <Hashtable>] [-Validation <ICustomRpValidations[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4cf67-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4cf67-105">DESCRIPTION</span></span>
<span data-ttu-id="4cf67-106">Umożliwia utworzenie lub zaktualizowanie niestandardowego dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4cf67-106">Creates or updates the custom resource provider.</span></span>

## <span data-ttu-id="4cf67-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4cf67-107">EXAMPLES</span></span>

### <span data-ttu-id="4cf67-108">Przykład 1. Tworzenie dostawcy niestandardowego</span><span class="sxs-lookup"><span data-stu-id="4cf67-108">Example 1: Create a custom provider</span></span>
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}


Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="4cf67-109">Tworzenie niestandardowego dostawcy zasobów</span><span class="sxs-lookup"><span data-stu-id="4cf67-109">Create a custom resource provider</span></span>

### <span data-ttu-id="4cf67-110">Przykład 2: Tworzenie niestandardowego dostawcy ze skojarzeniami</span><span class="sxs-lookup"><span data-stu-id="4cf67-110">Example 2: Create a custom provider with associations</span></span>
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace2.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}, @{Name="Associations"; Endpoint="https://contoso.com/myService", RoutingType="Proxy,Cache,Extension"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace2.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="4cf67-111">Utwórz dostawcę niestandardowego z trasą dla skojarzeń dostawców niestandardowych.</span><span class="sxs-lookup"><span data-stu-id="4cf67-111">Create a custom provider, with a route for Custom provider associations.</span></span>

## <span data-ttu-id="4cf67-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4cf67-112">PARAMETERS</span></span>

### <span data-ttu-id="4cf67-113">-Action</span><span class="sxs-lookup"><span data-stu-id="4cf67-113">-Action</span></span>
<span data-ttu-id="4cf67-114">Lista akcji implementowanych przez dostawcę zasobów niestandardowych.</span><span class="sxs-lookup"><span data-stu-id="4cf67-114">A list of actions that the custom resource provider implements.</span></span>
<span data-ttu-id="4cf67-115">Aby skonstruować, zobacz sekcję notatki dla właściwości akcji i Utwórz tabelę skrótów.</span><span class="sxs-lookup"><span data-stu-id="4cf67-115">To construct, see NOTES section for ACTION properties and create a hash table.</span></span>

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

### <span data-ttu-id="4cf67-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4cf67-116">-AsJob</span></span>
<span data-ttu-id="4cf67-117">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="4cf67-117">Run the command as a job</span></span>

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

### <span data-ttu-id="4cf67-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cf67-118">-DefaultProfile</span></span>
<span data-ttu-id="4cf67-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4cf67-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cf67-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="4cf67-120">-Location</span></span>
<span data-ttu-id="4cf67-121">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="4cf67-121">Resource location</span></span>

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

### <span data-ttu-id="4cf67-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4cf67-122">-Name</span></span>
<span data-ttu-id="4cf67-123">Nazwa dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4cf67-123">The name of the resource provider.</span></span>

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

### <span data-ttu-id="4cf67-124">-Nowait</span><span class="sxs-lookup"><span data-stu-id="4cf67-124">-NoWait</span></span>
<span data-ttu-id="4cf67-125">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="4cf67-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4cf67-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cf67-126">-ResourceGroupName</span></span>
<span data-ttu-id="4cf67-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4cf67-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="4cf67-128">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="4cf67-128">-ResourceType</span></span>
<span data-ttu-id="4cf67-129">Lista typów zasobów implementowanych przez niestandardowego dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="4cf67-129">A list of resource types that the custom resource provider implements.</span></span>
<span data-ttu-id="4cf67-130">Aby skonstruować, zobacz sekcję notatki dla właściwości ResourceType i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="4cf67-130">To construct, see NOTES section for RESOURCETYPE properties and create a hash table.</span></span>

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

### <span data-ttu-id="4cf67-131">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="4cf67-131">-SubscriptionId</span></span>
<span data-ttu-id="4cf67-132">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4cf67-132">The Azure subscription ID.</span></span>
<span data-ttu-id="4cf67-133">Jest to ciąg sformatowany przy użyciu identyfikatora GUID (na przykład 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="4cf67-133">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="4cf67-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="4cf67-134">-Tag</span></span>
<span data-ttu-id="4cf67-135">Znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="4cf67-135">Resource tags</span></span>

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

### <span data-ttu-id="4cf67-136">— Sprawdzanie poprawności</span><span class="sxs-lookup"><span data-stu-id="4cf67-136">-Validation</span></span>
<span data-ttu-id="4cf67-137">Lista funkcji sprawdzania poprawności, które mają być uruchamiane na żądaniach niestandardowych dostawców zasobów.</span><span class="sxs-lookup"><span data-stu-id="4cf67-137">A list of validations to run on the custom resource provider's requests.</span></span>
<span data-ttu-id="4cf67-138">Aby skonstruować, zobacz sekcję notatki dla właściwości sprawdzania poprawności i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="4cf67-138">To construct, see NOTES section for VALIDATION properties and create a hash table.</span></span>

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

### <span data-ttu-id="4cf67-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4cf67-139">-Confirm</span></span>
<span data-ttu-id="4cf67-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cf67-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cf67-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cf67-141">-WhatIf</span></span>
<span data-ttu-id="4cf67-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cf67-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cf67-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4cf67-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cf67-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cf67-144">CommonParameters</span></span>
<span data-ttu-id="4cf67-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cf67-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cf67-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4cf67-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cf67-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4cf67-147">INPUTS</span></span>

## <span data-ttu-id="4cf67-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4cf67-148">OUTPUTS</span></span>

### <span data-ttu-id="4cf67-149">Microsoft. Azure. PowerShell. polecenia. CustomProviders. models. Api20180901Preview. ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="4cf67-149">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="4cf67-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4cf67-150">NOTES</span></span>

<span data-ttu-id="4cf67-151">PISUJE</span><span class="sxs-lookup"><span data-stu-id="4cf67-151">ALIASES</span></span>

<span data-ttu-id="4cf67-152">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4cf67-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4cf67-153">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="4cf67-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4cf67-154">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4cf67-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4cf67-155">ACTION <ICustomRpActionRouteDefinition [] >: lista akcji, które implementuje dostawca zasobów niestandardowych.</span><span class="sxs-lookup"><span data-stu-id="4cf67-155">ACTION <ICustomRpActionRouteDefinition[]>: A list of actions that the custom resource provider implements.</span></span>
  - <span data-ttu-id="4cf67-156">`Endpoint <String>`: Identyfikator URI punktu końcowego definicji trasy, do którego dostawca zasobów jest żądaniem serwera proxy.</span><span class="sxs-lookup"><span data-stu-id="4cf67-156">`Endpoint <String>`: The route definition endpoint URI that the custom resource provider will proxy requests to.</span></span> <span data-ttu-id="4cf67-157">Może to być w postaci płaskiego identyfikatora URI (na przykład ' https://testendpoint/ ') lub może określać trasę za pośrednictwem ścieżki (na przykład ' https://testendpoint/{requestPath} ').</span><span class="sxs-lookup"><span data-stu-id="4cf67-157">This can be in the form of a flat URI (e.g. 'https://testendpoint/') or can specify to route via a path (e.g. 'https://testendpoint/{requestPath}')</span></span>
  - <span data-ttu-id="4cf67-158">`Name <String>`: Nazwa definicji trasy.</span><span class="sxs-lookup"><span data-stu-id="4cf67-158">`Name <String>`: The name of the route definition.</span></span> <span data-ttu-id="4cf67-159">To jest nazwa rozszerzenia ARM (na przykład "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}")</span><span class="sxs-lookup"><span data-stu-id="4cf67-159">This becomes the name for the ARM extension (e.g. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span></span>
  - <span data-ttu-id="4cf67-160">`[RoutingType <ActionRouting?>]`: Typy routingu obsługiwane w przypadku żądań akcji.</span><span class="sxs-lookup"><span data-stu-id="4cf67-160">`[RoutingType <ActionRouting?>]`: The routing types that are supported for action requests.</span></span>

<span data-ttu-id="4cf67-161">ResourceType <ICustomRpResourceTypeRouteDefinition [] >: Lista typów zasobów implementowanych przez niestandardowego dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="4cf67-161">RESOURCETYPE <ICustomRpResourceTypeRouteDefinition[]>: A list of resource types that the custom resource provider implements.</span></span>
  - <span data-ttu-id="4cf67-162">`Endpoint <String>`: Identyfikator URI punktu końcowego definicji trasy, do którego dostawca zasobów jest żądaniem serwera proxy.</span><span class="sxs-lookup"><span data-stu-id="4cf67-162">`Endpoint <String>`: The route definition endpoint URI that the custom resource provider will proxy requests to.</span></span> <span data-ttu-id="4cf67-163">Może to być w postaci płaskiego identyfikatora URI (na przykład ' https://testendpoint/ ') lub może określać trasę za pośrednictwem ścieżki (na przykład ' https://testendpoint/{requestPath} ').</span><span class="sxs-lookup"><span data-stu-id="4cf67-163">This can be in the form of a flat URI (e.g. 'https://testendpoint/') or can specify to route via a path (e.g. 'https://testendpoint/{requestPath}')</span></span>
  - <span data-ttu-id="4cf67-164">`Name <String>`: Nazwa definicji trasy.</span><span class="sxs-lookup"><span data-stu-id="4cf67-164">`Name <String>`: The name of the route definition.</span></span> <span data-ttu-id="4cf67-165">To jest nazwa rozszerzenia ARM (na przykład "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}")</span><span class="sxs-lookup"><span data-stu-id="4cf67-165">This becomes the name for the ARM extension (e.g. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span></span>
  - <span data-ttu-id="4cf67-166">`[RoutingType <ResourceTypeRouting?>]`: Typy routingu obsługiwane dla żądań zasobów.</span><span class="sxs-lookup"><span data-stu-id="4cf67-166">`[RoutingType <ResourceTypeRouting?>]`: The routing types that are supported for resource requests.</span></span>

<span data-ttu-id="4cf67-167">VALIDATION <ICustomRpValidations [] >: Lista funkcji sprawdzania poprawności, które mają zostać uruchomione na żądaniach niestandardowych dostawców zasobów.</span><span class="sxs-lookup"><span data-stu-id="4cf67-167">VALIDATION <ICustomRpValidations[]>: A list of validations to run on the custom resource provider's requests.</span></span>
  - <span data-ttu-id="4cf67-168">`Specification <String>`: Łącze do specyfikacji sprawdzania poprawności.</span><span class="sxs-lookup"><span data-stu-id="4cf67-168">`Specification <String>`: A link to the validation specification.</span></span> <span data-ttu-id="4cf67-169">Specyfikacja musi być hostowana w raw.githubusercontent.com.</span><span class="sxs-lookup"><span data-stu-id="4cf67-169">The specification must be hosted on raw.githubusercontent.com.</span></span>
  - <span data-ttu-id="4cf67-170">`[ValidationType <ValidationType?>]`: Typ walidacji, który ma zostać uruchomiony dla pasującego żądania.</span><span class="sxs-lookup"><span data-stu-id="4cf67-170">`[ValidationType <ValidationType?>]`: The type of validation to run against a matching request.</span></span>

## <span data-ttu-id="4cf67-171">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4cf67-171">RELATED LINKS</span></span>

