---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 34f92bfa7566679c4cee9f7a4281ac15c55676b4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184778"
---
# <span data-ttu-id="96dc7-101">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="96dc7-101">Get-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="96dc7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96dc7-102">SYNOPSIS</span></span>
<span data-ttu-id="96dc7-103">Pobiera błędy niestandardowe od słuchacza http bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="96dc7-103">Gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="96dc7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="96dc7-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayHttpListenerCustomError [-StatusCode <String>]
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="96dc7-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="96dc7-105">DESCRIPTION</span></span>
<span data-ttu-id="96dc7-106">Polecenie **cmdlet Get-AzApplicationGatewayCustomError** pobiera błędy niestandardowe od słuchacza http bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="96dc7-106">The **Get-AzApplicationGatewayCustomError** cmdlet gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="96dc7-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="96dc7-107">EXAMPLES</span></span>

### <span data-ttu-id="96dc7-108">Przykład 1. Zwraca błąd niestandardowy w słuchaczu http</span><span class="sxs-lookup"><span data-stu-id="96dc7-108">Example 1: Gets a custom error in a http listener</span></span>
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="96dc7-109">To polecenie pobiera i zwraca niestandardowy błąd kodu stanu http 502 od odbiorcy http $listener 01.</span><span class="sxs-lookup"><span data-stu-id="96dc7-109">This command gets and returns the custom error of http status code 502 from the http listener $listener01.</span></span>

### <span data-ttu-id="96dc7-110">Przykład 2. Pobiera listę wszystkich błędów niestandardowych w słuchaczu http</span><span class="sxs-lookup"><span data-stu-id="96dc7-110">Example 2: Gets the list of all custom errors in a http listener</span></span>
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -HttpListener $listener01
```

<span data-ttu-id="96dc7-111">To polecenie pobiera i zwraca listę wszystkich błędów niestandardowych z grupy $listener 01 http.</span><span class="sxs-lookup"><span data-stu-id="96dc7-111">This command gets and returns the list of all custom errors from the http listener $listener01.</span></span>

## <span data-ttu-id="96dc7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="96dc7-112">PARAMETERS</span></span>

### <span data-ttu-id="96dc7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96dc7-113">-DefaultProfile</span></span>
<span data-ttu-id="96dc7-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="96dc7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96dc7-115">- HttpListener</span><span class="sxs-lookup"><span data-stu-id="96dc7-115">-HttpListener</span></span>
<span data-ttu-id="96dc7-116">Słuchacz http bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="96dc7-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="96dc7-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="96dc7-117">-StatusCode</span></span>
<span data-ttu-id="96dc7-118">Kod stanu błędu klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="96dc7-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="96dc7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96dc7-119">CommonParameters</span></span>
<span data-ttu-id="96dc7-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96dc7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96dc7-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="96dc7-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96dc7-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="96dc7-122">INPUTS</span></span>

### <span data-ttu-id="96dc7-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="96dc7-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="96dc7-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="96dc7-124">OUTPUTS</span></span>

### <span data-ttu-id="96dc7-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="96dc7-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="96dc7-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="96dc7-126">NOTES</span></span>

## <span data-ttu-id="96dc7-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="96dc7-127">RELATED LINKS</span></span>

[<span data-ttu-id="96dc7-128">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="96dc7-128">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="96dc7-129">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="96dc7-129">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="96dc7-130">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="96dc7-130">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
