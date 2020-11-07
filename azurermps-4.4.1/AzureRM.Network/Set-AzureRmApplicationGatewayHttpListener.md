---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: 6805eaa6f1d710c607a7911b628d3642d48ece29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717567"
---
# <span data-ttu-id="1136d-101">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1136d-101">Set-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="1136d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1136d-102">SYNOPSIS</span></span>
<span data-ttu-id="1136d-103">Modyfikuje odbiornik HTTP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1136d-103">Modifies an HTTP listener for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1136d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1136d-104">SYNTAX</span></span>

### <span data-ttu-id="1136d-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1136d-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1136d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="1136d-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1136d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1136d-107">DESCRIPTION</span></span>
<span data-ttu-id="1136d-108">Polecenie cmdlet **Set-AzureRmApplicationGatewayHttpListener** modyfikuje odbiornik http dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1136d-108">The **Set-AzureRmApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="1136d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1136d-109">EXAMPLES</span></span>

### <span data-ttu-id="1136d-110">Przykład 1: Ustawianie odbiornika HTTP</span><span class="sxs-lookup"><span data-stu-id="1136d-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="1136d-111">Pierwsze polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="1136d-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="1136d-112">Drugie polecenie ustawia odbiornik HTTP dla bramy w celu używania konfiguracji frontonu przechowywanej w $FIP 01 z protokołem HTTP w porcie 80.</span><span class="sxs-lookup"><span data-stu-id="1136d-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

## <span data-ttu-id="1136d-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1136d-113">PARAMETERS</span></span>

### <span data-ttu-id="1136d-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1136d-114">-ApplicationGateway</span></span>
<span data-ttu-id="1136d-115">Określa bramę aplikacji, za pomocą której ten aplet polecenia kojarzy odbiornik HTTP.</span><span class="sxs-lookup"><span data-stu-id="1136d-115">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="1136d-116">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="1136d-116">-FrontendIPConfiguration</span></span>
<span data-ttu-id="1136d-117">Określa adres IP frontonu bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1136d-117">Specifies the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="1136d-118">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="1136d-118">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="1136d-119">Określa identyfikator adresu IP frontonu bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1136d-119">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="1136d-120">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="1136d-120">-FrontendPort</span></span>
<span data-ttu-id="1136d-121">Określa port frontonu bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1136d-121">Specifies the application gateway front-end port.</span></span>

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

### <span data-ttu-id="1136d-122">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="1136d-122">-FrontendPortId</span></span>
<span data-ttu-id="1136d-123">Określa identyfikator portu frontonu bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1136d-123">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="1136d-124">-HostName</span><span class="sxs-lookup"><span data-stu-id="1136d-124">-HostName</span></span>
<span data-ttu-id="1136d-125">Określa nazwę hosta, do którego to polecenie cmdlet wysyła odbiornik HTTP.</span><span class="sxs-lookup"><span data-stu-id="1136d-125">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="1136d-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1136d-126">-Name</span></span>
<span data-ttu-id="1136d-127">Określa nazwę odbiornika HTTP.</span><span class="sxs-lookup"><span data-stu-id="1136d-127">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="1136d-128">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="1136d-128">-Protocol</span></span>
<span data-ttu-id="1136d-129">Określa protokół używany przez odbiornik HTTP.</span><span class="sxs-lookup"><span data-stu-id="1136d-129">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="1136d-130">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="1136d-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1136d-131">URL</span><span class="sxs-lookup"><span data-stu-id="1136d-131">Http</span></span>
- <span data-ttu-id="1136d-132">Https</span><span class="sxs-lookup"><span data-stu-id="1136d-132">Https</span></span>

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

### <span data-ttu-id="1136d-133">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="1136d-133">-RequireServerNameIndication</span></span>
<span data-ttu-id="1136d-134">Określa, czy polecenie cmdlet wymaga wskazania nazwy serwera.</span><span class="sxs-lookup"><span data-stu-id="1136d-134">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="1136d-135">Dopuszczalne wartości tego parametru to: prawda lub FAŁSZ.</span><span class="sxs-lookup"><span data-stu-id="1136d-135">The acceptable values for this parameter are: true or false.</span></span>

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

### <span data-ttu-id="1136d-136">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="1136d-136">-SslCertificate</span></span>
<span data-ttu-id="1136d-137">Określa certyfikat SSL odbiornika HTTP.</span><span class="sxs-lookup"><span data-stu-id="1136d-137">Specifies the SSL certificate of the HTTP listener.</span></span>

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

### <span data-ttu-id="1136d-138">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="1136d-138">-SslCertificateId</span></span>
<span data-ttu-id="1136d-139">Określa identyfikator certyfikatu protokołu SSL (Secure Sockets Layer) odbiornika HTTP.</span><span class="sxs-lookup"><span data-stu-id="1136d-139">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="1136d-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1136d-140">-DefaultProfile</span></span>
<span data-ttu-id="1136d-141">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1136d-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1136d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1136d-142">CommonParameters</span></span>
<span data-ttu-id="1136d-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1136d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1136d-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1136d-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1136d-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1136d-145">INPUTS</span></span>

### <span data-ttu-id="1136d-146">System. String</span><span class="sxs-lookup"><span data-stu-id="1136d-146">System.String</span></span>

## <span data-ttu-id="1136d-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1136d-147">OUTPUTS</span></span>

### <span data-ttu-id="1136d-148">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1136d-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1136d-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1136d-149">NOTES</span></span>

## <span data-ttu-id="1136d-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1136d-150">RELATED LINKS</span></span>

[<span data-ttu-id="1136d-151">Dodaj-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1136d-151">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="1136d-152">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1136d-152">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="1136d-153">Nowe — AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1136d-153">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="1136d-154">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1136d-154">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)


