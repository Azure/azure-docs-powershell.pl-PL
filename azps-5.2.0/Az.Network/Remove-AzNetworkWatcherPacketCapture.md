---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: e22b9d85bbc17897742fa2ac0cbdf3e2d8187d5b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328067"
---
# <span data-ttu-id="e05bf-101">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e05bf-101">Remove-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="e05bf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e05bf-102">SYNOPSIS</span></span>
<span data-ttu-id="e05bf-103">Usuwa zasób przechwytywania pakietu.</span><span class="sxs-lookup"><span data-stu-id="e05bf-103">Removes a packet capture resource.</span></span>

## <span data-ttu-id="e05bf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e05bf-104">SYNTAX</span></span>

### <span data-ttu-id="e05bf-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e05bf-105">SetByResource (Default)</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e05bf-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="e05bf-106">SetByName</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e05bf-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="e05bf-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e05bf-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e05bf-108">DESCRIPTION</span></span>
<span data-ttu-id="e05bf-109">Remove-AzNetworkWatcherPacketCapture usuwa zasób przechwytywania pakietu.</span><span class="sxs-lookup"><span data-stu-id="e05bf-109">The Remove-AzNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="e05bf-110">Zaleca się nawiązanie połączenia Stop-AzNetworkWatcherPacketCapture przed wywołaniem funkcji Remove-AzNetworkWatcherPacketCapture.</span><span class="sxs-lookup"><span data-stu-id="e05bf-110">It is recommended to call Stop-AzNetworkWatcherPacketCapture before calling Remove-AzNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="e05bf-111">Jeśli sesja przechwytywania pakietów jest uruchomiona, gdy Remove-AzNetworkWatcherPacketCapture jest nazywany przechwytywanie pakietów, być może nie zostanie zapisana.</span><span class="sxs-lookup"><span data-stu-id="e05bf-111">If the packet capture session is running when Remove-AzNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="e05bf-112">Jeśli sesja zostanie zatrzymana przed usunięciem pliku Cap zawierającego przechwycone dane, nie zostanie usunięty.</span><span class="sxs-lookup"><span data-stu-id="e05bf-112">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="e05bf-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e05bf-113">EXAMPLES</span></span>

### <span data-ttu-id="e05bf-114">Przykład 1: usuwanie sesji przechwytywania pakietów</span><span class="sxs-lookup"><span data-stu-id="e05bf-114">Example 1: Remove a packet capture session</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="e05bf-115">W tym przykładzie została usunięta istniejąca sesja przechwytywania pakietu o nazwie "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="e05bf-115">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="e05bf-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e05bf-116">PARAMETERS</span></span>

### <span data-ttu-id="e05bf-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e05bf-117">-AsJob</span></span>
<span data-ttu-id="e05bf-118">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e05bf-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e05bf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e05bf-119">-DefaultProfile</span></span>
<span data-ttu-id="e05bf-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e05bf-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e05bf-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e05bf-121">-Location</span></span>
<span data-ttu-id="e05bf-122">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="e05bf-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="e05bf-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e05bf-123">-NetworkWatcher</span></span>
<span data-ttu-id="e05bf-124">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="e05bf-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="e05bf-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="e05bf-125">-NetworkWatcherName</span></span>
<span data-ttu-id="e05bf-126">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="e05bf-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="e05bf-127">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="e05bf-127">-PacketCaptureName</span></span>
<span data-ttu-id="e05bf-128">Nazwa przechwytywania pakietu.</span><span class="sxs-lookup"><span data-stu-id="e05bf-128">The packet capture name.</span></span>

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

### <span data-ttu-id="e05bf-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e05bf-129">-PassThru</span></span>
<span data-ttu-id="e05bf-130">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="e05bf-130">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="e05bf-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e05bf-131">-ResourceGroupName</span></span>
<span data-ttu-id="e05bf-132">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="e05bf-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="e05bf-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e05bf-133">-Confirm</span></span>
<span data-ttu-id="e05bf-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e05bf-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e05bf-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e05bf-135">-WhatIf</span></span>
<span data-ttu-id="e05bf-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e05bf-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e05bf-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e05bf-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e05bf-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e05bf-138">CommonParameters</span></span>
<span data-ttu-id="e05bf-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e05bf-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e05bf-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e05bf-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e05bf-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e05bf-141">INPUTS</span></span>

### <span data-ttu-id="e05bf-142">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e05bf-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="e05bf-143">System. String</span><span class="sxs-lookup"><span data-stu-id="e05bf-143">System.String</span></span>

## <span data-ttu-id="e05bf-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e05bf-144">OUTPUTS</span></span>

### <span data-ttu-id="e05bf-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e05bf-145">System.Boolean</span></span>

## <span data-ttu-id="e05bf-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e05bf-146">NOTES</span></span>
<span data-ttu-id="e05bf-147">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, Monitor sieci, pakiet, przechwytywanie, ruch, usuwanie</span><span class="sxs-lookup"><span data-stu-id="e05bf-147">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="e05bf-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e05bf-148">RELATED LINKS</span></span>

[<span data-ttu-id="e05bf-149">Nowe — AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e05bf-149">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="e05bf-150">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e05bf-150">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="e05bf-151">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e05bf-151">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="e05bf-152">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="e05bf-152">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="e05bf-153">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="e05bf-153">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="e05bf-154">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="e05bf-154">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="e05bf-155">Start — AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="e05bf-155">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="e05bf-156">Nowe — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e05bf-156">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e05bf-157">Nowe — AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="e05bf-157">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="e05bf-158">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e05bf-158">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e05bf-159">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e05bf-159">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e05bf-160">Zatrzymaj — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e05bf-160">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e05bf-161">Nowe — AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="e05bf-161">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="e05bf-162">Test — AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="e05bf-162">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="e05bf-163">Test — AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="e05bf-163">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="e05bf-164">Zatrzymaj — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e05bf-164">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e05bf-165">Start — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e05bf-165">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e05bf-166">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e05bf-166">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e05bf-167">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="e05bf-167">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="e05bf-168">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e05bf-168">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e05bf-169">Nowe — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e05bf-169">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e05bf-170">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="e05bf-170">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="e05bf-171">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="e05bf-171">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="e05bf-172">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="e05bf-172">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="e05bf-173">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="e05bf-173">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="e05bf-174">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="e05bf-174">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="e05bf-175">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e05bf-175">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
