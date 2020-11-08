---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 3fe26c99dd92afb65105008524908a10dec02e0e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232814"
---
# <span data-ttu-id="1160b-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="1160b-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="1160b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1160b-102">SYNOPSIS</span></span>
<span data-ttu-id="1160b-103">Pobiera względny wynik opóźnienia dla dostawców usług internetowych z określonej lokalizacji na regiony platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1160b-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="1160b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1160b-104">SYNTAX</span></span>

### <span data-ttu-id="1160b-105">SetByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1160b-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <String[]>] [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1160b-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="1160b-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1160b-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1160b-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String> [-Provider <String[]>] [-Location <String[]>]
 -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1160b-108">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="1160b-108">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherLocation <String> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1160b-109">Opis</span><span class="sxs-lookup"><span data-stu-id="1160b-109">DESCRIPTION</span></span>
<span data-ttu-id="1160b-110">Get-AzNetworkWatcherReachabilityReport pobiera względny wynik opóźnienia dla dostawców usług internetowych z określonej lokalizacji do regionów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1160b-110">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="1160b-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1160b-111">EXAMPLES</span></span>

### <span data-ttu-id="1160b-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1160b-112">Example 1</span></span>
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

<span data-ttu-id="1160b-113">Pobiera względne opóźnienia w usłudze Azure Data Center w Stanach Zjednoczonych na zachód od 2017-10-10 do 2017-10-12 w stanie amerykańskim.</span><span class="sxs-lookup"><span data-stu-id="1160b-113">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

### <span data-ttu-id="1160b-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="1160b-114">Example 2</span></span>

<span data-ttu-id="1160b-115">Pobiera względny wynik opóźnienia dla dostawców usług internetowych z określonej lokalizacji na regiony platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1160b-115">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span> <span data-ttu-id="1160b-116">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="1160b-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNetworkWatcherReachabilityReport -Country 'United States' -EndTime '2017-10-12' -Location 'West US' -NetworkWatcherName nw1 -ResourceGroupName myresourcegroup -StartTime '2017-10-10' -State 'washington'
```

## <span data-ttu-id="1160b-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1160b-117">PARAMETERS</span></span>

### <span data-ttu-id="1160b-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1160b-118">-AsJob</span></span>
<span data-ttu-id="1160b-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1160b-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1160b-120">-Miasto</span><span class="sxs-lookup"><span data-stu-id="1160b-120">-City</span></span>
<span data-ttu-id="1160b-121">Nazwa miasta.</span><span class="sxs-lookup"><span data-stu-id="1160b-121">The name of the city.</span></span>

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

### <span data-ttu-id="1160b-122">-Country</span><span class="sxs-lookup"><span data-stu-id="1160b-122">-Country</span></span>
<span data-ttu-id="1160b-123">Nazwa kraju.</span><span class="sxs-lookup"><span data-stu-id="1160b-123">The name of the country.</span></span>

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

### <span data-ttu-id="1160b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1160b-124">-DefaultProfile</span></span>
<span data-ttu-id="1160b-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1160b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1160b-126">-EndTime</span><span class="sxs-lookup"><span data-stu-id="1160b-126">-EndTime</span></span>
<span data-ttu-id="1160b-127">Godzina zakończenia dla raportu o nieobecności w usłudze Azure.</span><span class="sxs-lookup"><span data-stu-id="1160b-127">The end time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="1160b-128">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="1160b-128">-Location</span></span>
<span data-ttu-id="1160b-129">Opcjonalne regiony platformy Azure umożliwiające zakres kwerendy.</span><span class="sxs-lookup"><span data-stu-id="1160b-129">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="1160b-130">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1160b-130">-NetworkWatcher</span></span>
<span data-ttu-id="1160b-131">Zasób obserwatora sieci</span><span class="sxs-lookup"><span data-stu-id="1160b-131">The network watcher resource</span></span>

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

### <span data-ttu-id="1160b-132">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="1160b-132">-NetworkWatcherLocation</span></span>
<span data-ttu-id="1160b-133">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="1160b-133">Location of the network watcher.</span></span>

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

### <span data-ttu-id="1160b-134">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="1160b-134">-NetworkWatcherName</span></span>
<span data-ttu-id="1160b-135">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="1160b-135">The name of network watcher.</span></span>

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

### <span data-ttu-id="1160b-136">-Provider</span><span class="sxs-lookup"><span data-stu-id="1160b-136">-Provider</span></span>
<span data-ttu-id="1160b-137">Lista dostawców usług internetowych.</span><span class="sxs-lookup"><span data-stu-id="1160b-137">List of Internet service providers.</span></span>

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

### <span data-ttu-id="1160b-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1160b-138">-ResourceGroupName</span></span>
<span data-ttu-id="1160b-139">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="1160b-139">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="1160b-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1160b-140">-ResourceId</span></span>
<span data-ttu-id="1160b-141">Identyfikator zasobu obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="1160b-141">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="1160b-142">-StartTime</span><span class="sxs-lookup"><span data-stu-id="1160b-142">-StartTime</span></span>
<span data-ttu-id="1160b-143">Godzina rozpoczęcia dla raportu o nieobecności w usłudze Azure.</span><span class="sxs-lookup"><span data-stu-id="1160b-143">The start time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="1160b-144">-State</span><span class="sxs-lookup"><span data-stu-id="1160b-144">-State</span></span>
<span data-ttu-id="1160b-145">Nazwa województwa.</span><span class="sxs-lookup"><span data-stu-id="1160b-145">The name of the state.</span></span>

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

### <span data-ttu-id="1160b-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1160b-146">CommonParameters</span></span>
<span data-ttu-id="1160b-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1160b-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1160b-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1160b-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1160b-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1160b-149">INPUTS</span></span>

### <span data-ttu-id="1160b-150">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1160b-150">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="1160b-151">System. String</span><span class="sxs-lookup"><span data-stu-id="1160b-151">System.String</span></span>

## <span data-ttu-id="1160b-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1160b-152">OUTPUTS</span></span>

### <span data-ttu-id="1160b-153">Microsoft. Azure. Commands. Network. models. PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="1160b-153">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="1160b-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1160b-154">NOTES</span></span>
<span data-ttu-id="1160b-155">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, Monitor sieci, dotarcie, raport</span><span class="sxs-lookup"><span data-stu-id="1160b-155">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="1160b-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1160b-156">RELATED LINKS</span></span>

[<span data-ttu-id="1160b-157">Nowe — AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1160b-157">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="1160b-158">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1160b-158">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="1160b-159">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1160b-159">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="1160b-160">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="1160b-160">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="1160b-161">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="1160b-161">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="1160b-162">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="1160b-162">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="1160b-163">Start — AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="1160b-163">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="1160b-164">Nowe — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1160b-164">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1160b-165">Nowe — AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="1160b-165">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="1160b-166">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1160b-166">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1160b-167">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1160b-167">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1160b-168">Zatrzymaj — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1160b-168">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1160b-169">Nowe — AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="1160b-169">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="1160b-170">Test — AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="1160b-170">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="1160b-171">Test — AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="1160b-171">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="1160b-172">Zatrzymaj — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1160b-172">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1160b-173">Start — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1160b-173">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1160b-174">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1160b-174">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1160b-175">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="1160b-175">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="1160b-176">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1160b-176">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1160b-177">Nowe — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1160b-177">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1160b-178">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="1160b-178">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="1160b-179">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="1160b-179">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="1160b-180">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="1160b-180">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="1160b-181">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="1160b-181">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="1160b-182">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="1160b-182">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="1160b-183">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1160b-183">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
