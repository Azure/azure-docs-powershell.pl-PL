---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 288812137887e4fc22308bba56a3fbdbeeb28c85
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179474"
---
# <span data-ttu-id="5a62a-101">Remove-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="5a62a-101">Remove-AzVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="5a62a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a62a-102">SYNOPSIS</span></span>
<span data-ttu-id="5a62a-103">Usuwa witrynę domyślną z bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5a62a-103">Removes the default site from a virtual network gateway.</span></span>

## <span data-ttu-id="5a62a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5a62a-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a62a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5a62a-105">DESCRIPTION</span></span>
<span data-ttu-id="5a62a-106">Polecenie cmdlet **Remove-AzVirtualNetworkGatewayDefaultSite** usuwa z bramy sieci wirtualnej witrynę sieci wirtualnej, która jest wymuszana przez wydychanie z sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5a62a-106">The **Remove-AzVirtualNetworkGatewayDefaultSite** cmdlet removes the forced tunneling default site from a virtual network gateway.</span></span>
<span data-ttu-id="5a62a-107">Wymuszone podkoszowe zapewnia możliwość przekierowywania ruchu związanego z Internetem z maszyn wirtualnych platformy Azure do Twojej sieci lokalnej. umożliwia to inspekcję i inspekcję ruchu przed jego zwolnieniem.</span><span class="sxs-lookup"><span data-stu-id="5a62a-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="5a62a-108">Wymuszone podkołowy są wykonywane przy użyciu podkołowego wirtualnej sieci prywatnej (VPN); ten kork wymaga witryny domyślnej, bramy lokalnej, do której jest przekierowywany cały ruch internetowy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5a62a-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="5a62a-109">**Remove-AzVirtualNetworkGatewayDefaultSite** usuwa domyślną witrynę przypisaną do bramy.</span><span class="sxs-lookup"><span data-stu-id="5a62a-109">**Remove-AzVirtualNetworkGatewayDefaultSite** removes the default site assigned to a gateway.</span></span>
<span data-ttu-id="5a62a-110">W takim przypadku konieczne będzie użycie programu Set-AzVirtualNetworkGatewayDefaultSite do przypisania nowej witryny domyślnej, aby brama była używana do wymuszania wydychania bram.</span><span class="sxs-lookup"><span data-stu-id="5a62a-110">If you do this you will need to use Set-AzVirtualNetworkGatewayDefaultSite to assign a new default site before the gateway can be used for forced tunneling.</span></span>

## <span data-ttu-id="5a62a-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5a62a-111">EXAMPLES</span></span>

### <span data-ttu-id="5a62a-112">Przykład 1. Usuwanie witryny domyślnej przypisanej do bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="5a62a-112">Example 1: Remove the default site assigned to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway $Gateway
```

<span data-ttu-id="5a62a-113">W tym przykładzie jest usuwana witryna domyślna obecnie przypisana do wirtualnej bramy sieciowej o nazwie ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="5a62a-113">This example removes the default site currently assigned to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="5a62a-114">Pierwsze polecenie tworzy odwołanie do obiektu bramy za pomocą polecenia **Get-AzVirtualNetworkGateway;** to odwołanie do obiektu jest przechowywane w zmiennej o nazwie $Gateway.</span><span class="sxs-lookup"><span data-stu-id="5a62a-114">The first command uses **Get-AzVirtualNetworkGateway** to create an object reference to the gateway; this object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="5a62a-115">Drugie polecenie używa następnie **polecenia Remove-AzVirtualNetworkGatewayDefaultSite** w celu usunięcia witryny domyślnej przypisanej do tej bramy.</span><span class="sxs-lookup"><span data-stu-id="5a62a-115">The second command then uses **Remove-AzVirtualNetworkGatewayDefaultSite** to remove the default site assigned to that gateway.</span></span>

## <span data-ttu-id="5a62a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a62a-116">PARAMETERS</span></span>

### <span data-ttu-id="5a62a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a62a-117">-DefaultProfile</span></span>
<span data-ttu-id="5a62a-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5a62a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a62a-119">— VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5a62a-119">-VirtualNetworkGateway</span></span>
<span data-ttu-id="5a62a-120">Określa odwołanie do obiektu do bramy sieci wirtualnej zawierającej witrynę domyślną do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="5a62a-120">Specifies an object reference to the virtual network gateway containing the default site to be removed.</span></span>
<span data-ttu-id="5a62a-121">Możesz utworzyć odwołanie do obiektu do bramy sieci wirtualnej, używając Get-AzVirtualNetworkGateway i określając nazwę bramy.</span><span class="sxs-lookup"><span data-stu-id="5a62a-121">You can create an object reference to a virtual network gateway by using the Get-AzVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="5a62a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a62a-122">CommonParameters</span></span>
<span data-ttu-id="5a62a-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a62a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a62a-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a62a-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a62a-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a62a-125">INPUTS</span></span>

### <span data-ttu-id="5a62a-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5a62a-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="5a62a-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5a62a-127">OUTPUTS</span></span>

### <span data-ttu-id="5a62a-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5a62a-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="5a62a-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5a62a-129">NOTES</span></span>

## <span data-ttu-id="5a62a-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5a62a-130">RELATED LINKS</span></span>

[<span data-ttu-id="5a62a-131">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5a62a-131">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="5a62a-132">Set-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="5a62a-132">Set-AzVirtualNetworkGatewayDefaultSite</span></span>](./Set-AzVirtualNetworkGatewayDefaultSite.md)


