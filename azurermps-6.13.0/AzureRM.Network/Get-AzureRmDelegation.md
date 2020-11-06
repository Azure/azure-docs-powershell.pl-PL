---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmDelegation.md
ms.openlocfilehash: f3e8ef97ab618df37ba7d5adae107d65676ed29f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550279"
---
# <span data-ttu-id="5ba83-101">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="5ba83-101">Get-AzureRmDelegation</span></span>

## <span data-ttu-id="5ba83-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5ba83-102">SYNOPSIS</span></span>
<span data-ttu-id="5ba83-103">Uzyskaj delegację (lub wszystkie delegacje) w danej podsieci.</span><span class="sxs-lookup"><span data-stu-id="5ba83-103">Get a delegation (or all of the delegations) on a given subnet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ba83-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5ba83-104">SYNTAX</span></span>

```
Get-AzureRmDelegation [-Name <String>] -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5ba83-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5ba83-105">DESCRIPTION</span></span>
<span data-ttu-id="5ba83-106">Polecenie cmdlet **Get-AzureRmDelegation** pobiera nazwane delegowanie z podsieci.</span><span class="sxs-lookup"><span data-stu-id="5ba83-106">The **Get-AzureRmDelegation** cmdlet gets the named delegation from a subnet.</span></span> <span data-ttu-id="5ba83-107">Jeśli żadna delegacja nie jest określona, zwróci wszystkie delegacje w podanej podsieci.</span><span class="sxs-lookup"><span data-stu-id="5ba83-107">If no delegation is named, it returns all of the delegations on the provided subnet.</span></span>

## <span data-ttu-id="5ba83-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5ba83-108">EXAMPLES</span></span>

### <span data-ttu-id="5ba83-109">1: pobieranie określonej delegacji</span><span class="sxs-lookup"><span data-stu-id="5ba83-109">1: Retrieving a specific delegation</span></span>
```powershell
PS C:\> $subnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> Get-AzureRmDelegation -Name "myDelegation" -Subnet $subnet

ProvisioningState : Succeeded
ServiceName       : Microsoft.Sql/servers
Actions           : {}
Name              : myDelegation
Etag              : "thisisaguid"
Id                : /subscriptions/subId/resourceGroups/rg/providers/Microsoft.Network/virtualNetworks/myvnet/subnets/mySubnet/delegations/myDelegation
```

<span data-ttu-id="5ba83-110">Pierwszy wiersz pobiera dodaną sieć.</span><span class="sxs-lookup"><span data-stu-id="5ba83-110">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="5ba83-111">W drugim wierszu są wyświetlane informacje o delegowaniu dla delegowania o nazwie "Moja delegacja".</span><span class="sxs-lookup"><span data-stu-id="5ba83-111">The second line shows the delegation information for the delegation called "myDelegation."</span></span>

### <span data-ttu-id="5ba83-112">2: pobieranie wszystkich delegowań podsieci</span><span class="sxs-lookup"><span data-stu-id="5ba83-112">2: Retrieving all subnet delegations</span></span>
```powershell
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> $delegations = Get-AzureRmDelegation -Subnet $subnet
```

<span data-ttu-id="5ba83-113">Pierwszy wiersz pobiera dodaną sieć.</span><span class="sxs-lookup"><span data-stu-id="5ba83-113">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="5ba83-114">W drugim wierszu jest przechowywana lista wszystkich delegowań w _Podsieciie_ w zmiennej $delegations.</span><span class="sxs-lookup"><span data-stu-id="5ba83-114">The second line stores a list of all of the delegations on _mySubnet_ in the $delegations variable.</span></span>

## <span data-ttu-id="5ba83-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5ba83-115">PARAMETERS</span></span>

### <span data-ttu-id="5ba83-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ba83-116">-DefaultProfile</span></span>
<span data-ttu-id="5ba83-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5ba83-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ba83-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5ba83-118">-Name</span></span>
<span data-ttu-id="5ba83-119">Imię i nazwisko delegacji</span><span class="sxs-lookup"><span data-stu-id="5ba83-119">The name of the delegation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ba83-120">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="5ba83-120">-Subnet</span></span>
<span data-ttu-id="5ba83-121">Podsieć</span><span class="sxs-lookup"><span data-stu-id="5ba83-121">The subnet</span></span>

```yaml
Type: PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ba83-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ba83-122">CommonParameters</span></span>
<span data-ttu-id="5ba83-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ba83-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5ba83-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ba83-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ba83-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ba83-125">INPUTS</span></span>

### <span data-ttu-id="5ba83-126">Microsoft. Azure. Commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="5ba83-126">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="5ba83-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5ba83-127">OUTPUTS</span></span>

### <span data-ttu-id="5ba83-128">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="5ba83-128">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="5ba83-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5ba83-129">NOTES</span></span>

## <span data-ttu-id="5ba83-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ba83-130">RELATED LINKS</span></span>
<span data-ttu-id="5ba83-131">[Dodaj-AzureRmDelegation](./Add-AzureRmDelegation.md) 
 [Nowe — AzureRmDelegation](./New-AzureRmDelegation.md) 
 [Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md) 
 [Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md) 
 [Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)</span><span class="sxs-lookup"><span data-stu-id="5ba83-131">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md)
[New-AzureRmDelegation](./New-AzureRmDelegation.md)
[Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md)
[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)
[Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)</span></span>
