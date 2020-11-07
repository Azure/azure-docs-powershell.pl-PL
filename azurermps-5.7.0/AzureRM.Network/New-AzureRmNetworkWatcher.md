---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcher.md
ms.openlocfilehash: e1e0714c070c47d4be2cff0893a4428bdf0949c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718906"
---
# <span data-ttu-id="dda1e-101">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dda1e-101">New-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="dda1e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dda1e-102">SYNOPSIS</span></span>
<span data-ttu-id="dda1e-103">Tworzy nowy zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="dda1e-103">Creates a new Network Watcher resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dda1e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dda1e-104">SYNTAX</span></span>

```
New-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dda1e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dda1e-105">DESCRIPTION</span></span>
<span data-ttu-id="dda1e-106">Polecenie cmdlet New-AzureRmNetworkWatcher tworzy nowy zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="dda1e-106">The New-AzureRmNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="dda1e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dda1e-107">EXAMPLES</span></span>

### <span data-ttu-id="dda1e-108">Przykład 1. Tworzenie obserwatora sieci</span><span class="sxs-lookup"><span data-stu-id="dda1e-108">Example 1: Create a Network Watcher</span></span>
```
New-AzureRmResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"7cf1f2fe-8445-4aa7-9bf5-c15347282c39"
Location          : westcentralus
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="dda1e-109">W tym przykładzie utworzono nowy Monitor sieci w nowo utworzonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="dda1e-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="dda1e-110">Należy zauważyć, że dla każdego regionu można utworzyć tylko jeden Monitor sieci dla każdej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="dda1e-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="dda1e-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dda1e-111">PARAMETERS</span></span>

### <span data-ttu-id="dda1e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dda1e-112">-DefaultProfile</span></span>
<span data-ttu-id="dda1e-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dda1e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dda1e-114">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="dda1e-114">-Location</span></span>
<span data-ttu-id="dda1e-115">Pozycję.</span><span class="sxs-lookup"><span data-stu-id="dda1e-115">Location.</span></span>

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

### <span data-ttu-id="dda1e-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dda1e-116">-Name</span></span>
<span data-ttu-id="dda1e-117">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="dda1e-117">The network watcher name.</span></span>

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

### <span data-ttu-id="dda1e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dda1e-118">-ResourceGroupName</span></span>
<span data-ttu-id="dda1e-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="dda1e-119">The resource group name.</span></span>

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

### <span data-ttu-id="dda1e-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="dda1e-120">-Tag</span></span>
<span data-ttu-id="dda1e-121">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="dda1e-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="dda1e-122">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="dda1e-122">For example:</span></span>

<span data-ttu-id="dda1e-123">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="dda1e-123">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="dda1e-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dda1e-124">-Confirm</span></span>
<span data-ttu-id="dda1e-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dda1e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dda1e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dda1e-126">-WhatIf</span></span>
<span data-ttu-id="dda1e-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dda1e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dda1e-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dda1e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dda1e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dda1e-129">CommonParameters</span></span>
<span data-ttu-id="dda1e-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dda1e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dda1e-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dda1e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dda1e-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dda1e-132">INPUTS</span></span>

### <span data-ttu-id="dda1e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="dda1e-133">System.String</span></span>
<span data-ttu-id="dda1e-134">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="dda1e-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="dda1e-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dda1e-135">OUTPUTS</span></span>

### <span data-ttu-id="dda1e-136">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dda1e-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="dda1e-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dda1e-137">NOTES</span></span>
<span data-ttu-id="dda1e-138">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, obserwator sieci</span><span class="sxs-lookup"><span data-stu-id="dda1e-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="dda1e-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dda1e-139">RELATED LINKS</span></span>

[<span data-ttu-id="dda1e-140">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dda1e-140">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="dda1e-141">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dda1e-141">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="dda1e-142">Nowe — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dda1e-142">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dda1e-143">Nowe — AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="dda1e-143">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="dda1e-144">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dda1e-144">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dda1e-145">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dda1e-145">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dda1e-146">Zatrzymaj — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dda1e-146">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dda1e-147">Test — AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="dda1e-147">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="dda1e-148">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="dda1e-148">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="dda1e-149">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="dda1e-149">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="dda1e-150">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="dda1e-150">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="dda1e-151">Start — AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="dda1e-151">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
