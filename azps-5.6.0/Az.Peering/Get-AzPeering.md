---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeering.md
ms.openlocfilehash: e2827d08d813608dbf3f6f40bc15603d5a5a0d99
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989598"
---
# <span data-ttu-id="17170-101">Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="17170-101">Get-AzPeering</span></span>

## <span data-ttu-id="17170-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17170-102">SYNOPSIS</span></span>
<span data-ttu-id="17170-103">Pobiera zasoby komunikacji równorzędnej dla subskrypcji</span><span class="sxs-lookup"><span data-stu-id="17170-103">Gets the Peering Resources for a subscription</span></span>

## <span data-ttu-id="17170-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="17170-104">SYNTAX</span></span>

### <span data-ttu-id="17170-105">BySubscription (Default)</span><span class="sxs-lookup"><span data-stu-id="17170-105">BySubscription (Default)</span></span>
```
Get-AzPeering [-Kind <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17170-106">ByResourceGroupAndName</span><span class="sxs-lookup"><span data-stu-id="17170-106">ByResourceGroupAndName</span></span>
```
Get-AzPeering [-ResourceGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="17170-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="17170-107">ByResourceId</span></span>
```
Get-AzPeering [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17170-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="17170-108">DESCRIPTION</span></span>
<span data-ttu-id="17170-109">Pobiera komunikacji równorzędne z subskrypcji, grupy zasobów lub według nazwy.</span><span class="sxs-lookup"><span data-stu-id="17170-109">Gets the Peerings from a subscription, resource group, or by name.</span></span>

## <span data-ttu-id="17170-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="17170-110">EXAMPLES</span></span>

### <span data-ttu-id="17170-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="17170-111">Example 1</span></span>
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

<span data-ttu-id="17170-112">Pobiera wszystkie zasoby dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="17170-112">Gets all the resources for the subscription.</span></span>

### <span data-ttu-id="17170-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="17170-113">Example 2</span></span>
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

<span data-ttu-id="17170-114">Nazywa się komunikacja równorzędna programu Exchange `myExchangePeering1`</span><span class="sxs-lookup"><span data-stu-id="17170-114">Gets the Exchange peering named `myExchangePeering1`</span></span>

### <span data-ttu-id="17170-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="17170-115">Example 2</span></span>
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

<span data-ttu-id="17170-116">Pobiera nazwę komunikacji równorzędnej programu Exchange `myExchangePeering1` na podstawie identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="17170-116">Gets the Exchange peering named `myExchangePeering1` based on the resource id.</span></span>

## <span data-ttu-id="17170-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17170-117">PARAMETERS</span></span>

### <span data-ttu-id="17170-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17170-118">-DefaultProfile</span></span>
<span data-ttu-id="17170-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="17170-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17170-120">— Rodzaj</span><span class="sxs-lookup"><span data-stu-id="17170-120">-Kind</span></span>
<span data-ttu-id="17170-121">Pokazuje wszystkie zasoby komunikacji równorzędnej według typu.</span><span class="sxs-lookup"><span data-stu-id="17170-121">Shows all Peering resource by Kind.</span></span>

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

### <span data-ttu-id="17170-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="17170-122">-Name</span></span>
<span data-ttu-id="17170-123">Unikatowa nazwa pliku PSPeering.</span><span class="sxs-lookup"><span data-stu-id="17170-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="17170-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17170-124">-ResourceGroupName</span></span>
<span data-ttu-id="17170-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="17170-125">The resource group name.</span></span>

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

### <span data-ttu-id="17170-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="17170-126">-ResourceId</span></span>
<span data-ttu-id="17170-127">Nazwa ciągu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="17170-127">The resource id string name.</span></span>

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

### <span data-ttu-id="17170-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17170-128">CommonParameters</span></span>
<span data-ttu-id="17170-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17170-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17170-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="17170-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17170-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="17170-131">INPUTS</span></span>

### <span data-ttu-id="17170-132">System.String</span><span class="sxs-lookup"><span data-stu-id="17170-132">System.String</span></span>

## <span data-ttu-id="17170-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="17170-133">OUTPUTS</span></span>

### <span data-ttu-id="17170-134">Microsoft.Azure.PowerShell.Cmdlet.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="17170-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="17170-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="17170-135">NOTES</span></span>

## <span data-ttu-id="17170-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="17170-136">RELATED LINKS</span></span>
