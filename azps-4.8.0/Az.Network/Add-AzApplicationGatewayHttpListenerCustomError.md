---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: d810afe9f5fcf2a1377f55ffe0822d3e71ee409f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062192"
---
# <span data-ttu-id="e07ac-101">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="e07ac-101">Add-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="e07ac-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e07ac-102">SYNOPSIS</span></span>
<span data-ttu-id="e07ac-103">Dodaje niestandardowy błąd do odbiornika http bramy Application.</span><span class="sxs-lookup"><span data-stu-id="e07ac-103">Adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="e07ac-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e07ac-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e07ac-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e07ac-105">DESCRIPTION</span></span>
<span data-ttu-id="e07ac-106">Polecenie cmdlet **Add-AzApplicationGatewayCustomError** powoduje dodanie niestandardowego błędu do odbiornika http bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="e07ac-106">The **Add-AzApplicationGatewayCustomError** cmdlet adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="e07ac-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e07ac-107">EXAMPLES</span></span>

### <span data-ttu-id="e07ac-108">Przykład 1: dodanie błędu niestandardowego do poziomu odbiornika http</span><span class="sxs-lookup"><span data-stu-id="e07ac-108">Example 1: Adds custom error to http listener level</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Add-AzApplicationGatewayHttpListenerCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="e07ac-109">To polecenie umożliwia dodanie niestandardowego błędu kodu stanu HTTP 502 do odbiornika http $listener 01 i zwrócenie zaktualizowanego odbiornika.</span><span class="sxs-lookup"><span data-stu-id="e07ac-109">This command adds a custom error of http status code 502 to the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="e07ac-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e07ac-110">PARAMETERS</span></span>

### <span data-ttu-id="e07ac-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="e07ac-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="e07ac-112">Adres URL strony błędu z błędem klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e07ac-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="e07ac-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e07ac-113">-DefaultProfile</span></span>
<span data-ttu-id="e07ac-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e07ac-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e07ac-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="e07ac-115">-HttpListener</span></span>
<span data-ttu-id="e07ac-116">Odbiornik http bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="e07ac-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="e07ac-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="e07ac-117">-StatusCode</span></span>
<span data-ttu-id="e07ac-118">Kod stanu błędu klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e07ac-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="e07ac-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e07ac-119">CommonParameters</span></span>
<span data-ttu-id="e07ac-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e07ac-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e07ac-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e07ac-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e07ac-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e07ac-122">INPUTS</span></span>

### <span data-ttu-id="e07ac-123">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="e07ac-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="e07ac-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e07ac-124">OUTPUTS</span></span>

### <span data-ttu-id="e07ac-125">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e07ac-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="e07ac-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e07ac-126">NOTES</span></span>

## <span data-ttu-id="e07ac-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e07ac-127">RELATED LINKS</span></span>

[<span data-ttu-id="e07ac-128">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="e07ac-128">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="e07ac-129">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="e07ac-129">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="e07ac-130">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="e07ac-130">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
