---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 9825562ad5f0bec36da0efd14f2e06b93a3ad588
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398057"
---
# <span data-ttu-id="72a05-101">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="72a05-101">New-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="72a05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72a05-102">SYNOPSIS</span></span>
<span data-ttu-id="72a05-103">Tworzy nowy zasób przechwytywania pakietów i rozpoczyna sesję przechwytywania pakietów na maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="72a05-103">Creates a new packet capture resource and starts a packet capture session on a VM.</span></span>

## <span data-ttu-id="72a05-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="72a05-104">SYNTAX</span></span>

### <span data-ttu-id="72a05-105">SetByResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="72a05-105">SetByResource (Default)</span></span>
```
New-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72a05-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="72a05-106">SetByName</span></span>
```
New-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> -TargetVirtualMachineId <String> [-StorageAccountId <String>]
 [-StoragePath <String>] [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>]
 [-TotalBytesPerSession <Int32>] [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72a05-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="72a05-107">SetByLocation</span></span>
```
New-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72a05-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="72a05-108">DESCRIPTION</span></span>
<span data-ttu-id="72a05-109">Polecenie New-AzNetworkWatcherPacketCapture cmdlet tworzy nowy zasób przechwytywania pakietów i rozpoczyna sesję przechwytywania pakietów w maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="72a05-109">The New-AzNetworkWatcherPacketCapture cmdlet creates a new packet capture resource and starts a packet capture session on a VM.</span></span>
<span data-ttu-id="72a05-110">Długość sesji przechwytywania pakietów można skonfigurować za pośrednictwem ograniczenia czasowego lub ograniczenia rozmiaru.</span><span class="sxs-lookup"><span data-stu-id="72a05-110">The length of the Packet Capture sessions can be configured via a time constraint or a size constraint.</span></span> <span data-ttu-id="72a05-111">Można również skonfigurować ilość danych przechwyconych dla każdego pakietu.</span><span class="sxs-lookup"><span data-stu-id="72a05-111">The amount of data captured for each packet can also be configured.</span></span>
<span data-ttu-id="72a05-112">Filtry można stosować do danej sesji przechwytywania pakietów, co pozwala dostosowywać typ przechwyconych pakietów.</span><span class="sxs-lookup"><span data-stu-id="72a05-112">Filters can be applied to a given packet capture session, allowing you to customize the type of packets captured.</span></span> <span data-ttu-id="72a05-113">Filtry mogą ograniczać liczbę pakietów w lokalnych i zdalnych adresach IP & zakresach adresów, portach lokalnych i zdalnych & zakresach portów i protokole na poziomie sesji do przechwycenia.</span><span class="sxs-lookup"><span data-stu-id="72a05-113">Filters can restrict packets on local and remote IP addresses & address ranges, local and remote ports & port ranges, and the session level protocol to be captured.</span></span> <span data-ttu-id="72a05-114">Filtry można ująć i można zastosować wiele filtrów, aby zapewnić szczegółowość przechwytywania.</span><span class="sxs-lookup"><span data-stu-id="72a05-114">Filters are composable, and multiple filters can be applied to provide you with granularity of capture.</span></span>

## <span data-ttu-id="72a05-115">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="72a05-115">EXAMPLES</span></span>

### <span data-ttu-id="72a05-116">Przykład 1. Tworzenie przechwytywania pakietów za pomocą wielu filtrów</span><span class="sxs-lookup"><span data-stu-id="72a05-116">Example 1: Create a Packet Capture with multiple filters</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filter $filter1, $filter2
```

<span data-ttu-id="72a05-117">W tym przykładzie tworzymy przechwytywanie pakietów o nazwie "PacketCaptureTest" z wieloma filtrami i limitem czasu.</span><span class="sxs-lookup"><span data-stu-id="72a05-117">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="72a05-118">Po zakończeniu sesji zostanie ona zapisana na określonym koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="72a05-118">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="72a05-119">Uwaga: Aby tworzyć przechwycone pakiety, na docelowej maszynie wirtualnej musi być zainstalowane rozszerzenie Azure Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="72a05-119">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="72a05-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72a05-120">PARAMETERS</span></span>

### <span data-ttu-id="72a05-121">— AsJob</span><span class="sxs-lookup"><span data-stu-id="72a05-121">-AsJob</span></span>
<span data-ttu-id="72a05-122">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="72a05-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="72a05-123">-BytesToCapturePerPacket</span><span class="sxs-lookup"><span data-stu-id="72a05-123">-BytesToCapturePerPacket</span></span>
<span data-ttu-id="72a05-124">Bajty do przechwycenia 1 pakietu.</span><span class="sxs-lookup"><span data-stu-id="72a05-124">Bytes to capture per packet.</span></span>

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

### <span data-ttu-id="72a05-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72a05-125">-DefaultProfile</span></span>
<span data-ttu-id="72a05-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="72a05-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72a05-127">— Filtr</span><span class="sxs-lookup"><span data-stu-id="72a05-127">-Filter</span></span>
<span data-ttu-id="72a05-128">Filtry sesji przechwytywania pakietów.</span><span class="sxs-lookup"><span data-stu-id="72a05-128">Filters for packet capture session.</span></span>

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

### <span data-ttu-id="72a05-129">- LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="72a05-129">-LocalFilePath</span></span>
<span data-ttu-id="72a05-130">Ścieżka pliku lokalnego.</span><span class="sxs-lookup"><span data-stu-id="72a05-130">Local file path.</span></span>

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

### <span data-ttu-id="72a05-131">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="72a05-131">-Location</span></span>
<span data-ttu-id="72a05-132">Lokalizacja czujki sieci.</span><span class="sxs-lookup"><span data-stu-id="72a05-132">Location of the network watcher.</span></span>

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

### <span data-ttu-id="72a05-133">— NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="72a05-133">-NetworkWatcher</span></span>
<span data-ttu-id="72a05-134">Zasób obserwowania sieci.</span><span class="sxs-lookup"><span data-stu-id="72a05-134">The network watcher resource.</span></span>

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

### <span data-ttu-id="72a05-135">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="72a05-135">-NetworkWatcherName</span></span>
<span data-ttu-id="72a05-136">Nazwa osoby oglądacej sieć.</span><span class="sxs-lookup"><span data-stu-id="72a05-136">The name of network watcher.</span></span>

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

### <span data-ttu-id="72a05-137">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="72a05-137">-PacketCaptureName</span></span>
<span data-ttu-id="72a05-138">Nazwa przechwytywania pakietów.</span><span class="sxs-lookup"><span data-stu-id="72a05-138">The packet capture name.</span></span>

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

### <span data-ttu-id="72a05-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72a05-139">-ResourceGroupName</span></span>
<span data-ttu-id="72a05-140">Nazwa grupy zasobów obserwowanych sieci.</span><span class="sxs-lookup"><span data-stu-id="72a05-140">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="72a05-141">- StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="72a05-141">-StorageAccountId</span></span>
<span data-ttu-id="72a05-142">Identyfikator konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="72a05-142">Storage account Id.</span></span>

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

### <span data-ttu-id="72a05-143">— StoragePath</span><span class="sxs-lookup"><span data-stu-id="72a05-143">-StoragePath</span></span>
<span data-ttu-id="72a05-144">Ścieżka magazynowania.</span><span class="sxs-lookup"><span data-stu-id="72a05-144">Storage path.</span></span>

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

### <span data-ttu-id="72a05-145">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="72a05-145">-TargetVirtualMachineId</span></span>
<span data-ttu-id="72a05-146">Docelowy identyfikator maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="72a05-146">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="72a05-147">-TimeLimitInSeconds</span><span class="sxs-lookup"><span data-stu-id="72a05-147">-TimeLimitInSeconds</span></span>
<span data-ttu-id="72a05-148">Limit czasu w sekundach.</span><span class="sxs-lookup"><span data-stu-id="72a05-148">Time limit in seconds.</span></span>

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

### <span data-ttu-id="72a05-149">-TotalBytesPerSession</span><span class="sxs-lookup"><span data-stu-id="72a05-149">-TotalBytesPerSession</span></span>
<span data-ttu-id="72a05-150">Łączna liczba bajtów na sesję.</span><span class="sxs-lookup"><span data-stu-id="72a05-150">Total bytes per session.</span></span>

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

### <span data-ttu-id="72a05-151">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="72a05-151">-Confirm</span></span>
<span data-ttu-id="72a05-152">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="72a05-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72a05-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72a05-153">-WhatIf</span></span>
<span data-ttu-id="72a05-154">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72a05-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72a05-155">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="72a05-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72a05-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72a05-156">CommonParameters</span></span>
<span data-ttu-id="72a05-157">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72a05-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72a05-158">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72a05-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72a05-159">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="72a05-159">INPUTS</span></span>

### <span data-ttu-id="72a05-160">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="72a05-160">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="72a05-161">System.String</span><span class="sxs-lookup"><span data-stu-id="72a05-161">System.String</span></span>

### <span data-ttu-id="72a05-162">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="72a05-162">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="72a05-163">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="72a05-163">OUTPUTS</span></span>

### <span data-ttu-id="72a05-164">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="72a05-164">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureResult</span></span>

## <span data-ttu-id="72a05-165">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="72a05-165">NOTES</span></span>
<span data-ttu-id="72a05-166">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span><span class="sxs-lookup"><span data-stu-id="72a05-166">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span> 

## <span data-ttu-id="72a05-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="72a05-167">RELATED LINKS</span></span>

[<span data-ttu-id="72a05-168">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="72a05-168">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="72a05-169">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="72a05-169">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="72a05-170">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="72a05-170">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="72a05-171">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="72a05-171">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="72a05-172">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="72a05-172">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="72a05-173">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="72a05-173">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="72a05-174">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="72a05-174">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="72a05-175">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="72a05-175">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="72a05-176">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="72a05-176">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="72a05-177">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="72a05-177">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="72a05-178">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="72a05-178">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="72a05-179">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="72a05-179">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="72a05-180">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="72a05-180">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="72a05-181">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="72a05-181">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="72a05-182">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="72a05-182">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="72a05-183">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="72a05-183">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="72a05-184">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="72a05-184">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="72a05-185">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="72a05-185">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="72a05-186">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="72a05-186">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="72a05-187">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="72a05-187">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="72a05-188">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="72a05-188">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="72a05-189">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="72a05-189">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="72a05-190">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="72a05-190">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="72a05-191">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="72a05-191">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="72a05-192">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="72a05-192">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="72a05-193">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="72a05-193">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="72a05-194">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="72a05-194">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)


