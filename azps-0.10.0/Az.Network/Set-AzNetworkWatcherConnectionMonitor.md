---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 93c54df5cb0976aa0bd8f73881208c1966bbe9d0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892750"
---
# <span data-ttu-id="e07b3-101">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e07b3-101">Set-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="e07b3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e07b3-102">SYNOPSIS</span></span>
<span data-ttu-id="e07b3-103">Aktualizowanie monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="e07b3-103">Update a connection monitor.</span></span>

## <span data-ttu-id="e07b3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e07b3-104">SYNTAX</span></span>

### <span data-ttu-id="e07b3-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e07b3-105">SetByResource (Default)</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="e07b3-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="e07b3-106">SetByName</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="e07b3-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="e07b3-107">SetByLocation</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="e07b3-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e07b3-108">SetByResourceId</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="e07b3-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="e07b3-109">SetByInputObject</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="e07b3-110">Opis</span><span class="sxs-lookup"><span data-stu-id="e07b3-110">DESCRIPTION</span></span>
<span data-ttu-id="e07b3-111">Polecenie cmdlet Set-AzNetworkWatcherConnectionMonitor aktualizuje określony monitor połączeń.</span><span class="sxs-lookup"><span data-stu-id="e07b3-111">The Set-AzNetworkWatcherConnectionMonitor cmdlet updates the specified connection monitor.</span></span>

## <span data-ttu-id="e07b3-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e07b3-112">EXAMPLES</span></span>

### <span data-ttu-id="e07b3-113">---------------Przykład 1: aktualizowanie monitora połączeń---------------</span><span class="sxs-lookup"><span data-stu-id="e07b3-113">---------------  Example 1: Update a connection monitor ---------------</span></span>
```
PS C:\> Set-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm 
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

<span data-ttu-id="e07b3-114">W tym przykładzie Zaktualizowano istniejący monitor połączenia, zmieniając destinationAddress i dodając Tagi.</span><span class="sxs-lookup"><span data-stu-id="e07b3-114">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="e07b3-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e07b3-115">PARAMETERS</span></span>

### <span data-ttu-id="e07b3-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e07b3-116">-AsJob</span></span>
<span data-ttu-id="e07b3-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e07b3-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e07b3-118">-Autostart</span><span class="sxs-lookup"><span data-stu-id="e07b3-118">-AutoStart</span></span>
<span data-ttu-id="e07b3-119">Automatyczne uruchomienie.</span><span class="sxs-lookup"><span data-stu-id="e07b3-119">Auto start.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e07b3-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e07b3-120">-Confirm</span></span>
<span data-ttu-id="e07b3-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e07b3-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e07b3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e07b3-122">-DefaultProfile</span></span>
<span data-ttu-id="e07b3-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e07b3-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e07b3-124">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="e07b3-124">-DestinationAddress</span></span>
<span data-ttu-id="e07b3-125">Adres IP miejsca docelowego monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="e07b3-125">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="e07b3-126">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="e07b3-126">-DestinationPort</span></span>
<span data-ttu-id="e07b3-127">Port docelowy.</span><span class="sxs-lookup"><span data-stu-id="e07b3-127">Destination port.</span></span>

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

### <span data-ttu-id="e07b3-128">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="e07b3-128">-DestinationResourceId</span></span>
<span data-ttu-id="e07b3-129">Identyfikator miejsca docelowego monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="e07b3-129">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="e07b3-130">-Force</span><span class="sxs-lookup"><span data-stu-id="e07b3-130">-Force</span></span>
<span data-ttu-id="e07b3-131">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="e07b3-131">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="e07b3-132">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e07b3-132">-InputObject</span></span>
<span data-ttu-id="e07b3-133">Obiekt monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="e07b3-133">Connection monitor object.</span></span>

```yaml
Type: PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e07b3-134">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e07b3-134">-Location</span></span>
<span data-ttu-id="e07b3-135">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="e07b3-135">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e07b3-136">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="e07b3-136">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="e07b3-137">Interwał monitorowania w sekundach.</span><span class="sxs-lookup"><span data-stu-id="e07b3-137">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="e07b3-138">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e07b3-138">-Name</span></span>
<span data-ttu-id="e07b3-139">Nazwa monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="e07b3-139">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e07b3-140">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e07b3-140">-NetworkWatcher</span></span>
<span data-ttu-id="e07b3-141">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="e07b3-141">The network watcher resource.</span></span>

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

### <span data-ttu-id="e07b3-142">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="e07b3-142">-NetworkWatcherName</span></span>
<span data-ttu-id="e07b3-143">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="e07b3-143">The name of network watcher.</span></span>

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

### <span data-ttu-id="e07b3-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e07b3-144">-ResourceGroupName</span></span>
<span data-ttu-id="e07b3-145">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="e07b3-145">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="e07b3-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e07b3-146">-ResourceId</span></span>
<span data-ttu-id="e07b3-147">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="e07b3-147">Resource ID.</span></span>

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

### <span data-ttu-id="e07b3-148">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="e07b3-148">-SourcePort</span></span>
<span data-ttu-id="e07b3-149">Port źródłowy.</span><span class="sxs-lookup"><span data-stu-id="e07b3-149">Source port.</span></span>

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

### <span data-ttu-id="e07b3-150">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="e07b3-150">-SourceResourceId</span></span>
<span data-ttu-id="e07b3-151">Identyfikator źródła monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="e07b3-151">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="e07b3-152">-Tag</span><span class="sxs-lookup"><span data-stu-id="e07b3-152">-Tag</span></span>
<span data-ttu-id="e07b3-153">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="e07b3-153">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="e07b3-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e07b3-154">-WhatIf</span></span>
<span data-ttu-id="e07b3-155">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e07b3-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e07b3-156">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e07b3-156">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="e07b3-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e07b3-157">INPUTS</span></span>

### <span data-ttu-id="e07b3-158">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e07b3-158">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="e07b3-159">System. String Microsoft. Azure. Commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="e07b3-159">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="e07b3-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e07b3-160">OUTPUTS</span></span>

### <span data-ttu-id="e07b3-161">Microsoft. Azure. Commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="e07b3-161">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="e07b3-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e07b3-162">NOTES</span></span>
<span data-ttu-id="e07b3-163">Słowa kluczowe: Azure, azurerm, ARM, zasób, łączność, zarządzanie, Menedżer, Sieć, Sieć, obserwator sieci, monitor połączenia</span><span class="sxs-lookup"><span data-stu-id="e07b3-163">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="e07b3-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e07b3-164">RELATED LINKS</span></span>
<span data-ttu-id="e07b3-165">[Nowe — AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="e07b3-165">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="e07b3-166">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="e07b3-166">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="e07b3-167">[Nowe — AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [Nowe — AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Zatrzymaj — AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="e07b3-167">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="e07b3-168">[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md) 
 [Start — AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="e07b3-168">[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)
[Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)
[Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)</span></span>

