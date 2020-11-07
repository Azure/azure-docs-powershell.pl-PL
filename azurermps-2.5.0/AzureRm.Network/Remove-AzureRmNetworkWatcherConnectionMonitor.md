---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcher
schema: 2.0.0
ms.openlocfilehash: 046a2ee4591eb345efd71163d27140799cb229e2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898697"
---
# <span data-ttu-id="91edb-101">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="91edb-101">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="91edb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="91edb-102">SYNOPSIS</span></span>
<span data-ttu-id="91edb-103">Usuwanie monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="91edb-103">Remove connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91edb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="91edb-104">SYNTAX</span></span>

### <span data-ttu-id="91edb-105">SetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="91edb-105">SetByResource (Default)</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="91edb-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="91edb-106">SetByName</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="91edb-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="91edb-107">SetByLocation</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="91edb-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="91edb-108">SetByResourceId</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="91edb-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="91edb-109">SetByInputObject</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="91edb-110">Opis</span><span class="sxs-lookup"><span data-stu-id="91edb-110">DESCRIPTION</span></span>
<span data-ttu-id="91edb-111">Polecenie cmdlet Remove-AzureRmNetworkWatcherConnectionMonitor umożliwia usunięcie określonego monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="91edb-111">The remove-AzureRmNetworkWatcherConnectionMonitor cmdlet removes the specified connection monitor.</span></span>

## <span data-ttu-id="91edb-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="91edb-112">EXAMPLES</span></span>

### <span data-ttu-id="91edb-113">---------------Przykład 1: usuwanie określonego monitora połączeń---------------</span><span class="sxs-lookup"><span data-stu-id="91edb-113">---------------  Example 1: Remove the specified connection monitor ---------------</span></span>
```
PS C:\> Remove-AzureRmNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm
```

<span data-ttu-id="91edb-114">W tym przykładzie został usunięty monitor połączenia określony przez lokalizację i nazwę.</span><span class="sxs-lookup"><span data-stu-id="91edb-114">In this example we delete the connection monitor specified by location and name.</span></span>

## <span data-ttu-id="91edb-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="91edb-115">PARAMETERS</span></span>

### <span data-ttu-id="91edb-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91edb-116">-AsJob</span></span>
<span data-ttu-id="91edb-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="91edb-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="91edb-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="91edb-118">-Confirm</span></span>
<span data-ttu-id="91edb-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91edb-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91edb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91edb-120">-DefaultProfile</span></span>
<span data-ttu-id="91edb-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="91edb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91edb-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="91edb-122">-InputObject</span></span>
<span data-ttu-id="91edb-123">Obiekt monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="91edb-123">Connection monitor object.</span></span>

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

### <span data-ttu-id="91edb-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="91edb-124">-Location</span></span>
<span data-ttu-id="91edb-125">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="91edb-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="91edb-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="91edb-126">-Name</span></span>
<span data-ttu-id="91edb-127">Nazwa monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="91edb-127">The connection monitor name.</span></span>

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

### <span data-ttu-id="91edb-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="91edb-128">-NetworkWatcher</span></span>
<span data-ttu-id="91edb-129">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="91edb-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="91edb-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="91edb-130">-NetworkWatcherName</span></span>
<span data-ttu-id="91edb-131">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="91edb-131">The name of network watcher.</span></span>

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

### <span data-ttu-id="91edb-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="91edb-132">-PassThru</span></span>
<span data-ttu-id="91edb-133">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="91edb-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="91edb-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91edb-134">-ResourceGroupName</span></span>
<span data-ttu-id="91edb-135">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="91edb-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="91edb-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="91edb-136">-ResourceId</span></span>
<span data-ttu-id="91edb-137">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="91edb-137">Resource ID.</span></span>

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

### <span data-ttu-id="91edb-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91edb-138">-WhatIf</span></span>
<span data-ttu-id="91edb-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91edb-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91edb-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="91edb-140">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="91edb-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="91edb-141">INPUTS</span></span>

### <span data-ttu-id="91edb-142">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="91edb-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="91edb-143">System. String Microsoft. Azure. Commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="91edb-143">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="91edb-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="91edb-144">OUTPUTS</span></span>

### <span data-ttu-id="91edb-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="91edb-145">System.Boolean</span></span>


## <span data-ttu-id="91edb-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="91edb-146">NOTES</span></span>
<span data-ttu-id="91edb-147">Słowa kluczowe: Azure, azurerm, ARM, zasób, łączność, zarządzanie, Menedżer, Sieć, Sieć, obserwator sieci, monitor połączenia</span><span class="sxs-lookup"><span data-stu-id="91edb-147">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="91edb-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="91edb-148">RELATED LINKS</span></span>
<span data-ttu-id="91edb-149">[Nowe — AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md) 
 [Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md) 
 [Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="91edb-149">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="91edb-150">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="91edb-150">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="91edb-151">[Nowe — AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [Nowe — AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [Zatrzymaj — AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="91edb-151">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="91edb-152">[Nowe — AzureRmNetworkWatcherConnectionMonitor](./New-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)</span><span class="sxs-lookup"><span data-stu-id="91edb-152">[New-AzureRmNetworkWatcherConnectionMonitor](./New-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)</span></span>

