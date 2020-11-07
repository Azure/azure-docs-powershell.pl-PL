---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprobehealthresponsematch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
ms.openlocfilehash: c98d36e7f08d16f12581c340b875e26f5a393f1b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709361"
---
# <span data-ttu-id="a090d-101">New-AzApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="a090d-101">New-AzApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="a090d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a090d-102">SYNOPSIS</span></span>
<span data-ttu-id="a090d-103">Tworzy dopasowanie odpowiedzi badania kondycji używane przez sondę kondycji dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a090d-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="a090d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a090d-104">SYNTAX</span></span>

```
New-AzApplicationGatewayProbeHealthResponseMatch [-Body <String>] [-StatusCode <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a090d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a090d-105">DESCRIPTION</span></span>
<span data-ttu-id="a090d-106">Polecenie cmdlet **Add-AzApplicationGatewayProbeHealthResponseMatch** powoduje utworzenie dopasowania odpowiedzi badania kondycji, używanej przez sondę kondycji dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a090d-106">**The Add-AzApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="a090d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a090d-107">EXAMPLES</span></span>

### <span data-ttu-id="a090d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a090d-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="a090d-109">To polecenie tworzy zgodność z odpowiedzią na kondycję, która może zostać przekazana do ProbeConfig jako parametr.</span><span class="sxs-lookup"><span data-stu-id="a090d-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="a090d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a090d-110">PARAMETERS</span></span>

### <span data-ttu-id="a090d-111">-Body</span><span class="sxs-lookup"><span data-stu-id="a090d-111">-Body</span></span>
<span data-ttu-id="a090d-112">Treść, która musi być zawarta w odpowiedzi na kondycję.</span><span class="sxs-lookup"><span data-stu-id="a090d-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="a090d-113">Wartość domyślna jest pusta</span><span class="sxs-lookup"><span data-stu-id="a090d-113">Default value is empty</span></span>

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

### <span data-ttu-id="a090d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a090d-114">-DefaultProfile</span></span>
<span data-ttu-id="a090d-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a090d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a090d-116">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="a090d-116">-StatusCode</span></span>
<span data-ttu-id="a090d-117">Dozwolone zakresy kodów statusu w dobrej kondycji. Domyślnym zakresem prawidłowych kodów stanu jest 200-399</span><span class="sxs-lookup"><span data-stu-id="a090d-117">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

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

### <span data-ttu-id="a090d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a090d-118">CommonParameters</span></span>
<span data-ttu-id="a090d-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a090d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a090d-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a090d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a090d-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a090d-121">INPUTS</span></span>

### <span data-ttu-id="a090d-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a090d-122">None</span></span>

## <span data-ttu-id="a090d-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a090d-123">OUTPUTS</span></span>

### <span data-ttu-id="a090d-124">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="a090d-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="a090d-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a090d-125">NOTES</span></span>

## <span data-ttu-id="a090d-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a090d-126">RELATED LINKS</span></span>
