---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 93b7c79544f79a528fc09203fdae77f8ee76474a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890633"
---
# <span data-ttu-id="7aba1-101">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="7aba1-101">Get-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="7aba1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7aba1-102">SYNOPSIS</span></span>
<span data-ttu-id="7aba1-103">Pobiera podsieć w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7aba1-103">Gets a subnet in a virtual network.</span></span>

## <span data-ttu-id="7aba1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7aba1-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7aba1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7aba1-105">DESCRIPTION</span></span>
<span data-ttu-id="7aba1-106">Polecenie cmdlet **Get-AzVirtualNetworkSubnetConfig umożliwia pobranie** co najmniej jednej konfiguracji podsieci w sieci wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7aba1-106">The **Get-AzVirtualNetworkSubnetConfig** cmdlet gets one or more subnet configurations in an Azure virtual network.</span></span>

## <span data-ttu-id="7aba1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7aba1-107">EXAMPLES</span></span>

### <span data-ttu-id="7aba1-108">1: uzyskiwanie podsieci w sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="7aba1-108">1: Get a subnet in a virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

<span data-ttu-id="7aba1-109">W tym przykładzie jest tworzona Grupa zasobów i Sieć wirtualna z jedną podsiecią w tej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="7aba1-109">This example creates a resource group and a virtual network with a single subnet in that resource group.</span></span> <span data-ttu-id="7aba1-110">Następnie pobiera dane dotyczące tej podsieci.</span><span class="sxs-lookup"><span data-stu-id="7aba1-110">It then retrieves data about that subnet.</span></span>

## <span data-ttu-id="7aba1-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7aba1-111">PARAMETERS</span></span>

### <span data-ttu-id="7aba1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7aba1-112">-DefaultProfile</span></span>
<span data-ttu-id="7aba1-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7aba1-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7aba1-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7aba1-114">-Name</span></span>
<span data-ttu-id="7aba1-115">Określa nazwę konfiguracji podsieci, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7aba1-115">Specifies the name of the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7aba1-116">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7aba1-116">-VirtualNetwork</span></span>
<span data-ttu-id="7aba1-117">Określa obiekt **VirtualNetwork** , który zawiera konfigurację podsieci, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7aba1-117">Specifies the **VirtualNetwork** object that contains the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7aba1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7aba1-118">CommonParameters</span></span>
<span data-ttu-id="7aba1-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7aba1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7aba1-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7aba1-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7aba1-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7aba1-121">INPUTS</span></span>

### <span data-ttu-id="7aba1-122">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7aba1-122">PSVirtualNetwork</span></span>
<span data-ttu-id="7aba1-123">Parametr "VirtualNetwork" akceptuje wartość typu "PSVirtualNetwork" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="7aba1-123">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="7aba1-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7aba1-124">OUTPUTS</span></span>

### <span data-ttu-id="7aba1-125">Microsoft. Azure. Commands. Network. models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="7aba1-125">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="7aba1-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7aba1-126">NOTES</span></span>

## <span data-ttu-id="7aba1-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7aba1-127">RELATED LINKS</span></span>

[<span data-ttu-id="7aba1-128">Dodaj-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="7aba1-128">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="7aba1-129">Nowe — AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="7aba1-129">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="7aba1-130">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="7aba1-130">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="7aba1-131">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="7aba1-131">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)


