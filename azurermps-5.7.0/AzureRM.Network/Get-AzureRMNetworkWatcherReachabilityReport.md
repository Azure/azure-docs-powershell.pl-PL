---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRMNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRMNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 7ec4ebbe9e1224e47605a35f7f21feb2dfbcf045
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548936"
---
# <span data-ttu-id="35bca-101">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="35bca-101">Get-AzureRMNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="35bca-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="35bca-102">SYNOPSIS</span></span>
<span data-ttu-id="35bca-103">Pobiera względny wynik opóźnienia dla dostawców usług internetowych z określonej lokalizacji na regiony platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="35bca-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35bca-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="35bca-104">SYNTAX</span></span>

### <span data-ttu-id="35bca-105">SetByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="35bca-105">SetByName (Default)</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="35bca-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="35bca-106">SetByResource</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="35bca-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="35bca-107">SetByResourceId</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -ResourceId <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="35bca-108">Opis</span><span class="sxs-lookup"><span data-stu-id="35bca-108">DESCRIPTION</span></span>
<span data-ttu-id="35bca-109">Get-AzureRmNetworkWatcherReachabilityReport pobiera względny wynik opóźnienia dla dostawców usług internetowych z określonej lokalizacji do regionów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="35bca-109">The Get-AzureRmNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="35bca-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="35bca-110">EXAMPLES</span></span>

### <span data-ttu-id="35bca-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="35bca-111">Example 1</span></span>
```
$nw = Get-AzureRmNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
Get-AzureRmNetworkWatcherReachabilityReport -NetworkWatcher $nw -Location "West US" -Country "United States" -StartTime "2017-10-10" -EndTime "2017-10-12"

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

<span data-ttu-id="35bca-112">Pobiera względne opóźnienia w usłudze Azure Data Center w Stanach Zjednoczonych na zachód od 2017-10-10 do 2017-10-12 w stanie amerykańskim.</span><span class="sxs-lookup"><span data-stu-id="35bca-112">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

## <span data-ttu-id="35bca-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="35bca-113">PARAMETERS</span></span>

### <span data-ttu-id="35bca-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35bca-114">-AsJob</span></span>
<span data-ttu-id="35bca-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="35bca-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35bca-116">-Miasto</span><span class="sxs-lookup"><span data-stu-id="35bca-116">-City</span></span>
<span data-ttu-id="35bca-117">Nazwa miasta.</span><span class="sxs-lookup"><span data-stu-id="35bca-117">The name of the city.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35bca-118">-Country</span><span class="sxs-lookup"><span data-stu-id="35bca-118">-Country</span></span>
<span data-ttu-id="35bca-119">Nazwa kraju.</span><span class="sxs-lookup"><span data-stu-id="35bca-119">The name of the country.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35bca-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35bca-120">-DefaultProfile</span></span>
<span data-ttu-id="35bca-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="35bca-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35bca-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="35bca-122">-EndTime</span></span>
<span data-ttu-id="35bca-123">Godzina zakończenia dla raportu o nieobecności w usłudze Azure.</span><span class="sxs-lookup"><span data-stu-id="35bca-123">The end time for the Azure reachability report.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35bca-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="35bca-124">-Location</span></span>
<span data-ttu-id="35bca-125">Opcjonalne regiony platformy Azure umożliwiające zakres kwerendy.</span><span class="sxs-lookup"><span data-stu-id="35bca-125">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="35bca-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="35bca-126">-NetworkWatcher</span></span>
<span data-ttu-id="35bca-127">Zasób obserwatora sieci</span><span class="sxs-lookup"><span data-stu-id="35bca-127">The network watcher resource</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35bca-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="35bca-128">-NetworkWatcherName</span></span>
<span data-ttu-id="35bca-129">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="35bca-129">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: ResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35bca-130">-Provider</span><span class="sxs-lookup"><span data-stu-id="35bca-130">-Provider</span></span>
<span data-ttu-id="35bca-131">Lista dostawców usług internetowych.</span><span class="sxs-lookup"><span data-stu-id="35bca-131">List of Internet service providers.</span></span>

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

### <span data-ttu-id="35bca-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35bca-132">-ResourceGroupName</span></span>
<span data-ttu-id="35bca-133">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="35bca-133">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35bca-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35bca-134">-ResourceId</span></span>
<span data-ttu-id="35bca-135">Identyfikator zasobu obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="35bca-135">The Id of network watcher resource.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35bca-136">-StartTime</span><span class="sxs-lookup"><span data-stu-id="35bca-136">-StartTime</span></span>
<span data-ttu-id="35bca-137">Godzina rozpoczęcia dla raportu o nieobecności w usłudze Azure.</span><span class="sxs-lookup"><span data-stu-id="35bca-137">The start time for the Azure reachability report.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35bca-138">-State</span><span class="sxs-lookup"><span data-stu-id="35bca-138">-State</span></span>
<span data-ttu-id="35bca-139">Nazwa województwa.</span><span class="sxs-lookup"><span data-stu-id="35bca-139">The name of the state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35bca-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35bca-140">CommonParameters</span></span>
<span data-ttu-id="35bca-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35bca-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35bca-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35bca-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35bca-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="35bca-143">INPUTS</span></span>

### <span data-ttu-id="35bca-144">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="35bca-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="35bca-145">System. String</span><span class="sxs-lookup"><span data-stu-id="35bca-145">System.String</span></span>

## <span data-ttu-id="35bca-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="35bca-146">OUTPUTS</span></span>

### <span data-ttu-id="35bca-147">Microsoft. Azure. Commands. Network. models. PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="35bca-147">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="35bca-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="35bca-148">NOTES</span></span>
<span data-ttu-id="35bca-149">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, Monitor sieci, dotarcie, raport</span><span class="sxs-lookup"><span data-stu-id="35bca-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="35bca-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="35bca-150">RELATED LINKS</span></span>

[<span data-ttu-id="35bca-151">Nowe — AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="35bca-151">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="35bca-152">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="35bca-152">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="35bca-153">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="35bca-153">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="35bca-154">Test — AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="35bca-154">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="35bca-155">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="35bca-155">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="35bca-156">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="35bca-156">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="35bca-157">Start — AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="35bca-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="35bca-158">Nowe — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="35bca-158">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="35bca-159">Nowe — AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="35bca-159">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="35bca-160">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="35bca-160">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="35bca-161">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="35bca-161">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="35bca-162">Zatrzymaj — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="35bca-162">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)
