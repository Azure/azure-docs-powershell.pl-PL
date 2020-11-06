---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 6ea456ca5e8d06c1ff732664127ca2e7a62abb2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552212"
---
# <span data-ttu-id="7b57a-101">Remove-AzureRmVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="7b57a-101">Remove-AzureRmVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="7b57a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7b57a-102">SYNOPSIS</span></span>
<span data-ttu-id="7b57a-103">Usuwa witrynę domyślną z bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7b57a-103">Removes the default site from a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b57a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7b57a-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b57a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7b57a-105">DESCRIPTION</span></span>
<span data-ttu-id="7b57a-106">Polecenie cmdlet **Remove-AzureRmVirtualNetworkGatewayDefaultSite** umożliwia usunięcie domyślnej witryny tunelowania wymuszonego z bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7b57a-106">The **Remove-AzureRmVirtualNetworkGatewayDefaultSite** cmdlet removes the forced tunneling default site from a virtual network gateway.</span></span>
<span data-ttu-id="7b57a-107">Wymuszone tunelowanie zapewnia sposób na przekierowanie ruchu związanego z Internetem z maszyn wirtualnych platformy Azure do sieci lokalnej. Dzięki temu można sprawdzać ruch i prowadzić inspekcję ruchu przed jego zwolnieniem.</span><span class="sxs-lookup"><span data-stu-id="7b57a-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="7b57a-108">Tunelowanie wymuszone jest realizowane przy użyciu tunelu wirtualnej sieci prywatnej (VPN); ten tunel wymaga witryny domyślnej, bramy lokalnej, w której jest przekierowywany cały ruch związany z Internetem usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="7b57a-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>

<span data-ttu-id="7b57a-109">**Remove-AzureRmVirtualNetworkGatewayDefaultSite** usuwa domyślną witrynę przypisaną do bramy.</span><span class="sxs-lookup"><span data-stu-id="7b57a-109">**Remove-AzureRmVirtualNetworkGatewayDefaultSite** removes the default site assigned to a gateway.</span></span>
<span data-ttu-id="7b57a-110">Jeśli to zrobisz, musisz użyć Set-AzureRmVirtualNetworkGatewayDefaultSite, aby przypisać nową witrynę domyślną, zanim Brama będzie mogła być używana do wymuszonego tunelowania.</span><span class="sxs-lookup"><span data-stu-id="7b57a-110">If you do this you will need to use Set-AzureRmVirtualNetworkGatewayDefaultSite to assign a new default site before the gateway can be used for forced tunneling.</span></span>

## <span data-ttu-id="7b57a-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7b57a-111">EXAMPLES</span></span>

### <span data-ttu-id="7b57a-112">Przykład 1: usuwanie domyślnej witryny przypisanej do bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="7b57a-112">Example 1: Remove the default site assigned to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworknGateway $Gateway
```

<span data-ttu-id="7b57a-113">W tym przykładzie jest usuwana witryna domyślna obecnie przypisana do bramy sieci wirtualnej o nazwie ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="7b57a-113">This example removes the default site currently assigned to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="7b57a-114">W pierwszym poleceniu użyto polecenia **Get-AzureRmVirtualNetworkGateway** w celu utworzenia odwołania do obiektu do bramy; odwołanie do tego obiektu jest przechowywane w zmiennej o nazwie $Gateway.</span><span class="sxs-lookup"><span data-stu-id="7b57a-114">The first command uses **Get-AzureRmVirtualNetworkGateway** to create an object reference to the gateway; this object reference is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="7b57a-115">Drugie polecenie korzysta z polecenia **Remove-AzureRmVirtualNetworkGatewayDefaultSite** w celu usunięcia domyślnej witryny przypisanej do tej bramy.</span><span class="sxs-lookup"><span data-stu-id="7b57a-115">The second command then uses **Remove-AzureRmVirtualNetworkGatewayDefaultSite** to remove the default site assigned to that gateway.</span></span>

## <span data-ttu-id="7b57a-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7b57a-116">PARAMETERS</span></span>

### <span data-ttu-id="7b57a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b57a-117">-DefaultProfile</span></span>
<span data-ttu-id="7b57a-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7b57a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b57a-119">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7b57a-119">-VirtualNetworkGateway</span></span>
<span data-ttu-id="7b57a-120">Określa odwołanie do obiektu bramy sieci wirtualnej zawierającej domyślną witrynę do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="7b57a-120">Specifies an object reference to the virtual network gateway containing the default site to be removed.</span></span>
<span data-ttu-id="7b57a-121">Odwołanie do obiektu bramy sieci wirtualnej można utworzyć przy użyciu Get-AzureRmVirtualNetworkGateway i określając nazwę bramy.</span><span class="sxs-lookup"><span data-stu-id="7b57a-121">You can create an object reference to a virtual network gateway by using the Get-AzureRmVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="7b57a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b57a-122">CommonParameters</span></span>
<span data-ttu-id="7b57a-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b57a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b57a-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b57a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b57a-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7b57a-125">INPUTS</span></span>

###  
<span data-ttu-id="7b57a-126">To polecenie cmdlet akceptuje potokowe wystąpienia obiektu **Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="7b57a-126">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="7b57a-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7b57a-127">OUTPUTS</span></span>

###  
<span data-ttu-id="7b57a-128">To polecenie cmdlet modyfikuje istniejące wystąpienia obiektu **Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="7b57a-128">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="7b57a-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7b57a-129">NOTES</span></span>

## <span data-ttu-id="7b57a-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7b57a-130">RELATED LINKS</span></span>

[<span data-ttu-id="7b57a-131">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7b57a-131">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="7b57a-132">Set-AzureRmVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="7b57a-132">Set-AzureRmVirtualNetworkGatewayDefaultSite</span></span>](./Set-AzureRmVirtualNetworkGatewayDefaultSite.md)


