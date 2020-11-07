---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: a2c66f9e93a26c433c245f87c8506b71ad01c5e1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895065"
---
# <span data-ttu-id="76123-101">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="76123-101">Get-AzNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="76123-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="76123-102">SYNOPSIS</span></span>
<span data-ttu-id="76123-103">Wyświetla listę wszystkich dostępnych dostawców usług internetowych dla określonego regionu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="76123-103">Lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="76123-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="76123-104">SYNTAX</span></span>

### <span data-ttu-id="76123-105">SetByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="76123-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <String[]>] [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76123-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="76123-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="76123-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="76123-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherLocation <String> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="76123-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="76123-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -ResourceId <String> [-Location <String[]>] [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76123-109">Opis</span><span class="sxs-lookup"><span data-stu-id="76123-109">DESCRIPTION</span></span>
<span data-ttu-id="76123-110">Get-AzNetworkWatcherReachabilityProvidersList wyświetla listę wszystkich dostępnych dostawców usług internetowych dla określonego regionu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="76123-110">The Get-AzNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="76123-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="76123-111">EXAMPLES</span></span>

### <span data-ttu-id="76123-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="76123-112">Example 1</span></span>
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

<span data-ttu-id="76123-113">Wyświetla listę wszystkich dostępnych dostawców w Seattle, WA dla Azure Data Center w zachodnich Stanach Zjednoczonych.</span><span class="sxs-lookup"><span data-stu-id="76123-113">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

## <span data-ttu-id="76123-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="76123-114">PARAMETERS</span></span>

### <span data-ttu-id="76123-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="76123-115">-AsJob</span></span>
<span data-ttu-id="76123-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="76123-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="76123-117">-Miasto</span><span class="sxs-lookup"><span data-stu-id="76123-117">-City</span></span>
<span data-ttu-id="76123-118">Nazwa miasta.</span><span class="sxs-lookup"><span data-stu-id="76123-118">The name of the city.</span></span>

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

### <span data-ttu-id="76123-119">-Country</span><span class="sxs-lookup"><span data-stu-id="76123-119">-Country</span></span>
<span data-ttu-id="76123-120">Nazwa kraju.</span><span class="sxs-lookup"><span data-stu-id="76123-120">The name of the country.</span></span>

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

### <span data-ttu-id="76123-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76123-121">-DefaultProfile</span></span>
<span data-ttu-id="76123-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="76123-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76123-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="76123-123">-Location</span></span>
<span data-ttu-id="76123-124">Opcjonalne regiony platformy Azure umożliwiające zakres kwerendy.</span><span class="sxs-lookup"><span data-stu-id="76123-124">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="76123-125">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="76123-125">-NetworkWatcher</span></span>
<span data-ttu-id="76123-126">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="76123-126">The network watcher resource.</span></span>

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

### <span data-ttu-id="76123-127">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="76123-127">-NetworkWatcherLocation</span></span>
<span data-ttu-id="76123-128">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="76123-128">Location of the network watcher.</span></span>

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

### <span data-ttu-id="76123-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="76123-129">-NetworkWatcherName</span></span>
<span data-ttu-id="76123-130">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="76123-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="76123-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76123-131">-ResourceGroupName</span></span>
<span data-ttu-id="76123-132">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="76123-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="76123-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76123-133">-ResourceId</span></span>
<span data-ttu-id="76123-134">Identyfikator zasobu obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="76123-134">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="76123-135">-State</span><span class="sxs-lookup"><span data-stu-id="76123-135">-State</span></span>
<span data-ttu-id="76123-136">Nazwa województwa.</span><span class="sxs-lookup"><span data-stu-id="76123-136">The name of the state.</span></span>

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

### <span data-ttu-id="76123-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76123-137">CommonParameters</span></span>
<span data-ttu-id="76123-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76123-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76123-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76123-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76123-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76123-140">INPUTS</span></span>

### <span data-ttu-id="76123-141">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="76123-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="76123-142">System. String</span><span class="sxs-lookup"><span data-stu-id="76123-142">System.String</span></span>

## <span data-ttu-id="76123-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="76123-143">OUTPUTS</span></span>

### <span data-ttu-id="76123-144">Microsoft. Azure. Commands. Network. models. PSAvailableProvidersList</span><span class="sxs-lookup"><span data-stu-id="76123-144">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="76123-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="76123-145">NOTES</span></span>
<span data-ttu-id="76123-146">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, Monitor sieci, następny, przeskok</span><span class="sxs-lookup"><span data-stu-id="76123-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="76123-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="76123-147">RELATED LINKS</span></span>

[<span data-ttu-id="76123-148">Nowe — AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="76123-148">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="76123-149">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="76123-149">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="76123-150">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="76123-150">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="76123-151">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="76123-151">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="76123-152">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="76123-152">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="76123-153">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="76123-153">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="76123-154">Start — AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="76123-154">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="76123-155">Nowe — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="76123-155">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="76123-156">Nowe — AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="76123-156">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="76123-157">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="76123-157">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="76123-158">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="76123-158">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="76123-159">Zatrzymaj — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="76123-159">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="76123-160">Nowe — AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="76123-160">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="76123-161">Test — AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="76123-161">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="76123-162">Test — AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="76123-162">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="76123-163">Zatrzymaj — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="76123-163">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="76123-164">Start — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="76123-164">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="76123-165">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="76123-165">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="76123-166">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="76123-166">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="76123-167">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="76123-167">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="76123-168">Nowe — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="76123-168">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="76123-169">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="76123-169">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="76123-170">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="76123-170">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="76123-171">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="76123-171">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="76123-172">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="76123-172">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="76123-173">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="76123-173">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="76123-174">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="76123-174">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
