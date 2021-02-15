---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatchernetworkconfigurationdiagnosticprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
ms.openlocfilehash: c559001c68126c42c3d4ae6eaead2beda3ded5f0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193626"
---
# <span data-ttu-id="49b45-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span><span class="sxs-lookup"><span data-stu-id="49b45-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="49b45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49b45-102">SYNOPSIS</span></span>
<span data-ttu-id="49b45-103">Tworzy nowy obiekt profilu konfiguracji sieci.</span><span class="sxs-lookup"><span data-stu-id="49b45-103">Creates a new network configuration diagnostic profile object.</span></span> <span data-ttu-id="49b45-104">Ten obiekt służy do ograniczania konfiguracji sieci podczas sesji diagnostycznej przy użyciu określonych kryteriów.</span><span class="sxs-lookup"><span data-stu-id="49b45-104">This object is used to restrict the network configuration during a diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="49b45-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="49b45-105">SYNTAX</span></span>

```
New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile -Direction <String> -Protocol <String>
 -Source <String> -Destination <String> -DestinationPort <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="49b45-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="49b45-106">DESCRIPTION</span></span>
<span data-ttu-id="49b45-107">Polecenie New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile cmdlet tworzy nowy obiekt profilu diagnostycznego.</span><span class="sxs-lookup"><span data-stu-id="49b45-107">The New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile cmdlet creates a new diagnostic profile object.</span></span> <span data-ttu-id="49b45-108">Ten obiekt służy do ograniczania konfiguracji sieci podczas sesji diagnostycznej konfiguracji sieci przy użyciu określonych kryteriów.</span><span class="sxs-lookup"><span data-stu-id="49b45-108">This object is used to restrict the network configuration during a network configuration diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="49b45-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="49b45-109">EXAMPLES</span></span>

### <span data-ttu-id="49b45-110">Przykład 1. Wywoływanie sesji diagnostycznej konfiguracji sieciowej dla maszyny wirtualnej i określonego profilu sieciowego</span><span class="sxs-lookup"><span data-stu-id="49b45-110">Example 1: Invoke network configuration diagnostic session for VM and specified network profile</span></span>
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

## <span data-ttu-id="49b45-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49b45-111">PARAMETERS</span></span>

### <span data-ttu-id="49b45-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49b45-112">-DefaultProfile</span></span>
<span data-ttu-id="49b45-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="49b45-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49b45-114">— miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="49b45-114">-Destination</span></span>
<span data-ttu-id="49b45-115">Miejsce docelowe ruchu.</span><span class="sxs-lookup"><span data-stu-id="49b45-115">Traffic destination.</span></span>
<span data-ttu-id="49b45-116">Akceptowane wartości to: "\*", adres IP/CIDR, tag usługi.</span><span class="sxs-lookup"><span data-stu-id="49b45-116">Accepted values are: '\*', IP Address/CIDR, Service Tag.</span></span>

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

### <span data-ttu-id="49b45-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="49b45-117">-DestinationPort</span></span>
<span data-ttu-id="49b45-118">Port docelowy ruchu.</span><span class="sxs-lookup"><span data-stu-id="49b45-118">Traffic destination port.</span></span>
<span data-ttu-id="49b45-119">Akceptowane wartości to "\*", port (na przykład 3389) i zakres portów (na przykład 80-100).</span><span class="sxs-lookup"><span data-stu-id="49b45-119">Accepted values are '\*', port (for example, 3389) and port range (for example, 80-100).</span></span>

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

### <span data-ttu-id="49b45-120">— Kierunek</span><span class="sxs-lookup"><span data-stu-id="49b45-120">-Direction</span></span>
<span data-ttu-id="49b45-121">Kierunek ruchu.</span><span class="sxs-lookup"><span data-stu-id="49b45-121">The direction of the traffic.</span></span>
<span data-ttu-id="49b45-122">Akceptowane wartości to "Przychodzący" i "Wychodzący"</span><span class="sxs-lookup"><span data-stu-id="49b45-122">Accepted values are 'Inbound' and 'Outbound'</span></span>

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

### <span data-ttu-id="49b45-123">— Protokół</span><span class="sxs-lookup"><span data-stu-id="49b45-123">-Protocol</span></span>
<span data-ttu-id="49b45-124">Protokół do weryfikacji.</span><span class="sxs-lookup"><span data-stu-id="49b45-124">Protocol to be verified on.</span></span>
<span data-ttu-id="49b45-125">Akceptowane wartości to "\*", TCP, UDP.</span><span class="sxs-lookup"><span data-stu-id="49b45-125">Accepted values are '\*', TCP, UDP.</span></span>

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

### <span data-ttu-id="49b45-126">— Źródło</span><span class="sxs-lookup"><span data-stu-id="49b45-126">-Source</span></span>
<span data-ttu-id="49b45-127">Źródło ruchu.</span><span class="sxs-lookup"><span data-stu-id="49b45-127">Traffic source.</span></span>
<span data-ttu-id="49b45-128">Akceptowane wartości to "\*", adres IP/CIDR, tag usługi.</span><span class="sxs-lookup"><span data-stu-id="49b45-128">Accepted values are '\*', IP Address/CIDR, Service Tag.</span></span>

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

### <span data-ttu-id="49b45-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49b45-129">CommonParameters</span></span>
<span data-ttu-id="49b45-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49b45-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49b45-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49b45-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49b45-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49b45-132">INPUTS</span></span>

### <span data-ttu-id="49b45-133">System.String</span><span class="sxs-lookup"><span data-stu-id="49b45-133">System.String</span></span>

## <span data-ttu-id="49b45-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="49b45-134">OUTPUTS</span></span>

### <span data-ttu-id="49b45-135">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile</span><span class="sxs-lookup"><span data-stu-id="49b45-135">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="49b45-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="49b45-136">NOTES</span></span>
<span data-ttu-id="49b45-137">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking, watcher, diagnostic, profile</span><span class="sxs-lookup"><span data-stu-id="49b45-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, diagnostic, profile</span></span>

## <span data-ttu-id="49b45-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="49b45-138">RELATED LINKS</span></span>

[<span data-ttu-id="49b45-139">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="49b45-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="49b45-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="49b45-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="49b45-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="49b45-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="49b45-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="49b45-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="49b45-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="49b45-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="49b45-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="49b45-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="49b45-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="49b45-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="49b45-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="49b45-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="49b45-147">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="49b45-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="49b45-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="49b45-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="49b45-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="49b45-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="49b45-150">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="49b45-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="49b45-151">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="49b45-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="49b45-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="49b45-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="49b45-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="49b45-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="49b45-154">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="49b45-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="49b45-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="49b45-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="49b45-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="49b45-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="49b45-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="49b45-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="49b45-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="49b45-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="49b45-159">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="49b45-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="49b45-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="49b45-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="49b45-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="49b45-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="49b45-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="49b45-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="49b45-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="49b45-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="49b45-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="49b45-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="49b45-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="49b45-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
