---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 3fe26c99dd92afb65105008524908a10dec02e0e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500654"
---
# <span data-ttu-id="747b2-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="747b2-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="747b2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="747b2-102">SYNOPSIS</span></span>
<span data-ttu-id="747b2-103">Pobiera względny wynik opóźnienia dla dostawców usług internetowych z określonej lokalizacji na regiony platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="747b2-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="747b2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="747b2-104">SYNTAX</span></span>

### <span data-ttu-id="747b2-105">SetByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="747b2-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <String[]>] [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="747b2-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="747b2-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="747b2-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="747b2-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String> [-Provider <String[]>] [-Location <String[]>]
 -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="747b2-108">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="747b2-108">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherLocation <String> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="747b2-109">Opis</span><span class="sxs-lookup"><span data-stu-id="747b2-109">DESCRIPTION</span></span>
<span data-ttu-id="747b2-110">Get-AzNetworkWatcherReachabilityReport pobiera względny wynik opóźnienia dla dostawców usług internetowych z określonej lokalizacji do regionów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="747b2-110">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="747b2-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="747b2-111">EXAMPLES</span></span>

### <span data-ttu-id="747b2-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="747b2-112">Example 1</span></span>
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

<span data-ttu-id="747b2-113">Pobiera względne opóźnienia w usłudze Azure Data Center w Stanach Zjednoczonych na zachód od 2017-10-10 do 2017-10-12 w stanie amerykańskim.</span><span class="sxs-lookup"><span data-stu-id="747b2-113">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

### <span data-ttu-id="747b2-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="747b2-114">Example 2</span></span>

