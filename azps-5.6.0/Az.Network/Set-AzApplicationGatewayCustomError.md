---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 4c06b78062500ddb5c33353c00814a46e919bd8d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987722"
---
# <span data-ttu-id="ab4b8-101">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="ab4b8-101">Set-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="ab4b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab4b8-102">SYNOPSIS</span></span>
<span data-ttu-id="ab4b8-103">Aktualizuje błąd niestandardowy w bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ab4b8-103">Updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="ab4b8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ab4b8-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab4b8-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ab4b8-105">DESCRIPTION</span></span>
<span data-ttu-id="ab4b8-106">Polecenie **cmdlet Set-AzApplicationGatewayCustomError** aktualizuje błąd niestandardowy w bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ab4b8-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="ab4b8-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ab4b8-107">EXAMPLES</span></span>

### <span data-ttu-id="ab4b8-108">Przykład 1. Aktualizacja błędu niestandardowego w bramie aplikacji</span><span class="sxs-lookup"><span data-stu-id="ab4b8-108">Example 1: Updates custom error in an application gateway</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Set-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="ab4b8-109">To polecenie aktualizuje niestandardowy błąd kodu stanu http 502 w bramie aplikacji $appgw i zwraca zaktualizowaną bramę.</span><span class="sxs-lookup"><span data-stu-id="ab4b8-109">This command updates the custom error of http status code 502 in the application gateway $appgw, and returns the updated gateway.</span></span>

## <span data-ttu-id="ab4b8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab4b8-110">PARAMETERS</span></span>

### <span data-ttu-id="ab4b8-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ab4b8-111">-ApplicationGateway</span></span>
<span data-ttu-id="ab4b8-112">Brama aplikacji</span><span class="sxs-lookup"><span data-stu-id="ab4b8-112">The Application Gateway</span></span>

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

### <span data-ttu-id="ab4b8-113">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="ab4b8-113">-CustomErrorPageUrl</span></span>
<span data-ttu-id="ab4b8-114">Adres URL strony błędu klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ab4b8-114">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="ab4b8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab4b8-115">-DefaultProfile</span></span>
<span data-ttu-id="ab4b8-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ab4b8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab4b8-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="ab4b8-117">-StatusCode</span></span>
<span data-ttu-id="ab4b8-118">Kod stanu błędu klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ab4b8-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="ab4b8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab4b8-119">CommonParameters</span></span>
<span data-ttu-id="ab4b8-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab4b8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab4b8-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab4b8-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab4b8-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab4b8-122">INPUTS</span></span>

### <span data-ttu-id="ab4b8-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ab4b8-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ab4b8-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab4b8-124">OUTPUTS</span></span>

### <span data-ttu-id="ab4b8-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="ab4b8-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="ab4b8-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ab4b8-126">NOTES</span></span>

## <span data-ttu-id="ab4b8-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ab4b8-127">RELATED LINKS</span></span>

[<span data-ttu-id="ab4b8-128">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="ab4b8-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="ab4b8-129">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="ab4b8-129">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="ab4b8-130">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="ab4b8-130">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="ab4b8-131">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="ab4b8-131">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)
