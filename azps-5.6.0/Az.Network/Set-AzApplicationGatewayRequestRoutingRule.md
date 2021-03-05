---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75A4826A-7A5F-4742-9DC4-DC728CED63D0
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 832fd96f34e18413bfd72e1a05826954f3ae58e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005889"
---
# <span data-ttu-id="e8aaa-101">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e8aaa-101">Set-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="e8aaa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8aaa-102">SYNOPSIS</span></span>
<span data-ttu-id="e8aaa-103">Modyfikuje regułę routingu żądania dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e8aaa-103">Modifies a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="e8aaa-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e8aaa-104">SYNTAX</span></span>

### <span data-ttu-id="e8aaa-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e8aaa-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RewriteRuleSetId <String>]
 [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8aaa-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e8aaa-106">SetByResource</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8aaa-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="e8aaa-107">DESCRIPTION</span></span>
<span data-ttu-id="e8aaa-108">Polecenie **cmdlet Set-AzApplicationGatewayRequestRoutingRule** modyfikuje regułę routingu żądania.</span><span class="sxs-lookup"><span data-stu-id="e8aaa-108">The **Set-AzApplicationGatewayRequestRoutingRule** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="e8aaa-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e8aaa-109">EXAMPLES</span></span>

### <span data-ttu-id="e8aaa-110">Przykład 1. Aktualizowanie reguły routingu żądania</span><span class="sxs-lookup"><span data-stu-id="e8aaa-110">Example 1: Update a request routing rule</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -Priority 100 -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="e8aaa-111">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01 i zapisuje ją w zmiennej $AppGw aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e8aaa-111">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e8aaa-112">Drugie polecenie modyfikuje regułę routingu żądania dla bramy aplikacji w celu używania ustawień protokołu HTTP typu back-end określonych w zmiennej $Setting, słuchacza HTTP określonego w zmiennej $Listener oraz puli adresów back-end określonej w zmiennej $Pool.</span><span class="sxs-lookup"><span data-stu-id="e8aaa-112">The second command modifies the request routing rule for the application gateway to use back-end HTTP settings specified in the $Setting variable, an HTTP listener specified in the $Listener variable, and a back-end address pool specified in the $Pool variable.</span></span>

## <span data-ttu-id="e8aaa-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e8aaa-113">PARAMETERS</span></span>

### <span data-ttu-id="e8aaa-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e8aaa-114">-ApplicationGateway</span></span>
<span data-ttu-id="e8aaa-115">Określa obiekt bramy aplikacji, z którym to polecenie cmdlet skojarzy regułę routingu żądania.</span><span class="sxs-lookup"><span data-stu-id="e8aaa-115">Specifies the application gateway object with which this cmdlet associates a request routing rule.</span></span>

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

### <span data-ttu-id="e8aaa-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e8aaa-116">-BackendAddressPool</span></span>
<span data-ttu-id="e8aaa-117">Określa pulę adresów back-end bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e8aaa-117">Specifies the application gateway back-end address pool.</span></span>

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

### <span data-ttu-id="e8aaa-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="e8aaa-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="e8aaa-119">Określa identyfikator puli adresów back-end bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e8aaa-119">Specifies the application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="e8aaa-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e8aaa-120">-BackendHttpSettings</span></span>
<span data-ttu-id="e8aaa-121">Określa ustawienia protokołu HTTP zaplecza bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e8aaa-121">Specifies the application gateway backend HTTP settings.</span></span>

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

### <span data-ttu-id="e8aaa-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="e8aaa-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="e8aaa-123">Określa identyfikator ustawień protokołu HTTP bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e8aaa-123">Specifies the application gateway back-end HTTP settings ID.</span></span>

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

### <span data-ttu-id="e8aaa-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8aaa-124">-DefaultProfile</span></span>
<span data-ttu-id="e8aaa-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e8aaa-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8aaa-126">- HttpListener</span><span class="sxs-lookup"><span data-stu-id="e8aaa-126">-HttpListener</span></span>
<span data-ttu-id="e8aaa-127">Określa słuchacza HTTP bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e8aaa-127">Specifies the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="e8aaa-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="e8aaa-128">-HttpListenerId</span></span>
<span data-ttu-id="e8aaa-129">Określa identyfikator słuchacza HTTP bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e8aaa-129">Specifies the application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="e8aaa-130">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e8aaa-130">-Name</span></span>
<span data-ttu-id="e8aaa-131">Określa nazwę reguły routingu żądania, która zostanie zmodyfikowana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8aaa-131">Specifies the name of the request routing rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="e8aaa-132">— Priority (Priorytet)</span><span class="sxs-lookup"><span data-stu-id="e8aaa-132">-Priority</span></span>
<span data-ttu-id="e8aaa-133">Priorytet reguły</span><span class="sxs-lookup"><span data-stu-id="e8aaa-133">The priority of the rule</span></span>

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

### <span data-ttu-id="e8aaa-134">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e8aaa-134">-RedirectConfiguration</span></span>
<span data-ttu-id="e8aaa-135">RedirectConfiguration bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="e8aaa-135">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="e8aaa-136">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e8aaa-136">-RedirectConfigurationId</span></span>
<span data-ttu-id="e8aaa-137">Identyfikator konfiguracji przekierowywania przez bramę aplikacji</span><span class="sxs-lookup"><span data-stu-id="e8aaa-137">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="e8aaa-138">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e8aaa-138">-RewriteRuleSet</span></span>
<span data-ttu-id="e8aaa-139">Application gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e8aaa-139">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="e8aaa-140">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="e8aaa-140">-RewriteRuleSetId</span></span>
<span data-ttu-id="e8aaa-141">Identyfikator bramy aplikacji RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e8aaa-141">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="e8aaa-142">-RuleType</span><span class="sxs-lookup"><span data-stu-id="e8aaa-142">-RuleType</span></span>
<span data-ttu-id="e8aaa-143">Określa typ reguły routingu żądania.</span><span class="sxs-lookup"><span data-stu-id="e8aaa-143">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="e8aaa-144">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="e8aaa-144">-UrlPathMap</span></span>
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

### <span data-ttu-id="e8aaa-145">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="e8aaa-145">-UrlPathMapId</span></span>
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

### <span data-ttu-id="e8aaa-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8aaa-146">CommonParameters</span></span>
<span data-ttu-id="e8aaa-147">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8aaa-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8aaa-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e8aaa-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8aaa-149">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e8aaa-149">INPUTS</span></span>

### <span data-ttu-id="e8aaa-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e8aaa-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e8aaa-151">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e8aaa-151">OUTPUTS</span></span>

### <span data-ttu-id="e8aaa-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e8aaa-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e8aaa-153">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e8aaa-153">NOTES</span></span>

## <span data-ttu-id="e8aaa-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e8aaa-154">RELATED LINKS</span></span>

[<span data-ttu-id="e8aaa-155">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e8aaa-155">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="e8aaa-156">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e8aaa-156">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="e8aaa-157">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e8aaa-157">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="e8aaa-158">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e8aaa-158">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)


