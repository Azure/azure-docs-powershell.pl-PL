---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: bfdcfbf57f44479ad35a2b9075590a0d40351ec9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890449"
---
# <span data-ttu-id="6d6ff-101">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6d6ff-101">New-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="6d6ff-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6d6ff-102">SYNOPSIS</span></span>
<span data-ttu-id="6d6ff-103">Umożliwia utworzenie monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="6d6ff-103">Creates a connection monitor.</span></span>

## <span data-ttu-id="6d6ff-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6d6ff-104">SYNTAX</span></span>

### <span data-ttu-id="6d6ff-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6d6ff-105">SetByResource (Default)</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="6d6ff-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="6d6ff-106">SetByName</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="6d6ff-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="6d6ff-107">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="6d6ff-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6d6ff-108">DESCRIPTION</span></span>
<span data-ttu-id="6d6ff-109">Polecenie cmdlet New-AzNetworkWatcherConnectionMonitor rcreates monitorze połączeń dla określonego źródła i miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="6d6ff-109">The New-AzNetworkWatcherConnectionMonitor cmdlet rcreates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="6d6ff-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6d6ff-110">EXAMPLES</span></span>

### <span data-ttu-id="6d6ff-111">---------------Przykład 1: Tworzenie monitora połączeń dla maszyny wirtualnej i lokalizacji docelowej w Internecie---------------</span><span class="sxs-lookup"><span data-stu-id="6d6ff-111">---------------  Example 1: Create a connection monitor for a vm and internet destination ---------------</span></span>
```
PS C:\> New-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm -DestinationAddress bing.com -DestinationPort 80

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

<span data-ttu-id="6d6ff-112">Polecenie cmdlet New-AzNetworkWatcherConnectionMonitor tworzy monitor połączenia dla określonego źródła i miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="6d6ff-112">The New-AzNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="6d6ff-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6d6ff-113">PARAMETERS</span></span>

### <span data-ttu-id="6d6ff-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d6ff-114">-AsJob</span></span>
<span data-ttu-id="6d6ff-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6d6ff-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6d6ff-116">-Autostart</span><span class="sxs-lookup"><span data-stu-id="6d6ff-116">-AutoStart</span></span>
<span data-ttu-id="6d6ff-117">Automatyczne uruchomienie.</span><span class="sxs-lookup"><span data-stu-id="6d6ff-117">Auto start.</span></span>

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

### <span data-ttu-id="6d6ff-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6d6ff-118">-Confirm</span></span>
<span data-ttu-id="6d6ff-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d6ff-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d6ff-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d6ff-120">-DefaultProfile</span></span>
<span data-ttu-id="6d6ff-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6d6ff-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d6ff-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="6d6ff-122">-DestinationAddress</span></span>
<span data-ttu-id="6d6ff-123">Adres IP miejsca docelowego monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="6d6ff-123">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="6d6ff-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="6d6ff-124">-DestinationPort</span></span>
<span data-ttu-id="6d6ff-125">Port docelowy.</span><span class="sxs-lookup"><span data-stu-id="6d6ff-125">Destination port.</span></span>

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

### <span data-ttu-id="6d6ff-126">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="6d6ff-126">-DestinationResourceId</span></span>
<span data-ttu-id="6d6ff-127">Identyfikator miejsca docelowego monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="6d6ff-127">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="6d6ff-128">-Force</span><span class="sxs-lookup"><span data-stu-id="6d6ff-128">-Force</span></span>
<span data-ttu-id="6d6ff-129">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="6d6ff-129">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="6d6ff-130">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="6d6ff-130">-Location</span></span>
<span data-ttu-id="6d6ff-131">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="6d6ff-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="6d6ff-132">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="6d6ff-132">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="6d6ff-133">Interwał monitorowania w sekundach.</span><span class="sxs-lookup"><span data-stu-id="6d6ff-133">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="6d6ff-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6d6ff-134">-Name</span></span>
<span data-ttu-id="6d6ff-135">Nazwa monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="6d6ff-135">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d6ff-136">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6d6ff-136">-NetworkWatcher</span></span>
<span data-ttu-id="6d6ff-137">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="6d6ff-137">The network watcher resource.</span></span>

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

### <span data-ttu-id="6d6ff-138">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="6d6ff-138">-NetworkWatcherName</span></span>
<span data-ttu-id="6d6ff-139">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="6d6ff-139">The name of network watcher.</span></span>

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

### <span data-ttu-id="6d6ff-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d6ff-140">-ResourceGroupName</span></span>
<span data-ttu-id="6d6ff-141">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="6d6ff-141">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="6d6ff-142">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="6d6ff-142">-SourcePort</span></span>
<span data-ttu-id="6d6ff-143">Port źródłowy.</span><span class="sxs-lookup"><span data-stu-id="6d6ff-143">Source port.</span></span>

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

### <span data-ttu-id="6d6ff-144">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="6d6ff-144">-SourceResourceId</span></span>
<span data-ttu-id="6d6ff-145">Identyfikator źródła monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="6d6ff-145">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="6d6ff-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="6d6ff-146">-Tag</span></span>
<span data-ttu-id="6d6ff-147">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="6d6ff-147">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="6d6ff-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d6ff-148">-WhatIf</span></span>
<span data-ttu-id="6d6ff-149">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d6ff-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d6ff-150">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6d6ff-150">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="6d6ff-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6d6ff-151">INPUTS</span></span>

### <span data-ttu-id="6d6ff-152">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6d6ff-152">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="6d6ff-153">System. String</span><span class="sxs-lookup"><span data-stu-id="6d6ff-153">System.String</span></span>


## <span data-ttu-id="6d6ff-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6d6ff-154">OUTPUTS</span></span>

### <span data-ttu-id="6d6ff-155">Microsoft. Azure. Commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="6d6ff-155">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="6d6ff-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6d6ff-156">NOTES</span></span>
<span data-ttu-id="6d6ff-157">Słowa kluczowe: Azure, azurerm, ARM, zasób, łączność, zarządzanie, Menedżer, Sieć, Sieć, obserwator sieci, monitor połączenia</span><span class="sxs-lookup"><span data-stu-id="6d6ff-157">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="6d6ff-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6d6ff-158">RELATED LINKS</span></span>
<span data-ttu-id="6d6ff-159">[Nowe — AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="6d6ff-159">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="6d6ff-160">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="6d6ff-160">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="6d6ff-161">[Nowe — AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [Nowe — AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Zatrzymaj — AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="6d6ff-161">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="6d6ff-162">[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="6d6ff-162">[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)
[Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)</span></span>
