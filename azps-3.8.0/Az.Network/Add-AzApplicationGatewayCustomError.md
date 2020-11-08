---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 424dd1c13dbc6d860bec05da84704caba96735af
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050826"
---
# <span data-ttu-id="485a3-101">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="485a3-101">Add-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="485a3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="485a3-102">SYNOPSIS</span></span>
<span data-ttu-id="485a3-103">Umożliwia dodanie niestandardowego błędu do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="485a3-103">Adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="485a3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="485a3-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="485a3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="485a3-105">DESCRIPTION</span></span>
<span data-ttu-id="485a3-106">Polecenie cmdlet **Add-AzApplicationGatewayCustomError** powoduje dodanie niestandardowego błędu do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="485a3-106">The **Add-AzApplicationGatewayCustomError** cmdlet adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="485a3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="485a3-107">EXAMPLES</span></span>

### <span data-ttu-id="485a3-108">Przykład 1: dodanie błędu niestandardowego do poziomu bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="485a3-108">Example 1: Adds custom error to application gateway level</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Add-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="485a3-109">To polecenie umożliwia dodanie niestandardowego błędu kodu stanu HTTP 502 do bramy Application $appgw i zwrócenie zaktualizowanej bramy.</span><span class="sxs-lookup"><span data-stu-id="485a3-109">This command adds a custom error of http status code 502 to the application gateway $appgw, and return the updated gateway.</span></span>

### <span data-ttu-id="485a3-110">Przykład 2: dodanie błędu niestandardowego do poziomu odbiornika bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="485a3-110">Example 2: Adds custom error to application gateway listener level</span></span>
```powershell
PS C:\> $resourceGroup = "resourceGroupName"
PS C:\> $AppGWName = "applicationGatewayName"
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $listenerName = "listenerName"
PS C:\> $AppGw = Get-AzApplicationGateway -Name $AppGWName -ResourceGroupName $rg
PS C:\> $listener = Get-AzApplicationGatewayHttpListener -ApplicationGateway $AppGW -Name $listenerName
PS C:\> $updatedListener = Add-AzApplicationGatewayHttpListenerCustomError -HttpListener $listener -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url 
PS C:\> Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="485a3-111">To polecenie umożliwia dodanie niestandardowego błędu kodu stanu HTTP 502 do bramy Application $appgw na poziomie odbiornika i zwrócenie zaktualizowanej bramy.</span><span class="sxs-lookup"><span data-stu-id="485a3-111">This command adds a custom error of http status code 502 to the application gateway $appgw at the listener level, and return the updated gateway.</span></span>

## <span data-ttu-id="485a3-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="485a3-112">PARAMETERS</span></span>

### <span data-ttu-id="485a3-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="485a3-113">-ApplicationGateway</span></span>
<span data-ttu-id="485a3-114">Brama Application Gateway</span><span class="sxs-lookup"><span data-stu-id="485a3-114">The Application Gateway</span></span>

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

### <span data-ttu-id="485a3-115">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="485a3-115">-CustomErrorPageUrl</span></span>
<span data-ttu-id="485a3-116">Adres URL strony błędu z błędem klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="485a3-116">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="485a3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="485a3-117">-DefaultProfile</span></span>
<span data-ttu-id="485a3-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="485a3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="485a3-119">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="485a3-119">-StatusCode</span></span>
<span data-ttu-id="485a3-120">Kod stanu błędu klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="485a3-120">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="485a3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="485a3-121">CommonParameters</span></span>
<span data-ttu-id="485a3-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="485a3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="485a3-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="485a3-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="485a3-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="485a3-124">INPUTS</span></span>

### <span data-ttu-id="485a3-125">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="485a3-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="485a3-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="485a3-126">OUTPUTS</span></span>

### <span data-ttu-id="485a3-127">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="485a3-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="485a3-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="485a3-128">NOTES</span></span>

## <span data-ttu-id="485a3-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="485a3-129">RELATED LINKS</span></span>

[<span data-ttu-id="485a3-130">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="485a3-130">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="485a3-131">Nowe — AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="485a3-131">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="485a3-132">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="485a3-132">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="485a3-133">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="485a3-133">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
