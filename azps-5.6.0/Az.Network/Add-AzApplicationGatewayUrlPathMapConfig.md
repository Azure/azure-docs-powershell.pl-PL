---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 2bc6a8eed22660d966256afbc9783e4edfc04947
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986777"
---
# <span data-ttu-id="238e9-101">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="238e9-101">Add-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="238e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="238e9-102">SYNOPSIS</span></span>
<span data-ttu-id="238e9-103">Dodaje tablicę mapowań ścieżek adresu URL do puli serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="238e9-103">Adds an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="238e9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="238e9-104">SYNTAX</span></span>

### <span data-ttu-id="238e9-105">BackendSetByResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="238e9-105">BackendSetByResource (Default)</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="238e9-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="238e9-106">BackendSetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> -DefaultBackendAddressPoolId <String>
 -DefaultBackendHttpSettingsId <String> [-DefaultRewriteRuleSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="238e9-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="238e9-107">RedirectSetByResource</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="238e9-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="238e9-108">RedirectSetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSetId <String>]
 -DefaultRedirectConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="238e9-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="238e9-109">DESCRIPTION</span></span>
<span data-ttu-id="238e9-110">Polecenie **cmdlet Add-AzApplicationGatewayUrlPathMapConfig** dodaje tablicę mapowań ścieżek adresu URL do puli serwerów back end.</span><span class="sxs-lookup"><span data-stu-id="238e9-110">The **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="238e9-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="238e9-111">EXAMPLES</span></span>

### <span data-ttu-id="238e9-112">Przykład 1. Dodawanie mapowania ścieżek adresu URL do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="238e9-112">Example 1: Add an URL path mapping to an application gateway.</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $pool = Get-AzApplicationGatewayBackendAddressPool -ApplicationGateway $appgw -Name "pool01"
PS C:\> $poolSettings = Get-AzApplicationGatewayBackendHttpSettings -ApplicationGateway $appgw -Name "poolSettings01"
PS C:\> $pathRule = New-AzApplicationGatewayPathRuleConfig -Name "rule01" -Paths "/path" -BackendAddressPool $pool -BackendHttpSettings $poolSettings
PS C:\> $appgw = Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "url01" -PathRules $pathRule -DefaultBackendAddressPool $pool -DefaultBackendHttpSettings $poolSettings
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="238e9-113">Pierwsze polecenie pobiera bramę aplikacji o nazwie appGwName i przechowuje ją w $appgw zmienną.</span><span class="sxs-lookup"><span data-stu-id="238e9-113">The first command gets an application gateway named appGwName and stores it in $appgw variable.</span></span>
<span data-ttu-id="238e9-114">Drugie polecenie pobiera pulę adresów zaplecza i przechowuje je w $pool danych.</span><span class="sxs-lookup"><span data-stu-id="238e9-114">The second command gets backend address pool and stores it in $pool variable.</span></span>
<span data-ttu-id="238e9-115">Trzecie polecenie otrzymuje ustawienia http zaplecza i zapisuje je w $poolSettings zmienną.</span><span class="sxs-lookup"><span data-stu-id="238e9-115">The third command gets backend http settings and stores it in $poolSettings variable.</span></span>
<span data-ttu-id="238e9-116">Czwarte polecenie tworzy nową konfigurację reguł ścieżki o nazwie rule01 i zapisuje ją w $pathRule zmienną.</span><span class="sxs-lookup"><span data-stu-id="238e9-116">The fourth command create new path rule configuration named rule01 and stores it in $pathRule variable.</span></span>
<span data-ttu-id="238e9-117">Piąte polecenie dodaje do bramy aplikacji konfigurację mapowania ścieżek adresów URL o nazwie url01.</span><span class="sxs-lookup"><span data-stu-id="238e9-117">The fifth command adds url path mapping configuration named url01 to the application gateway.</span></span>
<span data-ttu-id="238e9-118">Szóste polecenie aktualizuje bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="238e9-118">The sixth command updates the application gateway.</span></span>

