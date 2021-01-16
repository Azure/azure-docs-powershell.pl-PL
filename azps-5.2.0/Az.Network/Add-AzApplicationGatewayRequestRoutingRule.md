---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BBA600C2-4813-4C12-8447-E770A949DA32
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 858af0fc06dc9df00eec100c3d07306797e99b56
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362985"
---
# <span data-ttu-id="3dba7-101">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="3dba7-101">Add-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="3dba7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3dba7-102">SYNOPSIS</span></span>
<span data-ttu-id="3dba7-103">Dodaje regułę rozsyłania żądań do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3dba7-103">Adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="3dba7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3dba7-104">SYNTAX</span></span>

### <span data-ttu-id="3dba7-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3dba7-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RewriteRuleSetId <String>]
 [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3dba7-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="3dba7-106">SetByResource</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3dba7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3dba7-107">DESCRIPTION</span></span>
<span data-ttu-id="3dba7-108">Polecenie cmdlet **Add-AzApplicationGatewayRequestRoutingRule** umożliwia dodanie reguły rozsyłania żądań do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3dba7-108">The **Add-AzApplicationGatewayRequestRoutingRule** cmdlet adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="3dba7-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3dba7-109">EXAMPLES</span></span>

### <span data-ttu-id="3dba7-110">Przykład 1: Dodawanie reguły rozsyłania żądań do bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="3dba7-110">Example 1: Add a request routing rule to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -Priority 100 -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="3dba7-111">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="3dba7-111">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="3dba7-112">Drugie polecenie dodaje regułę rozsyłania żądań do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3dba7-112">The second command adds the request routing rule to the application gateway.</span></span>

## <span data-ttu-id="3dba7-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3dba7-113">PARAMETERS</span></span>

### <span data-ttu-id="3dba7-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3dba7-114">-ApplicationGateway</span></span>
<span data-ttu-id="3dba7-115">Określa bramę aplikacji, z którą to polecenie cmdlet dodaje regułę routingu żądań.</span><span class="sxs-lookup"><span data-stu-id="3dba7-115">Specifies an application gateway to which this cmdlet adds a request routing rule.</span></span>

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

### <span data-ttu-id="3dba7-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3dba7-116">-BackendAddressPool</span></span>
<span data-ttu-id="3dba7-117">Określa obiekt puli adresów zaplecza bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3dba7-117">Specifies an application gateway back-end address pool object.</span></span>

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

### <span data-ttu-id="3dba7-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="3dba7-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="3dba7-119">Określa identyfikator puli adresów zaplecza bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3dba7-119">Specifies an application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="3dba7-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="3dba7-120">-BackendHttpSettings</span></span>
<span data-ttu-id="3dba7-121">Określa obiekt ustawienia HTTP zaplecza dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3dba7-121">Specifies a back-end HTTP settings object for an application gateway.</span></span>

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

### <span data-ttu-id="3dba7-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="3dba7-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="3dba7-123">Określa identyfikator ustawień HTTP zaplecza dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3dba7-123">Specifies a backend HTTP settings ID for an application gateway.</span></span>

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

### <span data-ttu-id="3dba7-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dba7-124">-DefaultProfile</span></span>
<span data-ttu-id="3dba7-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3dba7-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3dba7-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="3dba7-126">-HttpListener</span></span>
<span data-ttu-id="3dba7-127">Określa obiekt odbiornika HTTP bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3dba7-127">Specifies application gateway HTTP listener object.</span></span>

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

### <span data-ttu-id="3dba7-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="3dba7-128">-HttpListenerId</span></span>
<span data-ttu-id="3dba7-129">Określa identyfikator odbiornika HTTP bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3dba7-129">Specifies application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="3dba7-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3dba7-130">-Name</span></span>
<span data-ttu-id="3dba7-131">Określa nazwę reguły rozsyłania żądań, którą dodaje polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3dba7-131">Specifies the name of request routing rule this cmdlet adds.</span></span>

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

### <span data-ttu-id="3dba7-132">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="3dba7-132">-Priority</span></span>
<span data-ttu-id="3dba7-133">Priorytet reguły</span><span class="sxs-lookup"><span data-stu-id="3dba7-133">The priority of the rule</span></span>

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

### <span data-ttu-id="3dba7-134">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="3dba7-134">-RedirectConfiguration</span></span>
<span data-ttu-id="3dba7-135">Aplikacja Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="3dba7-135">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="3dba7-136">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="3dba7-136">-RedirectConfigurationId</span></span>
<span data-ttu-id="3dba7-137">Identyfikator bramy Application RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="3dba7-137">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="3dba7-138">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3dba7-138">-RewriteRuleSet</span></span>
<span data-ttu-id="3dba7-139">Aplikacja Application Gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3dba7-139">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="3dba7-140">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="3dba7-140">-RewriteRuleSetId</span></span>
<span data-ttu-id="3dba7-141">Identyfikator bramy Application RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3dba7-141">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="3dba7-142">-Ruletype</span><span class="sxs-lookup"><span data-stu-id="3dba7-142">-RuleType</span></span>
<span data-ttu-id="3dba7-143">Określa typ reguły routingu żądań.</span><span class="sxs-lookup"><span data-stu-id="3dba7-143">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="3dba7-144">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="3dba7-144">-UrlPathMap</span></span>
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

### <span data-ttu-id="3dba7-145">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="3dba7-145">-UrlPathMapId</span></span>
<span data-ttu-id="3dba7-146">Określa identyfikator mapy ścieżki URL dla reguły routingu.</span><span class="sxs-lookup"><span data-stu-id="3dba7-146">Specifies the URL path map ID for the routing rule.</span></span>

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

### <span data-ttu-id="3dba7-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dba7-147">CommonParameters</span></span>
<span data-ttu-id="3dba7-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dba7-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dba7-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3dba7-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dba7-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3dba7-150">INPUTS</span></span>

### <span data-ttu-id="3dba7-151">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3dba7-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3dba7-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3dba7-152">OUTPUTS</span></span>

### <span data-ttu-id="3dba7-153">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3dba7-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3dba7-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3dba7-154">NOTES</span></span>

## <span data-ttu-id="3dba7-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3dba7-155">RELATED LINKS</span></span>

[<span data-ttu-id="3dba7-156">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="3dba7-156">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="3dba7-157">Nowe — AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="3dba7-157">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="3dba7-158">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="3dba7-158">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="3dba7-159">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="3dba7-159">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


