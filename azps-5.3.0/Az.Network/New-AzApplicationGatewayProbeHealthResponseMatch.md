---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprobehealthresponsematch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
ms.openlocfilehash: edc0309b5e1a0c8b17d400e965074d38ca02bb80
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379393"
---
# <span data-ttu-id="ae26b-101">New-AzApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="ae26b-101">New-AzApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="ae26b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ae26b-102">SYNOPSIS</span></span>
<span data-ttu-id="ae26b-103">Tworzy dopasowanie odpowiedzi badania kondycji używane przez sondę kondycji dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ae26b-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="ae26b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ae26b-104">SYNTAX</span></span>

```
New-AzApplicationGatewayProbeHealthResponseMatch [-Body <String>] [-StatusCode <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae26b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ae26b-105">DESCRIPTION</span></span>
<span data-ttu-id="ae26b-106">Polecenie cmdlet **Add-AzApplicationGatewayProbeHealthResponseMatch** powoduje utworzenie dopasowania odpowiedzi badania kondycji, używanej przez sondę kondycji dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ae26b-106">**The Add-AzApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="ae26b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ae26b-107">EXAMPLES</span></span>

### <span data-ttu-id="ae26b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ae26b-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="ae26b-109">To polecenie tworzy zgodność z odpowiedzią na kondycję, która może zostać przekazana do ProbeConfig jako parametr.</span><span class="sxs-lookup"><span data-stu-id="ae26b-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="ae26b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ae26b-110">PARAMETERS</span></span>

### <span data-ttu-id="ae26b-111">-Body</span><span class="sxs-lookup"><span data-stu-id="ae26b-111">-Body</span></span>
<span data-ttu-id="ae26b-112">Treść, która musi być zawarta w odpowiedzi na kondycję.</span><span class="sxs-lookup"><span data-stu-id="ae26b-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="ae26b-113">Wartość domyślna jest pusta</span><span class="sxs-lookup"><span data-stu-id="ae26b-113">Default value is empty</span></span>

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

### <span data-ttu-id="ae26b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae26b-114">-DefaultProfile</span></span>
<span data-ttu-id="ae26b-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ae26b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae26b-116">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="ae26b-116">-StatusCode</span></span>
<span data-ttu-id="ae26b-117">Dozwolone zakresy kodów statusu w dobrej kondycji. Domyślnym zakresem prawidłowych kodów stanu jest 200-399</span><span class="sxs-lookup"><span data-stu-id="ae26b-117">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae26b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae26b-118">CommonParameters</span></span>
<span data-ttu-id="ae26b-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae26b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae26b-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae26b-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae26b-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae26b-121">INPUTS</span></span>

### <span data-ttu-id="ae26b-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ae26b-122">None</span></span>

## <span data-ttu-id="ae26b-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ae26b-123">OUTPUTS</span></span>

### <span data-ttu-id="ae26b-124">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="ae26b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="ae26b-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ae26b-125">NOTES</span></span>

## <span data-ttu-id="ae26b-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ae26b-126">RELATED LINKS</span></span>
