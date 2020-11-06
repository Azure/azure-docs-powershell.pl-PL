---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayCustomError.md
ms.openlocfilehash: cc1f6b487d0faf58999a0326a77e01bea74d8c91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527841"
---
# <span data-ttu-id="4bf0d-101">Remove-AzureRmApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="4bf0d-101">Remove-AzureRmApplicationGatewayCustomError</span></span>

## <span data-ttu-id="4bf0d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4bf0d-102">SYNOPSIS</span></span>
<span data-ttu-id="4bf0d-103">Usuwa błąd niestandardowy z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4bf0d-103">Removes a custom error from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4bf0d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4bf0d-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayCustomError -StatusCode <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4bf0d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4bf0d-105">DESCRIPTION</span></span>
<span data-ttu-id="4bf0d-106">Polecenie cmdlet **Remove-AzureRmApplicationGatewayCustomError** usuwa błąd niestandardowy z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4bf0d-106">The **Remove-AzureRmApplicationGatewayCustomError** cmdlet removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="4bf0d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4bf0d-107">EXAMPLES</span></span>

### <span data-ttu-id="4bf0d-108">Przykład 1. usuwa błąd niestandardowy z bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="4bf0d-108">Example 1: Removes custom error from an application gateway</span></span>
```
PS C:\> $updatedgateway = Remove-AzureRmApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="4bf0d-109">To polecenie usuwa błąd niestandardowy kodu stanu HTTP 502 z bramy Application Gateway $appgw i zwraca zaktualizowaną bramę.</span><span class="sxs-lookup"><span data-stu-id="4bf0d-109">This command removes the custom error of http status code 502 from the application gateway $appgw, and return the updated gateway.</span></span>

## <span data-ttu-id="4bf0d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4bf0d-110">PARAMETERS</span></span>

### <span data-ttu-id="4bf0d-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4bf0d-111">-ApplicationGateway</span></span>
<span data-ttu-id="4bf0d-112">Brama Application Gateway</span><span class="sxs-lookup"><span data-stu-id="4bf0d-112">The Application Gateway</span></span>

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

### <span data-ttu-id="4bf0d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bf0d-113">-DefaultProfile</span></span>
<span data-ttu-id="4bf0d-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4bf0d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bf0d-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="4bf0d-115">-StatusCode</span></span>
<span data-ttu-id="4bf0d-116">Kod stanu błędu klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4bf0d-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="4bf0d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bf0d-117">CommonParameters</span></span>
<span data-ttu-id="4bf0d-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bf0d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bf0d-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bf0d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bf0d-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4bf0d-120">INPUTS</span></span>

### <span data-ttu-id="4bf0d-121">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4bf0d-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4bf0d-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4bf0d-122">OUTPUTS</span></span>

### <span data-ttu-id="4bf0d-123">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4bf0d-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4bf0d-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4bf0d-124">NOTES</span></span>

## <span data-ttu-id="4bf0d-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4bf0d-125">RELATED LINKS</span></span>
