---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetwork
schema: 2.0.0
ms.openlocfilehash: 40f84388caed0d332c36ee398e842ae00f2f353f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897849"
---
# <span data-ttu-id="cf340-101">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cf340-101">Set-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="cf340-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cf340-102">SYNOPSIS</span></span>
<span data-ttu-id="cf340-103">Ustawia stan celu dla sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="cf340-103">Sets the goal state for a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf340-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cf340-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf340-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cf340-105">DESCRIPTION</span></span>
<span data-ttu-id="cf340-106">Polecenie cmdlet **Set-AzureRmVirtualNetwork** ustawia stan celu dla sieci wirtualnej usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="cf340-106">The **Set-AzureRmVirtualNetwork** cmdlet sets the goal state for an Azure virtual network.</span></span>

## <span data-ttu-id="cf340-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cf340-107">EXAMPLES</span></span>

### <span data-ttu-id="cf340-108">1: utworzenie sieci wirtualnej i usunięcie jednej z jej podsieci</span><span class="sxs-lookup"><span data-stu-id="cf340-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

Remove-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork

$virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="cf340-109">W tym przykładzie przedstawiono tworzenie sieci wirtualnej z dwiema podsieciami.</span><span class="sxs-lookup"><span data-stu-id="cf340-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="cf340-110">Następnie usuwana jest jedna podsieć z reprezentacji sieci wirtualnej w pamięci.</span><span class="sxs-lookup"><span data-stu-id="cf340-110">Then it removes one subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="cf340-111">Polecenie cmdlet Set-AzureRmVirtualNetwork jest następnie używane do napisania zmodyfikowanego stanu sieci wirtualnej po stronie usługi.</span><span class="sxs-lookup"><span data-stu-id="cf340-111">The Set-AzureRmVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span>

## <span data-ttu-id="cf340-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cf340-112">PARAMETERS</span></span>

### <span data-ttu-id="cf340-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cf340-113">-AsJob</span></span>
<span data-ttu-id="cf340-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="cf340-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf340-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf340-115">-DefaultProfile</span></span>
<span data-ttu-id="cf340-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cf340-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf340-117">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cf340-117">-VirtualNetwork</span></span>
<span data-ttu-id="cf340-118">Określa obiekt **VirtualNetwork** reprezentujący stan celu.</span><span class="sxs-lookup"><span data-stu-id="cf340-118">Specifies a **VirtualNetwork** object that represents the goal state.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf340-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf340-119">CommonParameters</span></span>
<span data-ttu-id="cf340-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf340-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf340-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf340-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf340-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cf340-122">INPUTS</span></span>

### <span data-ttu-id="cf340-123">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cf340-123">PSVirtualNetwork</span></span>
<span data-ttu-id="cf340-124">Parametr "VirtualNetwork" akceptuje wartość typu "PSVirtualNetwork" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="cf340-124">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="cf340-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cf340-125">OUTPUTS</span></span>

### <span data-ttu-id="cf340-126">Microsoft. Azure. Commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cf340-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="cf340-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cf340-127">NOTES</span></span>

## <span data-ttu-id="cf340-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cf340-128">RELATED LINKS</span></span>

[<span data-ttu-id="cf340-129">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cf340-129">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="cf340-130">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cf340-130">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="cf340-131">Nowe — AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cf340-131">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="cf340-132">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cf340-132">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)


