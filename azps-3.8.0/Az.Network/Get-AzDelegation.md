---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDelegation.md
ms.openlocfilehash: 213c6616a143f7be64454f6538fac5d5c89afd54
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053834"
---
# <span data-ttu-id="33290-101">Get-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="33290-101">Get-AzDelegation</span></span>

## <span data-ttu-id="33290-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="33290-102">SYNOPSIS</span></span>
<span data-ttu-id="33290-103">Uzyskaj delegację (lub wszystkie delegacje) w danej podsieci.</span><span class="sxs-lookup"><span data-stu-id="33290-103">Get a delegation (or all of the delegations) on a given subnet.</span></span>

## <span data-ttu-id="33290-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="33290-104">SYNTAX</span></span>

```
Get-AzDelegation [-Name <String>] -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="33290-105">Opis</span><span class="sxs-lookup"><span data-stu-id="33290-105">DESCRIPTION</span></span>
<span data-ttu-id="33290-106">Polecenie cmdlet **Get-AzDelegation** pobiera nazwane delegowanie z podsieci.</span><span class="sxs-lookup"><span data-stu-id="33290-106">The **Get-AzDelegation** cmdlet gets the named delegation from a subnet.</span></span> <span data-ttu-id="33290-107">Jeśli żadna delegacja nie jest określona, zwróci wszystkie delegacje w podanej podsieci.</span><span class="sxs-lookup"><span data-stu-id="33290-107">If no delegation is named, it returns all of the delegations on the provided subnet.</span></span>

## <span data-ttu-id="33290-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="33290-108">EXAMPLES</span></span>

### <span data-ttu-id="33290-109">1: pobieranie określonej delegacji</span><span class="sxs-lookup"><span data-stu-id="33290-109">1: Retrieving a specific delegation</span></span>
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

<span data-ttu-id="33290-110">Pierwszy wiersz pobiera dodaną sieć.</span><span class="sxs-lookup"><span data-stu-id="33290-110">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="33290-111">W drugim wierszu są wyświetlane informacje o delegowaniu dla delegowania o nazwie "Moja delegacja".</span><span class="sxs-lookup"><span data-stu-id="33290-111">The second line shows the delegation information for the delegation called "myDelegation."</span></span>

### <span data-ttu-id="33290-112">2: pobieranie wszystkich delegowań podsieci</span><span class="sxs-lookup"><span data-stu-id="33290-112">2: Retrieving all subnet delegations</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> $delegations = Get-AzDelegation -Subnet $subnet
```

<span data-ttu-id="33290-113">Pierwszy wiersz pobiera dodaną sieć.</span><span class="sxs-lookup"><span data-stu-id="33290-113">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="33290-114">W drugim wierszu jest przechowywana lista wszystkich delegowań w _Podsieciie_ w zmiennej $delegations.</span><span class="sxs-lookup"><span data-stu-id="33290-114">The second line stores a list of all of the delegations on _mySubnet_ in the $delegations variable.</span></span>

## <span data-ttu-id="33290-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="33290-115">PARAMETERS</span></span>

### <span data-ttu-id="33290-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33290-116">-DefaultProfile</span></span>
<span data-ttu-id="33290-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="33290-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33290-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="33290-118">-Name</span></span>
<span data-ttu-id="33290-119">Imię i nazwisko delegacji</span><span class="sxs-lookup"><span data-stu-id="33290-119">The name of the delegation</span></span>

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

### <span data-ttu-id="33290-120">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="33290-120">-Subnet</span></span>
<span data-ttu-id="33290-121">Podsieć</span><span class="sxs-lookup"><span data-stu-id="33290-121">The subnet</span></span>

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

### <span data-ttu-id="33290-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33290-122">CommonParameters</span></span>
<span data-ttu-id="33290-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33290-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33290-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="33290-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33290-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="33290-125">INPUTS</span></span>

### <span data-ttu-id="33290-126">System. String</span><span class="sxs-lookup"><span data-stu-id="33290-126">System.String</span></span>

### <span data-ttu-id="33290-127">Microsoft. Azure. Commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="33290-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="33290-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="33290-128">OUTPUTS</span></span>

### <span data-ttu-id="33290-129">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="33290-129">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="33290-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="33290-130">NOTES</span></span>

## <span data-ttu-id="33290-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="33290-131">RELATED LINKS</span></span>

<span data-ttu-id="33290-132">[Dodaj-AzDelegation](./Add-AzDelegation.md) 
 [Nowe — AzDelegation](./New-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)</span><span class="sxs-lookup"><span data-stu-id="33290-132">[Add-AzDelegation](./Add-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)</span></span>