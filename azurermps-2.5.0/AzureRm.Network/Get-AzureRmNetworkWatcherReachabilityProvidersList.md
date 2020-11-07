---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherreachabilityproviderslist
schema: 2.0.0
ms.openlocfilehash: c5a681f8be210e76ecbf3bc965e7e9e9c108a94a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897606"
---
# <span data-ttu-id="7d5ea-101">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="7d5ea-101">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="7d5ea-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7d5ea-102">SYNOPSIS</span></span>
<span data-ttu-id="7d5ea-103">Wyświetla listę wszystkich dostępnych dostawców usług internetowych dla określonego regionu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7d5ea-103">Lists all available internet service providers for a specified Azure region.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d5ea-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7d5ea-104">SYNTAX</span></span>

### <span data-ttu-id="7d5ea-105">SetByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7d5ea-105">SetByName (Default)</span></span>
```
Get-AzureRmNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d5ea-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7d5ea-106">SetByResource</span></span>
```
Get-AzureRmNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d5ea-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7d5ea-107">SetByResourceId</span></span>
```
Get-AzureRmNetworkWatcherReachabilityProvidersList -ResourceId <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d5ea-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7d5ea-108">DESCRIPTION</span></span>
<span data-ttu-id="7d5ea-109">Get-AzureRmNetworkWatcherReachabilityProvidersList wyświetla listę wszystkich dostępnych dostawców usług internetowych dla określonego regionu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7d5ea-109">The Get-AzureRmNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="7d5ea-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7d5ea-110">EXAMPLES</span></span>

### <span data-ttu-id="7d5ea-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7d5ea-111">Example 1</span></span>
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

<span data-ttu-id="7d5ea-112">Wyświetla listę wszystkich dostępnych dostawców w Seattle, WA dla Azure Data Center w zachodnich Stanach Zjednoczonych.</span><span class="sxs-lookup"><span data-stu-id="7d5ea-112">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

## <span data-ttu-id="7d5ea-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7d5ea-113">PARAMETERS</span></span>

### <span data-ttu-id="7d5ea-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7d5ea-114">-AsJob</span></span>
<span data-ttu-id="7d5ea-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7d5ea-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7d5ea-116">-Miasto</span><span class="sxs-lookup"><span data-stu-id="7d5ea-116">-City</span></span>
<span data-ttu-id="7d5ea-117">Nazwa miasta.</span><span class="sxs-lookup"><span data-stu-id="7d5ea-117">The name of the city.</span></span>

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

### <span data-ttu-id="7d5ea-118">-Country</span><span class="sxs-lookup"><span data-stu-id="7d5ea-118">-Country</span></span>
<span data-ttu-id="7d5ea-119">Nazwa kraju.</span><span class="sxs-lookup"><span data-stu-id="7d5ea-119">The name of the country.</span></span>

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

### <span data-ttu-id="7d5ea-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d5ea-120">-DefaultProfile</span></span>
<span data-ttu-id="7d5ea-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7d5ea-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d5ea-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="7d5ea-122">-Location</span></span>
<span data-ttu-id="7d5ea-123">Opcjonalne regiony platformy Azure umożliwiające zakres kwerendy.</span><span class="sxs-lookup"><span data-stu-id="7d5ea-123">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="7d5ea-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7d5ea-124">-NetworkWatcher</span></span>
<span data-ttu-id="7d5ea-125">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="7d5ea-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="7d5ea-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="7d5ea-126">-NetworkWatcherName</span></span>
<span data-ttu-id="7d5ea-127">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="7d5ea-127">The name of network watcher.</span></span>

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

### <span data-ttu-id="7d5ea-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d5ea-128">-ResourceGroupName</span></span>
<span data-ttu-id="7d5ea-129">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="7d5ea-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="7d5ea-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d5ea-130">-ResourceId</span></span>
<span data-ttu-id="7d5ea-131">Identyfikator zasobu obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="7d5ea-131">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="7d5ea-132">-State</span><span class="sxs-lookup"><span data-stu-id="7d5ea-132">-State</span></span>
<span data-ttu-id="7d5ea-133">Nazwa województwa.</span><span class="sxs-lookup"><span data-stu-id="7d5ea-133">The name of the state.</span></span>

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

### <span data-ttu-id="7d5ea-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d5ea-134">CommonParameters</span></span>
<span data-ttu-id="7d5ea-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d5ea-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d5ea-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d5ea-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d5ea-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7d5ea-137">INPUTS</span></span>

### <span data-ttu-id="7d5ea-138">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7d5ea-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="7d5ea-139">System. String.......... (System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="7d5ea-139">System.String System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="7d5ea-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7d5ea-140">OUTPUTS</span></span>

### <span data-ttu-id="7d5ea-141">Microsoft. Azure. Commands. Network. models. PSAvailableProvidersList</span><span class="sxs-lookup"><span data-stu-id="7d5ea-141">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="7d5ea-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7d5ea-142">NOTES</span></span>
<span data-ttu-id="7d5ea-143">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, Monitor sieci, następny, przeskok</span><span class="sxs-lookup"><span data-stu-id="7d5ea-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="7d5ea-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7d5ea-144">RELATED LINKS</span></span>

[<span data-ttu-id="7d5ea-145">Nowe — AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7d5ea-145">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7d5ea-146">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7d5ea-146">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7d5ea-147">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7d5ea-147">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7d5ea-148">Test — AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="7d5ea-148">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="7d5ea-149">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="7d5ea-149">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="7d5ea-150">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="7d5ea-150">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="7d5ea-151">Start — AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="7d5ea-151">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="7d5ea-152">Nowe — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7d5ea-152">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7d5ea-153">Nowe — AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="7d5ea-153">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="7d5ea-154">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7d5ea-154">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7d5ea-155">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7d5ea-155">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7d5ea-156">Zatrzymaj — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7d5ea-156">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)
