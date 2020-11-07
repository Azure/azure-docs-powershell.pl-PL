---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: 805c8d31b075a39fa8ccc407024aa5a32a91fdb6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890718"
---
# <span data-ttu-id="379bc-101">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="379bc-101">Get-AzNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="379bc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="379bc-102">SYNOPSIS</span></span>
<span data-ttu-id="379bc-103">Wyświetla listę wszystkich dostępnych dostawców usług internetowych dla określonego regionu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="379bc-103">Lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="379bc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="379bc-104">SYNTAX</span></span>

### <span data-ttu-id="379bc-105">SetByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="379bc-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="379bc-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="379bc-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="379bc-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="379bc-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -ResourceId <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="379bc-108">Opis</span><span class="sxs-lookup"><span data-stu-id="379bc-108">DESCRIPTION</span></span>
<span data-ttu-id="379bc-109">Get-AzNetworkWatcherReachabilityProvidersList wyświetla listę wszystkich dostępnych dostawców usług internetowych dla określonego regionu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="379bc-109">The Get-AzNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="379bc-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="379bc-110">EXAMPLES</span></span>

### <span data-ttu-id="379bc-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="379bc-111">Example 1</span></span>
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

<span data-ttu-id="379bc-112">Wyświetla listę wszystkich dostępnych dostawców w Seattle, WA dla Azure Data Center w zachodnich Stanach Zjednoczonych.</span><span class="sxs-lookup"><span data-stu-id="379bc-112">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

## <span data-ttu-id="379bc-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="379bc-113">PARAMETERS</span></span>

### <span data-ttu-id="379bc-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="379bc-114">-AsJob</span></span>
<span data-ttu-id="379bc-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="379bc-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="379bc-116">-Miasto</span><span class="sxs-lookup"><span data-stu-id="379bc-116">-City</span></span>
<span data-ttu-id="379bc-117">Nazwa miasta.</span><span class="sxs-lookup"><span data-stu-id="379bc-117">The name of the city.</span></span>

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

### <span data-ttu-id="379bc-118">-Country</span><span class="sxs-lookup"><span data-stu-id="379bc-118">-Country</span></span>
<span data-ttu-id="379bc-119">Nazwa kraju.</span><span class="sxs-lookup"><span data-stu-id="379bc-119">The name of the country.</span></span>

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

### <span data-ttu-id="379bc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="379bc-120">-DefaultProfile</span></span>
<span data-ttu-id="379bc-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="379bc-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="379bc-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="379bc-122">-Location</span></span>
<span data-ttu-id="379bc-123">Opcjonalne regiony platformy Azure umożliwiające zakres kwerendy.</span><span class="sxs-lookup"><span data-stu-id="379bc-123">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="379bc-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="379bc-124">-NetworkWatcher</span></span>
<span data-ttu-id="379bc-125">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="379bc-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="379bc-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="379bc-126">-NetworkWatcherName</span></span>
<span data-ttu-id="379bc-127">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="379bc-127">The name of network watcher.</span></span>

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

### <span data-ttu-id="379bc-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="379bc-128">-ResourceGroupName</span></span>
<span data-ttu-id="379bc-129">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="379bc-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="379bc-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="379bc-130">-ResourceId</span></span>
<span data-ttu-id="379bc-131">Identyfikator zasobu obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="379bc-131">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="379bc-132">-State</span><span class="sxs-lookup"><span data-stu-id="379bc-132">-State</span></span>
<span data-ttu-id="379bc-133">Nazwa województwa.</span><span class="sxs-lookup"><span data-stu-id="379bc-133">The name of the state.</span></span>

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

### <span data-ttu-id="379bc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="379bc-134">CommonParameters</span></span>
<span data-ttu-id="379bc-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="379bc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="379bc-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="379bc-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="379bc-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="379bc-137">INPUTS</span></span>

### <span data-ttu-id="379bc-138">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="379bc-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="379bc-139">System. String.......... (System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="379bc-139">System.String System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="379bc-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="379bc-140">OUTPUTS</span></span>

### <span data-ttu-id="379bc-141">Microsoft. Azure. Commands. Network. models. PSAvailableProvidersList</span><span class="sxs-lookup"><span data-stu-id="379bc-141">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="379bc-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="379bc-142">NOTES</span></span>
<span data-ttu-id="379bc-143">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, Monitor sieci, następny, przeskok</span><span class="sxs-lookup"><span data-stu-id="379bc-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="379bc-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="379bc-144">RELATED LINKS</span></span>

[<span data-ttu-id="379bc-145">Nowe — AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="379bc-145">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="379bc-146">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="379bc-146">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="379bc-147">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="379bc-147">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="379bc-148">Test — AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="379bc-148">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="379bc-149">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="379bc-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="379bc-150">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="379bc-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="379bc-151">Start — AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="379bc-151">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="379bc-152">Nowe — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="379bc-152">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="379bc-153">Nowe — AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="379bc-153">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="379bc-154">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="379bc-154">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="379bc-155">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="379bc-155">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="379bc-156">Zatrzymaj — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="379bc-156">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)
