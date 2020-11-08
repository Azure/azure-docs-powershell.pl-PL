---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 3f53bd59e85fa9dac03a99d7e192ce51325ca6a4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234095"
---
# <span data-ttu-id="5fb11-101">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="5fb11-101">Set-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="5fb11-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5fb11-102">SYNOPSIS</span></span>
<span data-ttu-id="5fb11-103">Aktualizuje błąd niestandardowy w odbiorniku http bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="5fb11-103">Updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="5fb11-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5fb11-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5fb11-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5fb11-105">DESCRIPTION</span></span>
<span data-ttu-id="5fb11-106">Polecenie cmdlet **Set-AzApplicationGatewayCustomError** aktualizuje błąd niestandardowy w odbiorniku http bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="5fb11-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="5fb11-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5fb11-107">EXAMPLES</span></span>

### <span data-ttu-id="5fb11-108">Przykład 1: aktualizowanie błędu niestandardowego od odbiornika http</span><span class="sxs-lookup"><span data-stu-id="5fb11-108">Example 1: Updates a custom error from a http listener</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Set-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="5fb11-109">To polecenie aktualizuje błąd niestandardowy kodu stanu HTTP 502 w odbiorniku http $listener 01 i zwraca zaktualizowany detektor.</span><span class="sxs-lookup"><span data-stu-id="5fb11-109">This command updates the custom error of http status code 502 in the http listener $listener01, and returns the updated listener.</span></span>

## <span data-ttu-id="5fb11-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5fb11-110">PARAMETERS</span></span>

### <span data-ttu-id="5fb11-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="5fb11-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="5fb11-112">Adres URL strony błędu z błędem klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5fb11-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="5fb11-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fb11-113">-DefaultProfile</span></span>
<span data-ttu-id="5fb11-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5fb11-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fb11-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="5fb11-115">-HttpListener</span></span>
<span data-ttu-id="5fb11-116">Odbiornik http bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="5fb11-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="5fb11-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="5fb11-117">-StatusCode</span></span>
<span data-ttu-id="5fb11-118">Kod stanu błędu klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5fb11-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="5fb11-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fb11-119">CommonParameters</span></span>
<span data-ttu-id="5fb11-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fb11-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fb11-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fb11-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fb11-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5fb11-122">INPUTS</span></span>

### <span data-ttu-id="5fb11-123">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5fb11-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="5fb11-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5fb11-124">OUTPUTS</span></span>

### <span data-ttu-id="5fb11-125">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="5fb11-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="5fb11-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5fb11-126">NOTES</span></span>

## <span data-ttu-id="5fb11-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5fb11-127">RELATED LINKS</span></span>

[<span data-ttu-id="5fb11-128">Dodaj-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="5fb11-128">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="5fb11-129">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="5fb11-129">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="5fb11-130">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="5fb11-130">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)
