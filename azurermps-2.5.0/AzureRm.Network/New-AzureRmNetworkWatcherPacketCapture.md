---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcherpacketcapture
schema: 2.0.0
ms.openlocfilehash: f91dc3942241237ddf3841d276ea442361d89987
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898703"
---
# <span data-ttu-id="d7457-101">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d7457-101">New-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="d7457-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d7457-102">SYNOPSIS</span></span>
<span data-ttu-id="d7457-103">Tworzy nowy zasób przechwytywania pakietów i rozpoczyna sesję przechwytywania pakietów na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d7457-103">Creates a new packet capture resource and starts a packet capture session on a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7457-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d7457-104">SYNTAX</span></span>

### <span data-ttu-id="d7457-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d7457-105">SetByResource (Default)</span></span>
```
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7457-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="d7457-106">SetByName</span></span>
```
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> -TargetVirtualMachineId <String> [-StorageAccountId <String>]
 [-StoragePath <String>] [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>]
 [-TotalBytesPerSession <Int32>] [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7457-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d7457-107">DESCRIPTION</span></span>
<span data-ttu-id="d7457-108">Polecenie cmdlet New-AzureRmNetworkWatcherPacketCapture tworzy nowy zasób przechwytywania pakietów i rozpoczyna sesję przechwytywania pakietów na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d7457-108">The New-AzureRmNetworkWatcherPacketCapture cmdlet creates a new packet capture resource and starts a packet capture session on a VM.</span></span>
<span data-ttu-id="d7457-109">Długość sesji przechwytywania pakietów można skonfigurować za pośrednictwem ograniczenia czasu lub ograniczenia rozmiaru.</span><span class="sxs-lookup"><span data-stu-id="d7457-109">The length of the Packet Capture sessions can be configured via a time constraint or a size constraint.</span></span> <span data-ttu-id="d7457-110">Można również skonfigurować ilość danych przechwyconych dla każdego pakietu.</span><span class="sxs-lookup"><span data-stu-id="d7457-110">The amount of data captured for each packet can also be configured.</span></span>
<span data-ttu-id="d7457-111">Filtry można stosować do danej sesji przechwytywania pakietów, co umożliwia dostosowanie typu przechwyconych pakietów.</span><span class="sxs-lookup"><span data-stu-id="d7457-111">Filters can be applied to a given packet capture session, allowing you to customize the type of packets captured.</span></span> <span data-ttu-id="d7457-112">Filtry mogą ograniczać pakiety na lokalnych i zdalnych adresach IP & zakres adresów, porty lokalne i zdalne & zakresy portów oraz protokół na poziomie sesji do przechwycenia.</span><span class="sxs-lookup"><span data-stu-id="d7457-112">Filters can restrict packets on local and remote IP addresses & address ranges, local and remote ports & port ranges, and the session level protocol to be captured.</span></span> <span data-ttu-id="d7457-113">Filtry są składane i można zastosować wiele filtrów w celu zapewnienia szczegółowości funkcji przechwytywania.</span><span class="sxs-lookup"><span data-stu-id="d7457-113">Filters are composable, and multiple filters can be applied to provide you with granularity of capture.</span></span>

## <span data-ttu-id="d7457-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d7457-114">EXAMPLES</span></span>

### <span data-ttu-id="d7457-115">---Przykład 1: Tworzenie przechwytywania pakietów z wieloma filtrami---</span><span class="sxs-lookup"><span data-stu-id="d7457-115">--- Example 1: Create a Packet Capture with multiple filters ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filter $filter1, $filter2
```

<span data-ttu-id="d7457-116">W tym przykładzie tworzymy przechwycony pakiet o nazwie "PacketCaptureTest" z wieloma filtrami i limitem czasu.</span><span class="sxs-lookup"><span data-stu-id="d7457-116">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="d7457-117">Po zakończeniu sesji zostanie ona zapisana na określonym koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="d7457-117">Once the session is complete, it will be saved to the specified storage account.</span></span> 

<span data-ttu-id="d7457-118">Uwaga: aby można było tworzyć przechwycenia pakietów, rozszerzenie obserwatora sieci Azure musi być zainstalowane na docelowej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d7457-118">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="d7457-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d7457-119">PARAMETERS</span></span>

### <span data-ttu-id="d7457-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d7457-120">-AsJob</span></span>
<span data-ttu-id="d7457-121">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d7457-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d7457-122">-BytesToCapturePerPacket</span><span class="sxs-lookup"><span data-stu-id="d7457-122">-BytesToCapturePerPacket</span></span>
<span data-ttu-id="d7457-123">Bajty do przechwycenia na pakiet.</span><span class="sxs-lookup"><span data-stu-id="d7457-123">Bytes to capture per packet.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7457-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7457-124">-DefaultProfile</span></span>
<span data-ttu-id="d7457-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d7457-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7457-126">-Filter</span><span class="sxs-lookup"><span data-stu-id="d7457-126">-Filter</span></span>
<span data-ttu-id="d7457-127">Filtry dla sesji przechwytywania pakietów.</span><span class="sxs-lookup"><span data-stu-id="d7457-127">Filters for packet capture session.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7457-128">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="d7457-128">-LocalFilePath</span></span>
<span data-ttu-id="d7457-129">Lokalna ścieżka pliku.</span><span class="sxs-lookup"><span data-stu-id="d7457-129">Local file path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7457-130">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d7457-130">-NetworkWatcher</span></span>
<span data-ttu-id="d7457-131">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="d7457-131">The network watcher resource.</span></span>

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

### <span data-ttu-id="d7457-132">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d7457-132">-NetworkWatcherName</span></span>
<span data-ttu-id="d7457-133">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="d7457-133">The name of network watcher.</span></span>

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

### <span data-ttu-id="d7457-134">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="d7457-134">-PacketCaptureName</span></span>
<span data-ttu-id="d7457-135">Nazwa przechwytywania pakietu.</span><span class="sxs-lookup"><span data-stu-id="d7457-135">The packet capture name.</span></span>

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

### <span data-ttu-id="d7457-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7457-136">-ResourceGroupName</span></span>
<span data-ttu-id="d7457-137">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="d7457-137">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="d7457-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="d7457-138">-StorageAccountId</span></span>
<span data-ttu-id="d7457-139">Identyfikator konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="d7457-139">Storage account Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7457-140">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="d7457-140">-StoragePath</span></span>
<span data-ttu-id="d7457-141">Ścieżka do magazynu.</span><span class="sxs-lookup"><span data-stu-id="d7457-141">Storage path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7457-142">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="d7457-142">-TargetVirtualMachineId</span></span>
<span data-ttu-id="d7457-143">Docelowy Identyfikator maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d7457-143">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="d7457-144">-TimeLimitInSeconds</span><span class="sxs-lookup"><span data-stu-id="d7457-144">-TimeLimitInSeconds</span></span>
<span data-ttu-id="d7457-145">Limit czasu w sekundach.</span><span class="sxs-lookup"><span data-stu-id="d7457-145">Time limit in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7457-146">-TotalBytesPerSession</span><span class="sxs-lookup"><span data-stu-id="d7457-146">-TotalBytesPerSession</span></span>
<span data-ttu-id="d7457-147">Całkowita liczba bajtów na sesję.</span><span class="sxs-lookup"><span data-stu-id="d7457-147">Total bytes per session.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7457-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d7457-148">-Confirm</span></span>
<span data-ttu-id="d7457-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7457-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7457-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7457-150">-WhatIf</span></span>
<span data-ttu-id="d7457-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7457-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7457-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d7457-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7457-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7457-153">CommonParameters</span></span>
<span data-ttu-id="d7457-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7457-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7457-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7457-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7457-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7457-156">INPUTS</span></span>

### <span data-ttu-id="d7457-157">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d7457-157">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="d7457-158">System. String system. Nullable \` 1 \[ \[ System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089\]\]</span><span class="sxs-lookup"><span data-stu-id="d7457-158">System.String System.Nullable\`1\[\[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\]</span></span>

## <span data-ttu-id="d7457-159">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d7457-159">OUTPUTS</span></span>

### <span data-ttu-id="d7457-160">Microsoft. Azure. Commands. Network. models. PSPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d7457-160">Microsoft.Azure.Commands.Network.Models.PSPacketCapture</span></span>

## <span data-ttu-id="d7457-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d7457-161">NOTES</span></span>
<span data-ttu-id="d7457-162">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, Monitor sieci, pakiet, przechwytywanie, ruch</span><span class="sxs-lookup"><span data-stu-id="d7457-162">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span> 

## <span data-ttu-id="d7457-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d7457-163">RELATED LINKS</span></span>

[<span data-ttu-id="d7457-164">Nowe — AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d7457-164">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="d7457-165">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d7457-165">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d7457-166">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d7457-166">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d7457-167">Zatrzymaj — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d7457-167">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d7457-168">Nowe — AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d7457-168">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="d7457-169">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d7457-169">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="d7457-170">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d7457-170">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="d7457-171">Test — AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d7457-171">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="d7457-172">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d7457-172">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="d7457-173">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d7457-173">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d7457-174">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d7457-174">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="d7457-175">Start — AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d7457-175">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)


