---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpacketcapturefilterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
ms.openlocfilehash: f8e51258a56051edf99aa1ec0cfa5e252e0ac0d6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869872"
---
# <span data-ttu-id="02d77-101">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="02d77-101">New-AzPacketCaptureFilterConfig</span></span>

## <span data-ttu-id="02d77-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="02d77-102">SYNOPSIS</span></span>
<span data-ttu-id="02d77-103">Tworzy nowy obiekt filtru przechwytywania pakietów.</span><span class="sxs-lookup"><span data-stu-id="02d77-103">Creates a new packet capture filter object.</span></span>

## <span data-ttu-id="02d77-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="02d77-104">SYNTAX</span></span>

```
New-AzPacketCaptureFilterConfig [-Protocol <String>] [-RemoteIPAddress <String>] [-LocalIPAddress <String>]
 [-LocalPort <String>] [-RemotePort <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02d77-105">Opis</span><span class="sxs-lookup"><span data-stu-id="02d77-105">DESCRIPTION</span></span>
<span data-ttu-id="02d77-106">Polecenie cmdlet New-AzPacketCaptureFilterConfig tworzy nowy obiekt filtru przechwytywania pakietów.</span><span class="sxs-lookup"><span data-stu-id="02d77-106">The New-AzPacketCaptureFilterConfig cmdlet creates a new packet capture filter object.</span></span> <span data-ttu-id="02d77-107">Ten obiekt służy do ograniczania typu pakietów, które są przechwytywane podczas sesji przechwytywania pakietów przy użyciu określonych kryteriów.</span><span class="sxs-lookup"><span data-stu-id="02d77-107">This object is used to restrict the type of packets that are captured during a packet capture session using the specified criteria.</span></span> <span data-ttu-id="02d77-108">Polecenie cmdlet New-AzNetworkWatcherPacketCapture może akceptować wiele obiektów filtrowania, aby umożliwić tworzenie sesji przechwytywania.</span><span class="sxs-lookup"><span data-stu-id="02d77-108">The New-AzNetworkWatcherPacketCapture cmdlet can accept multiple filter objects to enable composable capture sessions.</span></span>

## <span data-ttu-id="02d77-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="02d77-109">EXAMPLES</span></span>

### <span data-ttu-id="02d77-110">Przykład 1. Tworzenie przechwyconych pakietów za pomocą wielu filtrów</span><span class="sxs-lookup"><span data-stu-id="02d77-110">Example 1: Create a Packet Capture with multiple filters</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2
```

<span data-ttu-id="02d77-111">W tym przykładzie tworzymy przechwycony pakiet o nazwie "PacketCaptureTest" z wieloma filtrami i limitem czasu.</span><span class="sxs-lookup"><span data-stu-id="02d77-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="02d77-112">Po zakończeniu sesji zostanie ona zapisana na określonym koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="02d77-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="02d77-113">Uwaga: aby można było tworzyć przechwycenia pakietów, rozszerzenie obserwatora sieci Azure musi być zainstalowane na docelowej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="02d77-113">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="02d77-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="02d77-114">PARAMETERS</span></span>

### <span data-ttu-id="02d77-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02d77-115">-DefaultProfile</span></span>
<span data-ttu-id="02d77-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="02d77-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02d77-117">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="02d77-117">-LocalIPAddress</span></span>
<span data-ttu-id="02d77-118">Określa lokalny adres IP, według którego ma zostać wykonane filtrowanie.</span><span class="sxs-lookup"><span data-stu-id="02d77-118">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="02d77-119">Przykładowe dane wejściowe: "127.0.0.1" dla pojedynczego wpisu adresu.</span><span class="sxs-lookup"><span data-stu-id="02d77-119">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="02d77-120">"127.0.0.1-127.0.0.255" dla zakresu.</span><span class="sxs-lookup"><span data-stu-id="02d77-120">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="02d77-121">"127.0.0.1; 127.0.0.5;" dla wielu wpisów.</span><span class="sxs-lookup"><span data-stu-id="02d77-121">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="02d77-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="02d77-122">-LocalPort</span></span>
<span data-ttu-id="02d77-123">Określa lokalny adres IP, według którego ma zostać wykonane filtrowanie.</span><span class="sxs-lookup"><span data-stu-id="02d77-123">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="02d77-124">Przykładowe dane wejściowe: "127.0.0.1" dla pojedynczego wpisu adresu.</span><span class="sxs-lookup"><span data-stu-id="02d77-124">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="02d77-125">"127.0.0.1-127.0.0.255" dla zakresu.</span><span class="sxs-lookup"><span data-stu-id="02d77-125">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="02d77-126">"127.0.0.1; 127.0.0.5;" dla wielu wpisów.</span><span class="sxs-lookup"><span data-stu-id="02d77-126">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="02d77-127">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="02d77-127">-Protocol</span></span>
<span data-ttu-id="02d77-128">Określa protokół, według którego ma zostać wykonane filtrowanie.</span><span class="sxs-lookup"><span data-stu-id="02d77-128">Specifies the Protocol to filter on.</span></span> <span data-ttu-id="02d77-129">Dopuszczalne wartości "TCP", "UDP", "any"</span><span class="sxs-lookup"><span data-stu-id="02d77-129">Acceptable values "TCP","UDP","Any"</span></span>

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

