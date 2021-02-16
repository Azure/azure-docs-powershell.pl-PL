---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: d6d11590699b52bb7245222ddaa01fbc42938d22
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100414003"
---
# <span data-ttu-id="0daac-101">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0daac-101">Remove-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="0daac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0daac-102">SYNOPSIS</span></span>
<span data-ttu-id="0daac-103">Usuwa zasób przechwytywania pakietów.</span><span class="sxs-lookup"><span data-stu-id="0daac-103">Removes a packet capture resource.</span></span>

## <span data-ttu-id="0daac-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0daac-104">SYNTAX</span></span>

### <span data-ttu-id="0daac-105">SetByResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="0daac-105">SetByResource (Default)</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0daac-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="0daac-106">SetByName</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0daac-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="0daac-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0daac-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="0daac-108">DESCRIPTION</span></span>
<span data-ttu-id="0daac-109">Ta Remove-AzNetworkWatcherPacketCapture usuwa zasób przechwytywania pakietów.</span><span class="sxs-lookup"><span data-stu-id="0daac-109">The Remove-AzNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="0daac-110">Zalecane jest dzwonienie do Stop-AzNetworkWatcherPacketCapture przed wywołaniem funkcji Remove-AzNetworkWatcherPacketCapture.</span><span class="sxs-lookup"><span data-stu-id="0daac-110">It is recommended to call Stop-AzNetworkWatcherPacketCapture before calling Remove-AzNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="0daac-111">Jeśli sesja przechwytywania pakietów jest uruchomiona, Remove-AzNetworkWatcherPacketCapture nazywana przechwytywanie pakietów może nie zostać zapisana.</span><span class="sxs-lookup"><span data-stu-id="0daac-111">If the packet capture session is running when Remove-AzNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="0daac-112">Jeśli sesja została zatrzymana przed usunięciem pliku cap zawierającego przechwycone dane, nie zostanie usunięty.</span><span class="sxs-lookup"><span data-stu-id="0daac-112">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="0daac-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0daac-113">EXAMPLES</span></span>

### <span data-ttu-id="0daac-114">Przykład 1. Usuwanie sesji przechwytywania pakietów</span><span class="sxs-lookup"><span data-stu-id="0daac-114">Example 1: Remove a packet capture session</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="0daac-115">W tym przykładzie usuwamy istniejącą sesję przechwytywania pakietów o nazwie "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="0daac-115">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="0daac-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0daac-116">PARAMETERS</span></span>

### <span data-ttu-id="0daac-117">— AsJob</span><span class="sxs-lookup"><span data-stu-id="0daac-117">-AsJob</span></span>
<span data-ttu-id="0daac-118">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0daac-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0daac-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0daac-119">-DefaultProfile</span></span>
<span data-ttu-id="0daac-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0daac-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0daac-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="0daac-121">-Location</span></span>
<span data-ttu-id="0daac-122">Lokalizacja czujki sieci.</span><span class="sxs-lookup"><span data-stu-id="0daac-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="0daac-123">— NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0daac-123">-NetworkWatcher</span></span>
<span data-ttu-id="0daac-124">Zasób obserwowania sieci.</span><span class="sxs-lookup"><span data-stu-id="0daac-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="0daac-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="0daac-125">-NetworkWatcherName</span></span>
<span data-ttu-id="0daac-126">Nazwa osoby oglądacej sieć.</span><span class="sxs-lookup"><span data-stu-id="0daac-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="0daac-127">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="0daac-127">-PacketCaptureName</span></span>
<span data-ttu-id="0daac-128">Nazwa przechwytywania pakietów.</span><span class="sxs-lookup"><span data-stu-id="0daac-128">The packet capture name.</span></span>

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

### <span data-ttu-id="0daac-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0daac-129">-PassThru</span></span>
<span data-ttu-id="0daac-130">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="0daac-130">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="0daac-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0daac-131">-ResourceGroupName</span></span>
<span data-ttu-id="0daac-132">Nazwa grupy zasobów obserwowanych sieci.</span><span class="sxs-lookup"><span data-stu-id="0daac-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="0daac-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0daac-133">-Confirm</span></span>
<span data-ttu-id="0daac-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0daac-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0daac-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0daac-135">-WhatIf</span></span>
<span data-ttu-id="0daac-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0daac-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0daac-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0daac-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0daac-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0daac-138">CommonParameters</span></span>
<span data-ttu-id="0daac-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0daac-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0daac-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0daac-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0daac-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0daac-141">INPUTS</span></span>

### <span data-ttu-id="0daac-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0daac-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="0daac-143">System.String</span><span class="sxs-lookup"><span data-stu-id="0daac-143">System.String</span></span>

## <span data-ttu-id="0daac-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0daac-144">OUTPUTS</span></span>

### <span data-ttu-id="0daac-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0daac-145">System.Boolean</span></span>

## <span data-ttu-id="0daac-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0daac-146">NOTES</span></span>
<span data-ttu-id="0daac-147">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span><span class="sxs-lookup"><span data-stu-id="0daac-147">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="0daac-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0daac-148">RELATED LINKS</span></span>

[<span data-ttu-id="0daac-149">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0daac-149">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="0daac-150">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0daac-150">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="0daac-151">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0daac-151">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="0daac-152">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="0daac-152">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="0daac-153">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="0daac-153">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="0daac-154">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="0daac-154">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="0daac-155">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="0daac-155">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="0daac-156">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0daac-156">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0daac-157">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="0daac-157">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="0daac-158">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0daac-158">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0daac-159">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0daac-159">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0daac-160">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0daac-160">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0daac-161">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="0daac-161">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="0daac-162">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="0daac-162">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="0daac-163">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="0daac-163">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="0daac-164">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0daac-164">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0daac-165">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0daac-165">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0daac-166">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0daac-166">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0daac-167">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="0daac-167">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="0daac-168">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0daac-168">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0daac-169">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0daac-169">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0daac-170">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="0daac-170">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="0daac-171">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="0daac-171">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="0daac-172">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="0daac-172">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="0daac-173">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="0daac-173">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="0daac-174">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="0daac-174">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="0daac-175">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0daac-175">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
