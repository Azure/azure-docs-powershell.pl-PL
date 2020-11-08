---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F5EC8E7-12E9-40E5-B98D-AAFD8F9F3C37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: ec2eede30b6aef81210582b95b775200c8145943
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234094"
---
# <span data-ttu-id="8112d-101">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="8112d-101">Set-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="8112d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8112d-102">SYNOPSIS</span></span>
<span data-ttu-id="8112d-103">Ustawia konfigurację tablicy mapowań ścieżek adresów URL na pulę serwerów wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="8112d-103">Sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="8112d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8112d-104">SYNTAX</span></span>

### <span data-ttu-id="8112d-105">BackendSetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8112d-105">BackendSetByResource (Default)</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8112d-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8112d-106">BackendSetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> -DefaultBackendAddressPoolId <String>
 -DefaultBackendHttpSettingsId <String> [-DefaultRewriteRuleSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8112d-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="8112d-107">RedirectSetByResource</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8112d-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8112d-108">RedirectSetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSetId <String>]
 -DefaultRedirectConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8112d-109">Opis</span><span class="sxs-lookup"><span data-stu-id="8112d-109">DESCRIPTION</span></span>
<span data-ttu-id="8112d-110">Polecenie cmdlet **Set-AzApplicationGatewayUrlPathMapConfig** ustawia konfigurację tablicy mapowań ścieżek adresów URL na pulę serwerów wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="8112d-110">The **Set-AzApplicationGatewayUrlPathMapConfig** cmdlet sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="8112d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8112d-111">EXAMPLES</span></span>

### <span data-ttu-id="8112d-112">Przykład 1: Aktualizowanie mapowania ścieżki URL</span><span class="sxs-lookup"><span data-stu-id="8112d-112">Example 1: Update an URL path mapping</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "map01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="8112d-113">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie appGwName i zapisuje wynik w zmiennej $appgw.</span><span class="sxs-lookup"><span data-stu-id="8112d-113">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="8112d-114">Drugie polecenie aktualizuje mapowanie ścieżki adresu URL o nazwie map01 w bramie Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="8112d-114">The second command updates the URL path mapping named map01 in the application gateway.</span></span>
<span data-ttu-id="8112d-115">W trzecim poleceniu jest aktualizowana Brama Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="8112d-115">The third command updates the application gateway.</span></span>

## <span data-ttu-id="8112d-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8112d-116">PARAMETERS</span></span>

### <span data-ttu-id="8112d-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8112d-117">-ApplicationGateway</span></span>
<span data-ttu-id="8112d-118">Określa bramę aplikacji, do której to polecenie cmdlet ustawia konfigurację mapowania ścieżki URL.</span><span class="sxs-lookup"><span data-stu-id="8112d-118">Specifies the application gateway to which this cmdlet sets a URL path map configuration.</span></span>

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

### <span data-ttu-id="8112d-119">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8112d-119">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="8112d-120">Określa domyślną pulę adresów zaplecza, która ma być przekierowywana na wypadek, gdyby żadna z reguł określonych w parametrze *pathRules* nie była zgodna.</span><span class="sxs-lookup"><span data-stu-id="8112d-120">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="8112d-121">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="8112d-121">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="8112d-122">Określa domyślny identyfikator puli adresów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="8112d-122">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="8112d-123">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="8112d-123">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="8112d-124">Określa domyślne ustawienia protokołu HTTP zaplecza, których należy użyć na wypadek, gdyby żadna z reguł określonych w parametrze *pathRules* nie była zgodna.</span><span class="sxs-lookup"><span data-stu-id="8112d-124">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="8112d-125">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="8112d-125">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="8112d-126">Określa identyfikator domyślnych ustawień protokołu HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="8112d-126">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="8112d-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8112d-127">-DefaultProfile</span></span>
<span data-ttu-id="8112d-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8112d-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8112d-129">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="8112d-129">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="8112d-130">Domyślny RedirectConfiguration bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="8112d-130">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="8112d-131">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="8112d-131">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="8112d-132">Identyfikator domyślnej RedirectConfiguration bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="8112d-132">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="8112d-133">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8112d-133">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="8112d-134">Domyślny zestaw reguł ponownej edycji bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="8112d-134">Application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="8112d-135">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="8112d-135">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="8112d-136">Identyfikator zestawu reguł domyślnego zapisu bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="8112d-136">ID of the application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="8112d-137">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8112d-137">-Name</span></span>
<span data-ttu-id="8112d-138">Określa nazwę mapy ścieżki URL, w której to polecenie cmdlet ustawia konfigurację dla.</span><span class="sxs-lookup"><span data-stu-id="8112d-138">Specifies the URL path map name in which this cmdlet sets configuration for.</span></span>

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

### <span data-ttu-id="8112d-139">-PathRules</span><span class="sxs-lookup"><span data-stu-id="8112d-139">-PathRules</span></span>
<span data-ttu-id="8112d-140">Określa listę reguł ścieżek.</span><span class="sxs-lookup"><span data-stu-id="8112d-140">Specifies a list of path rules.</span></span>
<span data-ttu-id="8112d-141">Pamiętaj, że reguły ścieżki są zależne od kolejności, są one stosowane w kolejności, w jakiej zostały określone.</span><span class="sxs-lookup"><span data-stu-id="8112d-141">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="8112d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8112d-142">CommonParameters</span></span>
<span data-ttu-id="8112d-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8112d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8112d-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8112d-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8112d-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8112d-145">INPUTS</span></span>

### <span data-ttu-id="8112d-146">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8112d-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8112d-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8112d-147">OUTPUTS</span></span>

### <span data-ttu-id="8112d-148">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8112d-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8112d-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8112d-149">NOTES</span></span>

## <span data-ttu-id="8112d-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8112d-150">RELATED LINKS</span></span>

[<span data-ttu-id="8112d-151">Dodaj-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="8112d-151">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="8112d-152">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="8112d-152">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="8112d-153">Nowe — AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="8112d-153">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="8112d-154">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="8112d-154">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)


