---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkusage
schema: 2.0.0
ms.openlocfilehash: 24ffdb99efddf22a5e632ac576a4aa8e7db42af6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897941"
---
# <span data-ttu-id="253bb-101">Get-AzureRmNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="253bb-101">Get-AzureRmNetworkUsage</span></span>

## <span data-ttu-id="253bb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="253bb-102">SYNOPSIS</span></span>
<span data-ttu-id="253bb-103">Wyświetlanie użycia sieci dla subskrypcji</span><span class="sxs-lookup"><span data-stu-id="253bb-103">Lists network usages for a subscription</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="253bb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="253bb-104">SYNTAX</span></span>

```
Get-AzureRmNetworkUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="253bb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="253bb-105">DESCRIPTION</span></span>
<span data-ttu-id="253bb-106">Polecenie cmdlet Get-AzureRmNetworkUsage pobiera limity i bieżące użycie zasobów sieciowych.</span><span class="sxs-lookup"><span data-stu-id="253bb-106">The Get-AzureRmNetworkUsage cmdlet gets limits and current usage for Network resources.</span></span>

## <span data-ttu-id="253bb-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="253bb-107">EXAMPLES</span></span>

### <span data-ttu-id="253bb-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="253bb-108">Example 1</span></span>
```
PS C:\> Get-AzureRmNetworkUsage -Location westcentralus

ResourceType : Virtual Networks
CurrentValue : 6
Limit        : 50

ResourceType : Static Public IP Addresses
CurrentValue : 1
Limit        : 20

ResourceType : Network Security Groups
CurrentValue : 2
Limit        : 100

ResourceType : Public IP Addresses
CurrentValue : 6
Limit        : 60

ResourceType : Network Interfaces
CurrentValue : 1
Limit        : 300

ResourceType : Load Balancers
CurrentValue : 1
Limit        : 100

ResourceType : Application Gateways
CurrentValue : 1
Limit        : 50

ResourceType : Route Tables
CurrentValue : 0
Limit        : 100

ResourceType : Route Filters
CurrentValue : 0
Limit        : 1000

ResourceType : Network Watchers
CurrentValue : 1
Limit        : 1

ResourceType : Packet Captures
CurrentValue : 0
Limit        : 10
```

<span data-ttu-id="253bb-109">Pobiera dane użycia zasobów w regionie westcentralus</span><span class="sxs-lookup"><span data-stu-id="253bb-109">Gets resources usage data in westcentralus region</span></span>

## <span data-ttu-id="253bb-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="253bb-110">PARAMETERS</span></span>

### <span data-ttu-id="253bb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="253bb-111">-DefaultProfile</span></span>
<span data-ttu-id="253bb-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="253bb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="253bb-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="253bb-113">-Location</span></span>
<span data-ttu-id="253bb-114">Lokalizacja, w której jest wykonywane zapytanie dotyczące użycia zasobów.</span><span class="sxs-lookup"><span data-stu-id="253bb-114">The location where resource usage is queried.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="253bb-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="253bb-115">CommonParameters</span></span>
<span data-ttu-id="253bb-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="253bb-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="253bb-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="253bb-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="253bb-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="253bb-118">INPUTS</span></span>

### <span data-ttu-id="253bb-119">System. String</span><span class="sxs-lookup"><span data-stu-id="253bb-119">System.String</span></span>

## <span data-ttu-id="253bb-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="253bb-120">OUTPUTS</span></span>

### <span data-ttu-id="253bb-121">Microsoft. Azure. Commands. Network. models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="253bb-121">Microsoft.Azure.Commands.Network.Models.PSUsage</span></span>

## <span data-ttu-id="253bb-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="253bb-122">NOTES</span></span>

## <span data-ttu-id="253bb-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="253bb-123">RELATED LINKS</span></span>

