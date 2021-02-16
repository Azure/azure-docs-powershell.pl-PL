---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatchernetworkconfigurationdiagnosticprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
ms.openlocfilehash: fe3438e43bc623da0ba69b3b1224a47df8b15f1f
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100414683"
---
# <span data-ttu-id="14eee-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span><span class="sxs-lookup"><span data-stu-id="14eee-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="14eee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14eee-102">SYNOPSIS</span></span>
<span data-ttu-id="14eee-103">Tworzy nowy obiekt profilu konfiguracji sieci.</span><span class="sxs-lookup"><span data-stu-id="14eee-103">Creates a new network configuration diagnostic profile object.</span></span> <span data-ttu-id="14eee-104">Ten obiekt służy do ograniczania konfiguracji sieci podczas sesji diagnostycznej przy użyciu określonych kryteriów.</span><span class="sxs-lookup"><span data-stu-id="14eee-104">This object is used to restrict the network configuration during a diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="14eee-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="14eee-105">SYNTAX</span></span>

```
New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile -Direction <String> -Protocol <String>
 -Source <String> -Destination <String> -DestinationPort <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="14eee-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="14eee-106">DESCRIPTION</span></span>
<span data-ttu-id="14eee-107">Polecenie New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile cmdlet tworzy nowy obiekt profilu diagnostycznego.</span><span class="sxs-lookup"><span data-stu-id="14eee-107">The New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile cmdlet creates a new diagnostic profile object.</span></span> <span data-ttu-id="14eee-108">Ten obiekt służy do ograniczania konfiguracji sieci podczas sesji diagnostycznej konfiguracji sieci przy użyciu określonych kryteriów.</span><span class="sxs-lookup"><span data-stu-id="14eee-108">This object is used to restrict the network configuration during a network configuration diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="14eee-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="14eee-109">EXAMPLES</span></span>

### <span data-ttu-id="14eee-110">Przykład 1. Wywoływanie sesji diagnostycznej konfiguracji sieciowej dla maszyny wirtualnej i określonego profilu sieciowego</span><span class="sxs-lookup"><span data-stu-id="14eee-110">Example 1: Invoke network configuration diagnostic session for VM and specified network profile</span></span>
```
PS C:\> $profile = New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile -Direction Inbound -Protocol Tcp -Source 10.1.1.4 -Destination * -DestinationPort 50
PS C:\> Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -Location eastus -TargetResourceId /subscriptions/61cc8a98-a8be-4bfe-a04e-0b461f93fe35/resourceGroups/NwRgEastUS/providers/Microsoft.Compute/virtualMachines/vm1 -Profile $profile

