---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: d0f26991498d8efc88eaacf9d01ed7e95d92e2cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527833"
---
# <span data-ttu-id="9d637-101">Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="9d637-101">Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="9d637-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9d637-102">SYNOPSIS</span></span>
<span data-ttu-id="9d637-103">Usuwa błąd niestandardowy z odbiornika http bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="9d637-103">Removes a custom error from a http listener of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d637-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9d637-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayHttpListenerCustomError -StatusCode <String>
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9d637-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9d637-105">DESCRIPTION</span></span>
<span data-ttu-id="9d637-106">Polecenie cmdlet **Remove-AzureRmApplicationGatewayCustomError** usuwa błąd niestandardowy z odbiornika http bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="9d637-106">The **Remove-AzureRmApplicationGatewayCustomError** cmdlet removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="9d637-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9d637-107">EXAMPLES</span></span>

### <span data-ttu-id="9d637-108">Przykład 1. usuwa błąd niestandardowy z odbiornika http</span><span class="sxs-lookup"><span data-stu-id="9d637-108">Example 1: Removes custom error from a http listener</span></span>
```powershell
PS C:\> $updatedlistener = Remove-AzureRmApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="9d637-109">To polecenie powoduje usunięcie niestandardowego błędu kodu stanu HTTP 502 z odbiornika http $listener 01 i zwrócenie zaktualizowanego odbiornika.</span><span class="sxs-lookup"><span data-stu-id="9d637-109">This command removes the custom error of http status code 502 from the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="9d637-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9d637-110">PARAMETERS</span></span>

### <span data-ttu-id="9d637-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d637-111">-DefaultProfile</span></span>
<span data-ttu-id="9d637-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9d637-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d637-113">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="9d637-113">-HttpListener</span></span>
<span data-ttu-id="9d637-114">Odbiornik http bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="9d637-114">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="9d637-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="9d637-115">-StatusCode</span></span>
<span data-ttu-id="9d637-116">Kod stanu błędu klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9d637-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="9d637-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d637-117">CommonParameters</span></span>
<span data-ttu-id="9d637-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d637-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="9d637-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d637-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d637-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d637-120">INPUTS</span></span>

### <span data-ttu-id="9d637-121">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="9d637-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="9d637-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9d637-122">OUTPUTS</span></span>

### <span data-ttu-id="9d637-123">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="9d637-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="9d637-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9d637-124">NOTES</span></span>

## <span data-ttu-id="9d637-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9d637-125">RELATED LINKS</span></span>
