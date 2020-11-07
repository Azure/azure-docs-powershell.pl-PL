---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 0ad2b1fa6278e085a57d94f2fec9be2c6853993d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895066"
---
# <span data-ttu-id="2c210-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="2c210-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="2c210-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2c210-102">SYNOPSIS</span></span>
<span data-ttu-id="2c210-103">Pobiera względny wynik opóźnienia dla dostawców usług internetowych z określonej lokalizacji na regiony platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2c210-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="2c210-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2c210-104">SYNTAX</span></span>

### <span data-ttu-id="2c210-105">SetByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2c210-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <String[]>] [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c210-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="2c210-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c210-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2c210-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String> [-Provider <String[]>] [-Location <String[]>]
 -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c210-108">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="2c210-108">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherLocation <String> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c210-109">Opis</span><span class="sxs-lookup"><span data-stu-id="2c210-109">DESCRIPTION</span></span>
<span data-ttu-id="2c210-110">Get-AzNetworkWatcherReachabilityReport pobiera względny wynik opóźnienia dla dostawców usług internetowych z określonej lokalizacji do regionów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2c210-110">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="2c210-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2c210-111">EXAMPLES</span></span>

### <span data-ttu-id="2c210-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2c210-112">Example 1</span></span>
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

<span data-ttu-id="2c210-113">Pobiera względne opóźnienia w usłudze Azure Data Center w Stanach Zjednoczonych na zachód od 2017-10-10 do 2017-10-12 w stanie amerykańskim.</span><span class="sxs-lookup"><span data-stu-id="2c210-113">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

## <span data-ttu-id="2c210-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2c210-114">PARAMETERS</span></span>

### <span data-ttu-id="2c210-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2c210-115">-AsJob</span></span>
<span data-ttu-id="2c210-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="2c210-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2c210-117">-Miasto</span><span class="sxs-lookup"><span data-stu-id="2c210-117">-City</span></span>
<span data-ttu-id="2c210-118">Nazwa miasta.</span><span class="sxs-lookup"><span data-stu-id="2c210-118">The name of the city.</span></span>

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

### <span data-ttu-id="2c210-119">-Country</span><span class="sxs-lookup"><span data-stu-id="2c210-119">-Country</span></span>
<span data-ttu-id="2c210-120">Nazwa kraju.</span><span class="sxs-lookup"><span data-stu-id="2c210-120">The name of the country.</span></span>

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

### <span data-ttu-id="2c210-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c210-121">-DefaultProfile</span></span>
<span data-ttu-id="2c210-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2c210-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c210-123">-EndTime</span><span class="sxs-lookup"><span data-stu-id="2c210-123">-EndTime</span></span>
<span data-ttu-id="2c210-124">Godzina zakończenia dla raportu o nieobecności w usłudze Azure.</span><span class="sxs-lookup"><span data-stu-id="2c210-124">The end time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="2c210-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2c210-125">-Location</span></span>
<span data-ttu-id="2c210-126">Opcjonalne regiony platformy Azure umożliwiające zakres kwerendy.</span><span class="sxs-lookup"><span data-stu-id="2c210-126">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="2c210-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2c210-127">-NetworkWatcher</span></span>
<span data-ttu-id="2c210-128">Zasób obserwatora sieci</span><span class="sxs-lookup"><span data-stu-id="2c210-128">The network watcher resource</span></span>

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

### <span data-ttu-id="2c210-129">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="2c210-129">-NetworkWatcherLocation</span></span>
<span data-ttu-id="2c210-130">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="2c210-130">Location of the network watcher.</span></span>

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

### <span data-ttu-id="2c210-131">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="2c210-131">-NetworkWatcherName</span></span>
<span data-ttu-id="2c210-132">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="2c210-132">The name of network watcher.</span></span>

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

### <span data-ttu-id="2c210-133">-Provider</span><span class="sxs-lookup"><span data-stu-id="2c210-133">-Provider</span></span>
<span data-ttu-id="2c210-134">Lista dostawców usług internetowych.</span><span class="sxs-lookup"><span data-stu-id="2c210-134">List of Internet service providers.</span></span>

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

### <span data-ttu-id="2c210-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c210-135">-ResourceGroupName</span></span>
<span data-ttu-id="2c210-136">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="2c210-136">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="2c210-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c210-137">-ResourceId</span></span>
<span data-ttu-id="2c210-138">Identyfikator zasobu obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="2c210-138">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="2c210-139">-StartTime</span><span class="sxs-lookup"><span data-stu-id="2c210-139">-StartTime</span></span>
<span data-ttu-id="2c210-140">Godzina rozpoczęcia dla raportu o nieobecności w usłudze Azure.</span><span class="sxs-lookup"><span data-stu-id="2c210-140">The start time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="2c210-141">-State</span><span class="sxs-lookup"><span data-stu-id="2c210-141">-State</span></span>
<span data-ttu-id="2c210-142">Nazwa województwa.</span><span class="sxs-lookup"><span data-stu-id="2c210-142">The name of the state.</span></span>

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

### <span data-ttu-id="2c210-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c210-143">CommonParameters</span></span>
<span data-ttu-id="2c210-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c210-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c210-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c210-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c210-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2c210-146">INPUTS</span></span>

### <span data-ttu-id="2c210-147">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2c210-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="2c210-148">System. String</span><span class="sxs-lookup"><span data-stu-id="2c210-148">System.String</span></span>

## <span data-ttu-id="2c210-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2c210-149">OUTPUTS</span></span>

### <span data-ttu-id="2c210-150">Microsoft. Azure. Commands. Network. models. PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="2c210-150">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="2c210-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2c210-151">NOTES</span></span>
<span data-ttu-id="2c210-152">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, Monitor sieci, dotarcie, raport</span><span class="sxs-lookup"><span data-stu-id="2c210-152">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="2c210-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2c210-153">RELATED LINKS</span></span>

[<span data-ttu-id="2c210-154">Nowe — AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2c210-154">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="2c210-155">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2c210-155">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="2c210-156">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2c210-156">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="2c210-157">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="2c210-157">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="2c210-158">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="2c210-158">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="2c210-159">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="2c210-159">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="2c210-160">Start — AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="2c210-160">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="2c210-161">Nowe — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2c210-161">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2c210-162">Nowe — AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="2c210-162">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="2c210-163">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2c210-163">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2c210-164">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2c210-164">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2c210-165">Zatrzymaj — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2c210-165">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2c210-166">Nowe — AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c210-166">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="2c210-167">Test — AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2c210-167">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="2c210-168">Test — AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="2c210-168">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="2c210-169">Zatrzymaj — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2c210-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2c210-170">Start — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2c210-170">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2c210-171">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2c210-171">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2c210-172">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="2c210-172">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="2c210-173">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2c210-173">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2c210-174">Nowe — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2c210-174">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2c210-175">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="2c210-175">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="2c210-176">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="2c210-176">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="2c210-177">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="2c210-177">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="2c210-178">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="2c210-178">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="2c210-179">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="2c210-179">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="2c210-180">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2c210-180">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)