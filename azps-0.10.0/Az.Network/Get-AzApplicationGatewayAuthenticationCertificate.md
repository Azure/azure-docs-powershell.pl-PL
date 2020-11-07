---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 465567242c0ff13ea695c767cf1dda7f04f54174
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890917"
---
# <span data-ttu-id="c367b-101">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c367b-101">Get-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="c367b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c367b-102">SYNOPSIS</span></span>
<span data-ttu-id="c367b-103">Pobiera certyfikat uwierzytelniania dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c367b-103">Gets an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="c367b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c367b-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAuthenticationCertificate [-Name <String>]
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c367b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c367b-105">DESCRIPTION</span></span>
<span data-ttu-id="c367b-106">Polecenie cmdlet **Get-AzApplicationGatewayAuthenticationCertificate** pobiera certyfikat uwierzytelniania dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c367b-106">The **Get-AzApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="c367b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c367b-107">EXAMPLES</span></span>

### <span data-ttu-id="c367b-108">1:1</span><span class="sxs-lookup"><span data-stu-id="c367b-108">1:</span></span>
```

```

## <span data-ttu-id="c367b-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c367b-109">PARAMETERS</span></span>

### <span data-ttu-id="c367b-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c367b-110">-ApplicationGateway</span></span>
<span data-ttu-id="c367b-111">Określa nazwę bramy aplikacji, dla której to polecenie cmdlet pobiera certyfikat uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="c367b-111">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

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

### <span data-ttu-id="c367b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c367b-112">-DefaultProfile</span></span>
<span data-ttu-id="c367b-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c367b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c367b-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c367b-114">-Name</span></span>
<span data-ttu-id="c367b-115">Określa nazwę certyfikatu uwierzytelniania, który ma być pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c367b-115">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c367b-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c367b-116">CommonParameters</span></span>
<span data-ttu-id="c367b-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c367b-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c367b-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c367b-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c367b-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c367b-119">INPUTS</span></span>

### <span data-ttu-id="c367b-120">System. String</span><span class="sxs-lookup"><span data-stu-id="c367b-120">System.String</span></span>

## <span data-ttu-id="c367b-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c367b-121">OUTPUTS</span></span>

### <span data-ttu-id="c367b-122">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c367b-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="c367b-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c367b-123">NOTES</span></span>
* <span data-ttu-id="c367b-124">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="c367b-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="c367b-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c367b-125">RELATED LINKS</span></span>

[<span data-ttu-id="c367b-126">Dodaj-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c367b-126">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="c367b-127">Nowe — AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c367b-127">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="c367b-128">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c367b-128">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="c367b-129">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c367b-129">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