## <span data-ttu-id="238e9-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="238e9-119">PARAMETERS</span></span>

### <span data-ttu-id="238e9-120">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="238e9-120">-ApplicationGateway</span></span>
<span data-ttu-id="238e9-121">Określa bramę aplikacji, do której to polecenie cmdlet dodaje konfigurację mapy ścieżki adresu URL.</span><span class="sxs-lookup"><span data-stu-id="238e9-121">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="238e9-122">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="238e9-122">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="238e9-123">Określa domyślną pulę adresów zaplecza do rozsyłania na wypadek, gdy żadne z reguł określonych w parametrze *pathRules* nie jest zgodne.</span><span class="sxs-lookup"><span data-stu-id="238e9-123">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: BackendSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="238e9-124">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="238e9-124">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="238e9-125">Określa domyślny identyfikator puli adresów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="238e9-125">Specifies the default backend address pool ID.</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="238e9-126">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="238e9-126">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="238e9-127">Określa domyślne ustawienia protokołu HTTP zaplecza w przypadku, gdy żadne z reguł określonych w parametrze *pathRules* nie są zgodne.</span><span class="sxs-lookup"><span data-stu-id="238e9-127">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: BackendSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="238e9-128">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="238e9-128">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="238e9-129">Określa domyślny identyfikator ustawień protokołu HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="238e9-129">Specifies the default backend HTTP settings ID.</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="238e9-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="238e9-130">-DefaultProfile</span></span>
<span data-ttu-id="238e9-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="238e9-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="238e9-132">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="238e9-132">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="238e9-133">Domyślna konfiguracja RedirectConfiguration bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="238e9-133">Application gateway default RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: RedirectSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="238e9-134">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="238e9-134">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="238e9-135">Identyfikator domyślnej konfiguracji przekierowywania (RedirectConfiguration) bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="238e9-135">ID of the application gateway default RedirectConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: RedirectSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="238e9-136">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="238e9-136">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="238e9-137">Domyślny zestaw reguł ponownego ustawienia bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="238e9-137">Application gateway default rewrite rule set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: BackendSetByResource, RedirectSetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="238e9-138">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="238e9-138">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="238e9-139">Identyfikator domyślnego zestawu reguł ponownego edytowego bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="238e9-139">ID of the application gateway default rewrite rule set</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId, RedirectSetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="238e9-140">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="238e9-140">-Name</span></span>
<span data-ttu-id="238e9-141">Określa nazwę mapy ścieżki adresu URL, którą to polecenie cmdlet dodaje do puli serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="238e9-141">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="238e9-142">- PathRules</span><span class="sxs-lookup"><span data-stu-id="238e9-142">-PathRules</span></span>
<span data-ttu-id="238e9-143">Określa listę reguł ścieżki.</span><span class="sxs-lookup"><span data-stu-id="238e9-143">Specifies a list of path rules.</span></span>
<span data-ttu-id="238e9-144">Reguły ścieżki są poufne dla kolejności i są stosowane w określonej kolejności.</span><span class="sxs-lookup"><span data-stu-id="238e9-144">The path rules are order sensitive, they are applied in order they are specified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="238e9-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="238e9-145">CommonParameters</span></span>
<span data-ttu-id="238e9-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="238e9-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="238e9-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="238e9-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="238e9-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="238e9-148">INPUTS</span></span>

### <span data-ttu-id="238e9-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="238e9-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="238e9-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="238e9-150">OUTPUTS</span></span>

### <span data-ttu-id="238e9-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="238e9-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="238e9-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="238e9-152">NOTES</span></span>

## <span data-ttu-id="238e9-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="238e9-153">RELATED LINKS</span></span>

[<span data-ttu-id="238e9-154">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="238e9-154">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="238e9-155">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="238e9-155">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="238e9-156">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="238e9-156">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="238e9-157">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="238e9-157">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


