---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 89e323bd8e8dedbaa3c7716a6c10119a6fb69365
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545111"
---
# <span data-ttu-id="0cd8b-101">Get-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="0cd8b-101">Get-AzureRmApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="0cd8b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0cd8b-102">SYNOPSIS</span></span>
<span data-ttu-id="0cd8b-103">Pobiera błędy niestandardowe od odbiornika http bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="0cd8b-103">Gets custom error(s) from a http listener of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0cd8b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0cd8b-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayHttpListenerCustomError [-StatusCode <String>]
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0cd8b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0cd8b-105">DESCRIPTION</span></span>
<span data-ttu-id="0cd8b-106">Polecenie cmdlet **Get-AzureRmApplicationGatewayCustomError** pobiera błędy niestandardowe z odbiornika http bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="0cd8b-106">The **Get-AzureRmApplicationGatewayCustomError** cmdlet gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="0cd8b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0cd8b-107">EXAMPLES</span></span>

### <span data-ttu-id="0cd8b-108">Przykład 1. w przypadku odbiornika HTTP jest pobierany błąd niestandardowy</span><span class="sxs-lookup"><span data-stu-id="0cd8b-108">Example 1: Gets a custom error in a http listener</span></span>
```powershell
PS C:\> $ce = Get-AzureRmApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="0cd8b-109">To polecenie pobiera i zwraca błąd niestandardowy kodu stanu HTTP 502 z odbiornika http $listener 01.</span><span class="sxs-lookup"><span data-stu-id="0cd8b-109">This command gets and returns the custom error of http status code 502 from the http listener $listener01.</span></span>

### <span data-ttu-id="0cd8b-110">Przykład 2: Pobiera listę wszystkich błędów niestandardowych w odbiorniku http</span><span class="sxs-lookup"><span data-stu-id="0cd8b-110">Example 2: Gets the list of all custom errors in a http listener</span></span>
```powershell
PS C:\> $ces = Get-AzureRmApplicationGatewayCustomError -HttpListener $listener01
```

<span data-ttu-id="0cd8b-111">To polecenie pobiera i zwraca listę wszystkich błędów niestandardowych z odbiornika http $listener 01.</span><span class="sxs-lookup"><span data-stu-id="0cd8b-111">This command gets and returns the list of all custom errors from the http listener $listener01.</span></span>

## <span data-ttu-id="0cd8b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0cd8b-112">PARAMETERS</span></span>

### <span data-ttu-id="0cd8b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cd8b-113">-DefaultProfile</span></span>
<span data-ttu-id="0cd8b-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0cd8b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cd8b-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="0cd8b-115">-HttpListener</span></span>
<span data-ttu-id="0cd8b-116">Odbiornik http bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="0cd8b-116">The Application Gateway Http Listener</span></span>

```yaml
Type: PSApplicationGatewayHttpListener
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0cd8b-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="0cd8b-117">-StatusCode</span></span>
<span data-ttu-id="0cd8b-118">Kod stanu błędu klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="0cd8b-118">Status code of the application gateway customer error.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cd8b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cd8b-119">CommonParameters</span></span>
<span data-ttu-id="0cd8b-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cd8b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="0cd8b-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cd8b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cd8b-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0cd8b-122">INPUTS</span></span>

### <span data-ttu-id="0cd8b-123">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="0cd8b-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="0cd8b-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0cd8b-124">OUTPUTS</span></span>

### <span data-ttu-id="0cd8b-125">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="0cd8b-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="0cd8b-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0cd8b-126">NOTES</span></span>

## <span data-ttu-id="0cd8b-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0cd8b-127">RELATED LINKS</span></span>
