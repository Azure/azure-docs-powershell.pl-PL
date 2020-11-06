---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 317fd5bf8306416ad4cbef3d1fb64d56d556ed1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545635"
---
# <span data-ttu-id="baa7d-101">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="baa7d-101">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="baa7d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="baa7d-102">SYNOPSIS</span></span>
<span data-ttu-id="baa7d-103">Dodaje certyfikat uwierzytelniania do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="baa7d-103">Adds an authentication certificate to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="baa7d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="baa7d-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="baa7d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="baa7d-105">DESCRIPTION</span></span>
<span data-ttu-id="baa7d-106">Polecenie cmdlet **Add-AzureRmApplicationGatewayAuthenticationCertificate** dodaje certyfikat uwierzytelniania do bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="baa7d-106">The **Add-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="baa7d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="baa7d-107">EXAMPLES</span></span>

## <span data-ttu-id="baa7d-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="baa7d-108">PARAMETERS</span></span>

### <span data-ttu-id="baa7d-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="baa7d-109">-ApplicationGateway</span></span>
<span data-ttu-id="baa7d-110">Określa nazwę bramy aplikacji, dla której to polecenie cmdlet dodaje certyfikat uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="baa7d-110">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

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

### <span data-ttu-id="baa7d-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="baa7d-111">-CertificateFile</span></span>
<span data-ttu-id="baa7d-112">Określa ścieżkę certyfikatu uwierzytelniania, który jest dodawany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="baa7d-112">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="baa7d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baa7d-113">-DefaultProfile</span></span>
<span data-ttu-id="baa7d-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="baa7d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="baa7d-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="baa7d-115">-Name</span></span>
<span data-ttu-id="baa7d-116">Określa nazwę certyfikatu, który jest dodawany przez to polecenie cmdlet do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="baa7d-116">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

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

### <span data-ttu-id="baa7d-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="baa7d-117">-Confirm</span></span>
<span data-ttu-id="baa7d-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="baa7d-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baa7d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="baa7d-119">-WhatIf</span></span>
<span data-ttu-id="baa7d-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="baa7d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="baa7d-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="baa7d-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baa7d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baa7d-122">CommonParameters</span></span>
<span data-ttu-id="baa7d-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="baa7d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baa7d-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="baa7d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baa7d-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="baa7d-125">INPUTS</span></span>

### <span data-ttu-id="baa7d-126">System. String</span><span class="sxs-lookup"><span data-stu-id="baa7d-126">System.String</span></span>

## <span data-ttu-id="baa7d-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="baa7d-127">OUTPUTS</span></span>

### <span data-ttu-id="baa7d-128">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="baa7d-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="baa7d-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="baa7d-129">NOTES</span></span>
* <span data-ttu-id="baa7d-130">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="baa7d-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="baa7d-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="baa7d-131">RELATED LINKS</span></span>

[<span data-ttu-id="baa7d-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="baa7d-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="baa7d-133">Nowe — AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="baa7d-133">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="baa7d-134">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="baa7d-134">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="baa7d-135">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="baa7d-135">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


