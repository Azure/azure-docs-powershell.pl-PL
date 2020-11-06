---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 4ab32ab5830356740cdb1709799b7dcb8f811c90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543183"
---
# <span data-ttu-id="45a73-101">Set-AzureRmVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="45a73-101">Set-AzureRmVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="45a73-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="45a73-102">SYNOPSIS</span></span>
<span data-ttu-id="45a73-103">Ustawia domyślną witrynę bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="45a73-103">Sets the default site for a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45a73-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="45a73-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45a73-105">Opis</span><span class="sxs-lookup"><span data-stu-id="45a73-105">DESCRIPTION</span></span>
<span data-ttu-id="45a73-106">Polecenie cmdlet **Set-AzureRmVirtualNetworkGatewayDefaultSite** przypisuje domyślną witrynę tunelowania wymuszonego do bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="45a73-106">The **Set-AzureRmVirtualNetworkGatewayDefaultSite** cmdlet assigns a forced tunneling default site to a virtual network gateway.</span></span>
<span data-ttu-id="45a73-107">Wymuszone tunelowanie zapewnia sposób na przekierowanie ruchu związanego z Internetem z maszyn wirtualnych platformy Azure do sieci lokalnej. Dzięki temu można sprawdzać ruch i prowadzić inspekcję ruchu przed jego zwolnieniem.</span><span class="sxs-lookup"><span data-stu-id="45a73-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="45a73-108">Tunelowanie wymuszone jest realizowane przy użyciu tunelu wirtualnej sieci prywatnej (VPN); ten tunel wymaga witryny domyślnej, bramy lokalnej, w której jest przekierowywany cały ruch związany z Internetem usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="45a73-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="45a73-109">**Set-AzureRmVirtualNetworkGatewayDefaultSite** umożliwia zmianę domyślnej witryny przypisanej do bramy.</span><span class="sxs-lookup"><span data-stu-id="45a73-109">**Set-AzureRmVirtualNetworkGatewayDefaultSite** provides a way to change the default site assigned to a gateway.</span></span>

## <span data-ttu-id="45a73-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="45a73-110">EXAMPLES</span></span>

### <span data-ttu-id="45a73-111">Przykład 1: przypisywanie domyślnej witryny do bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="45a73-111">Example 1: Assign a default site to a virtual network gateway</span></span>
```
PS C:\>$LocalGateway = Get-AzureRmLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzureRmVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

<span data-ttu-id="45a73-112">W tym przykładzie przypiszesz witrynę domyślną do bramy sieci wirtualnej o nazwie ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="45a73-112">This example assigns a default site to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="45a73-113">Pierwsze polecenie tworzy odwołanie do obiektu do bramy lokalnej o nazwie ContosoLocalGateway.</span><span class="sxs-lookup"><span data-stu-id="45a73-113">The first command creates an object reference to a local gateway named ContosoLocalGateway.</span></span>
<span data-ttu-id="45a73-114">Odwołanie do obiektu przechowywane w zmiennej o nazwie $LocalGateway reprezentuje bramę, która ma zostać skonfigurowana jako witryna domyślna</span><span class="sxs-lookup"><span data-stu-id="45a73-114">This object reference that is stored in the variable named $LocalGateway represents the gateway to be configured as the default site</span></span>

<span data-ttu-id="45a73-115">.</span><span class="sxs-lookup"><span data-stu-id="45a73-115">.</span></span>
<span data-ttu-id="45a73-116">Drugie polecenie tworzy następnie odwołanie do obiektu bramy sieci wirtualnej i zapisuje wynik w zmiennej o nazwie $VirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="45a73-116">The second command then creates an object reference to the virtual network gateway and stores the result in the variable named $VirtualGateway.</span></span>

<span data-ttu-id="45a73-117">W trzecim poleceniu przypiszesz domyślną witrynę do ContosoVirtualGateway przy użyciu polecenia cmdlet **Set-AzureRmVirtualNetworkGatewayDefaultSite** .</span><span class="sxs-lookup"><span data-stu-id="45a73-117">The third command uses the **Set-AzureRmVirtualNetworkGatewayDefaultSite** cmdlet to assign the default site to ContosoVirtualGateway.</span></span>

## <span data-ttu-id="45a73-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="45a73-118">PARAMETERS</span></span>

### <span data-ttu-id="45a73-119">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="45a73-119">-GatewayDefaultSite</span></span>
<span data-ttu-id="45a73-120">Określa odwołanie do obiektu bramy sieci lokalnej, które ma zostać przypisane jako witryna domyślna dla określonej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="45a73-120">Specifies an object reference to the local network gateway to be assigned as the default site for the specified virtual network.</span></span>
<span data-ttu-id="45a73-121">Za pomocą polecenia cmdlet Get-AzureRmLocalNetworkGateway można utworzyć odwołanie do obiektu do bramy lokalnej.</span><span class="sxs-lookup"><span data-stu-id="45a73-121">You can use the Get-AzureRmLocalNetworkGateway cmdlet to create an object reference to a local gateway.</span></span>

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

### <span data-ttu-id="45a73-122">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="45a73-122">-VirtualNetworkGateway</span></span>
<span data-ttu-id="45a73-123">Określa odwołanie do obiektu bramy sieci wirtualnej, w której zostanie przypisana domyślna witryna.</span><span class="sxs-lookup"><span data-stu-id="45a73-123">Specifies an object reference to the virtual network gateway where the default site will be assigned.</span></span>
<span data-ttu-id="45a73-124">Odwołanie do obiektu bramy sieci wirtualnej można utworzyć, korzystając z funkcji **Get-AzureRmVirtualNetworkGateway** i określając nazwę bramy.</span><span class="sxs-lookup"><span data-stu-id="45a73-124">You can create an object reference to a virtual network gateway by using the **Get-AzureRmVirtualNetworkGateway** and specifying the name of the gateway.</span></span>

<span data-ttu-id="45a73-125">Zmienna $VirtualGateway może być następnie używana jako wartość parametru parametru *VirtualNetworkGateway* :</span><span class="sxs-lookup"><span data-stu-id="45a73-125">The variable $VirtualGateway can then be used as the parameter value for the *VirtualNetworkGateway* parameter:</span></span>

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

### <span data-ttu-id="45a73-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45a73-126">-DefaultProfile</span></span>
<span data-ttu-id="45a73-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="45a73-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45a73-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45a73-128">CommonParameters</span></span>
<span data-ttu-id="45a73-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45a73-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45a73-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45a73-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45a73-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45a73-131">INPUTS</span></span>

###  
<span data-ttu-id="45a73-132">To polecenie cmdlet akceptuje potokowe wystąpienia obiektu **Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="45a73-132">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="45a73-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="45a73-133">OUTPUTS</span></span>

###  
<span data-ttu-id="45a73-134">To polecenie cmdlet modyfikuje istniejące wystąpienia obiektu **Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="45a73-134">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="45a73-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="45a73-135">NOTES</span></span>

## <span data-ttu-id="45a73-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="45a73-136">RELATED LINKS</span></span>

[<span data-ttu-id="45a73-137">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="45a73-137">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="45a73-138">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="45a73-138">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="45a73-139">Remove-AzureRmVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="45a73-139">Remove-AzureRmVirtualNetworkGatewayDefaultSite</span></span>](./Remove-AzureRmVirtualNetworkGatewayDefaultSite.md)


