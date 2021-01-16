---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchertroubleshootingresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
ms.openlocfilehash: db3e3e529fd5c056acf793cd14280ef688c58a81
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379827"
---
# <span data-ttu-id="454b7-101">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="454b7-101">Get-AzNetworkWatcherTroubleshootingResult</span></span>

## <span data-ttu-id="454b7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="454b7-102">SYNOPSIS</span></span>
<span data-ttu-id="454b7-103">Pobiera wyniki rozwiązywania problemów z poprzednio uruchomionej lub obecnie uruchomionej operacji rozwiązywania problemów.</span><span class="sxs-lookup"><span data-stu-id="454b7-103">Gets the troubleshooting result from the previously run or currently running troubleshooting operation.</span></span>

## <span data-ttu-id="454b7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="454b7-104">SYNTAX</span></span>

### <span data-ttu-id="454b7-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="454b7-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="454b7-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="454b7-106">SetByName</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="454b7-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="454b7-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -Location <String> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="454b7-108">Opis</span><span class="sxs-lookup"><span data-stu-id="454b7-108">DESCRIPTION</span></span>
<span data-ttu-id="454b7-109">Polecenie cmdlet Get-AzNetworkWatcherTroubleshootingResult pobiera wyniki rozwiązywania problemów z poprzednio uruchomionego lub obecnie uruchomionego Start-AzNetworkWatcherResourceTroubleshooting operacji.</span><span class="sxs-lookup"><span data-stu-id="454b7-109">The Get-AzNetworkWatcherTroubleshootingResult cmdlet gets the troubleshooting result from the previously run or currently running Start-AzNetworkWatcherResourceTroubleshooting operation.</span></span> <span data-ttu-id="454b7-110">Jeśli obecnie trwa operacja rozwiązywania problemów, wykonanie tej operacji może potrwać kilka minut.</span><span class="sxs-lookup"><span data-stu-id="454b7-110">If the troubleshooting operation is currently in progress, then this operation may take a few minutes to complete.</span></span> <span data-ttu-id="454b7-111">Obecnie obsługiwane są bramy sieci wirtualnej i połączenia.</span><span class="sxs-lookup"><span data-stu-id="454b7-111">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="454b7-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="454b7-112">EXAMPLES</span></span>

### <span data-ttu-id="454b7-113">Przykład 1: Rozpoczynanie rozwiązywania problemów z bramą sieci wirtualnej i uzyskiwanie wyniku</span><span class="sxs-lookup"><span data-stu-id="454b7-113">Example 1: Start Troubleshooting on a Virtual Network Gateway and Retrieve Result</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath

Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher $NW -TargetResourceId $target
```

<span data-ttu-id="454b7-114">Powyższy przykład rozpoczyna Rozwiązywanie problemów z bramą sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="454b7-114">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="454b7-115">Ukończenie operacji może potrwać kilka minut.</span><span class="sxs-lookup"><span data-stu-id="454b7-115">The operation may take a few minutes to complete.</span></span>
<span data-ttu-id="454b7-116">Po rozpoczęciu rozwiązywania problemów z zasobem zostanie nawiązane połączenie Get-AzNetworkWatcherTroubleshootingResult, aby pobrać wynik tego połączenia.</span><span class="sxs-lookup"><span data-stu-id="454b7-116">After troubleshooting has started, a Get-AzNetworkWatcherTroubleshootingResult call is made to the resource to retrieve the result of this call.</span></span> 

## <span data-ttu-id="454b7-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="454b7-117">PARAMETERS</span></span>

### <span data-ttu-id="454b7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="454b7-118">-DefaultProfile</span></span>
<span data-ttu-id="454b7-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="454b7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="454b7-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="454b7-120">-Location</span></span>
<span data-ttu-id="454b7-121">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="454b7-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="454b7-122">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="454b7-122">-NetworkWatcher</span></span>
<span data-ttu-id="454b7-123">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="454b7-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="454b7-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="454b7-124">-NetworkWatcherName</span></span>
<span data-ttu-id="454b7-125">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="454b7-125">The name of network watcher.</span></span>

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

### <span data-ttu-id="454b7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="454b7-126">-ResourceGroupName</span></span>
<span data-ttu-id="454b7-127">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="454b7-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="454b7-128">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="454b7-128">-TargetResourceId</span></span>
<span data-ttu-id="454b7-129">Identyfikator zasobu docelowego.</span><span class="sxs-lookup"><span data-stu-id="454b7-129">The target resource ID.</span></span>

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

### <span data-ttu-id="454b7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="454b7-130">CommonParameters</span></span>
<span data-ttu-id="454b7-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="454b7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="454b7-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="454b7-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="454b7-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="454b7-133">INPUTS</span></span>

### <span data-ttu-id="454b7-134">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="454b7-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="454b7-135">System. String</span><span class="sxs-lookup"><span data-stu-id="454b7-135">System.String</span></span>

## <span data-ttu-id="454b7-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="454b7-136">OUTPUTS</span></span>

### <span data-ttu-id="454b7-137">Microsoft. Azure. Commands. Network. models. PSTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="454b7-137">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="454b7-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="454b7-138">NOTES</span></span>
<span data-ttu-id="454b7-139">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, Monitor sieci, rozwiązywanie problemów, VPN, połączenie</span><span class="sxs-lookup"><span data-stu-id="454b7-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="454b7-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="454b7-140">RELATED LINKS</span></span>

[<span data-ttu-id="454b7-141">Nowe — AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="454b7-141">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="454b7-142">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="454b7-142">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="454b7-143">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="454b7-143">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="454b7-144">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="454b7-144">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="454b7-145">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="454b7-145">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="454b7-146">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="454b7-146">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="454b7-147">Start — AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="454b7-147">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="454b7-148">Nowe — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="454b7-148">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="454b7-149">Nowe — AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="454b7-149">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="454b7-150">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="454b7-150">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="454b7-151">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="454b7-151">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="454b7-152">Zatrzymaj — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="454b7-152">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="454b7-153">Nowe — AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="454b7-153">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="454b7-154">Test — AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="454b7-154">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="454b7-155">Test — AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="454b7-155">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="454b7-156">Zatrzymaj — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="454b7-156">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="454b7-157">Start — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="454b7-157">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="454b7-158">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="454b7-158">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="454b7-159">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="454b7-159">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="454b7-160">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="454b7-160">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="454b7-161">Nowe — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="454b7-161">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="454b7-162">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="454b7-162">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="454b7-163">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="454b7-163">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="454b7-164">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="454b7-164">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="454b7-165">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="454b7-165">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="454b7-166">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="454b7-166">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="454b7-167">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="454b7-167">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
