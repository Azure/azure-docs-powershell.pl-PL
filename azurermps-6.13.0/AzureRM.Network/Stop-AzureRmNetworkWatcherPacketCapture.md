---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermnetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: fc78481ceeec796fe4a498bf76092955adb1639a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547424"
---
# <span data-ttu-id="303e1-101">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="303e1-101">Stop-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="303e1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="303e1-102">SYNOPSIS</span></span>
<span data-ttu-id="303e1-103">Zatrzymuje uruchomioną sesję przechwytywania pakietów.</span><span class="sxs-lookup"><span data-stu-id="303e1-103">Stops a running packet capture session</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="303e1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="303e1-104">SYNTAX</span></span>

### <span data-ttu-id="303e1-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="303e1-105">SetByResource (Default)</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="303e1-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="303e1-106">SetByName</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="303e1-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="303e1-107">SetByLocation</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="303e1-108">Opis</span><span class="sxs-lookup"><span data-stu-id="303e1-108">DESCRIPTION</span></span>
<span data-ttu-id="303e1-109">Stop-AzureRmNetworkWatcherPacketCapture zatrzymuje uruchomioną sesję przechwytywania pakietów.</span><span class="sxs-lookup"><span data-stu-id="303e1-109">The Stop-AzureRmNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="303e1-110">Po zatrzymaniu sesji plik przechwytywania pakietu zostanie przekazany do magazynu i/lub zapisany lokalnie na maszynie wirtualnej w zależności od konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="303e1-110">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="303e1-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="303e1-111">EXAMPLES</span></span>

### <span data-ttu-id="303e1-112">Przykład 1: zatrzymywanie sesji przechwytywania pakietów</span><span class="sxs-lookup"><span data-stu-id="303e1-112">Example 1: Stop a packet capture session</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="303e1-113">W tym przykładzie zatrzymano uruchomioną sesję przechwytywania pakietów o nazwie "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="303e1-113">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="303e1-114">Po zatrzymaniu sesji plik przechwytywania pakietu zostanie przekazany do magazynu i/lub zapisany lokalnie na maszynie wirtualnej w zależności od konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="303e1-114">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="303e1-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="303e1-115">PARAMETERS</span></span>

### <span data-ttu-id="303e1-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="303e1-116">-AsJob</span></span>
<span data-ttu-id="303e1-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="303e1-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="303e1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="303e1-118">-DefaultProfile</span></span>
<span data-ttu-id="303e1-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="303e1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="303e1-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="303e1-120">-Location</span></span>
<span data-ttu-id="303e1-121">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="303e1-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="303e1-122">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="303e1-122">-NetworkWatcher</span></span>
<span data-ttu-id="303e1-123">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="303e1-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="303e1-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="303e1-124">-NetworkWatcherName</span></span>
<span data-ttu-id="303e1-125">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="303e1-125">The name of network watcher.</span></span>

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

### <span data-ttu-id="303e1-126">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="303e1-126">-PacketCaptureName</span></span>
<span data-ttu-id="303e1-127">Nazwa przechwytywania pakietu.</span><span class="sxs-lookup"><span data-stu-id="303e1-127">The packet capture name.</span></span>

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

### <span data-ttu-id="303e1-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="303e1-128">-PassThru</span></span>
<span data-ttu-id="303e1-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="303e1-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="303e1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="303e1-130">-ResourceGroupName</span></span>
<span data-ttu-id="303e1-131">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="303e1-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="303e1-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="303e1-132">-Confirm</span></span>
<span data-ttu-id="303e1-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="303e1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="303e1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="303e1-134">-WhatIf</span></span>
<span data-ttu-id="303e1-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="303e1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="303e1-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="303e1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="303e1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="303e1-137">CommonParameters</span></span>
<span data-ttu-id="303e1-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="303e1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="303e1-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="303e1-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="303e1-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="303e1-140">INPUTS</span></span>

### <span data-ttu-id="303e1-141">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="303e1-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="303e1-142">Parametry: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="303e1-142">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="303e1-143">System. String</span><span class="sxs-lookup"><span data-stu-id="303e1-143">System.String</span></span>
<span data-ttu-id="303e1-144">Parametry: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="303e1-144">Parameters: NetworkWatcherName (ByValue)</span></span>

## <span data-ttu-id="303e1-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="303e1-145">OUTPUTS</span></span>

### <span data-ttu-id="303e1-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="303e1-146">System.Boolean</span></span>

## <span data-ttu-id="303e1-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="303e1-147">NOTES</span></span>
<span data-ttu-id="303e1-148">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, Monitor sieci, pakiet, przechwytywanie, ruch</span><span class="sxs-lookup"><span data-stu-id="303e1-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="303e1-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="303e1-149">RELATED LINKS</span></span>

[<span data-ttu-id="303e1-150">Nowe — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="303e1-150">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="303e1-151">Nowe — AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="303e1-151">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="303e1-152">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="303e1-152">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="303e1-153">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="303e1-153">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="303e1-154">Nowe — AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="303e1-154">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="303e1-155">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="303e1-155">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="303e1-156">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="303e1-156">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="303e1-157">Test — AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="303e1-157">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="303e1-158">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="303e1-158">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="303e1-159">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="303e1-159">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="303e1-160">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="303e1-160">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="303e1-161">Start — AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="303e1-161">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="303e1-162">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="303e1-162">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="303e1-163">Zatrzymaj — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="303e1-163">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="303e1-164">Nowe — AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="303e1-164">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="303e1-165">Test — AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="303e1-165">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="303e1-166">Zatrzymaj — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="303e1-166">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="303e1-167">Start — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="303e1-167">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="303e1-168">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="303e1-168">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="303e1-169">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="303e1-169">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="303e1-170">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="303e1-170">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="303e1-171">Nowe — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="303e1-171">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="303e1-172">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="303e1-172">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="303e1-173">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="303e1-173">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="303e1-174">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="303e1-174">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="303e1-175">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="303e1-175">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="303e1-176">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="303e1-176">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
