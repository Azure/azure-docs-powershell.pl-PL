---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 3f53bd59e85fa9dac03a99d7e192ce51325ca6a4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179386"
---
# <span data-ttu-id="8574e-101">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="8574e-101">Set-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="8574e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8574e-102">SYNOPSIS</span></span>
<span data-ttu-id="8574e-103">Aktualizuje błąd niestandardowy w słuchaczu http bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8574e-103">Updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="8574e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8574e-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8574e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8574e-105">DESCRIPTION</span></span>
<span data-ttu-id="8574e-106">Polecenie **cmdlet Set-AzApplicationGatewayCustomError** aktualizuje błąd niestandardowy w słuchaczu http bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8574e-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="8574e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8574e-107">EXAMPLES</span></span>

### <span data-ttu-id="8574e-108">Przykład 1. Aktualizacja błędu niestandardowego od słuchacza http</span><span class="sxs-lookup"><span data-stu-id="8574e-108">Example 1: Updates a custom error from a http listener</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Set-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="8574e-109">To polecenie aktualizuje niestandardowy błąd kodu stanu http 502 w interfejsie $listener 01 http i zwraca zaktualizowanego słuchacza.</span><span class="sxs-lookup"><span data-stu-id="8574e-109">This command updates the custom error of http status code 502 in the http listener $listener01, and returns the updated listener.</span></span>

## <span data-ttu-id="8574e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8574e-110">PARAMETERS</span></span>

### <span data-ttu-id="8574e-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="8574e-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="8574e-112">Adres URL strony błędu klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8574e-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="8574e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8574e-113">-DefaultProfile</span></span>
<span data-ttu-id="8574e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8574e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8574e-115">- HttpListener</span><span class="sxs-lookup"><span data-stu-id="8574e-115">-HttpListener</span></span>
<span data-ttu-id="8574e-116">Słuchacz http bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="8574e-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="8574e-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="8574e-117">-StatusCode</span></span>
<span data-ttu-id="8574e-118">Kod stanu błędu klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8574e-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="8574e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8574e-119">CommonParameters</span></span>
<span data-ttu-id="8574e-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8574e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8574e-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8574e-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8574e-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8574e-122">INPUTS</span></span>

### <span data-ttu-id="8574e-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="8574e-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="8574e-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8574e-124">OUTPUTS</span></span>

### <span data-ttu-id="8574e-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="8574e-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="8574e-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8574e-126">NOTES</span></span>

## <span data-ttu-id="8574e-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8574e-127">RELATED LINKS</span></span>

[<span data-ttu-id="8574e-128">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="8574e-128">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="8574e-129">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="8574e-129">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="8574e-130">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="8574e-130">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)
