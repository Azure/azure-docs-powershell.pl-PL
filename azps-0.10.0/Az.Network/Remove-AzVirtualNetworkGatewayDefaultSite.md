---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: bfd90797ff60c42927b23424e3c100efd16a6d24
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892910"
---
# <span data-ttu-id="810c4-101">Remove-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="810c4-101">Remove-AzVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="810c4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="810c4-102">SYNOPSIS</span></span>
<span data-ttu-id="810c4-103">Usuwa witrynę domyślną z bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="810c4-103">Removes the default site from a virtual network gateway.</span></span>

## <span data-ttu-id="810c4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="810c4-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="810c4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="810c4-105">DESCRIPTION</span></span>
<span data-ttu-id="810c4-106">Polecenie cmdlet **Remove-AzVirtualNetworkGatewayDefaultSite** umożliwia usunięcie domyślnej witryny tunelowania wymuszonego z bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="810c4-106">The **Remove-AzVirtualNetworkGatewayDefaultSite** cmdlet removes the forced tunneling default site from a virtual network gateway.</span></span>
<span data-ttu-id="810c4-107">Wymuszone tunelowanie zapewnia sposób na przekierowanie ruchu związanego z Internetem z maszyn wirtualnych platformy Azure do sieci lokalnej. Dzięki temu można sprawdzać ruch i prowadzić inspekcję ruchu przed jego zwolnieniem.</span><span class="sxs-lookup"><span data-stu-id="810c4-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="810c4-108">Tunelowanie wymuszone jest realizowane przy użyciu tunelu wirtualnej sieci prywatnej (VPN); ten tunel wymaga witryny domyślnej, bramy lokalnej, w której jest przekierowywany cały ruch związany z Internetem usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="810c4-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>

<span data-ttu-id="810c4-109">**Remove-AzVirtualNetworkGatewayDefaultSite** usuwa domyślną witrynę przypisaną do bramy.</span><span class="sxs-lookup"><span data-stu-id="810c4-109">**Remove-AzVirtualNetworkGatewayDefaultSite** removes the default site assigned to a gateway.</span></span>
<span data-ttu-id="810c4-110">Jeśli to zrobisz, musisz użyć Set-AzVirtualNetworkGatewayDefaultSite, aby przypisać nową witrynę domyślną, zanim Brama będzie mogła być używana do wymuszonego tunelowania.</span><span class="sxs-lookup"><span data-stu-id="810c4-110">If you do this you will need to use Set-AzVirtualNetworkGatewayDefaultSite to assign a new default site before the gateway can be used for forced tunneling.</span></span>

## <span data-ttu-id="810c4-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="810c4-111">EXAMPLES</span></span>

### <span data-ttu-id="810c4-112">Przykład 1: usuwanie domyślnej witryny przypisanej do bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="810c4-112">Example 1: Remove the default site assigned to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworknGateway $Gateway
```

<span data-ttu-id="810c4-113">W tym przykładzie jest usuwana witryna domyślna obecnie przypisana do bramy sieci wirtualnej o nazwie ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="810c4-113">This example removes the default site currently assigned to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="810c4-114">W pierwszym poleceniu użyto polecenia **Get-AzVirtualNetworkGateway** w celu utworzenia odwołania do obiektu do bramy; odwołanie do tego obiektu jest przechowywane w zmiennej o nazwie $Gateway.</span><span class="sxs-lookup"><span data-stu-id="810c4-114">The first command uses **Get-AzVirtualNetworkGateway** to create an object reference to the gateway; this object reference is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="810c4-115">Drugie polecenie korzysta z polecenia **Remove-AzVirtualNetworkGatewayDefaultSite** w celu usunięcia domyślnej witryny przypisanej do tej bramy.</span><span class="sxs-lookup"><span data-stu-id="810c4-115">The second command then uses **Remove-AzVirtualNetworkGatewayDefaultSite** to remove the default site assigned to that gateway.</span></span>

## <span data-ttu-id="810c4-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="810c4-116">PARAMETERS</span></span>

### <span data-ttu-id="810c4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="810c4-117">-DefaultProfile</span></span>
<span data-ttu-id="810c4-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="810c4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="810c4-119">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="810c4-119">-VirtualNetworkGateway</span></span>
<span data-ttu-id="810c4-120">Określa odwołanie do obiektu bramy sieci wirtualnej zawierającej domyślną witrynę do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="810c4-120">Specifies an object reference to the virtual network gateway containing the default site to be removed.</span></span>
<span data-ttu-id="810c4-121">Odwołanie do obiektu bramy sieci wirtualnej można utworzyć przy użyciu Get-AzVirtualNetworkGateway i określając nazwę bramy.</span><span class="sxs-lookup"><span data-stu-id="810c4-121">You can create an object reference to a virtual network gateway by using the Get-AzVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="810c4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="810c4-122">CommonParameters</span></span>
<span data-ttu-id="810c4-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="810c4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="810c4-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="810c4-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="810c4-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="810c4-125">INPUTS</span></span>

###  
<span data-ttu-id="810c4-126">To polecenie cmdlet akceptuje potokowe wystąpienia obiektu **Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="810c4-126">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="810c4-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="810c4-127">OUTPUTS</span></span>

###  
<span data-ttu-id="810c4-128">To polecenie cmdlet modyfikuje istniejące wystąpienia obiektu **Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="810c4-128">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="810c4-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="810c4-129">NOTES</span></span>

## <span data-ttu-id="810c4-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="810c4-130">RELATED LINKS</span></span>

[<span data-ttu-id="810c4-131">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="810c4-131">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="810c4-132">Set-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="810c4-132">Set-AzVirtualNetworkGatewayDefaultSite</span></span>](./Set-AzVirtualNetworkGatewayDefaultSite.md)


