---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 622FE9AC-1CC4-489C-BB17-9D6B9D1C151D
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 53963e7672881255cf23df99e53a1471c3c42250
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010330"
---
# <span data-ttu-id="da379-101">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="da379-101">New-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="da379-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da379-102">SYNOPSIS</span></span>
<span data-ttu-id="da379-103">Tworzy regułę routingu żądania dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="da379-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="da379-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="da379-104">SYNTAX</span></span>

### <span data-ttu-id="da379-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="da379-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String> [-Priority <Int32>]
 [-BackendHttpSettingsId <String>] [-HttpListenerId <String>] [-BackendAddressPoolId <String>]
 [-UrlPathMapId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da379-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="da379-106">SetByResource</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String> [-Priority <Int32>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da379-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="da379-107">DESCRIPTION</span></span>
<span data-ttu-id="da379-108">**Polecenie cmdlet Add-AzApplicationGatewayRequestRoutingRule** tworzy regułę routingu żądania dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="da379-108">**The Add-AzApplicationGatewayRequestRoutingRule** cmdlet creates a request routing rule for an Azure application gateway.</span></span>

## <span data-ttu-id="da379-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="da379-109">EXAMPLES</span></span>

### <span data-ttu-id="da379-110">Przykład 1. Tworzenie reguły routingu żądania dla bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="da379-110">Example 1: Create a request routing rule for an application gateway</span></span>
```
PS C:\>$Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType Basic -Priority 100 -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="da379-111">To polecenie tworzy podstawową regułę routingu żądania o nazwie Rule01 i przechowuje wynik w zmiennej o nazwie $Rule.</span><span class="sxs-lookup"><span data-stu-id="da379-111">This command creates a basic request routing rule named Rule01 and stores the result in the variable named $Rule.</span></span>

## <span data-ttu-id="da379-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da379-112">PARAMETERS</span></span>

### <span data-ttu-id="da379-113">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="da379-113">-BackendAddressPool</span></span>
<span data-ttu-id="da379-114">Określa pulę adresów końcowych jako obiekt dla reguły routingu żądania, która ma być tworzyć.</span><span class="sxs-lookup"><span data-stu-id="da379-114">Specifies the back-end address pool, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="da379-115">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="da379-115">-BackendAddressPoolId</span></span>
<span data-ttu-id="da379-116">Określa identyfikator puli adresów końcowych reguły routingu żądania, która ma być tworzyć.</span><span class="sxs-lookup"><span data-stu-id="da379-116">Specifies the back-end address pool ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="da379-117">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="da379-117">-BackendHttpSettings</span></span>
<span data-ttu-id="da379-118">Określa ustawienia protokołu HTTP jako obiekt dla reguły routingu żądania, która ma być tworzyć.</span><span class="sxs-lookup"><span data-stu-id="da379-118">Specifies the back-end HTTP settings, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="da379-119">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="da379-119">-BackendHttpSettingsId</span></span>
<span data-ttu-id="da379-120">Określa identyfikator ustawień HTTP strony, która ma być tworzyć regułę routingu żądania.</span><span class="sxs-lookup"><span data-stu-id="da379-120">Specifies the back-end HTTP settings ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="da379-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da379-121">-DefaultProfile</span></span>
<span data-ttu-id="da379-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="da379-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da379-123">- HttpListener</span><span class="sxs-lookup"><span data-stu-id="da379-123">-HttpListener</span></span>
<span data-ttu-id="da379-124">Określa słuchacza http na końcu, który ma tworzyć regułę routingu żądania.</span><span class="sxs-lookup"><span data-stu-id="da379-124">Specifies the back-end HTTP listener for the request routing rule to create.</span></span>

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

### <span data-ttu-id="da379-125">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="da379-125">-HttpListenerId</span></span>
<span data-ttu-id="da379-126">Określa identyfikator słuchacza http zaplecza dla reguły routingu żądania do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="da379-126">Specifies the backend HTTP listener ID for the request routing rule to create.</span></span>

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

### <span data-ttu-id="da379-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="da379-127">-Name</span></span>
<span data-ttu-id="da379-128">Określa nazwę reguły routingu żądania, która jest owana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da379-128">Specifies the name of the request routing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="da379-129">— Priority (Priorytet)</span><span class="sxs-lookup"><span data-stu-id="da379-129">-Priority</span></span>
<span data-ttu-id="da379-130">Priorytet reguły</span><span class="sxs-lookup"><span data-stu-id="da379-130">The priority of the rule</span></span>

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

### <span data-ttu-id="da379-131">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="da379-131">-RedirectConfiguration</span></span>
<span data-ttu-id="da379-132">RedirectConfiguration bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="da379-132">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="da379-133">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="da379-133">-RedirectConfigurationId</span></span>
<span data-ttu-id="da379-134">Identyfikator konfiguracji przekierowywania przez bramę aplikacji</span><span class="sxs-lookup"><span data-stu-id="da379-134">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="da379-135">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="da379-135">-RewriteRuleSet</span></span>
<span data-ttu-id="da379-136">Application gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="da379-136">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="da379-137">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="da379-137">-RewriteRuleSetId</span></span>
<span data-ttu-id="da379-138">Identyfikator bramy aplikacji RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="da379-138">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="da379-139">-RuleType</span><span class="sxs-lookup"><span data-stu-id="da379-139">-RuleType</span></span>
<span data-ttu-id="da379-140">Określa typ reguły routingu żądania.</span><span class="sxs-lookup"><span data-stu-id="da379-140">Specifies type of the request routing rule.</span></span>

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

### <span data-ttu-id="da379-141">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="da379-141">-UrlPathMap</span></span>
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

### <span data-ttu-id="da379-142">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="da379-142">-UrlPathMapId</span></span>
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

### <span data-ttu-id="da379-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da379-143">CommonParameters</span></span>
<span data-ttu-id="da379-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da379-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da379-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="da379-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da379-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da379-146">INPUTS</span></span>

### <span data-ttu-id="da379-147">Brak</span><span class="sxs-lookup"><span data-stu-id="da379-147">None</span></span>

## <span data-ttu-id="da379-148">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da379-148">OUTPUTS</span></span>

### <span data-ttu-id="da379-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="da379-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="da379-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="da379-150">NOTES</span></span>

## <span data-ttu-id="da379-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="da379-151">RELATED LINKS</span></span>

[<span data-ttu-id="da379-152">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="da379-152">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="da379-153">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="da379-153">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="da379-154">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="da379-154">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="da379-155">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="da379-155">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


