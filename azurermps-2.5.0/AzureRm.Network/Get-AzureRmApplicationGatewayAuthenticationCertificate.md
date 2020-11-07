---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
ms.openlocfilehash: 033ca62f766f854be27ad75a6b63a8f883ba58d0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899297"
---
# <span data-ttu-id="c38d7-101">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c38d7-101">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="c38d7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c38d7-102">SYNOPSIS</span></span>
<span data-ttu-id="c38d7-103">Pobiera certyfikat uwierzytelniania dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c38d7-103">Gets an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c38d7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c38d7-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAuthenticationCertificate [-Name <String>]
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c38d7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c38d7-105">DESCRIPTION</span></span>
<span data-ttu-id="c38d7-106">Polecenie cmdlet **Get-AzureRmApplicationGatewayAuthenticationCertificate** pobiera certyfikat uwierzytelniania dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c38d7-106">The **Get-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="c38d7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c38d7-107">EXAMPLES</span></span>

### <span data-ttu-id="c38d7-108">1:1</span><span class="sxs-lookup"><span data-stu-id="c38d7-108">1:</span></span>
```

```

## <span data-ttu-id="c38d7-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c38d7-109">PARAMETERS</span></span>

### <span data-ttu-id="c38d7-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c38d7-110">-ApplicationGateway</span></span>
<span data-ttu-id="c38d7-111">Określa nazwę bramy aplikacji, dla której to polecenie cmdlet pobiera certyfikat uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="c38d7-111">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

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

### <span data-ttu-id="c38d7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c38d7-112">-DefaultProfile</span></span>
<span data-ttu-id="c38d7-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c38d7-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c38d7-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c38d7-114">-Name</span></span>
<span data-ttu-id="c38d7-115">Określa nazwę certyfikatu uwierzytelniania, który ma być pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c38d7-115">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c38d7-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c38d7-116">CommonParameters</span></span>
<span data-ttu-id="c38d7-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c38d7-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c38d7-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c38d7-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c38d7-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c38d7-119">INPUTS</span></span>

### <span data-ttu-id="c38d7-120">System. String</span><span class="sxs-lookup"><span data-stu-id="c38d7-120">System.String</span></span>

## <span data-ttu-id="c38d7-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c38d7-121">OUTPUTS</span></span>

### <span data-ttu-id="c38d7-122">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c38d7-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="c38d7-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c38d7-123">NOTES</span></span>
* <span data-ttu-id="c38d7-124">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="c38d7-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="c38d7-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c38d7-125">RELATED LINKS</span></span>

[<span data-ttu-id="c38d7-126">Dodaj-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c38d7-126">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="c38d7-127">Nowe — AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c38d7-127">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="c38d7-128">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c38d7-128">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="c38d7-129">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c38d7-129">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


