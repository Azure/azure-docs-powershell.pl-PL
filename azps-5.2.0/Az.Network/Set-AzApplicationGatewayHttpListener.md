---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 8ce5d01d78b8b434e062b0f33ee41a4cbbce20ed
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342646"
---
# <span data-ttu-id="fe343-101">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="fe343-101">Set-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="fe343-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fe343-102">SYNOPSIS</span></span>
<span data-ttu-id="fe343-103">Modyfikuje odbiornik HTTP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="fe343-103">Modifies an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="fe343-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fe343-104">SYNTAX</span></span>

### <span data-ttu-id="fe343-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="fe343-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-FirewallPolicyId <String>] [-SslProfileId <String>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fe343-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="fe343-106">SetByResource</span></span>
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

## <span data-ttu-id="fe343-107">Opis</span><span class="sxs-lookup"><span data-stu-id="fe343-107">DESCRIPTION</span></span>
<span data-ttu-id="fe343-108">Polecenie cmdlet **Set-AzApplicationGatewayHttpListener** modyfikuje odbiornik http dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fe343-108">The **Set-AzApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="fe343-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fe343-109">EXAMPLES</span></span>

### <span data-ttu-id="fe343-110">Przykład 1: Ustawianie odbiornika HTTP</span><span class="sxs-lookup"><span data-stu-id="fe343-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="fe343-111">Pierwsze polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="fe343-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="fe343-112">Drugie polecenie ustawia odbiornik HTTP dla bramy w celu używania konfiguracji frontonu przechowywanej w $FIP 01 z protokołem HTTP w porcie 80.</span><span class="sxs-lookup"><span data-stu-id="fe343-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

### <span data-ttu-id="fe343-113">Przykład 2: Dodawanie odbiornika HTTPS przy użyciu protokołu SSL i nazw hostów</span><span class="sxs-lookup"><span data-stu-id="fe343-113">Example 2: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="fe343-114">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="fe343-114">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="fe343-115">Drugie polecenie dodaje odbiornik, który używa protokołu HTTPS z certyfikatami SSL i hostami do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="fe343-115">The second command adds the listener, which uses the HTTPS protocol, with SSL Certificates and HostNames, to the application gateway.</span></span>

## <span data-ttu-id="fe343-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fe343-116">PARAMETERS</span></span>

### <span data-ttu-id="fe343-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fe343-117">-ApplicationGateway</span></span>
<span data-ttu-id="fe343-118">Określa bramę aplikacji, za pomocą której ten aplet polecenia kojarzy odbiornik HTTP.</span><span class="sxs-lookup"><span data-stu-id="fe343-118">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="fe343-119">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="fe343-119">-CustomErrorConfiguration</span></span>
<span data-ttu-id="fe343-120">Błąd klienta bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="fe343-120">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="fe343-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe343-121">-DefaultProfile</span></span>
<span data-ttu-id="fe343-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fe343-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe343-123">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="fe343-123">-FirewallPolicy</span></span>
<span data-ttu-id="fe343-124">FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="fe343-124">FirewallPolicy</span></span>

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

### <span data-ttu-id="fe343-125">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="fe343-125">-FirewallPolicyId</span></span>
<span data-ttu-id="fe343-126">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="fe343-126">FirewallPolicyId</span></span>

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

### <span data-ttu-id="fe343-127">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="fe343-127">-FrontendIPConfiguration</span></span>
<span data-ttu-id="fe343-128">Określa adres IP frontonu bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="fe343-128">Specifies the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="fe343-129">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="fe343-129">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="fe343-130">Określa identyfikator adresu IP frontonu bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="fe343-130">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="fe343-131">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="fe343-131">-FrontendPort</span></span>
<span data-ttu-id="fe343-132">Określa port frontonu bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="fe343-132">Specifies the application gateway front-end port.</span></span>

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

