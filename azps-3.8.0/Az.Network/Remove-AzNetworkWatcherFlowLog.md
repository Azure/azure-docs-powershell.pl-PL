---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 5c8532502e4e74b94a9d0c1e252c8d1cea9ddad8
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398600"
---
# <span data-ttu-id="69b1d-101">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="69b1d-101">Remove-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="69b1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69b1d-102">SYNOPSIS</span></span>
<span data-ttu-id="69b1d-103">Usuwa określony zasób dziennika przepływów.</span><span class="sxs-lookup"><span data-stu-id="69b1d-103">Deletes the specified flow log resource.</span></span>

## <span data-ttu-id="69b1d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="69b1d-104">SYNTAX</span></span>

### <span data-ttu-id="69b1d-105">SetByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="69b1d-105">SetByName (Default)</span></span>
```
Remove-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69b1d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="69b1d-106">SetByResource</span></span>
```
Remove-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69b1d-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="69b1d-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherFlowLog -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69b1d-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="69b1d-108">SetByResourceId</span></span>
```
Remove-AzNetworkWatcherFlowLog -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69b1d-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="69b1d-109">SetByInputObject</span></span>
```
Remove-AzNetworkWatcherFlowLog -InputObject <PSFlowLogResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69b1d-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="69b1d-110">DESCRIPTION</span></span>
<span data-ttu-id="69b1d-111">Usuwa określony zasób dziennika przepływów.</span><span class="sxs-lookup"><span data-stu-id="69b1d-111">Deletes the specified flow log resource.</span></span>

## <span data-ttu-id="69b1d-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="69b1d-112">EXAMPLES</span></span>

### <span data-ttu-id="69b1d-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="69b1d-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkWatcherFlowLog -Location eastus -Name pstest
```

## <span data-ttu-id="69b1d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69b1d-114">PARAMETERS</span></span>

### <span data-ttu-id="69b1d-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="69b1d-115">-AsJob</span></span>
<span data-ttu-id="69b1d-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="69b1d-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69b1d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69b1d-117">-DefaultProfile</span></span>
<span data-ttu-id="69b1d-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="69b1d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69b1d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69b1d-119">-InputObject</span></span>
<span data-ttu-id="69b1d-120">Obiekt dziennika przepływu.</span><span class="sxs-lookup"><span data-stu-id="69b1d-120">Flow log object.</span></span>

```yaml
Type: PSFlowLogResource
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69b1d-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="69b1d-121">-Location</span></span>
<span data-ttu-id="69b1d-122">Lokalizacja czujki sieci.</span><span class="sxs-lookup"><span data-stu-id="69b1d-122">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69b1d-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="69b1d-123">-Name</span></span>
<span data-ttu-id="69b1d-124">Nazwa dziennika przepływu.</span><span class="sxs-lookup"><span data-stu-id="69b1d-124">The flow log name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: FlowLogName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69b1d-125">— NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="69b1d-125">-NetworkWatcher</span></span>
<span data-ttu-id="69b1d-126">Zasób obserwowania sieci.</span><span class="sxs-lookup"><span data-stu-id="69b1d-126">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69b1d-127">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="69b1d-127">-NetworkWatcherName</span></span>
<span data-ttu-id="69b1d-128">Nazwa osoby oglądacej sieć.</span><span class="sxs-lookup"><span data-stu-id="69b1d-128">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69b1d-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69b1d-129">-PassThru</span></span>
<span data-ttu-id="69b1d-130">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="69b1d-130">{{ Fill PassThru Description }}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69b1d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69b1d-131">-ResourceGroupName</span></span>
<span data-ttu-id="69b1d-132">Nazwa grupy zasobów obserwowanych sieci.</span><span class="sxs-lookup"><span data-stu-id="69b1d-132">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69b1d-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69b1d-133">-ResourceId</span></span>
<span data-ttu-id="69b1d-134">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="69b1d-134">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69b1d-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="69b1d-135">-Confirm</span></span>
<span data-ttu-id="69b1d-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="69b1d-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69b1d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69b1d-137">-WhatIf</span></span>
<span data-ttu-id="69b1d-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69b1d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69b1d-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="69b1d-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69b1d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69b1d-140">CommonParameters</span></span>
<span data-ttu-id="69b1d-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69b1d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69b1d-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="69b1d-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69b1d-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69b1d-143">INPUTS</span></span>

### <span data-ttu-id="69b1d-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="69b1d-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="69b1d-145">System.String</span><span class="sxs-lookup"><span data-stu-id="69b1d-145">System.String</span></span>

### <span data-ttu-id="69b1d-146">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="69b1d-146">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="69b1d-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="69b1d-147">OUTPUTS</span></span>

### <span data-ttu-id="69b1d-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="69b1d-148">System.Boolean</span></span>

## <span data-ttu-id="69b1d-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="69b1d-149">NOTES</span></span>

## <span data-ttu-id="69b1d-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="69b1d-150">RELATED LINKS</span></span>

[<span data-ttu-id="69b1d-151">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="69b1d-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="69b1d-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="69b1d-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="69b1d-153">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="69b1d-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="69b1d-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="69b1d-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="69b1d-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="69b1d-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="69b1d-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="69b1d-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="69b1d-157">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="69b1d-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="69b1d-158">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="69b1d-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="69b1d-159">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="69b1d-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="69b1d-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="69b1d-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="69b1d-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="69b1d-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="69b1d-162">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="69b1d-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="69b1d-163">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="69b1d-163">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="69b1d-164">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="69b1d-164">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="69b1d-165">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="69b1d-165">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="69b1d-166">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="69b1d-166">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="69b1d-167">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="69b1d-167">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="69b1d-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="69b1d-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="69b1d-169">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="69b1d-169">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="69b1d-170">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="69b1d-170">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="69b1d-171">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="69b1d-171">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="69b1d-172">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="69b1d-172">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="69b1d-173">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="69b1d-173">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="69b1d-174">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="69b1d-174">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="69b1d-175">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="69b1d-175">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="69b1d-176">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="69b1d-176">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="69b1d-177">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="69b1d-177">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="69b1d-178">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="69b1d-178">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="69b1d-179">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="69b1d-179">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="69b1d-180">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="69b1d-180">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog.md)
