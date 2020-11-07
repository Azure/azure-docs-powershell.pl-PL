---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: b8dd04fa4727465ee9b3be3eaf5e5e06a2243338
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718905"
---
# <span data-ttu-id="8bc1f-101">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8bc1f-101">New-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="8bc1f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8bc1f-102">SYNOPSIS</span></span>
<span data-ttu-id="8bc1f-103">Umożliwia utworzenie monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="8bc1f-103">Creates a connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8bc1f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8bc1f-104">SYNTAX</span></span>

### <span data-ttu-id="8bc1f-105">SetByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8bc1f-105">SetByName (Default)</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8bc1f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="8bc1f-106">SetByResource</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8bc1f-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="8bc1f-107">SetByLocation</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bc1f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8bc1f-108">DESCRIPTION</span></span>
<span data-ttu-id="8bc1f-109">Polecenie cmdlet New-AzureRmNetworkWatcherConnectionMonitor rcreates monitorze połączeń dla określonego źródła i miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="8bc1f-109">The New-AzureRmNetworkWatcherConnectionMonitor cmdlet rcreates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="8bc1f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8bc1f-110">EXAMPLES</span></span>

### <span data-ttu-id="8bc1f-111">Przykład 1. Tworzenie monitora połączeń dla maszyny wirtualnej i lokalizacji docelowej w Internecie</span><span class="sxs-lookup"><span data-stu-id="8bc1f-111">Example 1: Create a connection monitor for a vm and internet destination</span></span>
```
PS C:\> New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm -DestinationAddress bing.com -DestinationPort 80

Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/t1
Etag                        : W/"e86b28cf-b907-4475-a8b7-34d310367694"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000
                                00000/resourceGroups/RgCentralUSEUAP/providers/Microsoft
                                .Compute/virtualMachines/vm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "bing.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:13:11 PM
MonitoringStatus            : Running
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {}
```

<span data-ttu-id="8bc1f-112">Polecenie cmdlet New-AzureRmNetworkWatcherConnectionMonitor tworzy monitor połączenia dla określonego źródła i miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="8bc1f-112">The New-AzureRmNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="8bc1f-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8bc1f-113">PARAMETERS</span></span>

### <span data-ttu-id="8bc1f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8bc1f-114">-AsJob</span></span>
<span data-ttu-id="8bc1f-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="8bc1f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8bc1f-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8bc1f-116">-Confirm</span></span>
<span data-ttu-id="8bc1f-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bc1f-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bc1f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bc1f-118">-DefaultProfile</span></span>
<span data-ttu-id="8bc1f-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8bc1f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bc1f-120">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="8bc1f-120">-DestinationAddress</span></span>
<span data-ttu-id="8bc1f-121">Adres IP miejsca docelowego monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="8bc1f-121">The Ip address of the connection monitor destination.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bc1f-122">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="8bc1f-122">-DestinationPort</span></span>
<span data-ttu-id="8bc1f-123">Port docelowy.</span><span class="sxs-lookup"><span data-stu-id="8bc1f-123">Destination port.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bc1f-124">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="8bc1f-124">-DestinationResourceId</span></span>
<span data-ttu-id="8bc1f-125">Identyfikator miejsca docelowego monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="8bc1f-125">The ID of the connection monitor destination.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bc1f-126">-Force</span><span class="sxs-lookup"><span data-stu-id="8bc1f-126">-Force</span></span>
<span data-ttu-id="8bc1f-127">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="8bc1f-127">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="8bc1f-128">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="8bc1f-128">-Location</span></span>
<span data-ttu-id="8bc1f-129">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="8bc1f-129">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bc1f-130">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="8bc1f-130">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="8bc1f-131">Interwał monitorowania w sekundach.</span><span class="sxs-lookup"><span data-stu-id="8bc1f-131">Monitoring interval in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bc1f-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8bc1f-132">-Name</span></span>
<span data-ttu-id="8bc1f-133">Nazwa monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="8bc1f-133">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bc1f-134">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8bc1f-134">-NetworkWatcher</span></span>
<span data-ttu-id="8bc1f-135">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="8bc1f-135">The network watcher resource.</span></span>

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

### <span data-ttu-id="8bc1f-136">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="8bc1f-136">-NetworkWatcherName</span></span>
<span data-ttu-id="8bc1f-137">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="8bc1f-137">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bc1f-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bc1f-138">-ResourceGroupName</span></span>
<span data-ttu-id="8bc1f-139">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="8bc1f-139">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bc1f-140">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="8bc1f-140">-SourcePort</span></span>
<span data-ttu-id="8bc1f-141">Port źródłowy.</span><span class="sxs-lookup"><span data-stu-id="8bc1f-141">Source port.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bc1f-142">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="8bc1f-142">-SourceResourceId</span></span>
<span data-ttu-id="8bc1f-143">Identyfikator źródła monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="8bc1f-143">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="8bc1f-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="8bc1f-144">-Tag</span></span>
<span data-ttu-id="8bc1f-145">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="8bc1f-145">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bc1f-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bc1f-146">-WhatIf</span></span>
<span data-ttu-id="8bc1f-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bc1f-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bc1f-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8bc1f-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bc1f-149">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="8bc1f-149">-ConfigureOnly</span></span>
<span data-ttu-id="8bc1f-150">Konfigurowanie monitora połączeń, ale nie Rozpoczynanie go</span><span class="sxs-lookup"><span data-stu-id="8bc1f-150">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="8bc1f-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bc1f-151">CommonParameters</span></span>
<span data-ttu-id="8bc1f-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bc1f-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="8bc1f-153">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bc1f-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bc1f-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8bc1f-154">INPUTS</span></span>

### <span data-ttu-id="8bc1f-155">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8bc1f-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="8bc1f-156">System. String</span><span class="sxs-lookup"><span data-stu-id="8bc1f-156">System.String</span></span>

## <span data-ttu-id="8bc1f-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8bc1f-157">OUTPUTS</span></span>

### <span data-ttu-id="8bc1f-158">Microsoft. Azure. Commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="8bc1f-158">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="8bc1f-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8bc1f-159">NOTES</span></span>
<span data-ttu-id="8bc1f-160">Słowa kluczowe: Azure, azurerm, ARM, zasób, łączność, zarządzanie, Menedżer, Sieć, Sieć, obserwator sieci, monitor połączenia</span><span class="sxs-lookup"><span data-stu-id="8bc1f-160">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="8bc1f-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8bc1f-161">RELATED LINKS</span></span>

[<span data-ttu-id="8bc1f-162">Nowe — AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8bc1f-162">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="8bc1f-163">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8bc1f-163">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="8bc1f-164">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8bc1f-164">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="8bc1f-165">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="8bc1f-165">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="8bc1f-166">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="8bc1f-166">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="8bc1f-167">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="8bc1f-167">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="8bc1f-168">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="8bc1f-168">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="8bc1f-169">Nowe — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8bc1f-169">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="8bc1f-170">Nowe — AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="8bc1f-170">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="8bc1f-171">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8bc1f-171">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="8bc1f-172">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8bc1f-172">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="8bc1f-173">Zatrzymaj — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8bc1f-173">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="8bc1f-174">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8bc1f-174">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="8bc1f-175">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="8bc1f-175">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="8bc1f-176">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8bc1f-176">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="8bc1f-177">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8bc1f-177">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="8bc1f-178">Start — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8bc1f-178">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="8bc1f-179">Zatrzymaj — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8bc1f-179">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()
