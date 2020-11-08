---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 8a5f911529a4fc6f1ceb4e242b0e751e5f1a528f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053028"
---
# <span data-ttu-id="9c406-101">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="9c406-101">Remove-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="9c406-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9c406-102">SYNOPSIS</span></span>
<span data-ttu-id="9c406-103">Usuwa określony zasób dziennika przepływu.</span><span class="sxs-lookup"><span data-stu-id="9c406-103">Deletes the specified flow log resource.</span></span>

## <span data-ttu-id="9c406-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9c406-104">SYNTAX</span></span>

### <span data-ttu-id="9c406-105">SetByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9c406-105">SetByName (Default)</span></span>
```
Remove-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c406-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9c406-106">SetByResource</span></span>
```
Remove-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c406-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="9c406-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherFlowLog -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c406-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9c406-108">SetByResourceId</span></span>
```
Remove-AzNetworkWatcherFlowLog -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c406-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="9c406-109">SetByInputObject</span></span>
```
Remove-AzNetworkWatcherFlowLog -InputObject <PSFlowLogResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c406-110">Opis</span><span class="sxs-lookup"><span data-stu-id="9c406-110">DESCRIPTION</span></span>
<span data-ttu-id="9c406-111">Usuwa określony zasób dziennika przepływu.</span><span class="sxs-lookup"><span data-stu-id="9c406-111">Deletes the specified flow log resource.</span></span>

## <span data-ttu-id="9c406-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9c406-112">EXAMPLES</span></span>

### <span data-ttu-id="9c406-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9c406-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkWatcherFlowLog -Location eastus -Name pstest
```

## <span data-ttu-id="9c406-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9c406-114">PARAMETERS</span></span>

### <span data-ttu-id="9c406-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9c406-115">-AsJob</span></span>
<span data-ttu-id="9c406-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9c406-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9c406-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c406-117">-DefaultProfile</span></span>
<span data-ttu-id="9c406-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9c406-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c406-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9c406-119">-InputObject</span></span>
<span data-ttu-id="9c406-120">Obiekt dziennika przepływu.</span><span class="sxs-lookup"><span data-stu-id="9c406-120">Flow log object.</span></span>

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

### <span data-ttu-id="9c406-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="9c406-121">-Location</span></span>
<span data-ttu-id="9c406-122">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="9c406-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="9c406-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9c406-123">-Name</span></span>
<span data-ttu-id="9c406-124">Nazwa dziennika przepływu.</span><span class="sxs-lookup"><span data-stu-id="9c406-124">The flow log name.</span></span>

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

### <span data-ttu-id="9c406-125">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9c406-125">-NetworkWatcher</span></span>
<span data-ttu-id="9c406-126">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="9c406-126">The network watcher resource.</span></span>

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

### <span data-ttu-id="9c406-127">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="9c406-127">-NetworkWatcherName</span></span>
<span data-ttu-id="9c406-128">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="9c406-128">The name of network watcher.</span></span>

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

### <span data-ttu-id="9c406-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c406-129">-PassThru</span></span>
<span data-ttu-id="9c406-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="9c406-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="9c406-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c406-131">-ResourceGroupName</span></span>
<span data-ttu-id="9c406-132">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="9c406-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="9c406-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c406-133">-ResourceId</span></span>
<span data-ttu-id="9c406-134">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="9c406-134">Resource ID.</span></span>

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

### <span data-ttu-id="9c406-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9c406-135">-Confirm</span></span>
<span data-ttu-id="9c406-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c406-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c406-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c406-137">-WhatIf</span></span>
<span data-ttu-id="9c406-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c406-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c406-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9c406-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c406-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c406-140">CommonParameters</span></span>
<span data-ttu-id="9c406-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c406-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c406-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c406-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c406-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9c406-143">INPUTS</span></span>

### <span data-ttu-id="9c406-144">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9c406-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="9c406-145">System. String</span><span class="sxs-lookup"><span data-stu-id="9c406-145">System.String</span></span>

### <span data-ttu-id="9c406-146">Microsoft. Azure. Commands. Network. models. PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="9c406-146">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="9c406-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9c406-147">OUTPUTS</span></span>

### <span data-ttu-id="9c406-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9c406-148">System.Boolean</span></span>

## <span data-ttu-id="9c406-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9c406-149">NOTES</span></span>

## <span data-ttu-id="9c406-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9c406-150">RELATED LINKS</span></span>

[<span data-ttu-id="9c406-151">Nowe — AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9c406-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="9c406-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9c406-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="9c406-153">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9c406-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="9c406-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="9c406-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="9c406-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="9c406-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="9c406-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="9c406-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="9c406-157">Start — AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="9c406-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="9c406-158">Nowe — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9c406-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9c406-159">Nowe — AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="9c406-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="9c406-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9c406-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9c406-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9c406-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9c406-162">Zatrzymaj — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9c406-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9c406-163">Nowe — AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="9c406-163">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="9c406-164">Test — AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="9c406-164">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="9c406-165">Test — AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="9c406-165">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="9c406-166">Zatrzymaj — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9c406-166">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9c406-167">Start — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9c406-167">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9c406-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9c406-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9c406-169">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="9c406-169">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="9c406-170">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9c406-170">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9c406-171">Nowe — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9c406-171">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9c406-172">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="9c406-172">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="9c406-173">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="9c406-173">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="9c406-174">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="9c406-174">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="9c406-175">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="9c406-175">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="9c406-176">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="9c406-176">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="9c406-177">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9c406-177">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="9c406-178">Nowe — AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="9c406-178">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog)

[<span data-ttu-id="9c406-179">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="9c406-179">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog)

[<span data-ttu-id="9c406-180">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="9c406-180">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog)