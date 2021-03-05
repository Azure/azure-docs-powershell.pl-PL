---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorrulesengineactionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineActionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineActionObject.md
ms.openlocfilehash: 4d13df2e498dd3af0c0a29660673e61233e1d4bf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970970"
---
# <span data-ttu-id="794e9-101">New-AzFrontDoorRulesEngineActionObject</span><span class="sxs-lookup"><span data-stu-id="794e9-101">New-AzFrontDoorRulesEngineActionObject</span></span>

## <span data-ttu-id="794e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="794e9-102">SYNOPSIS</span></span>
<span data-ttu-id="794e9-103">Utwórz obiekt PSRulesEngineAction w celu utworzenia reguły aparatu reguł.</span><span class="sxs-lookup"><span data-stu-id="794e9-103">Create a PSRulesEngineAction object for creating a rules engine rule.</span></span>

## <span data-ttu-id="794e9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="794e9-104">SYNTAX</span></span>

### <span data-ttu-id="794e9-105">ByFieldsWithForwardingParameterSet</span><span class="sxs-lookup"><span data-stu-id="794e9-105">ByFieldsWithForwardingParameterSet</span></span>
```
New-AzFrontDoorRulesEngineActionObject
 [-RequestHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-ResponseHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-CustomForwardingPath <String>] [-ForwardingProtocol <String>] -ResourceGroupName <String>
 -FrontDoorName <String> -BackendPoolName <String> [-EnableCaching <Boolean>]
 [-QueryParameterStripDirective <String>] [-DynamicCompression <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="794e9-106">ByFieldsWithRedirectParameterSet</span><span class="sxs-lookup"><span data-stu-id="794e9-106">ByFieldsWithRedirectParameterSet</span></span>
```
New-AzFrontDoorRulesEngineActionObject
 [-RequestHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-ResponseHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-RedirectType <String>] [-RedirectProtocol <String>] [-CustomHost <String>] [-CustomPath <String>]
 [-CustomFragment <String>] [-CustomQueryString <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="794e9-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="794e9-107">DESCRIPTION</span></span>
<span data-ttu-id="794e9-108">Utwórz obiekt PSRulesEngineAction w celu utworzenia reguły aparatu reguł.</span><span class="sxs-lookup"><span data-stu-id="794e9-108">Create a PSRulesEngineAction object for creating a rules engine rule.</span></span> 

<span data-ttu-id="794e9-109">Użyj polecenia cmdlet "New-AzFrontDoorHeaderActionObject", aby utworzyć zapytania PSHeaderObjects w celu przekazania do parametrów "-RequestHeaderActions" i "-ResponseHeaderActions".</span><span class="sxs-lookup"><span data-stu-id="794e9-109">Use cmdlet "New-AzFrontDoorHeaderActionObject" to create PSHeaderObjects to pass into the parameters "-RequestHeaderActions" and "-ResponseHeaderActions"."</span></span>

## <span data-ttu-id="794e9-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="794e9-110">EXAMPLES</span></span>

### <span data-ttu-id="794e9-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="794e9-111">Example 1</span></span>
```powershell
PS C:\> $rulesEngineAction = New-AzFrontDoorRulesEngineActionObject -RequestHeaderAction $headerActions -ForwardingProtocol HttpsOnly -BackendPoolName mybackendpool -ResourceGroupName Jessicl-Test-RG -FrontDoorName jessicl-test-myappfrontend -QueryParameterStripDirective StripNone -DynamicCompression Disabled -EnableCaching $true
PS C:\> $rulesEngineAction

RequestHeaderAction            ResponseHeaderAction RouteConfigurationOverride
-------------------            -------------------- --------------------------
{headeraction1, headeraction2} {}                   Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingConfigurati�

PS C:\> $rulesEngineAction.RequestHeaderAction

HeaderName    HeaderActionType Value
----------    ---------------- -----
headeraction1        Overwrite
headeraction2           Append

PS C:\> $rulesEngineAction.ResponseHeaderAction
PS C:\> $rulesEngineAction.RouteConfigurationOverride

CustomForwardingPath         :
ForwardingProtocol           : HttpsOnly
BackendPoolId                : /subscriptions/47f4bc68-6fe4-43a2-be8b-dfd0e290efa2/resourceGroups/myresourcegroup/provi
                               ders/Microsoft.Network/frontDoors/myfrontdoor/BackendPools/mybackendpool
QueryParameterStripDirective : StripNone
DynamicCompression           : Disabled
EnableCaching                : True
```

<span data-ttu-id="794e9-112">Utwórz akcję aparatu reguł i pokaż, jak wyświetlić właściwości utworzonej akcji aparatu reguł.</span><span class="sxs-lookup"><span data-stu-id="794e9-112">Create a rules engine action and show how to view the properties of the rules engine action created.</span></span>

## <span data-ttu-id="794e9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="794e9-113">PARAMETERS</span></span>

### <span data-ttu-id="794e9-114">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="794e9-114">-BackendPoolName</span></span>
<span data-ttu-id="794e9-115">Nazwa buforu backendpool, do którego ta reguła jest przekierowy łana</span><span class="sxs-lookup"><span data-stu-id="794e9-115">The name of the BackendPool which this rule routes to</span></span>

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

### <span data-ttu-id="794e9-116">- CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="794e9-116">-CustomForwardingPath</span></span>
<span data-ttu-id="794e9-117">Ścieżka niestandardowa używana do ponownego wytyczania ścieżek zasobów, które są zgodne z tą regułą.</span><span class="sxs-lookup"><span data-stu-id="794e9-117">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="794e9-118">Pozostaw puste, aby użyć ścieżki przychodzącej.</span><span class="sxs-lookup"><span data-stu-id="794e9-118">Leave empty to use incoming path.</span></span>

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

### <span data-ttu-id="794e9-119">- CustomFragment</span><span class="sxs-lookup"><span data-stu-id="794e9-119">-CustomFragment</span></span>
<span data-ttu-id="794e9-120">Fragment, który należy dodać do adresu URL przekierowania.</span><span class="sxs-lookup"><span data-stu-id="794e9-120">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="794e9-121">Fragment to część adresu URL, która pojawia się po #.</span><span class="sxs-lookup"><span data-stu-id="794e9-121">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="794e9-122">Nie dołączaj błędu #.</span><span class="sxs-lookup"><span data-stu-id="794e9-122">Do not include the #.</span></span>

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

### <span data-ttu-id="794e9-123">- CustomHost</span><span class="sxs-lookup"><span data-stu-id="794e9-123">-CustomHost</span></span>
<span data-ttu-id="794e9-124">Host, aby przekierować.</span><span class="sxs-lookup"><span data-stu-id="794e9-124">Host to redirect.</span></span>
<span data-ttu-id="794e9-125">Pozostaw puste, aby użyć hosta poczty przychodzącej jako hosta docelowego.</span><span class="sxs-lookup"><span data-stu-id="794e9-125">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="794e9-126">— CustomPath</span><span class="sxs-lookup"><span data-stu-id="794e9-126">-CustomPath</span></span>
<span data-ttu-id="794e9-127">Pełna ścieżka przekierowania.</span><span class="sxs-lookup"><span data-stu-id="794e9-127">The full path to redirect.</span></span>
<span data-ttu-id="794e9-128">Ścieżka nie może być pusta i musi zaczynać się od /.</span><span class="sxs-lookup"><span data-stu-id="794e9-128">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="794e9-129">Pozostaw puste, aby użyć ścieżki przychodzącej jako ścieżki docelowej.</span><span class="sxs-lookup"><span data-stu-id="794e9-129">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="794e9-130">- CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="794e9-130">-CustomQueryString</span></span>
<span data-ttu-id="794e9-131">Zestaw ciągów zapytań, które mają zostać umieszczone w adresie URL przekierowania.</span><span class="sxs-lookup"><span data-stu-id="794e9-131">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="794e9-132">Ustawienie tej wartości zastąpi wszelkie istniejące ciągi zapytania. pozostaw puste, aby zachować ciąg zapytania przychodzącego.</span><span class="sxs-lookup"><span data-stu-id="794e9-132">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="794e9-133">Ciąg zapytania musi mieć \<key\> = \<value\> format.</span><span class="sxs-lookup"><span data-stu-id="794e9-133">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="794e9-134">Pierwsze ?</span><span class="sxs-lookup"><span data-stu-id="794e9-134">The first ?</span></span>
<span data-ttu-id="794e9-135">i & zostaną dodane automatycznie, więc nie dołączaj ich z przodu, ale oddzielaj wiele ciągów zapytań za pomocą &.</span><span class="sxs-lookup"><span data-stu-id="794e9-135">and & will be added automatically so do not include them in the front, but do separate multiple query strings with &.</span></span>

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

### <span data-ttu-id="794e9-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="794e9-136">-DefaultProfile</span></span>
<span data-ttu-id="794e9-137">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="794e9-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="794e9-138">- DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="794e9-138">-DynamicCompression</span></span>
<span data-ttu-id="794e9-139">Czy włączyć kompresję dynamiczną dla zawartości buforowanej.</span><span class="sxs-lookup"><span data-stu-id="794e9-139">Whether to enable dynamic compression for cached content.</span></span>
<span data-ttu-id="794e9-140">Wartość domyślna jest włączona</span><span class="sxs-lookup"><span data-stu-id="794e9-140">Default value is Enabled</span></span>

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

### <span data-ttu-id="794e9-141">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="794e9-141">-EnableCaching</span></span>
<span data-ttu-id="794e9-142">Czy należy włączyć buforowanie dla tej trasy.</span><span class="sxs-lookup"><span data-stu-id="794e9-142">Whether to enable caching for this route.</span></span>
<span data-ttu-id="794e9-143">Wartość domyślna ma wartość fałszywą</span><span class="sxs-lookup"><span data-stu-id="794e9-143">Default value is false</span></span>

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

### <span data-ttu-id="794e9-144">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="794e9-144">-ForwardingProtocol</span></span>
<span data-ttu-id="794e9-145">Protokół, który ta reguła będzie stosować podczas przesyłania ruchu dalej do zaplecza.</span><span class="sxs-lookup"><span data-stu-id="794e9-145">The protocol this rule will use when forwarding traffic to backends.</span></span>
<span data-ttu-id="794e9-146">Wartość domyślna to MatchRequest</span><span class="sxs-lookup"><span data-stu-id="794e9-146">Default value is MatchRequest</span></span>

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

### <span data-ttu-id="794e9-147">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="794e9-147">-FrontDoorName</span></span>
<span data-ttu-id="794e9-148">Nazwa drzwi frontowych, do których należy ta reguła przekierowania.</span><span class="sxs-lookup"><span data-stu-id="794e9-148">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="794e9-149">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="794e9-149">-QueryParameterStripDirective</span></span>
<span data-ttu-id="794e9-150">Sposób stosowania terminów zapytania adresu URL podczas formowania klucza pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="794e9-150">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="794e9-151">Wartość domyślna to StripAll</span><span class="sxs-lookup"><span data-stu-id="794e9-151">Default value is StripAll</span></span>

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

### <span data-ttu-id="794e9-152">-RedirectProtocol</span><span class="sxs-lookup"><span data-stu-id="794e9-152">-RedirectProtocol</span></span>
<span data-ttu-id="794e9-153">Protokół miejsca docelowego, do którego jest przekierowywany ruch.</span><span class="sxs-lookup"><span data-stu-id="794e9-153">The protocol of the destination to where the traffic is redirected.</span></span>
<span data-ttu-id="794e9-154">Wartość domyślna to MatchRequest</span><span class="sxs-lookup"><span data-stu-id="794e9-154">Default value is MatchRequest</span></span>

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

### <span data-ttu-id="794e9-155">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="794e9-155">-RedirectType</span></span>
<span data-ttu-id="794e9-156">Podczas przekierowywania ruchu wpisz regułę przekierowywania.</span><span class="sxs-lookup"><span data-stu-id="794e9-156">The redirect type the rule will use when redirecting traffic.</span></span>
<span data-ttu-id="794e9-157">Wartość domyślna jest przenoszony</span><span class="sxs-lookup"><span data-stu-id="794e9-157">Default Value is Moved</span></span>

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

### <span data-ttu-id="794e9-158">-RequestHeaderAction</span><span class="sxs-lookup"><span data-stu-id="794e9-158">-RequestHeaderAction</span></span>
<span data-ttu-id="794e9-159">Lista akcji nagłówków, które mają być stosowane w żądaniu od afd do pochodzenia.</span><span class="sxs-lookup"><span data-stu-id="794e9-159">A list of header actions to apply from the request from AFD to the origin.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="794e9-160">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="794e9-160">-ResourceGroupName</span></span>
<span data-ttu-id="794e9-161">Nazwa grupy zasobów, w których zostanie utworzony routingRule.</span><span class="sxs-lookup"><span data-stu-id="794e9-161">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="794e9-162">-ResponseHeaderAction</span><span class="sxs-lookup"><span data-stu-id="794e9-162">-ResponseHeaderAction</span></span>
<span data-ttu-id="794e9-163">Lista akcji nagłówka do zastosowania w odpowiedzi z programu AFD do klienta.</span><span class="sxs-lookup"><span data-stu-id="794e9-163">A list of header actions to apply from the response from AFD to the client.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="794e9-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="794e9-164">CommonParameters</span></span>
<span data-ttu-id="794e9-165">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="794e9-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="794e9-166">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="794e9-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="794e9-167">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="794e9-167">INPUTS</span></span>

### <span data-ttu-id="794e9-168">Brak</span><span class="sxs-lookup"><span data-stu-id="794e9-168">None</span></span>

## <span data-ttu-id="794e9-169">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="794e9-169">OUTPUTS</span></span>

### <span data-ttu-id="794e9-170">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineAction</span><span class="sxs-lookup"><span data-stu-id="794e9-170">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineAction</span></span>

## <span data-ttu-id="794e9-171">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="794e9-171">NOTES</span></span>

## <span data-ttu-id="794e9-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="794e9-172">RELATED LINKS</span></span>
