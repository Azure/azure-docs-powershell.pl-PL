---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 0c0568dc11411e27af1db9d9e3d59c0026b0a39a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552675"
---
# <span data-ttu-id="5e17f-101">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5e17f-101">Remove-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="5e17f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5e17f-102">SYNOPSIS</span></span>
<span data-ttu-id="5e17f-103">Usuwa zasób przechwytywania pakietu.</span><span class="sxs-lookup"><span data-stu-id="5e17f-103">Removes a packet capture resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e17f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5e17f-104">SYNTAX</span></span>

### <span data-ttu-id="5e17f-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5e17f-105">SetByResource (Default)</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e17f-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="5e17f-106">SetByName</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e17f-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="5e17f-107">SetByLocation</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e17f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5e17f-108">DESCRIPTION</span></span>
<span data-ttu-id="5e17f-109">Remove-AzureRmNetworkWatcherPacketCapture usuwa zasób przechwytywania pakietu.</span><span class="sxs-lookup"><span data-stu-id="5e17f-109">The Remove-AzureRmNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="5e17f-110">Zaleca się nawiązanie połączenia Stop-AzureRmNetworkWatcherPacketCapture przed wywołaniem funkcji Remove-AzureRmNetworkWatcherPacketCapture.</span><span class="sxs-lookup"><span data-stu-id="5e17f-110">It is recommended to call Stop-AzureRmNetworkWatcherPacketCapture before calling Remove-AzureRmNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="5e17f-111">Jeśli sesja przechwytywania pakietów jest uruchomiona, gdy Remove-AzureRmNetworkWatcherPacketCapture jest nazywany przechwytywanie pakietów, być może nie zostanie zapisana.</span><span class="sxs-lookup"><span data-stu-id="5e17f-111">If the packet capture session is running when Remove-AzureRmNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="5e17f-112">Jeśli sesja zostanie zatrzymana przed usunięciem pliku Cap zawierającego przechwycone dane, nie zostanie usunięty.</span><span class="sxs-lookup"><span data-stu-id="5e17f-112">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="5e17f-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5e17f-113">EXAMPLES</span></span>

### <span data-ttu-id="5e17f-114">Przykład 1: usuwanie sesji przechwytywania pakietów</span><span class="sxs-lookup"><span data-stu-id="5e17f-114">Example 1: Remove a packet capture session</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="5e17f-115">W tym przykładzie została usunięta istniejąca sesja przechwytywania pakietu o nazwie "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="5e17f-115">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="5e17f-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5e17f-116">PARAMETERS</span></span>

### <span data-ttu-id="5e17f-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5e17f-117">-AsJob</span></span>
<span data-ttu-id="5e17f-118">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="5e17f-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5e17f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e17f-119">-DefaultProfile</span></span>
<span data-ttu-id="5e17f-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5e17f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e17f-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="5e17f-121">-Location</span></span>
<span data-ttu-id="5e17f-122">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="5e17f-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="5e17f-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5e17f-123">-NetworkWatcher</span></span>
<span data-ttu-id="5e17f-124">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="5e17f-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="5e17f-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="5e17f-125">-NetworkWatcherName</span></span>
<span data-ttu-id="5e17f-126">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="5e17f-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="5e17f-127">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="5e17f-127">-PacketCaptureName</span></span>
<span data-ttu-id="5e17f-128">Nazwa przechwytywania pakietu.</span><span class="sxs-lookup"><span data-stu-id="5e17f-128">The packet capture name.</span></span>

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

### <span data-ttu-id="5e17f-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5e17f-129">-PassThru</span></span>
<span data-ttu-id="5e17f-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="5e17f-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="5e17f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e17f-131">-ResourceGroupName</span></span>
<span data-ttu-id="5e17f-132">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="5e17f-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="5e17f-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5e17f-133">-Confirm</span></span>
<span data-ttu-id="5e17f-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e17f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e17f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e17f-135">-WhatIf</span></span>
<span data-ttu-id="5e17f-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e17f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e17f-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5e17f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e17f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e17f-138">CommonParameters</span></span>
<span data-ttu-id="5e17f-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e17f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e17f-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e17f-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e17f-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5e17f-141">INPUTS</span></span>

### <span data-ttu-id="5e17f-142">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5e17f-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="5e17f-143">Parametry: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5e17f-143">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="5e17f-144">System. String</span><span class="sxs-lookup"><span data-stu-id="5e17f-144">System.String</span></span>
<span data-ttu-id="5e17f-145">Parametry: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5e17f-145">Parameters: NetworkWatcherName (ByValue)</span></span>

## <span data-ttu-id="5e17f-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5e17f-146">OUTPUTS</span></span>

### <span data-ttu-id="5e17f-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5e17f-147">System.Boolean</span></span>

## <span data-ttu-id="5e17f-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5e17f-148">NOTES</span></span>
<span data-ttu-id="5e17f-149">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, Monitor sieci, pakiet, przechwytywanie, ruch, usuwanie</span><span class="sxs-lookup"><span data-stu-id="5e17f-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="5e17f-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5e17f-150">RELATED LINKS</span></span>

[<span data-ttu-id="5e17f-151">Nowe — AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5e17f-151">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="5e17f-152">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5e17f-152">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="5e17f-153">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5e17f-153">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="5e17f-154">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="5e17f-154">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="5e17f-155">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="5e17f-155">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="5e17f-156">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="5e17f-156">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="5e17f-157">Start — AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="5e17f-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="5e17f-158">Nowe — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5e17f-158">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5e17f-159">Nowe — AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="5e17f-159">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="5e17f-160">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5e17f-160">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5e17f-161">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5e17f-161">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5e17f-162">Zatrzymaj — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5e17f-162">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5e17f-163">Nowe — AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="5e17f-163">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="5e17f-164">Test — AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="5e17f-164">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="5e17f-165">Test — AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="5e17f-165">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="5e17f-166">Zatrzymaj — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5e17f-166">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5e17f-167">Start — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5e17f-167">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5e17f-168">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5e17f-168">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5e17f-169">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="5e17f-169">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="5e17f-170">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5e17f-170">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5e17f-171">Nowe — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5e17f-171">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5e17f-172">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="5e17f-172">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="5e17f-173">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="5e17f-173">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="5e17f-174">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="5e17f-174">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="5e17f-175">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="5e17f-175">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="5e17f-176">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="5e17f-176">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="5e17f-177">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5e17f-177">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
