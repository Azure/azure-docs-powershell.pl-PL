---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkUsage.md
ms.openlocfilehash: c5bb92ad330b49ff015f21ae14fab42d6583305c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553819"
---
# <span data-ttu-id="c2b6f-101">Get-AzureRmNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="c2b6f-101">Get-AzureRmNetworkUsage</span></span>

## <span data-ttu-id="c2b6f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c2b6f-102">SYNOPSIS</span></span>
<span data-ttu-id="c2b6f-103">Wyświetlanie użycia sieci dla subskrypcji</span><span class="sxs-lookup"><span data-stu-id="c2b6f-103">Lists network usages for a subscription</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2b6f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c2b6f-104">SYNTAX</span></span>

```
Get-AzureRmNetworkUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2b6f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c2b6f-105">DESCRIPTION</span></span>
<span data-ttu-id="c2b6f-106">Polecenie cmdlet Get-AzureRmNetworkUsage pobiera limity i bieżące użycie zasobów sieciowych.</span><span class="sxs-lookup"><span data-stu-id="c2b6f-106">The Get-AzureRmNetworkUsage cmdlet gets limits and current usage for Network resources.</span></span>

## <span data-ttu-id="c2b6f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c2b6f-107">EXAMPLES</span></span>

### <span data-ttu-id="c2b6f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c2b6f-108">Example 1</span></span>
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

<span data-ttu-id="c2b6f-109">Pobiera dane użycia zasobów w regionie westcentralus</span><span class="sxs-lookup"><span data-stu-id="c2b6f-109">Gets resources usage data in westcentralus region</span></span>

## <span data-ttu-id="c2b6f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c2b6f-110">PARAMETERS</span></span>

### <span data-ttu-id="c2b6f-111">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c2b6f-111">-Location</span></span>
<span data-ttu-id="c2b6f-112">Lokalizacja, w której jest wykonywane zapytanie dotyczące użycia zasobów.</span><span class="sxs-lookup"><span data-stu-id="c2b6f-112">The location where resource usage is queried.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2b6f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2b6f-113">-DefaultProfile</span></span>
<span data-ttu-id="c2b6f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c2b6f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2b6f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2b6f-115">CommonParameters</span></span>
<span data-ttu-id="c2b6f-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2b6f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2b6f-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2b6f-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2b6f-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2b6f-118">INPUTS</span></span>

### <span data-ttu-id="c2b6f-119">System. String</span><span class="sxs-lookup"><span data-stu-id="c2b6f-119">System.String</span></span>

## <span data-ttu-id="c2b6f-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c2b6f-120">OUTPUTS</span></span>

### <span data-ttu-id="c2b6f-121">Microsoft. Azure. Commands. Network. models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="c2b6f-121">Microsoft.Azure.Commands.Network.Models.PSUsage</span></span>

## <span data-ttu-id="c2b6f-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c2b6f-122">NOTES</span></span>

## <span data-ttu-id="c2b6f-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2b6f-123">RELATED LINKS</span></span>
