---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcher.md
ms.openlocfilehash: d312eaa9f75fc13ecba0b00aa0fea64b5d3ea2e2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890746"
---
# <span data-ttu-id="69ba9-101">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="69ba9-101">Get-AzNetworkWatcher</span></span>

## <span data-ttu-id="69ba9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="69ba9-102">SYNOPSIS</span></span>
<span data-ttu-id="69ba9-103">Pobiera właściwości obserwatora sieci</span><span class="sxs-lookup"><span data-stu-id="69ba9-103">Gets the properties of a Network Watcher</span></span>

## <span data-ttu-id="69ba9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="69ba9-104">SYNTAX</span></span>

### <span data-ttu-id="69ba9-105">Pobierz</span><span class="sxs-lookup"><span data-stu-id="69ba9-105">Get</span></span>
```
Get-AzNetworkWatcher -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="69ba9-106">Lista</span><span class="sxs-lookup"><span data-stu-id="69ba9-106">List</span></span>
```
Get-AzNetworkWatcher [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="69ba9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="69ba9-107">DESCRIPTION</span></span>
<span data-ttu-id="69ba9-108">Polecenie cmdlet Get-AzNetworkWatcher powoduje wyświetlenie co najmniej jednego zasobu obserwatora sieci Azure.</span><span class="sxs-lookup"><span data-stu-id="69ba9-108">The Get-AzNetworkWatcher cmdlet gets one or more Azure Network Watcher resources.</span></span>

## <span data-ttu-id="69ba9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="69ba9-109">EXAMPLES</span></span>

### <span data-ttu-id="69ba9-110">--------------------------Przykład 1: uzyskiwanie monitora sieci--------------------------</span><span class="sxs-lookup"><span data-stu-id="69ba9-110">--------------------------  Example 1: Get a Network Watcher  --------------------------</span></span>
```
Get-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="69ba9-111">Pobiera Monitor sieci o nazwie NetworkWatcher_westcentralus w grupie zasobów NetworkWatcherRG.</span><span class="sxs-lookup"><span data-stu-id="69ba9-111">Gets the Network Watcher named NetworkWatcher_westcentralus in the resource group NetworkWatcherRG.</span></span>

## <span data-ttu-id="69ba9-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="69ba9-112">PARAMETERS</span></span>

### <span data-ttu-id="69ba9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69ba9-113">-DefaultProfile</span></span>
<span data-ttu-id="69ba9-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="69ba9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69ba9-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="69ba9-115">-Name</span></span>
<span data-ttu-id="69ba9-116">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="69ba9-116">The network watcher name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69ba9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69ba9-117">-ResourceGroupName</span></span>
<span data-ttu-id="69ba9-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="69ba9-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69ba9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69ba9-119">CommonParameters</span></span>
<span data-ttu-id="69ba9-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69ba9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69ba9-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69ba9-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69ba9-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69ba9-122">INPUTS</span></span>

### <span data-ttu-id="69ba9-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="69ba9-123">None</span></span>

## <span data-ttu-id="69ba9-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="69ba9-124">OUTPUTS</span></span>

### <span data-ttu-id="69ba9-125">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="69ba9-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="69ba9-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="69ba9-126">NOTES</span></span>
<span data-ttu-id="69ba9-127">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, obserwator sieci</span><span class="sxs-lookup"><span data-stu-id="69ba9-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span> 

## <span data-ttu-id="69ba9-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="69ba9-128">RELATED LINKS</span></span>

[<span data-ttu-id="69ba9-129">Nowe — AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="69ba9-129">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="69ba9-130">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="69ba9-130">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="69ba9-131">Nowe — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="69ba9-131">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="69ba9-132">Nowe — AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="69ba9-132">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="69ba9-133">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="69ba9-133">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="69ba9-134">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="69ba9-134">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="69ba9-135">Zatrzymaj — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="69ba9-135">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="69ba9-136">Test — AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="69ba9-136">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="69ba9-137">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="69ba9-137">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="69ba9-138">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="69ba9-138">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="69ba9-139">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="69ba9-139">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="69ba9-140">Start — AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="69ba9-140">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
