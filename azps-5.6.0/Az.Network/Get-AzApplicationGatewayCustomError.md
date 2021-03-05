---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 459880d6ab771e48a9fe2d5ba69abffae35db7b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996570"
---
# <span data-ttu-id="bc944-101">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="bc944-101">Get-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="bc944-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc944-102">SYNOPSIS</span></span>
<span data-ttu-id="bc944-103">Pobiera błędy niestandardowe z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="bc944-103">Gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="bc944-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bc944-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayCustomError [-StatusCode <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc944-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="bc944-105">DESCRIPTION</span></span>
<span data-ttu-id="bc944-106">Polecenie **cmdlet Get-AzApplicationGatewayCustomError** pobiera błędy niestandardowe z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="bc944-106">The **Get-AzApplicationGatewayCustomError** cmdlet gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="bc944-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bc944-107">EXAMPLES</span></span>

### <span data-ttu-id="bc944-108">Przykład 1. Zwraca błąd niestandardowy w bramie aplikacji</span><span class="sxs-lookup"><span data-stu-id="bc944-108">Example 1: Gets a custom error in an application gateway</span></span>
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="bc944-109">To polecenie pobiera i zwraca niestandardowy błąd kodu stanu http 502 z bramy $appgw.</span><span class="sxs-lookup"><span data-stu-id="bc944-109">This command gets and returns the custom error of http status code 502 from the application gateway $appgw.</span></span>

### <span data-ttu-id="bc944-110">Przykład 2. Pobiera listę wszystkich błędów niestandardowych w bramie aplikacji</span><span class="sxs-lookup"><span data-stu-id="bc944-110">Example 2: Gets the list of all custom errors in an application gateway</span></span>
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw
```

<span data-ttu-id="bc944-111">To polecenie pobiera i zwraca listę wszystkich błędów niestandardowych z wykazu $appgw.</span><span class="sxs-lookup"><span data-stu-id="bc944-111">This command gets and returns the list of all custom errors from the application gateway $appgw.</span></span>

## <span data-ttu-id="bc944-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc944-112">PARAMETERS</span></span>

### <span data-ttu-id="bc944-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bc944-113">-ApplicationGateway</span></span>
<span data-ttu-id="bc944-114">Brama aplikacji</span><span class="sxs-lookup"><span data-stu-id="bc944-114">The Application Gateway</span></span>

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

### <span data-ttu-id="bc944-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc944-115">-DefaultProfile</span></span>
<span data-ttu-id="bc944-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bc944-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc944-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="bc944-117">-StatusCode</span></span>
<span data-ttu-id="bc944-118">Kod stanu błędu klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="bc944-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="bc944-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc944-119">CommonParameters</span></span>
<span data-ttu-id="bc944-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc944-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc944-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bc944-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc944-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc944-122">INPUTS</span></span>

### <span data-ttu-id="bc944-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bc944-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bc944-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc944-124">OUTPUTS</span></span>

### <span data-ttu-id="bc944-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="bc944-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="bc944-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bc944-126">NOTES</span></span>

## <span data-ttu-id="bc944-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bc944-127">RELATED LINKS</span></span>

[<span data-ttu-id="bc944-128">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="bc944-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="bc944-129">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="bc944-129">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="bc944-130">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="bc944-130">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="bc944-131">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="bc944-131">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
