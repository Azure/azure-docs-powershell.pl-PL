---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 5c7709c234ba762e5b87418cc0e9b3fc4637ac11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717393"
---
# <span data-ttu-id="bcdea-101">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bcdea-101">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="bcdea-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bcdea-102">SYNOPSIS</span></span>
<span data-ttu-id="bcdea-103">Aktualizowanie monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="bcdea-103">Update a connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bcdea-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bcdea-104">SYNTAX</span></span>

### <span data-ttu-id="bcdea-105">SetByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bcdea-105">SetByName (Default)</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bcdea-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="bcdea-106">SetByResource</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bcdea-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="bcdea-107">SetByLocation</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bcdea-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="bcdea-108">SetByResourceId</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bcdea-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="bcdea-109">SetByInputObject</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcdea-110">Opis</span><span class="sxs-lookup"><span data-stu-id="bcdea-110">DESCRIPTION</span></span>
<span data-ttu-id="bcdea-111">Polecenie cmdlet Set-AzureRmNetworkWatcherConnectionMonitor aktualizuje określony monitor połączeń.</span><span class="sxs-lookup"><span data-stu-id="bcdea-111">The Set-AzureRmNetworkWatcherConnectionMonitor cmdlet updates the specified connection monitor.</span></span>

## <span data-ttu-id="bcdea-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bcdea-112">EXAMPLES</span></span>

### <span data-ttu-id="bcdea-113">Przykład 1: aktualizowanie monitora połączeń</span><span class="sxs-lookup"><span data-stu-id="bcdea-113">Example 1: Update a connection monitor</span></span>
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

<span data-ttu-id="bcdea-114">W tym przykładzie Zaktualizowano istniejący monitor połączenia, zmieniając destinationAddress i dodając Tagi.</span><span class="sxs-lookup"><span data-stu-id="bcdea-114">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="bcdea-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bcdea-115">PARAMETERS</span></span>

### <span data-ttu-id="bcdea-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bcdea-116">-AsJob</span></span>
<span data-ttu-id="bcdea-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="bcdea-117">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcdea-118">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="bcdea-118">-ConfigureOnly</span></span>
<span data-ttu-id="bcdea-119">Konfigurowanie monitora połączeń, ale nie Rozpoczynanie go</span><span class="sxs-lookup"><span data-stu-id="bcdea-119">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="bcdea-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcdea-120">-DefaultProfile</span></span>
<span data-ttu-id="bcdea-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bcdea-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcdea-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="bcdea-122">-DestinationAddress</span></span>
<span data-ttu-id="bcdea-123">Adres IP miejsca docelowego monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="bcdea-123">The Ip address of the connection monitor destination.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcdea-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="bcdea-124">-DestinationPort</span></span>
<span data-ttu-id="bcdea-125">Port docelowy.</span><span class="sxs-lookup"><span data-stu-id="bcdea-125">Destination port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcdea-126">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="bcdea-126">-DestinationResourceId</span></span>
<span data-ttu-id="bcdea-127">Identyfikator miejsca docelowego monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="bcdea-127">The ID of the connection monitor destination.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcdea-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bcdea-128">-InputObject</span></span>
<span data-ttu-id="bcdea-129">Obiekt monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="bcdea-129">Connection monitor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bcdea-130">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="bcdea-130">-Location</span></span>
<span data-ttu-id="bcdea-131">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="bcdea-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="bcdea-132">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="bcdea-132">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="bcdea-133">Interwał monitorowania w sekundach.</span><span class="sxs-lookup"><span data-stu-id="bcdea-133">Monitoring interval in seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcdea-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bcdea-134">-Name</span></span>
<span data-ttu-id="bcdea-135">Nazwa monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="bcdea-135">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcdea-136">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bcdea-136">-NetworkWatcher</span></span>
<span data-ttu-id="bcdea-137">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="bcdea-137">The network watcher resource.</span></span>

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

