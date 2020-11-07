---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/resize-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
ms.openlocfilehash: b3a468f06db6d75671049b08efcf7970553c5c79
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709040"
---
# <span data-ttu-id="95906-101">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="95906-101">Resize-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="95906-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="95906-102">SYNOPSIS</span></span>
<span data-ttu-id="95906-103">Zmienia rozmiar istniejącej bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="95906-103">Resizes an existing virtual network gateway.</span></span>

## <span data-ttu-id="95906-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="95906-104">SYNTAX</span></span>

```
Resize-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95906-105">Opis</span><span class="sxs-lookup"><span data-stu-id="95906-105">DESCRIPTION</span></span>
<span data-ttu-id="95906-106">Polecenie cmdlet Change **-AzVirtualNetworkGateway** umożliwia zmianę jednostki składowania zapasu (SKU) dla bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="95906-106">The **Resize-AzVirtualNetworkGateway** cmdlet enables you to change the stock-keeping unit (SKU) for a virtual network gateway.</span></span>
<span data-ttu-id="95906-107">Wersje SKU określają możliwości bramy, w tym takie jak przepływność i Maksymalna liczba dozwolonych tuneli IP.</span><span class="sxs-lookup"><span data-stu-id="95906-107">SKUs determine the capabilities of a gateway, including such things as throughput and the maximum number of IP tunnels that are allowed.</span></span>
<span data-ttu-id="95906-108">Platforma Azure obsługuje podstawowe, standardowe, High-Performance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ SKU (czasami nazywane małymi, średnimi i dużymi wersjami SKU).</span><span class="sxs-lookup"><span data-stu-id="95906-108">Azure supports Basic, Standard, High-Performance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ SKUs (sometimes referred to as Small, Medium, and Large SKUs).</span></span>
<span data-ttu-id="95906-109">Aby uzyskać szczegółowe informacje o możliwościach poszczególnych typów SKU, zobacz temat https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ .</span><span class="sxs-lookup"><span data-stu-id="95906-109">For detailed information about the capabilities of each SKU type, see https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/.</span></span>
<span data-ttu-id="95906-110">Pamiętaj, że jednostki SKU są różne w kalkulacji cen, a także możliwości.</span><span class="sxs-lookup"><span data-stu-id="95906-110">Keep in mind that SKUs differ in pricing as well as capabilities.</span></span>
<span data-ttu-id="95906-111">Aby uzyskać więcej informacji, zobacz https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .</span><span class="sxs-lookup"><span data-stu-id="95906-111">For more information, see https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/.</span></span>

## <span data-ttu-id="95906-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="95906-112">EXAMPLES</span></span>

### <span data-ttu-id="95906-113">Przykład 1. Zmienianie rozmiaru bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="95906-113">Example 1: Change the size of a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

<span data-ttu-id="95906-114">W tym przykładzie jest zmieniany rozmiar bramy sieci wirtualnej o nazwie ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="95906-114">This example changes the size of a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="95906-115">Pierwsze polecenie tworzy odwołanie do obiektu ContosoVirtualGateway; odwołanie do tego obiektu jest przechowywane w zmiennej o nazwie $Gateway.</span><span class="sxs-lookup"><span data-stu-id="95906-115">The first command creates an object reference to ContosoVirtualGateway; this object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="95906-116">Drugie polecenie używa polecenia cmdlet **zmiany rozmiaru AzVirtualNetworkGateway** , aby ustawić właściwość *GatewaySku* na podstawową.</span><span class="sxs-lookup"><span data-stu-id="95906-116">The second command then uses the **Resize-AzVirtualNetworkGateway** cmdlet to set the *GatewaySku* property to Basic.</span></span>

## <span data-ttu-id="95906-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="95906-117">PARAMETERS</span></span>

### <span data-ttu-id="95906-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95906-118">-DefaultProfile</span></span>
<span data-ttu-id="95906-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="95906-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95906-120">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="95906-120">-GatewaySku</span></span>
<span data-ttu-id="95906-121">Określa nowy typ jednostki SKU bramy.</span><span class="sxs-lookup"><span data-stu-id="95906-121">Specifies the new type of gateway SKU.</span></span>
<span data-ttu-id="95906-122">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="95906-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="95906-123">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="95906-123">Basic</span></span>
- <span data-ttu-id="95906-124">Standard</span><span class="sxs-lookup"><span data-stu-id="95906-124">Standard</span></span>
- <span data-ttu-id="95906-125">Wysoka wydajność</span><span class="sxs-lookup"><span data-stu-id="95906-125">High Performance</span></span>
- <span data-ttu-id="95906-126">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="95906-126">VpnGw1</span></span>
- <span data-ttu-id="95906-127">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="95906-127">VpnGw2</span></span>
- <span data-ttu-id="95906-128">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="95906-128">VpnGw3</span></span>
- <span data-ttu-id="95906-129">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="95906-129">VpnGw1AZ</span></span> 
- <span data-ttu-id="95906-130">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="95906-130">VpnGw2AZ</span></span> 
- <span data-ttu-id="95906-131">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="95906-131">VpnGw3AZ</span></span> 
- <span data-ttu-id="95906-132">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="95906-132">ErGw1AZ</span></span> 
- <span data-ttu-id="95906-133">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="95906-133">ErGw2AZ</span></span> 
- <span data-ttu-id="95906-134">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="95906-134">ErGw3AZ</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95906-135">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="95906-135">-VirtualNetworkGateway</span></span>
<span data-ttu-id="95906-136">Określa odwołanie do obiektu bramy sieci wirtualnej, którego rozmiar ma zostać zmieniony.</span><span class="sxs-lookup"><span data-stu-id="95906-136">Specifies an object reference to the virtual network gateway to be resized.</span></span>
<span data-ttu-id="95906-137">To odwołanie do obiektu można utworzyć przy użyciu Get-AzVirtualNetworkGateway i określając nazwę bramy.</span><span class="sxs-lookup"><span data-stu-id="95906-137">You can create this object reference by using the Get-AzVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="95906-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95906-138">CommonParameters</span></span>
<span data-ttu-id="95906-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95906-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95906-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95906-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95906-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="95906-141">INPUTS</span></span>

### <span data-ttu-id="95906-142">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="95906-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="95906-143">System. String</span><span class="sxs-lookup"><span data-stu-id="95906-143">System.String</span></span>

## <span data-ttu-id="95906-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="95906-144">OUTPUTS</span></span>

### <span data-ttu-id="95906-145">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="95906-145">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="95906-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="95906-146">NOTES</span></span>
<span data-ttu-id="95906-147">Nie można zmienić rozmiaru podstawowego/standardowego/HighPerformance SKU na nowy VpnGw1/VpnGw2/VpnGw3 SKU.</span><span class="sxs-lookup"><span data-stu-id="95906-147">You cannot resize from Basic/Standard/HighPerformance SKUs to the new VpnGw1/VpnGw2/VpnGw3 SKUs.</span></span> <span data-ttu-id="95906-148">Dalsze zmiany rozmiaru nie są dozwolone z poziomu/do VpnGw1AZ/VpnGw2AZ/VpnGw3AZ lub ErGw1AZ/ErGw2AZ/ErGw3AZ.</span><span class="sxs-lookup"><span data-stu-id="95906-148">Further resize is not allowed from/to VpnGw1AZ/VpnGw2AZ/VpnGw3AZ or ErGw1AZ/ErGw2AZ/ErGw3AZ.</span></span> <span data-ttu-id="95906-149">Zmienianie rozmiaru jest dozwolone tylko w obrębie serii SKU, na przykład zmiany rozmiaru VpnGw1AZ/z VpnGw2AZ/VpnGw3AZ i ErGw1AZ można zmieniać do/z ErGw2AZ/ErGw3AZ.</span><span class="sxs-lookup"><span data-stu-id="95906-149">Resize is allowed only within the SKU 'series' e.g VpnGw1AZ can be resized to/from VpnGw2AZ/VpnGw3AZ and ErGw1AZ can be resized to/from ErGw2AZ/ErGw3AZ.</span></span> <span data-ttu-id="95906-150">Zobacz https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways instrukcje.</span><span class="sxs-lookup"><span data-stu-id="95906-150">See https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways for instructions.</span></span>

## <span data-ttu-id="95906-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="95906-151">RELATED LINKS</span></span>

[<span data-ttu-id="95906-152">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="95906-152">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="95906-153">Nowe — AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="95906-153">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="95906-154">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="95906-154">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="95906-155">Resetowanie — AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="95906-155">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="95906-156">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="95906-156">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)

[<span data-ttu-id="95906-157">Get-AzVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="95906-157">Get-AzVpnClientPackage</span></span>](./Get-AzVpnClientPackage.md)

[<span data-ttu-id="95906-158">Set-AzVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="95906-158">Set-AzVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)
