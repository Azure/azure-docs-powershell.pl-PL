---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azpacketcapturefilterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
ms.openlocfilehash: b3732167d26f35b0e3e8ac6c29f187138cde0b18
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953914"
---
# <span data-ttu-id="7420c-101">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="7420c-101">New-AzPacketCaptureFilterConfig</span></span>

## <span data-ttu-id="7420c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7420c-102">SYNOPSIS</span></span>
<span data-ttu-id="7420c-103">Tworzy nowy obiekt filtru przechwytywania pakietów.</span><span class="sxs-lookup"><span data-stu-id="7420c-103">Creates a new packet capture filter object.</span></span>

## <span data-ttu-id="7420c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7420c-104">SYNTAX</span></span>

```
New-AzPacketCaptureFilterConfig [-Protocol <String>] [-RemoteIPAddress <String>] [-LocalIPAddress <String>]
 [-LocalPort <String>] [-RemotePort <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7420c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="7420c-105">DESCRIPTION</span></span>
<span data-ttu-id="7420c-106">Polecenie New-AzPacketCaptureFilterConfig cmdlet tworzy nowy obiekt filtru przechwytywania pakietów.</span><span class="sxs-lookup"><span data-stu-id="7420c-106">The New-AzPacketCaptureFilterConfig cmdlet creates a new packet capture filter object.</span></span> <span data-ttu-id="7420c-107">Ten obiekt służy do ograniczania typu pakietów przechwytywanych podczas sesji przechwytywania pakietów przy użyciu określonych kryteriów.</span><span class="sxs-lookup"><span data-stu-id="7420c-107">This object is used to restrict the type of packets that are captured during a packet capture session using the specified criteria.</span></span> <span data-ttu-id="7420c-108">Polecenie New-AzNetworkWatcherPacketCapture cmdlet może akceptować wiele obiektów filtru w celu włączenia sesji przechwytywania, które można ująć.</span><span class="sxs-lookup"><span data-stu-id="7420c-108">The New-AzNetworkWatcherPacketCapture cmdlet can accept multiple filter objects to enable composable capture sessions.</span></span>

## <span data-ttu-id="7420c-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7420c-109">EXAMPLES</span></span>

### <span data-ttu-id="7420c-110">Przykład 1. Tworzenie przechwytywania pakietów za pomocą wielu filtrów</span><span class="sxs-lookup"><span data-stu-id="7420c-110">Example 1: Create a Packet Capture with multiple filters</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2
```

<span data-ttu-id="7420c-111">W tym przykładzie tworzymy przechwytywanie pakietów o nazwie "PacketCaptureTest" z wieloma filtrami i limitem czasu.</span><span class="sxs-lookup"><span data-stu-id="7420c-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="7420c-112">Po zakończeniu sesji zostanie ona zapisana na określonym koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="7420c-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="7420c-113">Uwaga: Aby tworzyć przechwycone pakiety, na docelowej maszynie wirtualnej musi być zainstalowane rozszerzenie Azure Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="7420c-113">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="7420c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7420c-114">PARAMETERS</span></span>

### <span data-ttu-id="7420c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7420c-115">-DefaultProfile</span></span>
<span data-ttu-id="7420c-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7420c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7420c-117">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="7420c-117">-LocalIPAddress</span></span>
<span data-ttu-id="7420c-118">Określa lokalny adres IP, według których ma być filtrowany.</span><span class="sxs-lookup"><span data-stu-id="7420c-118">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="7420c-119">Przykładowe dane wejściowe: "127.0.0.1" dla wpisu adresu pojedynczego.</span><span class="sxs-lookup"><span data-stu-id="7420c-119">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="7420c-120">"127.0.0.1-127.0.0.255" dla zakresu.</span><span class="sxs-lookup"><span data-stu-id="7420c-120">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="7420c-121">"127.0.0.1;127.0.0.5;" dla wielu wpisów.</span><span class="sxs-lookup"><span data-stu-id="7420c-121">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="7420c-122">- LocalPort</span><span class="sxs-lookup"><span data-stu-id="7420c-122">-LocalPort</span></span>
<span data-ttu-id="7420c-123">Określa lokalny adres IP, według których ma być filtrowany.</span><span class="sxs-lookup"><span data-stu-id="7420c-123">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="7420c-124">Przykładowe dane wejściowe: "127.0.0.1" dla wpisu adresu pojedynczego.</span><span class="sxs-lookup"><span data-stu-id="7420c-124">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="7420c-125">"127.0.0.1-127.0.0.255" dla zakresu.</span><span class="sxs-lookup"><span data-stu-id="7420c-125">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="7420c-126">"127.0.0.1;127.0.0.5;" dla wielu wpisów.</span><span class="sxs-lookup"><span data-stu-id="7420c-126">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="7420c-127">— Protokół</span><span class="sxs-lookup"><span data-stu-id="7420c-127">-Protocol</span></span>
<span data-ttu-id="7420c-128">Określa protokół, według który ma być filtrowany.</span><span class="sxs-lookup"><span data-stu-id="7420c-128">Specifies the Protocol to filter on.</span></span> <span data-ttu-id="7420c-129">Dopuszczalne wartości"TCP", "UDP", "Any"</span><span class="sxs-lookup"><span data-stu-id="7420c-129">Acceptable values "TCP","UDP","Any"</span></span>

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

