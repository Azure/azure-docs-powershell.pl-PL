---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpacketcapturefilterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
ms.openlocfilehash: d7dac006abf09ec7c80d4a7e7659405936a8d20e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100409651"
---
# <span data-ttu-id="71442-101">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="71442-101">New-AzPacketCaptureFilterConfig</span></span>

## <span data-ttu-id="71442-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71442-102">SYNOPSIS</span></span>
<span data-ttu-id="71442-103">Tworzy nowy obiekt filtru przechwytywania pakietów.</span><span class="sxs-lookup"><span data-stu-id="71442-103">Creates a new packet capture filter object.</span></span>

## <span data-ttu-id="71442-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="71442-104">SYNTAX</span></span>

```
New-AzPacketCaptureFilterConfig [-Protocol <String>] [-RemoteIPAddress <String>] [-LocalIPAddress <String>]
 [-LocalPort <String>] [-RemotePort <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71442-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="71442-105">DESCRIPTION</span></span>
<span data-ttu-id="71442-106">Polecenie New-AzPacketCaptureFilterConfig cmdlet tworzy nowy obiekt filtru przechwytywania pakietów.</span><span class="sxs-lookup"><span data-stu-id="71442-106">The New-AzPacketCaptureFilterConfig cmdlet creates a new packet capture filter object.</span></span> <span data-ttu-id="71442-107">Ten obiekt służy do ograniczania typu pakietów przechwytywanych podczas sesji przechwytywania pakietów przy użyciu określonych kryteriów.</span><span class="sxs-lookup"><span data-stu-id="71442-107">This object is used to restrict the type of packets that are captured during a packet capture session using the specified criteria.</span></span> <span data-ttu-id="71442-108">Polecenie New-AzNetworkWatcherPacketCapture cmdlet może akceptować wiele obiektów filtru w celu włączenia sesji przechwytywania, które można composować.</span><span class="sxs-lookup"><span data-stu-id="71442-108">The New-AzNetworkWatcherPacketCapture cmdlet can accept multiple filter objects to enable composable capture sessions.</span></span>

## <span data-ttu-id="71442-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="71442-109">EXAMPLES</span></span>

### <span data-ttu-id="71442-110">Przykład 1. Tworzenie przechwytywania pakietów za pomocą wielu filtrów</span><span class="sxs-lookup"><span data-stu-id="71442-110">Example 1: Create a Packet Capture with multiple filters</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2
```

<span data-ttu-id="71442-111">W tym przykładzie tworzymy przechwytywanie pakietów o nazwie "PacketCaptureTest" z wieloma filtrami i limitem czasu.</span><span class="sxs-lookup"><span data-stu-id="71442-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="71442-112">Po zakończeniu sesji zostanie ona zapisana na określonym koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="71442-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="71442-113">Uwaga: Aby można było tworzyć przechwycone pakiety, na docelowej maszynie wirtualnej musi być zainstalowane rozszerzenie Azure Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="71442-113">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="71442-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71442-114">PARAMETERS</span></span>

