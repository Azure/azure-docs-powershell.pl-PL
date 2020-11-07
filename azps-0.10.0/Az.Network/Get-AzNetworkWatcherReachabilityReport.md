---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 6da0a36ee5e394008ea1d1de4a16f7982227ca06
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890714"
---
# <span data-ttu-id="8bb95-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="8bb95-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="8bb95-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8bb95-102">SYNOPSIS</span></span>
<span data-ttu-id="8bb95-103">Pobiera względny wynik opóźnienia dla dostawców usług internetowych z określonej lokalizacji na regiony platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8bb95-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="8bb95-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8bb95-104">SYNTAX</span></span>

### <span data-ttu-id="8bb95-105">SetByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8bb95-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8bb95-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="8bb95-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8bb95-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8bb95-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8bb95-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8bb95-108">DESCRIPTION</span></span>
<span data-ttu-id="8bb95-109">Get-AzNetworkWatcherReachabilityReport pobiera względny wynik opóźnienia dla dostawców usług internetowych z określonej lokalizacji do regionów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8bb95-109">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="8bb95-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8bb95-110">EXAMPLES</span></span>

### <span data-ttu-id="8bb95-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8bb95-111">Example 1</span></span>
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

<span data-ttu-id="8bb95-112">Pobiera względne opóźnienia w usłudze Azure Data Center w Stanach Zjednoczonych na zachód od 2017-10-10 do 2017-10-12 w stanie amerykańskim.</span><span class="sxs-lookup"><span data-stu-id="8bb95-112">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

## <span data-ttu-id="8bb95-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8bb95-113">PARAMETERS</span></span>

### <span data-ttu-id="8bb95-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8bb95-114">-AsJob</span></span>
<span data-ttu-id="8bb95-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="8bb95-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8bb95-116">-Miasto</span><span class="sxs-lookup"><span data-stu-id="8bb95-116">-City</span></span>
<span data-ttu-id="8bb95-117">Nazwa miasta.</span><span class="sxs-lookup"><span data-stu-id="8bb95-117">The name of the city.</span></span>

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

### <span data-ttu-id="8bb95-118">-Country</span><span class="sxs-lookup"><span data-stu-id="8bb95-118">-Country</span></span>
<span data-ttu-id="8bb95-119">Nazwa kraju.</span><span class="sxs-lookup"><span data-stu-id="8bb95-119">The name of the country.</span></span>

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

### <span data-ttu-id="8bb95-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bb95-120">-DefaultProfile</span></span>
<span data-ttu-id="8bb95-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8bb95-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8bb95-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="8bb95-122">-EndTime</span></span>
<span data-ttu-id="8bb95-123">Godzina zakończenia dla raportu o nieobecności w usłudze Azure.</span><span class="sxs-lookup"><span data-stu-id="8bb95-123">The end time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="8bb95-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="8bb95-124">-Location</span></span>
<span data-ttu-id="8bb95-125">Opcjonalne regiony platformy Azure umożliwiające zakres kwerendy.</span><span class="sxs-lookup"><span data-stu-id="8bb95-125">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="8bb95-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8bb95-126">-NetworkWatcher</span></span>
<span data-ttu-id="8bb95-127">Zasób obserwatora sieci</span><span class="sxs-lookup"><span data-stu-id="8bb95-127">The network watcher resource</span></span>

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

### <span data-ttu-id="8bb95-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="8bb95-128">-NetworkWatcherName</span></span>
<span data-ttu-id="8bb95-129">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="8bb95-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="8bb95-130">-Provider</span><span class="sxs-lookup"><span data-stu-id="8bb95-130">-Provider</span></span>
<span data-ttu-id="8bb95-131">Lista dostawców usług internetowych.</span><span class="sxs-lookup"><span data-stu-id="8bb95-131">List of Internet service providers.</span></span>

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

### <span data-ttu-id="8bb95-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bb95-132">-ResourceGroupName</span></span>
<span data-ttu-id="8bb95-133">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="8bb95-133">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="8bb95-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8bb95-134">-ResourceId</span></span>
<span data-ttu-id="8bb95-135">Identyfikator zasobu obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="8bb95-135">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="8bb95-136">-StartTime</span><span class="sxs-lookup"><span data-stu-id="8bb95-136">-StartTime</span></span>
<span data-ttu-id="8bb95-137">Godzina rozpoczęcia dla raportu o nieobecności w usłudze Azure.</span><span class="sxs-lookup"><span data-stu-id="8bb95-137">The start time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="8bb95-138">-State</span><span class="sxs-lookup"><span data-stu-id="8bb95-138">-State</span></span>
<span data-ttu-id="8bb95-139">Nazwa województwa.</span><span class="sxs-lookup"><span data-stu-id="8bb95-139">The name of the state.</span></span>

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

### <span data-ttu-id="8bb95-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bb95-140">CommonParameters</span></span>
<span data-ttu-id="8bb95-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bb95-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bb95-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bb95-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bb95-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8bb95-143">INPUTS</span></span>

### <span data-ttu-id="8bb95-144">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8bb95-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="8bb95-145">System. String</span><span class="sxs-lookup"><span data-stu-id="8bb95-145">System.String</span></span>

## <span data-ttu-id="8bb95-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8bb95-146">OUTPUTS</span></span>

### <span data-ttu-id="8bb95-147">Microsoft. Azure. Commands. Network. models. PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="8bb95-147">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="8bb95-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8bb95-148">NOTES</span></span>
<span data-ttu-id="8bb95-149">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, Monitor sieci, dotarcie, raport</span><span class="sxs-lookup"><span data-stu-id="8bb95-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="8bb95-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8bb95-150">RELATED LINKS</span></span>

[<span data-ttu-id="8bb95-151">Nowe — AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8bb95-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="8bb95-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8bb95-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="8bb95-153">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8bb95-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="8bb95-154">Test — AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="8bb95-154">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="8bb95-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="8bb95-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="8bb95-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="8bb95-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="8bb95-157">Start — AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="8bb95-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="8bb95-158">Nowe — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8bb95-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8bb95-159">Nowe — AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="8bb95-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="8bb95-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8bb95-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8bb95-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8bb95-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8bb95-162">Zatrzymaj — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8bb95-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)
