---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherConnectionMonitorReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherConnectionMonitorReport.md
ms.openlocfilehash: 6e5f7370740e069bc3c8ce5f83ef2e784cc4012a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718296"
---
# <span data-ttu-id="38e9a-101">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="38e9a-101">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>

## <span data-ttu-id="38e9a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="38e9a-102">SYNOPSIS</span></span>
<span data-ttu-id="38e9a-103">Zbadanie migawki najnowszych Stanów połączeń.</span><span class="sxs-lookup"><span data-stu-id="38e9a-103">Query a snapshot of the most recent connection states.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38e9a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="38e9a-104">SYNTAX</span></span>

### <span data-ttu-id="38e9a-105">SetByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="38e9a-105">SetByName (Default)</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitorReport -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38e9a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="38e9a-106">SetByResource</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitorReport -NetworkWatcher <PSNetworkWatcher> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38e9a-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="38e9a-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitorReport -Location <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38e9a-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="38e9a-108">SetByResourceId</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitorReport -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38e9a-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="38e9a-109">SetByInputObject</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitorReport -InputObject <PSConnectionMonitorResult> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38e9a-110">Opis</span><span class="sxs-lookup"><span data-stu-id="38e9a-110">DESCRIPTION</span></span>
<span data-ttu-id="38e9a-111">Polecenie cmdlet Get-AzureRmNetworkWatcherConnectionMonitorReport zwraca raport na temat najnowszych Stanów połączeń.</span><span class="sxs-lookup"><span data-stu-id="38e9a-111">The Get-AzureRmNetworkWatcherConnectionMonitorReport cmdlet returns the report on the most recent connection states.</span></span>

## <span data-ttu-id="38e9a-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="38e9a-112">EXAMPLES</span></span>

### <span data-ttu-id="38e9a-113">Przykład 1: Uzyskiwanie najnowszej migawki połączenia monitora połączeń według nazwy w określonej lokalizacji</span><span class="sxs-lookup"><span data-stu-id="38e9a-113">Example 1: Get the most recent connection snapshot of the connection monitor by name in the specified location</span></span>
```
PS C:\> Get-AzureRmNetworkWatcherConnectionMonitorReport -Location centraluseuap -Name cm


States : [
           {
             "ConnectionState": "Reachable",
             "StartTime": "2018-01-12T01:18:20Z",
             "EvaluationState": "Completed",
             "Hops": [
               {
                 "Type": "Source",
                 "Id": "1530e0f2-c9b7-4bc0-a205-cf7332cd8983",
                 "Address": "10.1.1.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "b19b74b1-423d-4f0b-99cd-bcaed4d0b8a2"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualAppliance",
                 "Id": "b19b74b1-423d-4f0b-99cd-bcaed4d0b8a2",
                 "Address": "10.1.2.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/fwNic/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "80e46c56-2cf9-4106-8602-608a74832d41"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualAppliance",
                 "Id": "80e46c56-2cf9-4106-8602-608a74832d41",
                 "Address": "10.1.3.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/auNic/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "e17cf884-69db-43b8-9cd5-f920770a0dbe"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualNetwork",
                 "Id": "e17cf884-69db-43b8-9cd5-f920770a0dbe",
                 "Address": "10.1.4.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/dbNic0/ipConfigurations/ipconfig1",
                 "NextHopIds": [],
                 "Issues": []
               }
             ]
           },
           {
             "ConnectionState": "Unreachable",
             "StartTime": "2018-01-12T01:14:11Z",
             "EvaluationState": "Completed",
             "Hops": [
               {
                 "Type": "Source",
                 "Id": "b6251ff8-3d07-4fdf-98f8-04b168e1cf90",
                 "Address": "10.1.1.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "de6d463b-47fb-4beb-afc4-d77782755313"
                 ],
                 "Issues": [
                   {
                     "Origin": "Local",
                     "Severity": "Error",
                     "Type": "NetworkError",
                     "Context": []
                   }
                 ]
               },
               {
                 "Type": "VirtualAppliance",
                 "Id": "de6d463b-47fb-4beb-afc4-d77782755313",
                 "Address": "10.1.2.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/fwNic/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "0cbadb7e-cd99-4fa9-a832-eb4e0d112293"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualAppliance",
                 "Id": "0cbadb7e-cd99-4fa9-a832-eb4e0d112293",
                 "Address": "10.1.3.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/auNic/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "538005d1-994a-4350-9866-6985385beecf"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualNetwork",
                 "Id": "538005d1-994a-4350-9866-6985385beecf",
                 "Address": "10.1.4.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/dbNic0/ipConfigurations/ipconfig1",
                 "NextHopIds": [],
                 "Issues": []
               }
             ]
           },
           {
             "ConnectionState": "Reachable",
             "StartTime": "2018-01-11T23:54:05Z",
             "EvaluationState": "Completed",
             "Hops": [
               {
                 "Type": "Source",
                 "Id": "3dbec7e8-a37f-4acd-bc5f-86918fffba0e",
                 "Address": "10.1.1.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "1a87cf61-1be6-4add-bba7-f84afbcf3726"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualAppliance",
                 "Id": "1a87cf61-1be6-4add-bba7-f84afbcf3726",
                 "Address": "10.1.2.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/fwNic/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "070c0740-308e-43ba-b72f-5d8d5a6537ec"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualAppliance",
                 "Id": "070c0740-308e-43ba-b72f-5d8d5a6537ec",
                 "Address": "10.1.3.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/auNic/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "760182e1-c88d-4cfc-a711-65e7e622a67a"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualNetwork",
                 "Id": "760182e1-c88d-4cfc-a711-65e7e622a67a",
                 "Address": "10.1.4.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/dbNic0/ipConfigurations/ipconfig1",
                 "NextHopIds": [],
                 "Issues": []
               }
             ]
           }
         ]
```

