---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47FE9EF4-6000-4096-8F04-26A0C6661FDB
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: c820d44ed8c3d32feb3f1d63d2b52a487c27f0dd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005969"
---
# <span data-ttu-id="5b5ec-101">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5b5ec-101">Remove-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="5b5ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b5ec-102">SYNOPSIS</span></span>
<span data-ttu-id="5b5ec-103">Usuwa konfigurację podsieci z sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5b5ec-103">Removes a subnet configuration from a virtual network.</span></span>

## <span data-ttu-id="5b5ec-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5b5ec-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b5ec-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5b5ec-105">DESCRIPTION</span></span>
<span data-ttu-id="5b5ec-106">Polecenie **cmdlet Remove-AzVirtualNetworkSubnetConfig** usuwa podsieci z sieci wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5b5ec-106">The **Remove-AzVirtualNetworkSubnetConfig** cmdlet removes a subnet from an Azure virtual network.</span></span>

## <span data-ttu-id="5b5ec-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5b5ec-107">EXAMPLES</span></span>

### <span data-ttu-id="5b5ec-108">1. Usuwanie podsieci z sieci wirtualnej i aktualizowanie sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="5b5ec-108">1: Remove a subnet from a virtual network and update the virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet 
    $frontendSubnet,$backendSubnet

Remove-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork 
    $virtualNetwork
    $virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="5b5ec-109">W tym przykładzie jest grupę zasobów i sieć wirtualną z dwiema podsieciami.</span><span class="sxs-lookup"><span data-stu-id="5b5ec-109">This example creates a resource group and a virtual network with two subnets.</span></span> <span data-ttu-id="5b5ec-110">Następnie używa polecenia Remove-AzVirtualNetworkSubnetConfig w celu usunięcia podsieci wewnętrznej z reprezentacji w pamięci sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5b5ec-110">It then uses the Remove-AzVirtualNetworkSubnetConfig command to remove the backend subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="5b5ec-111">Set-AzVirtualNetwork jest wywoływana w celu zmodyfikowania sieci wirtualnej po stronie serwera.</span><span class="sxs-lookup"><span data-stu-id="5b5ec-111">Set-AzVirtualNetwork is then called to modify the virtual network on the server side.</span></span>

## <span data-ttu-id="5b5ec-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b5ec-112">PARAMETERS</span></span>

### <span data-ttu-id="5b5ec-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b5ec-113">-DefaultProfile</span></span>
<span data-ttu-id="5b5ec-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5b5ec-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b5ec-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5b5ec-115">-Name</span></span>
<span data-ttu-id="5b5ec-116">Określa nazwę konfiguracji podsieci do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="5b5ec-116">Specifies the name of the subnet configuration to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b5ec-117">— VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5b5ec-117">-VirtualNetwork</span></span>
<span data-ttu-id="5b5ec-118">Określa obiekt **VirtualNetwork** zawierający konfigurację podsieci do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="5b5ec-118">Specifies the **VirtualNetwork** object that contains the subnet configuration to remove.</span></span>

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

### <span data-ttu-id="5b5ec-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b5ec-119">CommonParameters</span></span>
<span data-ttu-id="5b5ec-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b5ec-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b5ec-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters] http://go.microsoft.com/fwlink/?LinkID=113216) (.</span><span class="sxs-lookup"><span data-stu-id="5b5ec-121">For more information, see [about_CommonParameters] (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b5ec-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5b5ec-122">INPUTS</span></span>

### <span data-ttu-id="5b5ec-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5b5ec-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="5b5ec-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5b5ec-124">OUTPUTS</span></span>

### <span data-ttu-id="5b5ec-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5b5ec-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="5b5ec-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5b5ec-126">NOTES</span></span>

## <span data-ttu-id="5b5ec-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5b5ec-127">RELATED LINKS</span></span>

[<span data-ttu-id="5b5ec-128">Add-azVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5b5ec-128">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="5b5ec-129">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5b5ec-129">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="5b5ec-130">New-azVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5b5ec-130">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="5b5ec-131">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5b5ec-131">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)


