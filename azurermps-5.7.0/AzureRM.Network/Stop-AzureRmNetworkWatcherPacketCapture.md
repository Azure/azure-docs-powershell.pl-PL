---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermnetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 43dc48aaa58f086e6d05f45a81096612d3177a17
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718887"
---
# <span data-ttu-id="51b3e-101">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="51b3e-101">Stop-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="51b3e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="51b3e-102">SYNOPSIS</span></span>
<span data-ttu-id="51b3e-103">Zatrzymuje uruchomioną sesję przechwytywania pakietów.</span><span class="sxs-lookup"><span data-stu-id="51b3e-103">Stops a running packet capture session</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51b3e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="51b3e-104">SYNTAX</span></span>

### <span data-ttu-id="51b3e-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="51b3e-105">SetByResource (Default)</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51b3e-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="51b3e-106">SetByName</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51b3e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="51b3e-107">DESCRIPTION</span></span>
<span data-ttu-id="51b3e-108">Stop-AzureRmNetworkWatcherPacketCapture zatrzymuje uruchomioną sesję przechwytywania pakietów.</span><span class="sxs-lookup"><span data-stu-id="51b3e-108">The Stop-AzureRmNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="51b3e-109">Po zatrzymaniu sesji plik przechwytywania pakietu zostanie przekazany do magazynu i/lub zapisany lokalnie na maszynie wirtualnej w zależności od konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="51b3e-109">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="51b3e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="51b3e-110">EXAMPLES</span></span>

### <span data-ttu-id="51b3e-111">---Przykład 1: zatrzymywanie sesji przechwytywania pakietu---</span><span class="sxs-lookup"><span data-stu-id="51b3e-111">--- Example 1: Stop a packet capture session ---</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="51b3e-112">W tym przykładzie zatrzymano uruchomioną sesję przechwytywania pakietów o nazwie "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="51b3e-112">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="51b3e-113">Po zatrzymaniu sesji plik przechwytywania pakietu zostanie przekazany do magazynu i/lub zapisany lokalnie na maszynie wirtualnej w zależności od konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="51b3e-113">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="51b3e-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="51b3e-114">PARAMETERS</span></span>

### <span data-ttu-id="51b3e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="51b3e-115">-AsJob</span></span>
<span data-ttu-id="51b3e-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="51b3e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="51b3e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51b3e-117">-DefaultProfile</span></span>
<span data-ttu-id="51b3e-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="51b3e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51b3e-119">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="51b3e-119">-NetworkWatcher</span></span>
<span data-ttu-id="51b3e-120">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="51b3e-120">The network watcher resource.</span></span>

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

### <span data-ttu-id="51b3e-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="51b3e-121">-NetworkWatcherName</span></span>
<span data-ttu-id="51b3e-122">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="51b3e-122">The name of network watcher.</span></span>

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

### <span data-ttu-id="51b3e-123">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="51b3e-123">-PacketCaptureName</span></span>
<span data-ttu-id="51b3e-124">Nazwa przechwytywania pakietu.</span><span class="sxs-lookup"><span data-stu-id="51b3e-124">The packet capture name.</span></span>

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

### <span data-ttu-id="51b3e-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51b3e-125">-PassThru</span></span>
<span data-ttu-id="51b3e-126">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="51b3e-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="51b3e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51b3e-127">-ResourceGroupName</span></span>
<span data-ttu-id="51b3e-128">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="51b3e-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="51b3e-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="51b3e-129">-Confirm</span></span>
<span data-ttu-id="51b3e-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51b3e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51b3e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51b3e-131">-WhatIf</span></span>
<span data-ttu-id="51b3e-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51b3e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51b3e-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="51b3e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51b3e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51b3e-134">CommonParameters</span></span>
<span data-ttu-id="51b3e-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51b3e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51b3e-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51b3e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51b3e-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="51b3e-137">INPUTS</span></span>

### <span data-ttu-id="51b3e-138">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="51b3e-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="51b3e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="51b3e-139">System.String</span></span>

## <span data-ttu-id="51b3e-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="51b3e-140">OUTPUTS</span></span>

### <span data-ttu-id="51b3e-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="51b3e-141">System.Boolean</span></span>

## <span data-ttu-id="51b3e-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="51b3e-142">NOTES</span></span>
<span data-ttu-id="51b3e-143">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, Monitor sieci, pakiet, przechwytywanie, ruch</span><span class="sxs-lookup"><span data-stu-id="51b3e-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="51b3e-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="51b3e-144">RELATED LINKS</span></span>

[<span data-ttu-id="51b3e-145">Nowe — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="51b3e-145">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="51b3e-146">Nowe — AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="51b3e-146">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="51b3e-147">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="51b3e-147">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="51b3e-148">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="51b3e-148">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="51b3e-149">Nowe — AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="51b3e-149">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="51b3e-150">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="51b3e-150">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="51b3e-151">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="51b3e-151">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="51b3e-152">Test — AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="51b3e-152">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="51b3e-153">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="51b3e-153">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="51b3e-154">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="51b3e-154">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="51b3e-155">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="51b3e-155">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="51b3e-156">Start — AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="51b3e-156">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
