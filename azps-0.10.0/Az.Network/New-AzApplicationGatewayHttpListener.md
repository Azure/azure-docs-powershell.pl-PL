---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 104a5e022d89421ac960d699c7391db660c0dd6b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890565"
---
# <span data-ttu-id="a1908-101">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a1908-101">New-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="a1908-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a1908-102">SYNOPSIS</span></span>
<span data-ttu-id="a1908-103">Tworzy odbiornik HTTP dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a1908-103">Creates an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="a1908-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a1908-104">SYNTAX</span></span>

### <span data-ttu-id="a1908-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a1908-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-HostName <String>]
 [-RequireServerNameIndication <String>] -Protocol <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a1908-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="a1908-106">SetByResource</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1908-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a1908-107">DESCRIPTION</span></span>
<span data-ttu-id="a1908-108">Polecenie cmdlet **New-AzApplicationGatewayHttpListener** umożliwia utworzenie odbiornika HTTP dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a1908-108">The **New-AzApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="a1908-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a1908-109">EXAMPLES</span></span>

### <span data-ttu-id="a1908-110">Przykład 1: Tworzenie odbiornika HTTP</span><span class="sxs-lookup"><span data-stu-id="a1908-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="a1908-111">To polecenie tworzy odbiornik HTTP o nazwie Listener01 i zapisuje wynik w zmiennej o nazwie $Listener.</span><span class="sxs-lookup"><span data-stu-id="a1908-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="a1908-112">Przykład 2: Tworzenie odbiornika HTTP przy użyciu protokołu SSL</span><span class="sxs-lookup"><span data-stu-id="a1908-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="a1908-113">To polecenie tworzy odbiornik HTTP używający odciążania SSL i dostarcza certyfikat SSL w zmiennej $SSLCert 01.</span><span class="sxs-lookup"><span data-stu-id="a1908-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="a1908-114">Polecenie zapisuje wynik w zmiennej o nazwie $Listener.</span><span class="sxs-lookup"><span data-stu-id="a1908-114">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="a1908-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a1908-115">PARAMETERS</span></span>

### <span data-ttu-id="a1908-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1908-116">-DefaultProfile</span></span>
<span data-ttu-id="a1908-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a1908-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1908-118">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a1908-118">-FrontendIPConfiguration</span></span>
<span data-ttu-id="a1908-119">Określa obiekt konfiguracji IP frontonu dla odbiornika HTTP.</span><span class="sxs-lookup"><span data-stu-id="a1908-119">Specifies front-end IP configuration object for the HTTP listener.</span></span>

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

### <span data-ttu-id="a1908-120">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="a1908-120">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="a1908-121">Określa identyfikator zewnętrznej konfiguracji IP dla odbiornika HTTP.</span><span class="sxs-lookup"><span data-stu-id="a1908-121">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="a1908-122">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="a1908-122">-FrontendPort</span></span>
<span data-ttu-id="a1908-123">Określa port frontonu dla odbiornika HTTP.</span><span class="sxs-lookup"><span data-stu-id="a1908-123">Specifies the front-end port for the HTTP listener.</span></span>

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

### <span data-ttu-id="a1908-124">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="a1908-124">-FrontendPortId</span></span>
<span data-ttu-id="a1908-125">Określa identyfikator obiektu typu front-end dla odbiornika HTTP.</span><span class="sxs-lookup"><span data-stu-id="a1908-125">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="a1908-126">-HostName</span><span class="sxs-lookup"><span data-stu-id="a1908-126">-HostName</span></span>
<span data-ttu-id="a1908-127">Określa nazwę hosta odbiornika HTTP bramy Application.</span><span class="sxs-lookup"><span data-stu-id="a1908-127">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="a1908-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a1908-128">-Name</span></span>
<span data-ttu-id="a1908-129">Określa nazwę odbiornika HTTP, który tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1908-129">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="a1908-130">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="a1908-130">-Protocol</span></span>
<span data-ttu-id="a1908-131">Określa protokół używany przez odbiornik HTTP.</span><span class="sxs-lookup"><span data-stu-id="a1908-131">Specifies the protocol that the HTTP listener uses.</span></span>

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

### <span data-ttu-id="a1908-132">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="a1908-132">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="a1908-133">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="a1908-133">-SslCertificate</span></span>
<span data-ttu-id="a1908-134">Określa obiekt certyfikatu SSL dla odbiornika HTTP.</span><span class="sxs-lookup"><span data-stu-id="a1908-134">Specifies the SSL certificate object for  the HTTP listener.</span></span>

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

### <span data-ttu-id="a1908-135">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="a1908-135">-SslCertificateId</span></span>
<span data-ttu-id="a1908-136">Określa identyfikator certyfikatu SSL dla odbiornika HTTP.</span><span class="sxs-lookup"><span data-stu-id="a1908-136">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="a1908-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1908-137">CommonParameters</span></span>
<span data-ttu-id="a1908-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1908-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1908-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1908-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1908-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1908-140">INPUTS</span></span>

### <span data-ttu-id="a1908-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a1908-141">System.String</span></span>

## <span data-ttu-id="a1908-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a1908-142">OUTPUTS</span></span>

### <span data-ttu-id="a1908-143">Microsoft. Azure. Commands. Network. models. PSHttpListener</span><span class="sxs-lookup"><span data-stu-id="a1908-143">Microsoft.Azure.Commands.Network.Models.PSHttpListener</span></span>

## <span data-ttu-id="a1908-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a1908-144">NOTES</span></span>

## <span data-ttu-id="a1908-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a1908-145">RELATED LINKS</span></span>

[<span data-ttu-id="a1908-146">Dodaj-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a1908-146">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="a1908-147">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a1908-147">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="a1908-148">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a1908-148">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="a1908-149">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a1908-149">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


