---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BBA600C2-4813-4C12-8447-E770A949DA32
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 858af0fc06dc9df00eec100c3d07306797e99b56
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184794"
---
# <span data-ttu-id="a96d5-101">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a96d5-101">Add-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="a96d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a96d5-102">SYNOPSIS</span></span>
<span data-ttu-id="a96d5-103">Dodaje regułę routingu żądania do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a96d5-103">Adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="a96d5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a96d5-104">SYNTAX</span></span>

### <span data-ttu-id="a96d5-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a96d5-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RewriteRuleSetId <String>]
 [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a96d5-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="a96d5-106">SetByResource</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a96d5-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="a96d5-107">DESCRIPTION</span></span>
<span data-ttu-id="a96d5-108">Polecenie **cmdlet Add-AzApplicationGatewayRequestRoutingRule** dodaje regułę routingu żądania do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a96d5-108">The **Add-AzApplicationGatewayRequestRoutingRule** cmdlet adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="a96d5-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a96d5-109">EXAMPLES</span></span>

### <span data-ttu-id="a96d5-110">Przykład 1. Dodawanie reguły routingu żądania do bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="a96d5-110">Example 1: Add a request routing rule to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -Priority 100 -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="a96d5-111">Pierwsze polecenie pobiera bramę aplikacji i zapisuje ją w $AppGw zmienną.</span><span class="sxs-lookup"><span data-stu-id="a96d5-111">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a96d5-112">Drugie polecenie dodaje regułę routingu żądania do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a96d5-112">The second command adds the request routing rule to the application gateway.</span></span>

## <span data-ttu-id="a96d5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a96d5-113">PARAMETERS</span></span>

### <span data-ttu-id="a96d5-114">- ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a96d5-114">-ApplicationGateway</span></span>
<span data-ttu-id="a96d5-115">Określa bramę aplikacji, do której to polecenie cmdlet dodaje regułę routingu żądania.</span><span class="sxs-lookup"><span data-stu-id="a96d5-115">Specifies an application gateway to which this cmdlet adds a request routing rule.</span></span>

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

### <span data-ttu-id="a96d5-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a96d5-116">-BackendAddressPool</span></span>
<span data-ttu-id="a96d5-117">Określa obiekt puli adresów back-end bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a96d5-117">Specifies an application gateway back-end address pool object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a96d5-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="a96d5-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="a96d5-119">Określa identyfikator puli adresów dla bramy końcowej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a96d5-119">Specifies an application gateway back-end address pool ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a96d5-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="a96d5-120">-BackendHttpSettings</span></span>
<span data-ttu-id="a96d5-121">Określa obiekt ustawień protokołu HTTP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a96d5-121">Specifies a back-end HTTP settings object for an application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a96d5-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="a96d5-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="a96d5-123">Określa identyfikator ustawień protokołu HTTP zaplecza dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a96d5-123">Specifies a backend HTTP settings ID for an application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a96d5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a96d5-124">-DefaultProfile</span></span>
<span data-ttu-id="a96d5-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a96d5-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a96d5-126">- HttpListener</span><span class="sxs-lookup"><span data-stu-id="a96d5-126">-HttpListener</span></span>
<span data-ttu-id="a96d5-127">Określa obiekt słuchacza HTTP bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a96d5-127">Specifies application gateway HTTP listener object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a96d5-128">- HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="a96d5-128">-HttpListenerId</span></span>
<span data-ttu-id="a96d5-129">Określa identyfikator słuchacza HTTP bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a96d5-129">Specifies application gateway HTTP listener ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a96d5-130">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a96d5-130">-Name</span></span>
<span data-ttu-id="a96d5-131">Określa nazwę reguły routingu żądania, które dodaje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a96d5-131">Specifies the name of request routing rule this cmdlet adds.</span></span>

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

### <span data-ttu-id="a96d5-132">— Priority (Priorytet)</span><span class="sxs-lookup"><span data-stu-id="a96d5-132">-Priority</span></span>
<span data-ttu-id="a96d5-133">Priorytet reguły</span><span class="sxs-lookup"><span data-stu-id="a96d5-133">The priority of the rule</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:
Accepted Values: 1-20000

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a96d5-134">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="a96d5-134">-RedirectConfiguration</span></span>
<span data-ttu-id="a96d5-135">RedirectConfiguration bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="a96d5-135">Application gateway RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a96d5-136">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="a96d5-136">-RedirectConfigurationId</span></span>
<span data-ttu-id="a96d5-137">Identyfikator konfiguracji przekierowywania przez bramę aplikacji</span><span class="sxs-lookup"><span data-stu-id="a96d5-137">ID of the application gateway RedirectConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a96d5-138">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a96d5-138">-RewriteRuleSet</span></span>
<span data-ttu-id="a96d5-139">Application gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a96d5-139">Application gateway RewriteRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a96d5-140">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="a96d5-140">-RewriteRuleSetId</span></span>
<span data-ttu-id="a96d5-141">Identyfikator bramy aplikacji RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a96d5-141">ID of the application gateway RewriteRuleSet</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a96d5-142">-RuleType</span><span class="sxs-lookup"><span data-stu-id="a96d5-142">-RuleType</span></span>
<span data-ttu-id="a96d5-143">Określa typ reguły routingu żądania.</span><span class="sxs-lookup"><span data-stu-id="a96d5-143">Specifies the type of request routing rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, PathBasedRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a96d5-144">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="a96d5-144">-UrlPathMap</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a96d5-145">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="a96d5-145">-UrlPathMapId</span></span>
<span data-ttu-id="a96d5-146">Określa identyfikator mapy ścieżki adresu URL reguły routingu.</span><span class="sxs-lookup"><span data-stu-id="a96d5-146">Specifies the URL path map ID for the routing rule.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a96d5-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a96d5-147">CommonParameters</span></span>
<span data-ttu-id="a96d5-148">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a96d5-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a96d5-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a96d5-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a96d5-150">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a96d5-150">INPUTS</span></span>

### <span data-ttu-id="a96d5-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a96d5-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a96d5-152">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a96d5-152">OUTPUTS</span></span>

### <span data-ttu-id="a96d5-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a96d5-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a96d5-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a96d5-154">NOTES</span></span>

## <span data-ttu-id="a96d5-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a96d5-155">RELATED LINKS</span></span>

[<span data-ttu-id="a96d5-156">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a96d5-156">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="a96d5-157">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a96d5-157">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="a96d5-158">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a96d5-158">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="a96d5-159">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a96d5-159">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


