---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcher
schema: 2.0.0
ms.openlocfilehash: 3e5853d99157fef87c2f02c2be9fab7bb983d1ae
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898704"
---
# <span data-ttu-id="0598e-101">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0598e-101">New-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="0598e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0598e-102">SYNOPSIS</span></span>
<span data-ttu-id="0598e-103">Umożliwia utworzenie monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="0598e-103">Creates a connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0598e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0598e-104">SYNTAX</span></span>

### <span data-ttu-id="0598e-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0598e-105">SetByResource (Default)</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="0598e-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="0598e-106">SetByName</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="0598e-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="0598e-107">SetByLocation</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="0598e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="0598e-108">DESCRIPTION</span></span>
<span data-ttu-id="0598e-109">Polecenie cmdlet New-AzureRmNetworkWatcherConnectionMonitor rcreates monitorze połączeń dla określonego źródła i miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="0598e-109">The New-AzureRmNetworkWatcherConnectionMonitor cmdlet rcreates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="0598e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0598e-110">EXAMPLES</span></span>

### <span data-ttu-id="0598e-111">---------------Przykład 1: Tworzenie monitora połączeń dla maszyny wirtualnej i lokalizacji docelowej w Internecie---------------</span><span class="sxs-lookup"><span data-stu-id="0598e-111">---------------  Example 1: Create a connection monitor for a vm and internet destination ---------------</span></span>
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

<span data-ttu-id="0598e-112">Polecenie cmdlet New-AzureRmNetworkWatcherConnectionMonitor tworzy monitor połączenia dla określonego źródła i miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="0598e-112">The New-AzureRmNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="0598e-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0598e-113">PARAMETERS</span></span>

### <span data-ttu-id="0598e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0598e-114">-AsJob</span></span>
<span data-ttu-id="0598e-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0598e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0598e-116">-Autostart</span><span class="sxs-lookup"><span data-stu-id="0598e-116">-AutoStart</span></span>
<span data-ttu-id="0598e-117">Automatyczne uruchomienie.</span><span class="sxs-lookup"><span data-stu-id="0598e-117">Auto start.</span></span>

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

### <span data-ttu-id="0598e-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0598e-118">-Confirm</span></span>
<span data-ttu-id="0598e-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0598e-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0598e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0598e-120">-DefaultProfile</span></span>
<span data-ttu-id="0598e-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0598e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0598e-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="0598e-122">-DestinationAddress</span></span>
<span data-ttu-id="0598e-123">Adres IP miejsca docelowego monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="0598e-123">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="0598e-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="0598e-124">-DestinationPort</span></span>
<span data-ttu-id="0598e-125">Port docelowy.</span><span class="sxs-lookup"><span data-stu-id="0598e-125">Destination port.</span></span>

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

### <span data-ttu-id="0598e-126">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="0598e-126">-DestinationResourceId</span></span>
<span data-ttu-id="0598e-127">Identyfikator miejsca docelowego monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="0598e-127">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="0598e-128">-Force</span><span class="sxs-lookup"><span data-stu-id="0598e-128">-Force</span></span>
<span data-ttu-id="0598e-129">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="0598e-129">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="0598e-130">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="0598e-130">-Location</span></span>
<span data-ttu-id="0598e-131">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="0598e-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="0598e-132">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="0598e-132">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="0598e-133">Interwał monitorowania w sekundach.</span><span class="sxs-lookup"><span data-stu-id="0598e-133">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="0598e-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0598e-134">-Name</span></span>
<span data-ttu-id="0598e-135">Nazwa monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="0598e-135">The connection monitor name.</span></span>

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

### <span data-ttu-id="0598e-136">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0598e-136">-NetworkWatcher</span></span>
<span data-ttu-id="0598e-137">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="0598e-137">The network watcher resource.</span></span>

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

### <span data-ttu-id="0598e-138">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="0598e-138">-NetworkWatcherName</span></span>
<span data-ttu-id="0598e-139">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="0598e-139">The name of network watcher.</span></span>

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

### <span data-ttu-id="0598e-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0598e-140">-ResourceGroupName</span></span>
<span data-ttu-id="0598e-141">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="0598e-141">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="0598e-142">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="0598e-142">-SourcePort</span></span>
<span data-ttu-id="0598e-143">Port źródłowy.</span><span class="sxs-lookup"><span data-stu-id="0598e-143">Source port.</span></span>

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

### <span data-ttu-id="0598e-144">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="0598e-144">-SourceResourceId</span></span>
<span data-ttu-id="0598e-145">Identyfikator źródła monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="0598e-145">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="0598e-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="0598e-146">-Tag</span></span>
<span data-ttu-id="0598e-147">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="0598e-147">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="0598e-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0598e-148">-WhatIf</span></span>
<span data-ttu-id="0598e-149">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0598e-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0598e-150">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0598e-150">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="0598e-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0598e-151">INPUTS</span></span>

### <span data-ttu-id="0598e-152">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0598e-152">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="0598e-153">System. String</span><span class="sxs-lookup"><span data-stu-id="0598e-153">System.String</span></span>


## <span data-ttu-id="0598e-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0598e-154">OUTPUTS</span></span>

### <span data-ttu-id="0598e-155">Microsoft. Azure. Commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="0598e-155">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="0598e-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0598e-156">NOTES</span></span>
<span data-ttu-id="0598e-157">Słowa kluczowe: Azure, azurerm, ARM, zasób, łączność, zarządzanie, Menedżer, Sieć, Sieć, obserwator sieci, monitor połączenia</span><span class="sxs-lookup"><span data-stu-id="0598e-157">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="0598e-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0598e-158">RELATED LINKS</span></span>
<span data-ttu-id="0598e-159">[Nowe — AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md) 
 [Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md) 
 [Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="0598e-159">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="0598e-160">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="0598e-160">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="0598e-161">[Nowe — AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [Nowe — AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [Zatrzymaj — AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="0598e-161">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="0598e-162">[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="0598e-162">[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)
[Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)</span></span>
