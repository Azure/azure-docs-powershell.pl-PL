---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: dcdd4ef2fd6ca3481d9bb3f8333174307be7e3f6
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100404087"
---
# <span data-ttu-id="7362a-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="7362a-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="7362a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7362a-102">SYNOPSIS</span></span>
<span data-ttu-id="7362a-103">Pobiera wynik względnego opóźnienia dla dostawców usług internetowych z określonej lokalizacji do regionów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7362a-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="7362a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7362a-104">SYNTAX</span></span>

### <span data-ttu-id="7362a-105">SetByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="7362a-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <String[]>] [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7362a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7362a-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7362a-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7362a-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String> [-Provider <String[]>] [-Location <String[]>]
 -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7362a-108">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="7362a-108">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherLocation <String> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7362a-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="7362a-109">DESCRIPTION</span></span>
<span data-ttu-id="7362a-110">Ta Get-AzNetworkWatcherReachabilityReport uzyskuje wynik względnego opóźnienia dla dostawców usług internetowych z określonej lokalizacji do regionów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7362a-110">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="7362a-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7362a-111">EXAMPLES</span></span>

### <span data-ttu-id="7362a-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7362a-112">Example 1</span></span>
```
$nw = Get-AzNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher $nw -Location "West US" -Country "United States" -StartTime "2017-10-10" -EndTime "2017-10-12"

"aggregationLevel" : "Country",
"providerLocation" : {
    "country" : "United States"
},
"reachabilityReport" : [
    {
        "provider" : "Frontier Communications of America, Inc. - ASN 5650",
        "azureLocation": "West US",
        "latencies": [
            {
                "timeStamp": "2017-10-10T00:00:00Z",
                "score": 94
            },
            {
                "timeStamp": "2017-10-11T00:00:00Z",
                "score": 94
            },
            {
                "timeStamp": "2017-10-12T00:00:00Z",
                "score": 94    
            }
        ]  
    }
]
```

<span data-ttu-id="7362a-113">Pobiera względne opóźnienia do centrum danych Azure w Stanach Zjednoczonych w stanach zachód od 2017-10-10 do 2017-10-12 wewnątrz Stanów Zjednoczonych.</span><span class="sxs-lookup"><span data-stu-id="7362a-113">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

## <span data-ttu-id="7362a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7362a-114">PARAMETERS</span></span>

### <span data-ttu-id="7362a-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="7362a-115">-AsJob</span></span>
<span data-ttu-id="7362a-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7362a-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7362a-117">— Miasto</span><span class="sxs-lookup"><span data-stu-id="7362a-117">-City</span></span>
<span data-ttu-id="7362a-118">Nazwa miasta.</span><span class="sxs-lookup"><span data-stu-id="7362a-118">The name of the city.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7362a-119">— Kraj</span><span class="sxs-lookup"><span data-stu-id="7362a-119">-Country</span></span>
<span data-ttu-id="7362a-120">Nazwa kraju.</span><span class="sxs-lookup"><span data-stu-id="7362a-120">The name of the country.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7362a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7362a-121">-DefaultProfile</span></span>
<span data-ttu-id="7362a-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7362a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7362a-123">- EndTime</span><span class="sxs-lookup"><span data-stu-id="7362a-123">-EndTime</span></span>
<span data-ttu-id="7362a-124">Czas zakończenia raportu o osiągalności platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7362a-124">The end time for the Azure reachability report.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7362a-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="7362a-125">-Location</span></span>
<span data-ttu-id="7362a-126">Opcjonalne regiony platformy Azure, do których ma być objęte zapytaniem.</span><span class="sxs-lookup"><span data-stu-id="7362a-126">Optional Azure regions to scope the query to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7362a-127">— NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7362a-127">-NetworkWatcher</span></span>
<span data-ttu-id="7362a-128">Zasób obserwowania sieci</span><span class="sxs-lookup"><span data-stu-id="7362a-128">The network watcher resource</span></span>

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

### <span data-ttu-id="7362a-129">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="7362a-129">-NetworkWatcherLocation</span></span>
<span data-ttu-id="7362a-130">Lokalizacja czujki sieci.</span><span class="sxs-lookup"><span data-stu-id="7362a-130">Location of the network watcher.</span></span>

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

### <span data-ttu-id="7362a-131">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="7362a-131">-NetworkWatcherName</span></span>
<span data-ttu-id="7362a-132">Nazwa osoby oglądacej sieć.</span><span class="sxs-lookup"><span data-stu-id="7362a-132">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: ResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7362a-133">— Dostawca</span><span class="sxs-lookup"><span data-stu-id="7362a-133">-Provider</span></span>
<span data-ttu-id="7362a-134">Lista dostawców usług internetowych.</span><span class="sxs-lookup"><span data-stu-id="7362a-134">List of Internet service providers.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7362a-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7362a-135">-ResourceGroupName</span></span>
<span data-ttu-id="7362a-136">Nazwa grupy zasobów obserwowanych sieci.</span><span class="sxs-lookup"><span data-stu-id="7362a-136">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="7362a-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7362a-137">-ResourceId</span></span>
<span data-ttu-id="7362a-138">Identyfikator zasobu czujki sieciowej.</span><span class="sxs-lookup"><span data-stu-id="7362a-138">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="7362a-139">— StartTime</span><span class="sxs-lookup"><span data-stu-id="7362a-139">-StartTime</span></span>
<span data-ttu-id="7362a-140">Godzina rozpoczęcia raportu o osiągalności platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7362a-140">The start time for the Azure reachability report.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7362a-141">— województwo</span><span class="sxs-lookup"><span data-stu-id="7362a-141">-State</span></span>
<span data-ttu-id="7362a-142">Nazwa województwa.</span><span class="sxs-lookup"><span data-stu-id="7362a-142">The name of the state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7362a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7362a-143">CommonParameters</span></span>
<span data-ttu-id="7362a-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7362a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7362a-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7362a-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7362a-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7362a-146">INPUTS</span></span>

### <span data-ttu-id="7362a-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7362a-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="7362a-148">System.String</span><span class="sxs-lookup"><span data-stu-id="7362a-148">System.String</span></span>

## <span data-ttu-id="7362a-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7362a-149">OUTPUTS</span></span>

### <span data-ttu-id="7362a-150">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="7362a-150">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="7362a-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7362a-151">NOTES</span></span>
<span data-ttu-id="7362a-152">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span><span class="sxs-lookup"><span data-stu-id="7362a-152">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="7362a-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7362a-153">RELATED LINKS</span></span>

[<span data-ttu-id="7362a-154">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7362a-154">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="7362a-155">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7362a-155">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="7362a-156">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7362a-156">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="7362a-157">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="7362a-157">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="7362a-158">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="7362a-158">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="7362a-159">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="7362a-159">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="7362a-160">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="7362a-160">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="7362a-161">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7362a-161">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7362a-162">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="7362a-162">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="7362a-163">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7362a-163">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7362a-164">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7362a-164">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7362a-165">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7362a-165">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7362a-166">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="7362a-166">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="7362a-167">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="7362a-167">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="7362a-168">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="7362a-168">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="7362a-169">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7362a-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7362a-170">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7362a-170">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7362a-171">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7362a-171">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7362a-172">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="7362a-172">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="7362a-173">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7362a-173">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7362a-174">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7362a-174">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7362a-175">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="7362a-175">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="7362a-176">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="7362a-176">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="7362a-177">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="7362a-177">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="7362a-178">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="7362a-178">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="7362a-179">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="7362a-179">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="7362a-180">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7362a-180">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
