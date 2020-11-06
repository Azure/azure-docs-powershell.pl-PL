---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorroutingruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorRoutingRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorRoutingRuleObject.md
ms.openlocfilehash: c03a76943857e3615269a9584a3975ae6ab86666
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548652"
---
# <span data-ttu-id="9211d-101">New-AzureRmFrontDoorRoutingRuleObject</span><span class="sxs-lookup"><span data-stu-id="9211d-101">New-AzureRmFrontDoorRoutingRuleObject</span></span>

## <span data-ttu-id="9211d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9211d-102">SYNOPSIS</span></span>
<span data-ttu-id="9211d-103">Tworzenie PSRoutingRuleObject do tworzenia przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="9211d-103">Create a PSRoutingRuleObject for Front Door creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9211d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9211d-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> -BackendPoolName <String> [-AcceptedProtocol <PSProtocol[]>]
 [-PatternToMatch <String[]>] [-CustomForwardingPath <String>] [-ForwardingProtocol <PSForwardingProtocol>]
 [-EnableCaching <Boolean>] [-QueryParameterStripDirective <PSQueryParameterStripDirective>]
 [-DynamicCompression <PSEnabledState>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9211d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9211d-105">DESCRIPTION</span></span>
<span data-ttu-id="9211d-106">Tworzenie PSRoutingRuleObject do tworzenia przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="9211d-106">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="9211d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9211d-107">EXAMPLES</span></span>

### <span data-ttu-id="9211d-108">Przykład 1. Tworzenie PSRoutingRuleObject na potrzeby tworzenia drzwi przednich</span><span class="sxs-lookup"><span data-stu-id="9211d-108">Example 1: Create a PSRoutingRuleObject for Front Door creation</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorRoutingRuleObject -Name $routingRuleName -FrontDoorName $frontDoorName -ResourceGroupName  -FrontendEndpointName "frontendEndpoint1" -BackendPoolName "backendPool1" 

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

<span data-ttu-id="9211d-109">Tworzenie PSRoutingRuleObject do tworzenia przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="9211d-109">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="9211d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9211d-110">PARAMETERS</span></span>

### <span data-ttu-id="9211d-111">-AcceptedProtocol</span><span class="sxs-lookup"><span data-stu-id="9211d-111">-AcceptedProtocol</span></span>
<span data-ttu-id="9211d-112">Schematy protokołu zgodne z tą regułą.</span><span class="sxs-lookup"><span data-stu-id="9211d-112">Protocol schemes to match for this rule.</span></span>
<span data-ttu-id="9211d-113">Wartość domyślna to {https, http}</span><span class="sxs-lookup"><span data-stu-id="9211d-113">Default value is {Https, Http}</span></span>

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

### <span data-ttu-id="9211d-114">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="9211d-114">-BackendPoolName</span></span>
<span data-ttu-id="9211d-115">Identyfikator zasobu BackendPool, do którego jest zaszlaka ta reguła</span><span class="sxs-lookup"><span data-stu-id="9211d-115">Resource id of the BackendPool which this rule routes to</span></span>

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

### <span data-ttu-id="9211d-116">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="9211d-116">-CustomForwardingPath</span></span>
<span data-ttu-id="9211d-117">Ścieżka niestandardowa używana do przepisywania ścieżek zasobów zgodnych z tą regułą.</span><span class="sxs-lookup"><span data-stu-id="9211d-117">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="9211d-118">Pozostaw to pole puste, aby użyć ścieżki przychodzącej.</span><span class="sxs-lookup"><span data-stu-id="9211d-118">Leave empty to use incoming path.</span></span>

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

### <span data-ttu-id="9211d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9211d-119">-DefaultProfile</span></span>
<span data-ttu-id="9211d-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9211d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9211d-121">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="9211d-121">-DynamicCompression</span></span>
<span data-ttu-id="9211d-122">Czy włączyć kompresję dynamiczną dla zawartości buforowanej, gdy jest włączone buforowanie.</span><span class="sxs-lookup"><span data-stu-id="9211d-122">Whether to enable dynamic compression for cached content when caching is enabled.</span></span>
<span data-ttu-id="9211d-123">Wartość domyślna jest włączona</span><span class="sxs-lookup"><span data-stu-id="9211d-123">Default value is Enabled</span></span>

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

### <span data-ttu-id="9211d-124">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="9211d-124">-EnableCaching</span></span>
<span data-ttu-id="9211d-125">Określa, czy włączyć buforowanie dla tej trasy.</span><span class="sxs-lookup"><span data-stu-id="9211d-125">Whether to enable caching for this route.</span></span> <span data-ttu-id="9211d-126">Wartość domyślna to FAŁSZ</span><span class="sxs-lookup"><span data-stu-id="9211d-126">Default value is false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9211d-127">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="9211d-127">-EnabledState</span></span>
<span data-ttu-id="9211d-128">Czy włączyć korzystanie z tej reguły.</span><span class="sxs-lookup"><span data-stu-id="9211d-128">Whether to enable use of this rule.</span></span>
<span data-ttu-id="9211d-129">Wartość domyślna jest włączona</span><span class="sxs-lookup"><span data-stu-id="9211d-129">Default value is Enabled</span></span>

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

### <span data-ttu-id="9211d-130">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="9211d-130">-ForwardingProtocol</span></span>
<span data-ttu-id="9211d-131">Protokół, którego ta reguła będzie używać podczas przesyłania dalej ruchu do wartości domyślnej liczba punktów końcowych to MatchRequest.</span><span class="sxs-lookup"><span data-stu-id="9211d-131">The protocol this rule will use when forwarding traffic to backends Default value is MatchRequest.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingProtocol
Parameter Sets: (All)
Aliases:
Accepted values: HttpOnly, HttpsOnly, MatchRequest

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9211d-132">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="9211d-132">-FrontDoorName</span></span>
<span data-ttu-id="9211d-133">Nazwa przednich drzwi, do których należy ta reguła routingu.</span><span class="sxs-lookup"><span data-stu-id="9211d-133">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="9211d-134">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="9211d-134">-FrontendEndpointName</span></span>
<span data-ttu-id="9211d-135">Nazwy punktów końcowych frontonu skojarzonych z tą regułą</span><span class="sxs-lookup"><span data-stu-id="9211d-135">The names of Frontend endpoints associated with this rule</span></span>

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

### <span data-ttu-id="9211d-136">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9211d-136">-Name</span></span>
<span data-ttu-id="9211d-137">Nazwa RoutingRule.</span><span class="sxs-lookup"><span data-stu-id="9211d-137">RoutingRule name.</span></span>

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

### <span data-ttu-id="9211d-138">-PatternToMatch</span><span class="sxs-lookup"><span data-stu-id="9211d-138">-PatternToMatch</span></span>
<span data-ttu-id="9211d-139">Wzorce trasowania reguły nie mogą zawierać żadnych \*, z wyjątkiem sytuacji, gdy jest to możliwe po zakończeniu/na końcu ścieżki.</span><span class="sxs-lookup"><span data-stu-id="9211d-139">The route patterns of the rule,  Must not have any \* except possibly after the final / at the end of the path.</span></span> <span data-ttu-id="9211d-140">Wartość domyślna to/\*</span><span class="sxs-lookup"><span data-stu-id="9211d-140">Default value is /\*</span></span>

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

### <span data-ttu-id="9211d-141">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="9211d-141">-QueryParameterStripDirective</span></span>
<span data-ttu-id="9211d-142">Traktowanie terminów kwerendy URL podczas tworzenia klucza pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="9211d-142">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="9211d-143">Wartość domyślna to StripAll</span><span class="sxs-lookup"><span data-stu-id="9211d-143">Default value is StripAll</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSQueryParameterStripDirective
Parameter Sets: (All)
Aliases:
Accepted values: StripNone, StripAll

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9211d-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9211d-144">-ResourceGroupName</span></span>
<span data-ttu-id="9211d-145">Nazwa grupy zasobów, w której zostanie utworzony RoutingRule.</span><span class="sxs-lookup"><span data-stu-id="9211d-145">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="9211d-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9211d-146">CommonParameters</span></span>
<span data-ttu-id="9211d-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9211d-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9211d-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9211d-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9211d-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9211d-149">INPUTS</span></span>

### <span data-ttu-id="9211d-150">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9211d-150">None</span></span>

## <span data-ttu-id="9211d-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9211d-151">OUTPUTS</span></span>

### <span data-ttu-id="9211d-152">Microsoft. Azure. Commands. FrontDoor. models. PSRoutingRule</span><span class="sxs-lookup"><span data-stu-id="9211d-152">Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule</span></span>

## <span data-ttu-id="9211d-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9211d-153">NOTES</span></span>

## <span data-ttu-id="9211d-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9211d-154">RELATED LINKS</span></span>

<span data-ttu-id="9211d-155">[Nowe — AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="9211d-155">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span></span>
