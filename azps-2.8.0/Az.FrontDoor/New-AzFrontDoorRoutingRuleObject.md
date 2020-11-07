---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorroutingruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
ms.openlocfilehash: 3b0c9af411bace40d963158befcb7b178b638a3b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705386"
---
# <span data-ttu-id="89230-101">New-AzFrontDoorRoutingRuleObject</span><span class="sxs-lookup"><span data-stu-id="89230-101">New-AzFrontDoorRoutingRuleObject</span></span>

## <span data-ttu-id="89230-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="89230-102">SYNOPSIS</span></span>
<span data-ttu-id="89230-103">Tworzenie PSRoutingRuleObject do tworzenia przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="89230-103">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="89230-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="89230-104">SYNTAX</span></span>

### <span data-ttu-id="89230-105">ByFieldsWithForwardingParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="89230-105">ByFieldsWithForwardingParameterSet (Default)</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> -BackendPoolName <String> [-AcceptedProtocol <PSProtocol[]>]
 [-PatternToMatch <String[]>] [-CustomForwardingPath <String>] [-ForwardingProtocol <String>]
 [-EnableCaching <Boolean>] [-QueryParameterStripDirective <String>] [-DynamicCompression <PSEnabledState>]
 [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89230-106">ByFieldsWithRedirectParameterSet</span><span class="sxs-lookup"><span data-stu-id="89230-106">ByFieldsWithRedirectParameterSet</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> [-AcceptedProtocol <PSProtocol[]>] [-PatternToMatch <String[]>]
 [-RedirectType <String>] [-RedirectProtocol <String>] [-CustomHost <String>] [-CustomPath <String>]
 [-CustomFragment <String>] [-CustomQueryString <String>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89230-107">Opis</span><span class="sxs-lookup"><span data-stu-id="89230-107">DESCRIPTION</span></span>
<span data-ttu-id="89230-108">Tworzenie PSRoutingRuleObject do tworzenia przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="89230-108">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="89230-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="89230-109">EXAMPLES</span></span>

### <span data-ttu-id="89230-110">Przykład 1. Tworzenie PSRoutingRuleObject dla tworzenia przednich drzwi za pomocą reguły przesyłania dalej</span><span class="sxs-lookup"><span data-stu-id="89230-110">Example 1: Create a PSRoutingRuleObject for Front Door creation with a forwarding rule</span></span>
```powershell
PS C:\> New-AzFrontDoorRoutingRuleObject -Name $routingRuleName -FrontDoorName $frontDoorName -ResourceGroupName $rgname -FrontendEndpointName "frontendEndpoint1" -BackendPoolName "backendPool1" 

FrontendEndpointIds          : {/subscriptions/{subid}/resourceGroups/{rgname}/pro
                               viders/Microsoft.Network/frontDoors/{frontdoorname}/FrontendEndpoints/frontendEndpoint1}
AcceptedProtocols            : {Http, Https}
PatternsToMatch              : {/*}
HealthProbeSettings          :
RouteConfiguration           : Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingConfiguration
EnabledState                 : Enabled
ResourceState                :
Id                           :
Name                         : {routingRuleName}
Type                         :
```

### <span data-ttu-id="89230-111">Przykład 2: Tworzenie PSRoutingRuleObject dla tworzenia przednich drzwi za pomocą reguły przekierowania</span><span class="sxs-lookup"><span data-stu-id="89230-111">Example 2: Create a PSRoutingRuleObject for Front Door creation with a redirect rule</span></span>
```powershell
PS C:\> $customHost = "www.contoso.com"
PS C:\> $customPath = "/images/contoso.png"
PS C:\> $queryString = "field1=value1&field2=value2"
PS C:\> $destinationFragment = "section-header-2"
PS C:\> New-AzFrontDoorRoutingRuleObject -Name $routingRuleName -FrontDoorName $frontDoorName -ResourceGroupName $rgname -FrontendEndpointName "frontendEndpoint1" -CustomHost $customHost -CustomPath $customPath -CustomQueryString $queryString -CustomFragment $destinationFragment

FrontendEndpointIds          : {/subscriptions/{subid}/resourceGroups/{rgname}/pro
                               viders/Microsoft.Network/frontDoors/{frontdoorname}/FrontendEndpoints/frontendEndpoint1}
AcceptedProtocols            : {Http, Https}
PatternsToMatch              : {/*}
HealthProbeSettings          :
RouteConfiguration           : Microsoft.Azure.Commands.FrontDoor.Models.PSRedirectConfiguration
EnabledState                 : Enabled
ResourceState                :
Id                           :
Name                         : {routingRuleName}
Type                         :

```
<span data-ttu-id="89230-112">Tworzenie PSRoutingRuleObject do tworzenia przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="89230-112">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="89230-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="89230-113">PARAMETERS</span></span>

### <span data-ttu-id="89230-114">-AcceptedProtocol</span><span class="sxs-lookup"><span data-stu-id="89230-114">-AcceptedProtocol</span></span>
<span data-ttu-id="89230-115">Schematy protokołu zgodne z tą regułą.</span><span class="sxs-lookup"><span data-stu-id="89230-115">Protocol schemes to match for this rule.</span></span>
<span data-ttu-id="89230-116">Wartość domyślna to {https, http}</span><span class="sxs-lookup"><span data-stu-id="89230-116">Default value is {Https, Http}</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSProtocol[]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89230-117">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="89230-117">-BackendPoolName</span></span>
<span data-ttu-id="89230-118">Identyfikator zasobu BackendPool, do którego jest zaszlaka ta reguła</span><span class="sxs-lookup"><span data-stu-id="89230-118">Resource id of the BackendPool which this rule routes to</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89230-119">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="89230-119">-CustomForwardingPath</span></span>
<span data-ttu-id="89230-120">Ścieżka niestandardowa używana do przepisywania ścieżek zasobów zgodnych z tą regułą.</span><span class="sxs-lookup"><span data-stu-id="89230-120">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="89230-121">Pozostaw to pole puste, aby użyć ścieżki przychodzącej.</span><span class="sxs-lookup"><span data-stu-id="89230-121">Leave empty to use incoming path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89230-122">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="89230-122">-CustomFragment</span></span>
<span data-ttu-id="89230-123">Fragment do dodania do adresu URL przekierowania.</span><span class="sxs-lookup"><span data-stu-id="89230-123">Fragment to add to the redirect URL.</span></span> <span data-ttu-id="89230-124">Fragment jest częścią adresu URL, który jest dostarczany po #.</span><span class="sxs-lookup"><span data-stu-id="89230-124">Fragment is the part of the URL that comes after #.</span></span> <span data-ttu-id="89230-125">Nie należy umieszczać #.</span><span class="sxs-lookup"><span data-stu-id="89230-125">Do not include the #.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89230-126">-CustomHost</span><span class="sxs-lookup"><span data-stu-id="89230-126">-CustomHost</span></span>
<span data-ttu-id="89230-127">Host do przekierowania.</span><span class="sxs-lookup"><span data-stu-id="89230-127">Host to redirect.</span></span> <span data-ttu-id="89230-128">Pozostaw to pole puste, aby używać hosta przychodzącego jako hosta docelowego.</span><span class="sxs-lookup"><span data-stu-id="89230-128">Leave empty to use the incoming host as the destination host.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89230-129">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="89230-129">-CustomPath</span></span>
<span data-ttu-id="89230-130">Pełna ścieżka do przekierowania.</span><span class="sxs-lookup"><span data-stu-id="89230-130">The full path to redirect.</span></span> <span data-ttu-id="89230-131">Ścieżka nie może być pusta i musi zaczynać się od</span><span class="sxs-lookup"><span data-stu-id="89230-131">Path cannot be empty and must start with /.</span></span> <span data-ttu-id="89230-132">Pozostaw to pole puste, aby użyć ścieżki przychodzącej jako ścieżki docelowej.</span><span class="sxs-lookup"><span data-stu-id="89230-132">Leave empty to use the incoming path as destination path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89230-133">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="89230-133">-CustomQueryString</span></span>
<span data-ttu-id="89230-134">Zestaw ciągów zapytań, które mają zostać umieszczone w adresie URL przekierowania.</span><span class="sxs-lookup"><span data-stu-id="89230-134">The set of query strings to be placed in the redirect URL.</span></span> <span data-ttu-id="89230-135">Ustawienie tej wartości spowodowałoby zastąpienie dowolnego istniejącego ciągu kwerendy; Zostaw puste pole, aby zachować ciąg zapytania przychodzącego.</span><span class="sxs-lookup"><span data-stu-id="89230-135">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span> <span data-ttu-id="89230-136">Ciąg kwerendy musi się znajdować w <key>=</span><span class="sxs-lookup"><span data-stu-id="89230-136">Query string must be in <key>=</span></span><value> <span data-ttu-id="89230-137">formaty.</span><span class="sxs-lookup"><span data-stu-id="89230-137">format.</span></span> <span data-ttu-id="89230-138">Pierwsze?</span><span class="sxs-lookup"><span data-stu-id="89230-138">The first ?</span></span> <span data-ttu-id="89230-139">i & zostaną dodane automatycznie, więc nie Uwzględniaj ich z przodu, ale Oddziel wiele ciągów zapytań za pomocą &.</span><span class="sxs-lookup"><span data-stu-id="89230-139">and & will be added automatically so do not include them in the front, but do separate multiple query strings with &.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89230-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89230-140">-DefaultProfile</span></span>
<span data-ttu-id="89230-141">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="89230-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89230-142">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="89230-142">-DynamicCompression</span></span>
<span data-ttu-id="89230-143">Czy włączyć kompresję dynamiczną dla zawartości buforowanej, gdy jest włączone buforowanie.</span><span class="sxs-lookup"><span data-stu-id="89230-143">Whether to enable dynamic compression for cached content when caching is enabled.</span></span>
<span data-ttu-id="89230-144">Wartość domyślna jest włączona</span><span class="sxs-lookup"><span data-stu-id="89230-144">Default value is Enabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89230-145">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="89230-145">-EnableCaching</span></span>
<span data-ttu-id="89230-146">Określa, czy włączyć buforowanie dla tej trasy.</span><span class="sxs-lookup"><span data-stu-id="89230-146">Whether to enable caching for this route.</span></span> <span data-ttu-id="89230-147">Wartość domyślna to FAŁSZ</span><span class="sxs-lookup"><span data-stu-id="89230-147">Default value is false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89230-148">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="89230-148">-EnabledState</span></span>
<span data-ttu-id="89230-149">Czy włączyć korzystanie z tej reguły.</span><span class="sxs-lookup"><span data-stu-id="89230-149">Whether to enable use of this rule.</span></span>
<span data-ttu-id="89230-150">Wartość domyślna jest włączona</span><span class="sxs-lookup"><span data-stu-id="89230-150">Default value is Enabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89230-151">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="89230-151">-ForwardingProtocol</span></span>
<span data-ttu-id="89230-152">Protokół, którego ta reguła będzie używać podczas przesyłania dalej ruchu do wartości domyślnej liczba punktów końcowych to MatchRequest.</span><span class="sxs-lookup"><span data-stu-id="89230-152">The protocol this rule will use when forwarding traffic to backends Default value is MatchRequest.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89230-153">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="89230-153">-FrontDoorName</span></span>
<span data-ttu-id="89230-154">Nazwa przednich drzwi, do których należy ta reguła routingu.</span><span class="sxs-lookup"><span data-stu-id="89230-154">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="89230-155">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="89230-155">-FrontendEndpointName</span></span>
<span data-ttu-id="89230-156">Nazwy punktów końcowych frontonu skojarzonych z tą regułą</span><span class="sxs-lookup"><span data-stu-id="89230-156">The names of Frontend endpoints associated with this rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89230-157">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="89230-157">-Name</span></span>
<span data-ttu-id="89230-158">Nazwa RoutingRule.</span><span class="sxs-lookup"><span data-stu-id="89230-158">RoutingRule name.</span></span>

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

### <span data-ttu-id="89230-159">-PatternToMatch</span><span class="sxs-lookup"><span data-stu-id="89230-159">-PatternToMatch</span></span>
<span data-ttu-id="89230-160">Wzorce trasowania reguły nie mogą zawierać żadnych \*, z wyjątkiem sytuacji, gdy jest to możliwe po zakończeniu/na końcu ścieżki.</span><span class="sxs-lookup"><span data-stu-id="89230-160">The route patterns of the rule,  Must not have any \* except possibly after the final / at the end of the path.</span></span> <span data-ttu-id="89230-161">Wartość domyślna to/\*</span><span class="sxs-lookup"><span data-stu-id="89230-161">Default value is /\*</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89230-162">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="89230-162">-QueryParameterStripDirective</span></span>
<span data-ttu-id="89230-163">Traktowanie terminów kwerendy URL podczas tworzenia klucza pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="89230-163">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="89230-164">Wartość domyślna to StripAll</span><span class="sxs-lookup"><span data-stu-id="89230-164">Default value is StripAll</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89230-165">-RedirectProtocol</span><span class="sxs-lookup"><span data-stu-id="89230-165">-RedirectProtocol</span></span>
<span data-ttu-id="89230-166">Protokół lokalizacji docelowej, do której jest przekierowywany ruch.</span><span class="sxs-lookup"><span data-stu-id="89230-166">The protocol of the destination to where the traffic is redirected.</span></span> <span data-ttu-id="89230-167">Wartość domyślna to MatchRequest</span><span class="sxs-lookup"><span data-stu-id="89230-167">Default value is MatchRequest</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89230-168">-Redirecttype</span><span class="sxs-lookup"><span data-stu-id="89230-168">-RedirectType</span></span>
<span data-ttu-id="89230-169">Typ przekierowania, którego reguła będzie używana podczas przekierowywania ruchu.</span><span class="sxs-lookup"><span data-stu-id="89230-169">The redirect type the rule will use when redirecting traffic.</span></span> <span data-ttu-id="89230-170">Wartość domyślna jest przenoszona</span><span class="sxs-lookup"><span data-stu-id="89230-170">Default Value is Moved</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89230-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89230-171">-ResourceGroupName</span></span>
<span data-ttu-id="89230-172">Nazwa grupy zasobów, w której zostanie utworzony RoutingRule.</span><span class="sxs-lookup"><span data-stu-id="89230-172">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="89230-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89230-173">CommonParameters</span></span>
<span data-ttu-id="89230-174">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89230-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89230-175">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="89230-175">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89230-176">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="89230-176">INPUTS</span></span>

### <span data-ttu-id="89230-177">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="89230-177">None</span></span>

## <span data-ttu-id="89230-178">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="89230-178">OUTPUTS</span></span>

### <span data-ttu-id="89230-179">Microsoft. Azure. Commands. FrontDoor. models. PSRoutingRule</span><span class="sxs-lookup"><span data-stu-id="89230-179">Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule</span></span>

## <span data-ttu-id="89230-180">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="89230-180">NOTES</span></span>

## <span data-ttu-id="89230-181">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="89230-181">RELATED LINKS</span></span>

<span data-ttu-id="89230-182">[Nowe — AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="89230-182">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
