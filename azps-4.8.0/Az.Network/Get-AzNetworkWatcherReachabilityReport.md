---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: f29ab593ffac847ec6b089efdc39bc594ad1d785
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412371"
---
# <span data-ttu-id="83d46-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="83d46-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="83d46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83d46-102">SYNOPSIS</span></span>
<span data-ttu-id="83d46-103">Pobiera wynik względnego opóźnienia dla dostawców usług internetowych z określonej lokalizacji do regionów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="83d46-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="83d46-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="83d46-104">SYNTAX</span></span>

### <span data-ttu-id="83d46-105">SetByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="83d46-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <String[]>] [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83d46-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="83d46-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83d46-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="83d46-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String> [-Provider <String[]>] [-Location <String[]>]
 -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83d46-108">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="83d46-108">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherLocation <String> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83d46-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="83d46-109">DESCRIPTION</span></span>
<span data-ttu-id="83d46-110">Wyniki Get-AzNetworkWatcherReachabilityReport uzyskać wynik względnego opóźnienia dla dostawców usług internetowych z określonej lokalizacji do regionów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="83d46-110">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="83d46-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="83d46-111">EXAMPLES</span></span>

### <span data-ttu-id="83d46-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="83d46-112">Example 1</span></span>
```powershell
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

<span data-ttu-id="83d46-113">Pobiera względne opóźnienia do centrum danych Azure w Stanach Zjednoczonych w stanach zachód od 2017-10-10 do 2017-10-12 wewnątrz Stanów Zjednoczonych.</span><span class="sxs-lookup"><span data-stu-id="83d46-113">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

### <span data-ttu-id="83d46-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="83d46-114">Example 2</span></span>

<span data-ttu-id="83d46-115">Pobiera wynik względnego opóźnienia dla dostawców usług internetowych z określonej lokalizacji do regionów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="83d46-115">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span> <span data-ttu-id="83d46-116">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="83d46-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNetworkWatcherReachabilityReport -Country 'United States' -EndTime '2017-10-12' -Location 'West US' -NetworkWatcherName nw1 -ResourceGroupName myresourcegroup -StartTime '2017-10-10' -State 'washington'
```

## <span data-ttu-id="83d46-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83d46-117">PARAMETERS</span></span>

### <span data-ttu-id="83d46-118">— AsJob</span><span class="sxs-lookup"><span data-stu-id="83d46-118">-AsJob</span></span>
<span data-ttu-id="83d46-119">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="83d46-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="83d46-120">— Miasto</span><span class="sxs-lookup"><span data-stu-id="83d46-120">-City</span></span>
<span data-ttu-id="83d46-121">Nazwa miasta.</span><span class="sxs-lookup"><span data-stu-id="83d46-121">The name of the city.</span></span>

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

### <span data-ttu-id="83d46-122">— Kraj</span><span class="sxs-lookup"><span data-stu-id="83d46-122">-Country</span></span>
<span data-ttu-id="83d46-123">Nazwa kraju.</span><span class="sxs-lookup"><span data-stu-id="83d46-123">The name of the country.</span></span>

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

### <span data-ttu-id="83d46-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83d46-124">-DefaultProfile</span></span>
<span data-ttu-id="83d46-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="83d46-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83d46-126">- EndTime</span><span class="sxs-lookup"><span data-stu-id="83d46-126">-EndTime</span></span>
<span data-ttu-id="83d46-127">Czas zakończenia raportu o osiągalności platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="83d46-127">The end time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="83d46-128">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="83d46-128">-Location</span></span>
<span data-ttu-id="83d46-129">Opcjonalne regiony platformy Azure, do których ma być objęte zapytaniem.</span><span class="sxs-lookup"><span data-stu-id="83d46-129">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="83d46-130">- NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="83d46-130">-NetworkWatcher</span></span>
<span data-ttu-id="83d46-131">Zasób obserwowania sieci</span><span class="sxs-lookup"><span data-stu-id="83d46-131">The network watcher resource</span></span>

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

