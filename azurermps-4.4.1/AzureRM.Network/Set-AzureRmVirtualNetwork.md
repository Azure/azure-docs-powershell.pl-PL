---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
ms.openlocfilehash: a5158b1c2d1439286295a2f84f7273b37d608161
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553805"
---
# <span data-ttu-id="19652-101">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="19652-101">Set-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="19652-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="19652-102">SYNOPSIS</span></span>
<span data-ttu-id="19652-103">Ustawia stan celu dla sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="19652-103">Sets the goal state for a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19652-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="19652-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="19652-105">Opis</span><span class="sxs-lookup"><span data-stu-id="19652-105">DESCRIPTION</span></span>
<span data-ttu-id="19652-106">Polecenie cmdlet **Set-AzureRmVirtualNetwork** ustawia stan celu dla sieci wirtualnej usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="19652-106">The **Set-AzureRmVirtualNetwork** cmdlet sets the goal state for an Azure virtual network.</span></span>

## <span data-ttu-id="19652-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="19652-107">EXAMPLES</span></span>

### <span data-ttu-id="19652-108">1: utworzenie sieci wirtualnej i usunięcie jednej z jej podsieci</span><span class="sxs-lookup"><span data-stu-id="19652-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

Remove-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork

$virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="19652-109">W tym przykładzie przedstawiono tworzenie sieci wirtualnej z dwiema podsieciami.</span><span class="sxs-lookup"><span data-stu-id="19652-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="19652-110">Następnie usuwana jest jedna podsieć z reprezentacji sieci wirtualnej w pamięci.</span><span class="sxs-lookup"><span data-stu-id="19652-110">Then it removes one subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="19652-111">Polecenie cmdlet Set-AzureRmVirtualNetwork jest następnie używane do napisania zmodyfikowanego stanu sieci wirtualnej po stronie usługi.</span><span class="sxs-lookup"><span data-stu-id="19652-111">The Set-AzureRmVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span>

## <span data-ttu-id="19652-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="19652-112">PARAMETERS</span></span>

### <span data-ttu-id="19652-113">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="19652-113">-VirtualNetwork</span></span>
<span data-ttu-id="19652-114">Określa obiekt **VirtualNetwork** reprezentujący stan celu.</span><span class="sxs-lookup"><span data-stu-id="19652-114">Specifies a **VirtualNetwork** object that represents the goal state.</span></span>

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

### <span data-ttu-id="19652-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19652-115">-DefaultProfile</span></span>
<span data-ttu-id="19652-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="19652-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19652-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19652-117">CommonParameters</span></span>
<span data-ttu-id="19652-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19652-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19652-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19652-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19652-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="19652-120">INPUTS</span></span>

### <span data-ttu-id="19652-121">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="19652-121">PSVirtualNetwork</span></span>
<span data-ttu-id="19652-122">Parametr "VirtualNetwork" akceptuje wartość typu "PSVirtualNetwork" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="19652-122">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="19652-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="19652-123">OUTPUTS</span></span>

### <span data-ttu-id="19652-124">Microsoft. Azure. Commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="19652-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="19652-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="19652-125">NOTES</span></span>

## <span data-ttu-id="19652-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="19652-126">RELATED LINKS</span></span>

[<span data-ttu-id="19652-127">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="19652-127">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="19652-128">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="19652-128">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="19652-129">Nowe — AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="19652-129">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="19652-130">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="19652-130">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)


