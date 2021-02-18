---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: e836bb8738b594e09c65568cc0f454a476db9d34
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100410433"
---
# <span data-ttu-id="40d4e-101">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="40d4e-101">Get-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="40d4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40d4e-102">SYNOPSIS</span></span>
<span data-ttu-id="40d4e-103">Pobiera informacje, właściwości i stan zasobu przechwytywania pakietów.</span><span class="sxs-lookup"><span data-stu-id="40d4e-103">Gets information and properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="40d4e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="40d4e-104">SYNTAX</span></span>

### <span data-ttu-id="40d4e-105">SetByResource (Default)</span><span class="sxs-lookup"><span data-stu-id="40d4e-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40d4e-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="40d4e-106">SetByName</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40d4e-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="40d4e-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherPacketCapture -Location <String> [-PacketCaptureName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40d4e-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="40d4e-108">DESCRIPTION</span></span>
<span data-ttu-id="40d4e-109">Ta Get-AzNetworkWatcherPacketCapture pobiera właściwości i stan zasobu przechwytywania pakietów.</span><span class="sxs-lookup"><span data-stu-id="40d4e-109">The Get-AzNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="40d4e-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="40d4e-110">EXAMPLES</span></span>

### <span data-ttu-id="40d4e-111">Przykład 1. Tworzenie przechwytywania pakietów za pomocą wielu filtrów i pobieranie jego stanu</span><span class="sxs-lookup"><span data-stu-id="40d4e-111">Example 1: Create a Packet Capture with multiple filters and retrieve its status</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="40d4e-112">W tym przykładzie tworzymy przechwytywanie pakietów o nazwie "PacketCaptureTest" z wieloma filtrami i limitem czasu.</span><span class="sxs-lookup"><span data-stu-id="40d4e-112">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="40d4e-113">Po zakończeniu sesji zostanie ona zapisana na określonym koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="40d4e-113">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="40d4e-114">Następnie dzwonimy Get-AzNetworkWatcherPacketCapture, aby pobrać stan sesji przechwytywania.</span><span class="sxs-lookup"><span data-stu-id="40d4e-114">We then call Get-AzNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> <span data-ttu-id="40d4e-115">Uwaga: Aby można było tworzyć przechwycone pakiety, na docelowej maszynie wirtualnej musi być zainstalowane rozszerzenie Azure Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="40d4e-115">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

>[!NOTE]
><span data-ttu-id="40d4e-116">Jeśli utworzysz odwołanie do przechwytywania pakietu bezpośrednio z New-AzNetworkWatcherPacketCapture, nie będzie on miał wszystkich właściwości.</span><span class="sxs-lookup"><span data-stu-id="40d4e-116">If you create a reference to the packet capture directly from the New-AzNetworkWatcherPacketCapture command, it won't have all the properties.</span></span> <span data-ttu-id="40d4e-117">Wszystkie właściwości przechwytywania pakietów można uzyskać, wywołując polecenie Get-AzNetworkWatcherPacketCapture pakietu.</span><span class="sxs-lookup"><span data-stu-id="40d4e-117">You can get all of the properties of the packet capture by making a call to the Get-AzNetworkWatcherPacketCapture command.</span></span>

### <span data-ttu-id="40d4e-118">Przykład 2. Tworzenie przechwytywania pakietów za pomocą wielu filtrów i pobieranie jego stanu</span><span class="sxs-lookup"><span data-stu-id="40d4e-118">Example 2: Create a Packet Capture with multiple filters and retrieve its status</span></span>
```
Get-AzNetworkWatcherPacketCapture -ResourceGroupName rg1 -NetworkWatcherName nw1 -PacketCaptureName PacketCapture*
```

<span data-ttu-id="40d4e-119">To polecenie cmdlet zwraca wszystkie funkcje PacketCapture, które zaczynają się od "PacketCapture" w nw1 Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="40d4e-119">This cmdlet returns all PacketCaptures that start with "PacketCapture" in the nw1 Network Watcher.</span></span>

## <span data-ttu-id="40d4e-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40d4e-120">PARAMETERS</span></span>

### <span data-ttu-id="40d4e-121">— AsJob</span><span class="sxs-lookup"><span data-stu-id="40d4e-121">-AsJob</span></span>
<span data-ttu-id="40d4e-122">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="40d4e-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="40d4e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40d4e-123">-DefaultProfile</span></span>
<span data-ttu-id="40d4e-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="40d4e-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40d4e-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="40d4e-125">-Location</span></span>
<span data-ttu-id="40d4e-126">Lokalizacja czujki sieci.</span><span class="sxs-lookup"><span data-stu-id="40d4e-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="40d4e-127">— NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="40d4e-127">-NetworkWatcher</span></span>
<span data-ttu-id="40d4e-128">Zasób obserwowania sieci.</span><span class="sxs-lookup"><span data-stu-id="40d4e-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="40d4e-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="40d4e-129">-NetworkWatcherName</span></span>
<span data-ttu-id="40d4e-130">Nazwa osoby oglądacej sieć.</span><span class="sxs-lookup"><span data-stu-id="40d4e-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="40d4e-131">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="40d4e-131">-PacketCaptureName</span></span>
<span data-ttu-id="40d4e-132">Nazwa przechwytywania pakietów.</span><span class="sxs-lookup"><span data-stu-id="40d4e-132">The packet capture name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="40d4e-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40d4e-133">-ResourceGroupName</span></span>
<span data-ttu-id="40d4e-134">Nazwa grupy zasobów obserwowanych sieci.</span><span class="sxs-lookup"><span data-stu-id="40d4e-134">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="40d4e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40d4e-135">CommonParameters</span></span>
<span data-ttu-id="40d4e-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40d4e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40d4e-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="40d4e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40d4e-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="40d4e-138">INPUTS</span></span>

### <span data-ttu-id="40d4e-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="40d4e-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="40d4e-140">System.String</span><span class="sxs-lookup"><span data-stu-id="40d4e-140">System.String</span></span>

## <span data-ttu-id="40d4e-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="40d4e-141">OUTPUTS</span></span>

### <span data-ttu-id="40d4e-142">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="40d4e-142">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="40d4e-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="40d4e-143">NOTES</span></span>
<span data-ttu-id="40d4e-144">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span><span class="sxs-lookup"><span data-stu-id="40d4e-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="40d4e-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="40d4e-145">RELATED LINKS</span></span>

[<span data-ttu-id="40d4e-146">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="40d4e-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="40d4e-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="40d4e-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="40d4e-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="40d4e-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="40d4e-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="40d4e-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="40d4e-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="40d4e-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="40d4e-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="40d4e-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="40d4e-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="40d4e-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="40d4e-153">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="40d4e-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="40d4e-154">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="40d4e-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="40d4e-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="40d4e-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="40d4e-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="40d4e-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="40d4e-157">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="40d4e-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="40d4e-158">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="40d4e-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="40d4e-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="40d4e-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="40d4e-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="40d4e-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="40d4e-161">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="40d4e-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="40d4e-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="40d4e-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="40d4e-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="40d4e-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="40d4e-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="40d4e-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="40d4e-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="40d4e-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="40d4e-166">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="40d4e-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="40d4e-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="40d4e-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="40d4e-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="40d4e-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="40d4e-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="40d4e-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="40d4e-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="40d4e-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="40d4e-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="40d4e-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="40d4e-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="40d4e-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

