---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1E192553-61D8-4449-936B-68CF866C710C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayhttplistener
schema: 2.0.0
ms.openlocfilehash: bda8ce00d316d57522bb307518c535c591e7b602
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899323"
---
# <span data-ttu-id="7cc1b-101">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7cc1b-101">Add-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="7cc1b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7cc1b-102">SYNOPSIS</span></span>
<span data-ttu-id="7cc1b-103">Dodaje odbiornik HTTP do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7cc1b-103">Adds an HTTP listener to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7cc1b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7cc1b-104">SYNTAX</span></span>

### <span data-ttu-id="7cc1b-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7cc1b-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7cc1b-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7cc1b-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7cc1b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7cc1b-107">DESCRIPTION</span></span>
<span data-ttu-id="7cc1b-108">Polecenie cmdlet **Add-AzureRmApplicationGatewayHttpListener** umożliwia dodanie odbiornika HTTP do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7cc1b-108">The **Add-AzureRmApplicationGatewayHttpListener** cmdlet adds a HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="7cc1b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7cc1b-109">EXAMPLES</span></span>

### <span data-ttu-id="7cc1b-110">Przykład 1: Dodawanie odbiornika HTTP</span><span class="sxs-lookup"><span data-stu-id="7cc1b-110">Example 1: Add a HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

<span data-ttu-id="7cc1b-111">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $AppGw. Drugie polecenie dodaje odbiornik HTTP do bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="7cc1b-111">The first command gets the application gateway and stores it in the $AppGw variable.The second command adds the HTTP listener to the application gateway.</span></span>

### <span data-ttu-id="7cc1b-112">Przykład 2: Dodawanie odbiornika HTTPS przy użyciu protokołu SSL</span><span class="sxs-lookup"><span data-stu-id="7cc1b-112">Example 2: Add a HTTPS listener with SSL</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="7cc1b-113">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="7cc1b-113">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7cc1b-114">Drugie polecenie dodaje odbiornik, który używa protokołu HTTPS, do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7cc1b-114">The second command adds the listener, which uses the HTTPS protocol, to the application gateway.</span></span>

## <span data-ttu-id="7cc1b-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7cc1b-115">PARAMETERS</span></span>

### <span data-ttu-id="7cc1b-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7cc1b-116">-ApplicationGateway</span></span>
<span data-ttu-id="7cc1b-117">Określa bramę aplikacji, z którą to polecenie cmdlet dodaje odbiornik HTTP.</span><span class="sxs-lookup"><span data-stu-id="7cc1b-117">Specifies the application gateway to which this cmdlet adds an HTTP listener.</span></span>

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

### <span data-ttu-id="7cc1b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cc1b-118">-DefaultProfile</span></span>
<span data-ttu-id="7cc1b-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7cc1b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7cc1b-120">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="7cc1b-120">-FrontendIPConfiguration</span></span>
<span data-ttu-id="7cc1b-121">Określa obiekt zasobu IP frontonu bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7cc1b-121">Specifies the application gateway front-end IP resource object.</span></span>

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

### <span data-ttu-id="7cc1b-122">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="7cc1b-122">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="7cc1b-123">Określa identyfikator IP frontonu bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7cc1b-123">Specifies the application gateway front-end IP ID.</span></span>

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

### <span data-ttu-id="7cc1b-124">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="7cc1b-124">-FrontendPort</span></span>
<span data-ttu-id="7cc1b-125">Określa obiekt frontonu bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7cc1b-125">Specifies the application gateway front-end port object.</span></span>

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

### <span data-ttu-id="7cc1b-126">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="7cc1b-126">-FrontendPortId</span></span>
<span data-ttu-id="7cc1b-127">Określa identyfikator portu frontonu bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7cc1b-127">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="7cc1b-128">-HostName</span><span class="sxs-lookup"><span data-stu-id="7cc1b-128">-HostName</span></span>
<span data-ttu-id="7cc1b-129">Określa nazwę hosta, do którego to polecenie cmdlet dodaje odbiornik HTTP.</span><span class="sxs-lookup"><span data-stu-id="7cc1b-129">Specifies the host name that this cmdlet adds a HTTP listener to.</span></span>

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

### <span data-ttu-id="7cc1b-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7cc1b-130">-Name</span></span>
<span data-ttu-id="7cc1b-131">Określa nazwę portu frontonu, który jest dodawany przez to polecenie.</span><span class="sxs-lookup"><span data-stu-id="7cc1b-131">Specifies the name of the front-end port that this command adds.</span></span>

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

### <span data-ttu-id="7cc1b-132">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="7cc1b-132">-Protocol</span></span>
<span data-ttu-id="7cc1b-133">Określa protokół odbiornika HTTP.</span><span class="sxs-lookup"><span data-stu-id="7cc1b-133">Specifies the protocol of the HTTP listener.</span></span>
<span data-ttu-id="7cc1b-134">Obsługiwane są zarówno protokoły HTTP, jak i HTTPS.</span><span class="sxs-lookup"><span data-stu-id="7cc1b-134">Both HTTP and HTTPS are supported.</span></span>

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

### <span data-ttu-id="7cc1b-135">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="7cc1b-135">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="7cc1b-136">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="7cc1b-136">-SslCertificate</span></span>
<span data-ttu-id="7cc1b-137">Określa certyfikat SSL odbiornika HTTP.</span><span class="sxs-lookup"><span data-stu-id="7cc1b-137">Specifies the SSL certificate of the HTTP listener.</span></span>
<span data-ttu-id="7cc1b-138">Należy określić, czy protokół HTTPS jest wybrany jako protokół odbiornika.</span><span class="sxs-lookup"><span data-stu-id="7cc1b-138">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="7cc1b-139">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="7cc1b-139">-SslCertificateId</span></span>
<span data-ttu-id="7cc1b-140">Określa identyfikator certyfikatu SSL odbiornika HTTP.</span><span class="sxs-lookup"><span data-stu-id="7cc1b-140">Specifies the SSL certificate ID of the HTTP listener.</span></span>
<span data-ttu-id="7cc1b-141">Należy określić, czy protokół HTTPS jest wybrany jako protokół odbiornika.</span><span class="sxs-lookup"><span data-stu-id="7cc1b-141">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="7cc1b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cc1b-142">CommonParameters</span></span>
<span data-ttu-id="7cc1b-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cc1b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cc1b-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cc1b-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cc1b-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7cc1b-145">INPUTS</span></span>

### <span data-ttu-id="7cc1b-146">System. String</span><span class="sxs-lookup"><span data-stu-id="7cc1b-146">System.String</span></span>

## <span data-ttu-id="7cc1b-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7cc1b-147">OUTPUTS</span></span>

### <span data-ttu-id="7cc1b-148">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7cc1b-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7cc1b-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7cc1b-149">NOTES</span></span>

## <span data-ttu-id="7cc1b-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7cc1b-150">RELATED LINKS</span></span>

[<span data-ttu-id="7cc1b-151">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7cc1b-151">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="7cc1b-152">Nowe — AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7cc1b-152">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="7cc1b-153">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7cc1b-153">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="7cc1b-154">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7cc1b-154">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


