---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 7808b663b53cc33309a3de5f705eca798c297acc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179947"
---
# <span data-ttu-id="73f68-101">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="73f68-101">Add-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="73f68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73f68-102">SYNOPSIS</span></span>
<span data-ttu-id="73f68-103">Dodaje tablicę mapowań ścieżek adresu URL do puli serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="73f68-103">Adds an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="73f68-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="73f68-104">SYNTAX</span></span>

### <span data-ttu-id="73f68-105">BackendSetByResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="73f68-105">BackendSetByResource (Default)</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="73f68-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="73f68-106">BackendSetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> -DefaultBackendAddressPoolId <String>
 -DefaultBackendHttpSettingsId <String> [-DefaultRewriteRuleSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73f68-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="73f68-107">RedirectSetByResource</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73f68-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="73f68-108">RedirectSetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSetId <String>]
 -DefaultRedirectConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73f68-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="73f68-109">DESCRIPTION</span></span>
<span data-ttu-id="73f68-110">Polecenie **cmdlet Add-AzApplicationGatewayUrlPathMapConfig** dodaje tablicę mapowań ścieżek adresu URL do puli serwerów back end.</span><span class="sxs-lookup"><span data-stu-id="73f68-110">The **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="73f68-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="73f68-111">EXAMPLES</span></span>

### <span data-ttu-id="73f68-112">Przykład 1. Dodawanie mapowania ścieżki adresu URL do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="73f68-112">Example 1: Add an URL path mapping to an application gateway.</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $pool = Get-AzApplicationGatewayBackendAddressPool -ApplicationGateway $appgw -Name "pool01"
PS C:\> $poolSettings = Get-AzApplicationGatewayBackendHttpSettings -ApplicationGateway $appgw -Name "poolSettings01"
PS C:\> $pathRule = New-AzApplicationGatewayPathRuleConfig -Name "rule01" -Paths "/path" -BackendAddressPool $pool -BackendHttpSettings $poolSettings
PS C:\> $appgw = Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "url01" -PathRules $pathRule -DefaultBackendAddressPool $pool -DefaultBackendHttpSettings $poolSettings
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="73f68-113">Pierwsze polecenie pobiera bramę aplikacji o nazwie appGwName i przechowuje ją w $appgw zmienną.</span><span class="sxs-lookup"><span data-stu-id="73f68-113">The first command gets an application gateway named appGwName and stores it in $appgw variable.</span></span>
<span data-ttu-id="73f68-114">Drugie polecenie pobiera pulę adresów zaplecza i przechowuje je w $pool danych.</span><span class="sxs-lookup"><span data-stu-id="73f68-114">The second command gets backend address pool and stores it in $pool variable.</span></span>
<span data-ttu-id="73f68-115">Trzecie polecenie otrzymuje ustawienia http zaplecza i zapisuje je w $poolSettings zmienną.</span><span class="sxs-lookup"><span data-stu-id="73f68-115">The third command gets backend http settings and stores it in $poolSettings variable.</span></span>
<span data-ttu-id="73f68-116">Czwarte polecenie tworzy nową konfigurację reguł ścieżki o nazwie rule01 i zapisuje ją w $pathRule zmienną.</span><span class="sxs-lookup"><span data-stu-id="73f68-116">The fourth command create new path rule configuration named rule01 and stores it in $pathRule variable.</span></span>
<span data-ttu-id="73f68-117">Piąte polecenie dodaje do bramy aplikacji konfigurację mapowania ścieżek adresów URL o nazwie url01.</span><span class="sxs-lookup"><span data-stu-id="73f68-117">The fifth command adds url path mapping configuration named url01 to the application gateway.</span></span>
<span data-ttu-id="73f68-118">Szóste polecenie aktualizuje bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="73f68-118">The sixth command updates the application gateway.</span></span>

## <span data-ttu-id="73f68-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73f68-119">PARAMETERS</span></span>

### <span data-ttu-id="73f68-120">- ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="73f68-120">-ApplicationGateway</span></span>
<span data-ttu-id="73f68-121">Określa bramę aplikacji, do której to polecenie cmdlet dodaje konfigurację mapy ścieżki adresu URL.</span><span class="sxs-lookup"><span data-stu-id="73f68-121">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

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

### <span data-ttu-id="73f68-122">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="73f68-122">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="73f68-123">Określa domyślną pulę adresów zaplecza do rozsyłania na wypadek, gdy żadne z reguł określonych w parametrze *pathRules* nie jest zgodne.</span><span class="sxs-lookup"><span data-stu-id="73f68-123">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="73f68-124">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="73f68-124">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="73f68-125">Określa domyślny identyfikator puli adresów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="73f68-125">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="73f68-126">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="73f68-126">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="73f68-127">Określa domyślne ustawienia protokołu HTTP zaplecza w przypadku, gdy żadne z reguł określonych w parametrze *pathRules* nie są zgodne.</span><span class="sxs-lookup"><span data-stu-id="73f68-127">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="73f68-128">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="73f68-128">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="73f68-129">Określa domyślny identyfikator ustawień protokołu HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="73f68-129">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="73f68-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73f68-130">-DefaultProfile</span></span>
<span data-ttu-id="73f68-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="73f68-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73f68-132">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="73f68-132">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="73f68-133">Domyślna konfiguracja RedirectConfiguration bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="73f68-133">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="73f68-134">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="73f68-134">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="73f68-135">Identyfikator domyślnej konfiguracji przekierowywania (RedirectConfiguration) bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="73f68-135">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="73f68-136">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="73f68-136">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="73f68-137">Domyślny zestaw reguł ponownego ustawienia bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="73f68-137">Application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="73f68-138">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="73f68-138">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="73f68-139">Identyfikator domyślnego zestawu reguł ponownego ustawienia reguły dla bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="73f68-139">ID of the application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="73f68-140">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="73f68-140">-Name</span></span>
<span data-ttu-id="73f68-141">Określa nazwę mapy ścieżki adresu URL, którą to polecenie cmdlet dodaje do puli serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="73f68-141">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="73f68-142">- PathRules</span><span class="sxs-lookup"><span data-stu-id="73f68-142">-PathRules</span></span>
<span data-ttu-id="73f68-143">Określa listę reguł ścieżki.</span><span class="sxs-lookup"><span data-stu-id="73f68-143">Specifies a list of path rules.</span></span>
<span data-ttu-id="73f68-144">Reguły ścieżki mają porządek i są stosowane w określonej kolejności.</span><span class="sxs-lookup"><span data-stu-id="73f68-144">The path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="73f68-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73f68-145">CommonParameters</span></span>
<span data-ttu-id="73f68-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73f68-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73f68-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73f68-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73f68-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="73f68-148">INPUTS</span></span>

### <span data-ttu-id="73f68-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="73f68-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="73f68-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="73f68-150">OUTPUTS</span></span>

### <span data-ttu-id="73f68-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="73f68-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="73f68-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="73f68-152">NOTES</span></span>

## <span data-ttu-id="73f68-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="73f68-153">RELATED LINKS</span></span>

[<span data-ttu-id="73f68-154">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="73f68-154">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="73f68-155">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="73f68-155">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="73f68-156">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="73f68-156">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="73f68-157">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="73f68-157">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


