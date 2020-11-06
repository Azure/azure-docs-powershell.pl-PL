---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: 231ee3dc8d66d3960f0416cb410b6747b25ae278
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552620"
---
# <span data-ttu-id="db9b8-101">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="db9b8-101">Set-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="db9b8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="db9b8-102">SYNOPSIS</span></span>
<span data-ttu-id="db9b8-103">Modyfikuje odbiornik HTTP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="db9b8-103">Modifies an HTTP listener for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db9b8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="db9b8-104">SYNTAX</span></span>

### <span data-ttu-id="db9b8-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="db9b8-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db9b8-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="db9b8-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db9b8-107">Opis</span><span class="sxs-lookup"><span data-stu-id="db9b8-107">DESCRIPTION</span></span>
<span data-ttu-id="db9b8-108">Polecenie cmdlet **Set-AzureRmApplicationGatewayHttpListener** modyfikuje odbiornik http dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="db9b8-108">The **Set-AzureRmApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="db9b8-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="db9b8-109">EXAMPLES</span></span>

### <span data-ttu-id="db9b8-110">Przykład 1: Ustawianie odbiornika HTTP</span><span class="sxs-lookup"><span data-stu-id="db9b8-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="db9b8-111">Pierwsze polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="db9b8-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="db9b8-112">Drugie polecenie ustawia odbiornik HTTP dla bramy w celu używania konfiguracji frontonu przechowywanej w $FIP 01 z protokołem HTTP w porcie 80.</span><span class="sxs-lookup"><span data-stu-id="db9b8-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

## <span data-ttu-id="db9b8-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="db9b8-113">PARAMETERS</span></span>

### <span data-ttu-id="db9b8-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="db9b8-114">-ApplicationGateway</span></span>
<span data-ttu-id="db9b8-115">Określa bramę aplikacji, za pomocą której ten aplet polecenia kojarzy odbiornik HTTP.</span><span class="sxs-lookup"><span data-stu-id="db9b8-115">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="db9b8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db9b8-116">-DefaultProfile</span></span>
<span data-ttu-id="db9b8-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="db9b8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db9b8-118">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="db9b8-118">-FrontendIPConfiguration</span></span>
<span data-ttu-id="db9b8-119">Określa adres IP frontonu bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="db9b8-119">Specifies the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="db9b8-120">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="db9b8-120">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="db9b8-121">Określa identyfikator adresu IP frontonu bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="db9b8-121">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="db9b8-122">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="db9b8-122">-FrontendPort</span></span>
<span data-ttu-id="db9b8-123">Określa port frontonu bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="db9b8-123">Specifies the application gateway front-end port.</span></span>

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

### <span data-ttu-id="db9b8-124">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="db9b8-124">-FrontendPortId</span></span>
<span data-ttu-id="db9b8-125">Określa identyfikator portu frontonu bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="db9b8-125">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="db9b8-126">-HostName</span><span class="sxs-lookup"><span data-stu-id="db9b8-126">-HostName</span></span>
<span data-ttu-id="db9b8-127">Określa nazwę hosta, do którego to polecenie cmdlet wysyła odbiornik HTTP.</span><span class="sxs-lookup"><span data-stu-id="db9b8-127">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="db9b8-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="db9b8-128">-Name</span></span>
<span data-ttu-id="db9b8-129">Określa nazwę odbiornika HTTP.</span><span class="sxs-lookup"><span data-stu-id="db9b8-129">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="db9b8-130">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="db9b8-130">-Protocol</span></span>
<span data-ttu-id="db9b8-131">Określa protokół używany przez odbiornik HTTP.</span><span class="sxs-lookup"><span data-stu-id="db9b8-131">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="db9b8-132">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="db9b8-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="db9b8-133">URL</span><span class="sxs-lookup"><span data-stu-id="db9b8-133">Http</span></span>
- <span data-ttu-id="db9b8-134">Https</span><span class="sxs-lookup"><span data-stu-id="db9b8-134">Https</span></span>

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

### <span data-ttu-id="db9b8-135">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="db9b8-135">-RequireServerNameIndication</span></span>
<span data-ttu-id="db9b8-136">Określa, czy polecenie cmdlet wymaga wskazania nazwy serwera.</span><span class="sxs-lookup"><span data-stu-id="db9b8-136">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="db9b8-137">Dopuszczalne wartości tego parametru to: prawda lub FAŁSZ.</span><span class="sxs-lookup"><span data-stu-id="db9b8-137">The acceptable values for this parameter are: true or false.</span></span>

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

### <span data-ttu-id="db9b8-138">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="db9b8-138">-SslCertificate</span></span>
<span data-ttu-id="db9b8-139">Określa certyfikat SSL odbiornika HTTP.</span><span class="sxs-lookup"><span data-stu-id="db9b8-139">Specifies the SSL certificate of the HTTP listener.</span></span>

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

### <span data-ttu-id="db9b8-140">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="db9b8-140">-SslCertificateId</span></span>
<span data-ttu-id="db9b8-141">Określa identyfikator certyfikatu protokołu SSL (Secure Sockets Layer) odbiornika HTTP.</span><span class="sxs-lookup"><span data-stu-id="db9b8-141">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="db9b8-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db9b8-142">CommonParameters</span></span>
<span data-ttu-id="db9b8-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db9b8-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db9b8-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db9b8-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db9b8-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="db9b8-145">INPUTS</span></span>

### <span data-ttu-id="db9b8-146">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="db9b8-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="db9b8-147">Parametry: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="db9b8-147">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="db9b8-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="db9b8-148">OUTPUTS</span></span>

### <span data-ttu-id="db9b8-149">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="db9b8-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="db9b8-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="db9b8-150">NOTES</span></span>

## <span data-ttu-id="db9b8-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="db9b8-151">RELATED LINKS</span></span>

[<span data-ttu-id="db9b8-152">Dodaj-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="db9b8-152">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="db9b8-153">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="db9b8-153">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="db9b8-154">Nowe — AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="db9b8-154">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="db9b8-155">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="db9b8-155">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)