<span data-ttu-id="747b2-115">Pobiera względny wynik opóźnienia dla dostawców usług internetowych z określonej lokalizacji na regiony platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="747b2-115">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span> <span data-ttu-id="747b2-116">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="747b2-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNetworkWatcherReachabilityReport -Country 'United States' -EndTime '2017-10-12' -Location 'West US' -NetworkWatcherName nw1 -ResourceGroupName myresourcegroup -StartTime '2017-10-10' -State 'washington'
```

## <span data-ttu-id="747b2-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="747b2-117">PARAMETERS</span></span>

### <span data-ttu-id="747b2-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="747b2-118">-AsJob</span></span>
<span data-ttu-id="747b2-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="747b2-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="747b2-120">-Miasto</span><span class="sxs-lookup"><span data-stu-id="747b2-120">-City</span></span>
<span data-ttu-id="747b2-121">Nazwa miasta.</span><span class="sxs-lookup"><span data-stu-id="747b2-121">The name of the city.</span></span>

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

### <span data-ttu-id="747b2-122">-Country</span><span class="sxs-lookup"><span data-stu-id="747b2-122">-Country</span></span>
<span data-ttu-id="747b2-123">Nazwa kraju.</span><span class="sxs-lookup"><span data-stu-id="747b2-123">The name of the country.</span></span>

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

### <span data-ttu-id="747b2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="747b2-124">-DefaultProfile</span></span>
<span data-ttu-id="747b2-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="747b2-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="747b2-126">-EndTime</span><span class="sxs-lookup"><span data-stu-id="747b2-126">-EndTime</span></span>
<span data-ttu-id="747b2-127">Godzina zakończenia dla raportu o nieobecności w usłudze Azure.</span><span class="sxs-lookup"><span data-stu-id="747b2-127">The end time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="747b2-128">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="747b2-128">-Location</span></span>
<span data-ttu-id="747b2-129">Opcjonalne regiony platformy Azure umożliwiające zakres kwerendy.</span><span class="sxs-lookup"><span data-stu-id="747b2-129">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="747b2-130">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="747b2-130">-NetworkWatcher</span></span>
<span data-ttu-id="747b2-131">Zasób obserwatora sieci</span><span class="sxs-lookup"><span data-stu-id="747b2-131">The network watcher resource</span></span>

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

### <span data-ttu-id="747b2-132">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="747b2-132">-NetworkWatcherLocation</span></span>
<span data-ttu-id="747b2-133">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="747b2-133">Location of the network watcher.</span></span>

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

### <span data-ttu-id="747b2-134">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="747b2-134">-NetworkWatcherName</span></span>
<span data-ttu-id="747b2-135">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="747b2-135">The name of network watcher.</span></span>

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

### <span data-ttu-id="747b2-136">-Provider</span><span class="sxs-lookup"><span data-stu-id="747b2-136">-Provider</span></span>
<span data-ttu-id="747b2-137">Lista dostawców usług internetowych.</span><span class="sxs-lookup"><span data-stu-id="747b2-137">List of Internet service providers.</span></span>

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

### <span data-ttu-id="747b2-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="747b2-138">-ResourceGroupName</span></span>
<span data-ttu-id="747b2-139">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="747b2-139">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="747b2-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="747b2-140">-ResourceId</span></span>
<span data-ttu-id="747b2-141">Identyfikator zasobu obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="747b2-141">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="747b2-142">-StartTime</span><span class="sxs-lookup"><span data-stu-id="747b2-142">-StartTime</span></span>
<span data-ttu-id="747b2-143">Godzina rozpoczęcia dla raportu o nieobecności w usłudze Azure.</span><span class="sxs-lookup"><span data-stu-id="747b2-143">The start time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="747b2-144">-State</span><span class="sxs-lookup"><span data-stu-id="747b2-144">-State</span></span>
<span data-ttu-id="747b2-145">Nazwa województwa.</span><span class="sxs-lookup"><span data-stu-id="747b2-145">The name of the state.</span></span>

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

### <span data-ttu-id="747b2-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="747b2-146">CommonParameters</span></span>
<span data-ttu-id="747b2-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="747b2-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="747b2-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="747b2-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="747b2-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="747b2-149">INPUTS</span></span>

### <span data-ttu-id="747b2-150">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="747b2-150">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="747b2-151">System. String</span><span class="sxs-lookup"><span data-stu-id="747b2-151">System.String</span></span>

## <span data-ttu-id="747b2-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="747b2-152">OUTPUTS</span></span>

### <span data-ttu-id="747b2-153">Microsoft. Azure. Commands. Network. models. PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="747b2-153">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="747b2-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="747b2-154">NOTES</span></span>
<span data-ttu-id="747b2-155">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, Monitor sieci, dotarcie, raport</span><span class="sxs-lookup"><span data-stu-id="747b2-155">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="747b2-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="747b2-156">RELATED LINKS</span></span>

[<span data-ttu-id="747b2-157">Nowe — AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="747b2-157">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="747b2-158">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="747b2-158">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="747b2-159">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="747b2-159">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="747b2-160">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="747b2-160">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="747b2-161">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="747b2-161">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="747b2-162">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="747b2-162">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="747b2-163">Start — AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="747b2-163">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="747b2-164">Nowe — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="747b2-164">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="747b2-165">Nowe — AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="747b2-165">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="747b2-166">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="747b2-166">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="747b2-167">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="747b2-167">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="747b2-168">Zatrzymaj — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="747b2-168">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="747b2-169">Nowe — AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="747b2-169">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="747b2-170">Test — AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="747b2-170">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="747b2-171">Test — AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="747b2-171">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="747b2-172">Zatrzymaj — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="747b2-172">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="747b2-173">Start — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="747b2-173">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="747b2-174">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="747b2-174">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="747b2-175">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="747b2-175">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="747b2-176">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="747b2-176">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="747b2-177">Nowe — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="747b2-177">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="747b2-178">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="747b2-178">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="747b2-179">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="747b2-179">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="747b2-180">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="747b2-180">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="747b2-181">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="747b2-181">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="747b2-182">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="747b2-182">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="747b2-183">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="747b2-183">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
