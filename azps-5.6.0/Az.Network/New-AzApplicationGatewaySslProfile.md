---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: 4e58ee2c2f9b7854234913f0cf6ce7c6923f3345
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970506"
---
# <span data-ttu-id="0ffb6-101">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="0ffb6-101">New-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="0ffb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ffb6-102">SYNOPSIS</span></span>
<span data-ttu-id="0ffb6-103">Tworzy profil SSL dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="0ffb6-103">Creates SSL profile for an application gateway.</span></span>

## <span data-ttu-id="0ffb6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0ffb6-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslProfile -Name <String> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 [-ClientAuthConfiguration <PSApplicationGatewayClientAuthConfiguration>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ffb6-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="0ffb6-105">DESCRIPTION</span></span>
<span data-ttu-id="0ffb6-106">Polecenie **cmdlet New-AzApplicationGatewaySslProfile** tworzy profil SSL dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="0ffb6-106">The **New-AzApplicationGatewaySslProfile** cmdlet creates SSL profile for an application gateway.</span></span> <span data-ttu-id="0ffb6-107">Profil SSL jest skonfigurowany dla słuchaczy HTTPS.</span><span class="sxs-lookup"><span data-stu-id="0ffb6-107">The ssl profile is configured on the HTTPS listeners.</span></span>

## <span data-ttu-id="0ffb6-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0ffb6-108">EXAMPLES</span></span>

### <span data-ttu-id="0ffb6-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0ffb6-109">Example 1</span></span>
```powershell
PS C:\> $sslPolicy = New-AzApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
PS C:\> $trustedClient01 = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert01" -CertificateFile "C:\clientCAChain1.cer"
PS C:\> $profile = New-AzApplicationGatewaySslProfile -Name $sslProfile01Name -SslPolicy $sslPolicy -TrustedClientCertificates $trustedClient01
```
<span data-ttu-id="0ffb6-110">Pierwsze polecenie tworzy nowe zasady SSL i zapisuje je w $sslPolicy danych.</span><span class="sxs-lookup"><span data-stu-id="0ffb6-110">The first command creates a new SSL policy and stores it in the $sslPolicy variable.</span></span>
<span data-ttu-id="0ffb6-111">Drugie polecenie tworzy łańcuchy certyfikatów zaufanego urzędu certyfikacji klienta i przechowuje je w $ClientCert 01.</span><span class="sxs-lookup"><span data-stu-id="0ffb6-111">The second command creates a trusted client CA certificate chains and stores them in the $ClientCert01 variable.</span></span>
<span data-ttu-id="0ffb6-112">Trzecie polecenie tworzy nowy profil SSL z zasadami ssl i łańcuchem certyfikatów zaufanego urzędu certyfikacji klienta.</span><span class="sxs-lookup"><span data-stu-id="0ffb6-112">The third command create a new SSL profile with the the ssl policy and trusted client CA certificate chain.</span></span>

## <span data-ttu-id="0ffb6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ffb6-113">PARAMETERS</span></span>

### <span data-ttu-id="0ffb6-114">-ClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="0ffb6-114">-ClientAuthConfiguration</span></span>
<span data-ttu-id="0ffb6-115">Ustawienia konfiguracji uwierzytelniania klienta</span><span class="sxs-lookup"><span data-stu-id="0ffb6-115">Client authentication configuration settings</span></span>

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

### <span data-ttu-id="0ffb6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ffb6-116">-DefaultProfile</span></span>
<span data-ttu-id="0ffb6-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0ffb6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ffb6-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0ffb6-118">-Name</span></span>
<span data-ttu-id="0ffb6-119">Nazwa profilu SSL</span><span class="sxs-lookup"><span data-stu-id="0ffb6-119">The name of the SSL profile</span></span>

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

### <span data-ttu-id="0ffb6-120">- SslPolicy</span><span class="sxs-lookup"><span data-stu-id="0ffb6-120">-SslPolicy</span></span>
<span data-ttu-id="0ffb6-121">Zasady SSL</span><span class="sxs-lookup"><span data-stu-id="0ffb6-121">SSL policy</span></span>

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

### <span data-ttu-id="0ffb6-122">-TrustedClientCertificates</span><span class="sxs-lookup"><span data-stu-id="0ffb6-122">-TrustedClientCertificates</span></span>
<span data-ttu-id="0ffb6-123">Zaufane łańcuchy certyfikatów urzędu certyfikacji klienta</span><span class="sxs-lookup"><span data-stu-id="0ffb6-123">The trusted client CA certificate chains</span></span>

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

### <span data-ttu-id="0ffb6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ffb6-124">CommonParameters</span></span>
<span data-ttu-id="0ffb6-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ffb6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ffb6-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ffb6-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ffb6-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0ffb6-127">INPUTS</span></span>

### <span data-ttu-id="0ffb6-128">Brak</span><span class="sxs-lookup"><span data-stu-id="0ffb6-128">None</span></span>

## <span data-ttu-id="0ffb6-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0ffb6-129">OUTPUTS</span></span>

### <span data-ttu-id="0ffb6-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="0ffb6-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="0ffb6-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0ffb6-131">NOTES</span></span>

## <span data-ttu-id="0ffb6-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0ffb6-132">RELATED LINKS</span></span>

[<span data-ttu-id="0ffb6-133">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="0ffb6-133">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="0ffb6-134">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="0ffb6-134">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="0ffb6-135">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="0ffb6-135">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="0ffb6-136">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="0ffb6-136">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)