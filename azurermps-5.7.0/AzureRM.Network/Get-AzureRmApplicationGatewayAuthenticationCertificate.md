---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: bec9d197d039ea3934607ee291bdd6511ae6f4a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548935"
---
# <span data-ttu-id="ee3ec-101">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ee3ec-101">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="ee3ec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ee3ec-102">SYNOPSIS</span></span>
<span data-ttu-id="ee3ec-103">Pobiera certyfikat uwierzytelniania dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ee3ec-103">Gets an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee3ec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ee3ec-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAuthenticationCertificate [-Name <String>]
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee3ec-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ee3ec-105">DESCRIPTION</span></span>
<span data-ttu-id="ee3ec-106">Polecenie cmdlet **Get-AzureRmApplicationGatewayAuthenticationCertificate** pobiera certyfikat uwierzytelniania dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ee3ec-106">The **Get-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="ee3ec-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ee3ec-107">EXAMPLES</span></span>

## <span data-ttu-id="ee3ec-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ee3ec-108">PARAMETERS</span></span>

### <span data-ttu-id="ee3ec-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ee3ec-109">-ApplicationGateway</span></span>
<span data-ttu-id="ee3ec-110">Określa nazwę bramy aplikacji, dla której to polecenie cmdlet pobiera certyfikat uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="ee3ec-110">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

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

### <span data-ttu-id="ee3ec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee3ec-111">-DefaultProfile</span></span>
<span data-ttu-id="ee3ec-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ee3ec-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee3ec-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ee3ec-113">-Name</span></span>
<span data-ttu-id="ee3ec-114">Określa nazwę certyfikatu uwierzytelniania, który ma być pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee3ec-114">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ee3ec-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee3ec-115">CommonParameters</span></span>
<span data-ttu-id="ee3ec-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee3ec-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee3ec-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee3ec-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee3ec-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ee3ec-118">INPUTS</span></span>

### <span data-ttu-id="ee3ec-119">System. String</span><span class="sxs-lookup"><span data-stu-id="ee3ec-119">System.String</span></span>

## <span data-ttu-id="ee3ec-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ee3ec-120">OUTPUTS</span></span>

### <span data-ttu-id="ee3ec-121">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ee3ec-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="ee3ec-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ee3ec-122">NOTES</span></span>
* <span data-ttu-id="ee3ec-123">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="ee3ec-123">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="ee3ec-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ee3ec-124">RELATED LINKS</span></span>

[<span data-ttu-id="ee3ec-125">Dodaj-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ee3ec-125">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="ee3ec-126">Nowe — AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ee3ec-126">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="ee3ec-127">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ee3ec-127">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="ee3ec-128">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ee3ec-128">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