<span data-ttu-id="38e9a-114">W tym przykładzie zbadano ostatnie Stany połączeń określonego monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="38e9a-114">In this example we query the most recent connection states of the specified connection monitor.</span></span>

## <span data-ttu-id="38e9a-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="38e9a-115">PARAMETERS</span></span>

### <span data-ttu-id="38e9a-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="38e9a-116">-AsJob</span></span>
<span data-ttu-id="38e9a-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="38e9a-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="38e9a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38e9a-118">-DefaultProfile</span></span>
<span data-ttu-id="38e9a-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="38e9a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38e9a-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="38e9a-120">-InputObject</span></span>
<span data-ttu-id="38e9a-121">Obiekt monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="38e9a-121">Connection monitor object.</span></span>

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

### <span data-ttu-id="38e9a-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="38e9a-122">-Location</span></span>
<span data-ttu-id="38e9a-123">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="38e9a-123">Location of the network watcher.</span></span>

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

### <span data-ttu-id="38e9a-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="38e9a-124">-Name</span></span>
<span data-ttu-id="38e9a-125">Nazwa monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="38e9a-125">The connection monitor name.</span></span>

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

### <span data-ttu-id="38e9a-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="38e9a-126">-NetworkWatcher</span></span>
<span data-ttu-id="38e9a-127">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="38e9a-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="38e9a-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="38e9a-128">-NetworkWatcherName</span></span>
<span data-ttu-id="38e9a-129">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="38e9a-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="38e9a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38e9a-130">-ResourceGroupName</span></span>
<span data-ttu-id="38e9a-131">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="38e9a-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="38e9a-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38e9a-132">-ResourceId</span></span>
<span data-ttu-id="38e9a-133">Identyfikator zasobu monitora połączeń.</span><span class="sxs-lookup"><span data-stu-id="38e9a-133">Resource ID of the connection monitor.</span></span>

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

### <span data-ttu-id="38e9a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38e9a-134">CommonParameters</span></span>
<span data-ttu-id="38e9a-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38e9a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38e9a-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38e9a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38e9a-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="38e9a-137">INPUTS</span></span>

### <span data-ttu-id="38e9a-138">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="38e9a-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="38e9a-139">Parametry: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="38e9a-139">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="38e9a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="38e9a-140">System.String</span></span>

### <span data-ttu-id="38e9a-141">Microsoft. Azure. Commands. Network. models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="38e9a-141">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>
<span data-ttu-id="38e9a-142">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="38e9a-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="38e9a-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="38e9a-143">OUTPUTS</span></span>

### <span data-ttu-id="38e9a-144">Microsoft. Azure. Commands. Network. models. PSConnectionMonitorQueryResult</span><span class="sxs-lookup"><span data-stu-id="38e9a-144">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorQueryResult</span></span>

## <span data-ttu-id="38e9a-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="38e9a-145">NOTES</span></span>
<span data-ttu-id="38e9a-146">Słowa kluczowe: Azure, azurerm, ARM, zasób, łączność, zarządzanie, Menedżer, Sieć, Sieć, obserwator sieci, monitor połączenia</span><span class="sxs-lookup"><span data-stu-id="38e9a-146">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="38e9a-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="38e9a-147">RELATED LINKS</span></span>

[<span data-ttu-id="38e9a-148">Nowe — AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="38e9a-148">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="38e9a-149">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="38e9a-149">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="38e9a-150">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="38e9a-150">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="38e9a-151">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="38e9a-151">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="38e9a-152">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="38e9a-152">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="38e9a-153">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="38e9a-153">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="38e9a-154">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="38e9a-154">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="38e9a-155">Nowe — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="38e9a-155">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="38e9a-156">Nowe — AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="38e9a-156">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="38e9a-157">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="38e9a-157">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="38e9a-158">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="38e9a-158">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="38e9a-159">Zatrzymaj — AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="38e9a-159">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="38e9a-160">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="38e9a-160">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="38e9a-161">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="38e9a-161">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="38e9a-162">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="38e9a-162">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="38e9a-163">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="38e9a-163">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="38e9a-164">Zatrzymaj — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="38e9a-164">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="38e9a-165">Nowe — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="38e9a-165">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="38e9a-166">Nowe — AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="38e9a-166">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>]()

[<span data-ttu-id="38e9a-167">Test — AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="38e9a-167">Test-AzureRmNetworkWatcherIPFlow</span></span>]()

[<span data-ttu-id="38e9a-168">Test — AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="38e9a-168">Test-AzureRmNetworkWatcherConnectivity</span></span>]()

[<span data-ttu-id="38e9a-169">Start — AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="38e9a-169">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>]()

[<span data-ttu-id="38e9a-170">Start — AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="38e9a-170">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="38e9a-171">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="38e9a-171">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>]()

[<span data-ttu-id="38e9a-172">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="38e9a-172">Get-AzureRMNetworkWatcherReachabilityReport</span></span>]()

[<span data-ttu-id="38e9a-173">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="38e9a-173">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>]()

[<span data-ttu-id="38e9a-174">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="38e9a-174">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>]()
