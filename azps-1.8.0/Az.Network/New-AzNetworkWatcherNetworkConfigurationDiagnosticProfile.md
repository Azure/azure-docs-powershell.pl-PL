---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatchernetworkconfigurationdiagnosticprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
ms.openlocfilehash: b05f62559670bdbdb0c018dff8febd8c5c8dfb20
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709266"
---
# <span data-ttu-id="2fb93-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span><span class="sxs-lookup"><span data-stu-id="2fb93-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="2fb93-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2fb93-102">SYNOPSIS</span></span>
<span data-ttu-id="2fb93-103">Tworzy nowy obiekt profilu diagnostycznego konfiguracji sieci.</span><span class="sxs-lookup"><span data-stu-id="2fb93-103">Creates a new network configuration diagnostic profile object.</span></span> <span data-ttu-id="2fb93-104">Ten obiekt służy do ograniczania confiuration sieci podczas sesji diagnostycznej przy użyciu określonych kryteriów.</span><span class="sxs-lookup"><span data-stu-id="2fb93-104">This object is used to restrict the network confiuration during a diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="2fb93-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2fb93-105">SYNTAX</span></span>

```
New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile -Direction <String> -Protocol <String>
 -Source <String> -Destination <String> -DestinationPort <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2fb93-106">Opis</span><span class="sxs-lookup"><span data-stu-id="2fb93-106">DESCRIPTION</span></span>
<span data-ttu-id="2fb93-107">Polecenie cmdlet New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile tworzy nowy obiekt profilu diagnostycznego.</span><span class="sxs-lookup"><span data-stu-id="2fb93-107">The New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile cmdlet creates a new diagnostic profile object.</span></span> <span data-ttu-id="2fb93-108">Ten obiekt służy do ograniczania confiuration sieci podczas sesji diagnostycznej konfiguracji sieci przy użyciu określonych kryteriów.</span><span class="sxs-lookup"><span data-stu-id="2fb93-108">This object is used to restrict the network confiuration during a network configuration diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="2fb93-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2fb93-109">EXAMPLES</span></span>

### <span data-ttu-id="2fb93-110">Przykład 1: wywołanie sesji diagnostycznej konfiguracji sieci dla maszyny wirtualnej i określonego profilu sieciowego</span><span class="sxs-lookup"><span data-stu-id="2fb93-110">Example 1: Invoke network configuration diagnostic session for VM and specified network profile</span></span>
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

## <span data-ttu-id="2fb93-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2fb93-111">PARAMETERS</span></span>

### <span data-ttu-id="2fb93-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fb93-112">-DefaultProfile</span></span>
<span data-ttu-id="2fb93-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2fb93-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fb93-114">-Miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="2fb93-114">-Destination</span></span>
<span data-ttu-id="2fb93-115">Miejsce docelowe ruchu.</span><span class="sxs-lookup"><span data-stu-id="2fb93-115">Traffic destination.</span></span>
<span data-ttu-id="2fb93-116">Akceptowane wartości to: ' \* ', adres IP/CIDR, tag usługi.</span><span class="sxs-lookup"><span data-stu-id="2fb93-116">Accepted values are: '\*', IP Address/CIDR, Service Tag.</span></span>

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

### <span data-ttu-id="2fb93-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="2fb93-117">-DestinationPort</span></span>
<span data-ttu-id="2fb93-118">Port docelowy ruchu.</span><span class="sxs-lookup"><span data-stu-id="2fb93-118">Traffic destination port.</span></span>
<span data-ttu-id="2fb93-119">Akceptowane wartości to "\*", port (na przykład 3389) i zakres portów (na przykład 80-100).</span><span class="sxs-lookup"><span data-stu-id="2fb93-119">Accepted values are '\*', port (for example, 3389) and port range (for example, 80-100).</span></span>

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

### <span data-ttu-id="2fb93-120">-Direction</span><span class="sxs-lookup"><span data-stu-id="2fb93-120">-Direction</span></span>
<span data-ttu-id="2fb93-121">Kierunek ruchu.</span><span class="sxs-lookup"><span data-stu-id="2fb93-121">The direction of the traffic.</span></span>
<span data-ttu-id="2fb93-122">Akceptowane wartości to "przychodzące" i "wychodzące"</span><span class="sxs-lookup"><span data-stu-id="2fb93-122">Accepted values are 'Inbound' and 'Outbound'</span></span>

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

### <span data-ttu-id="2fb93-123">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="2fb93-123">-Protocol</span></span>
<span data-ttu-id="2fb93-124">Sprawdzanie poprawności protokołu.</span><span class="sxs-lookup"><span data-stu-id="2fb93-124">Protocol to be verified on.</span></span>
<span data-ttu-id="2fb93-125">Akceptowane wartości to ' \* ', TCP, UDP.</span><span class="sxs-lookup"><span data-stu-id="2fb93-125">Accepted values are '\*', TCP, UDP.</span></span>

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

### <span data-ttu-id="2fb93-126">-Source</span><span class="sxs-lookup"><span data-stu-id="2fb93-126">-Source</span></span>
<span data-ttu-id="2fb93-127">Źródło ruchu.</span><span class="sxs-lookup"><span data-stu-id="2fb93-127">Traffic source.</span></span>
<span data-ttu-id="2fb93-128">Akceptowane wartości to "\*", adres IP/CIDR, numer seryjny usługi.</span><span class="sxs-lookup"><span data-stu-id="2fb93-128">Accepted values are '\*', IP Address/CIDR, Service Tag.</span></span>

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

### <span data-ttu-id="2fb93-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fb93-129">CommonParameters</span></span>
<span data-ttu-id="2fb93-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fb93-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fb93-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fb93-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fb93-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2fb93-132">INPUTS</span></span>

### <span data-ttu-id="2fb93-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2fb93-133">System.String</span></span>

## <span data-ttu-id="2fb93-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2fb93-134">OUTPUTS</span></span>

### <span data-ttu-id="2fb93-135">Microsoft. Azure. Commands. Network. models. PSNetworkConfigurationDiagnosticProfile</span><span class="sxs-lookup"><span data-stu-id="2fb93-135">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="2fb93-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2fb93-136">NOTES</span></span>
<span data-ttu-id="2fb93-137">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, monitor, Diagnostyka, profil</span><span class="sxs-lookup"><span data-stu-id="2fb93-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, diagnostic, profile</span></span>

## <span data-ttu-id="2fb93-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2fb93-138">RELATED LINKS</span></span>

[<span data-ttu-id="2fb93-139">Nowe — AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2fb93-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="2fb93-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2fb93-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="2fb93-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2fb93-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="2fb93-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="2fb93-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="2fb93-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="2fb93-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="2fb93-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="2fb93-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="2fb93-145">Start — AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="2fb93-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="2fb93-146">Nowe — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2fb93-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2fb93-147">Nowe — AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="2fb93-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="2fb93-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2fb93-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2fb93-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2fb93-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2fb93-150">Zatrzymaj — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2fb93-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2fb93-151">Nowe — AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="2fb93-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="2fb93-152">Test — AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2fb93-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="2fb93-153">Test — AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="2fb93-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="2fb93-154">Zatrzymaj — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2fb93-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2fb93-155">Start — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2fb93-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2fb93-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2fb93-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2fb93-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="2fb93-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="2fb93-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2fb93-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2fb93-159">Nowe — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2fb93-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2fb93-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="2fb93-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="2fb93-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="2fb93-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="2fb93-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="2fb93-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="2fb93-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="2fb93-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="2fb93-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="2fb93-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="2fb93-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2fb93-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)