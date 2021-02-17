---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchertopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherTopology.md
ms.openlocfilehash: 41b4494da9f10267461dab5f2a6d205d6f9f9c15
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401253"
---
# <span data-ttu-id="6eb98-101">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="6eb98-101">Get-AzNetworkWatcherTopology</span></span>

## <span data-ttu-id="6eb98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6eb98-102">SYNOPSIS</span></span>
<span data-ttu-id="6eb98-103">Pobiera widok zasobów na poziomie sieci i ich relacje w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="6eb98-103">Gets a network level view of resources and their relationships in a resource group.</span></span>

## <span data-ttu-id="6eb98-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6eb98-104">SYNTAX</span></span>

### <span data-ttu-id="6eb98-105">SetByResource (Default)</span><span class="sxs-lookup"><span data-stu-id="6eb98-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherTopology -NetworkWatcher <PSNetworkWatcher> -TargetResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6eb98-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="6eb98-106">SetByName</span></span>
```
Get-AzNetworkWatcherTopology -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6eb98-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="6eb98-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherTopology -Location <String> -TargetResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6eb98-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="6eb98-108">DESCRIPTION</span></span>
<span data-ttu-id="6eb98-109">Polecenie Get-AzNetworkWatcherTopology cmdlet widoku poziomu sieci zasobów i ich relacji w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="6eb98-109">The Get-AzNetworkWatcherTopology cmdlet a network level view of resources and their relationships in a resource group.</span></span> <span data-ttu-id="6eb98-110">Uwaga: Jeśli zasoby z wielu regionów znajdują się w grupie zasobów, w wyniku JSON zostaną uwzględnione tylko zasoby w tym samym regionie, w którym znajduje się czujka sieci.</span><span class="sxs-lookup"><span data-stu-id="6eb98-110">Note: If resources from multiple regions reside in the resource group, only the resources in the same region as the Network Watcher will be included in the JSON output.</span></span>

## <span data-ttu-id="6eb98-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6eb98-111">EXAMPLES</span></span>

### <span data-ttu-id="6eb98-112">Przykład 1. Uzyskiwanie topologii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="6eb98-112">Example 1: Get an Azure Topology</span></span>
```
$networkWatcher = Get-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG 
Get-AzNetworkWatcherTopology -NetworkWatcher $networkWatcher -ResourceGroupName testresourcegroup

Id                : e33d80cf-4f76-4b8f-b51c-5bb8eba80103
CreatedDateTime   : 0/00/0000 9:21:51 PM
LastModified      : 0/00/0000 4:53:29 AM
TopologyResources : [
                      {
                        "Name": "testresourcegroup-vnet",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/virtualNetworks/testresourcegroup-vnet",
                        "Location": "westcentralus",
                        "TopologyAssociations": [
                          {
                            "Name": "default",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/virtualNetworks/testresourcegroup-vnet/subnets/default",
                            "AssociationType": "Contains"
                          }
                        ]
                      },
                      {
                        "Name": "default",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/virtualNetworks/testresourcegroup-vnet/subnets/default",
                        "Location": "westcentralus",
                        "TopologyAssociations": []
                      },
                      {
                        "Name": "VM0",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Compute/virtualMachines/VM0",
                        "TopologyAssociations": [
                          {
                            "Name": "vm0131",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkInterfaces/vm0131",
                            "AssociationType": "Contains"
                          }
                        ]
                      },
                      {
                        "Name": "vm0131",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkInterfaces/vm0131",
                        "Location": "westcentralus",
                        "TopologyAssociations": [
                          {
                            "Name": "VM0",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Compute/virtualMachines/VM0",
                            "AssociationType": "Associated"
                          },
                          {
                            "Name": "VM0-nsg",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkSecurityGroups/VM0-nsg",
                            "AssociationType": "Associated"
                          },
                          {
                            "Name": "default",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/virtualNetworks/testresourcegroup-vnet/subnets/default",
                            "AssociationType": "Associated"
                          },
                          {
                            "Name": "VM0-ip",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/publicIPAddresses/VM0-ip",
                            "AssociationType": "Associated"
                          }
                        ]
                      },
                      {
                        "Name": "VM0-nsg",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkSecurityGroups/VM0-nsg",
                        "Location": "westcentralus",
                        "TopologyAssociations": [
                          {
                            "Name": "default-allow-rdp",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkSecurityGroups/VM0-nsg/securityRules/default-allow-rdp",
                            "AssociationType": "Contains"
                          }
                        ]
                      },
                      {
                        "Name": "default-allow-rdp",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkSecurityGroups/VM0-nsg/securityRules/default-allow-rdp",
                        "Location": "westcentralus",
                        "TopologyAssociations": []
                      },
                      {
                        "Name": "VM0-ip",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/publicIPAddresses/VM0-ip",
                        "Location": "westcentralus",
                        "TopologyAssociations": [
                          {
                            "Name": "vm0131",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkInterfaces/vm0131",
                            "AssociationType": "Associated"
                          }
                        ]
                      }
                    ]
