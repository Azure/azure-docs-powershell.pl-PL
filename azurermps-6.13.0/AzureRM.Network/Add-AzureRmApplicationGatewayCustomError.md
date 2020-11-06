---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayCustomError.md
ms.openlocfilehash: b56c358a208683e513844e36e561efa9e76cbede
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527886"
---
# <span data-ttu-id="d1b1e-101">Add-AzureRmApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="d1b1e-101">Add-AzureRmApplicationGatewayCustomError</span></span>

## <span data-ttu-id="d1b1e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d1b1e-102">SYNOPSIS</span></span>
<span data-ttu-id="d1b1e-103">Umożliwia dodanie niestandardowego błędu do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d1b1e-103">Adds a custom error to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1b1e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d1b1e-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1b1e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d1b1e-105">DESCRIPTION</span></span>
<span data-ttu-id="d1b1e-106">Polecenie cmdlet **Add-AzureRmApplicationGatewayCustomError** powoduje dodanie niestandardowego błędu do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d1b1e-106">The **Add-AzureRmApplicationGatewayCustomError** cmdlet adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="d1b1e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d1b1e-107">EXAMPLES</span></span>

### <span data-ttu-id="d1b1e-108">Przykład 1: dodanie błędu niestandardowego do poziomu bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="d1b1e-108">Example 1: Adds custom error to application gateway level</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Add-AzureRmApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="d1b1e-109">To polecenie umożliwia dodanie niestandardowego błędu kodu stanu HTTP 502 do bramy Application $appgw i zwrócenie zaktualizowanej bramy.</span><span class="sxs-lookup"><span data-stu-id="d1b1e-109">This command adds a custom error of http status code 502 to the application gateway $appgw, and return the updated gateway.</span></span>

## <span data-ttu-id="d1b1e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d1b1e-110">PARAMETERS</span></span>

### <span data-ttu-id="d1b1e-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d1b1e-111">-ApplicationGateway</span></span>
<span data-ttu-id="d1b1e-112">Brama Application Gateway</span><span class="sxs-lookup"><span data-stu-id="d1b1e-112">The Application Gateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1b1e-113">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="d1b1e-113">-CustomErrorPageUrl</span></span>
<span data-ttu-id="d1b1e-114">Adres URL strony błędu z błędem klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d1b1e-114">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="d1b1e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1b1e-115">-DefaultProfile</span></span>
<span data-ttu-id="d1b1e-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d1b1e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1b1e-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="d1b1e-117">-StatusCode</span></span>
<span data-ttu-id="d1b1e-118">Kod stanu błędu klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d1b1e-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="d1b1e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1b1e-119">CommonParameters</span></span>
<span data-ttu-id="d1b1e-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1b1e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1b1e-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1b1e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1b1e-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d1b1e-122">INPUTS</span></span>

### <span data-ttu-id="d1b1e-123">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d1b1e-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d1b1e-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d1b1e-124">OUTPUTS</span></span>

### <span data-ttu-id="d1b1e-125">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d1b1e-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d1b1e-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d1b1e-126">NOTES</span></span>

## <span data-ttu-id="d1b1e-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d1b1e-127">RELATED LINKS</span></span>
