---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 970ae86a9664dad32e7c91c35abb17cd086a0130
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870331"
---
# <span data-ttu-id="e2e1c-101">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e2e1c-101">Add-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="e2e1c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e2e1c-102">SYNOPSIS</span></span>
<span data-ttu-id="e2e1c-103">Dodaje tablicę mapowań ścieżek adresów URL do puli serwerów wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="e2e1c-103">Adds an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="e2e1c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e2e1c-104">SYNTAX</span></span>

### <span data-ttu-id="e2e1c-105">BackendSetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e2e1c-105">BackendSetByResource (Default)</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e2e1c-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e2e1c-106">BackendSetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> -DefaultBackendAddressPoolId <String>
 -DefaultBackendHttpSettingsId <String> [-DefaultRewriteRuleSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2e1c-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="e2e1c-107">RedirectSetByResource</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2e1c-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e2e1c-108">RedirectSetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSetId <String>]
 -DefaultRedirectConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2e1c-109">Opis</span><span class="sxs-lookup"><span data-stu-id="e2e1c-109">DESCRIPTION</span></span>
<span data-ttu-id="e2e1c-110">Polecenie cmdlet **Add-AzApplicationGatewayUrlPathMapConfig** umożliwia dodanie tablicy mapowań ścieżek adresów URL do puli serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="e2e1c-110">The **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="e2e1c-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e2e1c-111">EXAMPLES</span></span>

### <span data-ttu-id="e2e1c-112">Przykład 1: Dodawanie mapowania ścieżki URL do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e2e1c-112">Example 1: Add an URL path mapping to an application gateway.</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $pool = Get-AzApplicationGatewayBackendAddressPool -ApplicationGateway $appgw -Name "pool01"
PS C:\> $poolSettings = Get-AzApplicationGatewayBackendHttpSettings -ApplicationGateway $appgw -Name "poolSettings01"
PS C:\> $pathRule = New-AzApplicationGatewayPathRuleConfig -Name "rule01" -Paths "/path" -BackendAddressPool $pool -BackendHttpSettings $poolSettings
PS C:\> $appgw = Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "url01" -PathRules $pathRule -DefaultBackendAddressPool $pool -DefaultBackendHttpSettings $poolSettings
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="e2e1c-113">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie appGwName i zapisuje ją w zmiennej $appgw.</span><span class="sxs-lookup"><span data-stu-id="e2e1c-113">The first command gets an application gateway named appGwName and stores it in $appgw variable.</span></span>
<span data-ttu-id="e2e1c-114">Drugie polecenie pobiera pulę adresów zaplecza i zapisuje ją w $pool zmiennej.</span><span class="sxs-lookup"><span data-stu-id="e2e1c-114">The second command gets backend address pool and stores it in $pool variable.</span></span>
<span data-ttu-id="e2e1c-115">Trzecie polecenie pobiera ustawienia http zaplecza i przechowuje je w zmiennej $poolSettings.</span><span class="sxs-lookup"><span data-stu-id="e2e1c-115">The third command gets backend http settings and stores it in $poolSettings variable.</span></span>
<span data-ttu-id="e2e1c-116">Czwarte polecenie tworzy nową konfigurację reguły ścieżki o nazwie rule01 i zapisuje ją w zmiennej $pathRule.</span><span class="sxs-lookup"><span data-stu-id="e2e1c-116">The fourth command create new path rule configuration named rule01 and stores it in $pathRule variable.</span></span>
<span data-ttu-id="e2e1c-117">Piąte polecenie dodaje konfigurację mapowania ścieżki adresu URL o nazwie url01 do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e2e1c-117">The fifth command adds url path mapping configuration named url01 to the application gateway.</span></span>
<span data-ttu-id="e2e1c-118">Szóste polecenie aktualizuje bramę Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="e2e1c-118">The sixth command updates the application gateway.</span></span>

## <span data-ttu-id="e2e1c-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e2e1c-119">PARAMETERS</span></span>

### <span data-ttu-id="e2e1c-120">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e2e1c-120">-ApplicationGateway</span></span>
<span data-ttu-id="e2e1c-121">Określa bramę aplikacji, z którą to polecenie cmdlet dodaje konfigurację mapowania ścieżki adresu URL.</span><span class="sxs-lookup"><span data-stu-id="e2e1c-121">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

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

### <span data-ttu-id="e2e1c-122">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e2e1c-122">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="e2e1c-123">Określa domyślną pulę adresów zaplecza, która ma być przekierowywana na wypadek, gdyby żadna z reguł określonych w parametrze *pathRules* nie była zgodna.</span><span class="sxs-lookup"><span data-stu-id="e2e1c-123">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="e2e1c-124">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="e2e1c-124">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="e2e1c-125">Określa domyślny identyfikator puli adresów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="e2e1c-125">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="e2e1c-126">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e2e1c-126">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="e2e1c-127">Określa domyślne ustawienia protokołu HTTP zaplecza, których należy użyć na wypadek, gdyby żadna z reguł określonych w parametrze *pathRules* nie była zgodna.</span><span class="sxs-lookup"><span data-stu-id="e2e1c-127">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="e2e1c-128">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="e2e1c-128">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="e2e1c-129">Określa identyfikator domyślnych ustawień protokołu HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="e2e1c-129">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="e2e1c-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2e1c-130">-DefaultProfile</span></span>
<span data-ttu-id="e2e1c-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e2e1c-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2e1c-132">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2e1c-132">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="e2e1c-133">Domyślny RedirectConfiguration bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="e2e1c-133">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="e2e1c-134">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e2e1c-134">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="e2e1c-135">Identyfikator domyślnej RedirectConfiguration bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="e2e1c-135">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="e2e1c-136">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e2e1c-136">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="e2e1c-137">Domyślny zestaw reguł ponownej edycji bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="e2e1c-137">Application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="e2e1c-138">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="e2e1c-138">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="e2e1c-139">Identyfikator zestawu reguł domyślnego zapisu bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="e2e1c-139">ID of the application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="e2e1c-140">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e2e1c-140">-Name</span></span>
<span data-ttu-id="e2e1c-141">Określa nazwę mapy ścieżki URL, którą to polecenie cmdlet dodaje do puli serwerów wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="e2e1c-141">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="e2e1c-142">-PathRules</span><span class="sxs-lookup"><span data-stu-id="e2e1c-142">-PathRules</span></span>
<span data-ttu-id="e2e1c-143">Określa listę reguł ścieżek.</span><span class="sxs-lookup"><span data-stu-id="e2e1c-143">Specifies a list of path rules.</span></span>
<span data-ttu-id="e2e1c-144">Reguły ścieżki są zależne od kolejności, są one stosowane w kolejności, w jakiej są określone.</span><span class="sxs-lookup"><span data-stu-id="e2e1c-144">The path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="e2e1c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2e1c-145">CommonParameters</span></span>
<span data-ttu-id="e2e1c-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2e1c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2e1c-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2e1c-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2e1c-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e2e1c-148">INPUTS</span></span>

### <span data-ttu-id="e2e1c-149">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e2e1c-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e2e1c-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e2e1c-150">OUTPUTS</span></span>

### <span data-ttu-id="e2e1c-151">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e2e1c-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e2e1c-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e2e1c-152">NOTES</span></span>

## <span data-ttu-id="e2e1c-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e2e1c-153">RELATED LINKS</span></span>

[<span data-ttu-id="e2e1c-154">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e2e1c-154">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="e2e1c-155">Nowe — AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e2e1c-155">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="e2e1c-156">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e2e1c-156">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="e2e1c-157">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e2e1c-157">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


