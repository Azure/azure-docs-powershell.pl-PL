---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/powershell/module/az.network/set-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetwork.md
ms.openlocfilehash: 1c5a5bc119c481c47c865ca72896b832f3a82b2b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997669"
---
# <span data-ttu-id="e9603-101">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e9603-101">Set-AzVirtualNetwork</span></span>

## <span data-ttu-id="e9603-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9603-102">SYNOPSIS</span></span>
<span data-ttu-id="e9603-103">Aktualizuje sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="e9603-103">Updates a virtual network.</span></span>

## <span data-ttu-id="e9603-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e9603-104">SYNTAX</span></span>

```
Set-AzVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e9603-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e9603-105">DESCRIPTION</span></span>
<span data-ttu-id="e9603-106">Polecenie **cmdlet Set-AzVirtualNetwork** aktualizuje sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="e9603-106">The **Set-AzVirtualNetwork** cmdlet updates a virtual network.</span></span>

## <span data-ttu-id="e9603-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e9603-107">EXAMPLES</span></span>

### <span data-ttu-id="e9603-108">1. Tworzy sieć wirtualną i usuwa jedną z jej podsieci.</span><span class="sxs-lookup"><span data-stu-id="e9603-108">1: Creates a virtual network and removes one of its subnets</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus ## Create resource group 
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" ## Create frontend subnet 
$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24" ## Create backend subnet

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup `
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet ## Create virtual network

Remove-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork ## Remove subnet from in memory representation of virtual network

$virtualNetwork | Set-AzVirtualNetwork ## Remove subnet from virtual network
```

<span data-ttu-id="e9603-109">W tym przykładzie jest wana sieć wirtualna o nazwie TestResourceGroup z dwiema podsieciami: frontendSubnet i backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="e9603-109">This example creates a virtual network called TestResourceGroup with two subnets: frontendSubnet and backendSubnet.</span></span> <span data-ttu-id="e9603-110">Następnie usuwa podsieci podsieci wewnętrznej (BackendSubnet) z reprezentacji w pamięci sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e9603-110">Then it removes backendSubnet subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="e9603-111">To Set-AzVirtualNetwork cmdlet służy do pisania zmodyfikowanego stanu sieci wirtualnej po stronie usługi.</span><span class="sxs-lookup"><span data-stu-id="e9603-111">The Set-AzVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span> <span data-ttu-id="e9603-112">Po wykonaniu Set-AzVirtualNetwork cmdlet zostanie usunięta podsieć backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="e9603-112">When the Set-AzVirtualNetwork cmdlet is executed, the backendSubnet is removed.</span></span>

## <span data-ttu-id="e9603-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9603-113">PARAMETERS</span></span>

### <span data-ttu-id="e9603-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="e9603-114">-AsJob</span></span>
<span data-ttu-id="e9603-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e9603-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9603-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9603-116">-DefaultProfile</span></span>
<span data-ttu-id="e9603-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e9603-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9603-118">— VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e9603-118">-VirtualNetwork</span></span>
<span data-ttu-id="e9603-119">Określa obiekt sieci wirtualnej reprezentujący stan, dla którego należy ustawić sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="e9603-119">Specifies a virtual network object representing the state to which the virtual network should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9603-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9603-120">CommonParameters</span></span>
<span data-ttu-id="e9603-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9603-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9603-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9603-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9603-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e9603-123">INPUTS</span></span>

### <span data-ttu-id="e9603-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e9603-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="e9603-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e9603-125">OUTPUTS</span></span>

### <span data-ttu-id="e9603-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e9603-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="e9603-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e9603-127">NOTES</span></span>

## <span data-ttu-id="e9603-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e9603-128">RELATED LINKS</span></span>

[<span data-ttu-id="e9603-129">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e9603-129">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="e9603-130">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e9603-130">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="e9603-131">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e9603-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="e9603-132">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e9603-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)


