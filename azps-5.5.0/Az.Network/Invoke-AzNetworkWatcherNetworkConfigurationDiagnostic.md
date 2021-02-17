---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/invoke-aznetworkwatchernetworkconfigurationdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic.md
ms.openlocfilehash: f9aa604cead73807d0a49a5e19be3193c21dce78
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100409056"
---
# <span data-ttu-id="64c2b-101">Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="64c2b-101">Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic</span></span>

## <span data-ttu-id="64c2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64c2b-102">SYNOPSIS</span></span>
<span data-ttu-id="64c2b-103">Wywoływanie sesji diagnostycznej konfiguracji sieci dla określonych profilów sieciowych w zasobie docelowym.</span><span class="sxs-lookup"><span data-stu-id="64c2b-103">Invoke network configuration diagnostic session for specified network profiles on target resource.</span></span>

## <span data-ttu-id="64c2b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="64c2b-104">SYNTAX</span></span>

### <span data-ttu-id="64c2b-105">SetByResource (Default)</span><span class="sxs-lookup"><span data-stu-id="64c2b-105">SetByResource (Default)</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -NetworkWatcher <PSNetworkWatcher>
 -TargetResourceId <String> [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64c2b-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="64c2b-106">SetByName</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64c2b-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="64c2b-107">SetByLocation</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -Location <String> -TargetResourceId <String>
 [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64c2b-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="64c2b-108">SetByResourceId</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -ResourceId <String> -TargetResourceId <String>
 [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64c2b-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="64c2b-109">DESCRIPTION</span></span>
<span data-ttu-id="64c2b-110">Polecenie cmdlet Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic sesji diagnostycznej konfiguracji sieci dla określonych profilów sieciowych w zasobie docelowym.</span><span class="sxs-lookup"><span data-stu-id="64c2b-110">The Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic cmdlet invoke network configuration diagnostic session for specified network profiles on target resource.</span></span>

## <span data-ttu-id="64c2b-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="64c2b-111">EXAMPLES</span></span>

### <span data-ttu-id="64c2b-112">Przykład 1. Wywoływanie sesji diagnostycznej konfiguracji sieciowej dla maszyny wirtualnej i określonego profilu sieciowego</span><span class="sxs-lookup"><span data-stu-id="64c2b-112">Example 1: Invoke network configuration diagnostic session for VM and specified network profile</span></span>
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

## <span data-ttu-id="64c2b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64c2b-113">PARAMETERS</span></span>

### <span data-ttu-id="64c2b-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="64c2b-114">-AsJob</span></span>
<span data-ttu-id="64c2b-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="64c2b-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64c2b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64c2b-116">-DefaultProfile</span></span>
<span data-ttu-id="64c2b-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="64c2b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64c2b-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="64c2b-118">-Location</span></span>
<span data-ttu-id="64c2b-119">Lokalizacja czujki sieci.</span><span class="sxs-lookup"><span data-stu-id="64c2b-119">Location of the network watcher.</span></span>

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

### <span data-ttu-id="64c2b-120">— NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="64c2b-120">-NetworkWatcher</span></span>
<span data-ttu-id="64c2b-121">Zasób obserwowania sieci.</span><span class="sxs-lookup"><span data-stu-id="64c2b-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="64c2b-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="64c2b-122">-NetworkWatcherName</span></span>
<span data-ttu-id="64c2b-123">Nazwa osoby oglądacej sieć.</span><span class="sxs-lookup"><span data-stu-id="64c2b-123">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64c2b-124">— Profil</span><span class="sxs-lookup"><span data-stu-id="64c2b-124">-Profile</span></span>
<span data-ttu-id="64c2b-125">Lista profilów diagnostycznych konfiguracji sieci.</span><span class="sxs-lookup"><span data-stu-id="64c2b-125">List of network configuration diagnostic profiles.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64c2b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64c2b-126">-ResourceGroupName</span></span>
<span data-ttu-id="64c2b-127">Nazwa grupy zasobów obserwowanych sieci.</span><span class="sxs-lookup"><span data-stu-id="64c2b-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="64c2b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="64c2b-128">-ResourceId</span></span>
<span data-ttu-id="64c2b-129">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="64c2b-129">Resource ID.</span></span>

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

### <span data-ttu-id="64c2b-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="64c2b-130">-TargetResourceId</span></span>
<span data-ttu-id="64c2b-131">Identyfikator zasobu docelowego do wykonania diagnostyki konfiguracji sieci.</span><span class="sxs-lookup"><span data-stu-id="64c2b-131">The ID of the target resource to perform network configuration diagnostic.</span></span>
<span data-ttu-id="64c2b-132">Prawidłowe opcje to: MASZYNY WIRTUALNE,Interface sieci, MASZYNY WIRTUALNE/Interface sieci i Brama aplikacji.</span><span class="sxs-lookup"><span data-stu-id="64c2b-132">Valid options are VM, NetworkInterface, VMSS/NetworkInterface and Application Gateway.</span></span>

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

### <span data-ttu-id="64c2b-133">-VerbosityLevel</span><span class="sxs-lookup"><span data-stu-id="64c2b-133">-VerbosityLevel</span></span>
<span data-ttu-id="64c2b-134">Poziom szczegółowości.</span><span class="sxs-lookup"><span data-stu-id="64c2b-134">Verbosity level.</span></span>
<span data-ttu-id="64c2b-135">Akceptowane wartości to "Normalny", "Minimum", "Pełny".</span><span class="sxs-lookup"><span data-stu-id="64c2b-135">Accepted values are 'Normal', 'Minimum', 'Full'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64c2b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64c2b-136">CommonParameters</span></span>
<span data-ttu-id="64c2b-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64c2b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64c2b-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64c2b-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64c2b-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64c2b-139">INPUTS</span></span>

### <span data-ttu-id="64c2b-140">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="64c2b-140">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="64c2b-141">System.String</span><span class="sxs-lookup"><span data-stu-id="64c2b-141">System.String</span></span>

## <span data-ttu-id="64c2b-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64c2b-142">OUTPUTS</span></span>

### <span data-ttu-id="64c2b-143">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticResponse</span><span class="sxs-lookup"><span data-stu-id="64c2b-143">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticResponse</span></span>

## <span data-ttu-id="64c2b-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="64c2b-144">NOTES</span></span>
<span data-ttu-id="64c2b-145">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking, watcher, diagnostic, profile</span><span class="sxs-lookup"><span data-stu-id="64c2b-145">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, diagnostic, profile</span></span>

## <span data-ttu-id="64c2b-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="64c2b-146">RELATED LINKS</span></span>

[<span data-ttu-id="64c2b-147">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="64c2b-147">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="64c2b-148">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="64c2b-148">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="64c2b-149">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="64c2b-149">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="64c2b-150">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="64c2b-150">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="64c2b-151">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="64c2b-151">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="64c2b-152">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="64c2b-152">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="64c2b-153">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="64c2b-153">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="64c2b-154">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="64c2b-154">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="64c2b-155">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="64c2b-155">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="64c2b-156">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="64c2b-156">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="64c2b-157">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="64c2b-157">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="64c2b-158">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="64c2b-158">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="64c2b-159">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="64c2b-159">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="64c2b-160">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="64c2b-160">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="64c2b-161">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="64c2b-161">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="64c2b-162">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="64c2b-162">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="64c2b-163">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="64c2b-163">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="64c2b-164">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="64c2b-164">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="64c2b-165">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="64c2b-165">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="64c2b-166">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="64c2b-166">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="64c2b-167">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="64c2b-167">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="64c2b-168">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="64c2b-168">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="64c2b-169">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="64c2b-169">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="64c2b-170">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="64c2b-170">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="64c2b-171">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="64c2b-171">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="64c2b-172">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="64c2b-172">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="64c2b-173">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="64c2b-173">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