### <span data-ttu-id="bcdea-138">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="bcdea-138">-NetworkWatcherName</span></span>
<span data-ttu-id="bcdea-139">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="bcdea-139">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcdea-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcdea-140">-ResourceGroupName</span></span>
<span data-ttu-id="bcdea-141">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="bcdea-141">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcdea-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bcdea-142">-ResourceId</span></span>
<span data-ttu-id="bcdea-143">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="bcdea-143">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcdea-144">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="bcdea-144">-SourcePort</span></span>
<span data-ttu-id="bcdea-145">Port źródłowy.</span><span class="sxs-lookup"><span data-stu-id="bcdea-145">Source port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcdea-146">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="bcdea-146">-SourceResourceId</span></span>
<span data-ttu-id="bcdea-147">Identyfikator źródła monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="bcdea-147">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="bcdea-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="bcdea-148">-Tag</span></span>
<span data-ttu-id="bcdea-149">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="bcdea-149">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcdea-150">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bcdea-150">-Confirm</span></span>
<span data-ttu-id="bcdea-151">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bcdea-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcdea-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcdea-152">-WhatIf</span></span>
<span data-ttu-id="bcdea-153">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bcdea-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcdea-154">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bcdea-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcdea-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcdea-155">CommonParameters</span></span>
<span data-ttu-id="bcdea-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcdea-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcdea-157">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcdea-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcdea-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bcdea-158">INPUTS</span></span>

### <span data-ttu-id="bcdea-159">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bcdea-159">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="bcdea-160">Parametry: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bcdea-160">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="bcdea-161">System. String</span><span class="sxs-lookup"><span data-stu-id="bcdea-161">System.String</span></span>

### <span data-ttu-id="bcdea-162">Microsoft. Azure. Commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="bcdea-162">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>
<span data-ttu-id="bcdea-163">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bcdea-163">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="bcdea-164">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bcdea-164">OUTPUTS</span></span>

### <span data-ttu-id="bcdea-165">Microsoft. Azure. Commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="bcdea-165">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="bcdea-166">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bcdea-166">NOTES</span></span>
<span data-ttu-id="bcdea-167">Słowa kluczowe: Azure, azurerm, ARM, zasób, łączność, zarządzanie, Menedżer, Sieć, Sieć, obserwator sieci, monitor połączenia</span><span class="sxs-lookup"><span data-stu-id="bcdea-167">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="bcdea-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bcdea-168">RELATED LINKS</span></span>

[<span data-ttu-id="bcdea-169">Nowe — AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bcdea-169">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="bcdea-170">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bcdea-170">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="bcdea-171">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bcdea-171">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="bcdea-172">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="bcdea-172">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="bcdea-173">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="bcdea-173">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="bcdea-174">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="bcdea-174">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="bcdea-175">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="bcdea-175">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="bcdea-176">Nowe — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bcdea-176">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="bcdea-177">Nowe — AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="bcdea-177">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="bcdea-178">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bcdea-178">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="bcdea-179">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bcdea-179">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="bcdea-180">Zatrzymaj — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bcdea-180">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="bcdea-181">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bcdea-181">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="bcdea-182">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="bcdea-182">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="bcdea-183">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bcdea-183">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="bcdea-184">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bcdea-184">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="bcdea-185">Zatrzymaj — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bcdea-185">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="bcdea-186">Nowe — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bcdea-186">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="bcdea-187">Nowe — AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="bcdea-187">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>]()

[<span data-ttu-id="bcdea-188">Test — AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="bcdea-188">Test-AzureRmNetworkWatcherIPFlow</span></span>]()

[<span data-ttu-id="bcdea-189">Test — AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="bcdea-189">Test-AzureRmNetworkWatcherConnectivity</span></span>]()

[<span data-ttu-id="bcdea-190">Start — AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="bcdea-190">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>]()

[<span data-ttu-id="bcdea-191">Start — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bcdea-191">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="bcdea-192">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="bcdea-192">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>]()

[<span data-ttu-id="bcdea-193">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="bcdea-193">Get-AzureRMNetworkWatcherReachabilityReport</span></span>]()

[<span data-ttu-id="bcdea-194">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="bcdea-194">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>]()

[<span data-ttu-id="bcdea-195">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="bcdea-195">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>]()
