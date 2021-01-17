---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1E192553-61D8-4449-936B-68CF866C710C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: f769eb91d524bc9115199127833471246f6fdd1f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380317"
---
# <span data-ttu-id="e6cd8-101">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="e6cd8-101">Add-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="e6cd8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e6cd8-102">SYNOPSIS</span></span>
<span data-ttu-id="e6cd8-103">Dodaje odbiornik HTTP do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e6cd8-103">Adds an HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="e6cd8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e6cd8-104">SYNTAX</span></span>

### <span data-ttu-id="e6cd8-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e6cd8-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-FirewallPolicyId <String>] [-SslProfileId <String>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e6cd8-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e6cd8-106">SetByResource</span></span>
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

## <span data-ttu-id="e6cd8-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e6cd8-107">DESCRIPTION</span></span>
<span data-ttu-id="e6cd8-108">Polecenie cmdlet **Add-AzApplicationGatewayHttpListener** umożliwia dodanie odbiornika HTTP do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e6cd8-108">The **Add-AzApplicationGatewayHttpListener** cmdlet adds a HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="e6cd8-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e6cd8-109">EXAMPLES</span></span>

### <span data-ttu-id="e6cd8-110">Przykład 1: Dodawanie odbiornika HTTP</span><span class="sxs-lookup"><span data-stu-id="e6cd8-110">Example 1: Add a HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

<span data-ttu-id="e6cd8-111">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $AppGw. Drugie polecenie dodaje odbiornik HTTP do bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="e6cd8-111">The first command gets the application gateway and stores it in the $AppGw variable.The second command adds the HTTP listener to the application gateway.</span></span>

### <span data-ttu-id="e6cd8-112">Przykład 2: Dodawanie odbiornika HTTPS przy użyciu protokołu SSL</span><span class="sxs-lookup"><span data-stu-id="e6cd8-112">Example 2: Add a HTTPS listener with SSL</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="e6cd8-113">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="e6cd8-113">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e6cd8-114">Drugie polecenie dodaje odbiornik, który używa protokołu HTTPS, do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e6cd8-114">The second command adds the listener, which uses the HTTPS protocol, to the application gateway.</span></span>

