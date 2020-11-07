---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherreachabilityreport
schema: 2.0.0
ms.openlocfilehash: 75335fb09bb8f4187879ab69ab138952cc873993
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899301"
---
# <span data-ttu-id="3309a-101">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="3309a-101">Get-AzureRMNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="3309a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3309a-102">SYNOPSIS</span></span>
<span data-ttu-id="3309a-103">Pobiera względny wynik opóźnienia dla dostawców usług internetowych z określonej lokalizacji na regiony platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3309a-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3309a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3309a-104">SYNTAX</span></span>

### <span data-ttu-id="3309a-105">SetByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3309a-105">SetByName (Default)</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3309a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="3309a-106">SetByResource</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3309a-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3309a-107">SetByResourceId</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -ResourceId <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3309a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3309a-108">DESCRIPTION</span></span>
<span data-ttu-id="3309a-109">Get-AzureRmNetworkWatcherReachabilityReport pobiera względny wynik opóźnienia dla dostawców usług internetowych z określonej lokalizacji do regionów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3309a-109">The Get-AzureRmNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="3309a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3309a-110">EXAMPLES</span></span>

### <span data-ttu-id="3309a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3309a-111">Example 1</span></span>
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

<span data-ttu-id="3309a-112">Pobiera względne opóźnienia w usłudze Azure Data Center w Stanach Zjednoczonych na zachód od 2017-10-10 do 2017-10-12 w stanie amerykańskim.</span><span class="sxs-lookup"><span data-stu-id="3309a-112">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

## <span data-ttu-id="3309a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3309a-113">PARAMETERS</span></span>

### <span data-ttu-id="3309a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3309a-114">-AsJob</span></span>
<span data-ttu-id="3309a-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="3309a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3309a-116">-Miasto</span><span class="sxs-lookup"><span data-stu-id="3309a-116">-City</span></span>
<span data-ttu-id="3309a-117">Nazwa miasta.</span><span class="sxs-lookup"><span data-stu-id="3309a-117">The name of the city.</span></span>

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

### <span data-ttu-id="3309a-118">-Country</span><span class="sxs-lookup"><span data-stu-id="3309a-118">-Country</span></span>
<span data-ttu-id="3309a-119">Nazwa kraju.</span><span class="sxs-lookup"><span data-stu-id="3309a-119">The name of the country.</span></span>

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

### <span data-ttu-id="3309a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3309a-120">-DefaultProfile</span></span>
<span data-ttu-id="3309a-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3309a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3309a-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="3309a-122">-EndTime</span></span>
<span data-ttu-id="3309a-123">Godzina zakończenia dla raportu o nieobecności w usłudze Azure.</span><span class="sxs-lookup"><span data-stu-id="3309a-123">The end time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="3309a-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3309a-124">-Location</span></span>
<span data-ttu-id="3309a-125">Opcjonalne regiony platformy Azure umożliwiające zakres kwerendy.</span><span class="sxs-lookup"><span data-stu-id="3309a-125">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="3309a-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3309a-126">-NetworkWatcher</span></span>
<span data-ttu-id="3309a-127">Zasób obserwatora sieci</span><span class="sxs-lookup"><span data-stu-id="3309a-127">The network watcher resource</span></span>

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

### <span data-ttu-id="3309a-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="3309a-128">-NetworkWatcherName</span></span>
<span data-ttu-id="3309a-129">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="3309a-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="3309a-130">-Provider</span><span class="sxs-lookup"><span data-stu-id="3309a-130">-Provider</span></span>
<span data-ttu-id="3309a-131">Lista dostawców usług internetowych.</span><span class="sxs-lookup"><span data-stu-id="3309a-131">List of Internet service providers.</span></span>

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

### <span data-ttu-id="3309a-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3309a-132">-ResourceGroupName</span></span>
<span data-ttu-id="3309a-133">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="3309a-133">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="3309a-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3309a-134">-ResourceId</span></span>
<span data-ttu-id="3309a-135">Identyfikator zasobu obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="3309a-135">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="3309a-136">-StartTime</span><span class="sxs-lookup"><span data-stu-id="3309a-136">-StartTime</span></span>
<span data-ttu-id="3309a-137">Godzina rozpoczęcia dla raportu o nieobecności w usłudze Azure.</span><span class="sxs-lookup"><span data-stu-id="3309a-137">The start time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="3309a-138">-State</span><span class="sxs-lookup"><span data-stu-id="3309a-138">-State</span></span>
<span data-ttu-id="3309a-139">Nazwa województwa.</span><span class="sxs-lookup"><span data-stu-id="3309a-139">The name of the state.</span></span>

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

### <span data-ttu-id="3309a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3309a-140">CommonParameters</span></span>
<span data-ttu-id="3309a-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3309a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3309a-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3309a-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3309a-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3309a-143">INPUTS</span></span>

### <span data-ttu-id="3309a-144">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3309a-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="3309a-145">System. String</span><span class="sxs-lookup"><span data-stu-id="3309a-145">System.String</span></span>

## <span data-ttu-id="3309a-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3309a-146">OUTPUTS</span></span>

### <span data-ttu-id="3309a-147">Microsoft. Azure. Commands. Network. models. PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="3309a-147">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="3309a-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3309a-148">NOTES</span></span>
<span data-ttu-id="3309a-149">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, Monitor sieci, dotarcie, raport</span><span class="sxs-lookup"><span data-stu-id="3309a-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="3309a-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3309a-150">RELATED LINKS</span></span>

[<span data-ttu-id="3309a-151">Nowe — AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3309a-151">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="3309a-152">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3309a-152">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="3309a-153">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3309a-153">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="3309a-154">Test — AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="3309a-154">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="3309a-155">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="3309a-155">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="3309a-156">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="3309a-156">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="3309a-157">Start — AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="3309a-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="3309a-158">Nowe — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3309a-158">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3309a-159">Nowe — AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="3309a-159">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="3309a-160">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3309a-160">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3309a-161">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3309a-161">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3309a-162">Zatrzymaj — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3309a-162">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)
