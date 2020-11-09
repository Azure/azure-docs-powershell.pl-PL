---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 91de215282dc05be2136237fa5fb2b244d7f0c4a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319158"
---
# <span data-ttu-id="b6542-101">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="b6542-101">Remove-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="b6542-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b6542-102">SYNOPSIS</span></span>
<span data-ttu-id="b6542-103">Usuwa błąd niestandardowy z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b6542-103">Removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="b6542-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b6542-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayCustomError -StatusCode <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6542-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b6542-105">DESCRIPTION</span></span>
<span data-ttu-id="b6542-106">Polecenie cmdlet **Remove-AzApplicationGatewayCustomError** usuwa błąd niestandardowy z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b6542-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="b6542-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b6542-107">EXAMPLES</span></span>

### <span data-ttu-id="b6542-108">Przykład 1. usuwa błąd niestandardowy z bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="b6542-108">Example 1: Removes custom error from an application gateway</span></span>
```
PS C:\> $updatedgateway = Remove-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="b6542-109">To polecenie usuwa błąd niestandardowy kodu stanu HTTP 502 z bramy Application Gateway $appgw i zwraca zaktualizowaną bramę.</span><span class="sxs-lookup"><span data-stu-id="b6542-109">This command removes the custom error of http status code 502 from the application gateway $appgw, and return the updated gateway.</span></span>

## <span data-ttu-id="b6542-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b6542-110">PARAMETERS</span></span>

### <span data-ttu-id="b6542-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b6542-111">-ApplicationGateway</span></span>
<span data-ttu-id="b6542-112">Brama Application Gateway</span><span class="sxs-lookup"><span data-stu-id="b6542-112">The Application Gateway</span></span>

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

### <span data-ttu-id="b6542-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6542-113">-DefaultProfile</span></span>
<span data-ttu-id="b6542-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b6542-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6542-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="b6542-115">-StatusCode</span></span>
<span data-ttu-id="b6542-116">Kod stanu błędu klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b6542-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="b6542-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6542-117">CommonParameters</span></span>
<span data-ttu-id="b6542-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6542-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6542-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6542-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6542-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6542-120">INPUTS</span></span>

### <span data-ttu-id="b6542-121">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b6542-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b6542-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b6542-122">OUTPUTS</span></span>

### <span data-ttu-id="b6542-123">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="b6542-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="b6542-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b6542-124">NOTES</span></span>

## <span data-ttu-id="b6542-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6542-125">RELATED LINKS</span></span>

[<span data-ttu-id="b6542-126">Dodaj-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="b6542-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="b6542-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="b6542-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="b6542-128">Nowe — AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="b6542-128">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="b6542-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="b6542-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
