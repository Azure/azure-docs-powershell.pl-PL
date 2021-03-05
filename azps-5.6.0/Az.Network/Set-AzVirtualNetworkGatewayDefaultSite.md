---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/powershell/module/az.network/set-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 8e35347813849badfa50100cc4cac418e2d66332
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979441"
---
# <span data-ttu-id="8aa44-101">Set-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="8aa44-101">Set-AzVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="8aa44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8aa44-102">SYNOPSIS</span></span>
<span data-ttu-id="8aa44-103">Ustawia domyślną witrynę dla bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8aa44-103">Sets the default site for a virtual network gateway.</span></span>

## <span data-ttu-id="8aa44-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8aa44-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8aa44-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8aa44-105">DESCRIPTION</span></span>
<span data-ttu-id="8aa44-106">Polecenie **cmdlet Set-AzVirtualNetworkGatewayDefaultSite** przypisuje do bramy sieci wirtualnej wymuszone wydyskokianie domyślnej witryny.</span><span class="sxs-lookup"><span data-stu-id="8aa44-106">The **Set-AzVirtualNetworkGatewayDefaultSite** cmdlet assigns a forced tunneling default site to a virtual network gateway.</span></span>
<span data-ttu-id="8aa44-107">Wymuszone podkoszowe zapewnia możliwość przekierowywania ruchu związanego z Internetem z maszyn wirtualnych platformy Azure do Twojej sieci lokalnej. umożliwia to inspekcję i inspekcję ruchu przed jego zwolnieniem.</span><span class="sxs-lookup"><span data-stu-id="8aa44-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="8aa44-108">Wymuszone podkołowy są wykonywane przy użyciu podkołowego wirtualnej sieci prywatnej (VPN); ten kork wymaga witryny domyślnej, bramy lokalnej, do której jest przekierowywany cały ruch internetowy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8aa44-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="8aa44-109">**Set-AzVirtualNetworkGatewayDefaultSite** umożliwia zmianę domyślnej witryny przypisanej do bramy.</span><span class="sxs-lookup"><span data-stu-id="8aa44-109">**Set-AzVirtualNetworkGatewayDefaultSite** provides a way to change the default site assigned to a gateway.</span></span>

## <span data-ttu-id="8aa44-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8aa44-110">EXAMPLES</span></span>

### <span data-ttu-id="8aa44-111">Przykład 1. Przypisywanie witryny domyślnej do bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="8aa44-111">Example 1: Assign a default site to a virtual network gateway</span></span>
```
PS C:\>$LocalGateway = Get-AzLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

<span data-ttu-id="8aa44-112">W tym przykładzie do bramy sieci wirtualnej jest przypisywana witryna domyślna o nazwie ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="8aa44-112">This example assigns a default site to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="8aa44-113">Pierwsze polecenie tworzy odwołanie do obiektu do bramy lokalnej o nazwie ContosoLocalGateway.</span><span class="sxs-lookup"><span data-stu-id="8aa44-113">The first command creates an object reference to a local gateway named ContosoLocalGateway.</span></span>
<span data-ttu-id="8aa44-114">To odwołanie do obiektu przechowywane w zmiennej o nazwie $LocalGateway reprezentuje bramę, która ma zostać skonfigurowana jako witryna domyślna.</span><span class="sxs-lookup"><span data-stu-id="8aa44-114">This object reference that is stored in the variable named $LocalGateway represents the gateway to be configured as the default site .</span></span>
<span data-ttu-id="8aa44-115">Drugie polecenie tworzy wówczas odwołanie do obiektu do bramy sieci wirtualnej i zapisuje wynik w zmiennej o nazwie $VirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="8aa44-115">The second command then creates an object reference to the virtual network gateway and stores the result in the variable named $VirtualGateway.</span></span>
<span data-ttu-id="8aa44-116">Trzecie polecenie używa polecenia cmdlet **Set-AzVirtualNetworkGatewayDefaultSite** w celu przypisania witryny domyślnej do obiektu ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="8aa44-116">The third command uses the **Set-AzVirtualNetworkGatewayDefaultSite** cmdlet to assign the default site to ContosoVirtualGateway.</span></span>

## <span data-ttu-id="8aa44-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8aa44-117">PARAMETERS</span></span>

### <span data-ttu-id="8aa44-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8aa44-118">-DefaultProfile</span></span>
<span data-ttu-id="8aa44-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8aa44-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8aa44-120">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="8aa44-120">-GatewayDefaultSite</span></span>
<span data-ttu-id="8aa44-121">Określa odwołanie do obiektu do lokalnej bramy sieciowej, które ma zostać przypisane jako witryna domyślna dla określonej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8aa44-121">Specifies an object reference to the local network gateway to be assigned as the default site for the specified virtual network.</span></span>
<span data-ttu-id="8aa44-122">Polecenie cmdlet Get-AzLocalNetworkGateway umożliwia utworzenie odwołania do obiektu do bramy lokalnej.</span><span class="sxs-lookup"><span data-stu-id="8aa44-122">You can use the Get-AzLocalNetworkGateway cmdlet to create an object reference to a local gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8aa44-123">— VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8aa44-123">-VirtualNetworkGateway</span></span>
<span data-ttu-id="8aa44-124">Określa odwołanie do obiektu do bramy sieci wirtualnej, do której zostanie przypisana witryna domyślna.</span><span class="sxs-lookup"><span data-stu-id="8aa44-124">Specifies an object reference to the virtual network gateway where the default site will be assigned.</span></span>
<span data-ttu-id="8aa44-125">Możesz utworzyć odwołanie do obiektu do bramy sieci wirtualnej, używając narzędzia **Get-AzVirtualNetworkGateway** i określając nazwę bramy.</span><span class="sxs-lookup"><span data-stu-id="8aa44-125">You can create an object reference to a virtual network gateway by using the **Get-AzVirtualNetworkGateway** and specifying the name of the gateway.</span></span>
<span data-ttu-id="8aa44-126">Wartość zmiennej $VirtualGateway następnie może być używana jako wartość parametru dla parametru *VirtualNetworkGateway:*</span><span class="sxs-lookup"><span data-stu-id="8aa44-126">The variable $VirtualGateway can then be used as the parameter value for the *VirtualNetworkGateway* parameter:</span></span>

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

### <span data-ttu-id="8aa44-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8aa44-127">CommonParameters</span></span>
<span data-ttu-id="8aa44-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8aa44-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8aa44-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8aa44-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8aa44-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8aa44-130">INPUTS</span></span>

### <span data-ttu-id="8aa44-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8aa44-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="8aa44-132">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8aa44-132">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="8aa44-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8aa44-133">OUTPUTS</span></span>

### <span data-ttu-id="8aa44-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8aa44-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="8aa44-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8aa44-135">NOTES</span></span>

## <span data-ttu-id="8aa44-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8aa44-136">RELATED LINKS</span></span>

[<span data-ttu-id="8aa44-137">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8aa44-137">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="8aa44-138">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8aa44-138">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="8aa44-139">Remove-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="8aa44-139">Remove-AzVirtualNetworkGatewayDefaultSite</span></span>](./Remove-AzVirtualNetworkGatewayDefaultSite.md)