### <span data-ttu-id="e6cd8-115">Przykład 3: Dodawanie odbiornika HTTPS przy użyciu protokołu SSL i nazw hostów</span><span class="sxs-lookup"><span data-stu-id="e6cd8-115">Example 3: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com","www.microsoft.com"
```

<span data-ttu-id="e6cd8-116">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="e6cd8-116">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e6cd8-117">Drugie polecenie dodaje odbiornik, który używa protokołu HTTPS z certyfikatami SSL i hostami do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e6cd8-117">The second command adds the listener, which uses the HTTPS protocol, with SSL Certificates and HostNames, to the application gateway.</span></span>

## <span data-ttu-id="e6cd8-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e6cd8-118">PARAMETERS</span></span>

### <span data-ttu-id="e6cd8-119">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e6cd8-119">-ApplicationGateway</span></span>
<span data-ttu-id="e6cd8-120">Określa bramę aplikacji, z którą to polecenie cmdlet dodaje odbiornik HTTP.</span><span class="sxs-lookup"><span data-stu-id="e6cd8-120">Specifies the application gateway to which this cmdlet adds an HTTP listener.</span></span>

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

### <span data-ttu-id="e6cd8-121">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="e6cd8-121">-CustomErrorConfiguration</span></span>
<span data-ttu-id="e6cd8-122">Błąd klienta bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="e6cd8-122">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="e6cd8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6cd8-123">-DefaultProfile</span></span>
<span data-ttu-id="e6cd8-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e6cd8-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6cd8-125">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="e6cd8-125">-FirewallPolicy</span></span>
<span data-ttu-id="e6cd8-126">FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="e6cd8-126">FirewallPolicy</span></span>

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

### <span data-ttu-id="e6cd8-127">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="e6cd8-127">-FirewallPolicyId</span></span>
<span data-ttu-id="e6cd8-128">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="e6cd8-128">FirewallPolicyId</span></span>

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

### <span data-ttu-id="e6cd8-129">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e6cd8-129">-FrontendIPConfiguration</span></span>
<span data-ttu-id="e6cd8-130">Określa obiekt zasobu IP frontonu bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e6cd8-130">Specifies the application gateway front-end IP resource object.</span></span>

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

### <span data-ttu-id="e6cd8-131">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e6cd8-131">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="e6cd8-132">Określa identyfikator IP frontonu bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e6cd8-132">Specifies the application gateway front-end IP ID.</span></span>

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

### <span data-ttu-id="e6cd8-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="e6cd8-133">-FrontendPort</span></span>
<span data-ttu-id="e6cd8-134">Określa obiekt frontonu bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e6cd8-134">Specifies the application gateway front-end port object.</span></span>

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

### <span data-ttu-id="e6cd8-135">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="e6cd8-135">-FrontendPortId</span></span>
<span data-ttu-id="e6cd8-136">Określa identyfikator portu frontonu bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e6cd8-136">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="e6cd8-137">-HostName</span><span class="sxs-lookup"><span data-stu-id="e6cd8-137">-HostName</span></span>
<span data-ttu-id="e6cd8-138">Określa nazwę hosta, do którego to polecenie cmdlet dodaje odbiornik HTTP.</span><span class="sxs-lookup"><span data-stu-id="e6cd8-138">Specifies the host name that this cmdlet adds a HTTP listener to.</span></span>

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

### <span data-ttu-id="e6cd8-139">-Nazwa_hostas</span><span class="sxs-lookup"><span data-stu-id="e6cd8-139">-HostNames</span></span>
<span data-ttu-id="e6cd8-140">Nazwy hostów</span><span class="sxs-lookup"><span data-stu-id="e6cd8-140">Host names</span></span>

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

### <span data-ttu-id="e6cd8-141">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e6cd8-141">-Name</span></span>
<span data-ttu-id="e6cd8-142">Określa nazwę portu frontonu, który jest dodawany przez to polecenie.</span><span class="sxs-lookup"><span data-stu-id="e6cd8-142">Specifies the name of the front-end port that this command adds.</span></span>

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

### <span data-ttu-id="e6cd8-143">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="e6cd8-143">-Protocol</span></span>
<span data-ttu-id="e6cd8-144">Określa protokół odbiornika HTTP.</span><span class="sxs-lookup"><span data-stu-id="e6cd8-144">Specifies the protocol of the HTTP listener.</span></span>
<span data-ttu-id="e6cd8-145">Obsługiwane są zarówno protokoły HTTP, jak i HTTPS.</span><span class="sxs-lookup"><span data-stu-id="e6cd8-145">Both HTTP and HTTPS are supported.</span></span>

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

### <span data-ttu-id="e6cd8-146">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="e6cd8-146">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="e6cd8-147">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="e6cd8-147">-SslCertificate</span></span>
<span data-ttu-id="e6cd8-148">Określa certyfikat SSL odbiornika HTTP.</span><span class="sxs-lookup"><span data-stu-id="e6cd8-148">Specifies the SSL certificate of the HTTP listener.</span></span>
<span data-ttu-id="e6cd8-149">Należy określić, czy protokół HTTPS jest wybrany jako protokół odbiornika.</span><span class="sxs-lookup"><span data-stu-id="e6cd8-149">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="e6cd8-150">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="e6cd8-150">-SslCertificateId</span></span>
<span data-ttu-id="e6cd8-151">Określa identyfikator certyfikatu SSL odbiornika HTTP.</span><span class="sxs-lookup"><span data-stu-id="e6cd8-151">Specifies the SSL certificate ID of the HTTP listener.</span></span>
<span data-ttu-id="e6cd8-152">Należy określić, czy protokół HTTPS jest wybrany jako protokół odbiornika.</span><span class="sxs-lookup"><span data-stu-id="e6cd8-152">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="e6cd8-153">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="e6cd8-153">-SslProfile</span></span>
<span data-ttu-id="e6cd8-154">SslProfile</span><span class="sxs-lookup"><span data-stu-id="e6cd8-154">SslProfile</span></span>

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

### <span data-ttu-id="e6cd8-155">-SslProfileId</span><span class="sxs-lookup"><span data-stu-id="e6cd8-155">-SslProfileId</span></span>
<span data-ttu-id="e6cd8-156">SslProfileId</span><span class="sxs-lookup"><span data-stu-id="e6cd8-156">SslProfileId</span></span>

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

### <span data-ttu-id="e6cd8-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6cd8-157">CommonParameters</span></span>
<span data-ttu-id="e6cd8-158">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6cd8-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6cd8-159">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e6cd8-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6cd8-160">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e6cd8-160">INPUTS</span></span>

### <span data-ttu-id="e6cd8-161">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e6cd8-161">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e6cd8-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e6cd8-162">OUTPUTS</span></span>

### <span data-ttu-id="e6cd8-163">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e6cd8-163">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e6cd8-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e6cd8-164">NOTES</span></span>

## <span data-ttu-id="e6cd8-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e6cd8-165">RELATED LINKS</span></span>

[<span data-ttu-id="e6cd8-166">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="e6cd8-166">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="e6cd8-167">Nowe — AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="e6cd8-167">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="e6cd8-168">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="e6cd8-168">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="e6cd8-169">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="e6cd8-169">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


