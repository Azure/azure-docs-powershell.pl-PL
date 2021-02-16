---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprobehealthresponsematch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
ms.openlocfilehash: edc0309b5e1a0c8b17d400e965074d38ca02bb80
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202895"
---
# <span data-ttu-id="b951f-101">New-AzApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="b951f-101">New-AzApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="b951f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b951f-102">SYNOPSIS</span></span>
<span data-ttu-id="b951f-103">Tworzy dopasowanie odpowiedzi kondycji używane przez kondycję bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b951f-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="b951f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b951f-104">SYNTAX</span></span>

```
New-AzApplicationGatewayProbeHealthResponseMatch [-Body <String>] [-StatusCode <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b951f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b951f-105">DESCRIPTION</span></span>
<span data-ttu-id="b951f-106">**Polecenie cmdlet Add-AzApplicationGatewayProbeHealthResponseMatch** tworzy dopasowanie odpowiedzi kondycji używane przez kondycję bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b951f-106">**The Add-AzApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="b951f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b951f-107">EXAMPLES</span></span>

### <span data-ttu-id="b951f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b951f-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="b951f-109">To polecenie tworzy dopasowanie odpowiedzi kondycji, które może zostać przekazane do konfiguracji danych w parametrze.</span><span class="sxs-lookup"><span data-stu-id="b951f-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="b951f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b951f-110">PARAMETERS</span></span>

### <span data-ttu-id="b951f-111">— Treść</span><span class="sxs-lookup"><span data-stu-id="b951f-111">-Body</span></span>
<span data-ttu-id="b951f-112">Treść, która musi znajdować się w odpowiedzi na stan zdrowia.</span><span class="sxs-lookup"><span data-stu-id="b951f-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="b951f-113">Wartość domyślna jest pusta</span><span class="sxs-lookup"><span data-stu-id="b951f-113">Default value is empty</span></span>

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

### <span data-ttu-id="b951f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b951f-114">-DefaultProfile</span></span>
<span data-ttu-id="b951f-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b951f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b951f-116">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="b951f-116">-StatusCode</span></span>
<span data-ttu-id="b951f-117">Dozwolone zakresy kodów stanu dobrej kondycji. Domyślny zakres kodów stanu dobrej kondycji to 200–399</span><span class="sxs-lookup"><span data-stu-id="b951f-117">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

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

### <span data-ttu-id="b951f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b951f-118">CommonParameters</span></span>
<span data-ttu-id="b951f-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b951f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b951f-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b951f-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b951f-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b951f-121">INPUTS</span></span>

### <span data-ttu-id="b951f-122">Brak</span><span class="sxs-lookup"><span data-stu-id="b951f-122">None</span></span>

## <span data-ttu-id="b951f-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b951f-123">OUTPUTS</span></span>

### <span data-ttu-id="b951f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="b951f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="b951f-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b951f-125">NOTES</span></span>

## <span data-ttu-id="b951f-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b951f-126">RELATED LINKS</span></span>
