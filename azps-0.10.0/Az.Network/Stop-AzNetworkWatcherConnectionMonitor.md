---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Stop-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Stop-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: f69910140f2bd7b57a30bd413c74e6f26e646787
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892677"
---
# <span data-ttu-id="19fd1-101">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="19fd1-101">Stop-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="19fd1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="19fd1-102">SYNOPSIS</span></span>
<span data-ttu-id="19fd1-103">Zatrzymywanie monitora połączeń</span><span class="sxs-lookup"><span data-stu-id="19fd1-103">Stop a connection monitor</span></span>

## <span data-ttu-id="19fd1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="19fd1-104">SYNTAX</span></span>

### <span data-ttu-id="19fd1-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="19fd1-105">SetByResource (Default)</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="19fd1-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="19fd1-106">SetByName</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="19fd1-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="19fd1-107">SetByLocation</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="19fd1-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="19fd1-108">SetByResourceId</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="19fd1-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="19fd1-109">SetByInputObject</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="19fd1-110">Opis</span><span class="sxs-lookup"><span data-stu-id="19fd1-110">DESCRIPTION</span></span>
<span data-ttu-id="19fd1-111">Polecenie cmdlet Stop-AzNetworkWatcherConnectionMonitor powoduje zatrzymanie określonego monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="19fd1-111">The Stop-AzNetworkWatcherConnectionMonitor cmdlet stops the specified connection monitor.</span></span>

## <span data-ttu-id="19fd1-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="19fd1-112">EXAMPLES</span></span>

### <span data-ttu-id="19fd1-113">---------------Przykład 1: zatrzymywanie monitora połączeń---------------</span><span class="sxs-lookup"><span data-stu-id="19fd1-113">---------------  Example 1: Stop a connection monitor ---------------</span></span>
```
PS C:\> Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm
```

<span data-ttu-id="19fd1-114">W tym przykładzie zatrzymano monitor połączenia określony przez nazwę i Monitor sieci</span><span class="sxs-lookup"><span data-stu-id="19fd1-114">In this example we stop connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="19fd1-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="19fd1-115">PARAMETERS</span></span>

### <span data-ttu-id="19fd1-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="19fd1-116">-AsJob</span></span>
<span data-ttu-id="19fd1-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="19fd1-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="19fd1-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="19fd1-118">-Confirm</span></span>
<span data-ttu-id="19fd1-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19fd1-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19fd1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19fd1-120">-DefaultProfile</span></span>
<span data-ttu-id="19fd1-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="19fd1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19fd1-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="19fd1-122">-InputObject</span></span>
<span data-ttu-id="19fd1-123">Obiekt monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="19fd1-123">Connection monitor object.</span></span>

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

### <span data-ttu-id="19fd1-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="19fd1-124">-Location</span></span>
<span data-ttu-id="19fd1-125">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="19fd1-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="19fd1-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="19fd1-126">-Name</span></span>
<span data-ttu-id="19fd1-127">Nazwa monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="19fd1-127">The connection monitor name.</span></span>

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

### <span data-ttu-id="19fd1-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="19fd1-128">-NetworkWatcher</span></span>
<span data-ttu-id="19fd1-129">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="19fd1-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="19fd1-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="19fd1-130">-NetworkWatcherName</span></span>
<span data-ttu-id="19fd1-131">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="19fd1-131">The name of network watcher.</span></span>

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

### <span data-ttu-id="19fd1-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19fd1-132">-PassThru</span></span>
<span data-ttu-id="19fd1-133">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="19fd1-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="19fd1-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19fd1-134">-ResourceGroupName</span></span>
<span data-ttu-id="19fd1-135">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="19fd1-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="19fd1-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="19fd1-136">-ResourceId</span></span>
<span data-ttu-id="19fd1-137">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="19fd1-137">Resource ID.</span></span>

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

### <span data-ttu-id="19fd1-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19fd1-138">-WhatIf</span></span>
<span data-ttu-id="19fd1-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19fd1-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19fd1-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="19fd1-140">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="19fd1-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="19fd1-141">INPUTS</span></span>

### <span data-ttu-id="19fd1-142">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="19fd1-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="19fd1-143">System. String Microsoft. Azure. Commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="19fd1-143">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="19fd1-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="19fd1-144">OUTPUTS</span></span>

### <span data-ttu-id="19fd1-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="19fd1-145">System.Boolean</span></span>


## <span data-ttu-id="19fd1-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="19fd1-146">NOTES</span></span>
<span data-ttu-id="19fd1-147">Słowa kluczowe: Azure, azurerm, ARM, zasób, łączność, zarządzanie, Menedżer, Sieć, Sieć, obserwator sieci, monitor połączenia</span><span class="sxs-lookup"><span data-stu-id="19fd1-147">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="19fd1-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="19fd1-148">RELATED LINKS</span></span>
<span data-ttu-id="19fd1-149">[Nowe — AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="19fd1-149">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="19fd1-150">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="19fd1-150">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="19fd1-151">[Nowe — AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [Nowe — AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Zatrzymaj — AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="19fd1-151">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="19fd1-152">[Nowe — AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md) 
 [Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md) 
 [Start — AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="19fd1-152">[New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)
[Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)
[Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md)
[Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)</span></span>