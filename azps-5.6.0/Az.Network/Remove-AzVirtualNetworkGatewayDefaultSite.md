---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: ddf0f6687550e544aa22efbce772c0751a7b810e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006001"
---
# <span data-ttu-id="21e70-101">Remove-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="21e70-101">Remove-AzVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="21e70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21e70-102">SYNOPSIS</span></span>
<span data-ttu-id="21e70-103">Usuwa witrynę domyślną z bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="21e70-103">Removes the default site from a virtual network gateway.</span></span>

## <span data-ttu-id="21e70-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="21e70-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21e70-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="21e70-105">DESCRIPTION</span></span>
<span data-ttu-id="21e70-106">Polecenie cmdlet **Remove-AzVirtualNetworkGatewayDefaultSite** usuwa z bramy sieci wirtualnej witrynę sieci wirtualnej, która jest wymuszana przez wydychanie z sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="21e70-106">The **Remove-AzVirtualNetworkGatewayDefaultSite** cmdlet removes the forced tunneling default site from a virtual network gateway.</span></span>
<span data-ttu-id="21e70-107">Wymuszone podkoszowe zapewnia możliwość przekierowywania ruchu związanego z Internetem z maszyn wirtualnych platformy Azure do Twojej sieci lokalnej. umożliwia to inspekcję i inspekcję ruchu przed jego zwolnieniem.</span><span class="sxs-lookup"><span data-stu-id="21e70-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="21e70-108">Wymuszone podkołowy są wykonywane przy użyciu podkołowego wirtualnej sieci prywatnej (VPN); ten kork wymaga witryny domyślnej, bramy lokalnej, do której jest przekierowywany cały ruch internetowy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="21e70-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="21e70-109">**Remove-AzVirtualNetworkGatewayDefaultSite** usuwa domyślną witrynę przypisaną do bramy.</span><span class="sxs-lookup"><span data-stu-id="21e70-109">**Remove-AzVirtualNetworkGatewayDefaultSite** removes the default site assigned to a gateway.</span></span>
<span data-ttu-id="21e70-110">W takim przypadku konieczne będzie użycie programu Set-AzVirtualNetworkGatewayDefaultSite do przypisania nowej witryny domyślnej, aby brama była używana do wymuszonego wydychania na wiadki.</span><span class="sxs-lookup"><span data-stu-id="21e70-110">If you do this you will need to use Set-AzVirtualNetworkGatewayDefaultSite to assign a new default site before the gateway can be used for forced tunneling.</span></span>

## <span data-ttu-id="21e70-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="21e70-111">EXAMPLES</span></span>

### <span data-ttu-id="21e70-112">Przykład 1. Usuwanie witryny domyślnej przypisanej do bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="21e70-112">Example 1: Remove the default site assigned to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway $Gateway
```

<span data-ttu-id="21e70-113">W tym przykładzie jest usuwana witryna domyślna obecnie przypisana do bramy sieci wirtualnej o nazwie ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="21e70-113">This example removes the default site currently assigned to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="21e70-114">Pierwsze polecenie tworzy odwołanie do obiektu bramy za pomocą polecenia **Get-AzVirtualNetworkGateway;** to odwołanie do obiektu jest przechowywane w zmiennej o nazwie $Gateway.</span><span class="sxs-lookup"><span data-stu-id="21e70-114">The first command uses **Get-AzVirtualNetworkGateway** to create an object reference to the gateway; this object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="21e70-115">Drugie polecenie używa następnie **polecenia Remove-AzVirtualNetworkGatewayDefaultSite** w celu usunięcia witryny domyślnej przypisanej do tej bramy.</span><span class="sxs-lookup"><span data-stu-id="21e70-115">The second command then uses **Remove-AzVirtualNetworkGatewayDefaultSite** to remove the default site assigned to that gateway.</span></span>

## <span data-ttu-id="21e70-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21e70-116">PARAMETERS</span></span>

### <span data-ttu-id="21e70-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21e70-117">-DefaultProfile</span></span>
<span data-ttu-id="21e70-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="21e70-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21e70-119">— VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="21e70-119">-VirtualNetworkGateway</span></span>
<span data-ttu-id="21e70-120">Określa odwołanie do obiektu do bramy sieci wirtualnej zawierającej witrynę domyślną do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="21e70-120">Specifies an object reference to the virtual network gateway containing the default site to be removed.</span></span>
<span data-ttu-id="21e70-121">Możesz utworzyć odwołanie do obiektu do bramy sieci wirtualnej, używając Get-AzVirtualNetworkGateway i określając nazwę bramy.</span><span class="sxs-lookup"><span data-stu-id="21e70-121">You can create an object reference to a virtual network gateway by using the Get-AzVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="21e70-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21e70-122">CommonParameters</span></span>
<span data-ttu-id="21e70-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21e70-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21e70-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21e70-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21e70-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21e70-125">INPUTS</span></span>

### <span data-ttu-id="21e70-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="21e70-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="21e70-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21e70-127">OUTPUTS</span></span>

### <span data-ttu-id="21e70-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="21e70-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="21e70-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="21e70-129">NOTES</span></span>

## <span data-ttu-id="21e70-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="21e70-130">RELATED LINKS</span></span>

[<span data-ttu-id="21e70-131">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="21e70-131">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="21e70-132">Set-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="21e70-132">Set-AzVirtualNetworkGatewayDefaultSite</span></span>](./Set-AzVirtualNetworkGatewayDefaultSite.md)


