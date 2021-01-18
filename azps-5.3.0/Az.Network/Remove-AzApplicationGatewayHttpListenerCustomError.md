---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 82675befb6a900bacdead036f323959e1e7a72a9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503230"
---
# <span data-ttu-id="dbb01-101">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="dbb01-101">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="dbb01-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dbb01-102">SYNOPSIS</span></span>
<span data-ttu-id="dbb01-103">Usuwa błąd niestandardowy z odbiornika http bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="dbb01-103">Removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="dbb01-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dbb01-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListenerCustomError -StatusCode <String>
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dbb01-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dbb01-105">DESCRIPTION</span></span>
<span data-ttu-id="dbb01-106">Polecenie cmdlet **Remove-AzApplicationGatewayCustomError** usuwa błąd niestandardowy z odbiornika http bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="dbb01-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="dbb01-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dbb01-107">EXAMPLES</span></span>

### <span data-ttu-id="dbb01-108">Przykład 1. usuwa błąd niestandardowy z odbiornika http</span><span class="sxs-lookup"><span data-stu-id="dbb01-108">Example 1: Removes custom error from a http listener</span></span>
```powershell
PS C:\> $updatedlistener = Remove-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="dbb01-109">To polecenie powoduje usunięcie niestandardowego błędu kodu stanu HTTP 502 z odbiornika http $listener 01 i zwrócenie zaktualizowanego odbiornika.</span><span class="sxs-lookup"><span data-stu-id="dbb01-109">This command removes the custom error of http status code 502 from the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="dbb01-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dbb01-110">PARAMETERS</span></span>

### <span data-ttu-id="dbb01-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbb01-111">-DefaultProfile</span></span>
<span data-ttu-id="dbb01-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dbb01-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbb01-113">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="dbb01-113">-HttpListener</span></span>
<span data-ttu-id="dbb01-114">Odbiornik http bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="dbb01-114">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="dbb01-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="dbb01-115">-StatusCode</span></span>
<span data-ttu-id="dbb01-116">Kod stanu błędu klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="dbb01-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="dbb01-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbb01-117">CommonParameters</span></span>
<span data-ttu-id="dbb01-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbb01-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbb01-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbb01-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbb01-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dbb01-120">INPUTS</span></span>

### <span data-ttu-id="dbb01-121">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="dbb01-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="dbb01-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dbb01-122">OUTPUTS</span></span>

### <span data-ttu-id="dbb01-123">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="dbb01-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="dbb01-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dbb01-124">NOTES</span></span>

## <span data-ttu-id="dbb01-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dbb01-125">RELATED LINKS</span></span>

[<span data-ttu-id="dbb01-126">Dodaj-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="dbb01-126">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="dbb01-127">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="dbb01-127">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="dbb01-128">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="dbb01-128">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
