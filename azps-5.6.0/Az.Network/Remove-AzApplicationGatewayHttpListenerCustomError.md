---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: fabe88c2b7606bac3d5a90011913a2beae513f09
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985748"
---
# <span data-ttu-id="9056b-101">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="9056b-101">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="9056b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9056b-102">SYNOPSIS</span></span>
<span data-ttu-id="9056b-103">Usuwa błąd niestandardowy z słuchacza http bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9056b-103">Removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="9056b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9056b-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListenerCustomError -StatusCode <String>
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9056b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9056b-105">DESCRIPTION</span></span>
<span data-ttu-id="9056b-106">Polecenie **cmdlet Remove-AzApplicationGatewayCustomError** usuwa błąd niestandardowy z słuchacza http bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9056b-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="9056b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9056b-107">EXAMPLES</span></span>

### <span data-ttu-id="9056b-108">Przykład 1. Usuwanie błędu niestandardowego z słuchacza http</span><span class="sxs-lookup"><span data-stu-id="9056b-108">Example 1: Removes custom error from a http listener</span></span>
```powershell
PS C:\> $updatedlistener = Remove-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="9056b-109">To polecenie usuwa błąd niestandardowy kodu stanu http 502 z grupy $listener 01 http i zwraca zaktualizowanego słuchacza.</span><span class="sxs-lookup"><span data-stu-id="9056b-109">This command removes the custom error of http status code 502 from the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="9056b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9056b-110">PARAMETERS</span></span>

### <span data-ttu-id="9056b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9056b-111">-DefaultProfile</span></span>
<span data-ttu-id="9056b-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9056b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9056b-113">- HttpListener</span><span class="sxs-lookup"><span data-stu-id="9056b-113">-HttpListener</span></span>
<span data-ttu-id="9056b-114">Słuchacz http bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="9056b-114">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="9056b-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="9056b-115">-StatusCode</span></span>
<span data-ttu-id="9056b-116">Kod stanu błędu klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9056b-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="9056b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9056b-117">CommonParameters</span></span>
<span data-ttu-id="9056b-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9056b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9056b-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9056b-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9056b-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9056b-120">INPUTS</span></span>

### <span data-ttu-id="9056b-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="9056b-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="9056b-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9056b-122">OUTPUTS</span></span>

### <span data-ttu-id="9056b-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9056b-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="9056b-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9056b-124">NOTES</span></span>

## <span data-ttu-id="9056b-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9056b-125">RELATED LINKS</span></span>

[<span data-ttu-id="9056b-126">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="9056b-126">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="9056b-127">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="9056b-127">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="9056b-128">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="9056b-128">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