### <span data-ttu-id="71442-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71442-115">-DefaultProfile</span></span>
<span data-ttu-id="71442-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="71442-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71442-117">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="71442-117">-LocalIPAddress</span></span>
<span data-ttu-id="71442-118">Określa lokalny adres IP, według których ma być filtrowany.</span><span class="sxs-lookup"><span data-stu-id="71442-118">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="71442-119">Przykładowe dane wejściowe: "127.0.0.1" dla wpisu adresu pojedynczego.</span><span class="sxs-lookup"><span data-stu-id="71442-119">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="71442-120">"127.0.0.1-127.0.0.255" dla zakresu.</span><span class="sxs-lookup"><span data-stu-id="71442-120">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="71442-121">"127.0.0.1;127.0.0.5;" dla wielu wpisów.</span><span class="sxs-lookup"><span data-stu-id="71442-121">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71442-122">- LocalPort</span><span class="sxs-lookup"><span data-stu-id="71442-122">-LocalPort</span></span>
<span data-ttu-id="71442-123">Określa lokalny adres IP, według których ma być filtrowany.</span><span class="sxs-lookup"><span data-stu-id="71442-123">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="71442-124">Przykładowe dane wejściowe: "127.0.0.1" dla wpisu adresu pojedynczego.</span><span class="sxs-lookup"><span data-stu-id="71442-124">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="71442-125">"127.0.0.1-127.0.0.255" dla zakresu.</span><span class="sxs-lookup"><span data-stu-id="71442-125">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="71442-126">"127.0.0.1;127.0.0.5;" dla wielu wpisów.</span><span class="sxs-lookup"><span data-stu-id="71442-126">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71442-127">— Protokół</span><span class="sxs-lookup"><span data-stu-id="71442-127">-Protocol</span></span>
<span data-ttu-id="71442-128">Określa protokół, według który ma być filtrowany.</span><span class="sxs-lookup"><span data-stu-id="71442-128">Specifies the Protocol to filter on.</span></span> <span data-ttu-id="71442-129">Dopuszczalne wartości"TCP", "UDP", "Any"</span><span class="sxs-lookup"><span data-stu-id="71442-129">Acceptable values "TCP","UDP","Any"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71442-130">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="71442-130">-RemoteIPAddress</span></span>
<span data-ttu-id="71442-131">Określa zdalny adres IP do filtrowania.</span><span class="sxs-lookup"><span data-stu-id="71442-131">Specifies the remote IP address to filter on.</span></span>
<span data-ttu-id="71442-132">Przykładowe dane wejściowe: "127.0.0.1" dla wpisu adresu pojedynczego.</span><span class="sxs-lookup"><span data-stu-id="71442-132">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="71442-133">"127.0.0.1-127.0.0.255" dla zakresu.</span><span class="sxs-lookup"><span data-stu-id="71442-133">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="71442-134">"127.0.0.1;127.0.0.5;" dla wielu wpisów.</span><span class="sxs-lookup"><span data-stu-id="71442-134">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71442-135">— RemotePort</span><span class="sxs-lookup"><span data-stu-id="71442-135">-RemotePort</span></span>
<span data-ttu-id="71442-136">Określa port zdalny, według których ma być filtrowany.</span><span class="sxs-lookup"><span data-stu-id="71442-136">Specifies the Remote Port to filter on.</span></span>
<span data-ttu-id="71442-137">Przykładowe dane wejściowe portu zdalnego: "80" dla wpisu z jednym portem.</span><span class="sxs-lookup"><span data-stu-id="71442-137">Remote port Example inputs: "80" for single port entry.</span></span>
<span data-ttu-id="71442-138">"80-85" dla zakresu.</span><span class="sxs-lookup"><span data-stu-id="71442-138">"80-85" for range.</span></span>
<span data-ttu-id="71442-139">"80;443;" dla wielu wpisów.</span><span class="sxs-lookup"><span data-stu-id="71442-139">"80;443;" for multiple entries.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71442-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71442-140">CommonParameters</span></span>
<span data-ttu-id="71442-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71442-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71442-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71442-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71442-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="71442-143">INPUTS</span></span>

### <span data-ttu-id="71442-144">System.String</span><span class="sxs-lookup"><span data-stu-id="71442-144">System.String</span></span>

## <span data-ttu-id="71442-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="71442-145">OUTPUTS</span></span>

### <span data-ttu-id="71442-146">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span><span class="sxs-lookup"><span data-stu-id="71442-146">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span></span>

## <span data-ttu-id="71442-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="71442-147">NOTES</span></span>
<span data-ttu-id="71442-148">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span><span class="sxs-lookup"><span data-stu-id="71442-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span> 

## <span data-ttu-id="71442-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="71442-149">RELATED LINKS</span></span>

[<span data-ttu-id="71442-150">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="71442-150">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="71442-151">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="71442-151">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="71442-152">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="71442-152">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="71442-153">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="71442-153">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="71442-154">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="71442-154">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="71442-155">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="71442-155">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="71442-156">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="71442-156">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="71442-157">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="71442-157">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="71442-158">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="71442-158">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="71442-159">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="71442-159">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="71442-160">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="71442-160">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="71442-161">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="71442-161">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="71442-162">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="71442-162">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="71442-163">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="71442-163">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="71442-164">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="71442-164">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="71442-165">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="71442-165">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="71442-166">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="71442-166">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="71442-167">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="71442-167">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="71442-168">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="71442-168">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="71442-169">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="71442-169">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="71442-170">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="71442-170">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="71442-171">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="71442-171">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="71442-172">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="71442-172">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="71442-173">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="71442-173">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="71442-174">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="71442-174">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="71442-175">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="71442-175">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="71442-176">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="71442-176">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
