---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Resize-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Resize-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 9f7b85ed3c8f7c1c64ec89f8575975dde81fed7c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719617"
---
# <span data-ttu-id="b9758-101">Resize-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b9758-101">Resize-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="b9758-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b9758-102">SYNOPSIS</span></span>
<span data-ttu-id="b9758-103">Zmienia rozmiar istniejącej bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b9758-103">Resizes an existing virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9758-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b9758-104">SYNTAX</span></span>

```
Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9758-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b9758-105">DESCRIPTION</span></span>
<span data-ttu-id="b9758-106">Polecenie cmdlet Change **-AzureRmVirtualNetworkGateway** umożliwia zmianę jednostki składowania zapasu (SKU) dla bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b9758-106">The **Resize-AzureRmVirtualNetworkGateway** cmdlet enables you to change the stock-keeping unit (SKU) for a virtual network gateway.</span></span>
<span data-ttu-id="b9758-107">Wersje SKU określają możliwości bramy, w tym takie jak przepływność i Maksymalna liczba dozwolonych tuneli IP.</span><span class="sxs-lookup"><span data-stu-id="b9758-107">SKUs determine the capabilities of a gateway, including such things as throughput and the maximum number of IP tunnels that are allowed.</span></span>
<span data-ttu-id="b9758-108">Platforma Azure obsługuje podstawowe, standardowe, wysoko wydajne, VpnGw1, VpnGw2 i VpnGw3 SKU (czasami nazywane małymi, średnimi i dużymi wersjami SKU).</span><span class="sxs-lookup"><span data-stu-id="b9758-108">Azure supports Basic, Standard, High-Performance, VpnGw1, VpnGw2 and VpnGw3 SKUs (sometimes referred to as Small, Medium, and Large SKUs).</span></span>
<span data-ttu-id="b9758-109">Aby uzyskać szczegółowe informacje o możliwościach poszczególnych typów SKU, zobacz temat https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ .</span><span class="sxs-lookup"><span data-stu-id="b9758-109">For detailed information about the capabilities of each SKU type, see https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/.</span></span>

<span data-ttu-id="b9758-110">Pamiętaj, że jednostki SKU są różne w kalkulacji cen, a także możliwości.</span><span class="sxs-lookup"><span data-stu-id="b9758-110">Keep in mind that SKUs differ in pricing as well as capabilities.</span></span>
<span data-ttu-id="b9758-111">Aby uzyskać więcej informacji, zobacz https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .</span><span class="sxs-lookup"><span data-stu-id="b9758-111">For more information, see https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/.</span></span>

## <span data-ttu-id="b9758-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b9758-112">EXAMPLES</span></span>

### <span data-ttu-id="b9758-113">Przykład 1. Zmienianie rozmiaru bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="b9758-113">Example 1: Change the size of a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

<span data-ttu-id="b9758-114">W tym przykładzie jest zmieniany rozmiar bramy sieci wirtualnej o nazwie ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="b9758-114">This example changes the size of a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="b9758-115">Pierwsze polecenie tworzy odwołanie do obiektu ContosoVirtualGateway; odwołanie do tego obiektu jest przechowywane w zmiennej o nazwie $Gateway.</span><span class="sxs-lookup"><span data-stu-id="b9758-115">The first command creates an object reference to ContosoVirtualGateway; this object reference is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="b9758-116">Drugie polecenie używa polecenia cmdlet **zmiany rozmiaru AzureRmVirtualNetworkGateway** , aby ustawić właściwość *GatewaySku* na podstawową.</span><span class="sxs-lookup"><span data-stu-id="b9758-116">The second command then uses the **Resize-AzureRmVirtualNetworkGateway** cmdlet to set the *GatewaySku* property to Basic.</span></span>

## <span data-ttu-id="b9758-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b9758-117">PARAMETERS</span></span>

### <span data-ttu-id="b9758-118">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="b9758-118">-GatewaySku</span></span>
<span data-ttu-id="b9758-119">Określa nowy typ jednostki SKU bramy.</span><span class="sxs-lookup"><span data-stu-id="b9758-119">Specifies the new type of gateway SKU.</span></span>
<span data-ttu-id="b9758-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b9758-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b9758-121">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="b9758-121">Basic</span></span>
- <span data-ttu-id="b9758-122">Standard</span><span class="sxs-lookup"><span data-stu-id="b9758-122">Standard</span></span>
- <span data-ttu-id="b9758-123">Wysoka wydajność</span><span class="sxs-lookup"><span data-stu-id="b9758-123">High Performance</span></span>
- <span data-ttu-id="b9758-124">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="b9758-124">VpnGw1</span></span>
- <span data-ttu-id="b9758-125">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="b9758-125">VpnGw2</span></span>
- <span data-ttu-id="b9758-126">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="b9758-126">VpnGw3</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9758-127">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b9758-127">-VirtualNetworkGateway</span></span>
<span data-ttu-id="b9758-128">Określa odwołanie do obiektu bramy sieci wirtualnej, którego rozmiar ma zostać zmieniony.</span><span class="sxs-lookup"><span data-stu-id="b9758-128">Specifies an object reference to the virtual network gateway to be resized.</span></span>
<span data-ttu-id="b9758-129">To odwołanie do obiektu można utworzyć przy użyciu Get-AzureRmVirtualNetworkGateway i określając nazwę bramy.</span><span class="sxs-lookup"><span data-stu-id="b9758-129">You can create this object reference by using the Get-AzureRmVirtualNetworkGateway and specifying the name of the gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9758-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9758-130">-DefaultProfile</span></span>
<span data-ttu-id="b9758-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b9758-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9758-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9758-132">CommonParameters</span></span>
<span data-ttu-id="b9758-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9758-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9758-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9758-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9758-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b9758-135">INPUTS</span></span>

###  
<span data-ttu-id="b9758-136">To polecenie cmdlet akceptuje potokowe wystąpienia obiektu **Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="b9758-136">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="b9758-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b9758-137">OUTPUTS</span></span>

###  
<span data-ttu-id="b9758-138">To polecenie cmdlet modyfikuje istniejące wystąpienia obiektu **Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="b9758-138">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="b9758-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b9758-139">NOTES</span></span>
<span data-ttu-id="b9758-140">Nie można zmienić rozmiaru podstawowego/standardowego/HighPerformance SKU na nowy VpnGw1/VpnGw2/VpnGw3 SKU.</span><span class="sxs-lookup"><span data-stu-id="b9758-140">You cannot resize from Basic/Standard/HighPerformance SKUs to the new VpnGw1/VpnGw2/VpnGw3 SKUs.</span></span> <span data-ttu-id="b9758-141">Zobacz https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways instrukcje.</span><span class="sxs-lookup"><span data-stu-id="b9758-141">See https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways for instructions.</span></span>

## <span data-ttu-id="b9758-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b9758-142">RELATED LINKS</span></span>

[<span data-ttu-id="b9758-143">Get-AzureRmVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="b9758-143">Get-AzureRmVpnClientPackage</span></span>](./Get-AzureRmVpnClientPackage.md)

[<span data-ttu-id="b9758-144">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b9758-144">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="b9758-145">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="b9758-145">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md)


