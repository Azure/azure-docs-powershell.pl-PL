---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 8718d79abef18217a727916d36c09e19de2a2de4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709708"
---
# <span data-ttu-id="f2bfe-101">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="f2bfe-101">Add-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="f2bfe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f2bfe-102">SYNOPSIS</span></span>
<span data-ttu-id="f2bfe-103">Dodaje niestandardowy błąd do odbiornika http bramy Application.</span><span class="sxs-lookup"><span data-stu-id="f2bfe-103">Adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="f2bfe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f2bfe-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f2bfe-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f2bfe-105">DESCRIPTION</span></span>
<span data-ttu-id="f2bfe-106">Polecenie cmdlet **Add-AzApplicationGatewayCustomError** powoduje dodanie niestandardowego błędu do odbiornika http bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f2bfe-106">The **Add-AzApplicationGatewayCustomError** cmdlet adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="f2bfe-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f2bfe-107">EXAMPLES</span></span>

### <span data-ttu-id="f2bfe-108">Przykład 1: dodanie błędu niestandardowego do poziomu odbiornika http</span><span class="sxs-lookup"><span data-stu-id="f2bfe-108">Example 1: Adds custom error to http listener level</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Add-AzApplicationGatewayHttpListenerCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="f2bfe-109">To polecenie umożliwia dodanie niestandardowego błędu kodu stanu HTTP 502 do odbiornika http $listener 01 i zwrócenie zaktualizowanego odbiornika.</span><span class="sxs-lookup"><span data-stu-id="f2bfe-109">This command adds a custom error of http status code 502 to the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="f2bfe-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f2bfe-110">PARAMETERS</span></span>

### <span data-ttu-id="f2bfe-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="f2bfe-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="f2bfe-112">Adres URL strony błędu z błędem klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f2bfe-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="f2bfe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2bfe-113">-DefaultProfile</span></span>
<span data-ttu-id="f2bfe-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f2bfe-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2bfe-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="f2bfe-115">-HttpListener</span></span>
<span data-ttu-id="f2bfe-116">Odbiornik http bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="f2bfe-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="f2bfe-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="f2bfe-117">-StatusCode</span></span>
<span data-ttu-id="f2bfe-118">Kod stanu błędu klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f2bfe-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="f2bfe-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2bfe-119">CommonParameters</span></span>
<span data-ttu-id="f2bfe-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2bfe-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2bfe-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2bfe-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2bfe-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2bfe-122">INPUTS</span></span>

### <span data-ttu-id="f2bfe-123">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f2bfe-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="f2bfe-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f2bfe-124">OUTPUTS</span></span>

### <span data-ttu-id="f2bfe-125">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f2bfe-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="f2bfe-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f2bfe-126">NOTES</span></span>

## <span data-ttu-id="f2bfe-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f2bfe-127">RELATED LINKS</span></span>

[<span data-ttu-id="f2bfe-128">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="f2bfe-128">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="f2bfe-129">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="f2bfe-129">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="f2bfe-130">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="f2bfe-130">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)