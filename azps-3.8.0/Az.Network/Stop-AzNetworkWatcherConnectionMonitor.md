---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 8840fc454601880fd2d4ed8bf7b816f7f3d83e5d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051753"
---
# <span data-ttu-id="b7c22-101">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b7c22-101">Stop-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="b7c22-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b7c22-102">SYNOPSIS</span></span>
<span data-ttu-id="b7c22-103">Zatrzymywanie monitora połączeń</span><span class="sxs-lookup"><span data-stu-id="b7c22-103">Stop a connection monitor</span></span>

## <span data-ttu-id="b7c22-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b7c22-104">SYNTAX</span></span>

### <span data-ttu-id="b7c22-105">SetByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b7c22-105">SetByName (Default)</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7c22-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b7c22-106">SetByResource</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7c22-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="b7c22-107">SetByLocation</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7c22-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b7c22-108">SetByResourceId</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7c22-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="b7c22-109">SetByInputObject</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7c22-110">Opis</span><span class="sxs-lookup"><span data-stu-id="b7c22-110">DESCRIPTION</span></span>
<span data-ttu-id="b7c22-111">Polecenie cmdlet Stop-AzNetworkWatcherConnectionMonitor powoduje zatrzymanie określonego monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="b7c22-111">The Stop-AzNetworkWatcherConnectionMonitor cmdlet stops the specified connection monitor.</span></span>

## <span data-ttu-id="b7c22-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b7c22-112">EXAMPLES</span></span>

### <span data-ttu-id="b7c22-113">Przykład 1: zatrzymywanie monitora połączeń</span><span class="sxs-lookup"><span data-stu-id="b7c22-113">Example 1: Stop a connection monitor</span></span>
```
PS C:\> Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm
```

<span data-ttu-id="b7c22-114">W tym przykładzie zatrzymano monitor połączenia określony przez nazwę i Monitor sieci</span><span class="sxs-lookup"><span data-stu-id="b7c22-114">In this example we stop connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="b7c22-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b7c22-115">PARAMETERS</span></span>

### <span data-ttu-id="b7c22-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b7c22-116">-AsJob</span></span>
<span data-ttu-id="b7c22-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b7c22-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b7c22-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7c22-118">-DefaultProfile</span></span>
<span data-ttu-id="b7c22-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b7c22-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7c22-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b7c22-120">-InputObject</span></span>
<span data-ttu-id="b7c22-121">Obiekt monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="b7c22-121">Connection monitor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7c22-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b7c22-122">-Location</span></span>
<span data-ttu-id="b7c22-123">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="b7c22-123">Location of the network watcher.</span></span>

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

### <span data-ttu-id="b7c22-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b7c22-124">-Name</span></span>
<span data-ttu-id="b7c22-125">Nazwa monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="b7c22-125">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7c22-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b7c22-126">-NetworkWatcher</span></span>
<span data-ttu-id="b7c22-127">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="b7c22-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="b7c22-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="b7c22-128">-NetworkWatcherName</span></span>
<span data-ttu-id="b7c22-129">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="b7c22-129">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7c22-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7c22-130">-PassThru</span></span>
<span data-ttu-id="b7c22-131">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="b7c22-131">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="b7c22-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7c22-132">-ResourceGroupName</span></span>
<span data-ttu-id="b7c22-133">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="b7c22-133">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7c22-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7c22-134">-ResourceId</span></span>
<span data-ttu-id="b7c22-135">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="b7c22-135">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7c22-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b7c22-136">-Confirm</span></span>
<span data-ttu-id="b7c22-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7c22-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7c22-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7c22-138">-WhatIf</span></span>
<span data-ttu-id="b7c22-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7c22-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7c22-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b7c22-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7c22-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7c22-141">CommonParameters</span></span>
<span data-ttu-id="b7c22-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7c22-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7c22-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7c22-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7c22-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b7c22-144">INPUTS</span></span>

### <span data-ttu-id="b7c22-145">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b7c22-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="b7c22-146">System. String</span><span class="sxs-lookup"><span data-stu-id="b7c22-146">System.String</span></span>

### <span data-ttu-id="b7c22-147">Microsoft. Azure. Commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="b7c22-147">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="b7c22-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b7c22-148">OUTPUTS</span></span>

### <span data-ttu-id="b7c22-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b7c22-149">System.Boolean</span></span>

## <span data-ttu-id="b7c22-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b7c22-150">NOTES</span></span>
<span data-ttu-id="b7c22-151">Słowa kluczowe: Azure, azurerm, ARM, zasób, łączność, zarządzanie, Menedżer, Sieć, Sieć, obserwator sieci, monitor połączenia</span><span class="sxs-lookup"><span data-stu-id="b7c22-151">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="b7c22-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b7c22-152">RELATED LINKS</span></span>

[<span data-ttu-id="b7c22-153">Nowe — AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b7c22-153">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="b7c22-154">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b7c22-154">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="b7c22-155">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b7c22-155">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="b7c22-156">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="b7c22-156">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="b7c22-157">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="b7c22-157">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="b7c22-158">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="b7c22-158">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="b7c22-159">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="b7c22-159">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="b7c22-160">Nowe — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b7c22-160">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b7c22-161">Nowe — AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="b7c22-161">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="b7c22-162">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b7c22-162">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b7c22-163">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b7c22-163">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b7c22-164">Zatrzymaj — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b7c22-164">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b7c22-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b7c22-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b7c22-166">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="b7c22-166">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="b7c22-167">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b7c22-167">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b7c22-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b7c22-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b7c22-169">Zatrzymaj — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b7c22-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b7c22-170">Nowe — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b7c22-170">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b7c22-171">Nowe — AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7c22-171">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="b7c22-172">Test — AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="b7c22-172">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="b7c22-173">Test — AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="b7c22-173">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="b7c22-174">Start — AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="b7c22-174">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="b7c22-175">Start — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b7c22-175">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b7c22-176">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="b7c22-176">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="b7c22-177">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="b7c22-177">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="b7c22-178">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="b7c22-178">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="b7c22-179">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="b7c22-179">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
