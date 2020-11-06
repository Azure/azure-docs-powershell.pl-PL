---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayCustomError.md
ms.openlocfilehash: 9e05684f40223711db7a8a6aaaf1cfb684efced4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551164"
---
# <span data-ttu-id="c38bf-101">New-AzureRmApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="c38bf-101">New-AzureRmApplicationGatewayCustomError</span></span>

## <span data-ttu-id="c38bf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c38bf-102">SYNOPSIS</span></span>
<span data-ttu-id="c38bf-103">Tworzy błąd niestandardowy z kodem stanu HTTP i adresem URL strony błędu niestandardowego</span><span class="sxs-lookup"><span data-stu-id="c38bf-103">Creates a custom error with http status code and custom error page url</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c38bf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c38bf-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayCustomError -StatusCode <String> -CustomErrorPageUrl <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c38bf-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c38bf-105">DESCRIPTION</span></span>
<span data-ttu-id="c38bf-106">Polecenie cmdlet **New-AzureRmApplicationGatewayCustomError** powoduje utworzenie niestandardowego błędu.</span><span class="sxs-lookup"><span data-stu-id="c38bf-106">The **New-AzureRmApplicationGatewayCustomError** cmdlet creates a custom error.</span></span>

## <span data-ttu-id="c38bf-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c38bf-107">EXAMPLES</span></span>

### <span data-ttu-id="c38bf-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c38bf-108">Example 1</span></span>
```powershell
PS C:\> $customError403Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/403-another.htm"
PS C:\> $ce = New-AzureRmApplicationGatewayCustomError -StatusCode HttpStatus403 -CustomErrorPageUrl $customError403Url
```

<span data-ttu-id="c38bf-109">To polecenie powoduje utworzenie niestandardowego błędu dotyczącego kodu stanu HTTP 403.</span><span class="sxs-lookup"><span data-stu-id="c38bf-109">This command creates the custom error of http status code 403.</span></span>

## <span data-ttu-id="c38bf-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c38bf-110">PARAMETERS</span></span>

### <span data-ttu-id="c38bf-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="c38bf-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="c38bf-112">Adres URL strony błędu z błędem klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c38bf-112">Error page URL of the application gateway customer error.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c38bf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c38bf-113">-DefaultProfile</span></span>
<span data-ttu-id="c38bf-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c38bf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c38bf-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="c38bf-115">-StatusCode</span></span>
<span data-ttu-id="c38bf-116">Kod stanu błędu klienta bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c38bf-116">Status code of the application gateway customer error.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c38bf-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c38bf-117">CommonParameters</span></span>
<span data-ttu-id="c38bf-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c38bf-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c38bf-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c38bf-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c38bf-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c38bf-120">INPUTS</span></span>

### <span data-ttu-id="c38bf-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c38bf-121">None</span></span>

## <span data-ttu-id="c38bf-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c38bf-122">OUTPUTS</span></span>

### <span data-ttu-id="c38bf-123">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="c38bf-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="c38bf-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c38bf-124">NOTES</span></span>

## <span data-ttu-id="c38bf-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c38bf-125">RELATED LINKS</span></span>
