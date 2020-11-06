---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
ms.openlocfilehash: 22ea0a6a28a24503413fa9b8958002616c03b884
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528010"
---
# <span data-ttu-id="9c5d0-101">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9c5d0-101">Set-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="9c5d0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9c5d0-102">SYNOPSIS</span></span>
<span data-ttu-id="9c5d0-103">Ustawia stan celu dla sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9c5d0-103">Sets the goal state for a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c5d0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9c5d0-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c5d0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9c5d0-105">DESCRIPTION</span></span>
<span data-ttu-id="9c5d0-106">Polecenie cmdlet **Set-AzureRmVirtualNetwork** ustawia stan celu dla sieci wirtualnej usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="9c5d0-106">The **Set-AzureRmVirtualNetwork** cmdlet sets the goal state for an Azure virtual network.</span></span>

## <span data-ttu-id="9c5d0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9c5d0-107">EXAMPLES</span></span>

### <span data-ttu-id="9c5d0-108">1: utworzenie sieci wirtualnej i usunięcie jednej z jej podsieci</span><span class="sxs-lookup"><span data-stu-id="9c5d0-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

Remove-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork

$virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="9c5d0-109">W tym przykładzie przedstawiono tworzenie sieci wirtualnej z dwiema podsieciami.</span><span class="sxs-lookup"><span data-stu-id="9c5d0-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="9c5d0-110">Następnie usuwana jest jedna podsieć z reprezentacji sieci wirtualnej w pamięci.</span><span class="sxs-lookup"><span data-stu-id="9c5d0-110">Then it removes one subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="9c5d0-111">Polecenie cmdlet Set-AzureRmVirtualNetwork jest następnie używane do napisania zmodyfikowanego stanu sieci wirtualnej po stronie usługi.</span><span class="sxs-lookup"><span data-stu-id="9c5d0-111">The Set-AzureRmVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span>

## <span data-ttu-id="9c5d0-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9c5d0-112">PARAMETERS</span></span>

### <span data-ttu-id="9c5d0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9c5d0-113">-AsJob</span></span>
<span data-ttu-id="9c5d0-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9c5d0-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9c5d0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c5d0-115">-DefaultProfile</span></span>
<span data-ttu-id="9c5d0-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9c5d0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c5d0-117">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9c5d0-117">-VirtualNetwork</span></span>
<span data-ttu-id="9c5d0-118">Określa obiekt **VirtualNetwork** reprezentujący stan celu.</span><span class="sxs-lookup"><span data-stu-id="9c5d0-118">Specifies a **VirtualNetwork** object that represents the goal state.</span></span>

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

### <span data-ttu-id="9c5d0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c5d0-119">CommonParameters</span></span>
<span data-ttu-id="9c5d0-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c5d0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c5d0-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c5d0-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c5d0-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9c5d0-122">INPUTS</span></span>

### <span data-ttu-id="9c5d0-123">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9c5d0-123">PSVirtualNetwork</span></span>
<span data-ttu-id="9c5d0-124">Parametr "VirtualNetwork" akceptuje wartość typu "PSVirtualNetwork" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="9c5d0-124">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="9c5d0-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9c5d0-125">OUTPUTS</span></span>

### <span data-ttu-id="9c5d0-126">Microsoft. Azure. Commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9c5d0-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="9c5d0-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9c5d0-127">NOTES</span></span>

## <span data-ttu-id="9c5d0-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9c5d0-128">RELATED LINKS</span></span>

[<span data-ttu-id="9c5d0-129">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9c5d0-129">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="9c5d0-130">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9c5d0-130">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="9c5d0-131">Nowe — AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9c5d0-131">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="9c5d0-132">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9c5d0-132">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)


