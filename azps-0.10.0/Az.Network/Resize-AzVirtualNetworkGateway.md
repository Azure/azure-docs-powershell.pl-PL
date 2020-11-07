---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/resize-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
ms.openlocfilehash: bd42d7cec30b7d42dcb1cdb3657f6681bf2cb6b0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892877"
---
# <span data-ttu-id="9cec2-101">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9cec2-101">Resize-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="9cec2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9cec2-102">SYNOPSIS</span></span>
<span data-ttu-id="9cec2-103">Zmienia rozmiar istniejącej bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9cec2-103">Resizes an existing virtual network gateway.</span></span>

## <span data-ttu-id="9cec2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9cec2-104">SYNTAX</span></span>

```
Resize-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9cec2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9cec2-105">DESCRIPTION</span></span>
<span data-ttu-id="9cec2-106">Polecenie cmdlet Change **-AzVirtualNetworkGateway** umożliwia zmianę jednostki składowania zapasu (SKU) dla bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9cec2-106">The **Resize-AzVirtualNetworkGateway** cmdlet enables you to change the stock-keeping unit (SKU) for a virtual network gateway.</span></span>
<span data-ttu-id="9cec2-107">Wersje SKU określają możliwości bramy, w tym takie jak przepływność i Maksymalna liczba dozwolonych tuneli IP.</span><span class="sxs-lookup"><span data-stu-id="9cec2-107">SKUs determine the capabilities of a gateway, including such things as throughput and the maximum number of IP tunnels that are allowed.</span></span>
<span data-ttu-id="9cec2-108">Platforma Azure obsługuje podstawowe, standardowe, wysoko wydajne, VpnGw1, VpnGw2 i VpnGw3 SKU (czasami nazywane małymi, średnimi i dużymi wersjami SKU).</span><span class="sxs-lookup"><span data-stu-id="9cec2-108">Azure supports Basic, Standard, High-Performance, VpnGw1, VpnGw2 and VpnGw3 SKUs (sometimes referred to as Small, Medium, and Large SKUs).</span></span>
<span data-ttu-id="9cec2-109">Aby uzyskać szczegółowe informacje o możliwościach poszczególnych typów SKU, zobacz temat https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ .</span><span class="sxs-lookup"><span data-stu-id="9cec2-109">For detailed information about the capabilities of each SKU type, see https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/.</span></span>

<span data-ttu-id="9cec2-110">Pamiętaj, że jednostki SKU są różne w kalkulacji cen, a także możliwości.</span><span class="sxs-lookup"><span data-stu-id="9cec2-110">Keep in mind that SKUs differ in pricing as well as capabilities.</span></span>
<span data-ttu-id="9cec2-111">Aby uzyskać więcej informacji, zobacz https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .</span><span class="sxs-lookup"><span data-stu-id="9cec2-111">For more information, see https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/.</span></span>

## <span data-ttu-id="9cec2-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9cec2-112">EXAMPLES</span></span>

### <span data-ttu-id="9cec2-113">Przykład 1. Zmienianie rozmiaru bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="9cec2-113">Example 1: Change the size of a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

<span data-ttu-id="9cec2-114">W tym przykładzie jest zmieniany rozmiar bramy sieci wirtualnej o nazwie ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="9cec2-114">This example changes the size of a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="9cec2-115">Pierwsze polecenie tworzy odwołanie do obiektu ContosoVirtualGateway; odwołanie do tego obiektu jest przechowywane w zmiennej o nazwie $Gateway.</span><span class="sxs-lookup"><span data-stu-id="9cec2-115">The first command creates an object reference to ContosoVirtualGateway; this object reference is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="9cec2-116">Drugie polecenie używa polecenia cmdlet **zmiany rozmiaru AzVirtualNetworkGateway** , aby ustawić właściwość *GatewaySku* na podstawową.</span><span class="sxs-lookup"><span data-stu-id="9cec2-116">The second command then uses the **Resize-AzVirtualNetworkGateway** cmdlet to set the *GatewaySku* property to Basic.</span></span>

## <span data-ttu-id="9cec2-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9cec2-117">PARAMETERS</span></span>

### <span data-ttu-id="9cec2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cec2-118">-DefaultProfile</span></span>
<span data-ttu-id="9cec2-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9cec2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9cec2-120">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="9cec2-120">-GatewaySku</span></span>
<span data-ttu-id="9cec2-121">Określa nowy typ jednostki SKU bramy.</span><span class="sxs-lookup"><span data-stu-id="9cec2-121">Specifies the new type of gateway SKU.</span></span>
<span data-ttu-id="9cec2-122">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="9cec2-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9cec2-123">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="9cec2-123">Basic</span></span>
- <span data-ttu-id="9cec2-124">Standard</span><span class="sxs-lookup"><span data-stu-id="9cec2-124">Standard</span></span>
- <span data-ttu-id="9cec2-125">Wysoka wydajność</span><span class="sxs-lookup"><span data-stu-id="9cec2-125">High Performance</span></span>
- <span data-ttu-id="9cec2-126">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="9cec2-126">VpnGw1</span></span>
- <span data-ttu-id="9cec2-127">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="9cec2-127">VpnGw2</span></span>
- <span data-ttu-id="9cec2-128">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="9cec2-128">VpnGw3</span></span>

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

### <span data-ttu-id="9cec2-129">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9cec2-129">-VirtualNetworkGateway</span></span>
<span data-ttu-id="9cec2-130">Określa odwołanie do obiektu bramy sieci wirtualnej, którego rozmiar ma zostać zmieniony.</span><span class="sxs-lookup"><span data-stu-id="9cec2-130">Specifies an object reference to the virtual network gateway to be resized.</span></span>
<span data-ttu-id="9cec2-131">To odwołanie do obiektu można utworzyć przy użyciu Get-AzVirtualNetworkGateway i określając nazwę bramy.</span><span class="sxs-lookup"><span data-stu-id="9cec2-131">You can create this object reference by using the Get-AzVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="9cec2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cec2-132">CommonParameters</span></span>
<span data-ttu-id="9cec2-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cec2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cec2-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cec2-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cec2-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9cec2-135">INPUTS</span></span>

###  
<span data-ttu-id="9cec2-136">To polecenie cmdlet akceptuje potokowe wystąpienia obiektu **Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="9cec2-136">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="9cec2-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9cec2-137">OUTPUTS</span></span>

###  
<span data-ttu-id="9cec2-138">To polecenie cmdlet modyfikuje istniejące wystąpienia obiektu **Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="9cec2-138">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="9cec2-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9cec2-139">NOTES</span></span>
<span data-ttu-id="9cec2-140">Nie można zmienić rozmiaru podstawowego/standardowego/HighPerformance SKU na nowy VpnGw1/VpnGw2/VpnGw3 SKU.</span><span class="sxs-lookup"><span data-stu-id="9cec2-140">You cannot resize from Basic/Standard/HighPerformance SKUs to the new VpnGw1/VpnGw2/VpnGw3 SKUs.</span></span> <span data-ttu-id="9cec2-141">Zobacz https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways instrukcje.</span><span class="sxs-lookup"><span data-stu-id="9cec2-141">See https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways for instructions.</span></span>

## <span data-ttu-id="9cec2-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9cec2-142">RELATED LINKS</span></span>

[<span data-ttu-id="9cec2-143">Get-AzVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="9cec2-143">Get-AzVpnClientPackage</span></span>](./Get-AzVpnClientPackage.md)

[<span data-ttu-id="9cec2-144">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9cec2-144">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="9cec2-145">Set-AzVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="9cec2-145">Set-AzVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)


