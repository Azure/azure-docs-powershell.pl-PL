---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: c4d31de526132974defc6b3d28542e1ec8de4c67
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892669"
---
# <span data-ttu-id="96823-101">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="96823-101">Stop-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="96823-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="96823-102">SYNOPSIS</span></span>
<span data-ttu-id="96823-103">Zatrzymuje uruchomioną sesję przechwytywania pakietów.</span><span class="sxs-lookup"><span data-stu-id="96823-103">Stops a running packet capture session</span></span>

## <span data-ttu-id="96823-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="96823-104">SYNTAX</span></span>

### <span data-ttu-id="96823-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="96823-105">SetByResource (Default)</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96823-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="96823-106">SetByName</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96823-107">Opis</span><span class="sxs-lookup"><span data-stu-id="96823-107">DESCRIPTION</span></span>
<span data-ttu-id="96823-108">Stop-AzNetworkWatcherPacketCapture zatrzymuje uruchomioną sesję przechwytywania pakietów.</span><span class="sxs-lookup"><span data-stu-id="96823-108">The Stop-AzNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="96823-109">Po zatrzymaniu sesji plik przechwytywania pakietu zostanie przekazany do magazynu i/lub zapisany lokalnie na maszynie wirtualnej w zależności od konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="96823-109">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="96823-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="96823-110">EXAMPLES</span></span>

### <span data-ttu-id="96823-111">---Przykład 1: zatrzymywanie sesji przechwytywania pakietu---</span><span class="sxs-lookup"><span data-stu-id="96823-111">--- Example 1: Stop a packet capture session ---</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="96823-112">W tym przykładzie zatrzymano uruchomioną sesję przechwytywania pakietów o nazwie "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="96823-112">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="96823-113">Po zatrzymaniu sesji plik przechwytywania pakietu zostanie przekazany do magazynu i/lub zapisany lokalnie na maszynie wirtualnej w zależności od konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="96823-113">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="96823-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="96823-114">PARAMETERS</span></span>

### <span data-ttu-id="96823-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="96823-115">-AsJob</span></span>
<span data-ttu-id="96823-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="96823-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="96823-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96823-117">-DefaultProfile</span></span>
<span data-ttu-id="96823-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="96823-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96823-119">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="96823-119">-NetworkWatcher</span></span>
<span data-ttu-id="96823-120">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="96823-120">The network watcher resource.</span></span>

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

### <span data-ttu-id="96823-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="96823-121">-NetworkWatcherName</span></span>
<span data-ttu-id="96823-122">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="96823-122">The name of network watcher.</span></span>

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

### <span data-ttu-id="96823-123">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="96823-123">-PacketCaptureName</span></span>
<span data-ttu-id="96823-124">Nazwa przechwytywania pakietu.</span><span class="sxs-lookup"><span data-stu-id="96823-124">The packet capture name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96823-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="96823-125">-PassThru</span></span>
<span data-ttu-id="96823-126">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="96823-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="96823-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96823-127">-ResourceGroupName</span></span>
<span data-ttu-id="96823-128">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="96823-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="96823-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="96823-129">-Confirm</span></span>
<span data-ttu-id="96823-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96823-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96823-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96823-131">-WhatIf</span></span>
<span data-ttu-id="96823-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96823-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96823-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="96823-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96823-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96823-134">CommonParameters</span></span>
<span data-ttu-id="96823-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96823-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96823-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96823-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96823-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="96823-137">INPUTS</span></span>

### <span data-ttu-id="96823-138">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="96823-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="96823-139">System. String</span><span class="sxs-lookup"><span data-stu-id="96823-139">System.String</span></span>

## <span data-ttu-id="96823-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="96823-140">OUTPUTS</span></span>

### <span data-ttu-id="96823-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="96823-141">System.Boolean</span></span>

## <span data-ttu-id="96823-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="96823-142">NOTES</span></span>
<span data-ttu-id="96823-143">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, Monitor sieci, pakiet, przechwytywanie, ruch</span><span class="sxs-lookup"><span data-stu-id="96823-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="96823-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="96823-144">RELATED LINKS</span></span>

[<span data-ttu-id="96823-145">Nowe — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="96823-145">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="96823-146">Nowe — AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="96823-146">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="96823-147">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="96823-147">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="96823-148">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="96823-148">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="96823-149">Nowe — AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="96823-149">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="96823-150">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="96823-150">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="96823-151">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="96823-151">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="96823-152">Test — AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="96823-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="96823-153">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="96823-153">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="96823-154">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="96823-154">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="96823-155">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="96823-155">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="96823-156">Start — AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="96823-156">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
