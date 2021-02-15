---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 84c80ba4469d8003344d99b7dfbb89ff7d6660b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189842"
---
# <span data-ttu-id="29272-101">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="29272-101">Get-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="29272-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29272-102">SYNOPSIS</span></span>
<span data-ttu-id="29272-103">Pobiera błędy niestandardowe z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="29272-103">Gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="29272-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="29272-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayCustomError [-StatusCode <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29272-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="29272-105">DESCRIPTION</span></span>
<span data-ttu-id="29272-106">Polecenie **cmdlet Get-AzApplicationGatewayCustomError** pobiera błędy niestandardowe z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="29272-106">The **Get-AzApplicationGatewayCustomError** cmdlet gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="29272-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="29272-107">EXAMPLES</span></span>

### <span data-ttu-id="29272-108">Przykład 1. Zwraca błąd niestandardowy w bramie aplikacji</span><span class="sxs-lookup"><span data-stu-id="29272-108">Example 1: Gets a custom error in an application gateway</span></span>
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="29272-109">To polecenie pobiera i zwraca niestandardowy błąd kodu stanu http 502 z bramy $appgw.</span><span class="sxs-lookup"><span data-stu-id="29272-109">This command gets and returns the custom error of http status code 502 from the application gateway $appgw.</span></span>

### <span data-ttu-id="29272-110">Przykład 2. Pobiera listę wszystkich błędów niestandardowych w bramie aplikacji</span><span class="sxs-lookup"><span data-stu-id="29272-110">Example 2: Gets the list of all custom errors in an application gateway</span></span>
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw
```

<span data-ttu-id="29272-111">To polecenie pobiera i zwraca listę wszystkich błędów niestandardowych z listy błędów $appgw.</span><span class="sxs-lookup"><span data-stu-id="29272-111">This command gets and returns the list of all custom errors from the application gateway $appgw.</span></span>

## <span data-ttu-id="29272-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29272-112">PARAMETERS</span></span>

### <span data-ttu-id="29272-113">- ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="29272-113">-ApplicationGateway</span></span>
<span data-ttu-id="29272-114">Brama aplikacji</span><span class="sxs-lookup"><span data-stu-id="29272-114">The Application Gateway</span></span>

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

### <span data-ttu-id="29272-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29272-115">-DefaultProfile</span></span>
<span data-ttu-id="29272-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="29272-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29272-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="29272-117">-StatusCode</span></span>
<span data-ttu-id="29272-118">Kod stanu błędu klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="29272-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="29272-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29272-119">CommonParameters</span></span>
<span data-ttu-id="29272-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29272-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29272-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="29272-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29272-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29272-122">INPUTS</span></span>

### <span data-ttu-id="29272-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="29272-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="29272-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="29272-124">OUTPUTS</span></span>

### <span data-ttu-id="29272-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="29272-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="29272-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="29272-126">NOTES</span></span>

## <span data-ttu-id="29272-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="29272-127">RELATED LINKS</span></span>

[<span data-ttu-id="29272-128">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="29272-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="29272-129">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="29272-129">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="29272-130">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="29272-130">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="29272-131">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="29272-131">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
