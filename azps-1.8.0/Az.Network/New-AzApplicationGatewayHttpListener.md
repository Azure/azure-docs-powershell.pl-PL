---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: e5593ae97692813cc36f14942edb21768517f317
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709373"
---
# <span data-ttu-id="a8624-101">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a8624-101">New-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="a8624-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a8624-102">SYNOPSIS</span></span>
<span data-ttu-id="a8624-103">Tworzy odbiornik HTTP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a8624-103">Creates an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="a8624-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a8624-104">SYNTAX</span></span>

### <span data-ttu-id="a8624-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a8624-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-HostName <String>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a8624-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="a8624-106">SetByResource</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a8624-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a8624-107">DESCRIPTION</span></span>
<span data-ttu-id="a8624-108">Polecenie cmdlet **New-AzApplicationGatewayHttpListener** umożliwia utworzenie odbiornika HTTP dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a8624-108">The **New-AzApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="a8624-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a8624-109">EXAMPLES</span></span>

### <span data-ttu-id="a8624-110">Przykład 1: Tworzenie odbiornika HTTP</span><span class="sxs-lookup"><span data-stu-id="a8624-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="a8624-111">To polecenie tworzy odbiornik HTTP o nazwie Listener01 i zapisuje wynik w zmiennej o nazwie $Listener.</span><span class="sxs-lookup"><span data-stu-id="a8624-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="a8624-112">Przykład 2: Tworzenie odbiornika HTTP przy użyciu protokołu SSL</span><span class="sxs-lookup"><span data-stu-id="a8624-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="a8624-113">To polecenie tworzy odbiornik HTTP używający odciążania SSL i dostarcza certyfikat SSL w zmiennej $SSLCert 01.</span><span class="sxs-lookup"><span data-stu-id="a8624-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="a8624-114">Polecenie zapisuje wynik w zmiennej o nazwie $Listener.</span><span class="sxs-lookup"><span data-stu-id="a8624-114">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="a8624-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a8624-115">PARAMETERS</span></span>

### <span data-ttu-id="a8624-116">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="a8624-116">-CustomErrorConfiguration</span></span>
<span data-ttu-id="a8624-117">Błąd klienta bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="a8624-117">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="a8624-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8624-118">-DefaultProfile</span></span>
<span data-ttu-id="a8624-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a8624-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8624-120">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a8624-120">-FrontendIPConfiguration</span></span>
<span data-ttu-id="a8624-121">Określa obiekt konfiguracji IP frontonu dla odbiornika HTTP.</span><span class="sxs-lookup"><span data-stu-id="a8624-121">Specifies front-end IP configuration object for the HTTP listener.</span></span>

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

### <span data-ttu-id="a8624-122">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="a8624-122">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="a8624-123">Określa identyfikator zewnętrznej konfiguracji IP dla odbiornika HTTP.</span><span class="sxs-lookup"><span data-stu-id="a8624-123">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="a8624-124">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="a8624-124">-FrontendPort</span></span>
<span data-ttu-id="a8624-125">Określa port frontonu dla odbiornika HTTP.</span><span class="sxs-lookup"><span data-stu-id="a8624-125">Specifies the front-end port for the HTTP listener.</span></span>

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

### <span data-ttu-id="a8624-126">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="a8624-126">-FrontendPortId</span></span>
<span data-ttu-id="a8624-127">Określa identyfikator obiektu typu front-end dla odbiornika HTTP.</span><span class="sxs-lookup"><span data-stu-id="a8624-127">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="a8624-128">-HostName</span><span class="sxs-lookup"><span data-stu-id="a8624-128">-HostName</span></span>
<span data-ttu-id="a8624-129">Określa nazwę hosta odbiornika HTTP bramy Application.</span><span class="sxs-lookup"><span data-stu-id="a8624-129">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="a8624-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a8624-130">-Name</span></span>
<span data-ttu-id="a8624-131">Określa nazwę odbiornika HTTP, który tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8624-131">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="a8624-132">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="a8624-132">-Protocol</span></span>
<span data-ttu-id="a8624-133">Określa protokół używany przez odbiornik HTTP.</span><span class="sxs-lookup"><span data-stu-id="a8624-133">Specifies the protocol that the HTTP listener uses.</span></span>

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

### <span data-ttu-id="a8624-134">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="a8624-134">-RequireServerNameIndication</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: true, false

Required: False
Position: Named
Default value: true
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8624-135">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="a8624-135">-SslCertificate</span></span>
<span data-ttu-id="a8624-136">Określa obiekt certyfikatu SSL dla odbiornika HTTP.</span><span class="sxs-lookup"><span data-stu-id="a8624-136">Specifies the SSL certificate object for the HTTP listener.</span></span>

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

### <span data-ttu-id="a8624-137">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="a8624-137">-SslCertificateId</span></span>
<span data-ttu-id="a8624-138">Określa identyfikator certyfikatu SSL dla odbiornika HTTP.</span><span class="sxs-lookup"><span data-stu-id="a8624-138">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="a8624-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8624-139">CommonParameters</span></span>
<span data-ttu-id="a8624-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8624-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8624-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8624-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8624-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a8624-142">INPUTS</span></span>

### <span data-ttu-id="a8624-143">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a8624-143">None</span></span>

## <span data-ttu-id="a8624-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a8624-144">OUTPUTS</span></span>

### <span data-ttu-id="a8624-145">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a8624-145">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="a8624-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a8624-146">NOTES</span></span>

## <span data-ttu-id="a8624-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a8624-147">RELATED LINKS</span></span>

[<span data-ttu-id="a8624-148">Dodaj-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a8624-148">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="a8624-149">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a8624-149">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="a8624-150">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a8624-150">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="a8624-151">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a8624-151">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