```

<span data-ttu-id="6eb98-113">W tym przykładzie uruchamiamy polecenie cmdlet Get-AzNetworkWatcherTopology grupy zasobów zawierającej maszyny wirtualnej, nic, NSG i publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="6eb98-113">In this example we run the Get-AzNetworkWatcherTopology cmdlet on a resource group that contains a VM, Nic, NSG, and public IP.</span></span>

## <span data-ttu-id="6eb98-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6eb98-114">PARAMETERS</span></span>

### <span data-ttu-id="6eb98-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eb98-115">-DefaultProfile</span></span>
<span data-ttu-id="6eb98-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6eb98-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6eb98-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="6eb98-117">-Location</span></span>
<span data-ttu-id="6eb98-118">Lokalizacja czujki sieci.</span><span class="sxs-lookup"><span data-stu-id="6eb98-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="6eb98-119">— NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6eb98-119">-NetworkWatcher</span></span>
<span data-ttu-id="6eb98-120">Zasób obserwowania sieci.</span><span class="sxs-lookup"><span data-stu-id="6eb98-120">The network watcher resource.</span></span>

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

### <span data-ttu-id="6eb98-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="6eb98-121">-NetworkWatcherName</span></span>
<span data-ttu-id="6eb98-122">Nazwa osoby oglądacej sieć.</span><span class="sxs-lookup"><span data-stu-id="6eb98-122">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6eb98-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6eb98-123">-ResourceGroupName</span></span>
<span data-ttu-id="6eb98-124">Nazwa grupy zasobów obserwowanych sieci.</span><span class="sxs-lookup"><span data-stu-id="6eb98-124">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6eb98-125">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6eb98-125">-TargetResourceGroupName</span></span>
<span data-ttu-id="6eb98-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6eb98-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6eb98-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eb98-127">CommonParameters</span></span>
<span data-ttu-id="6eb98-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6eb98-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eb98-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6eb98-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eb98-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6eb98-130">INPUTS</span></span>

### <span data-ttu-id="6eb98-131">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6eb98-131">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="6eb98-132">System.String</span><span class="sxs-lookup"><span data-stu-id="6eb98-132">System.String</span></span>

## <span data-ttu-id="6eb98-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6eb98-133">OUTPUTS</span></span>

### <span data-ttu-id="6eb98-134">Microsoft.Azure.Commands.Network.Models.PSTopology</span><span class="sxs-lookup"><span data-stu-id="6eb98-134">Microsoft.Azure.Commands.Network.Models.PSTopology</span></span>

## <span data-ttu-id="6eb98-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6eb98-135">NOTES</span></span>
<span data-ttu-id="6eb98-136">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, topologia, widok</span><span class="sxs-lookup"><span data-stu-id="6eb98-136">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, topology, view</span></span> 

## <span data-ttu-id="6eb98-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6eb98-137">RELATED LINKS</span></span>

[<span data-ttu-id="6eb98-138">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6eb98-138">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="6eb98-139">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6eb98-139">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="6eb98-140">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6eb98-140">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="6eb98-141">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="6eb98-141">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="6eb98-142">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="6eb98-142">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="6eb98-143">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="6eb98-143">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="6eb98-144">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="6eb98-144">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="6eb98-145">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6eb98-145">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6eb98-146">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="6eb98-146">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="6eb98-147">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6eb98-147">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6eb98-148">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6eb98-148">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6eb98-149">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6eb98-149">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6eb98-150">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="6eb98-150">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="6eb98-151">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="6eb98-151">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="6eb98-152">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="6eb98-152">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="6eb98-153">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6eb98-153">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6eb98-154">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6eb98-154">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6eb98-155">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6eb98-155">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6eb98-156">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="6eb98-156">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="6eb98-157">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6eb98-157">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6eb98-158">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6eb98-158">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6eb98-159">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="6eb98-159">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="6eb98-160">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="6eb98-160">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="6eb98-161">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="6eb98-161">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="6eb98-162">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="6eb98-162">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="6eb98-163">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="6eb98-163">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="6eb98-164">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6eb98-164">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

