---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: 227bd70bd67ff29015223becc6788f5043ae4776
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411045"
---
# <span data-ttu-id="d7ec6-101">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="d7ec6-101">Get-AzNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="d7ec6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7ec6-102">SYNOPSIS</span></span>
<span data-ttu-id="d7ec6-103">Lista wszystkich dostępnych dostawców usług internetowych dla określonego regionu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d7ec6-103">Lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="d7ec6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d7ec6-104">SYNTAX</span></span>

### <span data-ttu-id="d7ec6-105">SetByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="d7ec6-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <String[]>] [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7ec6-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d7ec6-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d7ec6-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="d7ec6-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherLocation <String> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d7ec6-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d7ec6-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -ResourceId <String> [-Location <String[]>] [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7ec6-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="d7ec6-109">DESCRIPTION</span></span>
<span data-ttu-id="d7ec6-110">Ten Get-AzNetworkWatcherReachabilityProvidersList listę wszystkich dostępnych dostawców usług internetowych dla określonego regionu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d7ec6-110">The Get-AzNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="d7ec6-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d7ec6-111">EXAMPLES</span></span>

### <span data-ttu-id="d7ec6-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d7ec6-112">Example 1</span></span>
```
PS C:\> $nw = Get-AzNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
PS C:\> Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher $nw -Location "West US" -Country "United States" -State "washington" -City "seattle"

"countries" : [
    {
        "countryName" : "United States",
        "states" : [
            {
                "stateName" : "washington",
                "cities" : [
                    {
                        "cityName" : "seattle",
                        "providers" : [
                            "Comcast Cable Communications, Inc. - ASN 7922",
                            "Comcast Cable Communications, LLC - ASN 7922",
                            "Level 3 Communications, Inc. (GBLX) - ASN 3549",
                            "Qwest Communications Company, LLC - ASN 209"
                        ]
                    }
                ]
            }
        ]
    }
]
```

<span data-ttu-id="d7ec6-113">Lista wszystkich dostępnych dostawców w Seattle, WA dla centrum danych Azure w Stanach Zjednoczonych Zachód.</span><span class="sxs-lookup"><span data-stu-id="d7ec6-113">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

## <span data-ttu-id="d7ec6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7ec6-114">PARAMETERS</span></span>

### <span data-ttu-id="d7ec6-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="d7ec6-115">-AsJob</span></span>
<span data-ttu-id="d7ec6-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d7ec6-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d7ec6-117">— Miasto</span><span class="sxs-lookup"><span data-stu-id="d7ec6-117">-City</span></span>
<span data-ttu-id="d7ec6-118">Nazwa miasta.</span><span class="sxs-lookup"><span data-stu-id="d7ec6-118">The name of the city.</span></span>

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

### <span data-ttu-id="d7ec6-119">— Kraj</span><span class="sxs-lookup"><span data-stu-id="d7ec6-119">-Country</span></span>
<span data-ttu-id="d7ec6-120">Nazwa kraju.</span><span class="sxs-lookup"><span data-stu-id="d7ec6-120">The name of the country.</span></span>

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

### <span data-ttu-id="d7ec6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7ec6-121">-DefaultProfile</span></span>
<span data-ttu-id="d7ec6-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d7ec6-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7ec6-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d7ec6-123">-Location</span></span>
<span data-ttu-id="d7ec6-124">Opcjonalne regiony platformy Azure, do których ma być objęte zapytaniem.</span><span class="sxs-lookup"><span data-stu-id="d7ec6-124">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="d7ec6-125">- NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d7ec6-125">-NetworkWatcher</span></span>
<span data-ttu-id="d7ec6-126">Zasób obserwowania sieci.</span><span class="sxs-lookup"><span data-stu-id="d7ec6-126">The network watcher resource.</span></span>

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

### <span data-ttu-id="d7ec6-127">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="d7ec6-127">-NetworkWatcherLocation</span></span>
<span data-ttu-id="d7ec6-128">Lokalizacja czujki sieci.</span><span class="sxs-lookup"><span data-stu-id="d7ec6-128">Location of the network watcher.</span></span>

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

### <span data-ttu-id="d7ec6-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d7ec6-129">-NetworkWatcherName</span></span>
<span data-ttu-id="d7ec6-130">Nazwa osoby oglądacej sieć.</span><span class="sxs-lookup"><span data-stu-id="d7ec6-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="d7ec6-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7ec6-131">-ResourceGroupName</span></span>
<span data-ttu-id="d7ec6-132">Nazwa grupy zasobów obserwowanych sieci.</span><span class="sxs-lookup"><span data-stu-id="d7ec6-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="d7ec6-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d7ec6-133">-ResourceId</span></span>
<span data-ttu-id="d7ec6-134">Identyfikator zasobu czujki sieciowej.</span><span class="sxs-lookup"><span data-stu-id="d7ec6-134">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="d7ec6-135">— województwo</span><span class="sxs-lookup"><span data-stu-id="d7ec6-135">-State</span></span>
<span data-ttu-id="d7ec6-136">Nazwa województwa.</span><span class="sxs-lookup"><span data-stu-id="d7ec6-136">The name of the state.</span></span>

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

### <span data-ttu-id="d7ec6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7ec6-137">CommonParameters</span></span>
<span data-ttu-id="d7ec6-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7ec6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7ec6-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d7ec6-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7ec6-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7ec6-140">INPUTS</span></span>

### <span data-ttu-id="d7ec6-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d7ec6-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="d7ec6-142">System.String</span><span class="sxs-lookup"><span data-stu-id="d7ec6-142">System.String</span></span>

## <span data-ttu-id="d7ec6-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7ec6-143">OUTPUTS</span></span>

### <span data-ttu-id="d7ec6-144">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span><span class="sxs-lookup"><span data-stu-id="d7ec6-144">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="d7ec6-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d7ec6-145">NOTES</span></span>
<span data-ttu-id="d7ec6-146">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span><span class="sxs-lookup"><span data-stu-id="d7ec6-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="d7ec6-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d7ec6-147">RELATED LINKS</span></span>

[<span data-ttu-id="d7ec6-148">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d7ec6-148">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="d7ec6-149">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d7ec6-149">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="d7ec6-150">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d7ec6-150">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="d7ec6-151">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d7ec6-151">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="d7ec6-152">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d7ec6-152">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d7ec6-153">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d7ec6-153">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="d7ec6-154">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d7ec6-154">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="d7ec6-155">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d7ec6-155">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d7ec6-156">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d7ec6-156">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="d7ec6-157">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d7ec6-157">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d7ec6-158">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d7ec6-158">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d7ec6-159">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d7ec6-159">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d7ec6-160">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="d7ec6-160">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="d7ec6-161">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d7ec6-161">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="d7ec6-162">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="d7ec6-162">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="d7ec6-163">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d7ec6-163">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d7ec6-164">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d7ec6-164">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d7ec6-165">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d7ec6-165">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d7ec6-166">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="d7ec6-166">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="d7ec6-167">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d7ec6-167">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d7ec6-168">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d7ec6-168">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d7ec6-169">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="d7ec6-169">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="d7ec6-170">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="d7ec6-170">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="d7ec6-171">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="d7ec6-171">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="d7ec6-172">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="d7ec6-172">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="d7ec6-173">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="d7ec6-173">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="d7ec6-174">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d7ec6-174">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
