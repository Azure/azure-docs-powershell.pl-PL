---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 35bd138a682eaca3b58ba82190961d3b7d7e3e26
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412184"
---
# <span data-ttu-id="0f818-101">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0f818-101">Remove-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="0f818-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f818-102">SYNOPSIS</span></span>
<span data-ttu-id="0f818-103">Usuwa zasób przechwytywania pakietów.</span><span class="sxs-lookup"><span data-stu-id="0f818-103">Removes a packet capture resource.</span></span>

## <span data-ttu-id="0f818-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0f818-104">SYNTAX</span></span>

### <span data-ttu-id="0f818-105">SetByResource (Default)</span><span class="sxs-lookup"><span data-stu-id="0f818-105">SetByResource (Default)</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f818-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="0f818-106">SetByName</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f818-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="0f818-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f818-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="0f818-108">DESCRIPTION</span></span>
<span data-ttu-id="0f818-109">Ta Remove-AzNetworkWatcherPacketCapture usuwa zasób przechwytywania pakietów.</span><span class="sxs-lookup"><span data-stu-id="0f818-109">The Remove-AzNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="0f818-110">Zaleca się dzwonienie do Stop-AzNetworkWatcherPacketCapture przed wywołaniem funkcji Remove-AzNetworkWatcherPacketCapture.</span><span class="sxs-lookup"><span data-stu-id="0f818-110">It is recommended to call Stop-AzNetworkWatcherPacketCapture before calling Remove-AzNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="0f818-111">Jeśli sesja przechwytywania pakietów jest uruchomiona, Remove-AzNetworkWatcherPacketCapture nazywana przechwytywanie pakietów może nie zostać zapisana.</span><span class="sxs-lookup"><span data-stu-id="0f818-111">If the packet capture session is running when Remove-AzNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="0f818-112">Jeśli sesja została zatrzymana przed usunięciem pliku cap zawierającego przechwycone dane, nie zostanie usunięty.</span><span class="sxs-lookup"><span data-stu-id="0f818-112">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="0f818-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0f818-113">EXAMPLES</span></span>

### <span data-ttu-id="0f818-114">Przykład 1. Usuwanie sesji przechwytywania pakietów</span><span class="sxs-lookup"><span data-stu-id="0f818-114">Example 1: Remove a packet capture session</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="0f818-115">W tym przykładzie usuwamy istniejącą sesję przechwytywania pakietów o nazwie "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="0f818-115">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="0f818-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f818-116">PARAMETERS</span></span>

### <span data-ttu-id="0f818-117">— AsJob</span><span class="sxs-lookup"><span data-stu-id="0f818-117">-AsJob</span></span>
<span data-ttu-id="0f818-118">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0f818-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0f818-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f818-119">-DefaultProfile</span></span>
<span data-ttu-id="0f818-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0f818-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f818-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="0f818-121">-Location</span></span>
<span data-ttu-id="0f818-122">Lokalizacja czujki sieci.</span><span class="sxs-lookup"><span data-stu-id="0f818-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="0f818-123">— NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0f818-123">-NetworkWatcher</span></span>
<span data-ttu-id="0f818-124">Zasób obserwowania sieci.</span><span class="sxs-lookup"><span data-stu-id="0f818-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="0f818-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="0f818-125">-NetworkWatcherName</span></span>
<span data-ttu-id="0f818-126">Nazwa osoby oglądacej sieć.</span><span class="sxs-lookup"><span data-stu-id="0f818-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="0f818-127">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="0f818-127">-PacketCaptureName</span></span>
<span data-ttu-id="0f818-128">Nazwa przechwytywania pakietów.</span><span class="sxs-lookup"><span data-stu-id="0f818-128">The packet capture name.</span></span>

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

### <span data-ttu-id="0f818-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0f818-129">-PassThru</span></span>
<span data-ttu-id="0f818-130">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="0f818-130">Returns an object representing the item with which you are working.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f818-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f818-131">-ResourceGroupName</span></span>
<span data-ttu-id="0f818-132">Nazwa grupy zasobów obserwowanych sieci.</span><span class="sxs-lookup"><span data-stu-id="0f818-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="0f818-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0f818-133">-Confirm</span></span>
<span data-ttu-id="0f818-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0f818-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f818-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f818-135">-WhatIf</span></span>
<span data-ttu-id="0f818-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f818-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f818-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0f818-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f818-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f818-138">CommonParameters</span></span>
<span data-ttu-id="0f818-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f818-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f818-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f818-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f818-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0f818-141">INPUTS</span></span>

### <span data-ttu-id="0f818-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0f818-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="0f818-143">System.String</span><span class="sxs-lookup"><span data-stu-id="0f818-143">System.String</span></span>

## <span data-ttu-id="0f818-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0f818-144">OUTPUTS</span></span>

### <span data-ttu-id="0f818-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0f818-145">System.Boolean</span></span>

## <span data-ttu-id="0f818-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0f818-146">NOTES</span></span>
<span data-ttu-id="0f818-147">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span><span class="sxs-lookup"><span data-stu-id="0f818-147">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="0f818-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0f818-148">RELATED LINKS</span></span>

[<span data-ttu-id="0f818-149">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0f818-149">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="0f818-150">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0f818-150">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="0f818-151">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0f818-151">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="0f818-152">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="0f818-152">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="0f818-153">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="0f818-153">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="0f818-154">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="0f818-154">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="0f818-155">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="0f818-155">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="0f818-156">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0f818-156">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0f818-157">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="0f818-157">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="0f818-158">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0f818-158">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0f818-159">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0f818-159">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0f818-160">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0f818-160">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0f818-161">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="0f818-161">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="0f818-162">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="0f818-162">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="0f818-163">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="0f818-163">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="0f818-164">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0f818-164">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0f818-165">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0f818-165">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0f818-166">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0f818-166">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0f818-167">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="0f818-167">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="0f818-168">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0f818-168">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0f818-169">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0f818-169">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0f818-170">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="0f818-170">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="0f818-171">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="0f818-171">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="0f818-172">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="0f818-172">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="0f818-173">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="0f818-173">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="0f818-174">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="0f818-174">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="0f818-175">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0f818-175">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
