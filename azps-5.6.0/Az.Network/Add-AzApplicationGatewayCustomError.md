---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayCustomError.md
ms.openlocfilehash: f5c36cc9e6133fbde4e7bae34b4bc6b479afb96e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967994"
---
# <span data-ttu-id="c5096-101">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="c5096-101">Add-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="c5096-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5096-102">SYNOPSIS</span></span>
<span data-ttu-id="c5096-103">Dodaje błąd niestandardowy do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c5096-103">Adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="c5096-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c5096-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5096-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c5096-105">DESCRIPTION</span></span>
<span data-ttu-id="c5096-106">Polecenie **cmdlet Add-AzApplicationGatewayCustomError** powoduje dodanie błędu niestandardowego do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c5096-106">The **Add-AzApplicationGatewayCustomError** cmdlet adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="c5096-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c5096-107">EXAMPLES</span></span>

### <span data-ttu-id="c5096-108">Przykład 1. Dodanie błędu niestandardowego do poziomu bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="c5096-108">Example 1: Adds custom error to application gateway level</span></span>
```powershell
PS C:\> $resourceGroupName = "resourceGroupName"
PS C:\> $AppGWName = "applicationGatewayName"
PS C:\> $AppGw = Get-AzApplicationGateway -Name $AppGWName -ResourceGroup $resourceGroupName
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Add-AzApplicationGatewayCustomError -ApplicationGateway $AppGw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
PS C:\> Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="c5096-109">To polecenie powoduje dodanie niestandardowego błędu o kodzie stanu http 502 do $appgw aplikacji i zwrócenie zaktualizowanej bramy.</span><span class="sxs-lookup"><span data-stu-id="c5096-109">This command adds a custom error of http status code 502 to the application gateway $appgw, and return the updated gateway.</span></span>

### <span data-ttu-id="c5096-110">Przykład 2. Dodaje błąd niestandardowy do poziomu słuchacza bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="c5096-110">Example 2: Adds custom error to application gateway listener level</span></span>
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

<span data-ttu-id="c5096-111">To polecenie dodaje niestandardowy błąd o kodzie stanu http 502 do bramy aplikacji, która $appgw na poziomie słuchacza, i zwraca zaktualizowaną bramę.</span><span class="sxs-lookup"><span data-stu-id="c5096-111">This command adds a custom error of http status code 502 to the application gateway $appgw at the listener level, and return the updated gateway.</span></span>

## <span data-ttu-id="c5096-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5096-112">PARAMETERS</span></span>

### <span data-ttu-id="c5096-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c5096-113">-ApplicationGateway</span></span>
<span data-ttu-id="c5096-114">Brama aplikacji</span><span class="sxs-lookup"><span data-stu-id="c5096-114">The Application Gateway</span></span>

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

### <span data-ttu-id="c5096-115">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="c5096-115">-CustomErrorPageUrl</span></span>
<span data-ttu-id="c5096-116">Adres URL strony błędu klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c5096-116">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="c5096-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5096-117">-DefaultProfile</span></span>
<span data-ttu-id="c5096-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c5096-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5096-119">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="c5096-119">-StatusCode</span></span>
<span data-ttu-id="c5096-120">Kod stanu błędu klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c5096-120">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="c5096-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5096-121">CommonParameters</span></span>
<span data-ttu-id="c5096-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5096-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5096-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5096-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5096-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c5096-124">INPUTS</span></span>

### <span data-ttu-id="c5096-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c5096-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c5096-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c5096-126">OUTPUTS</span></span>

### <span data-ttu-id="c5096-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="c5096-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="c5096-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c5096-128">NOTES</span></span>

## <span data-ttu-id="c5096-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c5096-129">RELATED LINKS</span></span>

[<span data-ttu-id="c5096-130">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="c5096-130">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="c5096-131">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="c5096-131">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="c5096-132">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="c5096-132">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="c5096-133">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="c5096-133">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
