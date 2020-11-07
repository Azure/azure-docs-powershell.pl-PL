---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 8a0ce9d3e2c2a5272f6544b5c98ef763b9b288ef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709178"
---
# <span data-ttu-id="4f9ca-101">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="4f9ca-101">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="4f9ca-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4f9ca-102">SYNOPSIS</span></span>
<span data-ttu-id="4f9ca-103">Usuwa błąd niestandardowy z odbiornika http bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="4f9ca-103">Removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="4f9ca-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4f9ca-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListenerCustomError -StatusCode <String>
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4f9ca-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4f9ca-105">DESCRIPTION</span></span>
<span data-ttu-id="4f9ca-106">Polecenie cmdlet **Remove-AzApplicationGatewayCustomError** usuwa błąd niestandardowy z odbiornika http bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="4f9ca-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="4f9ca-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4f9ca-107">EXAMPLES</span></span>

### <span data-ttu-id="4f9ca-108">Przykład 1. usuwa błąd niestandardowy z odbiornika http</span><span class="sxs-lookup"><span data-stu-id="4f9ca-108">Example 1: Removes custom error from a http listener</span></span>
```powershell
PS C:\> $updatedlistener = Remove-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="4f9ca-109">To polecenie powoduje usunięcie niestandardowego błędu kodu stanu HTTP 502 z odbiornika http $listener 01 i zwrócenie zaktualizowanego odbiornika.</span><span class="sxs-lookup"><span data-stu-id="4f9ca-109">This command removes the custom error of http status code 502 from the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="4f9ca-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4f9ca-110">PARAMETERS</span></span>

### <span data-ttu-id="4f9ca-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f9ca-111">-DefaultProfile</span></span>
<span data-ttu-id="4f9ca-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4f9ca-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f9ca-113">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="4f9ca-113">-HttpListener</span></span>
<span data-ttu-id="4f9ca-114">Odbiornik http bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="4f9ca-114">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="4f9ca-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="4f9ca-115">-StatusCode</span></span>
<span data-ttu-id="4f9ca-116">Kod stanu błędu klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4f9ca-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="4f9ca-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f9ca-117">CommonParameters</span></span>
<span data-ttu-id="4f9ca-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f9ca-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f9ca-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f9ca-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f9ca-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4f9ca-120">INPUTS</span></span>

### <span data-ttu-id="4f9ca-121">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4f9ca-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="4f9ca-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4f9ca-122">OUTPUTS</span></span>

### <span data-ttu-id="4f9ca-123">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="4f9ca-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="4f9ca-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4f9ca-124">NOTES</span></span>

## <span data-ttu-id="4f9ca-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4f9ca-125">RELATED LINKS</span></span>

[<span data-ttu-id="4f9ca-126">Dodaj-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="4f9ca-126">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="4f9ca-127">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="4f9ca-127">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="4f9ca-128">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="4f9ca-128">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
