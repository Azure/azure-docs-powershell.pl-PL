---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeHealthResponseMatch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeHealthResponseMatch.md
ms.openlocfilehash: 6b54c300eb6e37544246b785fe30b2a3dcb67b9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718518"
---
# <span data-ttu-id="1292f-101">New-AzureRmApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="1292f-101">New-AzureRmApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="1292f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1292f-102">SYNOPSIS</span></span>
<span data-ttu-id="1292f-103">Tworzy dopasowanie odpowiedzi badania kondycji używane przez sondę kondycji dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1292f-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1292f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1292f-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayProbeHealthResponseMatch [-Body <String>]
 [-StatusCode <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1292f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1292f-105">DESCRIPTION</span></span>
<span data-ttu-id="1292f-106">Polecenie cmdlet **Add-AzureRmApplicationGatewayProbeHealthResponseMatch** powoduje utworzenie dopasowania odpowiedzi badania kondycji, używanej przez sondę kondycji dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1292f-106">**The Add-AzureRmApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="1292f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1292f-107">EXAMPLES</span></span>

### <span data-ttu-id="1292f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1292f-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzureRmApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="1292f-109">To polecenie tworzy zgodność z odpowiedzią na kondycję, która może zostać przekazana do ProbeConfig jako parametr.</span><span class="sxs-lookup"><span data-stu-id="1292f-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="1292f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1292f-110">PARAMETERS</span></span>

### <span data-ttu-id="1292f-111">-Body</span><span class="sxs-lookup"><span data-stu-id="1292f-111">-Body</span></span>
<span data-ttu-id="1292f-112">Treść, która musi być zawarta w odpowiedzi na kondycję.</span><span class="sxs-lookup"><span data-stu-id="1292f-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="1292f-113">Wartość domyślna jest pusta</span><span class="sxs-lookup"><span data-stu-id="1292f-113">Default value is empty</span></span>

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

### <span data-ttu-id="1292f-114">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="1292f-114">-StatusCode</span></span>
<span data-ttu-id="1292f-115">Dozwolone zakresy kodów statusu w dobrej kondycji. Domyślnym zakresem prawidłowych kodów stanu jest 200-399</span><span class="sxs-lookup"><span data-stu-id="1292f-115">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

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

### <span data-ttu-id="1292f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1292f-116">-DefaultProfile</span></span>
<span data-ttu-id="1292f-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1292f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1292f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1292f-118">CommonParameters</span></span>
<span data-ttu-id="1292f-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1292f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1292f-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1292f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1292f-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1292f-121">INPUTS</span></span>

### <span data-ttu-id="1292f-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1292f-122">None</span></span>

## <span data-ttu-id="1292f-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1292f-123">OUTPUTS</span></span>

### <span data-ttu-id="1292f-124">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="1292f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="1292f-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1292f-125">NOTES</span></span>

## <span data-ttu-id="1292f-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1292f-126">RELATED LINKS</span></span>

