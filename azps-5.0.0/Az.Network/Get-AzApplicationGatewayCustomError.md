---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 84c80ba4469d8003344d99b7dfbb89ff7d6660b2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232817"
---
# <span data-ttu-id="a7c4f-101">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="a7c4f-101">Get-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="a7c4f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a7c4f-102">SYNOPSIS</span></span>
<span data-ttu-id="a7c4f-103">Pobiera błędy niestandardowe od bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a7c4f-103">Gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="a7c4f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a7c4f-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayCustomError [-StatusCode <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7c4f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a7c4f-105">DESCRIPTION</span></span>
<span data-ttu-id="a7c4f-106">Polecenie cmdlet **Get-AzApplicationGatewayCustomError** pobiera błędy niestandardowe od bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="a7c4f-106">The **Get-AzApplicationGatewayCustomError** cmdlet gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="a7c4f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a7c4f-107">EXAMPLES</span></span>

### <span data-ttu-id="a7c4f-108">Przykład 1: Pobiera błąd niestandardowy w bramie Application Gateway</span><span class="sxs-lookup"><span data-stu-id="a7c4f-108">Example 1: Gets a custom error in an application gateway</span></span>
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="a7c4f-109">To polecenie pobiera i zwraca błąd niestandardowy kodu stanu HTTP 502 z $appgw bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="a7c4f-109">This command gets and returns the custom error of http status code 502 from the application gateway $appgw.</span></span>

### <span data-ttu-id="a7c4f-110">Przykład 2: Pobiera listę wszystkich błędów niestandardowych w bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a7c4f-110">Example 2: Gets the list of all custom errors in an application gateway</span></span>
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw
```

<span data-ttu-id="a7c4f-111">To polecenie pobiera i zwraca listę wszystkich błędów niestandardowych z $appgw bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="a7c4f-111">This command gets and returns the list of all custom errors from the application gateway $appgw.</span></span>

## <span data-ttu-id="a7c4f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a7c4f-112">PARAMETERS</span></span>

### <span data-ttu-id="a7c4f-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a7c4f-113">-ApplicationGateway</span></span>
<span data-ttu-id="a7c4f-114">Brama Application Gateway</span><span class="sxs-lookup"><span data-stu-id="a7c4f-114">The Application Gateway</span></span>

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

### <span data-ttu-id="a7c4f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7c4f-115">-DefaultProfile</span></span>
<span data-ttu-id="a7c4f-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a7c4f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7c4f-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="a7c4f-117">-StatusCode</span></span>
<span data-ttu-id="a7c4f-118">Kod stanu błędu klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a7c4f-118">Status code of the application gateway customer error.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7c4f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7c4f-119">CommonParameters</span></span>
<span data-ttu-id="a7c4f-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7c4f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7c4f-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7c4f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7c4f-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a7c4f-122">INPUTS</span></span>

### <span data-ttu-id="a7c4f-123">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a7c4f-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a7c4f-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a7c4f-124">OUTPUTS</span></span>

### <span data-ttu-id="a7c4f-125">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="a7c4f-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="a7c4f-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a7c4f-126">NOTES</span></span>

## <span data-ttu-id="a7c4f-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a7c4f-127">RELATED LINKS</span></span>

[<span data-ttu-id="a7c4f-128">Dodaj-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="a7c4f-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="a7c4f-129">Nowe — AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="a7c4f-129">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="a7c4f-130">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="a7c4f-130">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="a7c4f-131">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="a7c4f-131">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
