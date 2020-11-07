---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 3e5b928696fde62a9628a055191d0aabf94b5311
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870551"
---
# <span data-ttu-id="d7979-101">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="d7979-101">New-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="d7979-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d7979-102">SYNOPSIS</span></span>
<span data-ttu-id="d7979-103">Tworzy błąd niestandardowy z kodem stanu HTTP i adresem URL strony błędu niestandardowego</span><span class="sxs-lookup"><span data-stu-id="d7979-103">Creates a custom error with http status code and custom error page url</span></span> 

## <span data-ttu-id="d7979-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d7979-104">SYNTAX</span></span>

```
New-AzApplicationGatewayCustomError -StatusCode <String> -CustomErrorPageUrl <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7979-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d7979-105">DESCRIPTION</span></span>
<span data-ttu-id="d7979-106">Polecenie cmdlet **New-AzApplicationGatewayCustomError** powoduje utworzenie niestandardowego błędu.</span><span class="sxs-lookup"><span data-stu-id="d7979-106">The **New-AzApplicationGatewayCustomError** cmdlet creates a custom error.</span></span>

## <span data-ttu-id="d7979-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d7979-107">EXAMPLES</span></span>

### <span data-ttu-id="d7979-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d7979-108">Example 1</span></span>
```powershell
PS C:\> $customError403Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/403-another.htm"
PS C:\> $ce = New-AzApplicationGatewayCustomError -StatusCode HttpStatus403 -CustomErrorPageUrl $customError403Url
```

<span data-ttu-id="d7979-109">To polecenie powoduje utworzenie niestandardowego błędu dotyczącego kodu stanu HTTP 403.</span><span class="sxs-lookup"><span data-stu-id="d7979-109">This command creates the custom error of http status code 403.</span></span>

## <span data-ttu-id="d7979-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d7979-110">PARAMETERS</span></span>

### <span data-ttu-id="d7979-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="d7979-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="d7979-112">Adres URL strony błędu z błędem klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d7979-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="d7979-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7979-113">-DefaultProfile</span></span>
<span data-ttu-id="d7979-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d7979-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7979-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="d7979-115">-StatusCode</span></span>
<span data-ttu-id="d7979-116">Kod stanu błędu klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d7979-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="d7979-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7979-117">CommonParameters</span></span>
<span data-ttu-id="d7979-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7979-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7979-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7979-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7979-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7979-120">INPUTS</span></span>

### <span data-ttu-id="d7979-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d7979-121">None</span></span>

## <span data-ttu-id="d7979-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d7979-122">OUTPUTS</span></span>

### <span data-ttu-id="d7979-123">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="d7979-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="d7979-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d7979-124">NOTES</span></span>

## <span data-ttu-id="d7979-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d7979-125">RELATED LINKS</span></span>

[<span data-ttu-id="d7979-126">Dodaj-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="d7979-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="d7979-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="d7979-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="d7979-128">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="d7979-128">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="d7979-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="d7979-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
