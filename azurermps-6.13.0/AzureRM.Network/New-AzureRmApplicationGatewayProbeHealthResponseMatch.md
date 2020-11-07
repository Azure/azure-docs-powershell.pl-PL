---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayprobehealthresponsematch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeHealthResponseMatch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeHealthResponseMatch.md
ms.openlocfilehash: f2c893f7568d33eaeb1684c00b06e36771aae8bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717627"
---
# <span data-ttu-id="b6de9-101">New-AzureRmApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="b6de9-101">New-AzureRmApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="b6de9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b6de9-102">SYNOPSIS</span></span>
<span data-ttu-id="b6de9-103">Tworzy dopasowanie odpowiedzi badania kondycji używane przez sondę kondycji dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b6de9-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6de9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b6de9-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayProbeHealthResponseMatch [-Body <String>]
 [-StatusCode <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b6de9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b6de9-105">DESCRIPTION</span></span>
<span data-ttu-id="b6de9-106">Polecenie cmdlet **Add-AzureRmApplicationGatewayProbeHealthResponseMatch** powoduje utworzenie dopasowania odpowiedzi badania kondycji, używanej przez sondę kondycji dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b6de9-106">**The Add-AzureRmApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="b6de9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b6de9-107">EXAMPLES</span></span>

### <span data-ttu-id="b6de9-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b6de9-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzureRmApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="b6de9-109">To polecenie tworzy zgodność z odpowiedzią na kondycję, która może zostać przekazana do ProbeConfig jako parametr.</span><span class="sxs-lookup"><span data-stu-id="b6de9-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="b6de9-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b6de9-110">PARAMETERS</span></span>

### <span data-ttu-id="b6de9-111">-Body</span><span class="sxs-lookup"><span data-stu-id="b6de9-111">-Body</span></span>
<span data-ttu-id="b6de9-112">Treść, która musi być zawarta w odpowiedzi na kondycję.</span><span class="sxs-lookup"><span data-stu-id="b6de9-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="b6de9-113">Wartość domyślna jest pusta</span><span class="sxs-lookup"><span data-stu-id="b6de9-113">Default value is empty</span></span>

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

### <span data-ttu-id="b6de9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6de9-114">-DefaultProfile</span></span>
<span data-ttu-id="b6de9-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b6de9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6de9-116">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="b6de9-116">-StatusCode</span></span>
<span data-ttu-id="b6de9-117">Dozwolone zakresy kodów statusu w dobrej kondycji. Domyślnym zakresem prawidłowych kodów stanu jest 200-399</span><span class="sxs-lookup"><span data-stu-id="b6de9-117">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6de9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6de9-118">CommonParameters</span></span>
<span data-ttu-id="b6de9-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6de9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6de9-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6de9-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6de9-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6de9-121">INPUTS</span></span>

### <span data-ttu-id="b6de9-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b6de9-122">None</span></span>

## <span data-ttu-id="b6de9-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b6de9-123">OUTPUTS</span></span>

### <span data-ttu-id="b6de9-124">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="b6de9-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="b6de9-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b6de9-125">NOTES</span></span>

## <span data-ttu-id="b6de9-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6de9-126">RELATED LINKS</span></span>