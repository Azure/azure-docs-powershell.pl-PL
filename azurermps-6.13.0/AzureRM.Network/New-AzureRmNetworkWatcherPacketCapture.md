---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: ab7b6176f8453d1a3e5e0001e6b6c1e47c4de1cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554058"
---
# <span data-ttu-id="2e5ad-101">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2e5ad-101">New-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="2e5ad-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2e5ad-102">SYNOPSIS</span></span>
<span data-ttu-id="2e5ad-103">Tworzy nowy zasób przechwytywania pakietów i rozpoczyna sesję przechwytywania pakietów na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2e5ad-103">Creates a new packet capture resource and starts a packet capture session on a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e5ad-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2e5ad-104">SYNTAX</span></span>

### <span data-ttu-id="2e5ad-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2e5ad-105">SetByResource (Default)</span></span>
```
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e5ad-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="2e5ad-106">SetByName</span></span>
```
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> -TargetVirtualMachineId <String> [-StorageAccountId <String>]
 [-StoragePath <String>] [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>]
 [-TotalBytesPerSession <Int32>] [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e5ad-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="2e5ad-107">SetByLocation</span></span>
```
New-AzureRmNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e5ad-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2e5ad-108">DESCRIPTION</span></span>
<span data-ttu-id="2e5ad-109">Polecenie cmdlet New-AzureRmNetworkWatcherPacketCapture tworzy nowy zasób przechwytywania pakietów i rozpoczyna sesję przechwytywania pakietów na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2e5ad-109">The New-AzureRmNetworkWatcherPacketCapture cmdlet creates a new packet capture resource and starts a packet capture session on a VM.</span></span>
<span data-ttu-id="2e5ad-110">Długość sesji przechwytywania pakietów można skonfigurować za pośrednictwem ograniczenia czasu lub ograniczenia rozmiaru.</span><span class="sxs-lookup"><span data-stu-id="2e5ad-110">The length of the Packet Capture sessions can be configured via a time constraint or a size constraint.</span></span> <span data-ttu-id="2e5ad-111">Można również skonfigurować ilość danych przechwyconych dla każdego pakietu.</span><span class="sxs-lookup"><span data-stu-id="2e5ad-111">The amount of data captured for each packet can also be configured.</span></span>
<span data-ttu-id="2e5ad-112">Filtry można stosować do danej sesji przechwytywania pakietów, co umożliwia dostosowanie typu przechwyconych pakietów.</span><span class="sxs-lookup"><span data-stu-id="2e5ad-112">Filters can be applied to a given packet capture session, allowing you to customize the type of packets captured.</span></span> <span data-ttu-id="2e5ad-113">Filtry mogą ograniczać pakiety na lokalnych i zdalnych adresach IP & zakres adresów, porty lokalne i zdalne & zakresy portów oraz protokół na poziomie sesji do przechwycenia.</span><span class="sxs-lookup"><span data-stu-id="2e5ad-113">Filters can restrict packets on local and remote IP addresses & address ranges, local and remote ports & port ranges, and the session level protocol to be captured.</span></span> <span data-ttu-id="2e5ad-114">Filtry są składane i można zastosować wiele filtrów w celu zapewnienia szczegółowości funkcji przechwytywania.</span><span class="sxs-lookup"><span data-stu-id="2e5ad-114">Filters are composable, and multiple filters can be applied to provide you with granularity of capture.</span></span>

## <span data-ttu-id="2e5ad-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2e5ad-115">EXAMPLES</span></span>

### <span data-ttu-id="2e5ad-116">Przykład 1. Tworzenie przechwyconych pakietów za pomocą wielu filtrów</span><span class="sxs-lookup"><span data-stu-id="2e5ad-116">Example 1: Create a Packet Capture with multiple filters</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filter $filter1, $filter2
```

<span data-ttu-id="2e5ad-117">W tym przykładzie tworzymy przechwycony pakiet o nazwie "PacketCaptureTest" z wieloma filtrami i limitem czasu.</span><span class="sxs-lookup"><span data-stu-id="2e5ad-117">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="2e5ad-118">Po zakończeniu sesji zostanie ona zapisana na określonym koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="2e5ad-118">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="2e5ad-119">Uwaga: aby można było tworzyć przechwycenia pakietów, rozszerzenie obserwatora sieci Azure musi być zainstalowane na docelowej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2e5ad-119">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="2e5ad-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2e5ad-120">PARAMETERS</span></span>

### <span data-ttu-id="2e5ad-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2e5ad-121">-AsJob</span></span>
<span data-ttu-id="2e5ad-122">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="2e5ad-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2e5ad-123">-BytesToCapturePerPacket</span><span class="sxs-lookup"><span data-stu-id="2e5ad-123">-BytesToCapturePerPacket</span></span>
<span data-ttu-id="2e5ad-124">Bajty do przechwycenia na pakiet.</span><span class="sxs-lookup"><span data-stu-id="2e5ad-124">Bytes to capture per packet.</span></span>

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

### <span data-ttu-id="2e5ad-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e5ad-125">-DefaultProfile</span></span>
<span data-ttu-id="2e5ad-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2e5ad-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e5ad-127">-Filter</span><span class="sxs-lookup"><span data-stu-id="2e5ad-127">-Filter</span></span>
<span data-ttu-id="2e5ad-128">Filtry dla sesji przechwytywania pakietów.</span><span class="sxs-lookup"><span data-stu-id="2e5ad-128">Filters for packet capture session.</span></span>

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

### <span data-ttu-id="2e5ad-129">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="2e5ad-129">-LocalFilePath</span></span>
<span data-ttu-id="2e5ad-130">Lokalna ścieżka pliku.</span><span class="sxs-lookup"><span data-stu-id="2e5ad-130">Local file path.</span></span>

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

### <span data-ttu-id="2e5ad-131">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2e5ad-131">-Location</span></span>
<span data-ttu-id="2e5ad-132">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="2e5ad-132">Location of the network watcher.</span></span>

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

### <span data-ttu-id="2e5ad-133">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2e5ad-133">-NetworkWatcher</span></span>
<span data-ttu-id="2e5ad-134">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="2e5ad-134">The network watcher resource.</span></span>

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

### <span data-ttu-id="2e5ad-135">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="2e5ad-135">-NetworkWatcherName</span></span>
<span data-ttu-id="2e5ad-136">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="2e5ad-136">The name of network watcher.</span></span>

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

### <span data-ttu-id="2e5ad-137">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="2e5ad-137">-PacketCaptureName</span></span>
<span data-ttu-id="2e5ad-138">Nazwa przechwytywania pakietu.</span><span class="sxs-lookup"><span data-stu-id="2e5ad-138">The packet capture name.</span></span>

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

### <span data-ttu-id="2e5ad-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e5ad-139">-ResourceGroupName</span></span>
<span data-ttu-id="2e5ad-140">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="2e5ad-140">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="2e5ad-141">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="2e5ad-141">-StorageAccountId</span></span>
<span data-ttu-id="2e5ad-142">Identyfikator konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="2e5ad-142">Storage account Id.</span></span>

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

### <span data-ttu-id="2e5ad-143">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="2e5ad-143">-StoragePath</span></span>
<span data-ttu-id="2e5ad-144">Ścieżka do magazynu.</span><span class="sxs-lookup"><span data-stu-id="2e5ad-144">Storage path.</span></span>

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

### <span data-ttu-id="2e5ad-145">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="2e5ad-145">-TargetVirtualMachineId</span></span>
<span data-ttu-id="2e5ad-146">Docelowy Identyfikator maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2e5ad-146">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="2e5ad-147">-TimeLimitInSeconds</span><span class="sxs-lookup"><span data-stu-id="2e5ad-147">-TimeLimitInSeconds</span></span>
<span data-ttu-id="2e5ad-148">Limit czasu w sekundach.</span><span class="sxs-lookup"><span data-stu-id="2e5ad-148">Time limit in seconds.</span></span>

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

### <span data-ttu-id="2e5ad-149">-TotalBytesPerSession</span><span class="sxs-lookup"><span data-stu-id="2e5ad-149">-TotalBytesPerSession</span></span>
<span data-ttu-id="2e5ad-150">Całkowita liczba bajtów na sesję.</span><span class="sxs-lookup"><span data-stu-id="2e5ad-150">Total bytes per session.</span></span>

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

### <span data-ttu-id="2e5ad-151">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2e5ad-151">-Confirm</span></span>
<span data-ttu-id="2e5ad-152">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e5ad-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e5ad-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e5ad-153">-WhatIf</span></span>
<span data-ttu-id="2e5ad-154">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e5ad-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e5ad-155">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2e5ad-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e5ad-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e5ad-156">CommonParameters</span></span>
<span data-ttu-id="2e5ad-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e5ad-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e5ad-158">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e5ad-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e5ad-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2e5ad-159">INPUTS</span></span>

### <span data-ttu-id="2e5ad-160">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2e5ad-160">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="2e5ad-161">Parametry: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2e5ad-161">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="2e5ad-162">System. String</span><span class="sxs-lookup"><span data-stu-id="2e5ad-162">System.String</span></span>
<span data-ttu-id="2e5ad-163">Parametry: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2e5ad-163">Parameters: NetworkWatcherName (ByValue)</span></span>

### <span data-ttu-id="2e5ad-164">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="2e5ad-164">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="2e5ad-165">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2e5ad-165">OUTPUTS</span></span>

### <span data-ttu-id="2e5ad-166">Microsoft. Azure. Commands. Network. models. PSPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="2e5ad-166">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureResult</span></span>

## <span data-ttu-id="2e5ad-167">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2e5ad-167">NOTES</span></span>
<span data-ttu-id="2e5ad-168">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, Monitor sieci, pakiet, przechwytywanie, ruch</span><span class="sxs-lookup"><span data-stu-id="2e5ad-168">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span> 

## <span data-ttu-id="2e5ad-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2e5ad-169">RELATED LINKS</span></span>

[<span data-ttu-id="2e5ad-170">Nowe — AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2e5ad-170">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="2e5ad-171">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2e5ad-171">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="2e5ad-172">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2e5ad-172">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="2e5ad-173">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="2e5ad-173">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="2e5ad-174">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="2e5ad-174">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="2e5ad-175">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="2e5ad-175">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="2e5ad-176">Start — AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="2e5ad-176">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="2e5ad-177">Nowe — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2e5ad-177">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2e5ad-178">Nowe — AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="2e5ad-178">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="2e5ad-179">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2e5ad-179">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2e5ad-180">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2e5ad-180">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2e5ad-181">Zatrzymaj — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2e5ad-181">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2e5ad-182">Nowe — AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="2e5ad-182">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="2e5ad-183">Test — AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2e5ad-183">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="2e5ad-184">Test — AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="2e5ad-184">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="2e5ad-185">Zatrzymaj — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2e5ad-185">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2e5ad-186">Start — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2e5ad-186">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2e5ad-187">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2e5ad-187">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2e5ad-188">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="2e5ad-188">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="2e5ad-189">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2e5ad-189">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2e5ad-190">Nowe — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2e5ad-190">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2e5ad-191">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="2e5ad-191">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="2e5ad-192">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="2e5ad-192">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="2e5ad-193">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="2e5ad-193">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="2e5ad-194">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="2e5ad-194">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="2e5ad-195">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="2e5ad-195">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="2e5ad-196">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2e5ad-196">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)


