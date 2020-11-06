---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: a2c6c51a1f9f22130436e7d0a0d5fd888bccfb99
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543627"
---
# <span data-ttu-id="fdd89-101">Remove-AzureRmVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="fdd89-101">Remove-AzureRmVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="fdd89-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fdd89-102">SYNOPSIS</span></span>
<span data-ttu-id="fdd89-103">Usuwa witrynę domyślną z bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fdd89-103">Removes the default site from a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdd89-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fdd89-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdd89-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fdd89-105">DESCRIPTION</span></span>
<span data-ttu-id="fdd89-106">Polecenie cmdlet **Remove-AzureRmVirtualNetworkGatewayDefaultSite** umożliwia usunięcie domyślnej witryny tunelowania wymuszonego z bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fdd89-106">The **Remove-AzureRmVirtualNetworkGatewayDefaultSite** cmdlet removes the forced tunneling default site from a virtual network gateway.</span></span>
<span data-ttu-id="fdd89-107">Wymuszone tunelowanie zapewnia sposób na przekierowanie ruchu związanego z Internetem z maszyn wirtualnych platformy Azure do sieci lokalnej. Dzięki temu można sprawdzać ruch i prowadzić inspekcję ruchu przed jego zwolnieniem.</span><span class="sxs-lookup"><span data-stu-id="fdd89-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="fdd89-108">Tunelowanie wymuszone jest realizowane przy użyciu tunelu wirtualnej sieci prywatnej (VPN); ten tunel wymaga witryny domyślnej, bramy lokalnej, w której jest przekierowywany cały ruch związany z Internetem usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="fdd89-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="fdd89-109">**Remove-AzureRmVirtualNetworkGatewayDefaultSite** usuwa domyślną witrynę przypisaną do bramy.</span><span class="sxs-lookup"><span data-stu-id="fdd89-109">**Remove-AzureRmVirtualNetworkGatewayDefaultSite** removes the default site assigned to a gateway.</span></span>
<span data-ttu-id="fdd89-110">Jeśli to zrobisz, musisz użyć Set-AzureRmVirtualNetworkGatewayDefaultSite, aby przypisać nową witrynę domyślną, zanim Brama będzie mogła być używana do wymuszonego tunelowania.</span><span class="sxs-lookup"><span data-stu-id="fdd89-110">If you do this you will need to use Set-AzureRmVirtualNetworkGatewayDefaultSite to assign a new default site before the gateway can be used for forced tunneling.</span></span>

## <span data-ttu-id="fdd89-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fdd89-111">EXAMPLES</span></span>

### <span data-ttu-id="fdd89-112">Przykład 1: usuwanie domyślnej witryny przypisanej do bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="fdd89-112">Example 1: Remove the default site assigned to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway $Gateway
```

<span data-ttu-id="fdd89-113">W tym przykładzie jest usuwana witryna domyślna obecnie przypisana do bramy sieci wirtualnej o nazwie ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="fdd89-113">This example removes the default site currently assigned to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="fdd89-114">W pierwszym poleceniu użyto polecenia **Get-AzureRmVirtualNetworkGateway** w celu utworzenia odwołania do obiektu do bramy; odwołanie do tego obiektu jest przechowywane w zmiennej o nazwie $Gateway.</span><span class="sxs-lookup"><span data-stu-id="fdd89-114">The first command uses **Get-AzureRmVirtualNetworkGateway** to create an object reference to the gateway; this object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="fdd89-115">Drugie polecenie korzysta z polecenia **Remove-AzureRmVirtualNetworkGatewayDefaultSite** w celu usunięcia domyślnej witryny przypisanej do tej bramy.</span><span class="sxs-lookup"><span data-stu-id="fdd89-115">The second command then uses **Remove-AzureRmVirtualNetworkGatewayDefaultSite** to remove the default site assigned to that gateway.</span></span>

## <span data-ttu-id="fdd89-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fdd89-116">PARAMETERS</span></span>

### <span data-ttu-id="fdd89-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdd89-117">-DefaultProfile</span></span>
<span data-ttu-id="fdd89-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fdd89-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fdd89-119">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fdd89-119">-VirtualNetworkGateway</span></span>
<span data-ttu-id="fdd89-120">Określa odwołanie do obiektu bramy sieci wirtualnej zawierającej domyślną witrynę do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="fdd89-120">Specifies an object reference to the virtual network gateway containing the default site to be removed.</span></span>
<span data-ttu-id="fdd89-121">Odwołanie do obiektu bramy sieci wirtualnej można utworzyć przy użyciu Get-AzureRmVirtualNetworkGateway i określając nazwę bramy.</span><span class="sxs-lookup"><span data-stu-id="fdd89-121">You can create an object reference to a virtual network gateway by using the Get-AzureRmVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="fdd89-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdd89-122">CommonParameters</span></span>
<span data-ttu-id="fdd89-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdd89-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdd89-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdd89-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdd89-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fdd89-125">INPUTS</span></span>

### <span data-ttu-id="fdd89-126">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fdd89-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="fdd89-127">Parametry: VirtualNetworkGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fdd89-127">Parameters: VirtualNetworkGateway (ByValue)</span></span>

## <span data-ttu-id="fdd89-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fdd89-128">OUTPUTS</span></span>

### <span data-ttu-id="fdd89-129">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fdd89-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="fdd89-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fdd89-130">NOTES</span></span>

## <span data-ttu-id="fdd89-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fdd89-131">RELATED LINKS</span></span>

[<span data-ttu-id="fdd89-132">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fdd89-132">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="fdd89-133">Set-AzureRmVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="fdd89-133">Set-AzureRmVirtualNetworkGatewayDefaultSite</span></span>](./Set-AzureRmVirtualNetworkGatewayDefaultSite.md)


