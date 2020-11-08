---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: a4e9c9a928d3a6c3ddeb7afa754cc957089a2283
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225379"
---
# <span data-ttu-id="4167d-101">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="4167d-101">Get-AzNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="4167d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4167d-102">SYNOPSIS</span></span>
<span data-ttu-id="4167d-103">Wyświetla listę wszystkich dostępnych dostawców usług internetowych dla określonego regionu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4167d-103">Lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="4167d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4167d-104">SYNTAX</span></span>

### <span data-ttu-id="4167d-105">SetByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4167d-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <String[]>] [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4167d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4167d-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4167d-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="4167d-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherLocation <String> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4167d-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4167d-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -ResourceId <String> [-Location <String[]>] [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4167d-109">Opis</span><span class="sxs-lookup"><span data-stu-id="4167d-109">DESCRIPTION</span></span>
<span data-ttu-id="4167d-110">Get-AzNetworkWatcherReachabilityProvidersList wyświetla listę wszystkich dostępnych dostawców usług internetowych dla określonego regionu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4167d-110">The Get-AzNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="4167d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4167d-111">EXAMPLES</span></span>

### <span data-ttu-id="4167d-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4167d-112">Example 1</span></span>
```powershell
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

<span data-ttu-id="4167d-113">Wyświetla listę wszystkich dostępnych dostawców w Seattle, WA dla Azure Data Center w zachodnich Stanach Zjednoczonych.</span><span class="sxs-lookup"><span data-stu-id="4167d-113">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

### <span data-ttu-id="4167d-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="4167d-114">Example 2</span></span>

<span data-ttu-id="4167d-115">Wyświetla listę wszystkich dostępnych dostawców usług internetowych dla określonego regionu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4167d-115">Lists all available internet service providers for a specified Azure region.</span></span> <span data-ttu-id="4167d-116">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="4167d-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName nw1 -ResourceGroupName myresourcegroup
```

## <span data-ttu-id="4167d-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4167d-117">PARAMETERS</span></span>

### <span data-ttu-id="4167d-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4167d-118">-AsJob</span></span>
<span data-ttu-id="4167d-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="4167d-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4167d-120">-Miasto</span><span class="sxs-lookup"><span data-stu-id="4167d-120">-City</span></span>
<span data-ttu-id="4167d-121">Nazwa miasta.</span><span class="sxs-lookup"><span data-stu-id="4167d-121">The name of the city.</span></span>

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

### <span data-ttu-id="4167d-122">-Country</span><span class="sxs-lookup"><span data-stu-id="4167d-122">-Country</span></span>
<span data-ttu-id="4167d-123">Nazwa kraju.</span><span class="sxs-lookup"><span data-stu-id="4167d-123">The name of the country.</span></span>

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

### <span data-ttu-id="4167d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4167d-124">-DefaultProfile</span></span>
<span data-ttu-id="4167d-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4167d-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4167d-126">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="4167d-126">-Location</span></span>
<span data-ttu-id="4167d-127">Opcjonalne regiony platformy Azure umożliwiające zakres kwerendy.</span><span class="sxs-lookup"><span data-stu-id="4167d-127">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="4167d-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4167d-128">-NetworkWatcher</span></span>
<span data-ttu-id="4167d-129">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="4167d-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="4167d-130">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="4167d-130">-NetworkWatcherLocation</span></span>
<span data-ttu-id="4167d-131">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="4167d-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="4167d-132">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="4167d-132">-NetworkWatcherName</span></span>
<span data-ttu-id="4167d-133">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="4167d-133">The name of network watcher.</span></span>

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

### <span data-ttu-id="4167d-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4167d-134">-ResourceGroupName</span></span>
<span data-ttu-id="4167d-135">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="4167d-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="4167d-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4167d-136">-ResourceId</span></span>
<span data-ttu-id="4167d-137">Identyfikator zasobu obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="4167d-137">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="4167d-138">-State</span><span class="sxs-lookup"><span data-stu-id="4167d-138">-State</span></span>
<span data-ttu-id="4167d-139">Nazwa województwa.</span><span class="sxs-lookup"><span data-stu-id="4167d-139">The name of the state.</span></span>

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

### <span data-ttu-id="4167d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4167d-140">CommonParameters</span></span>
<span data-ttu-id="4167d-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4167d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4167d-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4167d-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4167d-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4167d-143">INPUTS</span></span>

### <span data-ttu-id="4167d-144">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4167d-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="4167d-145">System. String</span><span class="sxs-lookup"><span data-stu-id="4167d-145">System.String</span></span>

## <span data-ttu-id="4167d-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4167d-146">OUTPUTS</span></span>

### <span data-ttu-id="4167d-147">Microsoft. Azure. Commands. Network. models. PSAvailableProvidersList</span><span class="sxs-lookup"><span data-stu-id="4167d-147">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="4167d-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4167d-148">NOTES</span></span>
<span data-ttu-id="4167d-149">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, Monitor sieci, następny, przeskok</span><span class="sxs-lookup"><span data-stu-id="4167d-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="4167d-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4167d-150">RELATED LINKS</span></span>

[<span data-ttu-id="4167d-151">Nowe — AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4167d-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="4167d-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4167d-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="4167d-153">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4167d-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="4167d-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="4167d-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="4167d-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="4167d-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="4167d-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="4167d-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="4167d-157">Start — AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="4167d-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="4167d-158">Nowe — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4167d-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4167d-159">Nowe — AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="4167d-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="4167d-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4167d-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4167d-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4167d-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4167d-162">Zatrzymaj — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4167d-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4167d-163">Nowe — AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="4167d-163">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="4167d-164">Test — AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="4167d-164">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="4167d-165">Test — AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="4167d-165">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="4167d-166">Zatrzymaj — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4167d-166">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4167d-167">Start — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4167d-167">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4167d-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4167d-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4167d-169">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="4167d-169">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="4167d-170">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4167d-170">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4167d-171">Nowe — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4167d-171">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4167d-172">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="4167d-172">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="4167d-173">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="4167d-173">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="4167d-174">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="4167d-174">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="4167d-175">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="4167d-175">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="4167d-176">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="4167d-176">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="4167d-177">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4167d-177">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
