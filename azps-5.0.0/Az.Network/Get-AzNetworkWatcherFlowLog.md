---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 5f4322ba81cdae5bdb0b33c2658a6d7934ed638d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225176"
---
# <span data-ttu-id="91dac-101">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="91dac-101">Get-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="91dac-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="91dac-102">SYNOPSIS</span></span>
<span data-ttu-id="91dac-103">Pobiera zasób dziennika przepływu lub listę zasobów dziennika przepływu w określonym abonamentzie i regionie.</span><span class="sxs-lookup"><span data-stu-id="91dac-103">Gets a flow log resource or a list of flow log resources in the specified subscription and region.</span></span>

## <span data-ttu-id="91dac-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="91dac-104">SYNTAX</span></span>

### <span data-ttu-id="91dac-105">SetByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="91dac-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91dac-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="91dac-106">SetByResource</span></span>
```
Get-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91dac-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="91dac-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherFlowLog -Location <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="91dac-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="91dac-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherFlowLog -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="91dac-109">Opis</span><span class="sxs-lookup"><span data-stu-id="91dac-109">DESCRIPTION</span></span>
<span data-ttu-id="91dac-110">Pobiera zasób dziennika przepływu lub listę zasobów dziennika przepływu w określonym abonamentzie i regionie.</span><span class="sxs-lookup"><span data-stu-id="91dac-110">Gets a flow log resource or a list of flow log resources in the specified subscription and region.</span></span>

## <span data-ttu-id="91dac-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="91dac-111">EXAMPLES</span></span>

### <span data-ttu-id="91dac-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="91dac-112">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkWatcherFlowLog -Location eastus -Name pstest
```

<span data-ttu-id="91dac-113">Nazwa: PStest ID:/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid nastawieni/Microsoft. Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest ETag: W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState: powiodło się lokalizacja:, TargetResourceId:/subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide RS/Microsoft. Network/networkSecurityGroups/MyNSG StorageId:/subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft. Storage/storageAccounts/moja magazyn włączone: prawda RetentionPolicy: {"dni": 5; {"Type": "JSON", "wersja": 2} FlowAnalyticsConfiguration: {"networkWatcherFlowAnalyticsConfiguration": {"Enabled": prawda; "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb", "workspaceRegion": "East", "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr oups/FlowLogsV2Demo, Providers/Microsoft. OperationalInsights/obszary robocze", "trafficAnalyticsInterval": 60}</span><span class="sxs-lookup"><span data-stu-id="91dac-113">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled                    : True RetentionPolicy            : { "Days": 5, "Enabled": true } Format                     : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": true, "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb", "workspaceRegion": "eastus", "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr oups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace", "trafficAnalyticsInterval": 60 }</span></span>

## <span data-ttu-id="91dac-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="91dac-114">PARAMETERS</span></span>

### <span data-ttu-id="91dac-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91dac-115">-DefaultProfile</span></span>
<span data-ttu-id="91dac-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="91dac-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91dac-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="91dac-117">-Location</span></span>
<span data-ttu-id="91dac-118">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="91dac-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="91dac-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="91dac-119">-Name</span></span>
<span data-ttu-id="91dac-120">Nazwa dziennika przepływu.</span><span class="sxs-lookup"><span data-stu-id="91dac-120">The flow log name.</span></span>

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

### <span data-ttu-id="91dac-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="91dac-121">-NetworkWatcher</span></span>
<span data-ttu-id="91dac-122">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="91dac-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="91dac-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="91dac-123">-NetworkWatcherName</span></span>
<span data-ttu-id="91dac-124">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="91dac-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="91dac-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91dac-125">-ResourceGroupName</span></span>
<span data-ttu-id="91dac-126">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="91dac-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="91dac-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="91dac-127">-ResourceId</span></span>
<span data-ttu-id="91dac-128">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="91dac-128">Resource ID.</span></span>

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

### <span data-ttu-id="91dac-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91dac-129">CommonParameters</span></span>
<span data-ttu-id="91dac-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91dac-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91dac-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91dac-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91dac-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="91dac-132">INPUTS</span></span>

### <span data-ttu-id="91dac-133">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="91dac-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="91dac-134">System. String</span><span class="sxs-lookup"><span data-stu-id="91dac-134">System.String</span></span>

## <span data-ttu-id="91dac-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="91dac-135">OUTPUTS</span></span>

### <span data-ttu-id="91dac-136">Microsoft. Azure. Commands. Network. models. PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="91dac-136">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="91dac-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="91dac-137">NOTES</span></span>

## <span data-ttu-id="91dac-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="91dac-138">RELATED LINKS</span></span>

[<span data-ttu-id="91dac-139">Nowe — AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="91dac-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="91dac-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="91dac-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="91dac-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="91dac-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="91dac-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="91dac-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="91dac-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="91dac-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="91dac-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="91dac-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="91dac-145">Start — AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="91dac-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="91dac-146">Nowe — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="91dac-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="91dac-147">Nowe — AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="91dac-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="91dac-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="91dac-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="91dac-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="91dac-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="91dac-150">Zatrzymaj — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="91dac-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="91dac-151">Nowe — AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="91dac-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="91dac-152">Test — AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="91dac-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="91dac-153">Test — AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="91dac-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="91dac-154">Zatrzymaj — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="91dac-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="91dac-155">Start — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="91dac-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="91dac-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="91dac-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="91dac-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="91dac-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="91dac-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="91dac-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="91dac-159">Nowe — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="91dac-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="91dac-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="91dac-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="91dac-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="91dac-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="91dac-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="91dac-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="91dac-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="91dac-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="91dac-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="91dac-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="91dac-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="91dac-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="91dac-166">Nowe — AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="91dac-166">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="91dac-167">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="91dac-167">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="91dac-168">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="91dac-168">Remove-AzNetworkWatcherFlowLog</span></span>](./Remove-AzNetworkWatcherFlowLog.md)
