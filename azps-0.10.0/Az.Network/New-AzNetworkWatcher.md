---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcher.md
ms.openlocfilehash: cace33dd9831dcfcc01f2a57eefb5f28367966d9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890450"
---
# <span data-ttu-id="0a810-101">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0a810-101">New-AzNetworkWatcher</span></span>

## <span data-ttu-id="0a810-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0a810-102">SYNOPSIS</span></span>
<span data-ttu-id="0a810-103">Tworzy nowy zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="0a810-103">Creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="0a810-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0a810-104">SYNTAX</span></span>

```
New-AzNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a810-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0a810-105">DESCRIPTION</span></span>
<span data-ttu-id="0a810-106">Polecenie cmdlet New-AzNetworkWatcher tworzy nowy zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="0a810-106">The New-AzNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="0a810-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0a810-107">EXAMPLES</span></span>

### <span data-ttu-id="0a810-108">Przykład 1. Tworzenie obserwatora sieci</span><span class="sxs-lookup"><span data-stu-id="0a810-108">Example 1: Create a Network Watcher</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"7cf1f2fe-8445-4aa7-9bf5-c15347282c39"
Location          : westcentralus
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="0a810-109">W tym przykładzie utworzono nowy Monitor sieci w nowo utworzonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="0a810-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="0a810-110">Należy zauważyć, że dla każdego regionu można utworzyć tylko jeden Monitor sieci dla każdej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="0a810-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="0a810-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0a810-111">PARAMETERS</span></span>

### <span data-ttu-id="0a810-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a810-112">-DefaultProfile</span></span>
<span data-ttu-id="0a810-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0a810-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a810-114">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="0a810-114">-Location</span></span>
<span data-ttu-id="0a810-115">Pozycję.</span><span class="sxs-lookup"><span data-stu-id="0a810-115">Location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a810-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0a810-116">-Name</span></span>
<span data-ttu-id="0a810-117">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="0a810-117">The network watcher name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a810-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a810-118">-ResourceGroupName</span></span>
<span data-ttu-id="0a810-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0a810-119">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a810-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="0a810-120">-Tag</span></span>
<span data-ttu-id="0a810-121">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="0a810-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0a810-122">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="0a810-122">For example:</span></span>

<span data-ttu-id="0a810-123">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="0a810-123">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a810-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0a810-124">-Confirm</span></span>
<span data-ttu-id="0a810-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a810-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a810-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a810-126">-WhatIf</span></span>
<span data-ttu-id="0a810-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a810-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a810-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0a810-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a810-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a810-129">CommonParameters</span></span>
<span data-ttu-id="0a810-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a810-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a810-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a810-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a810-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0a810-132">INPUTS</span></span>

### <span data-ttu-id="0a810-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0a810-133">System.String</span></span>
<span data-ttu-id="0a810-134">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0a810-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0a810-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0a810-135">OUTPUTS</span></span>

### <span data-ttu-id="0a810-136">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0a810-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="0a810-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0a810-137">NOTES</span></span>
<span data-ttu-id="0a810-138">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, obserwator sieci</span><span class="sxs-lookup"><span data-stu-id="0a810-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="0a810-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0a810-139">RELATED LINKS</span></span>

[<span data-ttu-id="0a810-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0a810-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="0a810-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0a810-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="0a810-142">Nowe — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0a810-142">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0a810-143">Nowe — AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="0a810-143">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="0a810-144">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0a810-144">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0a810-145">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0a810-145">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0a810-146">Zatrzymaj — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0a810-146">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0a810-147">Test — AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="0a810-147">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="0a810-148">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="0a810-148">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="0a810-149">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="0a810-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="0a810-150">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="0a810-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="0a810-151">Start — AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="0a810-151">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
