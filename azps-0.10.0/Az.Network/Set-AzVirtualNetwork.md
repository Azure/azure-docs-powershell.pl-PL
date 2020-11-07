---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetwork.md
ms.openlocfilehash: dc780e4b05b2f0ccb92f014f658a9b21aa1bd224
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892718"
---
# <span data-ttu-id="4df2c-101">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4df2c-101">Set-AzVirtualNetwork</span></span>

## <span data-ttu-id="4df2c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4df2c-102">SYNOPSIS</span></span>
<span data-ttu-id="4df2c-103">Ustawia stan celu dla sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4df2c-103">Sets the goal state for a virtual network.</span></span>

## <span data-ttu-id="4df2c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4df2c-104">SYNTAX</span></span>

```
Set-AzVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4df2c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4df2c-105">DESCRIPTION</span></span>
<span data-ttu-id="4df2c-106">Polecenie cmdlet **Set-AzVirtualNetwork** ustawia stan celu dla sieci wirtualnej usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="4df2c-106">The **Set-AzVirtualNetwork** cmdlet sets the goal state for an Azure virtual network.</span></span>

## <span data-ttu-id="4df2c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4df2c-107">EXAMPLES</span></span>

### <span data-ttu-id="4df2c-108">1: utworzenie sieci wirtualnej i usunięcie jednej z jej podsieci</span><span class="sxs-lookup"><span data-stu-id="4df2c-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

Remove-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="4df2c-109">W tym przykładzie przedstawiono tworzenie sieci wirtualnej z dwiema podsieciami.</span><span class="sxs-lookup"><span data-stu-id="4df2c-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="4df2c-110">Następnie usuwana jest jedna podsieć z reprezentacji sieci wirtualnej w pamięci.</span><span class="sxs-lookup"><span data-stu-id="4df2c-110">Then it removes one subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="4df2c-111">Polecenie cmdlet Set-AzVirtualNetwork jest następnie używane do napisania zmodyfikowanego stanu sieci wirtualnej po stronie usługi.</span><span class="sxs-lookup"><span data-stu-id="4df2c-111">The Set-AzVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span>

## <span data-ttu-id="4df2c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4df2c-112">PARAMETERS</span></span>

### <span data-ttu-id="4df2c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4df2c-113">-AsJob</span></span>
<span data-ttu-id="4df2c-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="4df2c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4df2c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4df2c-115">-DefaultProfile</span></span>
<span data-ttu-id="4df2c-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4df2c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4df2c-117">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4df2c-117">-VirtualNetwork</span></span>
<span data-ttu-id="4df2c-118">Określa obiekt **VirtualNetwork** reprezentujący stan celu.</span><span class="sxs-lookup"><span data-stu-id="4df2c-118">Specifies a **VirtualNetwork** object that represents the goal state.</span></span>

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

### <span data-ttu-id="4df2c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4df2c-119">CommonParameters</span></span>
<span data-ttu-id="4df2c-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4df2c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4df2c-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4df2c-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4df2c-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4df2c-122">INPUTS</span></span>

### <span data-ttu-id="4df2c-123">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4df2c-123">PSVirtualNetwork</span></span>
<span data-ttu-id="4df2c-124">Parametr "VirtualNetwork" akceptuje wartość typu "PSVirtualNetwork" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="4df2c-124">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="4df2c-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4df2c-125">OUTPUTS</span></span>

### <span data-ttu-id="4df2c-126">Microsoft. Azure. Commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4df2c-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="4df2c-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4df2c-127">NOTES</span></span>

## <span data-ttu-id="4df2c-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4df2c-128">RELATED LINKS</span></span>

[<span data-ttu-id="4df2c-129">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4df2c-129">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="4df2c-130">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4df2c-130">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="4df2c-131">Nowe — AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4df2c-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="4df2c-132">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4df2c-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)


