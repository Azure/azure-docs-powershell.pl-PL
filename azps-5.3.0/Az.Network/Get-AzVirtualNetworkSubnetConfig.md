---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: dcc5e688838508e6917a6732b24d7de3b27b2737
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489898"
---
# <span data-ttu-id="d9c62-101">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d9c62-101">Get-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="d9c62-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d9c62-102">SYNOPSIS</span></span>
<span data-ttu-id="d9c62-103">Pobiera podsieć w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d9c62-103">Gets a subnet in a virtual network.</span></span>

## <span data-ttu-id="d9c62-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d9c62-104">SYNTAX</span></span>

### <span data-ttu-id="d9c62-105">GetByVirtualNetwork (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d9c62-105">GetByVirtualNetwork (Default)</span></span>
```
Get-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9c62-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d9c62-106">GetByResourceId</span></span>
```
Get-AzVirtualNetworkSubnetConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d9c62-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d9c62-107">DESCRIPTION</span></span>
<span data-ttu-id="d9c62-108">Polecenie cmdlet **Get-AzVirtualNetworkSubnetConfig umożliwia pobranie** co najmniej jednej konfiguracji podsieci w sieci wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d9c62-108">The **Get-AzVirtualNetworkSubnetConfig** cmdlet gets one or more subnet configurations in an Azure virtual network.</span></span>

## <span data-ttu-id="d9c62-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d9c62-109">EXAMPLES</span></span>

### <span data-ttu-id="d9c62-110">1: uzyskiwanie podsieci w sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="d9c62-110">1: Get a subnet in a virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

<span data-ttu-id="d9c62-111">W tym przykładzie jest tworzona Grupa zasobów i Sieć wirtualna z jedną podsiecią w tej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="d9c62-111">This example creates a resource group and a virtual network with a single subnet in that resource group.</span></span> <span data-ttu-id="d9c62-112">Następnie pobiera dane dotyczące tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="d9c62-112">It then retrieves data about that subnet.</span></span>

## <span data-ttu-id="d9c62-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d9c62-113">PARAMETERS</span></span>

### <span data-ttu-id="d9c62-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9c62-114">-DefaultProfile</span></span>
<span data-ttu-id="d9c62-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d9c62-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9c62-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d9c62-116">-Name</span></span>
<span data-ttu-id="d9c62-117">Określa nazwę konfiguracji podsieci, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9c62-117">Specifies the name of the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d9c62-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9c62-118">-ResourceId</span></span>
<span data-ttu-id="d9c62-119">Określa identyfikator zasobu podsieci, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9c62-119">Specifies the resource id of the subnet that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d9c62-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d9c62-120">-VirtualNetwork</span></span>
<span data-ttu-id="d9c62-121">Określa obiekt **VirtualNetwork** , który zawiera konfigurację podsieci, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9c62-121">Specifies the **VirtualNetwork** object that contains the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d9c62-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9c62-122">CommonParameters</span></span>
<span data-ttu-id="d9c62-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9c62-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9c62-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9c62-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9c62-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9c62-125">INPUTS</span></span>

### <span data-ttu-id="d9c62-126">Microsoft. Azure. Commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d9c62-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="d9c62-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d9c62-127">System.String</span></span>

## <span data-ttu-id="d9c62-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d9c62-128">OUTPUTS</span></span>

### <span data-ttu-id="d9c62-129">Microsoft. Azure. Commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="d9c62-129">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="d9c62-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d9c62-130">NOTES</span></span>

## <span data-ttu-id="d9c62-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d9c62-131">RELATED LINKS</span></span>

[<span data-ttu-id="d9c62-132">Dodaj-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d9c62-132">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="d9c62-133">Nowe — AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d9c62-133">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="d9c62-134">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d9c62-134">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="d9c62-135">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d9c62-135">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
