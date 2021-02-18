---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 2c2b2136d01d96a219243a3ccd8f26fdcfaeeec3
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100410042"
---
# <span data-ttu-id="ad6d7-101">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="ad6d7-101">Get-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="ad6d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad6d7-102">SYNOPSIS</span></span>
<span data-ttu-id="ad6d7-103">Pobiera zasób dziennika przepływów lub listę zasobów dziennika przepływów w określonej subskrypcji i regionie.</span><span class="sxs-lookup"><span data-stu-id="ad6d7-103">Gets a flow log resource or a list of flow log resources in the specified subscription and region.</span></span>

## <span data-ttu-id="ad6d7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ad6d7-104">SYNTAX</span></span>

### <span data-ttu-id="ad6d7-105">SetByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="ad6d7-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad6d7-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ad6d7-106">SetByResource</span></span>
```
Get-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad6d7-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="ad6d7-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherFlowLog -Location <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ad6d7-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ad6d7-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherFlowLog -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ad6d7-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="ad6d7-109">DESCRIPTION</span></span>
<span data-ttu-id="ad6d7-110">Pobiera zasób dziennika przepływów lub listę zasobów dziennika przepływu w określonej subskrypcji i regionie.</span><span class="sxs-lookup"><span data-stu-id="ad6d7-110">Gets a flow log resource or a list of flow log resources in the specified subscription and region.</span></span>

## <span data-ttu-id="ad6d7-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ad6d7-111">EXAMPLES</span></span>

### <span data-ttu-id="ad6d7-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ad6d7-112">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkWatcherFlowLog -Location eastus -Name pstest
```

<span data-ttu-id="ad6d7-113">Name : pstest Id : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState : Succeeded Location : eastus TargetResourceId : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled : True RetentionPolicy : { "Days": 5, "Enabled": true } Format : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": true, "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb", "workspaceRegion": "eastus", "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr oups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace", "trafficAnalyticsInterval": 60 }</span><span class="sxs-lookup"><span data-stu-id="ad6d7-113">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled                    : True RetentionPolicy            : { "Days": 5, "Enabled": true } Format                     : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": true, "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb", "workspaceRegion": "eastus", "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr oups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace", "trafficAnalyticsInterval": 60 }</span></span>

## <span data-ttu-id="ad6d7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad6d7-114">PARAMETERS</span></span>

### <span data-ttu-id="ad6d7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad6d7-115">-DefaultProfile</span></span>
<span data-ttu-id="ad6d7-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ad6d7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad6d7-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ad6d7-117">-Location</span></span>
<span data-ttu-id="ad6d7-118">Lokalizacja czujki sieci.</span><span class="sxs-lookup"><span data-stu-id="ad6d7-118">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad6d7-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ad6d7-119">-Name</span></span>
<span data-ttu-id="ad6d7-120">Nazwa dziennika przepływu.</span><span class="sxs-lookup"><span data-stu-id="ad6d7-120">The flow log name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: FlowLogName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad6d7-121">— NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ad6d7-121">-NetworkWatcher</span></span>
<span data-ttu-id="ad6d7-122">Zasób obserwowania sieci.</span><span class="sxs-lookup"><span data-stu-id="ad6d7-122">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad6d7-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="ad6d7-123">-NetworkWatcherName</span></span>
<span data-ttu-id="ad6d7-124">Nazwa osoby oglądacej sieć.</span><span class="sxs-lookup"><span data-stu-id="ad6d7-124">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad6d7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad6d7-125">-ResourceGroupName</span></span>
<span data-ttu-id="ad6d7-126">Nazwa grupy zasobów obserwowanych sieci.</span><span class="sxs-lookup"><span data-stu-id="ad6d7-126">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad6d7-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad6d7-127">-ResourceId</span></span>
<span data-ttu-id="ad6d7-128">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="ad6d7-128">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad6d7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad6d7-129">CommonParameters</span></span>
<span data-ttu-id="ad6d7-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad6d7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad6d7-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ad6d7-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad6d7-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad6d7-132">INPUTS</span></span>

### <span data-ttu-id="ad6d7-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ad6d7-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="ad6d7-134">System.String</span><span class="sxs-lookup"><span data-stu-id="ad6d7-134">System.String</span></span>

## <span data-ttu-id="ad6d7-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad6d7-135">OUTPUTS</span></span>

### <span data-ttu-id="ad6d7-136">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="ad6d7-136">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="ad6d7-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ad6d7-137">NOTES</span></span>

## <span data-ttu-id="ad6d7-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ad6d7-138">RELATED LINKS</span></span>

[<span data-ttu-id="ad6d7-139">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ad6d7-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="ad6d7-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ad6d7-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="ad6d7-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ad6d7-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="ad6d7-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="ad6d7-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="ad6d7-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="ad6d7-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="ad6d7-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="ad6d7-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="ad6d7-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="ad6d7-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="ad6d7-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ad6d7-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ad6d7-147">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="ad6d7-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="ad6d7-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ad6d7-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ad6d7-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ad6d7-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ad6d7-150">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ad6d7-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ad6d7-151">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad6d7-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="ad6d7-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="ad6d7-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="ad6d7-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="ad6d7-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="ad6d7-154">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ad6d7-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ad6d7-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ad6d7-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ad6d7-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ad6d7-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ad6d7-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="ad6d7-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="ad6d7-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ad6d7-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ad6d7-159">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ad6d7-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ad6d7-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="ad6d7-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="ad6d7-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="ad6d7-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="ad6d7-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="ad6d7-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="ad6d7-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="ad6d7-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="ad6d7-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="ad6d7-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="ad6d7-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ad6d7-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ad6d7-166">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="ad6d7-166">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="ad6d7-167">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="ad6d7-167">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="ad6d7-168">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="ad6d7-168">Remove-AzNetworkWatcherFlowLog</span></span>](./Remove-AzNetworkWatcherFlowLog.md)
