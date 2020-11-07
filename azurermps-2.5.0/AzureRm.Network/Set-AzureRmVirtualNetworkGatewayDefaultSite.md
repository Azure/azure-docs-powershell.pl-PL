---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewaydefaultsite
schema: 2.0.0
ms.openlocfilehash: 463951ca6b6679671f330a3ddb0f9460a878a3d3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898880"
---
# <span data-ttu-id="eee38-101">Set-AzureRmVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="eee38-101">Set-AzureRmVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="eee38-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eee38-102">SYNOPSIS</span></span>
<span data-ttu-id="eee38-103">Ustawia domyślną witrynę bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="eee38-103">Sets the default site for a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eee38-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eee38-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eee38-105">Opis</span><span class="sxs-lookup"><span data-stu-id="eee38-105">DESCRIPTION</span></span>
<span data-ttu-id="eee38-106">Polecenie cmdlet **Set-AzureRmVirtualNetworkGatewayDefaultSite** przypisuje domyślną witrynę tunelowania wymuszonego do bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="eee38-106">The **Set-AzureRmVirtualNetworkGatewayDefaultSite** cmdlet assigns a forced tunneling default site to a virtual network gateway.</span></span>
<span data-ttu-id="eee38-107">Wymuszone tunelowanie zapewnia sposób na przekierowanie ruchu związanego z Internetem z maszyn wirtualnych platformy Azure do sieci lokalnej. Dzięki temu można sprawdzać ruch i prowadzić inspekcję ruchu przed jego zwolnieniem.</span><span class="sxs-lookup"><span data-stu-id="eee38-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="eee38-108">Tunelowanie wymuszone jest realizowane przy użyciu tunelu wirtualnej sieci prywatnej (VPN); ten tunel wymaga witryny domyślnej, bramy lokalnej, w której jest przekierowywany cały ruch związany z Internetem usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="eee38-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="eee38-109">**Set-AzureRmVirtualNetworkGatewayDefaultSite** umożliwia zmianę domyślnej witryny przypisanej do bramy.</span><span class="sxs-lookup"><span data-stu-id="eee38-109">**Set-AzureRmVirtualNetworkGatewayDefaultSite** provides a way to change the default site assigned to a gateway.</span></span>

## <span data-ttu-id="eee38-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eee38-110">EXAMPLES</span></span>

### <span data-ttu-id="eee38-111">Przykład 1: przypisywanie domyślnej witryny do bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="eee38-111">Example 1: Assign a default site to a virtual network gateway</span></span>
```
PS C:\>$LocalGateway = Get-AzureRmLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzureRmVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

<span data-ttu-id="eee38-112">W tym przykładzie przypiszesz witrynę domyślną do bramy sieci wirtualnej o nazwie ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="eee38-112">This example assigns a default site to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="eee38-113">Pierwsze polecenie tworzy odwołanie do obiektu do bramy lokalnej o nazwie ContosoLocalGateway.</span><span class="sxs-lookup"><span data-stu-id="eee38-113">The first command creates an object reference to a local gateway named ContosoLocalGateway.</span></span>
<span data-ttu-id="eee38-114">Odwołanie do obiektu przechowywane w zmiennej o nazwie $LocalGateway reprezentuje bramę, która ma zostać skonfigurowana jako witryna domyślna</span><span class="sxs-lookup"><span data-stu-id="eee38-114">This object reference that is stored in the variable named $LocalGateway represents the gateway to be configured as the default site</span></span>

<span data-ttu-id="eee38-115">.</span><span class="sxs-lookup"><span data-stu-id="eee38-115">.</span></span>
<span data-ttu-id="eee38-116">Drugie polecenie tworzy następnie odwołanie do obiektu bramy sieci wirtualnej i zapisuje wynik w zmiennej o nazwie $VirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="eee38-116">The second command then creates an object reference to the virtual network gateway and stores the result in the variable named $VirtualGateway.</span></span>

<span data-ttu-id="eee38-117">W trzecim poleceniu przypiszesz domyślną witrynę do ContosoVirtualGateway przy użyciu polecenia cmdlet **Set-AzureRmVirtualNetworkGatewayDefaultSite** .</span><span class="sxs-lookup"><span data-stu-id="eee38-117">The third command uses the **Set-AzureRmVirtualNetworkGatewayDefaultSite** cmdlet to assign the default site to ContosoVirtualGateway.</span></span>

## <span data-ttu-id="eee38-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eee38-118">PARAMETERS</span></span>

### <span data-ttu-id="eee38-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eee38-119">-DefaultProfile</span></span>
<span data-ttu-id="eee38-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="eee38-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eee38-121">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="eee38-121">-GatewayDefaultSite</span></span>
<span data-ttu-id="eee38-122">Określa odwołanie do obiektu bramy sieci lokalnej, które ma zostać przypisane jako witryna domyślna dla określonej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="eee38-122">Specifies an object reference to the local network gateway to be assigned as the default site for the specified virtual network.</span></span>
<span data-ttu-id="eee38-123">Za pomocą polecenia cmdlet Get-AzureRmLocalNetworkGateway można utworzyć odwołanie do obiektu do bramy lokalnej.</span><span class="sxs-lookup"><span data-stu-id="eee38-123">You can use the Get-AzureRmLocalNetworkGateway cmdlet to create an object reference to a local gateway.</span></span>

```yaml
Type: PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eee38-124">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="eee38-124">-VirtualNetworkGateway</span></span>
<span data-ttu-id="eee38-125">Określa odwołanie do obiektu bramy sieci wirtualnej, w której zostanie przypisana domyślna witryna.</span><span class="sxs-lookup"><span data-stu-id="eee38-125">Specifies an object reference to the virtual network gateway where the default site will be assigned.</span></span>
<span data-ttu-id="eee38-126">Odwołanie do obiektu bramy sieci wirtualnej można utworzyć, korzystając z funkcji **Get-AzureRmVirtualNetworkGateway** i określając nazwę bramy.</span><span class="sxs-lookup"><span data-stu-id="eee38-126">You can create an object reference to a virtual network gateway by using the **Get-AzureRmVirtualNetworkGateway** and specifying the name of the gateway.</span></span>

<span data-ttu-id="eee38-127">Zmienna $VirtualGateway może być następnie używana jako wartość parametru parametru *VirtualNetworkGateway* :</span><span class="sxs-lookup"><span data-stu-id="eee38-127">The variable $VirtualGateway can then be used as the parameter value for the *VirtualNetworkGateway* parameter:</span></span>

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

### <span data-ttu-id="eee38-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eee38-128">CommonParameters</span></span>
<span data-ttu-id="eee38-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eee38-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eee38-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eee38-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eee38-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eee38-131">INPUTS</span></span>

###  
<span data-ttu-id="eee38-132">To polecenie cmdlet akceptuje potokowe wystąpienia obiektu **Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="eee38-132">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="eee38-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eee38-133">OUTPUTS</span></span>

###  
<span data-ttu-id="eee38-134">To polecenie cmdlet modyfikuje istniejące wystąpienia obiektu **Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="eee38-134">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="eee38-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eee38-135">NOTES</span></span>

## <span data-ttu-id="eee38-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eee38-136">RELATED LINKS</span></span>

[<span data-ttu-id="eee38-137">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="eee38-137">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="eee38-138">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="eee38-138">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="eee38-139">Remove-AzureRmVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="eee38-139">Remove-AzureRmVirtualNetworkGatewayDefaultSite</span></span>](./Remove-AzureRmVirtualNetworkGatewayDefaultSite.md)


