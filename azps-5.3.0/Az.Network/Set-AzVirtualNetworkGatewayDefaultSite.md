---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: a4be0aed365517e1ae3ae11155f82ea097db309a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501208"
---
# <span data-ttu-id="e0bfa-101">Set-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="e0bfa-101">Set-AzVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="e0bfa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e0bfa-102">SYNOPSIS</span></span>
<span data-ttu-id="e0bfa-103">Ustawia domyślną witrynę bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e0bfa-103">Sets the default site for a virtual network gateway.</span></span>

## <span data-ttu-id="e0bfa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e0bfa-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0bfa-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e0bfa-105">DESCRIPTION</span></span>
<span data-ttu-id="e0bfa-106">Polecenie cmdlet **Set-AzVirtualNetworkGatewayDefaultSite** przypisuje domyślną witrynę tunelowania wymuszonego do bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e0bfa-106">The **Set-AzVirtualNetworkGatewayDefaultSite** cmdlet assigns a forced tunneling default site to a virtual network gateway.</span></span>
<span data-ttu-id="e0bfa-107">Wymuszone tunelowanie zapewnia sposób na przekierowanie ruchu związanego z Internetem z maszyn wirtualnych platformy Azure do sieci lokalnej. Dzięki temu można sprawdzać ruch i prowadzić inspekcję ruchu przed jego zwolnieniem.</span><span class="sxs-lookup"><span data-stu-id="e0bfa-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="e0bfa-108">Tunelowanie wymuszone jest realizowane przy użyciu tunelu wirtualnej sieci prywatnej (VPN); ten tunel wymaga witryny domyślnej, bramy lokalnej, w której jest przekierowywany cały ruch związany z Internetem usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="e0bfa-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="e0bfa-109">**Set-AzVirtualNetworkGatewayDefaultSite** umożliwia zmianę domyślnej witryny przypisanej do bramy.</span><span class="sxs-lookup"><span data-stu-id="e0bfa-109">**Set-AzVirtualNetworkGatewayDefaultSite** provides a way to change the default site assigned to a gateway.</span></span>

## <span data-ttu-id="e0bfa-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e0bfa-110">EXAMPLES</span></span>

### <span data-ttu-id="e0bfa-111">Przykład 1: przypisywanie domyślnej witryny do bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="e0bfa-111">Example 1: Assign a default site to a virtual network gateway</span></span>
```
PS C:\>$LocalGateway = Get-AzLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

<span data-ttu-id="e0bfa-112">W tym przykładzie przypiszesz witrynę domyślną do bramy sieci wirtualnej o nazwie ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="e0bfa-112">This example assigns a default site to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="e0bfa-113">Pierwsze polecenie tworzy odwołanie do obiektu do bramy lokalnej o nazwie ContosoLocalGateway.</span><span class="sxs-lookup"><span data-stu-id="e0bfa-113">The first command creates an object reference to a local gateway named ContosoLocalGateway.</span></span>
<span data-ttu-id="e0bfa-114">Odwołanie do obiektu przechowywane w zmiennej o nazwie $LocalGateway reprezentuje bramę, która ma zostać skonfigurowana jako witryna domyślna.</span><span class="sxs-lookup"><span data-stu-id="e0bfa-114">This object reference that is stored in the variable named $LocalGateway represents the gateway to be configured as the default site .</span></span>
<span data-ttu-id="e0bfa-115">Drugie polecenie tworzy następnie odwołanie do obiektu bramy sieci wirtualnej i zapisuje wynik w zmiennej o nazwie $VirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="e0bfa-115">The second command then creates an object reference to the virtual network gateway and stores the result in the variable named $VirtualGateway.</span></span>
<span data-ttu-id="e0bfa-116">W trzecim poleceniu przypiszesz domyślną witrynę do ContosoVirtualGateway przy użyciu polecenia cmdlet **Set-AzVirtualNetworkGatewayDefaultSite** .</span><span class="sxs-lookup"><span data-stu-id="e0bfa-116">The third command uses the **Set-AzVirtualNetworkGatewayDefaultSite** cmdlet to assign the default site to ContosoVirtualGateway.</span></span>

## <span data-ttu-id="e0bfa-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e0bfa-117">PARAMETERS</span></span>

### <span data-ttu-id="e0bfa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0bfa-118">-DefaultProfile</span></span>
<span data-ttu-id="e0bfa-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e0bfa-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0bfa-120">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="e0bfa-120">-GatewayDefaultSite</span></span>
<span data-ttu-id="e0bfa-121">Określa odwołanie do obiektu bramy sieci lokalnej, które ma zostać przypisane jako witryna domyślna dla określonej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e0bfa-121">Specifies an object reference to the local network gateway to be assigned as the default site for the specified virtual network.</span></span>
<span data-ttu-id="e0bfa-122">Za pomocą polecenia cmdlet Get-AzLocalNetworkGateway można utworzyć odwołanie do obiektu do bramy lokalnej.</span><span class="sxs-lookup"><span data-stu-id="e0bfa-122">You can use the Get-AzLocalNetworkGateway cmdlet to create an object reference to a local gateway.</span></span>

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

### <span data-ttu-id="e0bfa-123">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e0bfa-123">-VirtualNetworkGateway</span></span>
<span data-ttu-id="e0bfa-124">Określa odwołanie do obiektu bramy sieci wirtualnej, w której zostanie przypisana domyślna witryna.</span><span class="sxs-lookup"><span data-stu-id="e0bfa-124">Specifies an object reference to the virtual network gateway where the default site will be assigned.</span></span>
<span data-ttu-id="e0bfa-125">Odwołanie do obiektu bramy sieci wirtualnej można utworzyć, korzystając z funkcji **Get-AzVirtualNetworkGateway** i określając nazwę bramy.</span><span class="sxs-lookup"><span data-stu-id="e0bfa-125">You can create an object reference to a virtual network gateway by using the **Get-AzVirtualNetworkGateway** and specifying the name of the gateway.</span></span>
<span data-ttu-id="e0bfa-126">Zmienna $VirtualGateway może być następnie używana jako wartość parametru parametru *VirtualNetworkGateway* :</span><span class="sxs-lookup"><span data-stu-id="e0bfa-126">The variable $VirtualGateway can then be used as the parameter value for the *VirtualNetworkGateway* parameter:</span></span>

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

### <span data-ttu-id="e0bfa-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0bfa-127">CommonParameters</span></span>
<span data-ttu-id="e0bfa-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0bfa-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0bfa-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0bfa-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0bfa-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0bfa-130">INPUTS</span></span>

### <span data-ttu-id="e0bfa-131">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e0bfa-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="e0bfa-132">Microsoft. Azure. Commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e0bfa-132">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="e0bfa-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e0bfa-133">OUTPUTS</span></span>

### <span data-ttu-id="e0bfa-134">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e0bfa-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="e0bfa-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e0bfa-135">NOTES</span></span>

## <span data-ttu-id="e0bfa-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e0bfa-136">RELATED LINKS</span></span>

[<span data-ttu-id="e0bfa-137">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e0bfa-137">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="e0bfa-138">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e0bfa-138">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="e0bfa-139">Remove-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="e0bfa-139">Remove-AzVirtualNetworkGatewayDefaultSite</span></span>](./Remove-AzVirtualNetworkGatewayDefaultSite.md)


