---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
ms.openlocfilehash: 2a81b7bf5420bdbf4fa5252d71c511c7152e47fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543584"
---
# <span data-ttu-id="7adea-101">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7adea-101">Set-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="7adea-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7adea-102">SYNOPSIS</span></span>
<span data-ttu-id="7adea-103">Ustawia stan celu dla sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7adea-103">Sets the goal state for a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7adea-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7adea-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7adea-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7adea-105">DESCRIPTION</span></span>
<span data-ttu-id="7adea-106">Polecenie cmdlet **Set-AzureRmVirtualNetwork** ustawia stan celu dla sieci wirtualnej usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="7adea-106">The **Set-AzureRmVirtualNetwork** cmdlet sets the goal state for an Azure virtual network.</span></span>

## <span data-ttu-id="7adea-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7adea-107">EXAMPLES</span></span>

### <span data-ttu-id="7adea-108">1: utworzenie sieci wirtualnej i usunięcie jednej z jej podsieci</span><span class="sxs-lookup"><span data-stu-id="7adea-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" ## Create resource group
$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24" ## Create backend subnet

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet ## Create virtual network

Remove-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork ## Remove subnet from in memory representation of virtual network

$virtualNetwork | Set-AzureRmVirtualNetwork ## Remove subnet from virtual network
```

<span data-ttu-id="7adea-109">W tym przykładzie przedstawiono tworzenie sieci wirtualnej o nazwie TestResourceGroup z dwiema podsieciami: frontendSubnet i backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="7adea-109">This example creates a virtual network called TestResourceGroup with two subnets: frontendSubnet and backendSubnet.</span></span> <span data-ttu-id="7adea-110">Oznacza to, że podsieć backendSubnet jest usuwana z reprezentacji sieci wirtualnej w pamięci.</span><span class="sxs-lookup"><span data-stu-id="7adea-110">Then it removes backendSubnet subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="7adea-111">Polecenie cmdlet Set-AzureRmVirtualNetwork jest następnie używane do napisania zmodyfikowanego stanu sieci wirtualnej po stronie usługi.</span><span class="sxs-lookup"><span data-stu-id="7adea-111">The Set-AzureRmVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span> <span data-ttu-id="7adea-112">Po wykonaniu polecenia cmdlet Set-AzureRmVirtualNetwork zostanie usunięty backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="7adea-112">When the Set-AzureRmVirtualNetwork cmdlet is executed, the backendSubnet is removed.</span></span>

## <span data-ttu-id="7adea-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7adea-113">PARAMETERS</span></span>

### <span data-ttu-id="7adea-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7adea-114">-AsJob</span></span>
<span data-ttu-id="7adea-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7adea-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7adea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7adea-116">-DefaultProfile</span></span>
<span data-ttu-id="7adea-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7adea-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7adea-118">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7adea-118">-VirtualNetwork</span></span>
<span data-ttu-id="7adea-119">Określa obiekt **VirtualNetwork** reprezentujący stan celu.</span><span class="sxs-lookup"><span data-stu-id="7adea-119">Specifies a **VirtualNetwork** object that represents the goal state.</span></span>

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

### <span data-ttu-id="7adea-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7adea-120">CommonParameters</span></span>
<span data-ttu-id="7adea-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7adea-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7adea-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7adea-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7adea-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7adea-123">INPUTS</span></span>

### <span data-ttu-id="7adea-124">Microsoft. Azure. Commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7adea-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>
<span data-ttu-id="7adea-125">Parametry: VirtualNetwork (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7adea-125">Parameters: VirtualNetwork (ByValue)</span></span>

## <span data-ttu-id="7adea-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7adea-126">OUTPUTS</span></span>

### <span data-ttu-id="7adea-127">Microsoft. Azure. Commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7adea-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="7adea-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7adea-128">NOTES</span></span>

## <span data-ttu-id="7adea-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7adea-129">RELATED LINKS</span></span>

[<span data-ttu-id="7adea-130">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7adea-130">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="7adea-131">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7adea-131">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="7adea-132">Nowe — AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7adea-132">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="7adea-133">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7adea-133">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)


