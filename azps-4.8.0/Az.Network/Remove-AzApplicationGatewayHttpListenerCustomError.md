---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 82675befb6a900bacdead036f323959e1e7a72a9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063922"
---
# <span data-ttu-id="9ff7f-101">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="9ff7f-101">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="9ff7f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9ff7f-102">SYNOPSIS</span></span>
<span data-ttu-id="9ff7f-103">Usuwa błąd niestandardowy z odbiornika http bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="9ff7f-103">Removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="9ff7f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9ff7f-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListenerCustomError -StatusCode <String>
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9ff7f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9ff7f-105">DESCRIPTION</span></span>
<span data-ttu-id="9ff7f-106">Polecenie cmdlet **Remove-AzApplicationGatewayCustomError** usuwa błąd niestandardowy z odbiornika http bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="9ff7f-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="9ff7f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9ff7f-107">EXAMPLES</span></span>

### <span data-ttu-id="9ff7f-108">Przykład 1. usuwa błąd niestandardowy z odbiornika http</span><span class="sxs-lookup"><span data-stu-id="9ff7f-108">Example 1: Removes custom error from a http listener</span></span>
```powershell
PS C:\> $updatedlistener = Remove-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="9ff7f-109">To polecenie powoduje usunięcie niestandardowego błędu kodu stanu HTTP 502 z odbiornika http $listener 01 i zwrócenie zaktualizowanego odbiornika.</span><span class="sxs-lookup"><span data-stu-id="9ff7f-109">This command removes the custom error of http status code 502 from the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="9ff7f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9ff7f-110">PARAMETERS</span></span>

### <span data-ttu-id="9ff7f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ff7f-111">-DefaultProfile</span></span>
<span data-ttu-id="9ff7f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9ff7f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ff7f-113">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="9ff7f-113">-HttpListener</span></span>
<span data-ttu-id="9ff7f-114">Odbiornik http bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="9ff7f-114">The Application Gateway Http Listener</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ff7f-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="9ff7f-115">-StatusCode</span></span>
<span data-ttu-id="9ff7f-116">Kod stanu błędu klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9ff7f-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="9ff7f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ff7f-117">CommonParameters</span></span>
<span data-ttu-id="9ff7f-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ff7f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ff7f-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ff7f-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ff7f-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9ff7f-120">INPUTS</span></span>

### <span data-ttu-id="9ff7f-121">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="9ff7f-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="9ff7f-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9ff7f-122">OUTPUTS</span></span>

### <span data-ttu-id="9ff7f-123">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9ff7f-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="9ff7f-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9ff7f-124">NOTES</span></span>

## <span data-ttu-id="9ff7f-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9ff7f-125">RELATED LINKS</span></span>

[<span data-ttu-id="9ff7f-126">Dodaj-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="9ff7f-126">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="9ff7f-127">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="9ff7f-127">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="9ff7f-128">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="9ff7f-128">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
