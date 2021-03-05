---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
ms.openlocfilehash: abc97b0473353a0bc71aae59386bc5b5770b730b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980794"
---
# <span data-ttu-id="621a2-101">New-AzCosmosDBVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="621a2-101">New-AzCosmosDBVirtualNetworkRule</span></span>

## <span data-ttu-id="621a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="621a2-102">SYNOPSIS</span></span>
<span data-ttu-id="621a2-103">Utwórz nowy obiekt AADB VirtualNetworkRule Object(PSVirtualNetworkRule).</span><span class="sxs-lookup"><span data-stu-id="621a2-103">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="621a2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="621a2-104">SYNTAX</span></span>

```
New-AzCosmosDBVirtualNetworkRule -Id <String> [-IgnoreMissingVNetServiceEndpoint <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="621a2-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="621a2-105">DESCRIPTION</span></span>
<span data-ttu-id="621a2-106">Utwórz nowy obiekt ANETSDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span><span class="sxs-lookup"><span data-stu-id="621a2-106">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="621a2-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="621a2-107">EXAMPLES</span></span>

### <span data-ttu-id="621a2-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="621a2-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBVirtualNetworkRule -Id {id} -IgnoreMissingVNetServiceEndpoint 0
Id  IgnoreMissingVNetServiceEndpoint
--   --------------------------------
{id}                            False
```

## <span data-ttu-id="621a2-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="621a2-109">PARAMETERS</span></span>

### <span data-ttu-id="621a2-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="621a2-110">-DefaultProfile</span></span>
<span data-ttu-id="621a2-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="621a2-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="621a2-112">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="621a2-112">-Id</span></span>
<span data-ttu-id="621a2-113">Identyfikator zasobu podsieci, na przykład: /subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}</span><span class="sxs-lookup"><span data-stu-id="621a2-113">Resource ID of a subnet, for example: /subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="621a2-114">-IgnoreMissingVNetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="621a2-114">-IgnoreMissingVNetServiceEndpoint</span></span>
<span data-ttu-id="621a2-115">Wartość logiczna wskazująca, czy utworzyć regułę zapory, zanim sieć wirtualna będzie mieć włączony punkt końcowy usługi vnet.</span><span class="sxs-lookup"><span data-stu-id="621a2-115">Boolean to indicate if to create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="621a2-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="621a2-116">CommonParameters</span></span>
<span data-ttu-id="621a2-117">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="621a2-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="621a2-118">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="621a2-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="621a2-119">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="621a2-119">INPUTS</span></span>

### <span data-ttu-id="621a2-120">Brak</span><span class="sxs-lookup"><span data-stu-id="621a2-120">None</span></span>

## <span data-ttu-id="621a2-121">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="621a2-121">OUTPUTS</span></span>

### <span data-ttu-id="621a2-122">Microsoft.Azure.Commands.DoceńDB.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="621a2-122">Microsoft.Azure.Commands.CosmosDB.Models.PSVirtualNetworkRule</span></span>

## <span data-ttu-id="621a2-123">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="621a2-123">NOTES</span></span>

## <span data-ttu-id="621a2-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="621a2-124">RELATED LINKS</span></span>
