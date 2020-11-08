---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchertroubleshootingresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
ms.openlocfilehash: db3e3e529fd5c056acf793cd14280ef688c58a81
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234174"
---
# <span data-ttu-id="fab43-101">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="fab43-101">Get-AzNetworkWatcherTroubleshootingResult</span></span>

## <span data-ttu-id="fab43-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fab43-102">SYNOPSIS</span></span>
<span data-ttu-id="fab43-103">Pobiera wyniki rozwiązywania problemów z poprzednio uruchomionej lub obecnie uruchomionej operacji rozwiązywania problemów.</span><span class="sxs-lookup"><span data-stu-id="fab43-103">Gets the troubleshooting result from the previously run or currently running troubleshooting operation.</span></span>

## <span data-ttu-id="fab43-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fab43-104">SYNTAX</span></span>

### <span data-ttu-id="fab43-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fab43-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fab43-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="fab43-106">SetByName</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fab43-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="fab43-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -Location <String> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fab43-108">Opis</span><span class="sxs-lookup"><span data-stu-id="fab43-108">DESCRIPTION</span></span>
<span data-ttu-id="fab43-109">Polecenie cmdlet Get-AzNetworkWatcherTroubleshootingResult pobiera wyniki rozwiązywania problemów z poprzednio uruchomionego lub obecnie uruchomionego Start-AzNetworkWatcherResourceTroubleshooting operacji.</span><span class="sxs-lookup"><span data-stu-id="fab43-109">The Get-AzNetworkWatcherTroubleshootingResult cmdlet gets the troubleshooting result from the previously run or currently running Start-AzNetworkWatcherResourceTroubleshooting operation.</span></span> <span data-ttu-id="fab43-110">Jeśli obecnie trwa operacja rozwiązywania problemów, wykonanie tej operacji może potrwać kilka minut.</span><span class="sxs-lookup"><span data-stu-id="fab43-110">If the troubleshooting operation is currently in progress, then this operation may take a few minutes to complete.</span></span> <span data-ttu-id="fab43-111">Obecnie obsługiwane są bramy sieci wirtualnej i połączenia.</span><span class="sxs-lookup"><span data-stu-id="fab43-111">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="fab43-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fab43-112">EXAMPLES</span></span>

### <span data-ttu-id="fab43-113">Przykład 1: Rozpoczynanie rozwiązywania problemów z bramą sieci wirtualnej i uzyskiwanie wyniku</span><span class="sxs-lookup"><span data-stu-id="fab43-113">Example 1: Start Troubleshooting on a Virtual Network Gateway and Retrieve Result</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath

Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher $NW -TargetResourceId $target
```

<span data-ttu-id="fab43-114">Powyższy przykład rozpoczyna Rozwiązywanie problemów z bramą sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fab43-114">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="fab43-115">Ukończenie operacji może potrwać kilka minut.</span><span class="sxs-lookup"><span data-stu-id="fab43-115">The operation may take a few minutes to complete.</span></span>
<span data-ttu-id="fab43-116">Po rozpoczęciu rozwiązywania problemów z zasobem zostanie nawiązane połączenie Get-AzNetworkWatcherTroubleshootingResult, aby pobrać wynik tego połączenia.</span><span class="sxs-lookup"><span data-stu-id="fab43-116">After troubleshooting has started, a Get-AzNetworkWatcherTroubleshootingResult call is made to the resource to retrieve the result of this call.</span></span> 

## <span data-ttu-id="fab43-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fab43-117">PARAMETERS</span></span>

### <span data-ttu-id="fab43-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fab43-118">-DefaultProfile</span></span>
<span data-ttu-id="fab43-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fab43-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fab43-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="fab43-120">-Location</span></span>
<span data-ttu-id="fab43-121">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="fab43-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="fab43-122">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fab43-122">-NetworkWatcher</span></span>
<span data-ttu-id="fab43-123">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="fab43-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="fab43-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="fab43-124">-NetworkWatcherName</span></span>
<span data-ttu-id="fab43-125">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="fab43-125">The name of network watcher.</span></span>

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

### <span data-ttu-id="fab43-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fab43-126">-ResourceGroupName</span></span>
<span data-ttu-id="fab43-127">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="fab43-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="fab43-128">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="fab43-128">-TargetResourceId</span></span>
<span data-ttu-id="fab43-129">Identyfikator zasobu docelowego.</span><span class="sxs-lookup"><span data-stu-id="fab43-129">The target resource ID.</span></span>

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

### <span data-ttu-id="fab43-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fab43-130">CommonParameters</span></span>
<span data-ttu-id="fab43-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fab43-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fab43-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fab43-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fab43-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fab43-133">INPUTS</span></span>

### <span data-ttu-id="fab43-134">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fab43-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="fab43-135">System. String</span><span class="sxs-lookup"><span data-stu-id="fab43-135">System.String</span></span>

## <span data-ttu-id="fab43-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fab43-136">OUTPUTS</span></span>

### <span data-ttu-id="fab43-137">Microsoft. Azure. Commands. Network. models. PSTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="fab43-137">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="fab43-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fab43-138">NOTES</span></span>
<span data-ttu-id="fab43-139">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, Monitor sieci, rozwiązywanie problemów, VPN, połączenie</span><span class="sxs-lookup"><span data-stu-id="fab43-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="fab43-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fab43-140">RELATED LINKS</span></span>

[<span data-ttu-id="fab43-141">Nowe — AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fab43-141">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="fab43-142">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fab43-142">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="fab43-143">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fab43-143">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="fab43-144">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="fab43-144">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="fab43-145">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="fab43-145">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="fab43-146">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="fab43-146">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="fab43-147">Start — AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="fab43-147">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="fab43-148">Nowe — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fab43-148">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fab43-149">Nowe — AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="fab43-149">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="fab43-150">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fab43-150">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fab43-151">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fab43-151">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fab43-152">Zatrzymaj — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fab43-152">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fab43-153">Nowe — AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="fab43-153">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="fab43-154">Test — AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="fab43-154">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="fab43-155">Test — AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="fab43-155">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="fab43-156">Zatrzymaj — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fab43-156">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="fab43-157">Start — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fab43-157">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="fab43-158">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fab43-158">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="fab43-159">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="fab43-159">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="fab43-160">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fab43-160">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="fab43-161">Nowe — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fab43-161">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="fab43-162">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="fab43-162">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="fab43-163">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="fab43-163">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="fab43-164">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="fab43-164">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="fab43-165">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="fab43-165">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="fab43-166">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="fab43-166">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="fab43-167">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fab43-167">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
