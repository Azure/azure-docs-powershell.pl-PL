---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: 469b490b0f0c2bd37f7f58265108278322cbca60
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982481"
---
# <span data-ttu-id="d6ab8-101">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="d6ab8-101">Add-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="d6ab8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6ab8-102">SYNOPSIS</span></span>
<span data-ttu-id="d6ab8-103">Dodaje profil SSL do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d6ab8-103">Adds SSL profile to an application gateway.</span></span>

## <span data-ttu-id="d6ab8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d6ab8-104">SYNTAX</span></span>

```
Add-AzApplicationGatewaySslProfile -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SslPolicy <PSApplicationGatewaySslPolicy>]
 [-ClientAuthConfiguration <PSApplicationGatewayClientAuthConfiguration>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6ab8-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d6ab8-105">DESCRIPTION</span></span>
<span data-ttu-id="d6ab8-106">Polecenie **cmdlet Add-AzApplicationGatewaySslProfile** dodaje profil SSL do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d6ab8-106">The **Add-AzApplicationGatewaySslProfile** cmdlet adds a SSL profile to an application gateway.</span></span> <span data-ttu-id="d6ab8-107">Profil SSL jest stosowany do słuchaczy HTTPS.</span><span class="sxs-lookup"><span data-stu-id="d6ab8-107">The SSL profile is applied to HTTPS Listeners.</span></span>

## <span data-ttu-id="d6ab8-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d6ab8-108">EXAMPLES</span></span>

### <span data-ttu-id="d6ab8-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d6ab8-109">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslPolicy = New-AzApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
PS C:\> $trustedClient01 = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert01" -CertificateFile "C:\clientCAChain1.cer"
PS C:\> $trustedClient02 = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert02" -CertificateFile "C:\clientCAChain2.cer"
PS C:\> $AppGw = Add-AzApplicationGatewaySslProfile -Name $sslProfile01Name -ApplicationGateway $AppGw -SslPolicy $sslPolicy -TrustedClientCertificates $trustedClient01,$trustedClient02
```

<span data-ttu-id="d6ab8-110">Pierwsze polecenie pobiera bramę aplikacji i zapisuje je w $AppGw zmienną.</span><span class="sxs-lookup"><span data-stu-id="d6ab8-110">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d6ab8-111">Drugie polecenie tworzy nowe zasady SSL i zapisuje je w $sslPolicy danych.</span><span class="sxs-lookup"><span data-stu-id="d6ab8-111">The second command creates a new SSL policy and stores it in the $sslPolicy variable.</span></span>
<span data-ttu-id="d6ab8-112">Trzecie i czwarte polecenie tworzy dwa nowe łańcuchy certyfikatów zaufanego urzędu certyfikacji klienta i przechowuje je w $ClientCert 01 i $ClientCert 02 zmiennych.</span><span class="sxs-lookup"><span data-stu-id="d6ab8-112">The third and fourth command creates two new trusted client CA certificate chains and stores them in the $ClientCert01 and $ClientCert02 variables.</span></span>
<span data-ttu-id="d6ab8-113">Piąte polecenie dodaje profil SSL z zasadami ssl i łańcuchami certyfikatów zaufanego urzędu certyfikacji klienta do bramy aplikacji i $AppGw.</span><span class="sxs-lookup"><span data-stu-id="d6ab8-113">The fifth command adds the SSL profile with the the ssl policy and trusted client CA certificate chains to the application gateway $AppGw.</span></span>

## <span data-ttu-id="d6ab8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6ab8-114">PARAMETERS</span></span>

### <span data-ttu-id="d6ab8-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d6ab8-115">-ApplicationGateway</span></span>
<span data-ttu-id="d6ab8-116">The applicationGateway</span><span class="sxs-lookup"><span data-stu-id="d6ab8-116">The applicationGateway</span></span>

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

### <span data-ttu-id="d6ab8-117">-ClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6ab8-117">-ClientAuthConfiguration</span></span>
<span data-ttu-id="d6ab8-118">Ustawienia konfiguracji uwierzytelniania klienta</span><span class="sxs-lookup"><span data-stu-id="d6ab8-118">Client authentication configuration settings</span></span>

```yaml
Type: PSApplicationGatewayClientAuthConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6ab8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6ab8-119">-DefaultProfile</span></span>
<span data-ttu-id="d6ab8-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d6ab8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6ab8-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d6ab8-121">-Name</span></span>
<span data-ttu-id="d6ab8-122">Nazwa profilu SSL</span><span class="sxs-lookup"><span data-stu-id="d6ab8-122">The name of the SSL profile</span></span>

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

### <span data-ttu-id="d6ab8-123">- SslPolicy</span><span class="sxs-lookup"><span data-stu-id="d6ab8-123">-SslPolicy</span></span>
<span data-ttu-id="d6ab8-124">Zasady SSL</span><span class="sxs-lookup"><span data-stu-id="d6ab8-124">SSL policy</span></span>

```yaml
Type: PSApplicationGatewaySslPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6ab8-125">-TrustedClientCertificates</span><span class="sxs-lookup"><span data-stu-id="d6ab8-125">-TrustedClientCertificates</span></span>
<span data-ttu-id="d6ab8-126">Zaufane łańcuchy certyfikatów urzędu certyfikacji klienta</span><span class="sxs-lookup"><span data-stu-id="d6ab8-126">The trusted client CA certificate chains</span></span>

```yaml
Type: PSApplicationGatewayTrustedClientCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6ab8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6ab8-127">CommonParameters</span></span>
<span data-ttu-id="d6ab8-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6ab8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6ab8-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6ab8-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6ab8-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6ab8-130">INPUTS</span></span>

### <span data-ttu-id="d6ab8-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d6ab8-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d6ab8-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6ab8-132">OUTPUTS</span></span>

### <span data-ttu-id="d6ab8-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d6ab8-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d6ab8-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d6ab8-134">NOTES</span></span>

## <span data-ttu-id="d6ab8-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d6ab8-135">RELATED LINKS</span></span>

[<span data-ttu-id="d6ab8-136">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="d6ab8-136">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="d6ab8-137">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="d6ab8-137">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="d6ab8-138">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="d6ab8-138">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="d6ab8-139">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="d6ab8-139">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)