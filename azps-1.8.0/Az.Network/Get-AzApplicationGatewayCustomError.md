---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
ms.openlocfilehash: fbf10b3cfc323a25a7d7a63dc047a4b24141c5d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709627"
---
# <span data-ttu-id="3f628-101">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="3f628-101">Get-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="3f628-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3f628-102">SYNOPSIS</span></span>
<span data-ttu-id="3f628-103">Pobiera błędy niestandardowe od bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3f628-103">Gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="3f628-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3f628-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayCustomError [-StatusCode <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f628-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3f628-105">DESCRIPTION</span></span>
<span data-ttu-id="3f628-106">Polecenie cmdlet **Get-AzApplicationGatewayCustomError** pobiera błędy niestandardowe od bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="3f628-106">The **Get-AzApplicationGatewayCustomError** cmdlet gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="3f628-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3f628-107">EXAMPLES</span></span>

### <span data-ttu-id="3f628-108">Przykład 1: Pobiera błąd niestandardowy w bramie Application Gateway</span><span class="sxs-lookup"><span data-stu-id="3f628-108">Example 1: Gets a custom error in an application gateway</span></span>
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="3f628-109">To polecenie pobiera i zwraca błąd niestandardowy kodu stanu HTTP 502 z $appgw bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="3f628-109">This command gets and returns the custom error of http status code 502 from the application gateway $appgw.</span></span>

### <span data-ttu-id="3f628-110">Przykład 2: Pobiera listę wszystkich błędów niestandardowych w bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3f628-110">Example 2: Gets the list of all custom errors in an application gateway</span></span>
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw
```

<span data-ttu-id="3f628-111">To polecenie pobiera i zwraca listę wszystkich błędów niestandardowych z $appgw bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="3f628-111">This command gets and returns the list of all custom errors from the application gateway $appgw.</span></span>

## <span data-ttu-id="3f628-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3f628-112">PARAMETERS</span></span>

### <span data-ttu-id="3f628-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3f628-113">-ApplicationGateway</span></span>
<span data-ttu-id="3f628-114">Brama Application Gateway</span><span class="sxs-lookup"><span data-stu-id="3f628-114">The Application Gateway</span></span>

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

### <span data-ttu-id="3f628-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f628-115">-DefaultProfile</span></span>
<span data-ttu-id="3f628-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3f628-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f628-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="3f628-117">-StatusCode</span></span>
<span data-ttu-id="3f628-118">Kod stanu błędu klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3f628-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="3f628-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f628-119">CommonParameters</span></span>
<span data-ttu-id="3f628-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f628-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f628-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f628-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f628-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3f628-122">INPUTS</span></span>

### <span data-ttu-id="3f628-123">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3f628-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3f628-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3f628-124">OUTPUTS</span></span>

### <span data-ttu-id="3f628-125">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="3f628-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="3f628-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3f628-126">NOTES</span></span>

## <span data-ttu-id="3f628-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3f628-127">RELATED LINKS</span></span>

[<span data-ttu-id="3f628-128">Dodaj-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="3f628-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="3f628-129">Nowe — AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="3f628-129">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="3f628-130">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="3f628-130">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="3f628-131">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="3f628-131">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)