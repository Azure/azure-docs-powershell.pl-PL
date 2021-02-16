---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatchernetworkconfigurationdiagnosticprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
ms.openlocfilehash: e879de96f861c5a102077c3d392944f79a293b10
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100406812"
---
# <span data-ttu-id="64027-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span><span class="sxs-lookup"><span data-stu-id="64027-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="64027-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64027-102">SYNOPSIS</span></span>
<span data-ttu-id="64027-103">Tworzy nowy obiekt profilu konfiguracji sieci.</span><span class="sxs-lookup"><span data-stu-id="64027-103">Creates a new network configuration diagnostic profile object.</span></span> <span data-ttu-id="64027-104">Ten obiekt służy do ograniczania konfiguracji sieci podczas sesji diagnostycznej przy użyciu określonych kryteriów.</span><span class="sxs-lookup"><span data-stu-id="64027-104">This object is used to restrict the network configuration during a diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="64027-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="64027-105">SYNTAX</span></span>

```
New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile -Direction <String> -Protocol <String>
 -Source <String> -Destination <String> -DestinationPort <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="64027-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="64027-106">DESCRIPTION</span></span>
<span data-ttu-id="64027-107">Polecenie New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile cmdlet tworzy nowy obiekt profilu diagnostycznego.</span><span class="sxs-lookup"><span data-stu-id="64027-107">The New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile cmdlet creates a new diagnostic profile object.</span></span> <span data-ttu-id="64027-108">Ten obiekt służy do ograniczania konfiguracji sieci podczas sesji diagnostycznej konfiguracji sieci przy użyciu określonych kryteriów.</span><span class="sxs-lookup"><span data-stu-id="64027-108">This object is used to restrict the network configuration during a network configuration diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="64027-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="64027-109">EXAMPLES</span></span>

### <span data-ttu-id="64027-110">Przykład 1. Wywoływanie sesji diagnostycznej konfiguracji sieciowej dla maszyny wirtualnej i określonego profilu sieciowego</span><span class="sxs-lookup"><span data-stu-id="64027-110">Example 1: Invoke network configuration diagnostic session for VM and specified network profile</span></span>
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

## <span data-ttu-id="64027-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64027-111">PARAMETERS</span></span>

### <span data-ttu-id="64027-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64027-112">-DefaultProfile</span></span>
<span data-ttu-id="64027-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="64027-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64027-114">— miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="64027-114">-Destination</span></span>
<span data-ttu-id="64027-115">Miejsce docelowe ruchu.</span><span class="sxs-lookup"><span data-stu-id="64027-115">Traffic destination.</span></span>
<span data-ttu-id="64027-116">Akceptowane wartości to: "\*", adres IP/CIDR, tag usługi.</span><span class="sxs-lookup"><span data-stu-id="64027-116">Accepted values are: '\*', IP Address/CIDR, Service Tag.</span></span>

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

### <span data-ttu-id="64027-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="64027-117">-DestinationPort</span></span>
<span data-ttu-id="64027-118">Port docelowy ruchu.</span><span class="sxs-lookup"><span data-stu-id="64027-118">Traffic destination port.</span></span>
<span data-ttu-id="64027-119">Akceptowane wartości to "\*", port (na przykład 3389) i zakres portów (na przykład 80-100).</span><span class="sxs-lookup"><span data-stu-id="64027-119">Accepted values are '\*', port (for example, 3389) and port range (for example, 80-100).</span></span>

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

### <span data-ttu-id="64027-120">— Kierunek</span><span class="sxs-lookup"><span data-stu-id="64027-120">-Direction</span></span>
<span data-ttu-id="64027-121">Kierunek ruchu.</span><span class="sxs-lookup"><span data-stu-id="64027-121">The direction of the traffic.</span></span>
<span data-ttu-id="64027-122">Akceptowane wartości to "Przychodzący" i "Wychodzący"</span><span class="sxs-lookup"><span data-stu-id="64027-122">Accepted values are 'Inbound' and 'Outbound'</span></span>

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

### <span data-ttu-id="64027-123">— Protokół</span><span class="sxs-lookup"><span data-stu-id="64027-123">-Protocol</span></span>
<span data-ttu-id="64027-124">Protokół do weryfikacji.</span><span class="sxs-lookup"><span data-stu-id="64027-124">Protocol to be verified on.</span></span>
<span data-ttu-id="64027-125">Akceptowane wartości to "\*", TCP, UDP.</span><span class="sxs-lookup"><span data-stu-id="64027-125">Accepted values are '\*', TCP, UDP.</span></span>

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

### <span data-ttu-id="64027-126">— Źródło</span><span class="sxs-lookup"><span data-stu-id="64027-126">-Source</span></span>
<span data-ttu-id="64027-127">Źródło ruchu.</span><span class="sxs-lookup"><span data-stu-id="64027-127">Traffic source.</span></span>
<span data-ttu-id="64027-128">Akceptowane wartości to "\*", adres IP/CIDR, tag usługi.</span><span class="sxs-lookup"><span data-stu-id="64027-128">Accepted values are '\*', IP Address/CIDR, Service Tag.</span></span>

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

### <span data-ttu-id="64027-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64027-129">CommonParameters</span></span>
<span data-ttu-id="64027-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64027-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64027-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64027-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64027-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64027-132">INPUTS</span></span>

### <span data-ttu-id="64027-133">System.String</span><span class="sxs-lookup"><span data-stu-id="64027-133">System.String</span></span>

## <span data-ttu-id="64027-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="64027-134">OUTPUTS</span></span>

### <span data-ttu-id="64027-135">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile</span><span class="sxs-lookup"><span data-stu-id="64027-135">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="64027-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="64027-136">NOTES</span></span>
<span data-ttu-id="64027-137">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking, watcher, diagnostic, profile</span><span class="sxs-lookup"><span data-stu-id="64027-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, diagnostic, profile</span></span>

## <span data-ttu-id="64027-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="64027-138">RELATED LINKS</span></span>

[<span data-ttu-id="64027-139">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="64027-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="64027-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="64027-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="64027-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="64027-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="64027-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="64027-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="64027-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="64027-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="64027-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="64027-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="64027-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="64027-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="64027-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="64027-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="64027-147">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="64027-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="64027-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="64027-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="64027-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="64027-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="64027-150">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="64027-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="64027-151">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="64027-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="64027-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="64027-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="64027-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="64027-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="64027-154">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="64027-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="64027-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="64027-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="64027-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="64027-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="64027-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="64027-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="64027-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="64027-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="64027-159">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="64027-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="64027-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="64027-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="64027-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="64027-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="64027-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="64027-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="64027-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="64027-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="64027-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="64027-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="64027-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="64027-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
