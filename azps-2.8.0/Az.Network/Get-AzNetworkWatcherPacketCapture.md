---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: dc8093a9e508084639fe64b68378cf44f41aa67d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870655"
---
# <span data-ttu-id="384a9-101">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="384a9-101">Get-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="384a9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="384a9-102">SYNOPSIS</span></span>
<span data-ttu-id="384a9-103">Pobiera informacje i właściwości oraz stan zasobu przechwytywania pakietu.</span><span class="sxs-lookup"><span data-stu-id="384a9-103">Gets information and properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="384a9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="384a9-104">SYNTAX</span></span>

### <span data-ttu-id="384a9-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="384a9-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="384a9-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="384a9-106">SetByName</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="384a9-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="384a9-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherPacketCapture -Location <String> [-PacketCaptureName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="384a9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="384a9-108">DESCRIPTION</span></span>
<span data-ttu-id="384a9-109">Get-AzNetworkWatcherPacketCapture pobiera właściwości i stan zasobu przechwytywania pakietu.</span><span class="sxs-lookup"><span data-stu-id="384a9-109">The Get-AzNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="384a9-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="384a9-110">EXAMPLES</span></span>

### <span data-ttu-id="384a9-111">Przykład 1. Tworzenie przechwyconych pakietów za pomocą wielu filtrów i pobieranie ich stanu</span><span class="sxs-lookup"><span data-stu-id="384a9-111">Example 1: Create a Packet Capture with multiple filters and retrieve its status</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="384a9-112">W tym przykładzie tworzymy przechwycony pakiet o nazwie "PacketCaptureTest" z wieloma filtrami i limitem czasu.</span><span class="sxs-lookup"><span data-stu-id="384a9-112">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="384a9-113">Po zakończeniu sesji zostanie ona zapisana na określonym koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="384a9-113">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="384a9-114">Następnie dzwonimy Get-AzNetworkWatcherPacketCapture, aby pobrać stan sesji przechwytywania.</span><span class="sxs-lookup"><span data-stu-id="384a9-114">We then call Get-AzNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> <span data-ttu-id="384a9-115">Uwaga: aby można było tworzyć przechwycenia pakietów, rozszerzenie obserwatora sieci Azure musi być zainstalowane na docelowej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="384a9-115">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

>[!NOTE]
><span data-ttu-id="384a9-116">Jeśli utworzysz odwołanie do funkcji przechwytywania pakietu bezpośrednio z polecenia New-AzNetworkWatcherPacketCapture, nie będzie ona zawierać wszystkich właściwości.</span><span class="sxs-lookup"><span data-stu-id="384a9-116">If you create a reference to the packet capture directly from the New-AzNetworkWatcherPacketCapture command, it won't have all the properties.</span></span> <span data-ttu-id="384a9-117">Wszystkie właściwości przechwytywania pakietów można uzyskać, nadając mu połączenie z poleceniem Get-AzNetworkWatcherPacketCapture.</span><span class="sxs-lookup"><span data-stu-id="384a9-117">You can get all of the properties of the packet capture by making a call to the Get-AzNetworkWatcherPacketCapture command.</span></span>

### <span data-ttu-id="384a9-118">Przykład 2: Tworzenie przechwyconych pakietów za pomocą wielu filtrów i pobieranie ich stanu</span><span class="sxs-lookup"><span data-stu-id="384a9-118">Example 2: Create a Packet Capture with multiple filters and retrieve its status</span></span>
```
Get-AzNetworkWatcherPacketCapture -ResourceGroupName rg1 -NetworkWatcherName nw1 -PacketCaptureName PacketCapture*
```

<span data-ttu-id="384a9-119">To polecenie cmdlet zwraca wszystkie PacketCaptures, które zaczynają się od "PacketCapture" w monitorze sieci NW1.</span><span class="sxs-lookup"><span data-stu-id="384a9-119">This cmdlet returns all PacketCaptures that start with "PacketCapture" in the nw1 Network Watcher.</span></span>

## <span data-ttu-id="384a9-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="384a9-120">PARAMETERS</span></span>

### <span data-ttu-id="384a9-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="384a9-121">-AsJob</span></span>
<span data-ttu-id="384a9-122">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="384a9-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="384a9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="384a9-123">-DefaultProfile</span></span>
<span data-ttu-id="384a9-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="384a9-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="384a9-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="384a9-125">-Location</span></span>
<span data-ttu-id="384a9-126">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="384a9-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="384a9-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="384a9-127">-NetworkWatcher</span></span>
<span data-ttu-id="384a9-128">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="384a9-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="384a9-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="384a9-129">-NetworkWatcherName</span></span>
<span data-ttu-id="384a9-130">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="384a9-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="384a9-131">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="384a9-131">-PacketCaptureName</span></span>
<span data-ttu-id="384a9-132">Nazwa przechwytywania pakietu.</span><span class="sxs-lookup"><span data-stu-id="384a9-132">The packet capture name.</span></span>

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

### <span data-ttu-id="384a9-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="384a9-133">-ResourceGroupName</span></span>
<span data-ttu-id="384a9-134">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="384a9-134">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="384a9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="384a9-135">CommonParameters</span></span>
<span data-ttu-id="384a9-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="384a9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="384a9-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="384a9-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="384a9-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="384a9-138">INPUTS</span></span>

### <span data-ttu-id="384a9-139">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="384a9-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="384a9-140">System. String</span><span class="sxs-lookup"><span data-stu-id="384a9-140">System.String</span></span>

## <span data-ttu-id="384a9-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="384a9-141">OUTPUTS</span></span>

### <span data-ttu-id="384a9-142">Microsoft. Azure. Commands. Network. models. PSGetPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="384a9-142">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="384a9-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="384a9-143">NOTES</span></span>
<span data-ttu-id="384a9-144">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, Monitor sieci, pakiet, przechwytywanie, ruch</span><span class="sxs-lookup"><span data-stu-id="384a9-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="384a9-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="384a9-145">RELATED LINKS</span></span>

[<span data-ttu-id="384a9-146">Nowe — AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="384a9-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="384a9-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="384a9-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="384a9-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="384a9-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="384a9-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="384a9-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="384a9-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="384a9-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="384a9-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="384a9-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="384a9-152">Start — AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="384a9-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="384a9-153">Nowe — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="384a9-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="384a9-154">Nowe — AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="384a9-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="384a9-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="384a9-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="384a9-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="384a9-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="384a9-157">Zatrzymaj — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="384a9-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="384a9-158">Nowe — AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="384a9-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="384a9-159">Test — AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="384a9-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="384a9-160">Test — AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="384a9-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="384a9-161">Zatrzymaj — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="384a9-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="384a9-162">Start — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="384a9-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="384a9-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="384a9-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="384a9-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="384a9-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="384a9-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="384a9-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="384a9-166">Nowe — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="384a9-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="384a9-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="384a9-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="384a9-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="384a9-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="384a9-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="384a9-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="384a9-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="384a9-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="384a9-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="384a9-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="384a9-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="384a9-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

