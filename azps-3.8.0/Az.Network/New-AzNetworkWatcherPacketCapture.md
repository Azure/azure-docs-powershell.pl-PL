---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 348767f145c2dd407fc277549f89c44386c8a564
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050746"
---
# <span data-ttu-id="c0591-101">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c0591-101">New-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="c0591-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c0591-102">SYNOPSIS</span></span>
<span data-ttu-id="c0591-103">Tworzy nowy zasób przechwytywania pakietów i rozpoczyna sesję przechwytywania pakietów na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c0591-103">Creates a new packet capture resource and starts a packet capture session on a VM.</span></span>

## <span data-ttu-id="c0591-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c0591-104">SYNTAX</span></span>

### <span data-ttu-id="c0591-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c0591-105">SetByResource (Default)</span></span>
```
New-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0591-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="c0591-106">SetByName</span></span>
```
New-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> -TargetVirtualMachineId <String> [-StorageAccountId <String>]
 [-StoragePath <String>] [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>]
 [-TotalBytesPerSession <Int32>] [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0591-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="c0591-107">SetByLocation</span></span>
```
New-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0591-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c0591-108">DESCRIPTION</span></span>
<span data-ttu-id="c0591-109">Polecenie cmdlet New-AzNetworkWatcherPacketCapture tworzy nowy zasób przechwytywania pakietów i rozpoczyna sesję przechwytywania pakietów na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c0591-109">The New-AzNetworkWatcherPacketCapture cmdlet creates a new packet capture resource and starts a packet capture session on a VM.</span></span>
<span data-ttu-id="c0591-110">Długość sesji przechwytywania pakietów można skonfigurować za pośrednictwem ograniczenia czasu lub ograniczenia rozmiaru.</span><span class="sxs-lookup"><span data-stu-id="c0591-110">The length of the Packet Capture sessions can be configured via a time constraint or a size constraint.</span></span> <span data-ttu-id="c0591-111">Można również skonfigurować ilość danych przechwyconych dla każdego pakietu.</span><span class="sxs-lookup"><span data-stu-id="c0591-111">The amount of data captured for each packet can also be configured.</span></span>
<span data-ttu-id="c0591-112">Filtry można stosować do danej sesji przechwytywania pakietów, co umożliwia dostosowanie typu przechwyconych pakietów.</span><span class="sxs-lookup"><span data-stu-id="c0591-112">Filters can be applied to a given packet capture session, allowing you to customize the type of packets captured.</span></span> <span data-ttu-id="c0591-113">Filtry mogą ograniczać pakiety na lokalnych i zdalnych adresach IP & zakres adresów, porty lokalne i zdalne & zakresy portów oraz protokół na poziomie sesji do przechwycenia.</span><span class="sxs-lookup"><span data-stu-id="c0591-113">Filters can restrict packets on local and remote IP addresses & address ranges, local and remote ports & port ranges, and the session level protocol to be captured.</span></span> <span data-ttu-id="c0591-114">Filtry są składane i można zastosować wiele filtrów w celu zapewnienia szczegółowości funkcji przechwytywania.</span><span class="sxs-lookup"><span data-stu-id="c0591-114">Filters are composable, and multiple filters can be applied to provide you with granularity of capture.</span></span>

## <span data-ttu-id="c0591-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c0591-115">EXAMPLES</span></span>

### <span data-ttu-id="c0591-116">Przykład 1. Tworzenie przechwyconych pakietów za pomocą wielu filtrów</span><span class="sxs-lookup"><span data-stu-id="c0591-116">Example 1: Create a Packet Capture with multiple filters</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filter $filter1, $filter2
```

<span data-ttu-id="c0591-117">W tym przykładzie tworzymy przechwycony pakiet o nazwie "PacketCaptureTest" z wieloma filtrami i limitem czasu.</span><span class="sxs-lookup"><span data-stu-id="c0591-117">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="c0591-118">Po zakończeniu sesji zostanie ona zapisana na określonym koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="c0591-118">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="c0591-119">Uwaga: aby można było tworzyć przechwycenia pakietów, rozszerzenie obserwatora sieci Azure musi być zainstalowane na docelowej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c0591-119">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="c0591-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c0591-120">PARAMETERS</span></span>

### <span data-ttu-id="c0591-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0591-121">-AsJob</span></span>
<span data-ttu-id="c0591-122">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c0591-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c0591-123">-BytesToCapturePerPacket</span><span class="sxs-lookup"><span data-stu-id="c0591-123">-BytesToCapturePerPacket</span></span>
<span data-ttu-id="c0591-124">Bajty do przechwycenia na pakiet.</span><span class="sxs-lookup"><span data-stu-id="c0591-124">Bytes to capture per packet.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0591-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0591-125">-DefaultProfile</span></span>
<span data-ttu-id="c0591-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c0591-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0591-127">-Filter</span><span class="sxs-lookup"><span data-stu-id="c0591-127">-Filter</span></span>
<span data-ttu-id="c0591-128">Filtry dla sesji przechwytywania pakietów.</span><span class="sxs-lookup"><span data-stu-id="c0591-128">Filters for packet capture session.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0591-129">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="c0591-129">-LocalFilePath</span></span>
<span data-ttu-id="c0591-130">Lokalna ścieżka pliku.</span><span class="sxs-lookup"><span data-stu-id="c0591-130">Local file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0591-131">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c0591-131">-Location</span></span>
<span data-ttu-id="c0591-132">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="c0591-132">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0591-133">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c0591-133">-NetworkWatcher</span></span>
<span data-ttu-id="c0591-134">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="c0591-134">The network watcher resource.</span></span>

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

### <span data-ttu-id="c0591-135">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="c0591-135">-NetworkWatcherName</span></span>
<span data-ttu-id="c0591-136">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="c0591-136">The name of network watcher.</span></span>

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

### <span data-ttu-id="c0591-137">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="c0591-137">-PacketCaptureName</span></span>
<span data-ttu-id="c0591-138">Nazwa przechwytywania pakietu.</span><span class="sxs-lookup"><span data-stu-id="c0591-138">The packet capture name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0591-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0591-139">-ResourceGroupName</span></span>
<span data-ttu-id="c0591-140">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="c0591-140">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="c0591-141">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="c0591-141">-StorageAccountId</span></span>
<span data-ttu-id="c0591-142">Identyfikator konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="c0591-142">Storage account Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0591-143">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="c0591-143">-StoragePath</span></span>
<span data-ttu-id="c0591-144">Ścieżka do magazynu.</span><span class="sxs-lookup"><span data-stu-id="c0591-144">Storage path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0591-145">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="c0591-145">-TargetVirtualMachineId</span></span>
<span data-ttu-id="c0591-146">Docelowy Identyfikator maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c0591-146">The target virtual machine ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0591-147">-TimeLimitInSeconds</span><span class="sxs-lookup"><span data-stu-id="c0591-147">-TimeLimitInSeconds</span></span>
<span data-ttu-id="c0591-148">Limit czasu w sekundach.</span><span class="sxs-lookup"><span data-stu-id="c0591-148">Time limit in seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0591-149">-TotalBytesPerSession</span><span class="sxs-lookup"><span data-stu-id="c0591-149">-TotalBytesPerSession</span></span>
<span data-ttu-id="c0591-150">Całkowita liczba bajtów na sesję.</span><span class="sxs-lookup"><span data-stu-id="c0591-150">Total bytes per session.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0591-151">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c0591-151">-Confirm</span></span>
<span data-ttu-id="c0591-152">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0591-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0591-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0591-153">-WhatIf</span></span>
<span data-ttu-id="c0591-154">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0591-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0591-155">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c0591-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0591-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0591-156">CommonParameters</span></span>
<span data-ttu-id="c0591-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0591-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0591-158">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0591-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0591-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0591-159">INPUTS</span></span>

### <span data-ttu-id="c0591-160">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c0591-160">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="c0591-161">System. String</span><span class="sxs-lookup"><span data-stu-id="c0591-161">System.String</span></span>

### <span data-ttu-id="c0591-162">System. Nullable ' 1 [[System. Int32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c0591-162">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="c0591-163">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c0591-163">OUTPUTS</span></span>

### <span data-ttu-id="c0591-164">Microsoft. Azure. Commands. Network. models. PSPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="c0591-164">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureResult</span></span>

## <span data-ttu-id="c0591-165">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c0591-165">NOTES</span></span>
<span data-ttu-id="c0591-166">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, Monitor sieci, pakiet, przechwytywanie, ruch</span><span class="sxs-lookup"><span data-stu-id="c0591-166">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span> 

## <span data-ttu-id="c0591-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c0591-167">RELATED LINKS</span></span>

[<span data-ttu-id="c0591-168">Nowe — AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c0591-168">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="c0591-169">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c0591-169">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="c0591-170">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c0591-170">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="c0591-171">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c0591-171">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="c0591-172">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c0591-172">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c0591-173">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c0591-173">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="c0591-174">Start — AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c0591-174">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="c0591-175">Nowe — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c0591-175">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c0591-176">Nowe — AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c0591-176">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="c0591-177">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c0591-177">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c0591-178">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c0591-178">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c0591-179">Zatrzymaj — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c0591-179">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c0591-180">Nowe — AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="c0591-180">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="c0591-181">Test — AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c0591-181">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="c0591-182">Test — AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="c0591-182">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="c0591-183">Zatrzymaj — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c0591-183">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c0591-184">Start — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c0591-184">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c0591-185">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c0591-185">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c0591-186">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="c0591-186">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="c0591-187">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c0591-187">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c0591-188">Nowe — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c0591-188">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c0591-189">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="c0591-189">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="c0591-190">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="c0591-190">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="c0591-191">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="c0591-191">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="c0591-192">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="c0591-192">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="c0591-193">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="c0591-193">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="c0591-194">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c0591-194">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)


