---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDelegation.md
ms.openlocfilehash: cbb560b04219b0a77c9158afe3b76b1b9461cdb1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967946"
---
# <span data-ttu-id="e0ccb-101">Get-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="e0ccb-101">Get-AzDelegation</span></span>

## <span data-ttu-id="e0ccb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0ccb-102">SYNOPSIS</span></span>
<span data-ttu-id="e0ccb-103">Uzyskiwanie delegowania (lub wszystkich delegowania) w danej podsieci.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-103">Get a delegation (or all of the delegations) on a given subnet.</span></span>

## <span data-ttu-id="e0ccb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e0ccb-104">SYNTAX</span></span>

```
Get-AzDelegation [-Name <String>] -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e0ccb-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e0ccb-105">DESCRIPTION</span></span>
<span data-ttu-id="e0ccb-106">Polecenie **cmdlet Get-AzDelegation** pobiera nazwaną delegowanie z podsieci.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-106">The **Get-AzDelegation** cmdlet gets the named delegation from a subnet.</span></span> <span data-ttu-id="e0ccb-107">Jeśli nie zostanie nazwana żadna nazwa delegowania, funkcja zwraca wszystkie delegowanie w podanej podsieci.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-107">If no delegation is named, it returns all of the delegations on the provided subnet.</span></span>

## <span data-ttu-id="e0ccb-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e0ccb-108">EXAMPLES</span></span>

### <span data-ttu-id="e0ccb-109">1. Pobieranie określonej delegowania</span><span class="sxs-lookup"><span data-stu-id="e0ccb-109">1: Retrieving a specific delegation</span></span>
```powershell
PS C:\> $subnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> Get-AzDelegation -Name "myDelegation" -Subnet $subnet

ProvisioningState : Succeeded
ServiceName       : Microsoft.Sql/servers
Actions           : {}
Name              : myDelegation
Etag              : "thisisaguid"
Id                : /subscriptions/subId/resourceGroups/rg/providers/Microsoft.Network/virtualNetworks/myvnet/subnets/mySubnet/delegations/myDelegation
```

<span data-ttu-id="e0ccb-110">Pierwszy wiersz pobiera zainteresowaną podsieci.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-110">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="e0ccb-111">Drugi wiersz zawiera informacje dotyczące delegowania o nazwie "mojaDelegacja".</span><span class="sxs-lookup"><span data-stu-id="e0ccb-111">The second line shows the delegation information for the delegation called "myDelegation."</span></span>

### <span data-ttu-id="e0ccb-112">2. Pobieranie wszystkich delegowania podsieci</span><span class="sxs-lookup"><span data-stu-id="e0ccb-112">2: Retrieving all subnet delegations</span></span>
```powershell
PS C:\> $subnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> $delegations = Get-AzDelegation -Subnet $subnet
```

<span data-ttu-id="e0ccb-113">Pierwszy wiersz pobiera zainteresowaną podsieci.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-113">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="e0ccb-114">Drugi wiersz zawiera listę wszystkich delegowania w _mojejubnetu_ w $delegations zmienną.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-114">The second line stores a list of all of the delegations on _mySubnet_ in the $delegations variable.</span></span>

## <span data-ttu-id="e0ccb-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0ccb-115">PARAMETERS</span></span>

### <span data-ttu-id="e0ccb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0ccb-116">-DefaultProfile</span></span>
<span data-ttu-id="e0ccb-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0ccb-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e0ccb-118">-Name</span></span>
<span data-ttu-id="e0ccb-119">Nazwa delegowania</span><span class="sxs-lookup"><span data-stu-id="e0ccb-119">The name of the delegation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0ccb-120">-Subnet</span><span class="sxs-lookup"><span data-stu-id="e0ccb-120">-Subnet</span></span>
<span data-ttu-id="e0ccb-121">Podsieci</span><span class="sxs-lookup"><span data-stu-id="e0ccb-121">The subnet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0ccb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0ccb-122">CommonParameters</span></span>
<span data-ttu-id="e0ccb-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0ccb-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0ccb-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0ccb-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0ccb-125">INPUTS</span></span>

### <span data-ttu-id="e0ccb-126">System.String</span><span class="sxs-lookup"><span data-stu-id="e0ccb-126">System.String</span></span>

### <span data-ttu-id="e0ccb-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="e0ccb-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="e0ccb-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0ccb-128">OUTPUTS</span></span>

### <span data-ttu-id="e0ccb-129">Microsoft.Azure.Commands.Network.Models.PSDelegacja</span><span class="sxs-lookup"><span data-stu-id="e0ccb-129">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="e0ccb-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e0ccb-130">NOTES</span></span>

## <span data-ttu-id="e0ccb-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e0ccb-131">RELATED LINKS</span></span>

<span data-ttu-id="e0ccb-132">[Add-azDelegation](./Add-AzDelegation.md) 
 [New-AzDelegation](./New-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)</span><span class="sxs-lookup"><span data-stu-id="e0ccb-132">[Add-AzDelegation](./Add-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)</span></span>
