---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 83d7da65ad8c525d4c37ab1b5f78eb72bf1d9f49
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189443"
---
# <span data-ttu-id="46b97-101">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="46b97-101">Start-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="46b97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46b97-102">SYNOPSIS</span></span>
<span data-ttu-id="46b97-103">Uruchamianie monitora połączenia</span><span class="sxs-lookup"><span data-stu-id="46b97-103">Start a connection monitor</span></span>

## <span data-ttu-id="46b97-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="46b97-104">SYNTAX</span></span>

### <span data-ttu-id="46b97-105">SetByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="46b97-105">SetByName (Default)</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46b97-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="46b97-106">SetByResource</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46b97-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="46b97-107">SetByLocation</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46b97-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="46b97-108">SetByResourceId</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46b97-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="46b97-109">SetByInputObject</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46b97-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="46b97-110">DESCRIPTION</span></span>
<span data-ttu-id="46b97-111">Polecenie Start-AzNetworkWatcherConnectionMonitor uruchamia określony monitor połączenia.</span><span class="sxs-lookup"><span data-stu-id="46b97-111">The Start-AzNetworkWatcherConnectionMonitor cmdlet starts the specified connection monitor.</span></span>

## <span data-ttu-id="46b97-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="46b97-112">EXAMPLES</span></span>

### <span data-ttu-id="46b97-113">Przykład 1. Uruchamianie monitora połączenia</span><span class="sxs-lookup"><span data-stu-id="46b97-113">Example 1: Start a connection monitor</span></span>
```
PS C:\> Start-AzNetworkWatcherConnectionMonitor -NetworkWatcherName NetworkWatcher_centraluseuap -ResourceGroupName NetworkWatcherRG -Name cm
```

<span data-ttu-id="46b97-114">W tym przykładzie uruchamiamy monitor połączenia określony za pomocą nazwy i czujki sieciowej</span><span class="sxs-lookup"><span data-stu-id="46b97-114">In this example we start connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="46b97-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46b97-115">PARAMETERS</span></span>

### <span data-ttu-id="46b97-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="46b97-116">-AsJob</span></span>
<span data-ttu-id="46b97-117">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="46b97-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="46b97-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46b97-118">-DefaultProfile</span></span>
<span data-ttu-id="46b97-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="46b97-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46b97-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46b97-120">-InputObject</span></span>
<span data-ttu-id="46b97-121">Obiekt monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="46b97-121">Connection monitor object.</span></span>

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

### <span data-ttu-id="46b97-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="46b97-122">-Location</span></span>
<span data-ttu-id="46b97-123">Lokalizacja czujki sieci.</span><span class="sxs-lookup"><span data-stu-id="46b97-123">Location of the network watcher.</span></span>

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

### <span data-ttu-id="46b97-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="46b97-124">-Name</span></span>
<span data-ttu-id="46b97-125">Nazwa monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="46b97-125">The connection monitor name.</span></span>

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

### <span data-ttu-id="46b97-126">- NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="46b97-126">-NetworkWatcher</span></span>
<span data-ttu-id="46b97-127">Zasób obserwowania sieci.</span><span class="sxs-lookup"><span data-stu-id="46b97-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="46b97-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="46b97-128">-NetworkWatcherName</span></span>
<span data-ttu-id="46b97-129">Nazwa osoby oglądacej sieć.</span><span class="sxs-lookup"><span data-stu-id="46b97-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="46b97-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="46b97-130">-PassThru</span></span>
<span data-ttu-id="46b97-131">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="46b97-131">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="46b97-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46b97-132">-ResourceGroupName</span></span>
<span data-ttu-id="46b97-133">Nazwa grupy zasobów obserwowanych sieci.</span><span class="sxs-lookup"><span data-stu-id="46b97-133">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="46b97-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46b97-134">-ResourceId</span></span>
<span data-ttu-id="46b97-135">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="46b97-135">Resource ID.</span></span>

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

### <span data-ttu-id="46b97-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="46b97-136">-Confirm</span></span>
<span data-ttu-id="46b97-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="46b97-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46b97-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46b97-138">-WhatIf</span></span>
<span data-ttu-id="46b97-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46b97-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46b97-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="46b97-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46b97-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46b97-141">CommonParameters</span></span>
<span data-ttu-id="46b97-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46b97-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46b97-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46b97-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46b97-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="46b97-144">INPUTS</span></span>

### <span data-ttu-id="46b97-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="46b97-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="46b97-146">System.String</span><span class="sxs-lookup"><span data-stu-id="46b97-146">System.String</span></span>

### <span data-ttu-id="46b97-147">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="46b97-147">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="46b97-148">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="46b97-148">OUTPUTS</span></span>

### <span data-ttu-id="46b97-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="46b97-149">System.Boolean</span></span>

## <span data-ttu-id="46b97-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="46b97-150">NOTES</span></span>
<span data-ttu-id="46b97-151">Słowa kluczowe: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span><span class="sxs-lookup"><span data-stu-id="46b97-151">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="46b97-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="46b97-152">RELATED LINKS</span></span>

[<span data-ttu-id="46b97-153">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="46b97-153">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="46b97-154">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="46b97-154">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="46b97-155">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="46b97-155">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="46b97-156">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="46b97-156">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="46b97-157">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="46b97-157">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="46b97-158">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="46b97-158">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="46b97-159">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="46b97-159">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="46b97-160">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="46b97-160">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="46b97-161">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="46b97-161">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="46b97-162">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="46b97-162">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="46b97-163">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="46b97-163">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="46b97-164">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="46b97-164">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="46b97-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="46b97-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="46b97-166">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="46b97-166">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="46b97-167">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="46b97-167">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="46b97-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="46b97-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="46b97-169">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="46b97-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="46b97-170">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="46b97-170">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="46b97-171">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="46b97-171">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="46b97-172">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="46b97-172">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="46b97-173">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="46b97-173">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="46b97-174">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="46b97-174">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="46b97-175">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="46b97-175">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="46b97-176">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="46b97-176">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="46b97-177">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="46b97-177">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="46b97-178">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="46b97-178">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="46b97-179">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="46b97-179">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
