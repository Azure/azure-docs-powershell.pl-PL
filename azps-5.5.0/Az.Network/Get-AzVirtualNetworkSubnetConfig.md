---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: dcc5e688838508e6917a6732b24d7de3b27b2737
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184627"
---
# <span data-ttu-id="dbd34-101">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="dbd34-101">Get-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="dbd34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbd34-102">SYNOPSIS</span></span>
<span data-ttu-id="dbd34-103">Otrzymuje podsieci w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="dbd34-103">Gets a subnet in a virtual network.</span></span>

## <span data-ttu-id="dbd34-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="dbd34-104">SYNTAX</span></span>

### <span data-ttu-id="dbd34-105">GetByVirtualNetwork (domyślne)</span><span class="sxs-lookup"><span data-stu-id="dbd34-105">GetByVirtualNetwork (Default)</span></span>
```
Get-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbd34-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="dbd34-106">GetByResourceId</span></span>
```
Get-AzVirtualNetworkSubnetConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dbd34-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="dbd34-107">DESCRIPTION</span></span>
<span data-ttu-id="dbd34-108">Polecenie **cmdlet Get-AzVirtualNetworkSubnetConfig** pobiera jedną lub więcej konfiguracji podsieci w sieci wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="dbd34-108">The **Get-AzVirtualNetworkSubnetConfig** cmdlet gets one or more subnet configurations in an Azure virtual network.</span></span>

## <span data-ttu-id="dbd34-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="dbd34-109">EXAMPLES</span></span>

### <span data-ttu-id="dbd34-110">1. Uzyskiwanie podsieci w sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="dbd34-110">1: Get a subnet in a virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

<span data-ttu-id="dbd34-111">W tym przykładzie jest grupę zasobów i sieć wirtualną z jedną podsiecią w tej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="dbd34-111">This example creates a resource group and a virtual network with a single subnet in that resource group.</span></span> <span data-ttu-id="dbd34-112">Następnie pobiera dane dotyczące tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="dbd34-112">It then retrieves data about that subnet.</span></span>

## <span data-ttu-id="dbd34-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dbd34-113">PARAMETERS</span></span>

### <span data-ttu-id="dbd34-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbd34-114">-DefaultProfile</span></span>
<span data-ttu-id="dbd34-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="dbd34-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbd34-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="dbd34-116">-Name</span></span>
<span data-ttu-id="dbd34-117">Określa nazwę konfiguracji podsieci, która pobiera to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbd34-117">Specifies the name of the subnet configuration that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByVirtualNetwork
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbd34-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dbd34-118">-ResourceId</span></span>
<span data-ttu-id="dbd34-119">Określa identyfikator zasobu podsieci, do których otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbd34-119">Specifies the resource id of the subnet that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbd34-120">— VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="dbd34-120">-VirtualNetwork</span></span>
<span data-ttu-id="dbd34-121">Określa obiekt **VirtualNetwork** zawierający konfigurację podsieci, która otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbd34-121">Specifies the **VirtualNetwork** object that contains the subnet configuration that this cmdlet gets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: GetByVirtualNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dbd34-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbd34-122">CommonParameters</span></span>
<span data-ttu-id="dbd34-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbd34-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbd34-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbd34-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbd34-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dbd34-125">INPUTS</span></span>

### <span data-ttu-id="dbd34-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="dbd34-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="dbd34-127">System.String</span><span class="sxs-lookup"><span data-stu-id="dbd34-127">System.String</span></span>

## <span data-ttu-id="dbd34-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dbd34-128">OUTPUTS</span></span>

### <span data-ttu-id="dbd34-129">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="dbd34-129">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="dbd34-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="dbd34-130">NOTES</span></span>

## <span data-ttu-id="dbd34-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dbd34-131">RELATED LINKS</span></span>

[<span data-ttu-id="dbd34-132">Add-azVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="dbd34-132">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="dbd34-133">New-azVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="dbd34-133">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="dbd34-134">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="dbd34-134">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="dbd34-135">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="dbd34-135">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
