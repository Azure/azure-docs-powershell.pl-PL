---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 922026b14531cc1c65f60901914383b402d06889
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503132"
---
# <span data-ttu-id="74f7d-101">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="74f7d-101">Stop-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="74f7d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="74f7d-102">SYNOPSIS</span></span>
<span data-ttu-id="74f7d-103">Zatrzymuje uruchomioną sesję przechwytywania pakietów.</span><span class="sxs-lookup"><span data-stu-id="74f7d-103">Stops a running packet capture session</span></span>

## <span data-ttu-id="74f7d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="74f7d-104">SYNTAX</span></span>

### <span data-ttu-id="74f7d-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="74f7d-105">SetByResource (Default)</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74f7d-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="74f7d-106">SetByName</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74f7d-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="74f7d-107">SetByLocation</span></span>
```
Stop-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74f7d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="74f7d-108">DESCRIPTION</span></span>
<span data-ttu-id="74f7d-109">Stop-AzNetworkWatcherPacketCapture zatrzymuje uruchomioną sesję przechwytywania pakietów.</span><span class="sxs-lookup"><span data-stu-id="74f7d-109">The Stop-AzNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="74f7d-110">Po zatrzymaniu sesji plik przechwytywania pakietu zostanie przekazany do magazynu i/lub zapisany lokalnie na maszynie wirtualnej w zależności od konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="74f7d-110">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="74f7d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="74f7d-111">EXAMPLES</span></span>

### <span data-ttu-id="74f7d-112">Przykład 1: zatrzymywanie sesji przechwytywania pakietów</span><span class="sxs-lookup"><span data-stu-id="74f7d-112">Example 1: Stop a packet capture session</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="74f7d-113">W tym przykładzie zatrzymano uruchomioną sesję przechwytywania pakietów o nazwie "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="74f7d-113">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="74f7d-114">Po zatrzymaniu sesji plik przechwytywania pakietu zostanie przekazany do magazynu i/lub zapisany lokalnie na maszynie wirtualnej w zależności od konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="74f7d-114">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="74f7d-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="74f7d-115">PARAMETERS</span></span>

### <span data-ttu-id="74f7d-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74f7d-116">-AsJob</span></span>
<span data-ttu-id="74f7d-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="74f7d-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="74f7d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74f7d-118">-DefaultProfile</span></span>
<span data-ttu-id="74f7d-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="74f7d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74f7d-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="74f7d-120">-Location</span></span>
<span data-ttu-id="74f7d-121">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="74f7d-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="74f7d-122">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="74f7d-122">-NetworkWatcher</span></span>
<span data-ttu-id="74f7d-123">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="74f7d-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="74f7d-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="74f7d-124">-NetworkWatcherName</span></span>
<span data-ttu-id="74f7d-125">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="74f7d-125">The name of network watcher.</span></span>

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

### <span data-ttu-id="74f7d-126">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="74f7d-126">-PacketCaptureName</span></span>
<span data-ttu-id="74f7d-127">Nazwa przechwytywania pakietu.</span><span class="sxs-lookup"><span data-stu-id="74f7d-127">The packet capture name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74f7d-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74f7d-128">-PassThru</span></span>
<span data-ttu-id="74f7d-129">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="74f7d-129">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="74f7d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74f7d-130">-ResourceGroupName</span></span>
<span data-ttu-id="74f7d-131">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="74f7d-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="74f7d-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="74f7d-132">-Confirm</span></span>
<span data-ttu-id="74f7d-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74f7d-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74f7d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74f7d-134">-WhatIf</span></span>
<span data-ttu-id="74f7d-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74f7d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74f7d-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="74f7d-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74f7d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74f7d-137">CommonParameters</span></span>
<span data-ttu-id="74f7d-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74f7d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74f7d-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74f7d-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74f7d-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74f7d-140">INPUTS</span></span>

### <span data-ttu-id="74f7d-141">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="74f7d-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="74f7d-142">System. String</span><span class="sxs-lookup"><span data-stu-id="74f7d-142">System.String</span></span>

## <span data-ttu-id="74f7d-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="74f7d-143">OUTPUTS</span></span>

### <span data-ttu-id="74f7d-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="74f7d-144">System.Boolean</span></span>

## <span data-ttu-id="74f7d-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="74f7d-145">NOTES</span></span>
<span data-ttu-id="74f7d-146">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, Monitor sieci, pakiet, przechwytywanie, ruch</span><span class="sxs-lookup"><span data-stu-id="74f7d-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="74f7d-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="74f7d-147">RELATED LINKS</span></span>

[<span data-ttu-id="74f7d-148">Nowe — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="74f7d-148">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="74f7d-149">Nowe — AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="74f7d-149">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="74f7d-150">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="74f7d-150">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="74f7d-151">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="74f7d-151">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="74f7d-152">Nowe — AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="74f7d-152">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="74f7d-153">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="74f7d-153">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="74f7d-154">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="74f7d-154">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="74f7d-155">Test — AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="74f7d-155">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="74f7d-156">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="74f7d-156">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="74f7d-157">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="74f7d-157">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="74f7d-158">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="74f7d-158">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="74f7d-159">Start — AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="74f7d-159">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="74f7d-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="74f7d-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="74f7d-161">Zatrzymaj — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="74f7d-161">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="74f7d-162">Nowe — AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="74f7d-162">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="74f7d-163">Test — AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="74f7d-163">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="74f7d-164">Zatrzymaj — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="74f7d-164">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="74f7d-165">Start — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="74f7d-165">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="74f7d-166">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="74f7d-166">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="74f7d-167">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="74f7d-167">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="74f7d-168">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="74f7d-168">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="74f7d-169">Nowe — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="74f7d-169">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="74f7d-170">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="74f7d-170">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="74f7d-171">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="74f7d-171">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="74f7d-172">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="74f7d-172">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="74f7d-173">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="74f7d-173">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="74f7d-174">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="74f7d-174">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
