---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: 4cb80bec513459797790ae04c3e26a2f25fe95db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548644"
---
# <span data-ttu-id="5e8a7-101">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="5e8a7-101">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="5e8a7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5e8a7-102">SYNOPSIS</span></span>
<span data-ttu-id="5e8a7-103">Wyświetla listę wszystkich dostępnych dostawców usług internetowych dla określonego regionu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5e8a7-103">Lists all available internet service providers for a specified Azure region.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e8a7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5e8a7-104">SYNTAX</span></span>

### <span data-ttu-id="5e8a7-105">SetByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5e8a7-105">SetByName (Default)</span></span>
```
Get-AzureRmNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e8a7-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="5e8a7-106">SetByResource</span></span>
```
Get-AzureRmNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e8a7-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="5e8a7-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherReachabilityProvidersList -NetworkWatcherLocation <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e8a7-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5e8a7-108">SetByResourceId</span></span>
```
Get-AzureRmNetworkWatcherReachabilityProvidersList -ResourceId <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e8a7-109">Opis</span><span class="sxs-lookup"><span data-stu-id="5e8a7-109">DESCRIPTION</span></span>
<span data-ttu-id="5e8a7-110">Get-AzureRmNetworkWatcherReachabilityProvidersList wyświetla listę wszystkich dostępnych dostawców usług internetowych dla określonego regionu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5e8a7-110">The Get-AzureRmNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="5e8a7-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5e8a7-111">EXAMPLES</span></span>

### <span data-ttu-id="5e8a7-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5e8a7-112">Example 1</span></span>
```
PS C:\> $nw = Get-AzureRmNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
PS C:\> Get-AzureRmNetworkWatcherReachabilityProvidersList -NetworkWatcher $nw -Location "West US" -Country "United States" -State "washington" -City "seattle"

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

<span data-ttu-id="5e8a7-113">Wyświetla listę wszystkich dostępnych dostawców w Seattle, WA dla Azure Data Center w zachodnich Stanach Zjednoczonych.</span><span class="sxs-lookup"><span data-stu-id="5e8a7-113">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

## <span data-ttu-id="5e8a7-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5e8a7-114">PARAMETERS</span></span>

### <span data-ttu-id="5e8a7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5e8a7-115">-AsJob</span></span>
<span data-ttu-id="5e8a7-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="5e8a7-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5e8a7-117">-Miasto</span><span class="sxs-lookup"><span data-stu-id="5e8a7-117">-City</span></span>
<span data-ttu-id="5e8a7-118">Nazwa miasta.</span><span class="sxs-lookup"><span data-stu-id="5e8a7-118">The name of the city.</span></span>

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

### <span data-ttu-id="5e8a7-119">-Country</span><span class="sxs-lookup"><span data-stu-id="5e8a7-119">-Country</span></span>
<span data-ttu-id="5e8a7-120">Nazwa kraju.</span><span class="sxs-lookup"><span data-stu-id="5e8a7-120">The name of the country.</span></span>

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

### <span data-ttu-id="5e8a7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e8a7-121">-DefaultProfile</span></span>
<span data-ttu-id="5e8a7-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5e8a7-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e8a7-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="5e8a7-123">-Location</span></span>
<span data-ttu-id="5e8a7-124">Opcjonalne regiony platformy Azure umożliwiające zakres kwerendy.</span><span class="sxs-lookup"><span data-stu-id="5e8a7-124">Optional Azure regions to scope the query to.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e8a7-125">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5e8a7-125">-NetworkWatcher</span></span>
<span data-ttu-id="5e8a7-126">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="5e8a7-126">The network watcher resource.</span></span>

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

### <span data-ttu-id="5e8a7-127">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="5e8a7-127">-NetworkWatcherLocation</span></span>
<span data-ttu-id="5e8a7-128">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="5e8a7-128">Location of the network watcher.</span></span>

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

### <span data-ttu-id="5e8a7-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="5e8a7-129">-NetworkWatcherName</span></span>
<span data-ttu-id="5e8a7-130">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="5e8a7-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="5e8a7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e8a7-131">-ResourceGroupName</span></span>
<span data-ttu-id="5e8a7-132">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="5e8a7-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="5e8a7-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e8a7-133">-ResourceId</span></span>
<span data-ttu-id="5e8a7-134">Identyfikator zasobu obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="5e8a7-134">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="5e8a7-135">-State</span><span class="sxs-lookup"><span data-stu-id="5e8a7-135">-State</span></span>
<span data-ttu-id="5e8a7-136">Nazwa województwa.</span><span class="sxs-lookup"><span data-stu-id="5e8a7-136">The name of the state.</span></span>

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

### <span data-ttu-id="5e8a7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e8a7-137">CommonParameters</span></span>
<span data-ttu-id="5e8a7-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e8a7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e8a7-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e8a7-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e8a7-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5e8a7-140">INPUTS</span></span>

### <span data-ttu-id="5e8a7-141">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5e8a7-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="5e8a7-142">Parametry: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5e8a7-142">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="5e8a7-143">System. String</span><span class="sxs-lookup"><span data-stu-id="5e8a7-143">System.String</span></span>

## <span data-ttu-id="5e8a7-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5e8a7-144">OUTPUTS</span></span>

### <span data-ttu-id="5e8a7-145">Microsoft. Azure. Commands. Network. models. PSAvailableProvidersList</span><span class="sxs-lookup"><span data-stu-id="5e8a7-145">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="5e8a7-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5e8a7-146">NOTES</span></span>
<span data-ttu-id="5e8a7-147">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, Monitor sieci, następny, przeskok</span><span class="sxs-lookup"><span data-stu-id="5e8a7-147">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="5e8a7-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5e8a7-148">RELATED LINKS</span></span>

[<span data-ttu-id="5e8a7-149">Nowe — AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5e8a7-149">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="5e8a7-150">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5e8a7-150">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="5e8a7-151">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5e8a7-151">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="5e8a7-152">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="5e8a7-152">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="5e8a7-153">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="5e8a7-153">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="5e8a7-154">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="5e8a7-154">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="5e8a7-155">Start — AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="5e8a7-155">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="5e8a7-156">Nowe — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5e8a7-156">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5e8a7-157">Nowe — AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="5e8a7-157">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="5e8a7-158">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5e8a7-158">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5e8a7-159">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5e8a7-159">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5e8a7-160">Zatrzymaj — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5e8a7-160">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5e8a7-161">Nowe — AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="5e8a7-161">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="5e8a7-162">Test — AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="5e8a7-162">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="5e8a7-163">Test — AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="5e8a7-163">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="5e8a7-164">Zatrzymaj — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5e8a7-164">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5e8a7-165">Start — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5e8a7-165">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5e8a7-166">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5e8a7-166">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5e8a7-167">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="5e8a7-167">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="5e8a7-168">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5e8a7-168">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5e8a7-169">Nowe — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5e8a7-169">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5e8a7-170">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="5e8a7-170">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="5e8a7-171">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="5e8a7-171">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="5e8a7-172">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="5e8a7-172">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="5e8a7-173">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="5e8a7-173">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="5e8a7-174">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="5e8a7-174">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="5e8a7-175">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5e8a7-175">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
