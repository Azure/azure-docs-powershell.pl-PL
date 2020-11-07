---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 44f81008b0693a4ff14a80a818e9d2514dfe0ebf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718636"
---
# <span data-ttu-id="69916-101">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="69916-101">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="69916-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="69916-102">SYNOPSIS</span></span>
<span data-ttu-id="69916-103">Aktualizowanie monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="69916-103">Update a connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69916-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="69916-104">SYNTAX</span></span>

### <span data-ttu-id="69916-105">SetByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="69916-105">SetByName (Default)</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69916-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="69916-106">SetByResource</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69916-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="69916-107">SetByLocation</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69916-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="69916-108">SetByResourceId</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69916-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="69916-109">SetByInputObject</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69916-110">Opis</span><span class="sxs-lookup"><span data-stu-id="69916-110">DESCRIPTION</span></span>
<span data-ttu-id="69916-111">Polecenie cmdlet Set-AzureRmNetworkWatcherConnectionMonitor aktualizuje określony monitor połączeń.</span><span class="sxs-lookup"><span data-stu-id="69916-111">The Set-AzureRmNetworkWatcherConnectionMonitor cmdlet updates the specified connection monitor.</span></span>

## <span data-ttu-id="69916-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="69916-112">EXAMPLES</span></span>

### <span data-ttu-id="69916-113">Przykład 1: aktualizowanie monitora połączeń</span><span class="sxs-lookup"><span data-stu-id="69916-113">Example 1: Update a connection monitor</span></span>
```
PS C:\> Set-AzureRmNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm 
-DestinationAddress google.com -DestinationPort 80 -Tag @{"key1" = "value1"}

Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/cm
Etag                        : W/"5b2b20e8-0ce0-417e-9607-76208149bb67"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000
                                00000/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMach
                                ines/vm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "google.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:19:28 PM
MonitoringStatus            : Running
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {
                                "key1": "value1"
                              }
```

<span data-ttu-id="69916-114">W tym przykładzie Zaktualizowano istniejący monitor połączenia, zmieniając destinationAddress i dodając Tagi.</span><span class="sxs-lookup"><span data-stu-id="69916-114">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="69916-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="69916-115">PARAMETERS</span></span>

### <span data-ttu-id="69916-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69916-116">-AsJob</span></span>
<span data-ttu-id="69916-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="69916-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="69916-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="69916-118">-Confirm</span></span>
<span data-ttu-id="69916-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69916-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69916-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69916-120">-DefaultProfile</span></span>
<span data-ttu-id="69916-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="69916-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69916-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="69916-122">-DestinationAddress</span></span>
<span data-ttu-id="69916-123">Adres IP miejsca docelowego monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="69916-123">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="69916-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="69916-124">-DestinationPort</span></span>
<span data-ttu-id="69916-125">Port docelowy.</span><span class="sxs-lookup"><span data-stu-id="69916-125">Destination port.</span></span>

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

### <span data-ttu-id="69916-126">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="69916-126">-DestinationResourceId</span></span>
<span data-ttu-id="69916-127">Identyfikator miejsca docelowego monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="69916-127">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="69916-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="69916-128">-InputObject</span></span>
<span data-ttu-id="69916-129">Obiekt monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="69916-129">Connection monitor object.</span></span>

```yaml
Type: PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69916-130">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="69916-130">-Location</span></span>
<span data-ttu-id="69916-131">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="69916-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="69916-132">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="69916-132">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="69916-133">Interwał monitorowania w sekundach.</span><span class="sxs-lookup"><span data-stu-id="69916-133">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="69916-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="69916-134">-Name</span></span>
<span data-ttu-id="69916-135">Nazwa monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="69916-135">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69916-136">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="69916-136">-NetworkWatcher</span></span>
<span data-ttu-id="69916-137">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="69916-137">The network watcher resource.</span></span>

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

### <span data-ttu-id="69916-138">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="69916-138">-NetworkWatcherName</span></span>
<span data-ttu-id="69916-139">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="69916-139">The name of network watcher.</span></span>

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

### <span data-ttu-id="69916-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69916-140">-ResourceGroupName</span></span>
<span data-ttu-id="69916-141">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="69916-141">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="69916-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69916-142">-ResourceId</span></span>
<span data-ttu-id="69916-143">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="69916-143">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69916-144">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="69916-144">-SourcePort</span></span>
<span data-ttu-id="69916-145">Port źródłowy.</span><span class="sxs-lookup"><span data-stu-id="69916-145">Source port.</span></span>

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

### <span data-ttu-id="69916-146">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="69916-146">-SourceResourceId</span></span>
<span data-ttu-id="69916-147">Identyfikator źródła monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="69916-147">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="69916-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="69916-148">-Tag</span></span>
<span data-ttu-id="69916-149">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="69916-149">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="69916-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69916-150">-WhatIf</span></span>
<span data-ttu-id="69916-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69916-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69916-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="69916-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69916-153">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="69916-153">-ConfigureOnly</span></span>
<span data-ttu-id="69916-154">Konfigurowanie monitora połączeń, ale nie Rozpoczynanie go</span><span class="sxs-lookup"><span data-stu-id="69916-154">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="69916-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69916-155">CommonParameters</span></span>
<span data-ttu-id="69916-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69916-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="69916-157">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69916-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69916-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69916-158">INPUTS</span></span>

### <span data-ttu-id="69916-159">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="69916-159">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="69916-160">System. String Microsoft. Azure. Commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="69916-160">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="69916-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="69916-161">OUTPUTS</span></span>

### <span data-ttu-id="69916-162">Microsoft. Azure. Commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="69916-162">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="69916-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="69916-163">NOTES</span></span>
<span data-ttu-id="69916-164">Słowa kluczowe: Azure, azurerm, ARM, zasób, łączność, zarządzanie, Menedżer, Sieć, Sieć, obserwator sieci, monitor połączenia</span><span class="sxs-lookup"><span data-stu-id="69916-164">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="69916-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="69916-165">RELATED LINKS</span></span>

[<span data-ttu-id="69916-166">Nowe — AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="69916-166">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="69916-167">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="69916-167">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="69916-168">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="69916-168">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="69916-169">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="69916-169">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="69916-170">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="69916-170">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="69916-171">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="69916-171">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="69916-172">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="69916-172">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="69916-173">Nowe — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="69916-173">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="69916-174">Nowe — AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="69916-174">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="69916-175">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="69916-175">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="69916-176">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="69916-176">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="69916-177">Zatrzymaj — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="69916-177">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="69916-178">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="69916-178">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="69916-179">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="69916-179">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="69916-180">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="69916-180">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="69916-181">Start — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="69916-181">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="69916-182">Zatrzymaj — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="69916-182">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="69916-183">Nowe — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="69916-183">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()
