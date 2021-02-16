---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/resize-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
ms.openlocfilehash: 31ec0453b0ce64c27d1bb37d4bf6c0f100a8c760
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411759"
---
# <span data-ttu-id="5a53d-101">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5a53d-101">Resize-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="5a53d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a53d-102">SYNOPSIS</span></span>
<span data-ttu-id="5a53d-103">Zmienia rozmiar istniejącej bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5a53d-103">Resizes an existing virtual network gateway.</span></span>

## <span data-ttu-id="5a53d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5a53d-104">SYNTAX</span></span>

```
Resize-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a53d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5a53d-105">DESCRIPTION</span></span>
<span data-ttu-id="5a53d-106">Polecenie cmdlet **Resize-AzVirtualNetworkGateway** umożliwia zmianę jednostki magazynowej (SKU) dla bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5a53d-106">The **Resize-AzVirtualNetworkGateway** cmdlet enables you to change the stock-keeping unit (SKU) for a virtual network gateway.</span></span>
<span data-ttu-id="5a53d-107">Jednostki SKU określają możliwości bramy, w tym przepływność i maksymalną dozwoloną liczbę adresów IP.</span><span class="sxs-lookup"><span data-stu-id="5a53d-107">SKUs determine the capabilities of a gateway, including such things as throughput and the maximum number of IP tunnels that are allowed.</span></span>
<span data-ttu-id="5a53d-108">Platforma Azure obsługuje jednostki SKU Basic, Standard, High-Performance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ (czasami określane mianem małych, średnich i dużych jednostki SKU).</span><span class="sxs-lookup"><span data-stu-id="5a53d-108">Azure supports Basic, Standard, High-Performance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ SKUs (sometimes referred to as Small, Medium, and Large SKUs).</span></span>
<span data-ttu-id="5a53d-109">Aby uzyskać szczegółowe informacje na temat możliwości poszczególnych typów sKU, https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ zobacz.</span><span class="sxs-lookup"><span data-stu-id="5a53d-109">For detailed information about the capabilities of each SKU type, see https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/.</span></span>
<span data-ttu-id="5a53d-110">Pamiętaj, że ceny i możliwości aplikacji różnią się w poszczególnych cenach.</span><span class="sxs-lookup"><span data-stu-id="5a53d-110">Keep in mind that SKUs differ in pricing as well as capabilities.</span></span>
<span data-ttu-id="5a53d-111">Aby uzyskać więcej informacji, zobacz https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .</span><span class="sxs-lookup"><span data-stu-id="5a53d-111">For more information, see https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/.</span></span>

## <span data-ttu-id="5a53d-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5a53d-112">EXAMPLES</span></span>

### <span data-ttu-id="5a53d-113">Przykład 1. Zmienianie rozmiaru bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="5a53d-113">Example 1: Change the size of a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

<span data-ttu-id="5a53d-114">W tym przykładzie zmienia się rozmiar bramy sieci wirtualnej o nazwie ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="5a53d-114">This example changes the size of a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="5a53d-115">Pierwsze polecenie tworzy odwołanie do obiektu ContosoVirtualGateway. to odwołanie do obiektu jest przechowywane w zmiennej o nazwie $Gateway.</span><span class="sxs-lookup"><span data-stu-id="5a53d-115">The first command creates an object reference to ContosoVirtualGateway; this object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="5a53d-116">Drugie polecenie używa następnie polecenia cmdlet **Resize-AzVirtualNetworkGateway** w celu ustawienia właściwości *GatewaySku* na Wartość Podstawowa.</span><span class="sxs-lookup"><span data-stu-id="5a53d-116">The second command then uses the **Resize-AzVirtualNetworkGateway** cmdlet to set the *GatewaySku* property to Basic.</span></span>

## <span data-ttu-id="5a53d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a53d-117">PARAMETERS</span></span>

### <span data-ttu-id="5a53d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a53d-118">-DefaultProfile</span></span>
<span data-ttu-id="5a53d-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5a53d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a53d-120">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="5a53d-120">-GatewaySku</span></span>
<span data-ttu-id="5a53d-121">Określa nowy typ sKU bramy.</span><span class="sxs-lookup"><span data-stu-id="5a53d-121">Specifies the new type of gateway SKU.</span></span>
<span data-ttu-id="5a53d-122">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="5a53d-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5a53d-123">Podstawowe</span><span class="sxs-lookup"><span data-stu-id="5a53d-123">Basic</span></span>
- <span data-ttu-id="5a53d-124">Standardowe</span><span class="sxs-lookup"><span data-stu-id="5a53d-124">Standard</span></span>
- <span data-ttu-id="5a53d-125">Wysoka wydajność</span><span class="sxs-lookup"><span data-stu-id="5a53d-125">High Performance</span></span>
- <span data-ttu-id="5a53d-126">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="5a53d-126">VpnGw1</span></span>
- <span data-ttu-id="5a53d-127">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="5a53d-127">VpnGw2</span></span>
- <span data-ttu-id="5a53d-128">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="5a53d-128">VpnGw3</span></span>
- <span data-ttu-id="5a53d-129">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="5a53d-129">VpnGw1AZ</span></span> 
- <span data-ttu-id="5a53d-130">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="5a53d-130">VpnGw2AZ</span></span> 
- <span data-ttu-id="5a53d-131">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="5a53d-131">VpnGw3AZ</span></span> 
- <span data-ttu-id="5a53d-132">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="5a53d-132">ErGw1AZ</span></span> 
- <span data-ttu-id="5a53d-133">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="5a53d-133">ErGw2AZ</span></span> 
- <span data-ttu-id="5a53d-134">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="5a53d-134">ErGw3AZ</span></span> 

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

### <span data-ttu-id="5a53d-135">— VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5a53d-135">-VirtualNetworkGateway</span></span>
<span data-ttu-id="5a53d-136">Określa odwołanie do obiektu do bramy sieci wirtualnej, których rozmiar ma zostać zmieniony.</span><span class="sxs-lookup"><span data-stu-id="5a53d-136">Specifies an object reference to the virtual network gateway to be resized.</span></span>
<span data-ttu-id="5a53d-137">To odwołanie do obiektu można utworzyć, używając Get-AzVirtualNetworkGateway i określając nazwę bramy.</span><span class="sxs-lookup"><span data-stu-id="5a53d-137">You can create this object reference by using the Get-AzVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="5a53d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a53d-138">CommonParameters</span></span>
<span data-ttu-id="5a53d-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a53d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a53d-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a53d-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a53d-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a53d-141">INPUTS</span></span>

### <span data-ttu-id="5a53d-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5a53d-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="5a53d-143">System.String</span><span class="sxs-lookup"><span data-stu-id="5a53d-143">System.String</span></span>

## <span data-ttu-id="5a53d-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5a53d-144">OUTPUTS</span></span>

### <span data-ttu-id="5a53d-145">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5a53d-145">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="5a53d-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5a53d-146">NOTES</span></span>
<span data-ttu-id="5a53d-147">Nie można zmienić rozmiaru z wersji Basic/Standard/HighPerformance na nowe jednostki SKU VpnGw1/VpnGw2/VpnGw3.</span><span class="sxs-lookup"><span data-stu-id="5a53d-147">You cannot resize from Basic/Standard/HighPerformance SKUs to the new VpnGw1/VpnGw2/VpnGw3 SKUs.</span></span> <span data-ttu-id="5a53d-148">Dalsze zmienianie rozmiaru nie jest dozwolone z/do VpnGw1AZ/VpnGw2AZ/VpnGw3AZ lub ErGw1AZ/ErGw2AZ/ErGw3AZ.</span><span class="sxs-lookup"><span data-stu-id="5a53d-148">Further resize is not allowed from/to VpnGw1AZ/VpnGw2AZ/VpnGw3AZ or ErGw1AZ/ErGw2AZ/ErGw3AZ.</span></span> <span data-ttu-id="5a53d-149">Zmiana rozmiaru jest dozwolona tylko w "serii" SKU, np. VpnGw1AZ można zmienić na/z VpnGw2AZ/VpnGw3AZ i ErGw1AZ można zmienić na/z ErGw2AZ/ErGw3AZ.</span><span class="sxs-lookup"><span data-stu-id="5a53d-149">Resize is allowed only within the SKU 'series' e.g VpnGw1AZ can be resized to/from VpnGw2AZ/VpnGw3AZ and ErGw1AZ can be resized to/from ErGw2AZ/ErGw3AZ.</span></span> <span data-ttu-id="5a53d-150">Zobacz https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways instrukcje.</span><span class="sxs-lookup"><span data-stu-id="5a53d-150">See https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways for instructions.</span></span>

## <span data-ttu-id="5a53d-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5a53d-151">RELATED LINKS</span></span>

[<span data-ttu-id="5a53d-152">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5a53d-152">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="5a53d-153">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5a53d-153">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="5a53d-154">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5a53d-154">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="5a53d-155">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5a53d-155">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="5a53d-156">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5a53d-156">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)

[<span data-ttu-id="5a53d-157">Get-AzVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="5a53d-157">Get-AzVpnClientPackage</span></span>](./Get-AzVpnClientPackage.md)

