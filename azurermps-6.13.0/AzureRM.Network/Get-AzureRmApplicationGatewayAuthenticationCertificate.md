---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: fd2ddd3b8c3c124e85c743c6e331b18816c48be3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543776"
---
# <span data-ttu-id="ab0bc-101">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ab0bc-101">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="ab0bc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ab0bc-102">SYNOPSIS</span></span>
<span data-ttu-id="ab0bc-103">Pobiera certyfikat uwierzytelniania dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ab0bc-103">Gets an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab0bc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ab0bc-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAuthenticationCertificate [-Name <String>]
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab0bc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ab0bc-105">DESCRIPTION</span></span>
<span data-ttu-id="ab0bc-106">Polecenie cmdlet **Get-AzureRmApplicationGatewayAuthenticationCertificate** pobiera certyfikat uwierzytelniania dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ab0bc-106">The **Get-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="ab0bc-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ab0bc-107">EXAMPLES</span></span>

## <span data-ttu-id="ab0bc-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ab0bc-108">PARAMETERS</span></span>

### <span data-ttu-id="ab0bc-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ab0bc-109">-ApplicationGateway</span></span>
<span data-ttu-id="ab0bc-110">Określa nazwę bramy aplikacji, dla której to polecenie cmdlet pobiera certyfikat uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="ab0bc-110">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

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

### <span data-ttu-id="ab0bc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab0bc-111">-DefaultProfile</span></span>
<span data-ttu-id="ab0bc-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ab0bc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab0bc-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ab0bc-113">-Name</span></span>
<span data-ttu-id="ab0bc-114">Określa nazwę certyfikatu uwierzytelniania, który ma być pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab0bc-114">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ab0bc-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab0bc-115">CommonParameters</span></span>
<span data-ttu-id="ab0bc-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab0bc-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab0bc-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab0bc-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab0bc-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab0bc-118">INPUTS</span></span>

### <span data-ttu-id="ab0bc-119">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ab0bc-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="ab0bc-120">Parametry: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ab0bc-120">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="ab0bc-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ab0bc-121">OUTPUTS</span></span>

### <span data-ttu-id="ab0bc-122">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ab0bc-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="ab0bc-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ab0bc-123">NOTES</span></span>
* <span data-ttu-id="ab0bc-124">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="ab0bc-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="ab0bc-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ab0bc-125">RELATED LINKS</span></span>

[<span data-ttu-id="ab0bc-126">Dodaj-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ab0bc-126">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="ab0bc-127">Nowe — AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ab0bc-127">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="ab0bc-128">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ab0bc-128">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="ab0bc-129">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ab0bc-129">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


