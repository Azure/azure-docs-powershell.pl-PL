---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayCustomError.md
ms.openlocfilehash: e3bac58fca1c405aeef3366cb3ec1ee1b01a0891
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220578"
---
# <span data-ttu-id="7e0fa-101">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="7e0fa-101">Add-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="7e0fa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7e0fa-102">SYNOPSIS</span></span>
<span data-ttu-id="7e0fa-103">Umożliwia dodanie niestandardowego błędu do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7e0fa-103">Adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="7e0fa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7e0fa-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e0fa-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7e0fa-105">DESCRIPTION</span></span>
<span data-ttu-id="7e0fa-106">Polecenie cmdlet **Add-AzApplicationGatewayCustomError** powoduje dodanie niestandardowego błędu do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7e0fa-106">The **Add-AzApplicationGatewayCustomError** cmdlet adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="7e0fa-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7e0fa-107">EXAMPLES</span></span>

### <span data-ttu-id="7e0fa-108">Przykład 1: dodanie błędu niestandardowego do poziomu bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="7e0fa-108">Example 1: Adds custom error to application gateway level</span></span>
```powershell
PS C:\> $resourceGroupName = "resourceGroupName"
PS C:\> $AppGWName = "applicationGatewayName"
PS C:\> $AppGw = Get-AzApplicationGateway -Name $AppGWName -ResourceGroup $resourceGroupName
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Add-AzApplicationGatewayCustomError -ApplicationGateway $AppGw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
PS C:\> Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="7e0fa-109">To polecenie umożliwia dodanie niestandardowego błędu kodu stanu HTTP 502 do bramy Application $appgw i zwrócenie zaktualizowanej bramy.</span><span class="sxs-lookup"><span data-stu-id="7e0fa-109">This command adds a custom error of http status code 502 to the application gateway $appgw, and return the updated gateway.</span></span>

### <span data-ttu-id="7e0fa-110">Przykład 2: dodanie błędu niestandardowego do poziomu odbiornika bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="7e0fa-110">Example 2: Adds custom error to application gateway listener level</span></span>
```powershell
 $resourceGroupName = "resourceGroupName"
 $AppGWName = "applicationGatewayName"
 $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
 $listenerName = "listenerName"
 $AppGw = Get-AzApplicationGateway -Name $AppGWName -ResourceGroupName $resourceGroupName
 $listener = Get-AzApplicationGatewayHttpListener -ApplicationGateway $AppGW -Name $listenerName
 $updatedListener = Add-AzApplicationGatewayHttpListenerCustomError -HttpListener $listener -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url 
 Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="7e0fa-111">To polecenie umożliwia dodanie niestandardowego błędu kodu stanu HTTP 502 do bramy Application $appgw na poziomie odbiornika i zwrócenie zaktualizowanej bramy.</span><span class="sxs-lookup"><span data-stu-id="7e0fa-111">This command adds a custom error of http status code 502 to the application gateway $appgw at the listener level, and return the updated gateway.</span></span>

## <span data-ttu-id="7e0fa-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7e0fa-112">PARAMETERS</span></span>

### <span data-ttu-id="7e0fa-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7e0fa-113">-ApplicationGateway</span></span>
<span data-ttu-id="7e0fa-114">Brama Application Gateway</span><span class="sxs-lookup"><span data-stu-id="7e0fa-114">The Application Gateway</span></span>

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

### <span data-ttu-id="7e0fa-115">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="7e0fa-115">-CustomErrorPageUrl</span></span>
<span data-ttu-id="7e0fa-116">Adres URL strony błędu z błędem klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7e0fa-116">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="7e0fa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e0fa-117">-DefaultProfile</span></span>
<span data-ttu-id="7e0fa-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7e0fa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e0fa-119">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="7e0fa-119">-StatusCode</span></span>
<span data-ttu-id="7e0fa-120">Kod stanu błędu klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7e0fa-120">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="7e0fa-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e0fa-121">CommonParameters</span></span>
<span data-ttu-id="7e0fa-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e0fa-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e0fa-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e0fa-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e0fa-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7e0fa-124">INPUTS</span></span>

### <span data-ttu-id="7e0fa-125">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7e0fa-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7e0fa-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7e0fa-126">OUTPUTS</span></span>

### <span data-ttu-id="7e0fa-127">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="7e0fa-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="7e0fa-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7e0fa-128">NOTES</span></span>

## <span data-ttu-id="7e0fa-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7e0fa-129">RELATED LINKS</span></span>

[<span data-ttu-id="7e0fa-130">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="7e0fa-130">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="7e0fa-131">Nowe — AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="7e0fa-131">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="7e0fa-132">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="7e0fa-132">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="7e0fa-133">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="7e0fa-133">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
