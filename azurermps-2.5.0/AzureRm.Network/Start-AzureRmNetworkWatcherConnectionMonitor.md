---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: c8464183646ee9a78bad4f8f94a8e2093ad6b21d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897850"
---
# <span data-ttu-id="69400-101">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="69400-101">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="69400-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="69400-102">SYNOPSIS</span></span>
<span data-ttu-id="69400-103">Uruchamianie monitora połączeń</span><span class="sxs-lookup"><span data-stu-id="69400-103">Start a connection monitor</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69400-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="69400-104">SYNTAX</span></span>

### <span data-ttu-id="69400-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="69400-105">SetByResource (Default)</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="69400-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="69400-106">SetByName</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="69400-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="69400-107">SetByLocation</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="69400-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="69400-108">SetByResourceId</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="69400-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="69400-109">SetByInputObject</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="69400-110">Opis</span><span class="sxs-lookup"><span data-stu-id="69400-110">DESCRIPTION</span></span>
<span data-ttu-id="69400-111">Polecenie cmdlet Start-AzureRmNetworkWatcherConnectionMonitor uruchamia określony monitor połączeń.</span><span class="sxs-lookup"><span data-stu-id="69400-111">The Start-AzureRmNetworkWatcherConnectionMonitor cmdlet starts the specified connection monitor.</span></span>

## <span data-ttu-id="69400-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="69400-112">EXAMPLES</span></span>

### <span data-ttu-id="69400-113">---------------Przykład 1: uruchamianie monitora połączeń---------------</span><span class="sxs-lookup"><span data-stu-id="69400-113">---------------  Example 1: Start a connection monitor ---------------</span></span>
```
PS C:\> Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName NetworkWatcher_centraluseuap -ResourceGroupName NetworkWatcherRG -Name cm
```

<span data-ttu-id="69400-114">W tym przykładzie monitor połączeń określony przez nazwę i Monitor sieci został uruchomiony.</span><span class="sxs-lookup"><span data-stu-id="69400-114">In this example we start connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="69400-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="69400-115">PARAMETERS</span></span>

### <span data-ttu-id="69400-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69400-116">-AsJob</span></span>
<span data-ttu-id="69400-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="69400-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="69400-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="69400-118">-Confirm</span></span>
<span data-ttu-id="69400-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69400-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69400-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69400-120">-DefaultProfile</span></span>
<span data-ttu-id="69400-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="69400-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69400-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="69400-122">-InputObject</span></span>
<span data-ttu-id="69400-123">Obiekt monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="69400-123">Connection monitor object.</span></span>

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

### <span data-ttu-id="69400-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="69400-124">-Location</span></span>
<span data-ttu-id="69400-125">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="69400-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="69400-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="69400-126">-Name</span></span>
<span data-ttu-id="69400-127">Nazwa monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="69400-127">The connection monitor name.</span></span>

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

### <span data-ttu-id="69400-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="69400-128">-NetworkWatcher</span></span>
<span data-ttu-id="69400-129">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="69400-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="69400-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="69400-130">-NetworkWatcherName</span></span>
<span data-ttu-id="69400-131">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="69400-131">The name of network watcher.</span></span>

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

### <span data-ttu-id="69400-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69400-132">-PassThru</span></span>
<span data-ttu-id="69400-133">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="69400-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="69400-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69400-134">-ResourceGroupName</span></span>
<span data-ttu-id="69400-135">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="69400-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="69400-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69400-136">-ResourceId</span></span>
<span data-ttu-id="69400-137">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="69400-137">Resource ID.</span></span>

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

### <span data-ttu-id="69400-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69400-138">-WhatIf</span></span>
<span data-ttu-id="69400-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69400-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69400-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="69400-140">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="69400-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69400-141">INPUTS</span></span>

### <span data-ttu-id="69400-142">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="69400-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="69400-143">System. String Microsoft. Azure. Commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="69400-143">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="69400-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="69400-144">OUTPUTS</span></span>

### <span data-ttu-id="69400-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="69400-145">System.Boolean</span></span>


## <span data-ttu-id="69400-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="69400-146">NOTES</span></span>
<span data-ttu-id="69400-147">Słowa kluczowe: Azure, azurerm, ARM, zasób, łączność, zarządzanie, Menedżer, Sieć, Sieć, obserwator sieci, monitor połączenia</span><span class="sxs-lookup"><span data-stu-id="69400-147">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="69400-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="69400-148">RELATED LINKS</span></span>
<span data-ttu-id="69400-149">[Nowe — AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md) 
 [Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md) 
 [Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="69400-149">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="69400-150">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="69400-150">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="69400-151">[Nowe — AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [Nowe — AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [Zatrzymaj — AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="69400-151">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="69400-152">[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Set-AzureRmNetworkWatcherConnectionMonitor](./Set-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Zatrzymaj — AzureRmNetworkWatcherConnectionMonitor](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="69400-152">[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)
[Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)
[Set-AzureRmNetworkWatcherConnectionMonitor](./Set-AzureRmNetworkWatcherConnectionMonitor.md)
[Stop-AzureRmNetworkWatcherConnectionMonitor](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)</span></span>
