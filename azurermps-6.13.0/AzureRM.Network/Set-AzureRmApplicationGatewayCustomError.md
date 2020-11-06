---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayCustomError.md
ms.openlocfilehash: 94a4b4dc41aa1ae7c2a7bb2596018382296f5f87
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545011"
---
# <span data-ttu-id="4ad8c-101">Set-AzureRmApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="4ad8c-101">Set-AzureRmApplicationGatewayCustomError</span></span>

## <span data-ttu-id="4ad8c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4ad8c-102">SYNOPSIS</span></span>
<span data-ttu-id="4ad8c-103">Aktualizuje błąd niestandardowy w bramie Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="4ad8c-103">Updates a custom error in an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ad8c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4ad8c-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ad8c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4ad8c-105">DESCRIPTION</span></span>
<span data-ttu-id="4ad8c-106">Polecenie cmdlet **Set-AzureRmApplicationGatewayCustomError** aktualizuje błąd niestandardowy w bramie Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="4ad8c-106">The **Set-AzureRmApplicationGatewayCustomError** cmdlet updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="4ad8c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4ad8c-107">EXAMPLES</span></span>

### <span data-ttu-id="4ad8c-108">Przykład 1: błąd niestandardowy aktualizacji w bramie Application Gateway</span><span class="sxs-lookup"><span data-stu-id="4ad8c-108">Example 1: Updates custom error in an application gateway</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Set-AzureRmApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="4ad8c-109">To polecenie powoduje zaktualizowanie niestandardowego błędu kodu stanu HTTP 502 w bramie Application Gateway $appgw i zwrócenie zaktualizowanej bramy.</span><span class="sxs-lookup"><span data-stu-id="4ad8c-109">This command updates the custom error of http status code 502 in the application gateway $appgw, and returns the updated gateway.</span></span>

## <span data-ttu-id="4ad8c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4ad8c-110">PARAMETERS</span></span>

### <span data-ttu-id="4ad8c-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4ad8c-111">-ApplicationGateway</span></span>
<span data-ttu-id="4ad8c-112">Brama Application Gateway</span><span class="sxs-lookup"><span data-stu-id="4ad8c-112">The Application Gateway</span></span>

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

### <span data-ttu-id="4ad8c-113">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="4ad8c-113">-CustomErrorPageUrl</span></span>
<span data-ttu-id="4ad8c-114">Adres URL strony błędu z błędem klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4ad8c-114">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="4ad8c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ad8c-115">-DefaultProfile</span></span>
<span data-ttu-id="4ad8c-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4ad8c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ad8c-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="4ad8c-117">-StatusCode</span></span>
<span data-ttu-id="4ad8c-118">Kod stanu błędu klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4ad8c-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="4ad8c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ad8c-119">CommonParameters</span></span>
<span data-ttu-id="4ad8c-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ad8c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ad8c-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ad8c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ad8c-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4ad8c-122">INPUTS</span></span>

### <span data-ttu-id="4ad8c-123">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4ad8c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4ad8c-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4ad8c-124">OUTPUTS</span></span>

### <span data-ttu-id="4ad8c-125">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4ad8c-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4ad8c-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4ad8c-126">NOTES</span></span>

## <span data-ttu-id="4ad8c-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4ad8c-127">RELATED LINKS</span></span>
