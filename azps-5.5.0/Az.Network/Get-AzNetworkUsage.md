---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkUsage.md
ms.openlocfilehash: e02527c0f206607ae778d6447e65a1c93c620b02
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193811"
---
# <span data-ttu-id="55903-101">Get-AzNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="55903-101">Get-AzNetworkUsage</span></span>

## <span data-ttu-id="55903-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55903-102">SYNOPSIS</span></span>
<span data-ttu-id="55903-103">Lista użycia sieci dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="55903-103">Lists network usages for a subscription</span></span>

## <span data-ttu-id="55903-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="55903-104">SYNTAX</span></span>

```
Get-AzNetworkUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55903-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="55903-105">DESCRIPTION</span></span>
<span data-ttu-id="55903-106">Polecenie Get-AzNetworkUsage pobiera limity i bieżące użycie zasobów sieciowych.</span><span class="sxs-lookup"><span data-stu-id="55903-106">The Get-AzNetworkUsage cmdlet gets limits and current usage for Network resources.</span></span>

## <span data-ttu-id="55903-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="55903-107">EXAMPLES</span></span>

### <span data-ttu-id="55903-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="55903-108">Example 1</span></span>
```
PS C:\> Get-AzNetworkUsage -Location westcentralus

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

<span data-ttu-id="55903-109">Pobiera dane użycia zasobów w regionie westcentralus</span><span class="sxs-lookup"><span data-stu-id="55903-109">Gets resources usage data in westcentralus region</span></span>

## <span data-ttu-id="55903-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55903-110">PARAMETERS</span></span>

### <span data-ttu-id="55903-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55903-111">-DefaultProfile</span></span>
<span data-ttu-id="55903-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="55903-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55903-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="55903-113">-Location</span></span>
<span data-ttu-id="55903-114">Lokalizacja, do której jest ponawiane zapytanie dotyczące użycia zasobu.</span><span class="sxs-lookup"><span data-stu-id="55903-114">The location where resource usage is queried.</span></span>

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

### <span data-ttu-id="55903-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55903-115">CommonParameters</span></span>
<span data-ttu-id="55903-116">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55903-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55903-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55903-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55903-118">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="55903-118">INPUTS</span></span>

### <span data-ttu-id="55903-119">System.String</span><span class="sxs-lookup"><span data-stu-id="55903-119">System.String</span></span>

## <span data-ttu-id="55903-120">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="55903-120">OUTPUTS</span></span>

### <span data-ttu-id="55903-121">Microsoft.Azure.Commands.Network.Models.PSUsage</span><span class="sxs-lookup"><span data-stu-id="55903-121">Microsoft.Azure.Commands.Network.Models.PSUsage</span></span>

## <span data-ttu-id="55903-122">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="55903-122">NOTES</span></span>

## <span data-ttu-id="55903-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="55903-123">RELATED LINKS</span></span>
