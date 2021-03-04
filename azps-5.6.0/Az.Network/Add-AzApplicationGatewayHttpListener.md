---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1E192553-61D8-4449-936B-68CF866C710C
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 51d85ffa9c1181b45f7ea4aa45484a814759a953
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982634"
---
# <span data-ttu-id="30a0c-101">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="30a0c-101">Add-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="30a0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30a0c-102">SYNOPSIS</span></span>
<span data-ttu-id="30a0c-103">Dodaje słuchacza HTTP do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="30a0c-103">Adds an HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="30a0c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="30a0c-104">SYNTAX</span></span>

### <span data-ttu-id="30a0c-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="30a0c-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-FirewallPolicyId <String>] [-SslProfileId <String>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="30a0c-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="30a0c-106">SetByResource</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-SslProfile <PSApplicationGatewaySslProfile>]
 [-HostName <String>] [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="30a0c-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="30a0c-107">DESCRIPTION</span></span>
<span data-ttu-id="30a0c-108">Polecenie **cmdlet Add-AzApplicationGatewayHttpListener** dodaje słuchacza HTTP do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="30a0c-108">The **Add-AzApplicationGatewayHttpListener** cmdlet adds a HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="30a0c-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="30a0c-109">EXAMPLES</span></span>

### <span data-ttu-id="30a0c-110">Przykład 1. Dodawanie słuchacza HTTP</span><span class="sxs-lookup"><span data-stu-id="30a0c-110">Example 1: Add a HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

<span data-ttu-id="30a0c-111">Pierwsze polecenie pobiera bramę aplikacji i zapisuje je w $AppGw zmienną. Drugie polecenie dodaje słuchacza HTTP do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="30a0c-111">The first command gets the application gateway and stores it in the $AppGw variable.The second command adds the HTTP listener to the application gateway.</span></span>

### <span data-ttu-id="30a0c-112">Przykład 2. Dodawanie słuchacza HTTPS przy użyciu protokołu SSL</span><span class="sxs-lookup"><span data-stu-id="30a0c-112">Example 2: Add a HTTPS listener with SSL</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="30a0c-113">Pierwsze polecenie pobiera bramę aplikacji i zapisuje je w $AppGw zmienną.</span><span class="sxs-lookup"><span data-stu-id="30a0c-113">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="30a0c-114">Drugie polecenie dodaje słuchacza, który korzysta z protokołu HTTPS, do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="30a0c-114">The second command adds the listener, which uses the HTTPS protocol, to the application gateway.</span></span>

### <span data-ttu-id="30a0c-115">Przykład 3. Dodawanie słuchacza protokołu HTTPS przy użyciu protokołu SSL i nazw hostów</span><span class="sxs-lookup"><span data-stu-id="30a0c-115">Example 3: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com","www.microsoft.com"
```

<span data-ttu-id="30a0c-116">Pierwsze polecenie pobiera bramę aplikacji i zapisuje je w $AppGw zmienną.</span><span class="sxs-lookup"><span data-stu-id="30a0c-116">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="30a0c-117">Drugie polecenie dodaje słuchacza, który używa protokołu HTTPS, z certyfikatami SSL i nazwami hosta, do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="30a0c-117">The second command adds the listener, which uses the HTTPS protocol, with SSL Certificates and HostNames, to the application gateway.</span></span>

## <span data-ttu-id="30a0c-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30a0c-118">PARAMETERS</span></span>

### <span data-ttu-id="30a0c-119">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="30a0c-119">-ApplicationGateway</span></span>
<span data-ttu-id="30a0c-120">Określa bramę aplikacji, do której to polecenie cmdlet dodaje słuchacza HTTP.</span><span class="sxs-lookup"><span data-stu-id="30a0c-120">Specifies the application gateway to which this cmdlet adds an HTTP listener.</span></span>

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

### <span data-ttu-id="30a0c-121">- CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="30a0c-121">-CustomErrorConfiguration</span></span>
<span data-ttu-id="30a0c-122">Błąd klienta bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="30a0c-122">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="30a0c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30a0c-123">-DefaultProfile</span></span>
<span data-ttu-id="30a0c-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="30a0c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30a0c-125">- FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="30a0c-125">-FirewallPolicy</span></span>
<span data-ttu-id="30a0c-126">FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="30a0c-126">FirewallPolicy</span></span>

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

### <span data-ttu-id="30a0c-127">- FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="30a0c-127">-FirewallPolicyId</span></span>
<span data-ttu-id="30a0c-128">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="30a0c-128">FirewallPolicyId</span></span>

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

### <span data-ttu-id="30a0c-129">- FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="30a0c-129">-FrontendIPConfiguration</span></span>
<span data-ttu-id="30a0c-130">Określa obiekt zasobu frontoronu IP bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="30a0c-130">Specifies the application gateway front-end IP resource object.</span></span>

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

### <span data-ttu-id="30a0c-131">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="30a0c-131">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="30a0c-132">Określa fronto-endowy identyfikator IP bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="30a0c-132">Specifies the application gateway front-end IP ID.</span></span>

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

### <span data-ttu-id="30a0c-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="30a0c-133">-FrontendPort</span></span>
<span data-ttu-id="30a0c-134">Określa obiekt portu frontoronu bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="30a0c-134">Specifies the application gateway front-end port object.</span></span>

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

### <span data-ttu-id="30a0c-135">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="30a0c-135">-FrontendPortId</span></span>
<span data-ttu-id="30a0c-136">Określa identyfikator portu frontoronu bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="30a0c-136">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="30a0c-137">-HostName</span><span class="sxs-lookup"><span data-stu-id="30a0c-137">-HostName</span></span>
<span data-ttu-id="30a0c-138">Określa nazwę hosta, do których to polecenie cmdlet dodaje słuchacza HTTP.</span><span class="sxs-lookup"><span data-stu-id="30a0c-138">Specifies the host name that this cmdlet adds a HTTP listener to.</span></span>

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

### <span data-ttu-id="30a0c-139">-HostNames</span><span class="sxs-lookup"><span data-stu-id="30a0c-139">-HostNames</span></span>
<span data-ttu-id="30a0c-140">Nazwy hostów</span><span class="sxs-lookup"><span data-stu-id="30a0c-140">Host names</span></span>

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

### <span data-ttu-id="30a0c-141">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="30a0c-141">-Name</span></span>
<span data-ttu-id="30a0c-142">Określa nazwę portu frontoronu, który dodaje to polecenie.</span><span class="sxs-lookup"><span data-stu-id="30a0c-142">Specifies the name of the front-end port that this command adds.</span></span>

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

### <span data-ttu-id="30a0c-143">— Protokół</span><span class="sxs-lookup"><span data-stu-id="30a0c-143">-Protocol</span></span>
<span data-ttu-id="30a0c-144">Określa protokół odbiorcy HTTP.</span><span class="sxs-lookup"><span data-stu-id="30a0c-144">Specifies the protocol of the HTTP listener.</span></span>
<span data-ttu-id="30a0c-145">Obsługiwane są protokoły HTTP i HTTPS.</span><span class="sxs-lookup"><span data-stu-id="30a0c-145">Both HTTP and HTTPS are supported.</span></span>

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

### <span data-ttu-id="30a0c-146">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="30a0c-146">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="30a0c-147">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="30a0c-147">-SslCertificate</span></span>
<span data-ttu-id="30a0c-148">Określa certyfikat SSL odbiorcy HTTP.</span><span class="sxs-lookup"><span data-stu-id="30a0c-148">Specifies the SSL certificate of the HTTP listener.</span></span>
<span data-ttu-id="30a0c-149">Musi zostać określony, jeśli protokół HTTPS jest wybrany jako protokół odbiorcy.</span><span class="sxs-lookup"><span data-stu-id="30a0c-149">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="30a0c-150">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="30a0c-150">-SslCertificateId</span></span>
<span data-ttu-id="30a0c-151">Określa identyfikator certyfikatu SSL dla słuchacza HTTP.</span><span class="sxs-lookup"><span data-stu-id="30a0c-151">Specifies the SSL certificate ID of the HTTP listener.</span></span>
<span data-ttu-id="30a0c-152">Musi zostać określony, jeśli protokół HTTPS jest wybrany jako protokół odbiorcy.</span><span class="sxs-lookup"><span data-stu-id="30a0c-152">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="30a0c-153">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="30a0c-153">-SslProfile</span></span>
<span data-ttu-id="30a0c-154">SslProfile</span><span class="sxs-lookup"><span data-stu-id="30a0c-154">SslProfile</span></span>

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

### <span data-ttu-id="30a0c-155">-SslProfileId</span><span class="sxs-lookup"><span data-stu-id="30a0c-155">-SslProfileId</span></span>
<span data-ttu-id="30a0c-156">SslProfileId</span><span class="sxs-lookup"><span data-stu-id="30a0c-156">SslProfileId</span></span>

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

### <span data-ttu-id="30a0c-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30a0c-157">CommonParameters</span></span>
<span data-ttu-id="30a0c-158">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30a0c-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30a0c-159">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30a0c-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30a0c-160">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="30a0c-160">INPUTS</span></span>

### <span data-ttu-id="30a0c-161">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="30a0c-161">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="30a0c-162">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="30a0c-162">OUTPUTS</span></span>

### <span data-ttu-id="30a0c-163">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="30a0c-163">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="30a0c-164">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="30a0c-164">NOTES</span></span>

## <span data-ttu-id="30a0c-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="30a0c-165">RELATED LINKS</span></span>

[<span data-ttu-id="30a0c-166">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="30a0c-166">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="30a0c-167">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="30a0c-167">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="30a0c-168">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="30a0c-168">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="30a0c-169">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="30a0c-169">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


