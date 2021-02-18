---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcher.md
ms.openlocfilehash: 8ef85845221a84b26bf26e2116898d739325bc40
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100410620"
---
# <span data-ttu-id="2b3e9-101">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2b3e9-101">Get-AzNetworkWatcher</span></span>

## <span data-ttu-id="2b3e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b3e9-102">SYNOPSIS</span></span>
<span data-ttu-id="2b3e9-103">Pobiera właściwości obserwowania sieci</span><span class="sxs-lookup"><span data-stu-id="2b3e9-103">Gets the properties of a Network Watcher</span></span>

## <span data-ttu-id="2b3e9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2b3e9-104">SYNTAX</span></span>

### <span data-ttu-id="2b3e9-105">Lista</span><span class="sxs-lookup"><span data-stu-id="2b3e9-105">List</span></span>
```
Get-AzNetworkWatcher [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b3e9-106">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="2b3e9-106">SetByLocation</span></span>
```
Get-AzNetworkWatcher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b3e9-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="2b3e9-107">DESCRIPTION</span></span>
<span data-ttu-id="2b3e9-108">Polecenie Get-AzNetworkWatcher pobiera jeden lub więcej zasobów usługi Azure Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-108">The Get-AzNetworkWatcher cmdlet gets one or more Azure Network Watcher resources.</span></span>

## <span data-ttu-id="2b3e9-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2b3e9-109">EXAMPLES</span></span>

### <span data-ttu-id="2b3e9-110">Przykład 1. Uzyskiwanie czujki sieci</span><span class="sxs-lookup"><span data-stu-id="2b3e9-110">Example 1: Get a Network Watcher</span></span>
```
Get-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="2b3e9-111">Pobiera nazwę Network Watcher NetworkWatcher_westcentralus w grupie zasobów NetworkWatcherRG.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-111">Gets the Network Watcher named NetworkWatcher_westcentralus in the resource group NetworkWatcherRG.</span></span>

### <span data-ttu-id="2b3e9-112">Przykład 2. Lista obserwowanych sieci przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="2b3e9-112">Example 2: List Network Watchers using filtering</span></span>
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

<span data-ttu-id="2b3e9-113">Pobiera obserwowanych sieci, którzy zaczynają od "NetworkWatcher"</span><span class="sxs-lookup"><span data-stu-id="2b3e9-113">Gets the Network Watchers that start with "NetworkWatcher"</span></span>

## <span data-ttu-id="2b3e9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2b3e9-114">PARAMETERS</span></span>

### <span data-ttu-id="2b3e9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b3e9-115">-DefaultProfile</span></span>
<span data-ttu-id="2b3e9-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b3e9-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2b3e9-117">-Location</span></span>
<span data-ttu-id="2b3e9-118">Lokalizacja czujki sieci.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="2b3e9-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2b3e9-119">-Name</span></span>
<span data-ttu-id="2b3e9-120">Nazwa sieciowego czujki.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-120">The network watcher name.</span></span>

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

### <span data-ttu-id="2b3e9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b3e9-121">-ResourceGroupName</span></span>
<span data-ttu-id="2b3e9-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-122">The resource group name.</span></span>

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

### <span data-ttu-id="2b3e9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b3e9-123">CommonParameters</span></span>
<span data-ttu-id="2b3e9-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b3e9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b3e9-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2b3e9-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b3e9-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2b3e9-126">INPUTS</span></span>

### <span data-ttu-id="2b3e9-127">Brak</span><span class="sxs-lookup"><span data-stu-id="2b3e9-127">None</span></span>

## <span data-ttu-id="2b3e9-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2b3e9-128">OUTPUTS</span></span>

### <span data-ttu-id="2b3e9-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2b3e9-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="2b3e9-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2b3e9-130">NOTES</span></span>
<span data-ttu-id="2b3e9-131">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span><span class="sxs-lookup"><span data-stu-id="2b3e9-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span> 

## <span data-ttu-id="2b3e9-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2b3e9-132">RELATED LINKS</span></span>

[<span data-ttu-id="2b3e9-133">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2b3e9-133">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="2b3e9-134">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2b3e9-134">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="2b3e9-135">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2b3e9-135">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="2b3e9-136">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="2b3e9-136">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="2b3e9-137">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="2b3e9-137">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="2b3e9-138">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="2b3e9-138">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="2b3e9-139">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="2b3e9-139">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="2b3e9-140">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2b3e9-140">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2b3e9-141">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="2b3e9-141">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="2b3e9-142">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2b3e9-142">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2b3e9-143">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2b3e9-143">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2b3e9-144">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2b3e9-144">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2b3e9-145">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b3e9-145">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="2b3e9-146">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2b3e9-146">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="2b3e9-147">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="2b3e9-147">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="2b3e9-148">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2b3e9-148">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2b3e9-149">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2b3e9-149">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2b3e9-150">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2b3e9-150">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2b3e9-151">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="2b3e9-151">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="2b3e9-152">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2b3e9-152">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2b3e9-153">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2b3e9-153">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2b3e9-154">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="2b3e9-154">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="2b3e9-155">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="2b3e9-155">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="2b3e9-156">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="2b3e9-156">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="2b3e9-157">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="2b3e9-157">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="2b3e9-158">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="2b3e9-158">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="2b3e9-159">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2b3e9-159">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
