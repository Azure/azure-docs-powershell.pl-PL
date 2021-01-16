---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcher.md
ms.openlocfilehash: dc8d3a3db0eaa76974e02a62111b022ed81524b0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379911"
---
# <span data-ttu-id="d0306-101">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d0306-101">Get-AzNetworkWatcher</span></span>

## <span data-ttu-id="d0306-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d0306-102">SYNOPSIS</span></span>
<span data-ttu-id="d0306-103">Pobiera właściwości obserwatora sieci</span><span class="sxs-lookup"><span data-stu-id="d0306-103">Gets the properties of a Network Watcher</span></span>

## <span data-ttu-id="d0306-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d0306-104">SYNTAX</span></span>

### <span data-ttu-id="d0306-105">Lista</span><span class="sxs-lookup"><span data-stu-id="d0306-105">List</span></span>
```
Get-AzNetworkWatcher [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d0306-106">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="d0306-106">SetByLocation</span></span>
```
Get-AzNetworkWatcher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0306-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d0306-107">DESCRIPTION</span></span>
<span data-ttu-id="d0306-108">Polecenie cmdlet Get-AzNetworkWatcher powoduje wyświetlenie co najmniej jednego zasobu obserwatora sieci Azure.</span><span class="sxs-lookup"><span data-stu-id="d0306-108">The Get-AzNetworkWatcher cmdlet gets one or more Azure Network Watcher resources.</span></span>

## <span data-ttu-id="d0306-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d0306-109">EXAMPLES</span></span>

### <span data-ttu-id="d0306-110">Przykład 1: uzyskiwanie monitora sieci</span><span class="sxs-lookup"><span data-stu-id="d0306-110">Example 1: Get a Network Watcher</span></span>
```
Get-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="d0306-111">Pobiera Monitor sieci o nazwie NetworkWatcher_westcentralus w grupie zasobów NetworkWatcherRG.</span><span class="sxs-lookup"><span data-stu-id="d0306-111">Gets the Network Watcher named NetworkWatcher_westcentralus in the resource group NetworkWatcherRG.</span></span>

### <span data-ttu-id="d0306-112">Przykład 2: Wyświetlanie listy obserwatorów sieciowych przy użyciu funkcji filtrowania</span><span class="sxs-lookup"><span data-stu-id="d0306-112">Example 2: List Network Watchers using filtering</span></span>
```
Get-AzNetworkWatcher -Name NetworkWatcher*

Name              : NetworkWatcher_westcentralus1
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus1
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded

Name              : NetworkWatcher_westcentralus2
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus2
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="d0306-113">Pobiera obserwatorów sieciowych rozpoczynający się od "NetworkWatcher"</span><span class="sxs-lookup"><span data-stu-id="d0306-113">Gets the Network Watchers that start with "NetworkWatcher"</span></span>

## <span data-ttu-id="d0306-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d0306-114">PARAMETERS</span></span>

### <span data-ttu-id="d0306-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0306-115">-DefaultProfile</span></span>
<span data-ttu-id="d0306-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d0306-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0306-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d0306-117">-Location</span></span>
<span data-ttu-id="d0306-118">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="d0306-118">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0306-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d0306-119">-Name</span></span>
<span data-ttu-id="d0306-120">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="d0306-120">The network watcher name.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="d0306-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0306-121">-ResourceGroupName</span></span>
<span data-ttu-id="d0306-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d0306-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="d0306-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0306-123">CommonParameters</span></span>
<span data-ttu-id="d0306-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0306-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0306-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0306-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0306-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0306-126">INPUTS</span></span>

### <span data-ttu-id="d0306-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d0306-127">None</span></span>

## <span data-ttu-id="d0306-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d0306-128">OUTPUTS</span></span>

### <span data-ttu-id="d0306-129">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d0306-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="d0306-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d0306-130">NOTES</span></span>
<span data-ttu-id="d0306-131">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, obserwator sieci</span><span class="sxs-lookup"><span data-stu-id="d0306-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span> 

## <span data-ttu-id="d0306-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d0306-132">RELATED LINKS</span></span>

[<span data-ttu-id="d0306-133">Nowe — AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d0306-133">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="d0306-134">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d0306-134">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="d0306-135">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d0306-135">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="d0306-136">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d0306-136">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="d0306-137">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d0306-137">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d0306-138">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d0306-138">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="d0306-139">Start — AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d0306-139">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="d0306-140">Nowe — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d0306-140">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d0306-141">Nowe — AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d0306-141">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="d0306-142">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d0306-142">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d0306-143">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d0306-143">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d0306-144">Zatrzymaj — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d0306-144">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d0306-145">Nowe — AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0306-145">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="d0306-146">Test — AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d0306-146">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="d0306-147">Test — AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="d0306-147">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="d0306-148">Zatrzymaj — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d0306-148">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d0306-149">Start — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d0306-149">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d0306-150">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d0306-150">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d0306-151">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="d0306-151">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="d0306-152">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d0306-152">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d0306-153">Nowe — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d0306-153">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d0306-154">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="d0306-154">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="d0306-155">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="d0306-155">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="d0306-156">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="d0306-156">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="d0306-157">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="d0306-157">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="d0306-158">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="d0306-158">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="d0306-159">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d0306-159">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
