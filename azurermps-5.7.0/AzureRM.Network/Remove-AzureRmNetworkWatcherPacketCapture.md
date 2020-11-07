---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 034cca094bf6dd7d3911e3e705e03888f0ea10ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552219"
---
# <span data-ttu-id="54fe2-101">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="54fe2-101">Remove-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="54fe2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="54fe2-102">SYNOPSIS</span></span>
<span data-ttu-id="54fe2-103">Usuwa zasób przechwytywania pakietu.</span><span class="sxs-lookup"><span data-stu-id="54fe2-103">Removes a packet capture resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54fe2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="54fe2-104">SYNTAX</span></span>

### <span data-ttu-id="54fe2-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="54fe2-105">SetByResource (Default)</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54fe2-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="54fe2-106">SetByName</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54fe2-107">Opis</span><span class="sxs-lookup"><span data-stu-id="54fe2-107">DESCRIPTION</span></span>
<span data-ttu-id="54fe2-108">Remove-AzureRmNetworkWatcherPacketCapture usuwa zasób przechwytywania pakietu.</span><span class="sxs-lookup"><span data-stu-id="54fe2-108">The Remove-AzureRmNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="54fe2-109">Zaleca się nawiązanie połączenia Stop-AzureRmNetworkWatcherPacketCapture przed wywołaniem funkcji Remove-AzureRmNetworkWatcherPacketCapture.</span><span class="sxs-lookup"><span data-stu-id="54fe2-109">It is recommended to call Stop-AzureRmNetworkWatcherPacketCapture before calling Remove-AzureRmNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="54fe2-110">Jeśli sesja przechwytywania pakietów jest uruchomiona, gdy Remove-AzureRmNetworkWatcherPacketCapture jest nazywany przechwytywanie pakietów, być może nie zostanie zapisana.</span><span class="sxs-lookup"><span data-stu-id="54fe2-110">If the packet capture session is running when Remove-AzureRmNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="54fe2-111">Jeśli sesja zostanie zatrzymana przed usunięciem pliku Cap zawierającego przechwycone dane, nie zostanie usunięty.</span><span class="sxs-lookup"><span data-stu-id="54fe2-111">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="54fe2-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="54fe2-112">EXAMPLES</span></span>

### <span data-ttu-id="54fe2-113">---Przykład 1: usuwanie sesji przechwytywania pakietów —</span><span class="sxs-lookup"><span data-stu-id="54fe2-113">--- Example 1: Remove a packet capture session --</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="54fe2-114">W tym przykładzie została usunięta istniejąca sesja przechwytywania pakietu o nazwie "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="54fe2-114">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="54fe2-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="54fe2-115">PARAMETERS</span></span>

### <span data-ttu-id="54fe2-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="54fe2-116">-AsJob</span></span>
<span data-ttu-id="54fe2-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="54fe2-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="54fe2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54fe2-118">-DefaultProfile</span></span>
<span data-ttu-id="54fe2-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="54fe2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54fe2-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="54fe2-120">-NetworkWatcher</span></span>
<span data-ttu-id="54fe2-121">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="54fe2-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="54fe2-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="54fe2-122">-NetworkWatcherName</span></span>
<span data-ttu-id="54fe2-123">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="54fe2-123">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54fe2-124">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="54fe2-124">-PacketCaptureName</span></span>
<span data-ttu-id="54fe2-125">Nazwa przechwytywania pakietu.</span><span class="sxs-lookup"><span data-stu-id="54fe2-125">The packet capture name.</span></span>

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

### <span data-ttu-id="54fe2-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="54fe2-126">-PassThru</span></span>
<span data-ttu-id="54fe2-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="54fe2-127">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54fe2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54fe2-128">-ResourceGroupName</span></span>
<span data-ttu-id="54fe2-129">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="54fe2-129">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54fe2-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="54fe2-130">-Confirm</span></span>
<span data-ttu-id="54fe2-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54fe2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54fe2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54fe2-132">-WhatIf</span></span>
<span data-ttu-id="54fe2-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54fe2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54fe2-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="54fe2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54fe2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54fe2-135">CommonParameters</span></span>
<span data-ttu-id="54fe2-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54fe2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54fe2-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54fe2-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54fe2-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="54fe2-138">INPUTS</span></span>

### <span data-ttu-id="54fe2-139">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="54fe2-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="54fe2-140">System. String</span><span class="sxs-lookup"><span data-stu-id="54fe2-140">System.String</span></span>

## <span data-ttu-id="54fe2-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="54fe2-141">OUTPUTS</span></span>

### <span data-ttu-id="54fe2-142">System. Object</span><span class="sxs-lookup"><span data-stu-id="54fe2-142">System.Object</span></span>

## <span data-ttu-id="54fe2-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="54fe2-143">NOTES</span></span>
<span data-ttu-id="54fe2-144">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, Monitor sieci, pakiet, przechwytywanie, ruch, usuwanie</span><span class="sxs-lookup"><span data-stu-id="54fe2-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="54fe2-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="54fe2-145">RELATED LINKS</span></span>

[<span data-ttu-id="54fe2-146">Nowe — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="54fe2-146">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="54fe2-147">Nowe — AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="54fe2-147">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="54fe2-148">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="54fe2-148">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="54fe2-149">Zatrzymaj — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="54fe2-149">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="54fe2-150">Nowe — AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="54fe2-150">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="54fe2-151">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="54fe2-151">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="54fe2-152">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="54fe2-152">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="54fe2-153">Test — AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="54fe2-153">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="54fe2-154">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="54fe2-154">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="54fe2-155">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="54fe2-155">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="54fe2-156">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="54fe2-156">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="54fe2-157">Start — AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="54fe2-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)