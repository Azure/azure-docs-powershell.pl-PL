---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 622FE9AC-1CC4-489C-BB17-9D6B9D1C151D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 95f3e4b11d9253a232fc119faf39a4fa51fab60a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358239"
---
# <span data-ttu-id="e2142-101">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e2142-101">New-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="e2142-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e2142-102">SYNOPSIS</span></span>
<span data-ttu-id="e2142-103">Tworzy regułę rozsyłania żądań dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e2142-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="e2142-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e2142-104">SYNTAX</span></span>

### <span data-ttu-id="e2142-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e2142-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String> [-Priority <Int32>]
 [-BackendHttpSettingsId <String>] [-HttpListenerId <String>] [-BackendAddressPoolId <String>]
 [-UrlPathMapId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2142-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e2142-106">SetByResource</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String> [-Priority <Int32>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2142-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e2142-107">DESCRIPTION</span></span>
<span data-ttu-id="e2142-108">Polecenie cmdlet **Add-AzApplicationGatewayRequestRoutingRule** tworzy regułę rozsyłania żądań dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e2142-108">**The Add-AzApplicationGatewayRequestRoutingRule** cmdlet creates a request routing rule for an Azure application gateway.</span></span>

## <span data-ttu-id="e2142-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e2142-109">EXAMPLES</span></span>

### <span data-ttu-id="e2142-110">Przykład 1. Tworzenie reguły rozsyłania żądań dla bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="e2142-110">Example 1: Create a request routing rule for an application gateway</span></span>
```
PS C:\>$Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType Basic -Priority 100 -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="e2142-111">To polecenie tworzy podstawową zasadę rozsyłania żądań o nazwie Rule01 i zapisuje wynik w zmiennej o nazwie $Rule.</span><span class="sxs-lookup"><span data-stu-id="e2142-111">This command creates a basic request routing rule named Rule01 and stores the result in the variable named $Rule.</span></span>

## <span data-ttu-id="e2142-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e2142-112">PARAMETERS</span></span>

### <span data-ttu-id="e2142-113">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e2142-113">-BackendAddressPool</span></span>
<span data-ttu-id="e2142-114">Określa pulę adresów zaplecza jako obiekt dla reguły rozsyłania żądań, którą można utworzyć.</span><span class="sxs-lookup"><span data-stu-id="e2142-114">Specifies the back-end address pool, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="e2142-115">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="e2142-115">-BackendAddressPoolId</span></span>
<span data-ttu-id="e2142-116">Określa identyfikator puli adresów zaplecza reguły rozsyłania żądań, którą należy utworzyć.</span><span class="sxs-lookup"><span data-stu-id="e2142-116">Specifies the back-end address pool ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="e2142-117">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e2142-117">-BackendHttpSettings</span></span>
<span data-ttu-id="e2142-118">Określa ustawienia HTTP zaplecza jako obiekt do utworzenia reguły rozsyłania żądań.</span><span class="sxs-lookup"><span data-stu-id="e2142-118">Specifies the back-end HTTP settings, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="e2142-119">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="e2142-119">-BackendHttpSettingsId</span></span>
<span data-ttu-id="e2142-120">Określa identyfikator HTTP zaplecza dla reguły rozsyłania żądań, którą należy utworzyć.</span><span class="sxs-lookup"><span data-stu-id="e2142-120">Specifies the back-end HTTP settings ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="e2142-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2142-121">-DefaultProfile</span></span>
<span data-ttu-id="e2142-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e2142-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2142-123">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="e2142-123">-HttpListener</span></span>
<span data-ttu-id="e2142-124">Umożliwia określenie odbiornika HTTP zaplecza do utworzenia reguły routingu żądań.</span><span class="sxs-lookup"><span data-stu-id="e2142-124">Specifies the back-end HTTP listener for the request routing rule to create.</span></span>

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

### <span data-ttu-id="e2142-125">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="e2142-125">-HttpListenerId</span></span>
<span data-ttu-id="e2142-126">Określa identyfikator odbiornika HTTP zaplecza dla reguły rozsyłania żądań, którą należy utworzyć.</span><span class="sxs-lookup"><span data-stu-id="e2142-126">Specifies the backend HTTP listener ID for the request routing rule to create.</span></span>

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

### <span data-ttu-id="e2142-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e2142-127">-Name</span></span>
<span data-ttu-id="e2142-128">Określa nazwę reguły rozsyłania żądań, którą tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2142-128">Specifies the name of the request routing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="e2142-129">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="e2142-129">-Priority</span></span>
<span data-ttu-id="e2142-130">Priorytet reguły</span><span class="sxs-lookup"><span data-stu-id="e2142-130">The priority of the rule</span></span>

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

### <span data-ttu-id="e2142-131">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2142-131">-RedirectConfiguration</span></span>
<span data-ttu-id="e2142-132">Aplikacja Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2142-132">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="e2142-133">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e2142-133">-RedirectConfigurationId</span></span>
<span data-ttu-id="e2142-134">Identyfikator bramy Application RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2142-134">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="e2142-135">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e2142-135">-RewriteRuleSet</span></span>
<span data-ttu-id="e2142-136">Aplikacja Application Gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e2142-136">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="e2142-137">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="e2142-137">-RewriteRuleSetId</span></span>
<span data-ttu-id="e2142-138">Identyfikator bramy Application RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e2142-138">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="e2142-139">-Ruletype</span><span class="sxs-lookup"><span data-stu-id="e2142-139">-RuleType</span></span>
<span data-ttu-id="e2142-140">Określa typ reguły rozsyłania żądań.</span><span class="sxs-lookup"><span data-stu-id="e2142-140">Specifies type of the request routing rule.</span></span>

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

### <span data-ttu-id="e2142-141">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="e2142-141">-UrlPathMap</span></span>
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

### <span data-ttu-id="e2142-142">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="e2142-142">-UrlPathMapId</span></span>
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

### <span data-ttu-id="e2142-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2142-143">CommonParameters</span></span>
<span data-ttu-id="e2142-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2142-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2142-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2142-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2142-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e2142-146">INPUTS</span></span>

### <span data-ttu-id="e2142-147">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e2142-147">None</span></span>

## <span data-ttu-id="e2142-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e2142-148">OUTPUTS</span></span>

### <span data-ttu-id="e2142-149">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e2142-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="e2142-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e2142-150">NOTES</span></span>

## <span data-ttu-id="e2142-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e2142-151">RELATED LINKS</span></span>

[<span data-ttu-id="e2142-152">Dodaj-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e2142-152">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="e2142-153">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e2142-153">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="e2142-154">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e2142-154">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="e2142-155">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e2142-155">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


