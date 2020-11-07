---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1E192553-61D8-4449-936B-68CF866C710C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: 34c40e17ca1ae297677c05ffc198c7580ef7c4a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717106"
---
# <span data-ttu-id="9fa16-101">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="9fa16-101">Add-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="9fa16-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9fa16-102">SYNOPSIS</span></span>
<span data-ttu-id="9fa16-103">Dodaje odbiornik HTTP do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9fa16-103">Adds an HTTP listener to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fa16-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9fa16-104">SYNTAX</span></span>

### <span data-ttu-id="9fa16-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9fa16-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9fa16-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9fa16-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9fa16-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9fa16-107">DESCRIPTION</span></span>
<span data-ttu-id="9fa16-108">Polecenie cmdlet **Add-AzureRmApplicationGatewayHttpListener** umożliwia dodanie odbiornika HTTP do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9fa16-108">The **Add-AzureRmApplicationGatewayHttpListener** cmdlet adds a HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="9fa16-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9fa16-109">EXAMPLES</span></span>

### <span data-ttu-id="9fa16-110">Przykład 1: Dodawanie odbiornika HTTP</span><span class="sxs-lookup"><span data-stu-id="9fa16-110">Example 1: Add a HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

<span data-ttu-id="9fa16-111">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $AppGw. Drugie polecenie dodaje odbiornik HTTP do bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="9fa16-111">The first command gets the application gateway and stores it in the $AppGw variable.The second command adds the HTTP listener to the application gateway.</span></span>

### <span data-ttu-id="9fa16-112">Przykład 2: Dodawanie odbiornika HTTPS przy użyciu protokołu SSL</span><span class="sxs-lookup"><span data-stu-id="9fa16-112">Example 2: Add a HTTPS listener with SSL</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="9fa16-113">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="9fa16-113">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="9fa16-114">Drugie polecenie dodaje odbiornik, który używa protokołu HTTPS, do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9fa16-114">The second command adds the listener, which uses the HTTPS protocol, to the application gateway.</span></span>

## <span data-ttu-id="9fa16-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9fa16-115">PARAMETERS</span></span>

### <span data-ttu-id="9fa16-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9fa16-116">-ApplicationGateway</span></span>
<span data-ttu-id="9fa16-117">Określa bramę aplikacji, z którą to polecenie cmdlet dodaje odbiornik HTTP.</span><span class="sxs-lookup"><span data-stu-id="9fa16-117">Specifies the application gateway to which this cmdlet adds an HTTP listener.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9fa16-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fa16-118">-DefaultProfile</span></span>
<span data-ttu-id="9fa16-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9fa16-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fa16-120">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9fa16-120">-FrontendIPConfiguration</span></span>
<span data-ttu-id="9fa16-121">Określa obiekt zasobu IP frontonu bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9fa16-121">Specifies the application gateway front-end IP resource object.</span></span>

```yaml
Type: PSApplicationGatewayFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fa16-122">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="9fa16-122">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="9fa16-123">Określa identyfikator IP frontonu bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9fa16-123">Specifies the application gateway front-end IP ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fa16-124">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="9fa16-124">-FrontendPort</span></span>
<span data-ttu-id="9fa16-125">Określa obiekt frontonu bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9fa16-125">Specifies the application gateway front-end port object.</span></span>

```yaml
Type: PSApplicationGatewayFrontendPort
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fa16-126">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="9fa16-126">-FrontendPortId</span></span>
<span data-ttu-id="9fa16-127">Określa identyfikator portu frontonu bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9fa16-127">Specifies the application gateway front-end port ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fa16-128">-HostName</span><span class="sxs-lookup"><span data-stu-id="9fa16-128">-HostName</span></span>
<span data-ttu-id="9fa16-129">Określa nazwę hosta, do którego to polecenie cmdlet dodaje odbiornik HTTP.</span><span class="sxs-lookup"><span data-stu-id="9fa16-129">Specifies the host name that this cmdlet adds a HTTP listener to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fa16-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9fa16-130">-Name</span></span>
<span data-ttu-id="9fa16-131">Określa nazwę portu frontonu, który jest dodawany przez to polecenie.</span><span class="sxs-lookup"><span data-stu-id="9fa16-131">Specifies the name of the front-end port that this command adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fa16-132">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="9fa16-132">-Protocol</span></span>
<span data-ttu-id="9fa16-133">Określa protokół odbiornika HTTP.</span><span class="sxs-lookup"><span data-stu-id="9fa16-133">Specifies the protocol of the HTTP listener.</span></span>
<span data-ttu-id="9fa16-134">Obsługiwane są zarówno protokoły HTTP, jak i HTTPS.</span><span class="sxs-lookup"><span data-stu-id="9fa16-134">Both HTTP and HTTPS are supported.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fa16-135">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="9fa16-135">-RequireServerNameIndication</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: true, false

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fa16-136">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="9fa16-136">-SslCertificate</span></span>
<span data-ttu-id="9fa16-137">Określa certyfikat SSL odbiornika HTTP.</span><span class="sxs-lookup"><span data-stu-id="9fa16-137">Specifies the SSL certificate of the HTTP listener.</span></span>
<span data-ttu-id="9fa16-138">Należy określić, czy protokół HTTPS jest wybrany jako protokół odbiornika.</span><span class="sxs-lookup"><span data-stu-id="9fa16-138">Must be specified if HTTPS is chosen as listener protocol.</span></span>

```yaml
Type: PSApplicationGatewaySslCertificate
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fa16-139">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="9fa16-139">-SslCertificateId</span></span>
<span data-ttu-id="9fa16-140">Określa identyfikator certyfikatu SSL odbiornika HTTP.</span><span class="sxs-lookup"><span data-stu-id="9fa16-140">Specifies the SSL certificate ID of the HTTP listener.</span></span>
<span data-ttu-id="9fa16-141">Należy określić, czy protokół HTTPS jest wybrany jako protokół odbiornika.</span><span class="sxs-lookup"><span data-stu-id="9fa16-141">Must be specified if HTTPS is chosen as listener protocol.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fa16-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fa16-142">CommonParameters</span></span>
<span data-ttu-id="9fa16-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fa16-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fa16-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fa16-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fa16-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9fa16-145">INPUTS</span></span>

### <span data-ttu-id="9fa16-146">System. String</span><span class="sxs-lookup"><span data-stu-id="9fa16-146">System.String</span></span>

## <span data-ttu-id="9fa16-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9fa16-147">OUTPUTS</span></span>

### <span data-ttu-id="9fa16-148">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9fa16-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9fa16-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9fa16-149">NOTES</span></span>

## <span data-ttu-id="9fa16-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9fa16-150">RELATED LINKS</span></span>

[<span data-ttu-id="9fa16-151">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="9fa16-151">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="9fa16-152">Nowe — AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="9fa16-152">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="9fa16-153">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="9fa16-153">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="9fa16-154">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="9fa16-154">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


