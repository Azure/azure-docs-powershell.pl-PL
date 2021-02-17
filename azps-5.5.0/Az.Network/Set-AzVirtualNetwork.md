---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetwork.md
ms.openlocfilehash: 023d50aaf32d894722e2167737703d24776a1fd5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193338"
---
# <span data-ttu-id="75cf3-101">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="75cf3-101">Set-AzVirtualNetwork</span></span>

## <span data-ttu-id="75cf3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75cf3-102">SYNOPSIS</span></span>
<span data-ttu-id="75cf3-103">Aktualizuje sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="75cf3-103">Updates a virtual network.</span></span>

## <span data-ttu-id="75cf3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="75cf3-104">SYNTAX</span></span>

```
Set-AzVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="75cf3-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="75cf3-105">DESCRIPTION</span></span>
<span data-ttu-id="75cf3-106">Polecenie **cmdlet Set-AzVirtualNetwork** aktualizuje sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="75cf3-106">The **Set-AzVirtualNetwork** cmdlet updates a virtual network.</span></span>

## <span data-ttu-id="75cf3-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="75cf3-107">EXAMPLES</span></span>

### <span data-ttu-id="75cf3-108">1. Tworzy sieć wirtualną i usuwa jedną z jej podsieci</span><span class="sxs-lookup"><span data-stu-id="75cf3-108">1: Creates a virtual network and removes one of its subnets</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus ## Create resource group 
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" ## Create frontend subnet 
$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24" ## Create backend subnet

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup `
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet ## Create virtual network

Remove-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork ## Remove subnet from in memory representation of virtual network

$virtualNetwork | Set-AzVirtualNetwork ## Remove subnet from virtual network
```

<span data-ttu-id="75cf3-109">W tym przykładzie jest wana sieć wirtualna o nazwie TestResourceGroup z dwiema podsieciami: frontendSubnet i backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="75cf3-109">This example creates a virtual network called TestResourceGroup with two subnets: frontendSubnet and backendSubnet.</span></span> <span data-ttu-id="75cf3-110">Następnie usuwa podsieci podsieci wewnętrznej (BackendSubnet) z reprezentacji w pamięci sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="75cf3-110">Then it removes backendSubnet subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="75cf3-111">To Set-AzVirtualNetwork cmdlet służy do pisania zmodyfikowanego stanu sieci wirtualnej po stronie usługi.</span><span class="sxs-lookup"><span data-stu-id="75cf3-111">The Set-AzVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span> <span data-ttu-id="75cf3-112">Po wykonaniu Set-AzVirtualNetwork cmdlet zostanie usunięta podsieć backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="75cf3-112">When the Set-AzVirtualNetwork cmdlet is executed, the backendSubnet is removed.</span></span>

## <span data-ttu-id="75cf3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75cf3-113">PARAMETERS</span></span>

### <span data-ttu-id="75cf3-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="75cf3-114">-AsJob</span></span>
<span data-ttu-id="75cf3-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="75cf3-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="75cf3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75cf3-116">-DefaultProfile</span></span>
<span data-ttu-id="75cf3-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="75cf3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75cf3-118">— VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="75cf3-118">-VirtualNetwork</span></span>
<span data-ttu-id="75cf3-119">Określa obiekt sieci wirtualnej reprezentujący stan, dla którego należy ustawić sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="75cf3-119">Specifies a virtual network object representing the state to which the virtual network should be set.</span></span>

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

### <span data-ttu-id="75cf3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75cf3-120">CommonParameters</span></span>
<span data-ttu-id="75cf3-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75cf3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75cf3-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75cf3-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75cf3-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="75cf3-123">INPUTS</span></span>

### <span data-ttu-id="75cf3-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="75cf3-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="75cf3-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="75cf3-125">OUTPUTS</span></span>

### <span data-ttu-id="75cf3-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="75cf3-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="75cf3-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="75cf3-127">NOTES</span></span>

## <span data-ttu-id="75cf3-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="75cf3-128">RELATED LINKS</span></span>

[<span data-ttu-id="75cf3-129">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="75cf3-129">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="75cf3-130">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="75cf3-130">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="75cf3-131">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="75cf3-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="75cf3-132">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="75cf3-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)