### <span data-ttu-id="7420c-130">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="7420c-130">-RemoteIPAddress</span></span>
<span data-ttu-id="7420c-131">Określa zdalny adres IP do filtrowania.</span><span class="sxs-lookup"><span data-stu-id="7420c-131">Specifies the remote IP address to filter on.</span></span>
<span data-ttu-id="7420c-132">Przykładowe dane wejściowe: "127.0.0.1" dla wpisu adresu pojedynczego.</span><span class="sxs-lookup"><span data-stu-id="7420c-132">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="7420c-133">"127.0.0.1-127.0.0.255" dla zakresu.</span><span class="sxs-lookup"><span data-stu-id="7420c-133">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="7420c-134">"127.0.0.1;127.0.0.5;" dla wielu wpisów.</span><span class="sxs-lookup"><span data-stu-id="7420c-134">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="7420c-135">— RemotePort</span><span class="sxs-lookup"><span data-stu-id="7420c-135">-RemotePort</span></span>
<span data-ttu-id="7420c-136">Określa port zdalny, według których ma być filtrowany.</span><span class="sxs-lookup"><span data-stu-id="7420c-136">Specifies the Remote Port to filter on.</span></span>
<span data-ttu-id="7420c-137">Przykładowe dane wejściowe portu zdalnego: "80" dla wpisu z jednym portem.</span><span class="sxs-lookup"><span data-stu-id="7420c-137">Remote port Example inputs: "80" for single port entry.</span></span>
<span data-ttu-id="7420c-138">"80-85" dla zakresu.</span><span class="sxs-lookup"><span data-stu-id="7420c-138">"80-85" for range.</span></span>
<span data-ttu-id="7420c-139">"80;443;" dla wielu wpisów.</span><span class="sxs-lookup"><span data-stu-id="7420c-139">"80;443;" for multiple entries.</span></span>

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

### <span data-ttu-id="7420c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7420c-140">CommonParameters</span></span>
<span data-ttu-id="7420c-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7420c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7420c-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7420c-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7420c-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7420c-143">INPUTS</span></span>

### <span data-ttu-id="7420c-144">System.String</span><span class="sxs-lookup"><span data-stu-id="7420c-144">System.String</span></span>

## <span data-ttu-id="7420c-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7420c-145">OUTPUTS</span></span>

### <span data-ttu-id="7420c-146">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span><span class="sxs-lookup"><span data-stu-id="7420c-146">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span></span>

## <span data-ttu-id="7420c-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7420c-147">NOTES</span></span>
<span data-ttu-id="7420c-148">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span><span class="sxs-lookup"><span data-stu-id="7420c-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span> 

## <span data-ttu-id="7420c-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7420c-149">RELATED LINKS</span></span>

[<span data-ttu-id="7420c-150">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7420c-150">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="7420c-151">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7420c-151">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="7420c-152">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7420c-152">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="7420c-153">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="7420c-153">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="7420c-154">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="7420c-154">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="7420c-155">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="7420c-155">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="7420c-156">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="7420c-156">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="7420c-157">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7420c-157">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7420c-158">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="7420c-158">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="7420c-159">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7420c-159">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7420c-160">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7420c-160">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7420c-161">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7420c-161">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7420c-162">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="7420c-162">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="7420c-163">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="7420c-163">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="7420c-164">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="7420c-164">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="7420c-165">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7420c-165">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7420c-166">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7420c-166">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7420c-167">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7420c-167">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7420c-168">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="7420c-168">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="7420c-169">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7420c-169">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7420c-170">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7420c-170">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7420c-171">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="7420c-171">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="7420c-172">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="7420c-172">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="7420c-173">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="7420c-173">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="7420c-174">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="7420c-174">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="7420c-175">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="7420c-175">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="7420c-176">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7420c-176">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
