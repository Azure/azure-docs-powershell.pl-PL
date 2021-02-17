---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 1c06b6605cfa7d4b7d402dec2fcb0e33136b125c
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411028"
---
# <span data-ttu-id="b4b40-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="b4b40-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="b4b40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4b40-102">SYNOPSIS</span></span>
<span data-ttu-id="b4b40-103">Pobiera wynik względnego opóźnienia dla dostawców usług internetowych z określonej lokalizacji do regionów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b4b40-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="b4b40-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b4b40-104">SYNTAX</span></span>

### <span data-ttu-id="b4b40-105">SetByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="b4b40-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <String[]>] [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4b40-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b4b40-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4b40-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b4b40-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String> [-Provider <String[]>] [-Location <String[]>]
 -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4b40-108">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="b4b40-108">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherLocation <String> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4b40-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="b4b40-109">DESCRIPTION</span></span>
<span data-ttu-id="b4b40-110">Wyniki Get-AzNetworkWatcherReachabilityReport uzyskać wynik względnego opóźnienia dla dostawców usług internetowych z określonej lokalizacji do regionów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b4b40-110">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="b4b40-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b4b40-111">EXAMPLES</span></span>

### <span data-ttu-id="b4b40-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b4b40-112">Example 1</span></span>
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

<span data-ttu-id="b4b40-113">Pobiera względne opóźnienia do centrum danych Azure w Stanach Zjednoczonych w stanach zachód od 2017-10-10 do 2017-10-12 wewnątrz Stanów Zjednoczonych.</span><span class="sxs-lookup"><span data-stu-id="b4b40-113">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

## <span data-ttu-id="b4b40-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4b40-114">PARAMETERS</span></span>

### <span data-ttu-id="b4b40-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="b4b40-115">-AsJob</span></span>
<span data-ttu-id="b4b40-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b4b40-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b4b40-117">— Miasto</span><span class="sxs-lookup"><span data-stu-id="b4b40-117">-City</span></span>
<span data-ttu-id="b4b40-118">Nazwa miasta.</span><span class="sxs-lookup"><span data-stu-id="b4b40-118">The name of the city.</span></span>

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

### <span data-ttu-id="b4b40-119">— Kraj</span><span class="sxs-lookup"><span data-stu-id="b4b40-119">-Country</span></span>
<span data-ttu-id="b4b40-120">Nazwa kraju.</span><span class="sxs-lookup"><span data-stu-id="b4b40-120">The name of the country.</span></span>

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

### <span data-ttu-id="b4b40-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4b40-121">-DefaultProfile</span></span>
<span data-ttu-id="b4b40-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b4b40-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4b40-123">- EndTime</span><span class="sxs-lookup"><span data-stu-id="b4b40-123">-EndTime</span></span>
<span data-ttu-id="b4b40-124">Czas zakończenia raportu o osiągalności platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b4b40-124">The end time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="b4b40-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b4b40-125">-Location</span></span>
<span data-ttu-id="b4b40-126">Opcjonalne regiony platformy Azure, do których ma być zwracane zapytanie.</span><span class="sxs-lookup"><span data-stu-id="b4b40-126">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="b4b40-127">— NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b4b40-127">-NetworkWatcher</span></span>
<span data-ttu-id="b4b40-128">Zasób obserwowania sieci</span><span class="sxs-lookup"><span data-stu-id="b4b40-128">The network watcher resource</span></span>

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

### <span data-ttu-id="b4b40-129">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="b4b40-129">-NetworkWatcherLocation</span></span>
<span data-ttu-id="b4b40-130">Lokalizacja czujki sieci.</span><span class="sxs-lookup"><span data-stu-id="b4b40-130">Location of the network watcher.</span></span>

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

### <span data-ttu-id="b4b40-131">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="b4b40-131">-NetworkWatcherName</span></span>
<span data-ttu-id="b4b40-132">Nazwa osoby oglądacej sieć.</span><span class="sxs-lookup"><span data-stu-id="b4b40-132">The name of network watcher.</span></span>

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

### <span data-ttu-id="b4b40-133">— Dostawca</span><span class="sxs-lookup"><span data-stu-id="b4b40-133">-Provider</span></span>
<span data-ttu-id="b4b40-134">Lista dostawców usług internetowych.</span><span class="sxs-lookup"><span data-stu-id="b4b40-134">List of Internet service providers.</span></span>

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

### <span data-ttu-id="b4b40-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4b40-135">-ResourceGroupName</span></span>
<span data-ttu-id="b4b40-136">Nazwa grupy zasobów obserwowanych sieci.</span><span class="sxs-lookup"><span data-stu-id="b4b40-136">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="b4b40-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4b40-137">-ResourceId</span></span>
<span data-ttu-id="b4b40-138">Identyfikator zasobu czujki sieciowej.</span><span class="sxs-lookup"><span data-stu-id="b4b40-138">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="b4b40-139">— StartTime</span><span class="sxs-lookup"><span data-stu-id="b4b40-139">-StartTime</span></span>
<span data-ttu-id="b4b40-140">Godzina rozpoczęcia raportu o osiągalności platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b4b40-140">The start time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="b4b40-141">— województwo</span><span class="sxs-lookup"><span data-stu-id="b4b40-141">-State</span></span>
<span data-ttu-id="b4b40-142">Nazwa województwa.</span><span class="sxs-lookup"><span data-stu-id="b4b40-142">The name of the state.</span></span>

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

### <span data-ttu-id="b4b40-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4b40-143">CommonParameters</span></span>
<span data-ttu-id="b4b40-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4b40-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4b40-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b4b40-145">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4b40-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4b40-146">INPUTS</span></span>

### <span data-ttu-id="b4b40-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b4b40-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="b4b40-148">System.String</span><span class="sxs-lookup"><span data-stu-id="b4b40-148">System.String</span></span>

## <span data-ttu-id="b4b40-149">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4b40-149">OUTPUTS</span></span>

### <span data-ttu-id="b4b40-150">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="b4b40-150">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="b4b40-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b4b40-151">NOTES</span></span>
<span data-ttu-id="b4b40-152">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span><span class="sxs-lookup"><span data-stu-id="b4b40-152">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="b4b40-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b4b40-153">RELATED LINKS</span></span>

[<span data-ttu-id="b4b40-154">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b4b40-154">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="b4b40-155">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b4b40-155">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="b4b40-156">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b4b40-156">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="b4b40-157">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="b4b40-157">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="b4b40-158">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="b4b40-158">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="b4b40-159">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="b4b40-159">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="b4b40-160">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="b4b40-160">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="b4b40-161">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b4b40-161">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b4b40-162">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="b4b40-162">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="b4b40-163">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b4b40-163">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b4b40-164">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b4b40-164">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b4b40-165">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b4b40-165">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b4b40-166">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4b40-166">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="b4b40-167">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="b4b40-167">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="b4b40-168">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="b4b40-168">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="b4b40-169">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b4b40-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b4b40-170">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b4b40-170">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b4b40-171">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b4b40-171">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b4b40-172">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="b4b40-172">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="b4b40-173">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b4b40-173">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b4b40-174">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b4b40-174">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b4b40-175">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="b4b40-175">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="b4b40-176">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="b4b40-176">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="b4b40-177">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="b4b40-177">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="b4b40-178">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="b4b40-178">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="b4b40-179">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="b4b40-179">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="b4b40-180">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b4b40-180">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
