---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayavailablessloptions
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableSslOptions.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableSslOptions.md
ms.openlocfilehash: 157093dc382b4f56ac7759a9b32b42c8b2488d90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719410"
---
# <span data-ttu-id="b95c0-101">Get-AzureRmApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="b95c0-101">Get-AzureRmApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="b95c0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b95c0-102">SYNOPSIS</span></span>
<span data-ttu-id="b95c0-103">Pobiera wszystkie dostępne opcje protokołu SSL dla zasad SSL dla bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="b95c0-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b95c0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b95c0-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAvailableSslOptions [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b95c0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b95c0-105">DESCRIPTION</span></span>
<span data-ttu-id="b95c0-106">Polecenie cmdlet **Get-AzureRmApplicationGatewayAvailableSslOptions** pobiera wszystkie dostępne opcje protokołu SSL dla zasad SSL</span><span class="sxs-lookup"><span data-stu-id="b95c0-106">The **Get-AzureRmApplicationGatewayAvailableSslOptions** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="b95c0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b95c0-107">EXAMPLES</span></span>

### <span data-ttu-id="b95c0-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b95c0-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzureRmApplicationGatewayAvailableSslOptions
```

<span data-ttu-id="b95c0-109">To polecenie zwraca wszystkie dostępne opcje protokołu SSL dla zasad SSL.</span><span class="sxs-lookup"><span data-stu-id="b95c0-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="b95c0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b95c0-110">PARAMETERS</span></span>

### <span data-ttu-id="b95c0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b95c0-111">-DefaultProfile</span></span>
<span data-ttu-id="b95c0-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b95c0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b95c0-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b95c0-113">CommonParameters</span></span>
<span data-ttu-id="b95c0-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b95c0-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b95c0-115">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b95c0-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b95c0-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b95c0-116">INPUTS</span></span>

### <span data-ttu-id="b95c0-117">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b95c0-117">None</span></span>

## <span data-ttu-id="b95c0-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b95c0-118">OUTPUTS</span></span>

### <span data-ttu-id="b95c0-119">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="b95c0-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="b95c0-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b95c0-120">NOTES</span></span>

## <span data-ttu-id="b95c0-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b95c0-121">RELATED LINKS</span></span>