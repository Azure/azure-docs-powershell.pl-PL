---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeering.md
ms.openlocfilehash: 58ba131ab0bebc65d8fd5259d24b2846da229721
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053456"
---
# <span data-ttu-id="a67c0-101">Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="a67c0-101">Get-AzPeering</span></span>

## <span data-ttu-id="a67c0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a67c0-102">SYNOPSIS</span></span>
<span data-ttu-id="a67c0-103">Pobiera zasoby równorzędne dla subskrypcji</span><span class="sxs-lookup"><span data-stu-id="a67c0-103">Gets the Peering Resources for a subscription</span></span>

## <span data-ttu-id="a67c0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a67c0-104">SYNTAX</span></span>

### <span data-ttu-id="a67c0-105">BySubscription (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a67c0-105">BySubscription (Default)</span></span>
```
Get-AzPeering [-Kind <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a67c0-106">ByResourceGroupAndName</span><span class="sxs-lookup"><span data-stu-id="a67c0-106">ByResourceGroupAndName</span></span>
```
Get-AzPeering [-ResourceGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a67c0-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a67c0-107">ByResourceId</span></span>
```
Get-AzPeering [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a67c0-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a67c0-108">DESCRIPTION</span></span>
<span data-ttu-id="a67c0-109">Umożliwia pobieranie elementów równorzędnych z subskrypcji, grupy zasobów lub nazwy.</span><span class="sxs-lookup"><span data-stu-id="a67c0-109">Gets the Peerings from a subscription, resource group, or by name.</span></span>

## <span data-ttu-id="a67c0-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a67c0-110">EXAMPLES</span></span>

### <span data-ttu-id="a67c0-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a67c0-111">Example 1</span></span>
```powershell
PS C:> Get-AzPeering

Name              : myExchangePeering1
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {99999}
PeerAsn.Id        : /subscriptions/providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions/resourceGroups/test/providers/Microsoft.Peering/peerings/myExchangePeering1
Type              : Microsoft.Peering/peerings
Tags              : {}

Name                 : ContosoSeattlePeering
Sku                  : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringSku
Kind                 : Direct
Connections          : {99999}
UseForPeeringService : False
PeerAsn              : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSSubResource
PeeringLocation      : Seattle
ProvisioningState    : Succeeded
Location             : centralus
Id                   : /subscriptions/resourceGroups/testCarrier/providers/Microsoft.Peering/peerings/ContosoSeattlePeering
Type                 : Microsoft.Peering/peerings
Tags                 : {}
```

<span data-ttu-id="a67c0-112">Pobiera wszystkie zasoby dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a67c0-112">Gets all the resources for the subscription.</span></span>

### <span data-ttu-id="a67c0-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a67c0-113">Example 2</span></span>
```powershell
PS C:> Get-AzPeering -ResourceGroupName test -Name myExchangePeering1

Name              : myExchangePeering1
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {99999}
PeerAsn.Id        : /subscriptions/providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions/resourceGroups/test/providers/Microsoft.Peering/peerings/myExchangePeering1
Type              : Microsoft.Peering/peerings
Tags              : {}
```

<span data-ttu-id="a67c0-114">Pobiera wymianę równorzędną programu Exchange o nazwie `myExchangePeering1`</span><span class="sxs-lookup"><span data-stu-id="a67c0-114">Gets the Exchange peering named `myExchangePeering1`</span></span>

### <span data-ttu-id="a67c0-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a67c0-115">Example 2</span></span>
```powershell
PS C:> Get-AzPeering -ResourceId $resourceId

Name              : myExchangePeering1
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {99999}
PeerAsn.Id        : /subscriptions/providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions/resourceGroups/test/providers/Microsoft.Peering/peerings/myExchangePeering1
Type              : Microsoft.Peering/peerings
Tags              : {}
```

<span data-ttu-id="a67c0-116">Pobiera obiekty równorzędne programu Exchange nazwane na `myExchangePeering1` podstawie identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="a67c0-116">Gets the Exchange peering named `myExchangePeering1` based on the resource id.</span></span>

## <span data-ttu-id="a67c0-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a67c0-117">PARAMETERS</span></span>

### <span data-ttu-id="a67c0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a67c0-118">-DefaultProfile</span></span>
<span data-ttu-id="a67c0-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a67c0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a67c0-120">-Kind</span><span class="sxs-lookup"><span data-stu-id="a67c0-120">-Kind</span></span>
<span data-ttu-id="a67c0-121">Wyświetla wszystkie zasoby komunikacji równorzędnej według rodzaju.</span><span class="sxs-lookup"><span data-stu-id="a67c0-121">Shows all Peering resource by Kind.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a67c0-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a67c0-122">-Name</span></span>
<span data-ttu-id="a67c0-123">Unikatowa nazwa PSPeering.</span><span class="sxs-lookup"><span data-stu-id="a67c0-123">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a67c0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a67c0-124">-ResourceGroupName</span></span>
<span data-ttu-id="a67c0-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a67c0-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a67c0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a67c0-126">-ResourceId</span></span>
<span data-ttu-id="a67c0-127">Nazwa ciągu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="a67c0-127">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a67c0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a67c0-128">CommonParameters</span></span>
<span data-ttu-id="a67c0-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a67c0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a67c0-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a67c0-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a67c0-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a67c0-131">INPUTS</span></span>

### <span data-ttu-id="a67c0-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a67c0-132">System.String</span></span>

## <span data-ttu-id="a67c0-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a67c0-133">OUTPUTS</span></span>

### <span data-ttu-id="a67c0-134">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeering</span><span class="sxs-lookup"><span data-stu-id="a67c0-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="a67c0-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a67c0-135">NOTES</span></span>

## <span data-ttu-id="a67c0-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a67c0-136">RELATED LINKS</span></span>
