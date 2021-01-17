---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: a9b0d41ad700d0591e38fa339c38efb85cb00859
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369341"
---
# <span data-ttu-id="3f9bc-101">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="3f9bc-101">New-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="3f9bc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3f9bc-102">SYNOPSIS</span></span>
<span data-ttu-id="3f9bc-103">Tworzy profil SSL dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3f9bc-103">Creates SSL profile for an application gateway.</span></span>

## <span data-ttu-id="3f9bc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3f9bc-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslProfile -Name <String> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 [-ClientAuthConfiguration <PSApplicationGatewayClientAuthConfiguration>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f9bc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3f9bc-105">DESCRIPTION</span></span>
<span data-ttu-id="3f9bc-106">Polecenie cmdlet **New-AzApplicationGatewaySslProfile** tworzy profil SSL dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3f9bc-106">The **New-AzApplicationGatewaySslProfile** cmdlet creates SSL profile for an application gateway.</span></span> <span data-ttu-id="3f9bc-107">Profil SSL jest konfigurowany na odbiornikach HTTPS.</span><span class="sxs-lookup"><span data-stu-id="3f9bc-107">The ssl profile is configured on the HTTPS listeners.</span></span>

## <span data-ttu-id="3f9bc-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3f9bc-108">EXAMPLES</span></span>

### <span data-ttu-id="3f9bc-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3f9bc-109">Example 1</span></span>
```powershell
PS C:\> $sslPolicy = New-AzApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
PS C:\> $trustedClient01 = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert01" -CertificateFile "C:\clientCAChain1.cer"
PS C:\> $profile = New-AzApplicationGatewaySslProfile -Name $sslProfile01Name -SslPolicy $sslPolicy -TrustedClientCertificates $trustedClient01
```
<span data-ttu-id="3f9bc-110">Pierwsze polecenie tworzy nowe zasady SSL i zapisuje je w zmiennej $sslPolicy.</span><span class="sxs-lookup"><span data-stu-id="3f9bc-110">The first command creates a new SSL policy and stores it in the $sslPolicy variable.</span></span>
<span data-ttu-id="3f9bc-111">Drugie polecenie tworzy łańcuchy certyfikatów zaufanego urzędu certyfikacji klienta i zapisuje je w zmiennej $ClientCert 01.</span><span class="sxs-lookup"><span data-stu-id="3f9bc-111">The second command creates a trusted client CA certificate chains and stores them in the $ClientCert01 variable.</span></span>
<span data-ttu-id="3f9bc-112">Trzecie polecenie Utwórz nowy profil SSL z łańcuchem certyfikatów zasada SSL i zaufany certyfikat CA klienta.</span><span class="sxs-lookup"><span data-stu-id="3f9bc-112">The third command create a new SSL profile with the the ssl policy and trusted client CA certificate chain.</span></span>

## <span data-ttu-id="3f9bc-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3f9bc-113">PARAMETERS</span></span>

### <span data-ttu-id="3f9bc-114">-ClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="3f9bc-114">-ClientAuthConfiguration</span></span>
<span data-ttu-id="3f9bc-115">Ustawienia konfiguracji uwierzytelniania klienta</span><span class="sxs-lookup"><span data-stu-id="3f9bc-115">Client authentication configuration settings</span></span>

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

### <span data-ttu-id="3f9bc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f9bc-116">-DefaultProfile</span></span>
<span data-ttu-id="3f9bc-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3f9bc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f9bc-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3f9bc-118">-Name</span></span>
<span data-ttu-id="3f9bc-119">Nazwa profilu SSL</span><span class="sxs-lookup"><span data-stu-id="3f9bc-119">The name of the SSL profile</span></span>

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

### <span data-ttu-id="3f9bc-120">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="3f9bc-120">-SslPolicy</span></span>
<span data-ttu-id="3f9bc-121">Zasady SSL</span><span class="sxs-lookup"><span data-stu-id="3f9bc-121">SSL policy</span></span>

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

### <span data-ttu-id="3f9bc-122">-TrustedClientCertificates</span><span class="sxs-lookup"><span data-stu-id="3f9bc-122">-TrustedClientCertificates</span></span>
<span data-ttu-id="3f9bc-123">Łańcuch certyfikatu zaufanego urzędu certyfikacji klienta</span><span class="sxs-lookup"><span data-stu-id="3f9bc-123">The trusted client CA certificate chains</span></span>

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

### <span data-ttu-id="3f9bc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f9bc-124">CommonParameters</span></span>
<span data-ttu-id="3f9bc-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f9bc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f9bc-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f9bc-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f9bc-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3f9bc-127">INPUTS</span></span>

### <span data-ttu-id="3f9bc-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3f9bc-128">None</span></span>

## <span data-ttu-id="3f9bc-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3f9bc-129">OUTPUTS</span></span>

### <span data-ttu-id="3f9bc-130">Microsoft. Azure. Commands. Network. models. PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="3f9bc-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="3f9bc-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3f9bc-131">NOTES</span></span>

## <span data-ttu-id="3f9bc-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3f9bc-132">RELATED LINKS</span></span>

[<span data-ttu-id="3f9bc-133">Dodaj-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="3f9bc-133">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="3f9bc-134">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="3f9bc-134">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="3f9bc-135">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="3f9bc-135">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="3f9bc-136">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="3f9bc-136">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)