### <span data-ttu-id="83d46-132">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="83d46-132">-NetworkWatcherLocation</span></span>
<span data-ttu-id="83d46-133">Lokalizacja czujki sieci.</span><span class="sxs-lookup"><span data-stu-id="83d46-133">Location of the network watcher.</span></span>

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

### <span data-ttu-id="83d46-134">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="83d46-134">-NetworkWatcherName</span></span>
<span data-ttu-id="83d46-135">Nazwa osoby oglądacej sieć.</span><span class="sxs-lookup"><span data-stu-id="83d46-135">The name of network watcher.</span></span>

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

### <span data-ttu-id="83d46-136">— Dostawca</span><span class="sxs-lookup"><span data-stu-id="83d46-136">-Provider</span></span>
<span data-ttu-id="83d46-137">Lista dostawców usług internetowych.</span><span class="sxs-lookup"><span data-stu-id="83d46-137">List of Internet service providers.</span></span>

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

### <span data-ttu-id="83d46-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83d46-138">-ResourceGroupName</span></span>
<span data-ttu-id="83d46-139">Nazwa grupy zasobów obserwowanych sieci.</span><span class="sxs-lookup"><span data-stu-id="83d46-139">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="83d46-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="83d46-140">-ResourceId</span></span>
<span data-ttu-id="83d46-141">Identyfikator zasobu czujki sieciowej.</span><span class="sxs-lookup"><span data-stu-id="83d46-141">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="83d46-142">— StartTime</span><span class="sxs-lookup"><span data-stu-id="83d46-142">-StartTime</span></span>
<span data-ttu-id="83d46-143">Godzina rozpoczęcia raportu o osiągalności platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="83d46-143">The start time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="83d46-144">— województwo</span><span class="sxs-lookup"><span data-stu-id="83d46-144">-State</span></span>
<span data-ttu-id="83d46-145">Nazwa województwa.</span><span class="sxs-lookup"><span data-stu-id="83d46-145">The name of the state.</span></span>

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

### <span data-ttu-id="83d46-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83d46-146">CommonParameters</span></span>
<span data-ttu-id="83d46-147">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83d46-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83d46-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="83d46-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83d46-149">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="83d46-149">INPUTS</span></span>

### <span data-ttu-id="83d46-150">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="83d46-150">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="83d46-151">System.String</span><span class="sxs-lookup"><span data-stu-id="83d46-151">System.String</span></span>

## <span data-ttu-id="83d46-152">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="83d46-152">OUTPUTS</span></span>

### <span data-ttu-id="83d46-153">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="83d46-153">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="83d46-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="83d46-154">NOTES</span></span>
<span data-ttu-id="83d46-155">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span><span class="sxs-lookup"><span data-stu-id="83d46-155">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="83d46-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="83d46-156">RELATED LINKS</span></span>

[<span data-ttu-id="83d46-157">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="83d46-157">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="83d46-158">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="83d46-158">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="83d46-159">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="83d46-159">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="83d46-160">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="83d46-160">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="83d46-161">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="83d46-161">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="83d46-162">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="83d46-162">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="83d46-163">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="83d46-163">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="83d46-164">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="83d46-164">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="83d46-165">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="83d46-165">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="83d46-166">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="83d46-166">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="83d46-167">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="83d46-167">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="83d46-168">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="83d46-168">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="83d46-169">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="83d46-169">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="83d46-170">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="83d46-170">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="83d46-171">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="83d46-171">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="83d46-172">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="83d46-172">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="83d46-173">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="83d46-173">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="83d46-174">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="83d46-174">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="83d46-175">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="83d46-175">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="83d46-176">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="83d46-176">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="83d46-177">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="83d46-177">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="83d46-178">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="83d46-178">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="83d46-179">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="83d46-179">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="83d46-180">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="83d46-180">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="83d46-181">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="83d46-181">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="83d46-182">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="83d46-182">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="83d46-183">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="83d46-183">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
