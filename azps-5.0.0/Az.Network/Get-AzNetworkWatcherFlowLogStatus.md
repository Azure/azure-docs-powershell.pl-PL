---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherflowlogstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
ms.openlocfilehash: dd88c40876bf3ceb5f90a7088f5943fcf5f18ce8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318061"
---
# <span data-ttu-id="7d904-101">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="7d904-101">Get-AzNetworkWatcherFlowLogStatus</span></span>

## <span data-ttu-id="7d904-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7d904-102">SYNOPSIS</span></span>
<span data-ttu-id="7d904-103">Pobiera stan rejestrowania przepływu dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="7d904-103">Gets the status of flow logging on a resource.</span></span>

## <span data-ttu-id="7d904-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7d904-104">SYNTAX</span></span>

### <span data-ttu-id="7d904-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7d904-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d904-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="7d904-106">SetByName</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d904-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="7d904-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -Location <String> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d904-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7d904-108">DESCRIPTION</span></span>
<span data-ttu-id="7d904-109">Polecenie cmdlet Get-AzNetworkWatcherFlowLogStatus Pobiera stan rejestrowania przepływu dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="7d904-109">The Get-AzNetworkWatcherFlowLogStatus cmdlet Gets the status of flow logging on a resource.</span></span> <span data-ttu-id="7d904-110">Stan uwzględnia, czy w przypadku danego zasobu jest włączone rejestrowanie przepływu, skonfigurowane konto magazynu do wysyłania dzienników oraz zasady przechowywania dzienników.</span><span class="sxs-lookup"><span data-stu-id="7d904-110">The status includes whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="7d904-111">W przypadku rejestrowania przepływów są obsługiwane obecnie grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="7d904-111">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="7d904-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7d904-112">EXAMPLES</span></span>

### <span data-ttu-id="7d904-113">Przykład 1: uzyskiwanie stanu rejestrowania przepływu dla określonego NSG</span><span class="sxs-lookup"><span data-stu-id="7d904-113">Example 1: Get the Flow Logging Status for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG

PS C:\> Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher $NW -TargetResourceId $nsg.Id

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
Properties       : {
                     "Enabled": true,
                     "RetentionPolicy": {
                       "Days": 0,
                       "Enabled": false
                     },
                     "StorageId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"
                     "Format"         : {
                       "Type ": "Json",
                       "Version": 1
                     }
                   }
```

<span data-ttu-id="7d904-114">W tym przykładzie jest wyświetlany stan rejestrowania przepływu dla grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="7d904-114">In this example we get the flow logging status for a Network Security Group.</span></span> <span data-ttu-id="7d904-115">Określony NSG ma włączone rejestrowanie przepływów, format domyślny i nie ustawiono zasad przechowywania.</span><span class="sxs-lookup"><span data-stu-id="7d904-115">The specified NSG has flow logging enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="7d904-116">Przykład 2: uzyskiwanie rejestrowania przepływu i stanu analizy ruchu dla określonego NSG</span><span class="sxs-lookup"><span data-stu-id="7d904-116">Example 2: Get the Flow Logging and Traffic Analytics Status for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG

PS C:\> Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher $NW -TargetResourceId $nsg.Id

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
Format           : {
                     "Type ": "Json",
                     "Version": 1
                   }
FlowAnalyticsConfiguration : {
            "networkWatcherFlowAnalyticsConfiguration": {
              "enabled": true,
              "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb",
              "workspaceRegion": "WorkspaceLocation",
              "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/WorkspaceRg/providers/microsoft.operationalinsights/workspaces/WorkspaceName",
              "TrafficAnalyticsInterval": 60
            }
          }
```

<span data-ttu-id="7d904-117">W tym przykładzie jest wyświetlany stan rejestrowania przepływu i analizy ruchu dla grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="7d904-117">In this example we get the flow logging and Traffic Analytics status for a Network Security Group.</span></span> <span data-ttu-id="7d904-118">Określony NSG ma włączone rejestrowanie przepływów oraz Analiza ruchu, format domyślny i bez ustawionych zasad przechowywania.</span><span class="sxs-lookup"><span data-stu-id="7d904-118">The specified NSG has flow logging and Traffic Analytics enabled, default format and no retention policy set.</span></span>

## <span data-ttu-id="7d904-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7d904-119">PARAMETERS</span></span>

### <span data-ttu-id="7d904-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7d904-120">-AsJob</span></span>
<span data-ttu-id="7d904-121">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7d904-121">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d904-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d904-122">-DefaultProfile</span></span>
<span data-ttu-id="7d904-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7d904-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d904-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="7d904-124">-Location</span></span>
<span data-ttu-id="7d904-125">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="7d904-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="7d904-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7d904-126">-NetworkWatcher</span></span>
<span data-ttu-id="7d904-127">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="7d904-127">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d904-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="7d904-128">-NetworkWatcherName</span></span>
<span data-ttu-id="7d904-129">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="7d904-129">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d904-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d904-130">-ResourceGroupName</span></span>
<span data-ttu-id="7d904-131">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="7d904-131">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d904-132">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="7d904-132">-TargetResourceId</span></span>
<span data-ttu-id="7d904-133">Identyfikator zasobu docelowego.</span><span class="sxs-lookup"><span data-stu-id="7d904-133">The target resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d904-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d904-134">CommonParameters</span></span>
<span data-ttu-id="7d904-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d904-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d904-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7d904-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d904-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7d904-137">INPUTS</span></span>

### <span data-ttu-id="7d904-138">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7d904-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="7d904-139">System. String</span><span class="sxs-lookup"><span data-stu-id="7d904-139">System.String</span></span>

## <span data-ttu-id="7d904-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7d904-140">OUTPUTS</span></span>

### <span data-ttu-id="7d904-141">Microsoft. Azure. Commands. Network. models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="7d904-141">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="7d904-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7d904-142">NOTES</span></span>
<span data-ttu-id="7d904-143">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, monitor, przepływ, dzienniki, flowlog, rejestrowanie</span><span class="sxs-lookup"><span data-stu-id="7d904-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="7d904-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7d904-144">RELATED LINKS</span></span>

[<span data-ttu-id="7d904-145">Nowe — AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7d904-145">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="7d904-146">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7d904-146">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="7d904-147">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7d904-147">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="7d904-148">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="7d904-148">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="7d904-149">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="7d904-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="7d904-150">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="7d904-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="7d904-151">Start — AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="7d904-151">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="7d904-152">Nowe — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7d904-152">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7d904-153">Nowe — AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="7d904-153">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="7d904-154">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7d904-154">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7d904-155">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7d904-155">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7d904-156">Zatrzymaj — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7d904-156">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7d904-157">Nowe — AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d904-157">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="7d904-158">Test — AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="7d904-158">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="7d904-159">Test — AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="7d904-159">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="7d904-160">Zatrzymaj — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7d904-160">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7d904-161">Start — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7d904-161">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7d904-162">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7d904-162">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7d904-163">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="7d904-163">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="7d904-164">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7d904-164">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7d904-165">Nowe — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7d904-165">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7d904-166">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="7d904-166">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="7d904-167">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="7d904-167">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="7d904-168">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="7d904-168">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="7d904-169">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="7d904-169">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="7d904-170">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="7d904-170">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="7d904-171">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7d904-171">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