Results : [
            {
              "Profile": {
                "Direction": "Inbound",
                "Protocol": "Tcp",
                "Source": "10.1.1.4",
                "Destination": "*",
                "DestinationPort": "50"
              },
              "NetworkSecurityGroupResult": {
                "SecurityRuleAccessResult": "Allow",
                "EvaluatedNetworkSecurityGroups": [
                  {
                    "NetworkSecurityGroupId": "/subscriptions/61cc8a98-a8be-4bfe-a04e-0b461f93fe35/resourceGroups/clean
          upservice/providers/Microsoft.Network/networkSecurityGroups/rg-cleanupservice-nsg1",
                    "MatchedRule": {
                      "RuleName": "UserRule_Cleanuptool-Allow-4001",
                      "Action": "Allow"
                    },
                    "RulesEvaluationResult": [
                      {
                        "Name": "UserRule_Cleanuptool-Allow-100",
                        "ProtocolMatched": true,
                        "SourceMatched": false,
                        "SourcePortMatched": true,
                        "DestinationMatched": true,
                        "DestinationPortMatched": false
                      },
```

## <span data-ttu-id="14eee-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14eee-111">PARAMETERS</span></span>

### <span data-ttu-id="14eee-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14eee-112">-DefaultProfile</span></span>
<span data-ttu-id="14eee-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="14eee-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14eee-114">— miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="14eee-114">-Destination</span></span>
<span data-ttu-id="14eee-115">Miejsce docelowe ruchu.</span><span class="sxs-lookup"><span data-stu-id="14eee-115">Traffic destination.</span></span>
<span data-ttu-id="14eee-116">Akceptowane wartości to: "\*", adres IP/CIDR, tag usługi.</span><span class="sxs-lookup"><span data-stu-id="14eee-116">Accepted values are: '\*', IP Address/CIDR, Service Tag.</span></span>

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

### <span data-ttu-id="14eee-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="14eee-117">-DestinationPort</span></span>
<span data-ttu-id="14eee-118">Port docelowy ruchu.</span><span class="sxs-lookup"><span data-stu-id="14eee-118">Traffic destination port.</span></span>
<span data-ttu-id="14eee-119">Akceptowane wartości to "\*", port (na przykład 3389) i zakres portów (na przykład 80-100).</span><span class="sxs-lookup"><span data-stu-id="14eee-119">Accepted values are '\*', port (for example, 3389) and port range (for example, 80-100).</span></span>

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

### <span data-ttu-id="14eee-120">— Kierunek</span><span class="sxs-lookup"><span data-stu-id="14eee-120">-Direction</span></span>
<span data-ttu-id="14eee-121">Kierunek ruchu.</span><span class="sxs-lookup"><span data-stu-id="14eee-121">The direction of the traffic.</span></span>
<span data-ttu-id="14eee-122">Akceptowane wartości to "Przychodzący" i "Wychodzący"</span><span class="sxs-lookup"><span data-stu-id="14eee-122">Accepted values are 'Inbound' and 'Outbound'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14eee-123">— Protokół</span><span class="sxs-lookup"><span data-stu-id="14eee-123">-Protocol</span></span>
<span data-ttu-id="14eee-124">Protokół do weryfikacji.</span><span class="sxs-lookup"><span data-stu-id="14eee-124">Protocol to be verified on.</span></span>
<span data-ttu-id="14eee-125">Akceptowane wartości to "\*", TCP, UDP.</span><span class="sxs-lookup"><span data-stu-id="14eee-125">Accepted values are '\*', TCP, UDP.</span></span>

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

### <span data-ttu-id="14eee-126">— Źródło</span><span class="sxs-lookup"><span data-stu-id="14eee-126">-Source</span></span>
<span data-ttu-id="14eee-127">Źródło ruchu.</span><span class="sxs-lookup"><span data-stu-id="14eee-127">Traffic source.</span></span>
<span data-ttu-id="14eee-128">Zaakceptowane wartości to "\*", adres IP/CIDR, tag usługi.</span><span class="sxs-lookup"><span data-stu-id="14eee-128">Accepted values are '\*', IP Address/CIDR, Service Tag.</span></span>

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

### <span data-ttu-id="14eee-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14eee-129">CommonParameters</span></span>
<span data-ttu-id="14eee-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14eee-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14eee-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14eee-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14eee-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14eee-132">INPUTS</span></span>

### <span data-ttu-id="14eee-133">System.String</span><span class="sxs-lookup"><span data-stu-id="14eee-133">System.String</span></span>

## <span data-ttu-id="14eee-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14eee-134">OUTPUTS</span></span>

### <span data-ttu-id="14eee-135">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile</span><span class="sxs-lookup"><span data-stu-id="14eee-135">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="14eee-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="14eee-136">NOTES</span></span>
<span data-ttu-id="14eee-137">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking, watcher, diagnostic, profile</span><span class="sxs-lookup"><span data-stu-id="14eee-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, diagnostic, profile</span></span>

## <span data-ttu-id="14eee-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="14eee-138">RELATED LINKS</span></span>

[<span data-ttu-id="14eee-139">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="14eee-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="14eee-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="14eee-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="14eee-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="14eee-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="14eee-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="14eee-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="14eee-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="14eee-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="14eee-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="14eee-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="14eee-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="14eee-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="14eee-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="14eee-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="14eee-147">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="14eee-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="14eee-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="14eee-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="14eee-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="14eee-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="14eee-150">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="14eee-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="14eee-151">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="14eee-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="14eee-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="14eee-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="14eee-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="14eee-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="14eee-154">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="14eee-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="14eee-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="14eee-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="14eee-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="14eee-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="14eee-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="14eee-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="14eee-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="14eee-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="14eee-159">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="14eee-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="14eee-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="14eee-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="14eee-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="14eee-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="14eee-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="14eee-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="14eee-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="14eee-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="14eee-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="14eee-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="14eee-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="14eee-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
