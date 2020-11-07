---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/resize-azurermvirtualnetworkgateway
schema: 2.0.0
ms.openlocfilehash: 0a3dea2b706f7efcdc76b48175df225e2974728c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899215"
---
# <span data-ttu-id="1dadd-101">Resize-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1dadd-101">Resize-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="1dadd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1dadd-102">SYNOPSIS</span></span>
<span data-ttu-id="1dadd-103">Zmienia rozmiar istniejącej bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1dadd-103">Resizes an existing virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1dadd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1dadd-104">SYNTAX</span></span>

```
Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1dadd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1dadd-105">DESCRIPTION</span></span>
<span data-ttu-id="1dadd-106">Polecenie cmdlet Change **-AzureRmVirtualNetworkGateway** umożliwia zmianę jednostki składowania zapasu (SKU) dla bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1dadd-106">The **Resize-AzureRmVirtualNetworkGateway** cmdlet enables you to change the stock-keeping unit (SKU) for a virtual network gateway.</span></span>
<span data-ttu-id="1dadd-107">Wersje SKU określają możliwości bramy, w tym takie jak przepływność i Maksymalna liczba dozwolonych tuneli IP.</span><span class="sxs-lookup"><span data-stu-id="1dadd-107">SKUs determine the capabilities of a gateway, including such things as throughput and the maximum number of IP tunnels that are allowed.</span></span>
<span data-ttu-id="1dadd-108">Platforma Azure obsługuje podstawowe, standardowe, wysoko wydajne, VpnGw1, VpnGw2 i VpnGw3 SKU (czasami nazywane małymi, średnimi i dużymi wersjami SKU).</span><span class="sxs-lookup"><span data-stu-id="1dadd-108">Azure supports Basic, Standard, High-Performance, VpnGw1, VpnGw2 and VpnGw3 SKUs (sometimes referred to as Small, Medium, and Large SKUs).</span></span>
<span data-ttu-id="1dadd-109">Aby uzyskać szczegółowe informacje o możliwościach poszczególnych typów SKU, zobacz temat https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ .</span><span class="sxs-lookup"><span data-stu-id="1dadd-109">For detailed information about the capabilities of each SKU type, see https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/.</span></span>

<span data-ttu-id="1dadd-110">Pamiętaj, że jednostki SKU są różne w kalkulacji cen, a także możliwości.</span><span class="sxs-lookup"><span data-stu-id="1dadd-110">Keep in mind that SKUs differ in pricing as well as capabilities.</span></span>
<span data-ttu-id="1dadd-111">Aby uzyskać więcej informacji, zobacz https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .</span><span class="sxs-lookup"><span data-stu-id="1dadd-111">For more information, see https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/.</span></span>

## <span data-ttu-id="1dadd-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1dadd-112">EXAMPLES</span></span>

### <span data-ttu-id="1dadd-113">Przykład 1. Zmienianie rozmiaru bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="1dadd-113">Example 1: Change the size of a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

<span data-ttu-id="1dadd-114">W tym przykładzie jest zmieniany rozmiar bramy sieci wirtualnej o nazwie ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="1dadd-114">This example changes the size of a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="1dadd-115">Pierwsze polecenie tworzy odwołanie do obiektu ContosoVirtualGateway; odwołanie do tego obiektu jest przechowywane w zmiennej o nazwie $Gateway.</span><span class="sxs-lookup"><span data-stu-id="1dadd-115">The first command creates an object reference to ContosoVirtualGateway; this object reference is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="1dadd-116">Drugie polecenie używa polecenia cmdlet **zmiany rozmiaru AzureRmVirtualNetworkGateway** , aby ustawić właściwość *GatewaySku* na podstawową.</span><span class="sxs-lookup"><span data-stu-id="1dadd-116">The second command then uses the **Resize-AzureRmVirtualNetworkGateway** cmdlet to set the *GatewaySku* property to Basic.</span></span>

## <span data-ttu-id="1dadd-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1dadd-117">PARAMETERS</span></span>

### <span data-ttu-id="1dadd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dadd-118">-DefaultProfile</span></span>
<span data-ttu-id="1dadd-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1dadd-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1dadd-120">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="1dadd-120">-GatewaySku</span></span>
<span data-ttu-id="1dadd-121">Określa nowy typ jednostki SKU bramy.</span><span class="sxs-lookup"><span data-stu-id="1dadd-121">Specifies the new type of gateway SKU.</span></span>
<span data-ttu-id="1dadd-122">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="1dadd-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1dadd-123">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="1dadd-123">Basic</span></span>
- <span data-ttu-id="1dadd-124">Standard</span><span class="sxs-lookup"><span data-stu-id="1dadd-124">Standard</span></span>
- <span data-ttu-id="1dadd-125">Wysoka wydajność</span><span class="sxs-lookup"><span data-stu-id="1dadd-125">High Performance</span></span>
- <span data-ttu-id="1dadd-126">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="1dadd-126">VpnGw1</span></span>
- <span data-ttu-id="1dadd-127">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="1dadd-127">VpnGw2</span></span>
- <span data-ttu-id="1dadd-128">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="1dadd-128">VpnGw3</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dadd-129">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1dadd-129">-VirtualNetworkGateway</span></span>
<span data-ttu-id="1dadd-130">Określa odwołanie do obiektu bramy sieci wirtualnej, którego rozmiar ma zostać zmieniony.</span><span class="sxs-lookup"><span data-stu-id="1dadd-130">Specifies an object reference to the virtual network gateway to be resized.</span></span>
<span data-ttu-id="1dadd-131">To odwołanie do obiektu można utworzyć przy użyciu Get-AzureRmVirtualNetworkGateway i określając nazwę bramy.</span><span class="sxs-lookup"><span data-stu-id="1dadd-131">You can create this object reference by using the Get-AzureRmVirtualNetworkGateway and specifying the name of the gateway.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1dadd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dadd-132">CommonParameters</span></span>
<span data-ttu-id="1dadd-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dadd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dadd-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dadd-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dadd-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1dadd-135">INPUTS</span></span>

###  
<span data-ttu-id="1dadd-136">To polecenie cmdlet akceptuje potokowe wystąpienia obiektu **Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="1dadd-136">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="1dadd-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1dadd-137">OUTPUTS</span></span>

###  
<span data-ttu-id="1dadd-138">To polecenie cmdlet modyfikuje istniejące wystąpienia obiektu **Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="1dadd-138">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="1dadd-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1dadd-139">NOTES</span></span>
<span data-ttu-id="1dadd-140">Nie można zmienić rozmiaru podstawowego/standardowego/HighPerformance SKU na nowy VpnGw1/VpnGw2/VpnGw3 SKU.</span><span class="sxs-lookup"><span data-stu-id="1dadd-140">You cannot resize from Basic/Standard/HighPerformance SKUs to the new VpnGw1/VpnGw2/VpnGw3 SKUs.</span></span> <span data-ttu-id="1dadd-141">Zobacz https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways instrukcje.</span><span class="sxs-lookup"><span data-stu-id="1dadd-141">See https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways for instructions.</span></span>

## <span data-ttu-id="1dadd-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1dadd-142">RELATED LINKS</span></span>

[<span data-ttu-id="1dadd-143">Get-AzureRmVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="1dadd-143">Get-AzureRmVpnClientPackage</span></span>](./Get-AzureRmVpnClientPackage.md)

[<span data-ttu-id="1dadd-144">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1dadd-144">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="1dadd-145">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="1dadd-145">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md)


