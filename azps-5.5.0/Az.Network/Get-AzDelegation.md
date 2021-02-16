---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDelegation.md
ms.openlocfilehash: f32b06e9b162a4d142d6d6fff9b7cdca34e0b30b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189794"
---
# <span data-ttu-id="ed2f9-101">Get-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="ed2f9-101">Get-AzDelegation</span></span>

## <span data-ttu-id="ed2f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed2f9-102">SYNOPSIS</span></span>
<span data-ttu-id="ed2f9-103">Uzyskiwanie delegowania (lub wszystkich delegowania) w danej podsieci.</span><span class="sxs-lookup"><span data-stu-id="ed2f9-103">Get a delegation (or all of the delegations) on a given subnet.</span></span>

## <span data-ttu-id="ed2f9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ed2f9-104">SYNTAX</span></span>

```
Get-AzDelegation [-Name <String>] -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ed2f9-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ed2f9-105">DESCRIPTION</span></span>
<span data-ttu-id="ed2f9-106">Polecenie **cmdlet Get-AzDelegation** pobiera nazwaną delegowanie z podsieci.</span><span class="sxs-lookup"><span data-stu-id="ed2f9-106">The **Get-AzDelegation** cmdlet gets the named delegation from a subnet.</span></span> <span data-ttu-id="ed2f9-107">Jeśli nie zostanie nazwana żadna delegowanie, funkcja zwraca wszystkie delegowanie w podanej podsieci.</span><span class="sxs-lookup"><span data-stu-id="ed2f9-107">If no delegation is named, it returns all of the delegations on the provided subnet.</span></span>

## <span data-ttu-id="ed2f9-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ed2f9-108">EXAMPLES</span></span>

### <span data-ttu-id="ed2f9-109">1. Pobieranie określonej delegowania</span><span class="sxs-lookup"><span data-stu-id="ed2f9-109">1: Retrieving a specific delegation</span></span>
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

<span data-ttu-id="ed2f9-110">Pierwszy wiersz pobiera zainteresowaną podsieci.</span><span class="sxs-lookup"><span data-stu-id="ed2f9-110">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="ed2f9-111">Drugi wiersz zawiera informacje dotyczące delegowania o nazwie "mojaDelegacja".</span><span class="sxs-lookup"><span data-stu-id="ed2f9-111">The second line shows the delegation information for the delegation called "myDelegation."</span></span>

### <span data-ttu-id="ed2f9-112">2. Pobieranie wszystkich delegowania podsieci</span><span class="sxs-lookup"><span data-stu-id="ed2f9-112">2: Retrieving all subnet delegations</span></span>
```powershell
PS C:\> $subnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> $delegations = Get-AzDelegation -Subnet $subnet
```

<span data-ttu-id="ed2f9-113">Pierwszy wiersz pobiera zainteresowaną podsieci.</span><span class="sxs-lookup"><span data-stu-id="ed2f9-113">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="ed2f9-114">Drugi wiersz zawiera listę wszystkich delegowania w _mojej_ podsieci w $delegations zmienną.</span><span class="sxs-lookup"><span data-stu-id="ed2f9-114">The second line stores a list of all of the delegations on _mySubnet_ in the $delegations variable.</span></span>

## <span data-ttu-id="ed2f9-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed2f9-115">PARAMETERS</span></span>

### <span data-ttu-id="ed2f9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed2f9-116">-DefaultProfile</span></span>
<span data-ttu-id="ed2f9-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ed2f9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed2f9-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ed2f9-118">-Name</span></span>
<span data-ttu-id="ed2f9-119">Nazwa delegowania</span><span class="sxs-lookup"><span data-stu-id="ed2f9-119">The name of the delegation</span></span>

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

### <span data-ttu-id="ed2f9-120">-Subnet</span><span class="sxs-lookup"><span data-stu-id="ed2f9-120">-Subnet</span></span>
<span data-ttu-id="ed2f9-121">Podsieci</span><span class="sxs-lookup"><span data-stu-id="ed2f9-121">The subnet</span></span>

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

### <span data-ttu-id="ed2f9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed2f9-122">CommonParameters</span></span>
<span data-ttu-id="ed2f9-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed2f9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed2f9-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed2f9-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed2f9-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed2f9-125">INPUTS</span></span>

### <span data-ttu-id="ed2f9-126">System.String</span><span class="sxs-lookup"><span data-stu-id="ed2f9-126">System.String</span></span>

### <span data-ttu-id="ed2f9-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="ed2f9-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="ed2f9-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ed2f9-128">OUTPUTS</span></span>

### <span data-ttu-id="ed2f9-129">Microsoft.Azure.Commands.Network.Models.PSDelegacja</span><span class="sxs-lookup"><span data-stu-id="ed2f9-129">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="ed2f9-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ed2f9-130">NOTES</span></span>

## <span data-ttu-id="ed2f9-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ed2f9-131">RELATED LINKS</span></span>

<span data-ttu-id="ed2f9-132">[Add-azDelegation](./Add-AzDelegation.md) 
 [New-AzDelegation](./New-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)</span><span class="sxs-lookup"><span data-stu-id="ed2f9-132">[Add-AzDelegation](./Add-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)</span></span>
