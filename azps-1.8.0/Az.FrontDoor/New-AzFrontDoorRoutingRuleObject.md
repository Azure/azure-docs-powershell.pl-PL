---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorroutingruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
ms.openlocfilehash: 02291202966ab832bf11edbd59a1504c001c948e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868367"
---
# <span data-ttu-id="aea45-101">New-AzFrontDoorRoutingRuleObject</span><span class="sxs-lookup"><span data-stu-id="aea45-101">New-AzFrontDoorRoutingRuleObject</span></span>

## <span data-ttu-id="aea45-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aea45-102">SYNOPSIS</span></span>
<span data-ttu-id="aea45-103">Tworzenie PSRoutingRuleObject do tworzenia przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="aea45-103">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="aea45-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aea45-104">SYNTAX</span></span>

### <span data-ttu-id="aea45-105">ByFieldsWithForwardingParameterSet</span><span class="sxs-lookup"><span data-stu-id="aea45-105">ByFieldsWithForwardingParameterSet</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> -BackendPoolName <String> [-AcceptedProtocol <PSProtocol[]>]
 [-PatternToMatch <String[]>] [-CustomForwardingPath <String>] [-ForwardingProtocol <PSForwardingProtocol>]
 [-EnableCaching <Boolean>] [-QueryParameterStripDirective <PSQueryParameterStripDirective>]
 [-DynamicCompression <PSEnabledState>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aea45-106">ByFieldsWithRedirectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aea45-106">ByFieldsWithRedirectParameterSet</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> [-AcceptedProtocol <PSProtocol[]>] [-PatternToMatch <String[]>]
 [-RedirectType <PSRedirectType>] [-RedirectProtocol <PSRedirectProtocol>] [-CustomHost <String>]
 [-CustomPath <String>] [-CustomFragment <String>] [-CustomQueryString <String>]
 [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aea45-107">Opis</span><span class="sxs-lookup"><span data-stu-id="aea45-107">DESCRIPTION</span></span>
<span data-ttu-id="aea45-108">Tworzenie PSRoutingRuleObject do tworzenia przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="aea45-108">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="aea45-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aea45-109">EXAMPLES</span></span>

### <span data-ttu-id="aea45-110">Przykład 1. Tworzenie PSRoutingRuleObject na potrzeby tworzenia drzwi przednich</span><span class="sxs-lookup"><span data-stu-id="aea45-110">Example 1: Create a PSRoutingRuleObject for Front Door creation</span></span>
```powershell
PS C:\> New-AzFrontDoorRoutingRuleObject -Name $routingRuleName -FrontDoorName $frontDoorName -ResourceGroupName  -FrontendEndpointName "frontendEndpoint1" -BackendPoolName "backendPool1" 

FrontendEndpointIds          : {/subscriptions/{subid}/resourceGroups/{rgname}/pro
                               viders/Microsoft.Network/frontDoors/{frontdoorname}/FrontendEndpoints/frontendEndpoint1}
AcceptedProtocols            : {Http, Https}
PatternsToMatch              : {/*}
ForwardingProtocol           : MatchRequest
CustomForwardingPath         :
QueryParameterStripDirective : StripAll
DynamicCompression           : Enabled
HealthProbeSettings          :
BackendPoolId                : /subscriptions/{subid}/resourceGroups/{rgname}/prov
                               iders/Microsoft.Network/frontDoors/{frontdoorname}/BackendPools/backendPool1
EnableCaching                : Disabled
EnabledState                 : Enabled
ResourceState                :
Id                           :
Name                         : routingrule1
Type                         :
```

<span data-ttu-id="aea45-111">Tworzenie PSRoutingRuleObject do tworzenia przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="aea45-111">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="aea45-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aea45-112">PARAMETERS</span></span>

### <span data-ttu-id="aea45-113">-AcceptedProtocol</span><span class="sxs-lookup"><span data-stu-id="aea45-113">-AcceptedProtocol</span></span>
<span data-ttu-id="aea45-114">Schematy protokołu zgodne z tą regułą.</span><span class="sxs-lookup"><span data-stu-id="aea45-114">Protocol schemes to match for this rule.</span></span>
<span data-ttu-id="aea45-115">Wartość domyślna to {https, http}</span><span class="sxs-lookup"><span data-stu-id="aea45-115">Default value is {Https, Http}</span></span>

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

### <span data-ttu-id="aea45-116">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="aea45-116">-BackendPoolName</span></span>
<span data-ttu-id="aea45-117">Identyfikator zasobu BackendPool, do którego jest zaszlaka ta reguła</span><span class="sxs-lookup"><span data-stu-id="aea45-117">Resource id of the BackendPool which this rule routes to</span></span>

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

### <span data-ttu-id="aea45-118">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="aea45-118">-CustomForwardingPath</span></span>
<span data-ttu-id="aea45-119">Ścieżka niestandardowa używana do przepisywania ścieżek zasobów zgodnych z tą regułą.</span><span class="sxs-lookup"><span data-stu-id="aea45-119">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="aea45-120">Pozostaw to pole puste, aby użyć ścieżki przychodzącej.</span><span class="sxs-lookup"><span data-stu-id="aea45-120">Leave empty to use incoming path.</span></span>

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

### <span data-ttu-id="aea45-121">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="aea45-121">-CustomFragment</span></span>
<span data-ttu-id="aea45-122">Fragment do dodania do adresu URL przekierowania.</span><span class="sxs-lookup"><span data-stu-id="aea45-122">Fragment to add to the redirect URL.</span></span> <span data-ttu-id="aea45-123">Fragment jest częścią adresu URL, który jest dostarczany po #.</span><span class="sxs-lookup"><span data-stu-id="aea45-123">Fragment is the part of the URL that comes after #.</span></span> <span data-ttu-id="aea45-124">Nie należy umieszczać #.</span><span class="sxs-lookup"><span data-stu-id="aea45-124">Do not include the #.</span></span>

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

### <span data-ttu-id="aea45-125">-CustomHost</span><span class="sxs-lookup"><span data-stu-id="aea45-125">-CustomHost</span></span>
<span data-ttu-id="aea45-126">Host do przekierowania.</span><span class="sxs-lookup"><span data-stu-id="aea45-126">Host to redirect.</span></span> <span data-ttu-id="aea45-127">Pozostaw to pole puste, aby używać hosta przychodzącego jako hosta docelowego.</span><span class="sxs-lookup"><span data-stu-id="aea45-127">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="aea45-128">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="aea45-128">-CustomPath</span></span>
<span data-ttu-id="aea45-129">Pełna ścieżka do przekierowania.</span><span class="sxs-lookup"><span data-stu-id="aea45-129">The full path to redirect.</span></span> <span data-ttu-id="aea45-130">Ścieżka nie może być pusta i musi zaczynać się od</span><span class="sxs-lookup"><span data-stu-id="aea45-130">Path cannot be empty and must start with /.</span></span> <span data-ttu-id="aea45-131">Pozostaw to pole puste, aby użyć ścieżki przychodzącej jako ścieżki docelowej.</span><span class="sxs-lookup"><span data-stu-id="aea45-131">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="aea45-132">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="aea45-132">-CustomQueryString</span></span>
<span data-ttu-id="aea45-133">Zestaw ciągów zapytań, które mają zostać umieszczone w adresie URL przekierowania.</span><span class="sxs-lookup"><span data-stu-id="aea45-133">The set of query strings to be placed in the redirect URL.</span></span> <span data-ttu-id="aea45-134">Ustawienie tej wartości spowodowałoby zastąpienie dowolnego istniejącego ciągu kwerendy; Zostaw puste pole, aby zachować ciąg zapytania przychodzącego.</span><span class="sxs-lookup"><span data-stu-id="aea45-134">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span> <span data-ttu-id="aea45-135">Ciąg kwerendy musi się znajdować w <key>=</span><span class="sxs-lookup"><span data-stu-id="aea45-135">Query string must be in <key>=</span></span><value> <span data-ttu-id="aea45-136">formaty.</span><span class="sxs-lookup"><span data-stu-id="aea45-136">format.</span></span> <span data-ttu-id="aea45-137">Pierwsze?</span><span class="sxs-lookup"><span data-stu-id="aea45-137">The first ?</span></span> <span data-ttu-id="aea45-138">i & zostaną dodane automatycznie, więc nie Uwzględniaj ich z przodu, ale Oddziel wiele ciągów zapytań za pomocą &.</span><span class="sxs-lookup"><span data-stu-id="aea45-138">and & will be added automatically so do not include them in the front, but do separate multiple query strings with &.</span></span>

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

### <span data-ttu-id="aea45-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aea45-139">-DefaultProfile</span></span>
<span data-ttu-id="aea45-140">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="aea45-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aea45-141">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="aea45-141">-DynamicCompression</span></span>
<span data-ttu-id="aea45-142">Czy włączyć kompresję dynamiczną dla zawartości buforowanej, gdy jest włączone buforowanie.</span><span class="sxs-lookup"><span data-stu-id="aea45-142">Whether to enable dynamic compression for cached content when caching is enabled.</span></span>
<span data-ttu-id="aea45-143">Wartość domyślna jest włączona</span><span class="sxs-lookup"><span data-stu-id="aea45-143">Default value is Enabled</span></span>

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

### <span data-ttu-id="aea45-144">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="aea45-144">-EnableCaching</span></span>
<span data-ttu-id="aea45-145">Określa, czy włączyć buforowanie dla tej trasy.</span><span class="sxs-lookup"><span data-stu-id="aea45-145">Whether to enable caching for this route.</span></span> <span data-ttu-id="aea45-146">Wartość domyślna to FAŁSZ</span><span class="sxs-lookup"><span data-stu-id="aea45-146">Default value is false</span></span>

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

### <span data-ttu-id="aea45-147">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="aea45-147">-EnabledState</span></span>
<span data-ttu-id="aea45-148">Czy włączyć korzystanie z tej reguły.</span><span class="sxs-lookup"><span data-stu-id="aea45-148">Whether to enable use of this rule.</span></span>
<span data-ttu-id="aea45-149">Wartość domyślna jest włączona</span><span class="sxs-lookup"><span data-stu-id="aea45-149">Default value is Enabled</span></span>

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

### <span data-ttu-id="aea45-150">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="aea45-150">-ForwardingProtocol</span></span>
<span data-ttu-id="aea45-151">Protokół, którego ta reguła będzie używać podczas przesyłania dalej ruchu do wartości domyślnej liczba punktów końcowych to MatchRequest.</span><span class="sxs-lookup"><span data-stu-id="aea45-151">The protocol this rule will use when forwarding traffic to backends Default value is MatchRequest.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingProtocol
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:
Accepted values: HttpOnly, HttpsOnly, MatchRequest

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aea45-152">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="aea45-152">-FrontDoorName</span></span>
<span data-ttu-id="aea45-153">Nazwa przednich drzwi, do których należy ta reguła routingu.</span><span class="sxs-lookup"><span data-stu-id="aea45-153">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="aea45-154">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="aea45-154">-FrontendEndpointName</span></span>
<span data-ttu-id="aea45-155">Nazwy punktów końcowych frontonu skojarzonych z tą regułą</span><span class="sxs-lookup"><span data-stu-id="aea45-155">The names of Frontend endpoints associated with this rule</span></span>

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

### <span data-ttu-id="aea45-156">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="aea45-156">-Name</span></span>
<span data-ttu-id="aea45-157">Nazwa RoutingRule.</span><span class="sxs-lookup"><span data-stu-id="aea45-157">RoutingRule name.</span></span>

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

### <span data-ttu-id="aea45-158">-PatternToMatch</span><span class="sxs-lookup"><span data-stu-id="aea45-158">-PatternToMatch</span></span>
<span data-ttu-id="aea45-159">Wzorce trasowania reguły nie mogą zawierać żadnych \*, z wyjątkiem sytuacji, gdy jest to możliwe po zakończeniu/na końcu ścieżki.</span><span class="sxs-lookup"><span data-stu-id="aea45-159">The route patterns of the rule,  Must not have any \* except possibly after the final / at the end of the path.</span></span> <span data-ttu-id="aea45-160">Wartość domyślna to/\*</span><span class="sxs-lookup"><span data-stu-id="aea45-160">Default value is /\*</span></span>

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

### <span data-ttu-id="aea45-161">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="aea45-161">-QueryParameterStripDirective</span></span>
<span data-ttu-id="aea45-162">Traktowanie terminów kwerendy URL podczas tworzenia klucza pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="aea45-162">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="aea45-163">Wartość domyślna to StripAll</span><span class="sxs-lookup"><span data-stu-id="aea45-163">Default value is StripAll</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSQueryParameterStripDirective
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:
Accepted values: StripNone, StripAll

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aea45-164">-RedirectProtocol</span><span class="sxs-lookup"><span data-stu-id="aea45-164">-RedirectProtocol</span></span>
<span data-ttu-id="aea45-165">Protokół lokalizacji docelowej, do której jest przekierowywany ruch.</span><span class="sxs-lookup"><span data-stu-id="aea45-165">The protocol of the destination to where the traffic is redirected.</span></span> <span data-ttu-id="aea45-166">Wartość domyślna to MatchRequest</span><span class="sxs-lookup"><span data-stu-id="aea45-166">Default value is MatchRequest</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRedirectProtocol
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:
Accepted values: HttpOnly, HttpsOnly, MatchRequest

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aea45-167">-Redirecttype</span><span class="sxs-lookup"><span data-stu-id="aea45-167">-RedirectType</span></span>
<span data-ttu-id="aea45-168">Typ przekierowania, którego reguła będzie używana podczas przekierowywania ruchu.</span><span class="sxs-lookup"><span data-stu-id="aea45-168">The redirect type the rule will use when redirecting traffic.</span></span> <span data-ttu-id="aea45-169">Wartość domyślna jest przenoszona</span><span class="sxs-lookup"><span data-stu-id="aea45-169">Default Value is Moved</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRedirectType
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:
Accepted values: Moved, Found, TemporaryRedirect, PermanentRedirect

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aea45-170">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aea45-170">-ResourceGroupName</span></span>
<span data-ttu-id="aea45-171">Nazwa grupy zasobów, w której zostanie utworzony RoutingRule.</span><span class="sxs-lookup"><span data-stu-id="aea45-171">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="aea45-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aea45-172">CommonParameters</span></span>
<span data-ttu-id="aea45-173">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aea45-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aea45-174">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aea45-174">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aea45-175">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aea45-175">INPUTS</span></span>

### <span data-ttu-id="aea45-176">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="aea45-176">None</span></span>

## <span data-ttu-id="aea45-177">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aea45-177">OUTPUTS</span></span>

### <span data-ttu-id="aea45-178">Microsoft. Azure. Commands. FrontDoor. models. PSRoutingRule</span><span class="sxs-lookup"><span data-stu-id="aea45-178">Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule</span></span>

## <span data-ttu-id="aea45-179">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aea45-179">NOTES</span></span>

## <span data-ttu-id="aea45-180">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aea45-180">RELATED LINKS</span></span>

<span data-ttu-id="aea45-181">[Nowe — AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="aea45-181">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
