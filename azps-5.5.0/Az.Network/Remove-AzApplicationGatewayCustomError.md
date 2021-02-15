---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 91de215282dc05be2136237fa5fb2b244d7f0c4a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186971"
---
# <span data-ttu-id="457f8-101">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="457f8-101">Remove-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="457f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="457f8-102">SYNOPSIS</span></span>
<span data-ttu-id="457f8-103">Usuwa błąd niestandardowy z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="457f8-103">Removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="457f8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="457f8-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayCustomError -StatusCode <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="457f8-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="457f8-105">DESCRIPTION</span></span>
<span data-ttu-id="457f8-106">Polecenie **cmdlet Remove-AzApplicationGatewayCustomError** usuwa błąd niestandardowy z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="457f8-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="457f8-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="457f8-107">EXAMPLES</span></span>

### <span data-ttu-id="457f8-108">Przykład 1. Usuwanie błędu niestandardowego z bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="457f8-108">Example 1: Removes custom error from an application gateway</span></span>
```
PS C:\> $updatedgateway = Remove-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="457f8-109">To polecenie usuwa niestandardowy błąd kodu stanu http 502 z serwera $appgw i zwraca zaktualizowaną bramę.</span><span class="sxs-lookup"><span data-stu-id="457f8-109">This command removes the custom error of http status code 502 from the application gateway $appgw, and return the updated gateway.</span></span>

## <span data-ttu-id="457f8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="457f8-110">PARAMETERS</span></span>

### <span data-ttu-id="457f8-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="457f8-111">-ApplicationGateway</span></span>
<span data-ttu-id="457f8-112">Brama aplikacji</span><span class="sxs-lookup"><span data-stu-id="457f8-112">The Application Gateway</span></span>

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

### <span data-ttu-id="457f8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="457f8-113">-DefaultProfile</span></span>
<span data-ttu-id="457f8-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="457f8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="457f8-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="457f8-115">-StatusCode</span></span>
<span data-ttu-id="457f8-116">Kod stanu błędu klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="457f8-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="457f8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="457f8-117">CommonParameters</span></span>
<span data-ttu-id="457f8-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="457f8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="457f8-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="457f8-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="457f8-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="457f8-120">INPUTS</span></span>

### <span data-ttu-id="457f8-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="457f8-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="457f8-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="457f8-122">OUTPUTS</span></span>

### <span data-ttu-id="457f8-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="457f8-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="457f8-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="457f8-124">NOTES</span></span>

## <span data-ttu-id="457f8-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="457f8-125">RELATED LINKS</span></span>

[<span data-ttu-id="457f8-126">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="457f8-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="457f8-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="457f8-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="457f8-128">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="457f8-128">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="457f8-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="457f8-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
