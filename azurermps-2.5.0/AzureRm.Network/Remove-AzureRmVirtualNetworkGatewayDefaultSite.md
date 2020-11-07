---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgatewaydefaultsite
schema: 2.0.0
ms.openlocfilehash: ded608261981073ef5544df2b64e99171eef7710
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897862"
---
# <span data-ttu-id="552d6-101">Remove-AzureRmVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="552d6-101">Remove-AzureRmVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="552d6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="552d6-102">SYNOPSIS</span></span>
<span data-ttu-id="552d6-103">Usuwa witrynę domyślną z bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="552d6-103">Removes the default site from a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="552d6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="552d6-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="552d6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="552d6-105">DESCRIPTION</span></span>
<span data-ttu-id="552d6-106">Polecenie cmdlet **Remove-AzureRmVirtualNetworkGatewayDefaultSite** umożliwia usunięcie domyślnej witryny tunelowania wymuszonego z bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="552d6-106">The **Remove-AzureRmVirtualNetworkGatewayDefaultSite** cmdlet removes the forced tunneling default site from a virtual network gateway.</span></span>
<span data-ttu-id="552d6-107">Wymuszone tunelowanie zapewnia sposób na przekierowanie ruchu związanego z Internetem z maszyn wirtualnych platformy Azure do sieci lokalnej. Dzięki temu można sprawdzać ruch i prowadzić inspekcję ruchu przed jego zwolnieniem.</span><span class="sxs-lookup"><span data-stu-id="552d6-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="552d6-108">Tunelowanie wymuszone jest realizowane przy użyciu tunelu wirtualnej sieci prywatnej (VPN); ten tunel wymaga witryny domyślnej, bramy lokalnej, w której jest przekierowywany cały ruch związany z Internetem usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="552d6-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>

<span data-ttu-id="552d6-109">**Remove-AzureRmVirtualNetworkGatewayDefaultSite** usuwa domyślną witrynę przypisaną do bramy.</span><span class="sxs-lookup"><span data-stu-id="552d6-109">**Remove-AzureRmVirtualNetworkGatewayDefaultSite** removes the default site assigned to a gateway.</span></span>
<span data-ttu-id="552d6-110">Jeśli to zrobisz, musisz użyć Set-AzureRmVirtualNetworkGatewayDefaultSite, aby przypisać nową witrynę domyślną, zanim Brama będzie mogła być używana do wymuszonego tunelowania.</span><span class="sxs-lookup"><span data-stu-id="552d6-110">If you do this you will need to use Set-AzureRmVirtualNetworkGatewayDefaultSite to assign a new default site before the gateway can be used for forced tunneling.</span></span>

## <span data-ttu-id="552d6-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="552d6-111">EXAMPLES</span></span>

### <span data-ttu-id="552d6-112">Przykład 1: usuwanie domyślnej witryny przypisanej do bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="552d6-112">Example 1: Remove the default site assigned to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworknGateway $Gateway
```

<span data-ttu-id="552d6-113">W tym przykładzie jest usuwana witryna domyślna obecnie przypisana do bramy sieci wirtualnej o nazwie ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="552d6-113">This example removes the default site currently assigned to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="552d6-114">W pierwszym poleceniu użyto polecenia **Get-AzureRmVirtualNetworkGateway** w celu utworzenia odwołania do obiektu do bramy; odwołanie do tego obiektu jest przechowywane w zmiennej o nazwie $Gateway.</span><span class="sxs-lookup"><span data-stu-id="552d6-114">The first command uses **Get-AzureRmVirtualNetworkGateway** to create an object reference to the gateway; this object reference is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="552d6-115">Drugie polecenie korzysta z polecenia **Remove-AzureRmVirtualNetworkGatewayDefaultSite** w celu usunięcia domyślnej witryny przypisanej do tej bramy.</span><span class="sxs-lookup"><span data-stu-id="552d6-115">The second command then uses **Remove-AzureRmVirtualNetworkGatewayDefaultSite** to remove the default site assigned to that gateway.</span></span>

## <span data-ttu-id="552d6-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="552d6-116">PARAMETERS</span></span>

### <span data-ttu-id="552d6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="552d6-117">-DefaultProfile</span></span>
<span data-ttu-id="552d6-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="552d6-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="552d6-119">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="552d6-119">-VirtualNetworkGateway</span></span>
<span data-ttu-id="552d6-120">Określa odwołanie do obiektu bramy sieci wirtualnej zawierającej domyślną witrynę do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="552d6-120">Specifies an object reference to the virtual network gateway containing the default site to be removed.</span></span>
<span data-ttu-id="552d6-121">Odwołanie do obiektu bramy sieci wirtualnej można utworzyć przy użyciu Get-AzureRmVirtualNetworkGateway i określając nazwę bramy.</span><span class="sxs-lookup"><span data-stu-id="552d6-121">You can create an object reference to a virtual network gateway by using the Get-AzureRmVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="552d6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="552d6-122">CommonParameters</span></span>
<span data-ttu-id="552d6-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="552d6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="552d6-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="552d6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="552d6-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="552d6-125">INPUTS</span></span>

###  
<span data-ttu-id="552d6-126">To polecenie cmdlet akceptuje potokowe wystąpienia obiektu **Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="552d6-126">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="552d6-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="552d6-127">OUTPUTS</span></span>

###  
<span data-ttu-id="552d6-128">To polecenie cmdlet modyfikuje istniejące wystąpienia obiektu **Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="552d6-128">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="552d6-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="552d6-129">NOTES</span></span>

## <span data-ttu-id="552d6-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="552d6-130">RELATED LINKS</span></span>

[<span data-ttu-id="552d6-131">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="552d6-131">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="552d6-132">Set-AzureRmVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="552d6-132">Set-AzureRmVirtualNetworkGatewayDefaultSite</span></span>](./Set-AzureRmVirtualNetworkGatewayDefaultSite.md)


