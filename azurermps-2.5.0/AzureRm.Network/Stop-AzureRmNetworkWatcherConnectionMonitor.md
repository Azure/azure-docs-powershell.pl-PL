---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: a67dde4b1e8f3f97038304086b63d02d75ff8fec
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897842"
---
# <span data-ttu-id="20ee5-101">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="20ee5-101">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="20ee5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="20ee5-102">SYNOPSIS</span></span>
<span data-ttu-id="20ee5-103">Zatrzymywanie monitora połączeń</span><span class="sxs-lookup"><span data-stu-id="20ee5-103">Stop a connection monitor</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20ee5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="20ee5-104">SYNTAX</span></span>

### <span data-ttu-id="20ee5-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="20ee5-105">SetByResource (Default)</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="20ee5-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="20ee5-106">SetByName</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="20ee5-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="20ee5-107">SetByLocation</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="20ee5-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="20ee5-108">SetByResourceId</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="20ee5-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="20ee5-109">SetByInputObject</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="20ee5-110">Opis</span><span class="sxs-lookup"><span data-stu-id="20ee5-110">DESCRIPTION</span></span>
<span data-ttu-id="20ee5-111">Polecenie cmdlet Stop-AzureRmNetworkWatcherConnectionMonitor powoduje zatrzymanie określonego monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="20ee5-111">The Stop-AzureRmNetworkWatcherConnectionMonitor cmdlet stops the specified connection monitor.</span></span>

## <span data-ttu-id="20ee5-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="20ee5-112">EXAMPLES</span></span>

### <span data-ttu-id="20ee5-113">---------------Przykład 1: zatrzymywanie monitora połączeń---------------</span><span class="sxs-lookup"><span data-stu-id="20ee5-113">---------------  Example 1: Stop a connection monitor ---------------</span></span>
```
PS C:\> Stop-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm
```

<span data-ttu-id="20ee5-114">W tym przykładzie zatrzymano monitor połączenia określony przez nazwę i Monitor sieci</span><span class="sxs-lookup"><span data-stu-id="20ee5-114">In this example we stop connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="20ee5-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="20ee5-115">PARAMETERS</span></span>

### <span data-ttu-id="20ee5-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="20ee5-116">-AsJob</span></span>
<span data-ttu-id="20ee5-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="20ee5-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="20ee5-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="20ee5-118">-Confirm</span></span>
<span data-ttu-id="20ee5-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20ee5-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20ee5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20ee5-120">-DefaultProfile</span></span>
<span data-ttu-id="20ee5-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="20ee5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20ee5-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="20ee5-122">-InputObject</span></span>
<span data-ttu-id="20ee5-123">Obiekt monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="20ee5-123">Connection monitor object.</span></span>

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

### <span data-ttu-id="20ee5-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="20ee5-124">-Location</span></span>
<span data-ttu-id="20ee5-125">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="20ee5-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="20ee5-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="20ee5-126">-Name</span></span>
<span data-ttu-id="20ee5-127">Nazwa monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="20ee5-127">The connection monitor name.</span></span>

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

### <span data-ttu-id="20ee5-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="20ee5-128">-NetworkWatcher</span></span>
<span data-ttu-id="20ee5-129">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="20ee5-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="20ee5-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="20ee5-130">-NetworkWatcherName</span></span>
<span data-ttu-id="20ee5-131">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="20ee5-131">The name of network watcher.</span></span>

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

### <span data-ttu-id="20ee5-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20ee5-132">-PassThru</span></span>
<span data-ttu-id="20ee5-133">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="20ee5-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="20ee5-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20ee5-134">-ResourceGroupName</span></span>
<span data-ttu-id="20ee5-135">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="20ee5-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="20ee5-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="20ee5-136">-ResourceId</span></span>
<span data-ttu-id="20ee5-137">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="20ee5-137">Resource ID.</span></span>

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

### <span data-ttu-id="20ee5-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20ee5-138">-WhatIf</span></span>
<span data-ttu-id="20ee5-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20ee5-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20ee5-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="20ee5-140">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="20ee5-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="20ee5-141">INPUTS</span></span>

### <span data-ttu-id="20ee5-142">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="20ee5-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="20ee5-143">System. String Microsoft. Azure. Commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="20ee5-143">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="20ee5-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="20ee5-144">OUTPUTS</span></span>

### <span data-ttu-id="20ee5-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="20ee5-145">System.Boolean</span></span>


## <span data-ttu-id="20ee5-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="20ee5-146">NOTES</span></span>
<span data-ttu-id="20ee5-147">Słowa kluczowe: Azure, azurerm, ARM, zasób, łączność, zarządzanie, Menedżer, Sieć, Sieć, obserwator sieci, monitor połączenia</span><span class="sxs-lookup"><span data-stu-id="20ee5-147">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="20ee5-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="20ee5-148">RELATED LINKS</span></span>
<span data-ttu-id="20ee5-149">[Nowe — AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md) 
 [Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md) 
 [Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="20ee5-149">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="20ee5-150">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="20ee5-150">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="20ee5-151">[Nowe — AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [Nowe — AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [Zatrzymaj — AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="20ee5-151">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="20ee5-152">[Nowe — AzureRmNetworkWatcherConnectionMonitor](./New-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Set-AzureRmNetworkWatcherConnectionMonitor](./Set-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Start — AzureRmNetworkWatcherConnectionMonitor](./Start-AzureRmNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="20ee5-152">[New-AzureRmNetworkWatcherConnectionMonitor](./New-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)
[Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)
[Set-AzureRmNetworkWatcherConnectionMonitor](./Set-AzureRmNetworkWatcherConnectionMonitor.md)
[Start-AzureRmNetworkWatcherConnectionMonitor](./Start-AzureRmNetworkWatcherConnectionMonitor.md)</span></span>
