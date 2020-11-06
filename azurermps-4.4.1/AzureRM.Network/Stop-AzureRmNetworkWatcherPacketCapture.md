---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 3f1206b79f8e80793106b1e294b591e21b9fb77d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527369"
---
# <span data-ttu-id="d63a3-101">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d63a3-101">Stop-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="d63a3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d63a3-102">SYNOPSIS</span></span>
<span data-ttu-id="d63a3-103">Zatrzymuje uruchomioną sesję przechwytywania pakietów.</span><span class="sxs-lookup"><span data-stu-id="d63a3-103">Stops a running packet capture session</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d63a3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d63a3-104">SYNTAX</span></span>

### <span data-ttu-id="d63a3-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d63a3-105">SetByResource (Default)</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d63a3-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="d63a3-106">SetByName</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d63a3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d63a3-107">DESCRIPTION</span></span>
<span data-ttu-id="d63a3-108">Stop-AzureRmNetworkWatcherPacketCapture zatrzymuje uruchomioną sesję przechwytywania pakietów.</span><span class="sxs-lookup"><span data-stu-id="d63a3-108">The Stop-AzureRmNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="d63a3-109">Po zatrzymaniu sesji plik przechwytywania pakietu zostanie przekazany do magazynu i/lub zapisany lokalnie na maszynie wirtualnej w zależności od konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="d63a3-109">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="d63a3-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d63a3-110">EXAMPLES</span></span>

### <span data-ttu-id="d63a3-111">---Przykład 1: zatrzymywanie sesji przechwytywania pakietu---</span><span class="sxs-lookup"><span data-stu-id="d63a3-111">--- Example 1: Stop a packet capture session ---</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="d63a3-112">W tym przykładzie zatrzymano uruchomioną sesję przechwytywania pakietów o nazwie "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="d63a3-112">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="d63a3-113">Po zatrzymaniu sesji plik przechwytywania pakietu zostanie przekazany do magazynu i/lub zapisany lokalnie na maszynie wirtualnej w zależności od konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="d63a3-113">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="d63a3-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d63a3-114">PARAMETERS</span></span>

### <span data-ttu-id="d63a3-115">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d63a3-115">-NetworkWatcher</span></span>
<span data-ttu-id="d63a3-116">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="d63a3-116">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d63a3-117">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d63a3-117">-NetworkWatcherName</span></span>
<span data-ttu-id="d63a3-118">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="d63a3-118">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d63a3-119">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="d63a3-119">-PacketCaptureName</span></span>
<span data-ttu-id="d63a3-120">Nazwa przechwytywania pakietu.</span><span class="sxs-lookup"><span data-stu-id="d63a3-120">The packet capture name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d63a3-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d63a3-121">-PassThru</span></span>
<span data-ttu-id="d63a3-122">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="d63a3-122">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d63a3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d63a3-123">-ResourceGroupName</span></span>
<span data-ttu-id="d63a3-124">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="d63a3-124">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d63a3-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d63a3-125">-Confirm</span></span>
<span data-ttu-id="d63a3-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d63a3-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d63a3-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d63a3-127">-WhatIf</span></span>
<span data-ttu-id="d63a3-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d63a3-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d63a3-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d63a3-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d63a3-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d63a3-130">-DefaultProfile</span></span>
<span data-ttu-id="d63a3-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d63a3-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d63a3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d63a3-132">CommonParameters</span></span>
<span data-ttu-id="d63a3-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d63a3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d63a3-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d63a3-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d63a3-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d63a3-135">INPUTS</span></span>

### <span data-ttu-id="d63a3-136">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d63a3-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="d63a3-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d63a3-137">System.String</span></span>

## <span data-ttu-id="d63a3-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d63a3-138">OUTPUTS</span></span>

### <span data-ttu-id="d63a3-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d63a3-139">System.Boolean</span></span>

## <span data-ttu-id="d63a3-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d63a3-140">NOTES</span></span>
<span data-ttu-id="d63a3-141">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, Monitor sieci, pakiet, przechwytywanie, ruch</span><span class="sxs-lookup"><span data-stu-id="d63a3-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="d63a3-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d63a3-142">RELATED LINKS</span></span>

[<span data-ttu-id="d63a3-143">Nowe — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d63a3-143">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d63a3-144">Nowe — AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d63a3-144">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="d63a3-145">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d63a3-145">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d63a3-146">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d63a3-146">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d63a3-147">Nowe — AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d63a3-147">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="d63a3-148">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d63a3-148">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="d63a3-149">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d63a3-149">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="d63a3-150">Test — AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d63a3-150">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="d63a3-151">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d63a3-151">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="d63a3-152">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d63a3-152">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d63a3-153">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d63a3-153">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="d63a3-154">Start — AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d63a3-154">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
