---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayCustomError.md
ms.openlocfilehash: b2f748bca68bff772026237f3bb6205ca6bc1923
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718814"
---
# <span data-ttu-id="5e251-101">Get-AzureRmApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="5e251-101">Get-AzureRmApplicationGatewayCustomError</span></span>

## <span data-ttu-id="5e251-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5e251-102">SYNOPSIS</span></span>
<span data-ttu-id="5e251-103">Pobiera błędy niestandardowe od bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5e251-103">Gets custom error(s) from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e251-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5e251-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayCustomError [-StatusCode <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e251-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5e251-105">DESCRIPTION</span></span>
<span data-ttu-id="5e251-106">Polecenie cmdlet **Get-AzureRmApplicationGatewayCustomError** pobiera błędy niestandardowe od bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="5e251-106">The **Get-AzureRmApplicationGatewayCustomError** cmdlet gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="5e251-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5e251-107">EXAMPLES</span></span>

### <span data-ttu-id="5e251-108">Przykład 1: Pobiera błąd niestandardowy w bramie Application Gateway</span><span class="sxs-lookup"><span data-stu-id="5e251-108">Example 1: Gets a custom error in an application gateway</span></span>
```powershell
PS C:\> $ce = Get-AzureRmApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="5e251-109">To polecenie pobiera i zwraca błąd niestandardowy kodu stanu HTTP 502 z $appgw bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="5e251-109">This command gets and returns the custom error of http status code 502 from the application gateway $appgw.</span></span>

### <span data-ttu-id="5e251-110">Przykład 2: Pobiera listę wszystkich błędów niestandardowych w bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5e251-110">Example 2: Gets the list of all custom errors in an application gateway</span></span>
```powershell
PS C:\> $ces = Get-AzureRmApplicationGatewayCustomError -ApplicationGateway $appgw
```

<span data-ttu-id="5e251-111">To polecenie pobiera i zwraca listę wszystkich błędów niestandardowych z $appgw bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="5e251-111">This command gets and returns the list of all custom errors from the application gateway $appgw.</span></span>

## <span data-ttu-id="5e251-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5e251-112">PARAMETERS</span></span>

### <span data-ttu-id="5e251-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5e251-113">-ApplicationGateway</span></span>
<span data-ttu-id="5e251-114">Brama Application Gateway</span><span class="sxs-lookup"><span data-stu-id="5e251-114">The Application Gateway</span></span>

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

### <span data-ttu-id="5e251-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e251-115">-DefaultProfile</span></span>
<span data-ttu-id="5e251-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5e251-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e251-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="5e251-117">-StatusCode</span></span>
<span data-ttu-id="5e251-118">Kod stanu błędu klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5e251-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="5e251-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e251-119">CommonParameters</span></span>
<span data-ttu-id="5e251-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e251-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e251-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e251-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e251-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5e251-122">INPUTS</span></span>

### <span data-ttu-id="5e251-123">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5e251-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5e251-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5e251-124">OUTPUTS</span></span>

### <span data-ttu-id="5e251-125">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="5e251-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="5e251-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5e251-126">NOTES</span></span>

## <span data-ttu-id="5e251-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5e251-127">RELATED LINKS</span></span>
