---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherflowlogstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherFlowLogStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherFlowLogStatus.md
ms.openlocfilehash: a045acd86141b57d02fef9931cfb01ff8b783e8a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716943"
---
# <span data-ttu-id="b2de6-101">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="b2de6-101">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>

## <span data-ttu-id="b2de6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b2de6-102">SYNOPSIS</span></span>
<span data-ttu-id="b2de6-103">Pobiera stan rejestrowania przepływu dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="b2de6-103">Gets the status of flow logging on a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2de6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b2de6-104">SYNTAX</span></span>

### <span data-ttu-id="b2de6-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b2de6-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2de6-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="b2de6-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2de6-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="b2de6-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherFlowLogStatus -Location <String> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2de6-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b2de6-108">DESCRIPTION</span></span>
<span data-ttu-id="b2de6-109">Polecenie cmdlet Get-AzureRmNetworkWatcherFlowLogStatus Pobiera stan rejestrowania przepływu dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="b2de6-109">The Get-AzureRmNetworkWatcherFlowLogStatus cmdlet Gets the status of flow logging on a resource.</span></span> <span data-ttu-id="b2de6-110">Stan uwzględnia, czy w przypadku danego zasobu jest włączone rejestrowanie przepływu, skonfigurowane konto magazynu do wysyłania dzienników oraz zasady przechowywania dzienników.</span><span class="sxs-lookup"><span data-stu-id="b2de6-110">The status includes whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="b2de6-111">W przypadku rejestrowania przepływów są obsługiwane obecnie grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="b2de6-111">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="b2de6-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b2de6-112">EXAMPLES</span></span>

### <span data-ttu-id="b2de6-113">Przykład 1: uzyskiwanie stanu rejestrowania przepływu dla określonego NSG</span><span class="sxs-lookup"><span data-stu-id="b2de6-113">Example 1: Get the Flow Logging Status for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzurermNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzureRmNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG

PS C:\> Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcher $NW -TargetResourceId $nsg.Id

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
Properties       : {
                     "Enabled": true,
                     "RetentionPolicy": {
                       "Days": 0,
                       "Enabled": false
                     },
                     "StorageId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"
                   }
```

<span data-ttu-id="b2de6-114">W tym przykładzie jest wyświetlany stan rejestrowania przepływu dla grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="b2de6-114">In this example we get the flow logging status for a Network Security Group.</span></span> <span data-ttu-id="b2de6-115">Określony NSG ma włączone rejestrowanie przepływów i nie ustawiono zasad przechowywania.</span><span class="sxs-lookup"><span data-stu-id="b2de6-115">The specified NSG has flow logging enabled, and no retention policy set.</span></span>

### <span data-ttu-id="b2de6-116">Przykład 2: uzyskiwanie rejestrowania przepływu i stanu analizy ruchu dla określonego NSG</span><span class="sxs-lookup"><span data-stu-id="b2de6-116">Example 2: Get the Flow Logging and Traffic Analytics Status for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzurermNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzureRmNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG

PS C:\> Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcher $NW -TargetResourceId $nsg.Id

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
FlowAnalyticsConfiguration : {
            "networkWatcherFlowAnalyticsConfiguration": {
              "enabled": true,
              "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb",
              "workspaceRegion": "WorkspaceLocation",
              "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/WorkspaceRg/providers/microsoft.operationalinsights/workspaces/WorkspaceName"
            }
          }
```

<span data-ttu-id="b2de6-117">W tym przykładzie jest wyświetlany stan rejestrowania przepływu i analizy ruchu dla grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="b2de6-117">In this example we get the flow logging and Traffic Analytics status for a Network Security Group.</span></span> <span data-ttu-id="b2de6-118">Określony NSG ma włączone rejestrowanie przepływów oraz Analiza ruchu i nie ustawiono zasad przechowywania.</span><span class="sxs-lookup"><span data-stu-id="b2de6-118">The specified NSG has flow logging and Traffic Analytics enabled, and no retention policy set.</span></span>

## <span data-ttu-id="b2de6-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b2de6-119">PARAMETERS</span></span>

### <span data-ttu-id="b2de6-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b2de6-120">-AsJob</span></span>
<span data-ttu-id="b2de6-121">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b2de6-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b2de6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2de6-122">-DefaultProfile</span></span>
<span data-ttu-id="b2de6-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b2de6-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2de6-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b2de6-124">-Location</span></span>
<span data-ttu-id="b2de6-125">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="b2de6-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="b2de6-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b2de6-126">-NetworkWatcher</span></span>
<span data-ttu-id="b2de6-127">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="b2de6-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="b2de6-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="b2de6-128">-NetworkWatcherName</span></span>
<span data-ttu-id="b2de6-129">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="b2de6-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="b2de6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2de6-130">-ResourceGroupName</span></span>
<span data-ttu-id="b2de6-131">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="b2de6-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="b2de6-132">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="b2de6-132">-TargetResourceId</span></span>
<span data-ttu-id="b2de6-133">Identyfikator zasobu docelowego.</span><span class="sxs-lookup"><span data-stu-id="b2de6-133">The target resource ID.</span></span>

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

### <span data-ttu-id="b2de6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2de6-134">CommonParameters</span></span>
<span data-ttu-id="b2de6-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2de6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2de6-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2de6-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2de6-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b2de6-137">INPUTS</span></span>

### <span data-ttu-id="b2de6-138">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b2de6-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="b2de6-139">Parametry: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b2de6-139">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="b2de6-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b2de6-140">System.String</span></span>
<span data-ttu-id="b2de6-141">Parametry: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b2de6-141">Parameters: NetworkWatcherName (ByValue)</span></span>

## <span data-ttu-id="b2de6-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b2de6-142">OUTPUTS</span></span>

### <span data-ttu-id="b2de6-143">Microsoft. Azure. Commands. Network. models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="b2de6-143">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="b2de6-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b2de6-144">NOTES</span></span>
<span data-ttu-id="b2de6-145">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, monitor, przepływ, dzienniki, flowlog, rejestrowanie</span><span class="sxs-lookup"><span data-stu-id="b2de6-145">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="b2de6-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b2de6-146">RELATED LINKS</span></span>

[<span data-ttu-id="b2de6-147">Nowe — AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b2de6-147">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="b2de6-148">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b2de6-148">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="b2de6-149">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b2de6-149">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="b2de6-150">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="b2de6-150">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="b2de6-151">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="b2de6-151">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="b2de6-152">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="b2de6-152">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="b2de6-153">Start — AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="b2de6-153">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="b2de6-154">Nowe — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b2de6-154">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b2de6-155">Nowe — AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="b2de6-155">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="b2de6-156">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b2de6-156">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b2de6-157">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b2de6-157">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b2de6-158">Zatrzymaj — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b2de6-158">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b2de6-159">Nowe — AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2de6-159">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="b2de6-160">Test — AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="b2de6-160">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="b2de6-161">Test — AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="b2de6-161">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="b2de6-162">Zatrzymaj — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b2de6-162">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b2de6-163">Start — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b2de6-163">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b2de6-164">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b2de6-164">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b2de6-165">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="b2de6-165">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="b2de6-166">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b2de6-166">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b2de6-167">Nowe — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b2de6-167">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b2de6-168">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="b2de6-168">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="b2de6-169">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="b2de6-169">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="b2de6-170">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="b2de6-170">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="b2de6-171">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="b2de6-171">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="b2de6-172">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="b2de6-172">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="b2de6-173">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b2de6-173">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
