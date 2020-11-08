---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 34f92bfa7566679c4cee9f7a4281ac15c55676b4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234471"
---
# <span data-ttu-id="260fd-101">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="260fd-101">Get-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="260fd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="260fd-102">SYNOPSIS</span></span>
<span data-ttu-id="260fd-103">Pobiera błędy niestandardowe od odbiornika http bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="260fd-103">Gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="260fd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="260fd-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayHttpListenerCustomError [-StatusCode <String>]
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="260fd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="260fd-105">DESCRIPTION</span></span>
<span data-ttu-id="260fd-106">Polecenie cmdlet **Get-AzApplicationGatewayCustomError** pobiera błędy niestandardowe z odbiornika http bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="260fd-106">The **Get-AzApplicationGatewayCustomError** cmdlet gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="260fd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="260fd-107">EXAMPLES</span></span>

### <span data-ttu-id="260fd-108">Przykład 1. w przypadku odbiornika HTTP jest pobierany błąd niestandardowy</span><span class="sxs-lookup"><span data-stu-id="260fd-108">Example 1: Gets a custom error in a http listener</span></span>
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="260fd-109">To polecenie pobiera i zwraca błąd niestandardowy kodu stanu HTTP 502 z odbiornika http $listener 01.</span><span class="sxs-lookup"><span data-stu-id="260fd-109">This command gets and returns the custom error of http status code 502 from the http listener $listener01.</span></span>

### <span data-ttu-id="260fd-110">Przykład 2: Pobiera listę wszystkich błędów niestandardowych w odbiorniku http</span><span class="sxs-lookup"><span data-stu-id="260fd-110">Example 2: Gets the list of all custom errors in a http listener</span></span>
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -HttpListener $listener01
```

<span data-ttu-id="260fd-111">To polecenie pobiera i zwraca listę wszystkich błędów niestandardowych z odbiornika http $listener 01.</span><span class="sxs-lookup"><span data-stu-id="260fd-111">This command gets and returns the list of all custom errors from the http listener $listener01.</span></span>

## <span data-ttu-id="260fd-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="260fd-112">PARAMETERS</span></span>

### <span data-ttu-id="260fd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="260fd-113">-DefaultProfile</span></span>
<span data-ttu-id="260fd-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="260fd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="260fd-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="260fd-115">-HttpListener</span></span>
<span data-ttu-id="260fd-116">Odbiornik http bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="260fd-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="260fd-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="260fd-117">-StatusCode</span></span>
<span data-ttu-id="260fd-118">Kod stanu błędu klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="260fd-118">Status code of the application gateway customer error.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="260fd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="260fd-119">CommonParameters</span></span>
<span data-ttu-id="260fd-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="260fd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="260fd-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="260fd-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="260fd-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="260fd-122">INPUTS</span></span>

### <span data-ttu-id="260fd-123">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="260fd-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="260fd-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="260fd-124">OUTPUTS</span></span>

### <span data-ttu-id="260fd-125">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="260fd-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="260fd-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="260fd-126">NOTES</span></span>

## <span data-ttu-id="260fd-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="260fd-127">RELATED LINKS</span></span>

[<span data-ttu-id="260fd-128">Dodaj-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="260fd-128">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="260fd-129">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="260fd-129">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="260fd-130">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="260fd-130">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
