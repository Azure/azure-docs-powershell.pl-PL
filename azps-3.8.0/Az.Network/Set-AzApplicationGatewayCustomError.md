---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 08447949836af59223572bac1b8fec54f3704d9d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050374"
---
# <span data-ttu-id="f4e9b-101">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f4e9b-101">Set-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="f4e9b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f4e9b-102">SYNOPSIS</span></span>
<span data-ttu-id="f4e9b-103">Aktualizuje błąd niestandardowy w bramie Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f4e9b-103">Updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="f4e9b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f4e9b-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4e9b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f4e9b-105">DESCRIPTION</span></span>
<span data-ttu-id="f4e9b-106">Polecenie cmdlet **Set-AzApplicationGatewayCustomError** aktualizuje błąd niestandardowy w bramie Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f4e9b-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="f4e9b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f4e9b-107">EXAMPLES</span></span>

### <span data-ttu-id="f4e9b-108">Przykład 1: błąd niestandardowy aktualizacji w bramie Application Gateway</span><span class="sxs-lookup"><span data-stu-id="f4e9b-108">Example 1: Updates custom error in an application gateway</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Set-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="f4e9b-109">To polecenie powoduje zaktualizowanie niestandardowego błędu kodu stanu HTTP 502 w bramie Application Gateway $appgw i zwrócenie zaktualizowanej bramy.</span><span class="sxs-lookup"><span data-stu-id="f4e9b-109">This command updates the custom error of http status code 502 in the application gateway $appgw, and returns the updated gateway.</span></span>

## <span data-ttu-id="f4e9b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f4e9b-110">PARAMETERS</span></span>

### <span data-ttu-id="f4e9b-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f4e9b-111">-ApplicationGateway</span></span>
<span data-ttu-id="f4e9b-112">Brama Application Gateway</span><span class="sxs-lookup"><span data-stu-id="f4e9b-112">The Application Gateway</span></span>

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

### <span data-ttu-id="f4e9b-113">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="f4e9b-113">-CustomErrorPageUrl</span></span>
<span data-ttu-id="f4e9b-114">Adres URL strony błędu z błędem klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f4e9b-114">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="f4e9b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4e9b-115">-DefaultProfile</span></span>
<span data-ttu-id="f4e9b-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f4e9b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4e9b-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="f4e9b-117">-StatusCode</span></span>
<span data-ttu-id="f4e9b-118">Kod stanu błędu klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f4e9b-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="f4e9b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4e9b-119">CommonParameters</span></span>
<span data-ttu-id="f4e9b-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4e9b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4e9b-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4e9b-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4e9b-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f4e9b-122">INPUTS</span></span>

### <span data-ttu-id="f4e9b-123">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f4e9b-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f4e9b-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f4e9b-124">OUTPUTS</span></span>

### <span data-ttu-id="f4e9b-125">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f4e9b-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="f4e9b-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f4e9b-126">NOTES</span></span>

## <span data-ttu-id="f4e9b-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f4e9b-127">RELATED LINKS</span></span>

[<span data-ttu-id="f4e9b-128">Dodaj-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f4e9b-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="f4e9b-129">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f4e9b-129">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="f4e9b-130">Nowe — AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f4e9b-130">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="f4e9b-131">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f4e9b-131">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)
