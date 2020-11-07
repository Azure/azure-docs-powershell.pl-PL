---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 58cef33d6e7c05167376fe81a7c3b1e3f464f407
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709612"
---
# <span data-ttu-id="1063d-101">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="1063d-101">Get-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="1063d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1063d-102">SYNOPSIS</span></span>
<span data-ttu-id="1063d-103">Pobiera błędy niestandardowe od odbiornika http bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="1063d-103">Gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="1063d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1063d-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayHttpListenerCustomError [-StatusCode <String>]
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1063d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1063d-105">DESCRIPTION</span></span>
<span data-ttu-id="1063d-106">Polecenie cmdlet **Get-AzApplicationGatewayCustomError** pobiera błędy niestandardowe z odbiornika http bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="1063d-106">The **Get-AzApplicationGatewayCustomError** cmdlet gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="1063d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1063d-107">EXAMPLES</span></span>

### <span data-ttu-id="1063d-108">Przykład 1. w przypadku odbiornika HTTP jest pobierany błąd niestandardowy</span><span class="sxs-lookup"><span data-stu-id="1063d-108">Example 1: Gets a custom error in a http listener</span></span>
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="1063d-109">To polecenie pobiera i zwraca błąd niestandardowy kodu stanu HTTP 502 z odbiornika http $listener 01.</span><span class="sxs-lookup"><span data-stu-id="1063d-109">This command gets and returns the custom error of http status code 502 from the http listener $listener01.</span></span>

### <span data-ttu-id="1063d-110">Przykład 2: Pobiera listę wszystkich błędów niestandardowych w odbiorniku http</span><span class="sxs-lookup"><span data-stu-id="1063d-110">Example 2: Gets the list of all custom errors in a http listener</span></span>
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -HttpListener $listener01
```

<span data-ttu-id="1063d-111">To polecenie pobiera i zwraca listę wszystkich błędów niestandardowych z odbiornika http $listener 01.</span><span class="sxs-lookup"><span data-stu-id="1063d-111">This command gets and returns the list of all custom errors from the http listener $listener01.</span></span>

## <span data-ttu-id="1063d-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1063d-112">PARAMETERS</span></span>

### <span data-ttu-id="1063d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1063d-113">-DefaultProfile</span></span>
<span data-ttu-id="1063d-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1063d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1063d-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="1063d-115">-HttpListener</span></span>
<span data-ttu-id="1063d-116">Odbiornik http bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="1063d-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="1063d-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="1063d-117">-StatusCode</span></span>
<span data-ttu-id="1063d-118">Kod stanu błędu klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1063d-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="1063d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1063d-119">CommonParameters</span></span>
<span data-ttu-id="1063d-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1063d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1063d-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1063d-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1063d-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1063d-122">INPUTS</span></span>

### <span data-ttu-id="1063d-123">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1063d-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="1063d-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1063d-124">OUTPUTS</span></span>

### <span data-ttu-id="1063d-125">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="1063d-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="1063d-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1063d-126">NOTES</span></span>

## <span data-ttu-id="1063d-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1063d-127">RELATED LINKS</span></span>

[<span data-ttu-id="1063d-128">Dodaj-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="1063d-128">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="1063d-129">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="1063d-129">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="1063d-130">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="1063d-130">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)