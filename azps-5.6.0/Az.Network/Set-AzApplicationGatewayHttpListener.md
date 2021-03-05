---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 91e8aef2e5d12a13648132a1c8d6ece9dc4d21cf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992510"
---
# <span data-ttu-id="92bf5-101">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="92bf5-101">Set-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="92bf5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92bf5-102">SYNOPSIS</span></span>
<span data-ttu-id="92bf5-103">Modyfikuje słuchacza HTTP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="92bf5-103">Modifies an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="92bf5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="92bf5-104">SYNTAX</span></span>

### <span data-ttu-id="92bf5-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="92bf5-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-FirewallPolicyId <String>] [-SslProfileId <String>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="92bf5-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="92bf5-106">SetByResource</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-SslProfile <PSApplicationGatewaySslProfile>]
 [-HostName <String>] [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="92bf5-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="92bf5-107">DESCRIPTION</span></span>
<span data-ttu-id="92bf5-108">Polecenie cmdlet **Set-AzApplicationGatewayHttpListener modyfikuje** słuchacza HTTP dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="92bf5-108">The **Set-AzApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="92bf5-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="92bf5-109">EXAMPLES</span></span>

### <span data-ttu-id="92bf5-110">Przykład 1. Ustawianie słuchacza HTTP</span><span class="sxs-lookup"><span data-stu-id="92bf5-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="92bf5-111">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01, która należy do grupy zasobów o nazwie ResourceGroup01, i przechowuje ją w zmiennej $AppGw zasobów.</span><span class="sxs-lookup"><span data-stu-id="92bf5-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="92bf5-112">Drugie polecenie ustawia słuchacza HTTP bramy na używanie konfiguracji frontoronu przechowywanej w programie $FIP 01 z protokołem HTTP dla portu 80.</span><span class="sxs-lookup"><span data-stu-id="92bf5-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

### <span data-ttu-id="92bf5-113">Przykład 2. Dodawanie słuchacza protokołu HTTPS przy użyciu protokołu SSL i nazw hostów</span><span class="sxs-lookup"><span data-stu-id="92bf5-113">Example 2: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="92bf5-114">Pierwsze polecenie pobiera bramę aplikacji i zapisuje je w $AppGw zmienną.</span><span class="sxs-lookup"><span data-stu-id="92bf5-114">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="92bf5-115">Drugie polecenie dodaje słuchacza, który używa protokołu HTTPS, z certyfikatami SSL i nazwami hosta, do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="92bf5-115">The second command adds the listener, which uses the HTTPS protocol, with SSL Certificates and HostNames, to the application gateway.</span></span>

## <span data-ttu-id="92bf5-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92bf5-116">PARAMETERS</span></span>

### <span data-ttu-id="92bf5-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="92bf5-117">-ApplicationGateway</span></span>
<span data-ttu-id="92bf5-118">Określa bramę aplikacji, z którą to polecenie cmdlet skojarzy słuchacza HTTP.</span><span class="sxs-lookup"><span data-stu-id="92bf5-118">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="92bf5-119">- CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="92bf5-119">-CustomErrorConfiguration</span></span>
<span data-ttu-id="92bf5-120">Błąd klienta bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="92bf5-120">Customer error of an application gateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92bf5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92bf5-121">-DefaultProfile</span></span>
<span data-ttu-id="92bf5-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="92bf5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92bf5-123">- FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="92bf5-123">-FirewallPolicy</span></span>
<span data-ttu-id="92bf5-124">FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="92bf5-124">FirewallPolicy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92bf5-125">- FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="92bf5-125">-FirewallPolicyId</span></span>
<span data-ttu-id="92bf5-126">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="92bf5-126">FirewallPolicyId</span></span>

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

### <span data-ttu-id="92bf5-127">- FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="92bf5-127">-FrontendIPConfiguration</span></span>
<span data-ttu-id="92bf5-128">Określa frontowy adres IP bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="92bf5-128">Specifies the front-end IP address of the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92bf5-129">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="92bf5-129">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="92bf5-130">Określa identyfikator frontoronowego adresu IP bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="92bf5-130">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="92bf5-131">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="92bf5-131">-FrontendPort</span></span>
<span data-ttu-id="92bf5-132">Określa port frontoronu bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="92bf5-132">Specifies the application gateway front-end port.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92bf5-133">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="92bf5-133">-FrontendPortId</span></span>
<span data-ttu-id="92bf5-134">Określa identyfikator portu frontoronu bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="92bf5-134">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="92bf5-135">-HostName</span><span class="sxs-lookup"><span data-stu-id="92bf5-135">-HostName</span></span>
<span data-ttu-id="92bf5-136">Określa nazwę hosta, do których to polecenie cmdlet wysyła słuchacza http.</span><span class="sxs-lookup"><span data-stu-id="92bf5-136">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92bf5-137">-HostNames</span><span class="sxs-lookup"><span data-stu-id="92bf5-137">-HostNames</span></span>
<span data-ttu-id="92bf5-138">Nazwy hostów</span><span class="sxs-lookup"><span data-stu-id="92bf5-138">Host names</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92bf5-139">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="92bf5-139">-Name</span></span>
<span data-ttu-id="92bf5-140">Określa nazwę słuchacza HTTP.</span><span class="sxs-lookup"><span data-stu-id="92bf5-140">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="92bf5-141">— Protokół</span><span class="sxs-lookup"><span data-stu-id="92bf5-141">-Protocol</span></span>
<span data-ttu-id="92bf5-142">Określa protokół używany przez słuchacza HTTP.</span><span class="sxs-lookup"><span data-stu-id="92bf5-142">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="92bf5-143">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="92bf5-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="92bf5-144">Http</span><span class="sxs-lookup"><span data-stu-id="92bf5-144">Http</span></span>
- <span data-ttu-id="92bf5-145">https</span><span class="sxs-lookup"><span data-stu-id="92bf5-145">Https</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92bf5-146">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="92bf5-146">-RequireServerNameIndication</span></span>
<span data-ttu-id="92bf5-147">Określa, czy polecenie cmdlet wymaga wskazania nazwy serwera.</span><span class="sxs-lookup"><span data-stu-id="92bf5-147">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="92bf5-148">Dopuszczalne wartości dla tego parametru to: prawda lub fałsz.</span><span class="sxs-lookup"><span data-stu-id="92bf5-148">The acceptable values for this parameter are: true or false.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: true, false

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92bf5-149">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="92bf5-149">-SslCertificate</span></span>
<span data-ttu-id="92bf5-150">Określa certyfikat SSL odbiorcy HTTP.</span><span class="sxs-lookup"><span data-stu-id="92bf5-150">Specifies the SSL certificate of the HTTP listener.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92bf5-151">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="92bf5-151">-SslCertificateId</span></span>
<span data-ttu-id="92bf5-152">Określa identyfikator certyfikatu SSL (Secure Socket Layer) dla słuchacza protokołu HTTP.</span><span class="sxs-lookup"><span data-stu-id="92bf5-152">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="92bf5-153">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="92bf5-153">-SslProfile</span></span>
<span data-ttu-id="92bf5-154">SslProfile</span><span class="sxs-lookup"><span data-stu-id="92bf5-154">SslProfile</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92bf5-155">-SslProfileId</span><span class="sxs-lookup"><span data-stu-id="92bf5-155">-SslProfileId</span></span>
<span data-ttu-id="92bf5-156">SslProfileId</span><span class="sxs-lookup"><span data-stu-id="92bf5-156">SslProfileId</span></span>

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

### <span data-ttu-id="92bf5-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92bf5-157">CommonParameters</span></span>
<span data-ttu-id="92bf5-158">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92bf5-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92bf5-159">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="92bf5-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92bf5-160">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="92bf5-160">INPUTS</span></span>

### <span data-ttu-id="92bf5-161">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="92bf5-161">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="92bf5-162">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="92bf5-162">OUTPUTS</span></span>

### <span data-ttu-id="92bf5-163">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="92bf5-163">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="92bf5-164">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="92bf5-164">NOTES</span></span>

## <span data-ttu-id="92bf5-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="92bf5-165">RELATED LINKS</span></span>

[<span data-ttu-id="92bf5-166">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="92bf5-166">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="92bf5-167">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="92bf5-167">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="92bf5-168">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="92bf5-168">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="92bf5-169">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="92bf5-169">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)


