---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 377145933832c587691ed30db08754ef1e6f1f64
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971921"
---
# <span data-ttu-id="c3be7-101">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="c3be7-101">New-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="c3be7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3be7-102">SYNOPSIS</span></span>
<span data-ttu-id="c3be7-103">Tworzy błąd niestandardowy z kodem stanu http i niestandardowym adresem URL strony błędu</span><span class="sxs-lookup"><span data-stu-id="c3be7-103">Creates a custom error with http status code and custom error page url</span></span> 

## <span data-ttu-id="c3be7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c3be7-104">SYNTAX</span></span>

```
New-AzApplicationGatewayCustomError -StatusCode <String> -CustomErrorPageUrl <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3be7-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c3be7-105">DESCRIPTION</span></span>
<span data-ttu-id="c3be7-106">Polecenie **cmdlet New-AzApplicationGatewayCustomError** powoduje utworzenie błędu niestandardowego.</span><span class="sxs-lookup"><span data-stu-id="c3be7-106">The **New-AzApplicationGatewayCustomError** cmdlet creates a custom error.</span></span>

## <span data-ttu-id="c3be7-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c3be7-107">EXAMPLES</span></span>

### <span data-ttu-id="c3be7-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c3be7-108">Example 1</span></span>
```powershell
PS C:\> $customError403Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/403-another.htm"
PS C:\> $ce = New-AzApplicationGatewayCustomError -StatusCode HttpStatus403 -CustomErrorPageUrl $customError403Url
```

<span data-ttu-id="c3be7-109">To polecenie tworzy niestandardowy błąd o kodzie stanu http 403.</span><span class="sxs-lookup"><span data-stu-id="c3be7-109">This command creates the custom error of http status code 403.</span></span>

## <span data-ttu-id="c3be7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3be7-110">PARAMETERS</span></span>

### <span data-ttu-id="c3be7-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="c3be7-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="c3be7-112">Adres URL strony błędu klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c3be7-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="c3be7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3be7-113">-DefaultProfile</span></span>
<span data-ttu-id="c3be7-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c3be7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3be7-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="c3be7-115">-StatusCode</span></span>
<span data-ttu-id="c3be7-116">Kod stanu błędu klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c3be7-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="c3be7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3be7-117">CommonParameters</span></span>
<span data-ttu-id="c3be7-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3be7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3be7-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3be7-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3be7-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c3be7-120">INPUTS</span></span>

### <span data-ttu-id="c3be7-121">Brak</span><span class="sxs-lookup"><span data-stu-id="c3be7-121">None</span></span>

## <span data-ttu-id="c3be7-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c3be7-122">OUTPUTS</span></span>

### <span data-ttu-id="c3be7-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="c3be7-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="c3be7-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c3be7-124">NOTES</span></span>

## <span data-ttu-id="c3be7-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c3be7-125">RELATED LINKS</span></span>

[<span data-ttu-id="c3be7-126">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="c3be7-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="c3be7-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="c3be7-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="c3be7-128">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="c3be7-128">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="c3be7-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="c3be7-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
