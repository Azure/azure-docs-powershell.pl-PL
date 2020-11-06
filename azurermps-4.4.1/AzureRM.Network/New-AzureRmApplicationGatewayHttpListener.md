---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: ea7a140d2dca2a590a8d3bc83e946d122fb8fd31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551827"
---
# <span data-ttu-id="b4ae0-101">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b4ae0-101">New-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="b4ae0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b4ae0-102">SYNOPSIS</span></span>
<span data-ttu-id="b4ae0-103">Tworzy odbiornik HTTP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b4ae0-103">Creates an HTTP listener for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4ae0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b4ae0-104">SYNTAX</span></span>

### <span data-ttu-id="b4ae0-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b4ae0-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-HostName <String>]
 [-RequireServerNameIndication <String>] -Protocol <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b4ae0-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b4ae0-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4ae0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b4ae0-107">DESCRIPTION</span></span>
<span data-ttu-id="b4ae0-108">Polecenie cmdlet **New-AzureRmApplicationGatewayHttpListener** umożliwia utworzenie odbiornika HTTP dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b4ae0-108">The **New-AzureRmApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="b4ae0-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b4ae0-109">EXAMPLES</span></span>

### <span data-ttu-id="b4ae0-110">Przykład 1: Tworzenie odbiornika HTTP</span><span class="sxs-lookup"><span data-stu-id="b4ae0-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzureRmApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="b4ae0-111">To polecenie tworzy odbiornik HTTP o nazwie Listener01 i zapisuje wynik w zmiennej o nazwie $Listener.</span><span class="sxs-lookup"><span data-stu-id="b4ae0-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="b4ae0-112">Przykład 2: Tworzenie odbiornika HTTP przy użyciu protokołu SSL</span><span class="sxs-lookup"><span data-stu-id="b4ae0-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzureRmApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="b4ae0-113">To polecenie tworzy odbiornik HTTP używający odciążania SSL i dostarcza certyfikat SSL w zmiennej $SSLCert 01.</span><span class="sxs-lookup"><span data-stu-id="b4ae0-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="b4ae0-114">Polecenie zapisuje wynik w zmiennej o nazwie $Listener.</span><span class="sxs-lookup"><span data-stu-id="b4ae0-114">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="b4ae0-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b4ae0-115">PARAMETERS</span></span>

### <span data-ttu-id="b4ae0-116">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4ae0-116">-FrontendIPConfiguration</span></span>
<span data-ttu-id="b4ae0-117">Określa obiekt konfiguracji IP frontonu dla odbiornika HTTP.</span><span class="sxs-lookup"><span data-stu-id="b4ae0-117">Specifies front-end IP configuration object for the HTTP listener.</span></span>

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

### <span data-ttu-id="b4ae0-118">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b4ae0-118">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="b4ae0-119">Określa identyfikator zewnętrznej konfiguracji IP dla odbiornika HTTP.</span><span class="sxs-lookup"><span data-stu-id="b4ae0-119">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="b4ae0-120">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="b4ae0-120">-FrontendPort</span></span>
<span data-ttu-id="b4ae0-121">Określa port frontonu dla odbiornika HTTP.</span><span class="sxs-lookup"><span data-stu-id="b4ae0-121">Specifies the front-end port for the HTTP listener.</span></span>

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

### <span data-ttu-id="b4ae0-122">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="b4ae0-122">-FrontendPortId</span></span>
<span data-ttu-id="b4ae0-123">Określa identyfikator obiektu typu front-end dla odbiornika HTTP.</span><span class="sxs-lookup"><span data-stu-id="b4ae0-123">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="b4ae0-124">-HostName</span><span class="sxs-lookup"><span data-stu-id="b4ae0-124">-HostName</span></span>
<span data-ttu-id="b4ae0-125">Określa nazwę hosta odbiornika HTTP bramy Application.</span><span class="sxs-lookup"><span data-stu-id="b4ae0-125">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="b4ae0-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b4ae0-126">-Name</span></span>
<span data-ttu-id="b4ae0-127">Określa nazwę odbiornika HTTP, który tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4ae0-127">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="b4ae0-128">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="b4ae0-128">-Protocol</span></span>
<span data-ttu-id="b4ae0-129">Określa protokół używany przez odbiornik HTTP.</span><span class="sxs-lookup"><span data-stu-id="b4ae0-129">Specifies the protocol that the HTTP listener uses.</span></span>

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

### <span data-ttu-id="b4ae0-130">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="b4ae0-130">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="b4ae0-131">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="b4ae0-131">-SslCertificate</span></span>
<span data-ttu-id="b4ae0-132">Określa obiekt certyfikatu SSL dla odbiornika HTTP.</span><span class="sxs-lookup"><span data-stu-id="b4ae0-132">Specifies the SSL certificate object for  the HTTP listener.</span></span>

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

### <span data-ttu-id="b4ae0-133">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="b4ae0-133">-SslCertificateId</span></span>
<span data-ttu-id="b4ae0-134">Określa identyfikator certyfikatu SSL dla odbiornika HTTP.</span><span class="sxs-lookup"><span data-stu-id="b4ae0-134">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="b4ae0-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4ae0-135">-DefaultProfile</span></span>
<span data-ttu-id="b4ae0-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b4ae0-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4ae0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4ae0-137">CommonParameters</span></span>
<span data-ttu-id="b4ae0-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4ae0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4ae0-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4ae0-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4ae0-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4ae0-140">INPUTS</span></span>

### <span data-ttu-id="b4ae0-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b4ae0-141">System.String</span></span>

## <span data-ttu-id="b4ae0-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b4ae0-142">OUTPUTS</span></span>

### <span data-ttu-id="b4ae0-143">Microsoft. Azure. Commands. Network. models. PSHttpListener</span><span class="sxs-lookup"><span data-stu-id="b4ae0-143">Microsoft.Azure.Commands.Network.Models.PSHttpListener</span></span>

## <span data-ttu-id="b4ae0-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b4ae0-144">NOTES</span></span>

## <span data-ttu-id="b4ae0-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b4ae0-145">RELATED LINKS</span></span>

[<span data-ttu-id="b4ae0-146">Dodaj-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b4ae0-146">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="b4ae0-147">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b4ae0-147">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="b4ae0-148">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b4ae0-148">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="b4ae0-149">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b4ae0-149">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


