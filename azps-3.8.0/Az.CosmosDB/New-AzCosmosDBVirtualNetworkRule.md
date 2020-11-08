---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
ms.openlocfilehash: d60284cec84c1b0a023f06a77acfe794d8d5315f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052594"
---
# <span data-ttu-id="0fbe8-101">New-AzCosmosDBVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="0fbe8-101">New-AzCosmosDBVirtualNetworkRule</span></span>

## <span data-ttu-id="0fbe8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0fbe8-102">SYNOPSIS</span></span>
<span data-ttu-id="0fbe8-103">Utwórz nowy obiekt CosmosDB VirtualNetworkRule (PSVirtualNetworkRule).</span><span class="sxs-lookup"><span data-stu-id="0fbe8-103">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="0fbe8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0fbe8-104">SYNTAX</span></span>

```
New-AzCosmosDBVirtualNetworkRule -Id <String> [-IgnoreMissingVNetServiceEndpoint <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0fbe8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0fbe8-105">DESCRIPTION</span></span>
<span data-ttu-id="0fbe8-106">Utwórz nowy obiekt CosmosDB VirtualNetworkRule (PSVirtualNetworkRule).</span><span class="sxs-lookup"><span data-stu-id="0fbe8-106">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="0fbe8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0fbe8-107">EXAMPLES</span></span>

### <span data-ttu-id="0fbe8-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0fbe8-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBVirtualNetworkRule -Id {id} -IgnoreMissingVNetServiceEndpoint 0
Id  IgnoreMissingVNetServiceEndpoint
--   --------------------------------
{id}                            False
```

## <span data-ttu-id="0fbe8-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0fbe8-109">PARAMETERS</span></span>

### <span data-ttu-id="0fbe8-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fbe8-110">-DefaultProfile</span></span>
<span data-ttu-id="0fbe8-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0fbe8-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fbe8-112">-ID</span><span class="sxs-lookup"><span data-stu-id="0fbe8-112">-Id</span></span>
<span data-ttu-id="0fbe8-113">Identyfikator zasobu podsieci, na przykład:/subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}</span><span class="sxs-lookup"><span data-stu-id="0fbe8-113">Resource ID of a subnet, for example: /subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}</span></span>

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

### <span data-ttu-id="0fbe8-114">-IgnoreMissingVNetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="0fbe8-114">-IgnoreMissingVNetServiceEndpoint</span></span>
<span data-ttu-id="0fbe8-115">Wartość logiczna wskazująca, czy należy utworzyć regułę zapory, zanim Sieć wirtualna ma włączony punkt końcowy usługi VNET.</span><span class="sxs-lookup"><span data-stu-id="0fbe8-115">Boolean to indicate if to create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="0fbe8-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fbe8-116">CommonParameters</span></span>
<span data-ttu-id="0fbe8-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fbe8-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fbe8-118">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0fbe8-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fbe8-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0fbe8-119">INPUTS</span></span>

### <span data-ttu-id="0fbe8-120">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="0fbe8-120">None</span></span>

## <span data-ttu-id="0fbe8-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0fbe8-121">OUTPUTS</span></span>

### <span data-ttu-id="0fbe8-122">Microsoft. Azure. Commands. CosmosDB. models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="0fbe8-122">Microsoft.Azure.Commands.CosmosDB.Models.PSVirtualNetworkRule</span></span>

## <span data-ttu-id="0fbe8-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0fbe8-123">NOTES</span></span>

## <span data-ttu-id="0fbe8-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0fbe8-124">RELATED LINKS</span></span>