### <span data-ttu-id="fe343-133">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="fe343-133">-FrontendPortId</span></span>
<span data-ttu-id="fe343-134">Określa identyfikator portu frontonu bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="fe343-134">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="fe343-135">-HostName</span><span class="sxs-lookup"><span data-stu-id="fe343-135">-HostName</span></span>
<span data-ttu-id="fe343-136">Określa nazwę hosta, do którego to polecenie cmdlet wysyła odbiornik HTTP.</span><span class="sxs-lookup"><span data-stu-id="fe343-136">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="fe343-137">-Nazwa_hostas</span><span class="sxs-lookup"><span data-stu-id="fe343-137">-HostNames</span></span>
<span data-ttu-id="fe343-138">Nazwy hostów</span><span class="sxs-lookup"><span data-stu-id="fe343-138">Host names</span></span>

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

### <span data-ttu-id="fe343-139">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fe343-139">-Name</span></span>
<span data-ttu-id="fe343-140">Określa nazwę odbiornika HTTP.</span><span class="sxs-lookup"><span data-stu-id="fe343-140">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="fe343-141">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="fe343-141">-Protocol</span></span>
<span data-ttu-id="fe343-142">Określa protokół używany przez odbiornik HTTP.</span><span class="sxs-lookup"><span data-stu-id="fe343-142">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="fe343-143">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="fe343-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fe343-144">URL</span><span class="sxs-lookup"><span data-stu-id="fe343-144">Http</span></span>
- <span data-ttu-id="fe343-145">Https</span><span class="sxs-lookup"><span data-stu-id="fe343-145">Https</span></span>

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

### <span data-ttu-id="fe343-146">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="fe343-146">-RequireServerNameIndication</span></span>
<span data-ttu-id="fe343-147">Określa, czy polecenie cmdlet wymaga wskazania nazwy serwera.</span><span class="sxs-lookup"><span data-stu-id="fe343-147">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="fe343-148">Dopuszczalne wartości tego parametru to: prawda lub FAŁSZ.</span><span class="sxs-lookup"><span data-stu-id="fe343-148">The acceptable values for this parameter are: true or false.</span></span>

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

### <span data-ttu-id="fe343-149">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="fe343-149">-SslCertificate</span></span>
<span data-ttu-id="fe343-150">Określa certyfikat SSL odbiornika HTTP.</span><span class="sxs-lookup"><span data-stu-id="fe343-150">Specifies the SSL certificate of the HTTP listener.</span></span>

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

### <span data-ttu-id="fe343-151">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="fe343-151">-SslCertificateId</span></span>
<span data-ttu-id="fe343-152">Określa identyfikator certyfikatu protokołu SSL (Secure Sockets Layer) odbiornika HTTP.</span><span class="sxs-lookup"><span data-stu-id="fe343-152">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="fe343-153">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="fe343-153">-SslProfile</span></span>
<span data-ttu-id="fe343-154">SslProfile</span><span class="sxs-lookup"><span data-stu-id="fe343-154">SslProfile</span></span>

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

### <span data-ttu-id="fe343-155">-SslProfileId</span><span class="sxs-lookup"><span data-stu-id="fe343-155">-SslProfileId</span></span>
<span data-ttu-id="fe343-156">SslProfileId</span><span class="sxs-lookup"><span data-stu-id="fe343-156">SslProfileId</span></span>

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

### <span data-ttu-id="fe343-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe343-157">CommonParameters</span></span>
<span data-ttu-id="fe343-158">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe343-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe343-159">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe343-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe343-160">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe343-160">INPUTS</span></span>

### <span data-ttu-id="fe343-161">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fe343-161">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fe343-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fe343-162">OUTPUTS</span></span>

### <span data-ttu-id="fe343-163">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fe343-163">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fe343-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fe343-164">NOTES</span></span>

## <span data-ttu-id="fe343-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fe343-165">RELATED LINKS</span></span>

[<span data-ttu-id="fe343-166">Dodaj-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="fe343-166">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="fe343-167">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="fe343-167">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="fe343-168">Nowe — AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="fe343-168">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="fe343-169">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="fe343-169">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)


