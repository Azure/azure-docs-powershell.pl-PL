---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 42067c978c7791740d10af4df88c51dde3096c0e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398397"
---
# <span data-ttu-id="d2a73-101">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d2a73-101">Stop-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="d2a73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2a73-102">SYNOPSIS</span></span>
<span data-ttu-id="d2a73-103">Zatrzymuje sesję przechwytywania uruchomionego pakietu</span><span class="sxs-lookup"><span data-stu-id="d2a73-103">Stops a running packet capture session</span></span>

## <span data-ttu-id="d2a73-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d2a73-104">SYNTAX</span></span>

### <span data-ttu-id="d2a73-105">SetByResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="d2a73-105">SetByResource (Default)</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2a73-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="d2a73-106">SetByName</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2a73-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="d2a73-107">SetByLocation</span></span>
```
Stop-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2a73-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d2a73-108">DESCRIPTION</span></span>
<span data-ttu-id="d2a73-109">Sesja Stop-AzNetworkWatcherPacketCapture zatrzyma sesję przechwytywania uruchomionego pakietu.</span><span class="sxs-lookup"><span data-stu-id="d2a73-109">The Stop-AzNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="d2a73-110">Po zatrzymaniu sesji plik przechwytywania pakietów jest przekazywany do magazynu i/lub zapisywany lokalnie na maszyny wirtualnej w zależności od jej konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="d2a73-110">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="d2a73-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d2a73-111">EXAMPLES</span></span>

### <span data-ttu-id="d2a73-112">Przykład 1. Zatrzymanie sesji przechwytywania pakietów</span><span class="sxs-lookup"><span data-stu-id="d2a73-112">Example 1: Stop a packet capture session</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="d2a73-113">W tym przykładzie zatrzymujemy uruchamianą sesję przechwytywania pakietów o nazwie "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="d2a73-113">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="d2a73-114">Po zatrzymaniu sesji plik przechwytywania pakietów jest przekazywany do magazynu i/lub zapisywany lokalnie na maszyny wirtualnej, w zależności od jej konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="d2a73-114">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="d2a73-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2a73-115">PARAMETERS</span></span>

### <span data-ttu-id="d2a73-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="d2a73-116">-AsJob</span></span>
<span data-ttu-id="d2a73-117">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d2a73-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d2a73-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2a73-118">-DefaultProfile</span></span>
<span data-ttu-id="d2a73-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d2a73-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2a73-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d2a73-120">-Location</span></span>
<span data-ttu-id="d2a73-121">Lokalizacja czujki sieci.</span><span class="sxs-lookup"><span data-stu-id="d2a73-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="d2a73-122">— NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d2a73-122">-NetworkWatcher</span></span>
<span data-ttu-id="d2a73-123">Zasób obserwowania sieci.</span><span class="sxs-lookup"><span data-stu-id="d2a73-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="d2a73-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d2a73-124">-NetworkWatcherName</span></span>
<span data-ttu-id="d2a73-125">Nazwa osoby oglądacej sieć.</span><span class="sxs-lookup"><span data-stu-id="d2a73-125">The name of network watcher.</span></span>

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

### <span data-ttu-id="d2a73-126">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="d2a73-126">-PacketCaptureName</span></span>
<span data-ttu-id="d2a73-127">Nazwa przechwytywania pakietów.</span><span class="sxs-lookup"><span data-stu-id="d2a73-127">The packet capture name.</span></span>

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

### <span data-ttu-id="d2a73-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2a73-128">-PassThru</span></span>
<span data-ttu-id="d2a73-129">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="d2a73-129">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="d2a73-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2a73-130">-ResourceGroupName</span></span>
<span data-ttu-id="d2a73-131">Nazwa grupy zasobów obserwowanych sieci.</span><span class="sxs-lookup"><span data-stu-id="d2a73-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="d2a73-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d2a73-132">-Confirm</span></span>
<span data-ttu-id="d2a73-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d2a73-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2a73-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2a73-134">-WhatIf</span></span>
<span data-ttu-id="d2a73-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2a73-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2a73-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d2a73-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2a73-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2a73-137">CommonParameters</span></span>
<span data-ttu-id="d2a73-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2a73-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2a73-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2a73-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2a73-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2a73-140">INPUTS</span></span>

### <span data-ttu-id="d2a73-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d2a73-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="d2a73-142">System.String</span><span class="sxs-lookup"><span data-stu-id="d2a73-142">System.String</span></span>

## <span data-ttu-id="d2a73-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2a73-143">OUTPUTS</span></span>

### <span data-ttu-id="d2a73-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d2a73-144">System.Boolean</span></span>

## <span data-ttu-id="d2a73-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d2a73-145">NOTES</span></span>
<span data-ttu-id="d2a73-146">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span><span class="sxs-lookup"><span data-stu-id="d2a73-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="d2a73-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d2a73-147">RELATED LINKS</span></span>

[<span data-ttu-id="d2a73-148">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d2a73-148">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d2a73-149">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d2a73-149">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="d2a73-150">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d2a73-150">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d2a73-151">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d2a73-151">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d2a73-152">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d2a73-152">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="d2a73-153">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d2a73-153">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="d2a73-154">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d2a73-154">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="d2a73-155">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d2a73-155">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="d2a73-156">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d2a73-156">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="d2a73-157">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d2a73-157">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d2a73-158">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d2a73-158">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="d2a73-159">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d2a73-159">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="d2a73-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="d2a73-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="d2a73-161">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d2a73-161">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d2a73-162">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2a73-162">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="d2a73-163">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="d2a73-163">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="d2a73-164">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d2a73-164">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d2a73-165">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d2a73-165">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d2a73-166">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d2a73-166">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d2a73-167">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="d2a73-167">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="d2a73-168">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d2a73-168">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d2a73-169">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d2a73-169">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d2a73-170">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="d2a73-170">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="d2a73-171">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="d2a73-171">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="d2a73-172">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="d2a73-172">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="d2a73-173">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="d2a73-173">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="d2a73-174">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d2a73-174">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
