---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75A4826A-7A5F-4742-9DC4-DC728CED63D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: f815994a6f60490bd930a17748cd00167c2b52ed
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378632"
---
# <span data-ttu-id="f7b7f-101">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f7b7f-101">Set-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="f7b7f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f7b7f-102">SYNOPSIS</span></span>
<span data-ttu-id="f7b7f-103">Modyfikuje regułę rozsyłania żądań dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f7b7f-103">Modifies a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="f7b7f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f7b7f-104">SYNTAX</span></span>

### <span data-ttu-id="f7b7f-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f7b7f-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RewriteRuleSetId <String>]
 [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7b7f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f7b7f-106">SetByResource</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7b7f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f7b7f-107">DESCRIPTION</span></span>
<span data-ttu-id="f7b7f-108">Polecenie cmdlet **Set-AzApplicationGatewayRequestRoutingRule** modyfikuje regułę rozsyłania żądań.</span><span class="sxs-lookup"><span data-stu-id="f7b7f-108">The **Set-AzApplicationGatewayRequestRoutingRule** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="f7b7f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f7b7f-109">EXAMPLES</span></span>

### <span data-ttu-id="f7b7f-110">Przykład 1: aktualizowanie reguły routingu żądań</span><span class="sxs-lookup"><span data-stu-id="f7b7f-110">Example 1: Update a request routing rule</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -Priority 100 -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="f7b7f-111">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="f7b7f-111">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="f7b7f-112">Drugie polecenie modyfikuje regułę rozsyłania żądań dla bramy aplikacji w celu użycia wewnętrznych ustawień HTTP określonych w zmiennej $Setting, odbiornika HTTP określonego w zmiennej $Listener i puli adresów zaplecza określonej w zmiennej $Pool.</span><span class="sxs-lookup"><span data-stu-id="f7b7f-112">The second command modifies the request routing rule for the application gateway to use back-end HTTP settings specified in the $Setting variable, an HTTP listener specified in the $Listener variable, and a back-end address pool specified in the $Pool variable.</span></span>

## <span data-ttu-id="f7b7f-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f7b7f-113">PARAMETERS</span></span>

### <span data-ttu-id="f7b7f-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f7b7f-114">-ApplicationGateway</span></span>
<span data-ttu-id="f7b7f-115">Określa obiekt bramy aplikacji, z którym to polecenie cmdlet kojarzy regułę routingu żądań.</span><span class="sxs-lookup"><span data-stu-id="f7b7f-115">Specifies the application gateway object with which this cmdlet associates a request routing rule.</span></span>

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

### <span data-ttu-id="f7b7f-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f7b7f-116">-BackendAddressPool</span></span>
<span data-ttu-id="f7b7f-117">Określa pulę adresów zaplecza bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f7b7f-117">Specifies the application gateway back-end address pool.</span></span>

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

### <span data-ttu-id="f7b7f-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="f7b7f-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="f7b7f-119">Określa identyfikator puli adresów zaplecza bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f7b7f-119">Specifies the application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="f7b7f-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f7b7f-120">-BackendHttpSettings</span></span>
<span data-ttu-id="f7b7f-121">Określa ustawienia HTTP zaplecza bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f7b7f-121">Specifies the application gateway backend HTTP settings.</span></span>

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

### <span data-ttu-id="f7b7f-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="f7b7f-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="f7b7f-123">Określa identyfikator ustawień HTTP bramy Application end.</span><span class="sxs-lookup"><span data-stu-id="f7b7f-123">Specifies the application gateway back-end HTTP settings ID.</span></span>

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

### <span data-ttu-id="f7b7f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7b7f-124">-DefaultProfile</span></span>
<span data-ttu-id="f7b7f-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f7b7f-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7b7f-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="f7b7f-126">-HttpListener</span></span>
<span data-ttu-id="f7b7f-127">Określa odbiornik HTTP bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f7b7f-127">Specifies the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="f7b7f-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="f7b7f-128">-HttpListenerId</span></span>
<span data-ttu-id="f7b7f-129">Określa identyfikator odbiornika HTTP bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f7b7f-129">Specifies the application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="f7b7f-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f7b7f-130">-Name</span></span>
<span data-ttu-id="f7b7f-131">Określa nazwę reguły rozsyłania żądań, którą to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="f7b7f-131">Specifies the name of the request routing rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="f7b7f-132">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="f7b7f-132">-Priority</span></span>
<span data-ttu-id="f7b7f-133">Priorytet reguły</span><span class="sxs-lookup"><span data-stu-id="f7b7f-133">The priority of the rule</span></span>

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

### <span data-ttu-id="f7b7f-134">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f7b7f-134">-RedirectConfiguration</span></span>
<span data-ttu-id="f7b7f-135">Aplikacja Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f7b7f-135">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="f7b7f-136">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f7b7f-136">-RedirectConfigurationId</span></span>
<span data-ttu-id="f7b7f-137">Identyfikator bramy Application RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f7b7f-137">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="f7b7f-138">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f7b7f-138">-RewriteRuleSet</span></span>
<span data-ttu-id="f7b7f-139">Aplikacja Application Gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f7b7f-139">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="f7b7f-140">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="f7b7f-140">-RewriteRuleSetId</span></span>
<span data-ttu-id="f7b7f-141">Identyfikator bramy Application RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f7b7f-141">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="f7b7f-142">-Ruletype</span><span class="sxs-lookup"><span data-stu-id="f7b7f-142">-RuleType</span></span>
<span data-ttu-id="f7b7f-143">Określa typ reguły routingu żądań.</span><span class="sxs-lookup"><span data-stu-id="f7b7f-143">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="f7b7f-144">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="f7b7f-144">-UrlPathMap</span></span>
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

### <span data-ttu-id="f7b7f-145">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="f7b7f-145">-UrlPathMapId</span></span>
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

### <span data-ttu-id="f7b7f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7b7f-146">CommonParameters</span></span>
<span data-ttu-id="f7b7f-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7b7f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7b7f-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7b7f-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7b7f-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f7b7f-149">INPUTS</span></span>

### <span data-ttu-id="f7b7f-150">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f7b7f-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f7b7f-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f7b7f-151">OUTPUTS</span></span>

### <span data-ttu-id="f7b7f-152">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f7b7f-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f7b7f-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f7b7f-153">NOTES</span></span>

## <span data-ttu-id="f7b7f-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f7b7f-154">RELATED LINKS</span></span>

[<span data-ttu-id="f7b7f-155">Dodaj-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f7b7f-155">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="f7b7f-156">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f7b7f-156">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="f7b7f-157">Nowe — AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f7b7f-157">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="f7b7f-158">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f7b7f-158">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)


