---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: b3095aace7fa8e1959e51ef64aa92b6d2bcaffba
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892946"
---
# <span data-ttu-id="a9643-101">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a9643-101">Remove-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="a9643-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a9643-102">SYNOPSIS</span></span>
<span data-ttu-id="a9643-103">Usuwa zasób przechwytywania pakietu.</span><span class="sxs-lookup"><span data-stu-id="a9643-103">Removes a packet capture resource.</span></span>

## <span data-ttu-id="a9643-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a9643-104">SYNTAX</span></span>

### <span data-ttu-id="a9643-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a9643-105">SetByResource (Default)</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9643-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="a9643-106">SetByName</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9643-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a9643-107">DESCRIPTION</span></span>
<span data-ttu-id="a9643-108">Remove-AzNetworkWatcherPacketCapture usuwa zasób przechwytywania pakietu.</span><span class="sxs-lookup"><span data-stu-id="a9643-108">The Remove-AzNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="a9643-109">Zaleca się nawiązanie połączenia Stop-AzNetworkWatcherPacketCapture przed wywołaniem funkcji Remove-AzNetworkWatcherPacketCapture.</span><span class="sxs-lookup"><span data-stu-id="a9643-109">It is recommended to call Stop-AzNetworkWatcherPacketCapture before calling Remove-AzNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="a9643-110">Jeśli sesja przechwytywania pakietów jest uruchomiona, gdy Remove-AzNetworkWatcherPacketCapture jest nazywany przechwytywanie pakietów, być może nie zostanie zapisana.</span><span class="sxs-lookup"><span data-stu-id="a9643-110">If the packet capture session is running when Remove-AzNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="a9643-111">Jeśli sesja zostanie zatrzymana przed usunięciem pliku Cap zawierającego przechwycone dane, nie zostanie usunięty.</span><span class="sxs-lookup"><span data-stu-id="a9643-111">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="a9643-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a9643-112">EXAMPLES</span></span>

### <span data-ttu-id="a9643-113">---Przykład 1: usuwanie sesji przechwytywania pakietów —</span><span class="sxs-lookup"><span data-stu-id="a9643-113">--- Example 1: Remove a packet capture session --</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="a9643-114">W tym przykładzie została usunięta istniejąca sesja przechwytywania pakietu o nazwie "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="a9643-114">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="a9643-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a9643-115">PARAMETERS</span></span>

### <span data-ttu-id="a9643-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a9643-116">-AsJob</span></span>
<span data-ttu-id="a9643-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a9643-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a9643-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9643-118">-DefaultProfile</span></span>
<span data-ttu-id="a9643-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a9643-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9643-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a9643-120">-NetworkWatcher</span></span>
<span data-ttu-id="a9643-121">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="a9643-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="a9643-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="a9643-122">-NetworkWatcherName</span></span>
<span data-ttu-id="a9643-123">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="a9643-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="a9643-124">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="a9643-124">-PacketCaptureName</span></span>
<span data-ttu-id="a9643-125">Nazwa przechwytywania pakietu.</span><span class="sxs-lookup"><span data-stu-id="a9643-125">The packet capture name.</span></span>

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

### <span data-ttu-id="a9643-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a9643-126">-PassThru</span></span>
<span data-ttu-id="a9643-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="a9643-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a9643-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9643-128">-ResourceGroupName</span></span>
<span data-ttu-id="a9643-129">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="a9643-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="a9643-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a9643-130">-Confirm</span></span>
<span data-ttu-id="a9643-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9643-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9643-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9643-132">-WhatIf</span></span>
<span data-ttu-id="a9643-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9643-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9643-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a9643-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9643-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9643-135">CommonParameters</span></span>
<span data-ttu-id="a9643-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9643-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9643-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9643-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9643-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9643-138">INPUTS</span></span>

### <span data-ttu-id="a9643-139">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a9643-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="a9643-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a9643-140">System.String</span></span>

## <span data-ttu-id="a9643-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a9643-141">OUTPUTS</span></span>

### <span data-ttu-id="a9643-142">System. Object</span><span class="sxs-lookup"><span data-stu-id="a9643-142">System.Object</span></span>

## <span data-ttu-id="a9643-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a9643-143">NOTES</span></span>
<span data-ttu-id="a9643-144">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, Monitor sieci, pakiet, przechwytywanie, ruch, usuwanie</span><span class="sxs-lookup"><span data-stu-id="a9643-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="a9643-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a9643-145">RELATED LINKS</span></span>

[<span data-ttu-id="a9643-146">Nowe — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a9643-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a9643-147">Nowe — AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="a9643-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="a9643-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a9643-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a9643-149">Zatrzymaj — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a9643-149">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a9643-150">Nowe — AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a9643-150">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="a9643-151">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a9643-151">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="a9643-152">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a9643-152">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="a9643-153">Test — AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="a9643-153">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="a9643-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="a9643-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="a9643-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="a9643-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="a9643-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="a9643-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="a9643-157">Start — AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="a9643-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