### <span data-ttu-id="02d77-130">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="02d77-130">-RemoteIPAddress</span></span>
<span data-ttu-id="02d77-131">Określa zdalny adres IP, według którego ma zostać wykonane filtrowanie.</span><span class="sxs-lookup"><span data-stu-id="02d77-131">Specifies the remote IP address to filter on.</span></span>
<span data-ttu-id="02d77-132">Przykładowe dane wejściowe: "127.0.0.1" dla pojedynczego wpisu adresu.</span><span class="sxs-lookup"><span data-stu-id="02d77-132">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="02d77-133">"127.0.0.1-127.0.0.255" dla zakresu.</span><span class="sxs-lookup"><span data-stu-id="02d77-133">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="02d77-134">"127.0.0.1; 127.0.0.5;" dla wielu wpisów.</span><span class="sxs-lookup"><span data-stu-id="02d77-134">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="02d77-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="02d77-135">-RemotePort</span></span>
<span data-ttu-id="02d77-136">Określa port zdalny, według którego ma zostać wykonane filtrowanie.</span><span class="sxs-lookup"><span data-stu-id="02d77-136">Specifies the Remote Port to filter on.</span></span>
<span data-ttu-id="02d77-137">Przykładowe dane wejściowe portu zdalnego: "80" dla wpisu Single Port.</span><span class="sxs-lookup"><span data-stu-id="02d77-137">Remote port Example inputs: "80" for single port entry.</span></span>
<span data-ttu-id="02d77-138">"80-85" dla zakresu.</span><span class="sxs-lookup"><span data-stu-id="02d77-138">"80-85" for range.</span></span>
<span data-ttu-id="02d77-139">"80; 443;" dla wielu wpisów.</span><span class="sxs-lookup"><span data-stu-id="02d77-139">"80;443;" for multiple entries.</span></span>

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

### <span data-ttu-id="02d77-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02d77-140">CommonParameters</span></span>
<span data-ttu-id="02d77-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02d77-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02d77-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02d77-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02d77-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="02d77-143">INPUTS</span></span>

### <span data-ttu-id="02d77-144">System. String</span><span class="sxs-lookup"><span data-stu-id="02d77-144">System.String</span></span>

## <span data-ttu-id="02d77-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="02d77-145">OUTPUTS</span></span>

### <span data-ttu-id="02d77-146">Microsoft. Azure. Commands. Network. models. PSPacketCaptureFilter</span><span class="sxs-lookup"><span data-stu-id="02d77-146">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span></span>

## <span data-ttu-id="02d77-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="02d77-147">NOTES</span></span>
<span data-ttu-id="02d77-148">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, monitor, pakiet, przechwytywanie, ruch, filtr</span><span class="sxs-lookup"><span data-stu-id="02d77-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span> 

## <span data-ttu-id="02d77-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="02d77-149">RELATED LINKS</span></span>

[<span data-ttu-id="02d77-150">Nowe — AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="02d77-150">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="02d77-151">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="02d77-151">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="02d77-152">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="02d77-152">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="02d77-153">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="02d77-153">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="02d77-154">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="02d77-154">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="02d77-155">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="02d77-155">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="02d77-156">Start — AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="02d77-156">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="02d77-157">Nowe — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="02d77-157">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="02d77-158">Nowe — AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="02d77-158">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="02d77-159">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="02d77-159">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="02d77-160">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="02d77-160">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="02d77-161">Zatrzymaj — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="02d77-161">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="02d77-162">Nowe — AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="02d77-162">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="02d77-163">Test — AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="02d77-163">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="02d77-164">Test — AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="02d77-164">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="02d77-165">Zatrzymaj — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="02d77-165">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="02d77-166">Start — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="02d77-166">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="02d77-167">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="02d77-167">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="02d77-168">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="02d77-168">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="02d77-169">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="02d77-169">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="02d77-170">Nowe — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="02d77-170">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="02d77-171">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="02d77-171">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="02d77-172">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="02d77-172">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="02d77-173">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="02d77-173">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="02d77-174">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="02d77-174">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="02d77-175">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="02d77-175">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="02d77-176">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="02d77-176">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)