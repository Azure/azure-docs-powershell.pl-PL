---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetwork.md
ms.openlocfilehash: 822b982b2c1714e2c0331cc9b64fe2c1753044f7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063292"
---
# <span data-ttu-id="03d8b-101">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="03d8b-101">Set-AzVirtualNetwork</span></span>

## <span data-ttu-id="03d8b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="03d8b-102">SYNOPSIS</span></span>
<span data-ttu-id="03d8b-103">Umożliwia zaktualizowanie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="03d8b-103">Updates a virtual network.</span></span>

## <span data-ttu-id="03d8b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="03d8b-104">SYNTAX</span></span>

```
Set-AzVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="03d8b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="03d8b-105">DESCRIPTION</span></span>
<span data-ttu-id="03d8b-106">Polecenie cmdlet **Set-AzVirtualNetwork** umożliwia zaktualizowanie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="03d8b-106">The **Set-AzVirtualNetwork** cmdlet updates a virtual network.</span></span>

## <span data-ttu-id="03d8b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="03d8b-107">EXAMPLES</span></span>

### <span data-ttu-id="03d8b-108">1: utworzenie sieci wirtualnej i usunięcie jednej z jej podsieci</span><span class="sxs-lookup"><span data-stu-id="03d8b-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" ## Create resource group
$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24" ## Create backend subnet

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet ## Create virtual network

Remove-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork ## Remove subnet from in memory representation of virtual network

$virtualNetwork | Set-AzVirtualNetwork ## Remove subnet from virtual network
```

<span data-ttu-id="03d8b-109">W tym przykładzie przedstawiono tworzenie sieci wirtualnej o nazwie TestResourceGroup z dwiema podsieciami: frontendSubnet i backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="03d8b-109">This example creates a virtual network called TestResourceGroup with two subnets: frontendSubnet and backendSubnet.</span></span> <span data-ttu-id="03d8b-110">Oznacza to, że podsieć backendSubnet jest usuwana z reprezentacji sieci wirtualnej w pamięci.</span><span class="sxs-lookup"><span data-stu-id="03d8b-110">Then it removes backendSubnet subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="03d8b-111">Polecenie cmdlet Set-AzVirtualNetwork jest następnie używane do napisania zmodyfikowanego stanu sieci wirtualnej po stronie usługi.</span><span class="sxs-lookup"><span data-stu-id="03d8b-111">The Set-AzVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span> <span data-ttu-id="03d8b-112">Po wykonaniu polecenia cmdlet Set-AzVirtualNetwork zostanie usunięty backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="03d8b-112">When the Set-AzVirtualNetwork cmdlet is executed, the backendSubnet is removed.</span></span>

## <span data-ttu-id="03d8b-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="03d8b-113">PARAMETERS</span></span>

### <span data-ttu-id="03d8b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03d8b-114">-AsJob</span></span>
<span data-ttu-id="03d8b-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="03d8b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="03d8b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03d8b-116">-DefaultProfile</span></span>
<span data-ttu-id="03d8b-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="03d8b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03d8b-118">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="03d8b-118">-VirtualNetwork</span></span>
<span data-ttu-id="03d8b-119">Określa wirtualny obiekt sieciowy reprezentujący stan, do którego powinna być ustawiona Sieć wirtualna.</span><span class="sxs-lookup"><span data-stu-id="03d8b-119">Specifies a virtual network object representing the state to which the virtual network should be set.</span></span>

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

### <span data-ttu-id="03d8b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03d8b-120">CommonParameters</span></span>
<span data-ttu-id="03d8b-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03d8b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03d8b-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03d8b-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03d8b-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03d8b-123">INPUTS</span></span>

### <span data-ttu-id="03d8b-124">Microsoft. Azure. Commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="03d8b-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="03d8b-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="03d8b-125">OUTPUTS</span></span>

### <span data-ttu-id="03d8b-126">Microsoft. Azure. Commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="03d8b-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="03d8b-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="03d8b-127">NOTES</span></span>

## <span data-ttu-id="03d8b-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="03d8b-128">RELATED LINKS</span></span>

[<span data-ttu-id="03d8b-129">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="03d8b-129">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="03d8b-130">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="03d8b-130">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="03d8b-131">Nowe — AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="03d8b-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="03d8b-132">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="03d8b-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)


