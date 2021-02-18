---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F5EC8E7-12E9-40E5-B98D-AAFD8F9F3C37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: ec2eede30b6aef81210582b95b775200c8145943
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240595"
---
# <span data-ttu-id="908be-101">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="908be-101">Set-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="908be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="908be-102">SYNOPSIS</span></span>
<span data-ttu-id="908be-103">Ustawia konfigurację tablicy mapowań ścieżek adresu URL na pulę serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="908be-103">Sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="908be-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="908be-104">SYNTAX</span></span>

### <span data-ttu-id="908be-105">BackendSetByResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="908be-105">BackendSetByResource (Default)</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="908be-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="908be-106">BackendSetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> -DefaultBackendAddressPoolId <String>
 -DefaultBackendHttpSettingsId <String> [-DefaultRewriteRuleSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="908be-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="908be-107">RedirectSetByResource</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="908be-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="908be-108">RedirectSetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSetId <String>]
 -DefaultRedirectConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="908be-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="908be-109">DESCRIPTION</span></span>
<span data-ttu-id="908be-110">Polecenie **cmdlet Set-AzApplicationGatewayUrlPathMapConfig** ustawia konfigurację tablicy mapowań ścieżek adresu URL na pulę serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="908be-110">The **Set-AzApplicationGatewayUrlPathMapConfig** cmdlet sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="908be-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="908be-111">EXAMPLES</span></span>

### <span data-ttu-id="908be-112">Przykład 1. Aktualizowanie mapowania ścieżki adresu URL</span><span class="sxs-lookup"><span data-stu-id="908be-112">Example 1: Update an URL path mapping</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "map01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="908be-113">Pierwsze polecenie pobiera nazwę bramy aplikacji appGwName i zapisuje wynik w $appgw zmienną.</span><span class="sxs-lookup"><span data-stu-id="908be-113">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="908be-114">Drugie polecenie aktualizuje mapowanie ścieżki adresu URL o nazwie map01 w bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="908be-114">The second command updates the URL path mapping named map01 in the application gateway.</span></span>
<span data-ttu-id="908be-115">Trzecie polecenie aktualizuje bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="908be-115">The third command updates the application gateway.</span></span>

## <span data-ttu-id="908be-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="908be-116">PARAMETERS</span></span>

### <span data-ttu-id="908be-117">- ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="908be-117">-ApplicationGateway</span></span>
<span data-ttu-id="908be-118">Określa bramę aplikacji, dla której to polecenie cmdlet ustawia konfigurację mapy ścieżki adresu URL.</span><span class="sxs-lookup"><span data-stu-id="908be-118">Specifies the application gateway to which this cmdlet sets a URL path map configuration.</span></span>

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

### <span data-ttu-id="908be-119">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="908be-119">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="908be-120">Określa domyślną pulę adresów zaplecza do rozsyłania na wypadek, gdy żadne z reguł określonych w parametrze *pathRules* nie jest zgodne.</span><span class="sxs-lookup"><span data-stu-id="908be-120">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="908be-121">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="908be-121">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="908be-122">Określa domyślny identyfikator puli adresów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="908be-122">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="908be-123">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="908be-123">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="908be-124">Określa domyślne ustawienia protokołu HTTP zaplecza w przypadku, gdy żadne z reguł określonych w parametrze *pathRules* nie są zgodne.</span><span class="sxs-lookup"><span data-stu-id="908be-124">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="908be-125">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="908be-125">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="908be-126">Określa domyślny identyfikator ustawień protokołu HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="908be-126">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="908be-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="908be-127">-DefaultProfile</span></span>
<span data-ttu-id="908be-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="908be-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="908be-129">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="908be-129">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="908be-130">Domyślna konfiguracja RedirectConfiguration bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="908be-130">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="908be-131">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="908be-131">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="908be-132">Identyfikator domyślnej konfiguracji przekierowywania (RedirectConfiguration) bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="908be-132">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="908be-133">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="908be-133">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="908be-134">Domyślny zestaw reguł ponownego ustawienia bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="908be-134">Application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="908be-135">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="908be-135">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="908be-136">Identyfikator domyślnego zestawu reguł ponownego ustawienia reguły dla bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="908be-136">ID of the application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="908be-137">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="908be-137">-Name</span></span>
<span data-ttu-id="908be-138">Określa nazwę mapy ścieżki adresu URL, dla której to polecenie cmdlet ustawia konfigurację.</span><span class="sxs-lookup"><span data-stu-id="908be-138">Specifies the URL path map name in which this cmdlet sets configuration for.</span></span>

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

### <span data-ttu-id="908be-139">- PathRules</span><span class="sxs-lookup"><span data-stu-id="908be-139">-PathRules</span></span>
<span data-ttu-id="908be-140">Określa listę reguł ścieżki.</span><span class="sxs-lookup"><span data-stu-id="908be-140">Specifies a list of path rules.</span></span>
<span data-ttu-id="908be-141">Zwróć uwagę, że reguły ścieżki mają porządek i są stosowane w określonej kolejności.</span><span class="sxs-lookup"><span data-stu-id="908be-141">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="908be-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="908be-142">CommonParameters</span></span>
<span data-ttu-id="908be-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="908be-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="908be-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="908be-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="908be-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="908be-145">INPUTS</span></span>

### <span data-ttu-id="908be-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="908be-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="908be-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="908be-147">OUTPUTS</span></span>

### <span data-ttu-id="908be-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="908be-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="908be-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="908be-149">NOTES</span></span>

## <span data-ttu-id="908be-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="908be-150">RELATED LINKS</span></span>

[<span data-ttu-id="908be-151">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="908be-151">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="908be-152">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="908be-152">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="908be-153">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="908be-153">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="908be-154">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="908be-154">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)


