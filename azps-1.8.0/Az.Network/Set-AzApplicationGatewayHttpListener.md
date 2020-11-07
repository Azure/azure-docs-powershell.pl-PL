---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 11a416e237ff4a12dc3aafbd161e1ae77faab732
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709020"
---
# <span data-ttu-id="16d7a-101">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="16d7a-101">Set-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="16d7a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="16d7a-102">SYNOPSIS</span></span>
<span data-ttu-id="16d7a-103">Modyfikuje odbiornik HTTP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="16d7a-103">Modifies an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="16d7a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="16d7a-104">SYNTAX</span></span>

### <span data-ttu-id="16d7a-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="16d7a-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="16d7a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="16d7a-106">SetByResource</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="16d7a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="16d7a-107">DESCRIPTION</span></span>
<span data-ttu-id="16d7a-108">Polecenie cmdlet **Set-AzApplicationGatewayHttpListener** modyfikuje odbiornik http dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="16d7a-108">The **Set-AzApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="16d7a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="16d7a-109">EXAMPLES</span></span>

### <span data-ttu-id="16d7a-110">Przykład 1: Ustawianie odbiornika HTTP</span><span class="sxs-lookup"><span data-stu-id="16d7a-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="16d7a-111">Pierwsze polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="16d7a-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="16d7a-112">Drugie polecenie ustawia odbiornik HTTP dla bramy w celu używania konfiguracji frontonu przechowywanej w $FIP 01 z protokołem HTTP w porcie 80.</span><span class="sxs-lookup"><span data-stu-id="16d7a-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

## <span data-ttu-id="16d7a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="16d7a-113">PARAMETERS</span></span>

### <span data-ttu-id="16d7a-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="16d7a-114">-ApplicationGateway</span></span>
<span data-ttu-id="16d7a-115">Określa bramę aplikacji, za pomocą której ten aplet polecenia kojarzy odbiornik HTTP.</span><span class="sxs-lookup"><span data-stu-id="16d7a-115">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="16d7a-116">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="16d7a-116">-CustomErrorConfiguration</span></span>
<span data-ttu-id="16d7a-117">Błąd klienta bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="16d7a-117">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="16d7a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16d7a-118">-DefaultProfile</span></span>
<span data-ttu-id="16d7a-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="16d7a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16d7a-120">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="16d7a-120">-FrontendIPConfiguration</span></span>
<span data-ttu-id="16d7a-121">Określa adres IP frontonu bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="16d7a-121">Specifies the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="16d7a-122">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="16d7a-122">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="16d7a-123">Określa identyfikator adresu IP frontonu bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="16d7a-123">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="16d7a-124">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="16d7a-124">-FrontendPort</span></span>
<span data-ttu-id="16d7a-125">Określa port frontonu bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="16d7a-125">Specifies the application gateway front-end port.</span></span>

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

### <span data-ttu-id="16d7a-126">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="16d7a-126">-FrontendPortId</span></span>
<span data-ttu-id="16d7a-127">Określa identyfikator portu frontonu bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="16d7a-127">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="16d7a-128">-HostName</span><span class="sxs-lookup"><span data-stu-id="16d7a-128">-HostName</span></span>
<span data-ttu-id="16d7a-129">Określa nazwę hosta, do którego to polecenie cmdlet wysyła odbiornik HTTP.</span><span class="sxs-lookup"><span data-stu-id="16d7a-129">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="16d7a-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="16d7a-130">-Name</span></span>
<span data-ttu-id="16d7a-131">Określa nazwę odbiornika HTTP.</span><span class="sxs-lookup"><span data-stu-id="16d7a-131">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="16d7a-132">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="16d7a-132">-Protocol</span></span>
<span data-ttu-id="16d7a-133">Określa protokół używany przez odbiornik HTTP.</span><span class="sxs-lookup"><span data-stu-id="16d7a-133">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="16d7a-134">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="16d7a-134">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="16d7a-135">URL</span><span class="sxs-lookup"><span data-stu-id="16d7a-135">Http</span></span>
- <span data-ttu-id="16d7a-136">Https</span><span class="sxs-lookup"><span data-stu-id="16d7a-136">Https</span></span>

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

### <span data-ttu-id="16d7a-137">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="16d7a-137">-RequireServerNameIndication</span></span>
<span data-ttu-id="16d7a-138">Określa, czy polecenie cmdlet wymaga wskazania nazwy serwera.</span><span class="sxs-lookup"><span data-stu-id="16d7a-138">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="16d7a-139">Dopuszczalne wartości tego parametru to: prawda lub FAŁSZ.</span><span class="sxs-lookup"><span data-stu-id="16d7a-139">The acceptable values for this parameter are: true or false.</span></span>

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

### <span data-ttu-id="16d7a-140">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="16d7a-140">-SslCertificate</span></span>
<span data-ttu-id="16d7a-141">Określa certyfikat SSL odbiornika HTTP.</span><span class="sxs-lookup"><span data-stu-id="16d7a-141">Specifies the SSL certificate of the HTTP listener.</span></span>

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

### <span data-ttu-id="16d7a-142">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="16d7a-142">-SslCertificateId</span></span>
<span data-ttu-id="16d7a-143">Określa identyfikator certyfikatu protokołu SSL (Secure Sockets Layer) odbiornika HTTP.</span><span class="sxs-lookup"><span data-stu-id="16d7a-143">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="16d7a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16d7a-144">CommonParameters</span></span>
<span data-ttu-id="16d7a-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16d7a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16d7a-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16d7a-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16d7a-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="16d7a-147">INPUTS</span></span>

### <span data-ttu-id="16d7a-148">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="16d7a-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="16d7a-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="16d7a-149">OUTPUTS</span></span>

### <span data-ttu-id="16d7a-150">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="16d7a-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="16d7a-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="16d7a-151">NOTES</span></span>

## <span data-ttu-id="16d7a-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="16d7a-152">RELATED LINKS</span></span>

[<span data-ttu-id="16d7a-153">Dodaj-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="16d7a-153">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="16d7a-154">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="16d7a-154">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="16d7a-155">Nowe — AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="16d7a-155">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="16d7a-156">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="16d7a-156">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)


