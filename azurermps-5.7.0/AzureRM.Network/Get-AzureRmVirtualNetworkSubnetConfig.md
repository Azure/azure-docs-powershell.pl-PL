---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 531eab9d8b1405b34a4676cd3e06430cfeda0680
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545576"
---
# <span data-ttu-id="c6006-101">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c6006-101">Get-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="c6006-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c6006-102">SYNOPSIS</span></span>
<span data-ttu-id="c6006-103">Pobiera podsieć w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c6006-103">Gets a subnet in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6006-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c6006-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6006-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c6006-105">DESCRIPTION</span></span>
<span data-ttu-id="c6006-106">Polecenie cmdlet **Get-AzureRmVirtualNetworkSubnetConfig umożliwia pobranie** co najmniej jednej konfiguracji podsieci w sieci wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c6006-106">The **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet gets one or more subnet configurations in an Azure virtual network.</span></span>

## <span data-ttu-id="c6006-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c6006-107">EXAMPLES</span></span>

### <span data-ttu-id="c6006-108">1: uzyskiwanie podsieci w sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="c6006-108">1: Get a subnet in a virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

<span data-ttu-id="c6006-109">W tym przykładzie jest tworzona Grupa zasobów i Sieć wirtualna z jedną podsiecią w tej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="c6006-109">This example creates a resource group and a virtual network with a single subnet in that resource group.</span></span> <span data-ttu-id="c6006-110">Następnie pobiera dane dotyczące tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="c6006-110">It then retrieves data about that subnet.</span></span>

## <span data-ttu-id="c6006-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c6006-111">PARAMETERS</span></span>

### <span data-ttu-id="c6006-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6006-112">-DefaultProfile</span></span>
<span data-ttu-id="c6006-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c6006-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6006-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c6006-114">-Name</span></span>
<span data-ttu-id="c6006-115">Określa nazwę konfiguracji podsieci, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6006-115">Specifies the name of the subnet configuration that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6006-116">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c6006-116">-VirtualNetwork</span></span>
<span data-ttu-id="c6006-117">Określa obiekt **VirtualNetwork** , który zawiera konfigurację podsieci, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6006-117">Specifies the **VirtualNetwork** object that contains the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c6006-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6006-118">CommonParameters</span></span>
<span data-ttu-id="c6006-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6006-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6006-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6006-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6006-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c6006-121">INPUTS</span></span>

### <span data-ttu-id="c6006-122">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c6006-122">PSVirtualNetwork</span></span>
<span data-ttu-id="c6006-123">Parametr "VirtualNetwork" akceptuje wartość typu "PSVirtualNetwork" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="c6006-123">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="c6006-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c6006-124">OUTPUTS</span></span>

### <span data-ttu-id="c6006-125">Microsoft. Azure. Commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="c6006-125">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="c6006-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c6006-126">NOTES</span></span>

## <span data-ttu-id="c6006-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c6006-127">RELATED LINKS</span></span>

[<span data-ttu-id="c6006-128">Dodaj-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c6006-128">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="c6006-129">Nowe — AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c6006-129">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="c6006-130">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c6006-130">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="c6006-131">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c6006-131">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)

