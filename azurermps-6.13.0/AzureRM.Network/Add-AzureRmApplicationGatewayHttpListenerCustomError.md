---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 23cb65073f25f65a4e09f3b4a28891cff4e49c59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718825"
---
# <span data-ttu-id="6ab42-101">Add-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="6ab42-101">Add-AzureRmApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="6ab42-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6ab42-102">SYNOPSIS</span></span>
<span data-ttu-id="6ab42-103">Dodaje niestandardowy błąd do odbiornika http bramy Application.</span><span class="sxs-lookup"><span data-stu-id="6ab42-103">Adds a custom error to a http listener of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ab42-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6ab42-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6ab42-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6ab42-105">DESCRIPTION</span></span>
<span data-ttu-id="6ab42-106">Polecenie cmdlet **Add-AzureRmApplicationGatewayCustomError** powoduje dodanie niestandardowego błędu do odbiornika http bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="6ab42-106">The **Add-AzureRmApplicationGatewayCustomError** cmdlet adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="6ab42-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6ab42-107">EXAMPLES</span></span>

### <span data-ttu-id="6ab42-108">Przykład 1: dodanie błędu niestandardowego do poziomu odbiornika http</span><span class="sxs-lookup"><span data-stu-id="6ab42-108">Example 1: Adds custom error to http listener level</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Add-AzureRmApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="6ab42-109">To polecenie umożliwia dodanie niestandardowego błędu kodu stanu HTTP 502 do odbiornika http $listener 01 i zwrócenie zaktualizowanego odbiornika.</span><span class="sxs-lookup"><span data-stu-id="6ab42-109">This command adds a custom error of http status code 502 to the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="6ab42-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6ab42-110">PARAMETERS</span></span>

### <span data-ttu-id="6ab42-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="6ab42-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="6ab42-112">Adres URL strony błędu z błędem klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6ab42-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="6ab42-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ab42-113">-DefaultProfile</span></span>
<span data-ttu-id="6ab42-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6ab42-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ab42-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="6ab42-115">-HttpListener</span></span>
<span data-ttu-id="6ab42-116">Odbiornik http bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="6ab42-116">The Application Gateway Http Listener</span></span>

```yaml
Type: PSApplicationGatewayHttpListener
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ab42-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="6ab42-117">-StatusCode</span></span>
<span data-ttu-id="6ab42-118">Kod stanu błędu klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6ab42-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="6ab42-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ab42-119">CommonParameters</span></span>
<span data-ttu-id="6ab42-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ab42-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6ab42-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ab42-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ab42-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ab42-122">INPUTS</span></span>

### <span data-ttu-id="6ab42-123">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="6ab42-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="6ab42-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6ab42-124">OUTPUTS</span></span>

### <span data-ttu-id="6ab42-125">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="6ab42-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="6ab42-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6ab42-126">NOTES</span></span>

## <span data-ttu-id="6ab42-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6ab42-127">RELATED LINKS</span></span>
