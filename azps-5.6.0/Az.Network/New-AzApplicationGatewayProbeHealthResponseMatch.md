---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayprobehealthresponsematch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
ms.openlocfilehash: 04da18bcd50fa547f1a59142682c93b4e3e5ab62
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974785"
---
# <span data-ttu-id="579f6-101">New-AzApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="579f6-101">New-AzApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="579f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="579f6-102">SYNOPSIS</span></span>
<span data-ttu-id="579f6-103">Tworzy dopasowanie odpowiedzi kondycji używane przez kondycję bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="579f6-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="579f6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="579f6-104">SYNTAX</span></span>

```
New-AzApplicationGatewayProbeHealthResponseMatch [-Body <String>] [-StatusCode <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="579f6-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="579f6-105">DESCRIPTION</span></span>
<span data-ttu-id="579f6-106">**Polecenie cmdlet Add-AzApplicationGatewayProbeHealthResponseMatch** tworzy dopasowanie odpowiedzi kondycji używane przez kondycję bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="579f6-106">**The Add-AzApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="579f6-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="579f6-107">EXAMPLES</span></span>

### <span data-ttu-id="579f6-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="579f6-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="579f6-109">To polecenie tworzy dopasowanie odpowiedzi kondycji, które może zostać przekazane do konfiguracji danych w parametrze.</span><span class="sxs-lookup"><span data-stu-id="579f6-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="579f6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="579f6-110">PARAMETERS</span></span>

### <span data-ttu-id="579f6-111">— Treść</span><span class="sxs-lookup"><span data-stu-id="579f6-111">-Body</span></span>
<span data-ttu-id="579f6-112">Treść, która musi być zawarta w odpowiedzi na stan zdrowia.</span><span class="sxs-lookup"><span data-stu-id="579f6-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="579f6-113">Wartość domyślna jest pusta</span><span class="sxs-lookup"><span data-stu-id="579f6-113">Default value is empty</span></span>

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

### <span data-ttu-id="579f6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="579f6-114">-DefaultProfile</span></span>
<span data-ttu-id="579f6-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="579f6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="579f6-116">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="579f6-116">-StatusCode</span></span>
<span data-ttu-id="579f6-117">Dozwolone zakresy kodów stanu dobrej kondycji. Domyślny zakres kodów stanu dobrej kondycji to 200–399</span><span class="sxs-lookup"><span data-stu-id="579f6-117">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

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

### <span data-ttu-id="579f6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="579f6-118">CommonParameters</span></span>
<span data-ttu-id="579f6-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="579f6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="579f6-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="579f6-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="579f6-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="579f6-121">INPUTS</span></span>

### <span data-ttu-id="579f6-122">Brak</span><span class="sxs-lookup"><span data-stu-id="579f6-122">None</span></span>

## <span data-ttu-id="579f6-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="579f6-123">OUTPUTS</span></span>

### <span data-ttu-id="579f6-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="579f6-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="579f6-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="579f6-125">NOTES</span></span>

## <span data-ttu-id="579f6-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="579f6-126">RELATED LINKS</span></span>
