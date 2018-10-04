---
title: Dziennik zmian w programie Azure PowerShell | Microsoft Docs
description: Jest to historia zmian wprowadzonych w programie Azure PowerShell w jego najnowszej wersji.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 08/28/2018
ms.openlocfilehash: 3cb71087a61a0fcd06c014394e8f9e5654d4c1a8
ms.sourcegitcommit: 6c38e86e16da99f65cd183c63e34f7176b121ab8
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/04/2018
ms.locfileid: "47425027"
---
# <a name="release-notes"></a><span data-ttu-id="c4bbc-103">Informacje o wersji</span><span class="sxs-lookup"><span data-stu-id="c4bbc-103">Release notes</span></span>

<span data-ttu-id="c4bbc-104">To jest lista zmian wprowadzonych w programie Azure PowerShell w tym wydaniu.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="690---september-2018"></a><span data-ttu-id="c4bbc-105">6.9.0 — wrzesień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-105">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="c4bbc-106">Ogólne</span><span class="sxs-lookup"><span data-stu-id="c4bbc-106">General</span></span>
* <span data-ttu-id="c4bbc-107">Element AzureRM.SignalR został dodany do modułu zbiorczego AzureRM</span><span class="sxs-lookup"><span data-stu-id="c4bbc-107">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="c4bbc-108">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c4bbc-108">AzureRM.Profile</span></span>
* <span data-ttu-id="c4bbc-109">Drobne zmiany wspólnego kodu magazynu</span><span class="sxs-lookup"><span data-stu-id="c4bbc-109">Minor changes to the storage common code</span></span>
* <span data-ttu-id="c4bbc-110">Zaktualizowano pliki pomocy w celu uwzględnienia pełnych typów parametrów.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-110">Updated help files to include full parameter types.</span></span>
- <span data-ttu-id="c4bbc-111">Zmieniono opcję -ServicePrincipal na nieobowiązkową w zestawie parametrów ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c4bbc-111">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="c4bbc-112">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="c4bbc-112">Azure.Storage</span></span>
* <span data-ttu-id="c4bbc-113">Obsługa tworzenia kontekstu magazynu przy użyciu protokołu OAuth.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-113">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="c4bbc-114">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="c4bbc-114">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="c4bbc-115">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="c4bbc-115">AzureRM.Cdn</span></span>
* <span data-ttu-id="c4bbc-116">Dodano element Standard_Microsoft w jednostce SKU cen usługi CDN.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-116">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="c4bbc-117">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c4bbc-117">AzureRM.Compute</span></span>
* <span data-ttu-id="c4bbc-118">Przeniesiono zależności magazynu kluczy i magazynu do zależności wspólnych</span><span class="sxs-lookup"><span data-stu-id="c4bbc-118">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="c4bbc-119">Dodano obsługę kolejnych rozmiarów maszyn wirtualnych do poleceń cmdlet funkcji AEM</span><span class="sxs-lookup"><span data-stu-id="c4bbc-119">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="c4bbc-120">Dodano parametr PublicIPPrefix do polecenia New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="c4bbc-120">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="c4bbc-121">Dodano parametr ResourceId do polecenia cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="c4bbc-121">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="c4bbc-122">Dodano polecenie cmdlet Invoke-AzureRmVmssVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="c4bbc-122">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="c4bbc-123">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="c4bbc-123">AzureRM.Dns</span></span>
* <span data-ttu-id="c4bbc-124">Dodano obsługę rekordu aliasu podczas tworzenia rekordów DNS</span><span class="sxs-lookup"><span data-stu-id="c4bbc-124">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="c4bbc-125">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="c4bbc-125">AzureRM.Insights</span></span>
* <span data-ttu-id="c4bbc-126">Rozwiązano problemy nr 6833 i 7102 (obszar ustawień diagnostycznych)</span><span class="sxs-lookup"><span data-stu-id="c4bbc-126">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="c4bbc-127">Problemy z nazwą domyślną, np. „usługa”, podczas tworzenia i tworzenia/pobierania listy ustawień diagnostycznych</span><span class="sxs-lookup"><span data-stu-id="c4bbc-127">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="c4bbc-128">Problemy z tworzeniem ustawień diagnostycznych przy użyciu kategorii</span><span class="sxs-lookup"><span data-stu-id="c4bbc-128">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="c4bbc-129">Dodano komunikat o zakończeniu obsługi parametrów ziarn czasu metryk</span><span class="sxs-lookup"><span data-stu-id="c4bbc-129">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="c4bbc-130">Parametry typu Timegrain są nadal akceptowane (jest to zmiana niepowodująca niezgodności), ale są one ignorowane w zapleczu, ponieważ tylko wersja PT1M jest prawidłowa</span><span class="sxs-lookup"><span data-stu-id="c4bbc-130">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c4bbc-131">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c4bbc-131">AzureRM.Network</span></span>
* <span data-ttu-id="c4bbc-132">Zmiany poleceń cmdlet usługi LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c4bbc-132">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="c4bbc-133">LoadBalancerInboundNatPoolConfig: dodano parametry IdleTimeoutInMinutes, EnableFloatingIp i EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="c4bbc-133">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="c4bbc-134">LoadBalancerInboundNatRuleConfig: dodano parametr EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="c4bbc-134">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="c4bbc-135">LoadBalancerRuleConfig: dodano parametr EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="c4bbc-135">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="c4bbc-136">LoadBalancerProbeConfig: dodano obsługę wartości „Https” dla parametru Protocol</span><span class="sxs-lookup"><span data-stu-id="c4bbc-136">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="c4bbc-137">Dodano nowe polecenia dla nowego zasobu podrzędnego OutboundRule usługi LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c4bbc-137">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="c4bbc-138">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c4bbc-138">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="c4bbc-139">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c4bbc-139">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="c4bbc-140">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c4bbc-140">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="c4bbc-141">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c4bbc-141">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="c4bbc-142">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c4bbc-142">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="c4bbc-143">Dodano nową właściwość HostedWorkloads dla interfejsu PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c4bbc-143">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="c4bbc-144">Dodano nowe polecenia cmdlet dla funkcji Azure Firewall za pośrednictwem usługi ARM</span><span class="sxs-lookup"><span data-stu-id="c4bbc-144">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="c4bbc-145">Dodano polecenie Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="c4bbc-145">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="c4bbc-146">Dodano polecenie Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="c4bbc-146">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="c4bbc-147">Dodano polecenie New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="c4bbc-147">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="c4bbc-148">Dodano polecenie Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="c4bbc-148">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="c4bbc-149">Dodano polecenie New-AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c4bbc-149">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="c4bbc-150">Dodano polecenie New-AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="c4bbc-150">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="c4bbc-151">Dodano polecenie New-AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c4bbc-151">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="c4bbc-152">Dodano polecenie New-AzureRmFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="c4bbc-152">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="c4bbc-153">Dodano polecenie New-AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c4bbc-153">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="c4bbc-154">Dodano polecenie New-AzureRmFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c4bbc-154">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="c4bbc-155">Dodano obsługę zaufanego certyfikatu głównego i konfiguracji skalowania automatycznego w usłudze Application Gateway</span><span class="sxs-lookup"><span data-stu-id="c4bbc-155">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="c4bbc-156">Dodano nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="c4bbc-156">New Cmdlets added:</span></span>
      - <span data-ttu-id="c4bbc-157">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c4bbc-157">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="c4bbc-158">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c4bbc-158">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="c4bbc-159">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c4bbc-159">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="c4bbc-160">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c4bbc-160">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="c4bbc-161">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c4bbc-161">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="c4bbc-162">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4bbc-162">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="c4bbc-163">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4bbc-163">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="c4bbc-164">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4bbc-164">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="c4bbc-165">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4bbc-165">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="c4bbc-166">Zaktualizowano polecenia cmdlet przy użyciu opcjonalnego parametru -TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c4bbc-166">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="c4bbc-167">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c4bbc-167">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="c4bbc-168">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c4bbc-168">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="c4bbc-169">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="c4bbc-169">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="c4bbc-170">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="c4bbc-170">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="c4bbc-171">Zaktualizowano polecenia cmdlet przy użyciu opcjonalnego parametru -AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4bbc-171">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="c4bbc-172">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c4bbc-172">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="c4bbc-173">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c4bbc-173">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="c4bbc-174">Dodano polecenie cmdlet dla punktu końcowego interfejsu Get-AzureInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="c4bbc-174">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="c4bbc-175">Dodano obsługę wielu prefiksów adresów w podsieci.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-175">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="c4bbc-176">Zaktualizowano następujące polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="c4bbc-176">Updated cmdlets:</span></span>
  - <span data-ttu-id="c4bbc-177">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c4bbc-177">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="c4bbc-178">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c4bbc-178">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="c4bbc-179">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c4bbc-179">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="c4bbc-180">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c4bbc-180">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="c4bbc-181">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c4bbc-181">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="c4bbc-182">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="c4bbc-182">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="c4bbc-183">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="c4bbc-183">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="c4bbc-184">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="c4bbc-184">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="c4bbc-185">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4bbc-185">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="c4bbc-186">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4bbc-186">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="c4bbc-187">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4bbc-187">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="c4bbc-188">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="c4bbc-188">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="c4bbc-189">New-AzureRmNetworkInterfaceIpConfig — Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="c4bbc-189">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="c4bbc-190">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="c4bbc-190">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="c4bbc-191">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="c4bbc-191">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="c4bbc-192">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c4bbc-192">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="c4bbc-193">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c4bbc-193">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="c4bbc-194">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c4bbc-194">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="c4bbc-195">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c4bbc-195">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="c4bbc-196">Dodano polecenia cmdlet na potrzeby delegowania podsieci.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-196">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="c4bbc-197">New-AzureRmDelegation: tworzy nowe delegowanie, które można dodać do podsieci</span><span class="sxs-lookup"><span data-stu-id="c4bbc-197">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="c4bbc-198">Remove-AzureRmDelegation: pobiera podsieć i usuwa z niej podaną nazwę delegowania</span><span class="sxs-lookup"><span data-stu-id="c4bbc-198">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="c4bbc-199">Add-AzureRmDelegation: pobiera podsieć i dodaje do niej podaną nazwę usługi jako delegowanie</span><span class="sxs-lookup"><span data-stu-id="c4bbc-199">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="c4bbc-200">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="c4bbc-200">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="c4bbc-201">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="c4bbc-201">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="c4bbc-202">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="c4bbc-202">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="c4bbc-203">Obsługa dysków zarządzanych</span><span class="sxs-lookup"><span data-stu-id="c4bbc-203">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="c4bbc-204">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="c4bbc-204">AzureRM.RedisCache</span></span>
* <span data-ttu-id="c4bbc-205">Zaktualizowano zależność szczegółowych informacji.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-205">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c4bbc-206">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c4bbc-206">AzureRM.Resources</span></span>
* <span data-ttu-id="c4bbc-207">Zaktualizowano polecenie New-AzureRmResourceGroupDeployment przy użyciu nowego parametru RollbackAction</span><span class="sxs-lookup"><span data-stu-id="c4bbc-207">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="c4bbc-208">Dodano obsługę elementu OnErrorDeployment przy użyciu nowego parametru.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-208">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="c4bbc-209">Obsługa tożsamości zarządzanej w przypisaniach zasad.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-209">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="c4bbc-210">Parametry z wartościami domyślnymi nie są już wymagane podczas przypisywania zasad za pomocą polecenia „New-AzureRmPolicyAssignment”</span><span class="sxs-lookup"><span data-stu-id="c4bbc-210">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="c4bbc-211">Dodano nowe polecenie cmdlet Get-AzureRmPolicyAlias służące do pobierania aliasów zasad</span><span class="sxs-lookup"><span data-stu-id="c4bbc-211">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="c4bbc-212">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c4bbc-212">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c4bbc-213">Rozwiązano problem nr 7161</span><span class="sxs-lookup"><span data-stu-id="c4bbc-213">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="c4bbc-214">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="c4bbc-214">AzureRM.SignalR</span></span>
* <span data-ttu-id="c4bbc-215">Zaktualizowano nazwy jednostek SKU Bezpłatna_F1 i Standardowa_S1</span><span class="sxs-lookup"><span data-stu-id="c4bbc-215">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="c4bbc-216">Dodano pole wersji do obiektu PSSignalRResource i parametry połączenia do obiektu PSSignalRKeys.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-216">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="c4bbc-217">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="c4bbc-217">AzureRM.Storage</span></span>
* <span data-ttu-id="c4bbc-218">Obsługa zasad niezmienności w elemencie AzureRm.Storage</span><span class="sxs-lookup"><span data-stu-id="c4bbc-218">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="c4bbc-219">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c4bbc-219">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="c4bbc-220">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c4bbc-220">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="c4bbc-221">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c4bbc-221">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="c4bbc-222">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c4bbc-222">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="c4bbc-223">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c4bbc-223">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="c4bbc-224">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="c4bbc-224">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="c4bbc-225">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="c4bbc-225">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="c4bbc-226">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="c4bbc-226">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="c4bbc-227">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="c4bbc-227">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="c4bbc-228">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="c4bbc-228">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="c4bbc-229">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="c4bbc-229">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="c4bbc-230">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="c4bbc-230">AzureRM.Websites</span></span>
* <span data-ttu-id="c4bbc-231">Dodano dwa nowe polecenia cmdlet: Get-AzureRmDeletedWebApp i Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="c4bbc-231">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="c4bbc-232">New-AzureRmAppServicePlan — dodano przełącznik funkcji Hyper-V na potrzeby tworzenia planu usługi App Service przy użyciu kontenera systemu Windows</span><span class="sxs-lookup"><span data-stu-id="c4bbc-232">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="c4bbc-233">New-AzureRmWebApp/New-AzureRmWebAppSlot/Set-AzureRmWebApp/Set-AzureRmWebAppSlot — dodano nowe parametry (ciąg –ContainerRegistryUser -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) na potrzeby tworzenia aplikacji kontenera systemu Windows oraz zarządzania nią</span><span class="sxs-lookup"><span data-stu-id="c4bbc-233">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="c4bbc-234">6.8.1 — sierpień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-234">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="c4bbc-235">Ogólne</span><span class="sxs-lookup"><span data-stu-id="c4bbc-235">General</span></span>
* <span data-ttu-id="c4bbc-236">Rozwiązano problem z nieustawionymi domyślnymi grupami zasobów.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-236">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="c4bbc-237">Zaktualizowano wspólne zestawy środowiska uruchomieniowego</span><span class="sxs-lookup"><span data-stu-id="c4bbc-237">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="c4bbc-238">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c4bbc-238">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="c4bbc-239">Rozwiązano problem z nieustawionymi domyślnymi grupami zasobów.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-239">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="c4bbc-240">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="c4bbc-240">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="c4bbc-241">Polecenia cmdlet Import-AzureRmApiManagementApi i \*-AzureRmApiManagementCertificate teraz obsługują ścieżki względne</span><span class="sxs-lookup"><span data-stu-id="c4bbc-241">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="c4bbc-242">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="c4bbc-242">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="c4bbc-243">CertificateInformation to możliwa do ustawienia właściwość pozwalająca poleceniu cmdlet Set-AzureRmApiManagement poprawnie działać.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-243">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="c4bbc-244">Rozwiązano przez aktualizację do pakietu nuget 4.0.4-preview</span><span class="sxs-lookup"><span data-stu-id="c4bbc-244">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="c4bbc-245">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="c4bbc-245">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="c4bbc-246">W filtrze Odata naprawiono wyszukiwanie według nazwy dla produktu</span><span class="sxs-lookup"><span data-stu-id="c4bbc-246">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="c4bbc-247">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="c4bbc-247">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="c4bbc-248">W filtrze Odata naprawiono wyszukiwanie według nazwy dla interfejsu API</span><span class="sxs-lookup"><span data-stu-id="c4bbc-248">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="c4bbc-249">Dodano obsługę rejestratora AzureMonitor</span><span class="sxs-lookup"><span data-stu-id="c4bbc-249">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="c4bbc-250">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c4bbc-250">AzureRM.Compute</span></span>
* <span data-ttu-id="c4bbc-251">Naprawiono problem polegający na braku elementu docelowego w danych wyjściowych błędu.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-251">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="c4bbc-252">Rozwiązano problem z typem konta magazynu dla maszyny wirtualnej z dyskiem zarządzanym</span><span class="sxs-lookup"><span data-stu-id="c4bbc-252">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="c4bbc-253">Rozwiązano problem z nieustawionymi domyślnymi grupami zasobów.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-253">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="c4bbc-254">Naprawiono polecenia cmdlet rozszerzenia AEM dla innych środowisk, na przykład Azure — Chiny</span><span class="sxs-lookup"><span data-stu-id="c4bbc-254">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c4bbc-255">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c4bbc-255">AzureRM.Network</span></span>
* <span data-ttu-id="c4bbc-256">Zmieniono domyślną prezentację danych wyjściowych polecenia cmdlet na widok tabeli</span><span class="sxs-lookup"><span data-stu-id="c4bbc-256">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="c4bbc-257">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="c4bbc-257">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="c4bbc-258">Naprawiono błąd w poleceniu Update-AzureRmPowerBIEmbeddedCapacity występujący podczas próby skalowania wstrzymanej pojemności</span><span class="sxs-lookup"><span data-stu-id="c4bbc-258">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="c4bbc-259">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c4bbc-259">AzureRM.Resources</span></span>
* <span data-ttu-id="c4bbc-260">Rozwiązano problem z tworzeniem aplikacji zarządzanych z witryny MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-260">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="c4bbc-261">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c4bbc-261">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c4bbc-262">Rozwiązane problemy</span><span class="sxs-lookup"><span data-stu-id="c4bbc-262">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="c4bbc-263">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="c4bbc-263">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="c4bbc-264">Dodano obsługę metody routingu MultiValue</span><span class="sxs-lookup"><span data-stu-id="c4bbc-264">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="c4bbc-265">Nowy parametr „MaxReturn” dla routingu MultiValue</span><span class="sxs-lookup"><span data-stu-id="c4bbc-265">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="c4bbc-266">Dodano obsługę metody routingu Subnet</span><span class="sxs-lookup"><span data-stu-id="c4bbc-266">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="c4bbc-267">Obsługa zakresów adresów IP (podsieci) w punktach końcowych</span><span class="sxs-lookup"><span data-stu-id="c4bbc-267">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="c4bbc-268">Dodano obsługę nagłówków niestandardowych w profilach</span><span class="sxs-lookup"><span data-stu-id="c4bbc-268">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="c4bbc-269">Dodano obsługę zakresów kodów oczekiwanego stanu w profilach</span><span class="sxs-lookup"><span data-stu-id="c4bbc-269">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="c4bbc-270">Dodano obsługę nagłówków niestandardowych w punktach końcowych</span><span class="sxs-lookup"><span data-stu-id="c4bbc-270">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="c4bbc-271">6.8.0 — sierpień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-271">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="c4bbc-272">Ogólne</span><span class="sxs-lookup"><span data-stu-id="c4bbc-272">General</span></span>
* <span data-ttu-id="c4bbc-273">Rozwiązano problem z nieustawionymi domyślnymi grupami zasobów.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-273">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="c4bbc-274">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c4bbc-274">AzureRM.Profile</span></span>
* <span data-ttu-id="c4bbc-275">Dodano właściwość wygasania do tokenów zwracanych podczas operacji Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="c4bbc-275">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c4bbc-276">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c4bbc-276">AzureRM.Compute</span></span>
* <span data-ttu-id="c4bbc-277">Naprawiono problem polegający na braku elementu docelowego w danych wyjściowych błędu.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-277">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="c4bbc-278">Rozwiązano problem z typem konta magazynu dla maszyny wirtualnej z dyskiem zarządzanym</span><span class="sxs-lookup"><span data-stu-id="c4bbc-278">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="c4bbc-279">Naprawiono polecenia cmdlet rozszerzenia AEM dla innych środowisk, na przykład Azure — Chiny</span><span class="sxs-lookup"><span data-stu-id="c4bbc-279">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="c4bbc-280">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="c4bbc-280">AzureRM.IotHub</span></span>
* <span data-ttu-id="c4bbc-281">Naprawiono przykłady dla poleceń New-AzureRmIotHubExportDevices i New-AzureRmIotHubImportDevices</span><span class="sxs-lookup"><span data-stu-id="c4bbc-281">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c4bbc-282">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c4bbc-282">AzureRM.Network</span></span>
* <span data-ttu-id="c4bbc-283">Zmieniono domyślną reprezentację modeli na widok tabeli</span><span class="sxs-lookup"><span data-stu-id="c4bbc-283">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="c4bbc-284">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="c4bbc-284">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="c4bbc-285">Naprawiono błąd w poleceniu Update-AzureRmPowerBIEmbeddedCapacity występujący podczas próby skalowania wstrzymanej pojemności</span><span class="sxs-lookup"><span data-stu-id="c4bbc-285">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c4bbc-286">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c4bbc-286">AzureRM.Resources</span></span>
* <span data-ttu-id="c4bbc-287">Rozwiązano problem z tworzeniem aplikacji zarządzanej z witryny MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-287">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="c4bbc-288">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c4bbc-288">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c4bbc-289">Rozwiązano problemy</span><span class="sxs-lookup"><span data-stu-id="c4bbc-289">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="c4bbc-290">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="c4bbc-290">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="c4bbc-291">Obsługa metody routingu MultiValue</span><span class="sxs-lookup"><span data-stu-id="c4bbc-291">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="c4bbc-292">Nowy parametr „MaxReturn” dla routingu MultiValue</span><span class="sxs-lookup"><span data-stu-id="c4bbc-292">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="c4bbc-293">Obsługa metody routingu Subnet</span><span class="sxs-lookup"><span data-stu-id="c4bbc-293">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="c4bbc-294">Obsługa zakresów adresów IP (podsieci) w punktach końcowych</span><span class="sxs-lookup"><span data-stu-id="c4bbc-294">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="c4bbc-295">Obsługa nagłówków niestandardowych w profilach</span><span class="sxs-lookup"><span data-stu-id="c4bbc-295">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="c4bbc-296">Obsługa zakresów kodów oczekiwanego stanu w profilach</span><span class="sxs-lookup"><span data-stu-id="c4bbc-296">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="c4bbc-297">Obsługa nagłówków niestandardowych w punktach końcowych</span><span class="sxs-lookup"><span data-stu-id="c4bbc-297">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="c4bbc-298">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="c4bbc-298">AzureRM.Websites</span></span>
* <span data-ttu-id="c4bbc-299">Rozwiązano problem z niepoprawnie ustawionymi domyślnymi grupami zasobów.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-299">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="c4bbc-300">6.7.0 — sierpień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-300">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="c4bbc-301">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c4bbc-301">AzureRM.Profile</span></span>
* <span data-ttu-id="c4bbc-302">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-302">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="c4bbc-303">Dodaj identyfikator użytkownika do domyślnej nazwy kontekstu, aby uniknąć konfliktów kontekstów</span><span class="sxs-lookup"><span data-stu-id="c4bbc-303">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="c4bbc-304">Rozwiązanie problemu z poleceniem Clear-AzureRmContext, który powodował problemy w przypadku wybrania kontekstu nr 6398</span><span class="sxs-lookup"><span data-stu-id="c4bbc-304">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="c4bbc-305">Umożliwienie przekazywania domeny dzierżawy do parametru „-TenantId” polecenia „Connect-AzureRmAccount”</span><span class="sxs-lookup"><span data-stu-id="c4bbc-305">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="c4bbc-306">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="c4bbc-306">Azure.Storage</span></span>
* <span data-ttu-id="c4bbc-307">Usunięcie ograniczenia limitu przydziału udziału plików platformy Azure do 5 TB</span><span class="sxs-lookup"><span data-stu-id="c4bbc-307">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="c4bbc-308">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="c4bbc-308">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="c4bbc-309">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c4bbc-309">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="c4bbc-310">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-310">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="c4bbc-311">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c4bbc-311">Azure.AnalysisServices</span></span>
* <span data-ttu-id="c4bbc-312">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-312">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="c4bbc-313">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c4bbc-313">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="c4bbc-314">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-314">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="c4bbc-315">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="c4bbc-315">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="c4bbc-316">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-316">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="c4bbc-317">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="c4bbc-317">AzureRM.Automation</span></span>
* <span data-ttu-id="c4bbc-318">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-318">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="c4bbc-319">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="c4bbc-319">AzureRM.Backup</span></span>
* <span data-ttu-id="c4bbc-320">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-320">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="c4bbc-321">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="c4bbc-321">AzureRM.Batch</span></span>
* <span data-ttu-id="c4bbc-322">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-322">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="c4bbc-323">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="c4bbc-323">AzureRM.Billing</span></span>
* <span data-ttu-id="c4bbc-324">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-324">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="c4bbc-325">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="c4bbc-325">AzureRM.Cdn</span></span>
* <span data-ttu-id="c4bbc-326">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-326">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="c4bbc-327">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c4bbc-327">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="c4bbc-328">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-328">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c4bbc-329">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c4bbc-329">AzureRM.Compute</span></span>
* <span data-ttu-id="c4bbc-330">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-330">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="c4bbc-331">Dodanie parametru EvictionPolicy do polecenia New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="c4bbc-331">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="c4bbc-332">Użycie domyślnej lokalizacji w parametrze DiskFileParameterSet polecenia New-AzureRmVm, jeśli nie określono lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-332">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="c4bbc-333">Naprawienie opisu parametru w poleceniu Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="c4bbc-333">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="c4bbc-334">Naprawienie działania polecenia cmdlet Get-AzureRmVMDiskEncryptionStatus w przypadku niektórych scenariuszy powiązanych z pojedynczym przebiegiem</span><span class="sxs-lookup"><span data-stu-id="c4bbc-334">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="c4bbc-335">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="c4bbc-335">AzureRM.Consumption</span></span>
* <span data-ttu-id="c4bbc-336">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-336">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="c4bbc-337">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="c4bbc-337">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="c4bbc-338">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-338">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="c4bbc-339">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c4bbc-339">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="c4bbc-340">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-340">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="c4bbc-341">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="c4bbc-341">AzureRM.DataFactories</span></span>
* <span data-ttu-id="c4bbc-342">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-342">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="c4bbc-343">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="c4bbc-343">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="c4bbc-344">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-344">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="c4bbc-345">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="c4bbc-345">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="c4bbc-346">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-346">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="c4bbc-347">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c4bbc-347">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="c4bbc-348">Naprawienie debugowania, gdy parametr DebugPreference jest ustawiany w wierszu polecenia programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="c4bbc-348">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="c4bbc-349">Aktualizacja przykładu polecenia Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="c4bbc-349">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="c4bbc-350">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-350">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="c4bbc-351">Aktualizacja przykładu polecenia Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c4bbc-351">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="c4bbc-352">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="c4bbc-352">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="c4bbc-353">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-353">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="c4bbc-354">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="c4bbc-354">AzureRM.Dns</span></span>
* <span data-ttu-id="c4bbc-355">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-355">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="c4bbc-356">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="c4bbc-356">AzureRM.EventGrid</span></span>
* <span data-ttu-id="c4bbc-357">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-357">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="c4bbc-358">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="c4bbc-358">AzureRM.EventHub</span></span>
* <span data-ttu-id="c4bbc-359">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-359">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="c4bbc-360">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="c4bbc-360">AzureRM.HDInsight</span></span>
* <span data-ttu-id="c4bbc-361">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-361">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="c4bbc-362">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="c4bbc-362">AzureRM.Insights</span></span>
* <span data-ttu-id="c4bbc-363">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-363">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="c4bbc-364">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="c4bbc-364">AzureRM.IotHub</span></span>
* <span data-ttu-id="c4bbc-365">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-365">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="c4bbc-366">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c4bbc-366">AzureRM.KeyVault</span></span>
* <span data-ttu-id="c4bbc-367">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-367">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="c4bbc-368">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="c4bbc-368">AzureRM.LogicApp</span></span>
* <span data-ttu-id="c4bbc-369">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-369">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="c4bbc-370">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="c4bbc-370">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="c4bbc-371">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-371">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="c4bbc-372">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="c4bbc-372">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="c4bbc-373">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-373">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="c4bbc-374">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="c4bbc-374">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="c4bbc-375">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-375">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="c4bbc-376">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="c4bbc-376">AzureRM.Media</span></span>
* <span data-ttu-id="c4bbc-377">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-377">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c4bbc-378">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c4bbc-378">AzureRM.Network</span></span>
* <span data-ttu-id="c4bbc-379">Dodano przykład dla polecenia Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c4bbc-379">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="c4bbc-380">Dodano przykłady i opisy dla poleceń Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey oraz New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c4bbc-380">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="c4bbc-381">Dodano przykłady dla poleceń Remove-AzureRmVirtualNetworkGatewayIpConfig i Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c4bbc-381">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="c4bbc-382">Dodano przykład dla polecenia Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="c4bbc-382">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="c4bbc-383">Dodano przykład dla polecenia Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="c4bbc-383">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="c4bbc-384">Dodano przykład dla polecenia Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c4bbc-384">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="c4bbc-385">Ponownie wygenerowano polecenia cmdlet ApplicationSecurityGroup, RouteTable i Usage z użyciem najnowszej wersji generatora</span><span class="sxs-lookup"><span data-stu-id="c4bbc-385">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="c4bbc-386">Poprawiono czytelność komunikatu o błędzie dla polecenia Get-AzureRmVirtualNetworkSubnetConfig podczas próby pobrania podsieci, która nie istnieje</span><span class="sxs-lookup"><span data-stu-id="c4bbc-386">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="c4bbc-387">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="c4bbc-387">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="c4bbc-388">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-388">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="c4bbc-389">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c4bbc-389">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="c4bbc-390">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-390">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="c4bbc-391">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="c4bbc-391">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="c4bbc-392">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-392">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="c4bbc-393">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="c4bbc-393">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="c4bbc-394">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-394">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="c4bbc-395">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c4bbc-395">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="c4bbc-396">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-396">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="c4bbc-397">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="c4bbc-397">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="c4bbc-398">Dodano filtr zasad do polecenia cmdlet Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-398">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="c4bbc-399">Polecenie zwraca listę elementów kopii zapasowej chronionych przez zasady o danym identyfikatorze.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-399">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="c4bbc-400">Zaktualizowano przestrzeń nazw Microsoft.Azure.Management.RecoveryServices.Backup do wersji 3.0.0-preview.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-400">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="c4bbc-401">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-401">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="c4bbc-402">Dodano parametr TargetResourceGroupName do polecenia Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-402">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="c4bbc-403">Grupa zasobów, do której są przywracane dyski zarządzane.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-403">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="c4bbc-404">Ma zastosowanie do wykonywania kopii zapasowych maszyn wirtualnych z dyskami zarządzanymi.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-404">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="c4bbc-405">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="c4bbc-405">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="c4bbc-406">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-406">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="c4bbc-407">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="c4bbc-407">AzureRM.RedisCache</span></span>
* <span data-ttu-id="c4bbc-408">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-408">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="c4bbc-409">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="c4bbc-409">AzureRM.Relay</span></span>
* <span data-ttu-id="c4bbc-410">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-410">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c4bbc-411">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c4bbc-411">AzureRM.Resources</span></span>
* <span data-ttu-id="c4bbc-412">Obsługa wdrażania szablonów w zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-412">Support template deployment at subscription scope.</span></span> <span data-ttu-id="c4bbc-413">Dodanie nowych poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="c4bbc-413">Add new Cmdlets:</span></span>
    - <span data-ttu-id="c4bbc-414">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="c4bbc-414">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="c4bbc-415">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="c4bbc-415">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="c4bbc-416">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="c4bbc-416">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="c4bbc-417">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="c4bbc-417">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="c4bbc-418">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="c4bbc-418">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="c4bbc-419">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="c4bbc-419">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="c4bbc-420">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="c4bbc-420">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="c4bbc-421">Rozwiązanie problemu, w przypadku którego podczas przekazywania kontekstu do polecenia Set-AzureRmResource jest zgłaszany błąd</span><span class="sxs-lookup"><span data-stu-id="c4bbc-421">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="c4bbc-422">Naprawienie przykładu polecenia New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c4bbc-422">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="c4bbc-423">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-423">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="c4bbc-424">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="c4bbc-424">AzureRM.Scheduler</span></span>
* <span data-ttu-id="c4bbc-425">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-425">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="c4bbc-426">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c4bbc-426">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c4bbc-427">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-427">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="c4bbc-428">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c4bbc-428">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="c4bbc-429">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-429">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="c4bbc-430">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c4bbc-430">AzureRM.Sql</span></span>
* <span data-ttu-id="c4bbc-431">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-431">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="c4bbc-432">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="c4bbc-432">AzureRM.Storage</span></span>
* <span data-ttu-id="c4bbc-433">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-433">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="c4bbc-434">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="c4bbc-434">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="c4bbc-435">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-435">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="c4bbc-436">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="c4bbc-436">AzureRM.Tags</span></span>
* <span data-ttu-id="c4bbc-437">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-437">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="c4bbc-438">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="c4bbc-438">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="c4bbc-439">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-439">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="c4bbc-440">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="c4bbc-440">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="c4bbc-441">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-441">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="c4bbc-442">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="c4bbc-442">AzureRM.Websites</span></span>
* <span data-ttu-id="c4bbc-443">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-443">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="c4bbc-444">6.6.0 — lipiec 2018 r.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-444">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="c4bbc-445">Ogólne</span><span class="sxs-lookup"><span data-stu-id="c4bbc-445">General</span></span>
* <span data-ttu-id="c4bbc-446">Zaktualizowano wszystkie pliki pomocy, aby uwzględniały pełne typy parametrów i poprawne typy wejściowe/wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-446">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="c4bbc-447">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c4bbc-447">AzureRM.Profile</span></span>
* <span data-ttu-id="c4bbc-448">Zaktualizowano bibliotekę Common.Strategy, aby mogła ona weryfikować, czy bieżąca konfiguracja zasobu jest zgodna z zasobem docelowym.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-448">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="c4bbc-449">Dodano typy ps1xml do biblioteki Common.Storage</span><span class="sxs-lookup"><span data-stu-id="c4bbc-449">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="c4bbc-450">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="c4bbc-450">Azure.Storage</span></span>
* <span data-ttu-id="c4bbc-451">Dodano obsługę pobierania kontekstu magazynu z profilu DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4bbc-451">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="c4bbc-452">Dodano atrybut Ps1XmlAttribute do właściwości typów wyjściowych poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-452">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="c4bbc-453">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c4bbc-453">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="c4bbc-454">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="c4bbc-454">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="c4bbc-455">Usunięto usterkę w maperze Automapper dotyczącą translacji obiektu PsApiManagementApi na obiekt ApiContract</span><span class="sxs-lookup"><span data-stu-id="c4bbc-455">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="c4bbc-456">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="c4bbc-456">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="c4bbc-457">Usunięto usterkę w elemencie File.Save dotyczącą przeciążania typem kodowania</span><span class="sxs-lookup"><span data-stu-id="c4bbc-457">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="c4bbc-458">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="c4bbc-458">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="c4bbc-459">Uaktualniono menedżer NuGet do wersji 4.0.3, co rozwiązuje problem z występowaniem wyjątku dotyczącego wzorca w parametrze apiId</span><span class="sxs-lookup"><span data-stu-id="c4bbc-459">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c4bbc-460">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c4bbc-460">AzureRM.Compute</span></span>
* <span data-ttu-id="c4bbc-461">Rozwiązanie problemu powodującego zakończenie niepowodzeniem tworzenia maszyny wirtualnej przy użyciu zestawu DiskFileParameterSet w poleceniu New-AzureRmVm z powodu zmiany nazwy typu konta magazynu PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-461">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="c4bbc-462">Poprawienie polecenia cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="c4bbc-462">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="c4bbc-463">Zaktualizowanie polecenia Get-AzureRmAvailabilitySet, aby umożliwić zwrócenie listy wszystkich zestawów dostępności w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-463">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="c4bbc-464">(Parametr ResouceGroupName jest teraz opcjonalny).</span><span class="sxs-lookup"><span data-stu-id="c4bbc-464">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="c4bbc-465">Zaktualizowanie zestawu SimpleParameterSet polecenia „New-AzureRmVm”, aby umożliwić korzystanie z przyspieszonej łączności sieciowej na kwalifikujących się maszynach wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-465">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="c4bbc-466">Zaktualizowanie prostego zestawu parametrów polecenia New-AzureRmVmss w taki sposób, aby tworzenie zestawu skalowania maszyn wirtualnych kończyło się niepowodzeniem, gdy moduł równoważenia obciążenia określony przez użytkownika już istnieje.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-466">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="c4bbc-467">Zaktualizowanie przykładu dla polecenia New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="c4bbc-467">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="c4bbc-468">Dodanie przykładu dla polecenia „New-AzureRmVM”</span><span class="sxs-lookup"><span data-stu-id="c4bbc-468">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="c4bbc-469">Zaktualizowanie opisu polecenia Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="c4bbc-469">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="c4bbc-470">Zaktualizowanie przykładu 1 dla polecenia Set-AzureRmVMBginfoExtension przez poprawienie pisowni i prefiksu.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-470">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="c4bbc-471">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="c4bbc-471">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="c4bbc-472">Zaktualizowano zestaw ADF .Net SDK do wersji 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-472">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="c4bbc-473">Obsługa udostępniania własnego środowiska Integration Runtime dla wielu fabryk danych.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-473">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="c4bbc-474">Dodanie nowego parametru -SharedIntegrationRuntimeResourceId do polecenia cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-474">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="c4bbc-475">Dodanie nowego opcjonalnego parametru -LinkedDataFactoryName do polecenia cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-475">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="c4bbc-476">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c4bbc-476">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="c4bbc-477">Zaktualizowano zestaw SDK płaszczyzny danych (Microsoft.Azure.DataLake.Store) do wersji 1.1.9</span><span class="sxs-lookup"><span data-stu-id="c4bbc-477">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="c4bbc-478">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="c4bbc-478">AzureRM.EventHub</span></span>
* <span data-ttu-id="c4bbc-479">Zaktualizowano potokowanie elementów InputObject i ResourceId w poleceniach cmdlet usuwania</span><span class="sxs-lookup"><span data-stu-id="c4bbc-479">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="c4bbc-480">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="c4bbc-480">AzureRM.Insights</span></span>
* <span data-ttu-id="c4bbc-481">Naprawiono formatowanie typu OutputType w plikach pomocy</span><span class="sxs-lookup"><span data-stu-id="c4bbc-481">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="c4bbc-482">Użycie zestawu Microsoft.Azure.Management.Monitor SDK w wersji 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="c4bbc-482">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="c4bbc-483">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c4bbc-483">AzureRM.KeyVault</span></span>
* <span data-ttu-id="c4bbc-484">Rozwiązanie problemu z potokowaniem w poleceniu Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c4bbc-484">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c4bbc-485">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c4bbc-485">AzureRM.Network</span></span>
* <span data-ttu-id="c4bbc-486">Dodano przykłady dla poleceń cmdlet LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-486">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c4bbc-487">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c4bbc-487">AzureRM.Resources</span></span>
* <span data-ttu-id="c4bbc-488">Rozwiązanie problemu w przypadku podawania zarówno wartości, jak i nazwy tagu w poleceniu „Get-AzureRmResource”</span><span class="sxs-lookup"><span data-stu-id="c4bbc-488">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="c4bbc-489">Naprawienie scenariusza potokowania w poleceniu „Set-AzureRmResource”</span><span class="sxs-lookup"><span data-stu-id="c4bbc-489">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="c4bbc-490">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c4bbc-490">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c4bbc-491">Zaktualizowano potokowanie elementów InputObject i ResourceId w poleceniach cmdlet usuwania</span><span class="sxs-lookup"><span data-stu-id="c4bbc-491">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="c4bbc-492">Rozwiązano kilka problemów</span><span class="sxs-lookup"><span data-stu-id="c4bbc-492">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="c4bbc-493">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c4bbc-493">AzureRM.Sql</span></span>
* <span data-ttu-id="c4bbc-494">Dodanie obsługi zaawansowanej ochrony serwera przed zagrożeniami przy użyciu następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="c4bbc-494">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="c4bbc-495">Enable-AzureRmSqlServerAdvancedThreatProtection, Disable-AzureRmSqlServerAdvancedThreatProtection, Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c4bbc-495">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="c4bbc-496">Dodanie obsługi oceny luk w zabezpieczeniach przy użyciu następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="c4bbc-496">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="c4bbc-497">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings, Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings, Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="c4bbc-497">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="c4bbc-498">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline, Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline, Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="c4bbc-498">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="c4bbc-499">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan, Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord, Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="c4bbc-499">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="c4bbc-500">Poprawiono przykład w poleceniu Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c4bbc-500">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="c4bbc-501">Naprawienie niepoprawnej obsługi daty/godziny w przypadku podstawowej kultury innej niż Stany Zjednoczone w poleceniu Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="c4bbc-501">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="c4bbc-502">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="c4bbc-502">AzureRM.Storage</span></span>
* <span data-ttu-id="c4bbc-503">Dodanie atrybutu Ps1XmlAttribute do właściwości typów wyjściowych poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="c4bbc-503">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="c4bbc-504">Pokazywanie danych wyjściowych polecenia cmdlet StorageAccount w widoku tabeli</span><span class="sxs-lookup"><span data-stu-id="c4bbc-504">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="c4bbc-505">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c4bbc-505">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="c4bbc-506">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c4bbc-506">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="c4bbc-507">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c4bbc-507">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="c4bbc-508">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="c4bbc-508">AzureRM.Tags</span></span>
* <span data-ttu-id="c4bbc-509">Usunięcie niepoprawnej informacji z pomocy polecenia cmdlet Tag</span><span class="sxs-lookup"><span data-stu-id="c4bbc-509">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="c4bbc-510">6.5.0 — lipiec 2018 r.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-510">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="c4bbc-511">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c4bbc-511">AzureRM.Profile</span></span>
* <span data-ttu-id="c4bbc-512">Zaktualizowano pomoc dotyczącą polecenia „Get-AzureRmContextAutosaveSetting”</span><span class="sxs-lookup"><span data-stu-id="c4bbc-512">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="c4bbc-513">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="c4bbc-513">Azure.Storage</span></span>
* <span data-ttu-id="c4bbc-514">Dodano obsługę przekazywania obiektu blob lub pliku z tokenem sygnatury dostępu współdzielonego tylko do odczytu</span><span class="sxs-lookup"><span data-stu-id="c4bbc-514">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="c4bbc-515">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="c4bbc-515">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="c4bbc-516">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="c4bbc-516">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="c4bbc-517">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c4bbc-517">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="c4bbc-518">Dodano wymaganą właściwość ResourceGroupName do usługi AS.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-518">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="c4bbc-519">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="c4bbc-519">AzureRM.Automation</span></span>
* <span data-ttu-id="c4bbc-520">Zaktualizowano pomoc i dodano przykład polecenia „New-AzureRMAutomationSchedule”</span><span class="sxs-lookup"><span data-stu-id="c4bbc-520">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c4bbc-521">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c4bbc-521">AzureRM.Compute</span></span>
* <span data-ttu-id="c4bbc-522">Dodano parametr -Tag do polecenia Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c4bbc-522">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="c4bbc-523">Dodano przykład polecenia „Add-AzureRmVmssExtension”</span><span class="sxs-lookup"><span data-stu-id="c4bbc-523">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="c4bbc-524">Dodano przykłady polecenia „Remove-AzureRmVmssExtension”</span><span class="sxs-lookup"><span data-stu-id="c4bbc-524">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="c4bbc-525">Zaktualizowano pomoc dotyczącą polecenia „Set-AzureRmVMAccessExtension”</span><span class="sxs-lookup"><span data-stu-id="c4bbc-525">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="c4bbc-526">Zaktualizowano atrybut SimpleParameterSet dla polecenia New-AzureRmVmss, aby domyślnie ustawiał parametr SinglePlacementGroup na wartość false oraz dodano parametr przełącznika „SinglePlacementGroup” umożliwiający użytkownikowi tworzenie zestawów VMSS w pojedynczej grupie umieszczania.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-526">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="c4bbc-527">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="c4bbc-527">AzureRM.EventHub</span></span>
* <span data-ttu-id="c4bbc-528">Dodano właściwość tylko do odczytu „PendingReplicationOperationsCount” do klasy PSEventHubDRConfigurationAttributes, która umożliwia wyświetlenie liczby oczekujących operacji replikacji w czasie działania replikacji</span><span class="sxs-lookup"><span data-stu-id="c4bbc-528">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="c4bbc-529">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c4bbc-529">AzureRM.KeyVault</span></span>
* <span data-ttu-id="c4bbc-530">Zaktualizowano komunikat o błędzie dla polecenia Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c4bbc-530">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="c4bbc-531">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="c4bbc-531">AzureRM.LogicApp</span></span>
* <span data-ttu-id="c4bbc-532">Naprawiono błąd „nie można rozpoznać zestawu parametrów” w poleceniu New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="c4bbc-532">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c4bbc-533">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c4bbc-533">AzureRM.Network</span></span>
* <span data-ttu-id="c4bbc-534">Włączono komunikację równorzędną między sieciami wirtualnymi w wielu dzierżawach dla polecenia Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="c4bbc-534">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="c4bbc-535">Zaktualizowano poniższe polecenia cmdlet usługi Application Gateway</span><span class="sxs-lookup"><span data-stu-id="c4bbc-535">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="c4bbc-536">New-AzureRmApplicationGateway: dodano obsługę flagi EnableFIPS i stref</span><span class="sxs-lookup"><span data-stu-id="c4bbc-536">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="c4bbc-537">New-AzureRmApplicationGatewaySku: dodano nowe jednostki SKU — Standard_v2 i WAF_v2</span><span class="sxs-lookup"><span data-stu-id="c4bbc-537">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="c4bbc-538">Set-AzureRmApplicationGatewaySku: dodano nowe jednostki SKU — Standard_v2 i WAF_v2</span><span class="sxs-lookup"><span data-stu-id="c4bbc-538">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="c4bbc-539">Ponownie wygenerowano polecenia cmdlet RouteTable z użyciem najnowszej wersji generatora</span><span class="sxs-lookup"><span data-stu-id="c4bbc-539">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="c4bbc-540">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="c4bbc-540">AzureRM.Relay</span></span>
* <span data-ttu-id="c4bbc-541">Zaktualizowano pliki markdown, naprawiono problem z nazwą parametru w przykładzie</span><span class="sxs-lookup"><span data-stu-id="c4bbc-541">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c4bbc-542">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c4bbc-542">AzureRM.Resources</span></span>
* <span data-ttu-id="c4bbc-543">Zaktualizowano polecenia cmdlet Roleassignment i roledefinition:</span><span class="sxs-lookup"><span data-stu-id="c4bbc-543">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="c4bbc-544">Usunięto dodatkowe wywołania polecenia roledefinition wykonywane w ramach stronicowania.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-544">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="c4bbc-545">Naprawiono polecenie cmdlet Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="c4bbc-545">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="c4bbc-546">Naprawiono funkcjonalność parametru polecenia -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="c4bbc-546">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="c4bbc-547">Rozwiązano problem z poleceniem „Get-AzureRmResource”, który polegał na tym, że w parametrze „-ResourceType” była uwzględniana wielkość liter</span><span class="sxs-lookup"><span data-stu-id="c4bbc-547">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="c4bbc-548">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c4bbc-548">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c4bbc-549">Dodano parametry top i skip do poleceń cmdlet „list”</span><span class="sxs-lookup"><span data-stu-id="c4bbc-549">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="c4bbc-550">Dodano polecenia cmdlet migracji przestrzeni nazw z warstwy Standardowa do warstwy Premium:</span><span class="sxs-lookup"><span data-stu-id="c4bbc-550">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="c4bbc-551">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="c4bbc-551">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="c4bbc-552">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="c4bbc-552">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="c4bbc-553">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="c4bbc-553">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="c4bbc-554">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="c4bbc-554">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="c4bbc-555">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="c4bbc-555">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="c4bbc-556">Dodano właściwość tylko do odczytu „PendingReplicationOperationsCount” do klasy PSServiceBusDRConfigurationAttributes, która umożliwia wyświetlenie liczby oczekujących operacji replikacji w czasie działania replikacji</span><span class="sxs-lookup"><span data-stu-id="c4bbc-556">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="c4bbc-557">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c4bbc-557">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="c4bbc-558">Zaktualizowano przykład dotyczący polecenia „New-AzureRmServiceFabricCluster”</span><span class="sxs-lookup"><span data-stu-id="c4bbc-558">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="c4bbc-559">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c4bbc-559">AzureRM.Sql</span></span>
* <span data-ttu-id="c4bbc-560">Dodano nowe polecenia cmdlet dla przestrzeni nazw Management.Sql, aby umożliwić klientom dodawanie certyfikatu TDE do wystąpienia programu SQL Server lub wystąpienia zarządzanego</span><span class="sxs-lookup"><span data-stu-id="c4bbc-560">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="c4bbc-561">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="c4bbc-561">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="c4bbc-562">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="c4bbc-562">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="c4bbc-563">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="c4bbc-563">AzureRM.Websites</span></span>
* <span data-ttu-id="c4bbc-564">Polecenia `Set-AzureRmWebApp -AssignIdentity` i `Set-AzureRmWebAppSlot -AssignIdentity` po ustawieniu na wartość false spowodują teraz usunięcie właściwości Identity z obiektu lokacji. Usuwany jest także tag podglądu.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-564">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="c4bbc-565">Zaktualizowano przykład dotyczący poleceń `Get-AzureRmWebAppMetrics` i `Get-AzureRmAppServicePlanMetrics`</span><span class="sxs-lookup"><span data-stu-id="c4bbc-565">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="c4bbc-566">Polecenie `Set-AzureRmWebApp -PhpVersion` obsługuje wartość off jako prawidłową wersję języka PHP</span><span class="sxs-lookup"><span data-stu-id="c4bbc-566">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="c4bbc-567">6.4.0 — lipiec 2018 r.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-567">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="c4bbc-568">Ogólne</span><span class="sxs-lookup"><span data-stu-id="c4bbc-568">General</span></span>
* <span data-ttu-id="c4bbc-569">Naprawiono formatowanie typu OutputType w plikach pomocy dotyczących większości modułów</span><span class="sxs-lookup"><span data-stu-id="c4bbc-569">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="c4bbc-570">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c4bbc-570">AzureRM.Profile</span></span>
* <span data-ttu-id="c4bbc-571">Dodano atrybut Ps1Xml do podstawowych typów danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="c4bbc-571">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c4bbc-572">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c4bbc-572">AzureRM.Compute</span></span>
* <span data-ttu-id="c4bbc-573">Funkcja tagów adresów IP dla zestawu skalowania maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="c4bbc-573">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="c4bbc-574">Dodano polecenie cmdlet „New-AzureRmVmssIpTagConfig”</span><span class="sxs-lookup"><span data-stu-id="c4bbc-574">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="c4bbc-575">Dodano parametr IpTag do polecenia New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="c4bbc-575">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="c4bbc-576">Funkcja automatycznego wycofywania systemu operacyjnego dla zestawu skalowania maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="c4bbc-576">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="c4bbc-577">Dodano parametry DisableAutoRollback do poleceń New-AzureRmVmssConfig i Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c4bbc-577">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="c4bbc-578">Funkcja historii uaktualniania systemu operacyjnego dla zestawu skalowania maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="c4bbc-578">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="c4bbc-579">Dodano parametr przełącznika OSUpgradeHistory do polecenia Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c4bbc-579">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="c4bbc-580">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="c4bbc-580">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="c4bbc-581">Dodano obsługę list ACL wykazu przy użyciu następujących poleceń:</span><span class="sxs-lookup"><span data-stu-id="c4bbc-581">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="c4bbc-582">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c4bbc-582">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="c4bbc-583">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c4bbc-583">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="c4bbc-584">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c4bbc-584">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="c4bbc-585">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c4bbc-585">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="c4bbc-586">Dodano obsługę anulowania i śledzenia postępu dla poleceń Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="c4bbc-586">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="c4bbc-587">Dodano obsługę anulowania dla polecenia Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="c4bbc-587">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="c4bbc-588">Naprawiono opróżnianie komunikatów debugowania dla poleceń cmdlet wykonujących operacje cykliczne</span><span class="sxs-lookup"><span data-stu-id="c4bbc-588">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="c4bbc-589">Naprawiono lokalizację testu poleceń cmdlet DataLake</span><span class="sxs-lookup"><span data-stu-id="c4bbc-589">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="c4bbc-590">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="c4bbc-590">AzureRM.EventHub</span></span>
* <span data-ttu-id="c4bbc-591">Dodano opcjonalny parametr MaxCount do poleceń cmdlet tworzących listę operacji: Get-AzureRmEventHub i Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="c4bbc-591">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="c4bbc-592">Rozwiązano problem z poleceniem cmdlet New-AzureRmEventHub polegający na tym, że podczas tworzenia nowego centrum EventHub był wymagany co najmniej jeden parametr.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-592">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="c4bbc-593">Udostępniono zestaw parametrów domyślnych.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-593">Provided Default Parameter set.</span></span>
* <span data-ttu-id="c4bbc-594">Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmEventHubKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-594">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="c4bbc-595">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c4bbc-595">AzureRM.KeyVault</span></span>
* <span data-ttu-id="c4bbc-596">Rozwiązano problem polegający na tym, że wszystkie zasoby były zwracane przez polecenie Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="c4bbc-596">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c4bbc-597">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c4bbc-597">AzureRM.Network</span></span>
* <span data-ttu-id="c4bbc-598">Uwidoczniono nowe jednostki SKU dla strefowo nadmiarowych bram VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="c4bbc-598">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="c4bbc-599">Dodano nowe polecenia dla funkcji interfejsów API partnerów usługi ExpressRoute za pośrednictwem usługi ARM</span><span class="sxs-lookup"><span data-stu-id="c4bbc-599">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="c4bbc-600">Dodano polecenie Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="c4bbc-600">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="c4bbc-601">Dodano polecenie Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="c4bbc-601">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="c4bbc-602">Dodano polecenie Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="c4bbc-602">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="c4bbc-603">Dodano polecenie Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="c4bbc-603">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="c4bbc-604">Dodano polecenie Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="c4bbc-604">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="c4bbc-605">Dodano polecenie Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="c4bbc-605">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="c4bbc-606">Dodano polecenie Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="c4bbc-606">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="c4bbc-607">Dodano polecenie Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="c4bbc-607">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="c4bbc-608">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="c4bbc-608">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="c4bbc-609">Dodano polecenie cmdlet Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-609">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="c4bbc-610">To polecenie cmdlet pobiera identyfikator maszyny wirtualnej i sprawdza, czy maszyna wirtualna jest chroniona przez magazyn w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-610">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="c4bbc-611">Jeśli taki magazyn istnieje, polecenie cmdlet wyświetla jego szczegóły.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-611">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c4bbc-612">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c4bbc-612">AzureRM.Resources</span></span>
* <span data-ttu-id="c4bbc-613">Zaktualizowano polecenia cmdlet Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="c4bbc-613">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="c4bbc-614">Dodano obsługę wyświetlania listy wartości -Scope na poziomie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="c4bbc-614">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="c4bbc-615">Dodano obsługę pobierania poszczególnych przydziałów za pomocą wartości -Scope na poziomie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="c4bbc-615">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="c4bbc-616">Dodano przełączniki -Effective i -All do parametru kontroli</span><span class="sxs-lookup"><span data-stu-id="c4bbc-616">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="c4bbc-617">Zaktualizowano polecenia cmdlet Get/New/Remove/Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c4bbc-617">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="c4bbc-618">Dodano parametr -ManagementGroupName w celu zastosowania operacji do danej grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="c4bbc-618">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="c4bbc-619">Dodano parametr -SubscriptionId w celu zastosowania operacji do danej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="c4bbc-619">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="c4bbc-620">Zaktualizowano polecenia cmdlet Get/New/Remove/Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="c4bbc-620">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="c4bbc-621">Dodano parametr -ManagementGroupName w celu zastosowania operacji do danej grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="c4bbc-621">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="c4bbc-622">Dodano parametr -SubscriptionId w celu zastosowania operacji do danej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="c4bbc-622">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="c4bbc-623">Dodano obsługę odwołania do wpisu tajnego KeyVault w parametrach w przypadku używania elementu „TemplateParameterObject” w poleceniu „New-AzureRmResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="c4bbc-623">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="c4bbc-624">Rozwiązano problem polegający na tym, że parametr „-EndDate” był ignorowany w poleceniu „New-AzureRmADAppCredential”</span><span class="sxs-lookup"><span data-stu-id="c4bbc-624">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="c4bbc-625">Rozwiązano problem polegający na tym, że w poleceniu „Add-AzureRmADGroupMember” używano nieprawidłowego adres URL podczas zgłaszania żądania</span><span class="sxs-lookup"><span data-stu-id="c4bbc-625">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="c4bbc-626">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c4bbc-626">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c4bbc-627">Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmServiceBusKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-627">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="c4bbc-628">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c4bbc-628">AzureRM.Sql</span></span>
* <span data-ttu-id="c4bbc-629">Objaśniono punkty przywracania zdefiniowane przez użytkownika dla usługi SQLDW w pomocy polecenia New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="c4bbc-629">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="c4bbc-630">Zaktualizowano dokumentację parametru -ComputeGeneration w kilku poleceniach cmdlet</span><span class="sxs-lookup"><span data-stu-id="c4bbc-630">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="c4bbc-631">6.3.0 — czerwiec 2018</span><span class="sxs-lookup"><span data-stu-id="c4bbc-631">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="c4bbc-632">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c4bbc-632">AzureRM.Profile</span></span>
* <span data-ttu-id="c4bbc-633">Zaktualizowano komunikaty o błędach dotyczące polecenia Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="c4bbc-633">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="c4bbc-634">Tworzenie kontekstu dla każdej subskrypcji w przypadku uruchomienia polecenia „Connect-AzureRmAccount” bez wcześniejszego kontekstu</span><span class="sxs-lookup"><span data-stu-id="c4bbc-634">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="c4bbc-635">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="c4bbc-635">Azure.Storage</span></span>
* <span data-ttu-id="c4bbc-636">Dodano informacje dotyczące parametru -Permissions w plikach pomocy.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-636">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c4bbc-637">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c4bbc-637">AzureRM.Compute</span></span>
* <span data-ttu-id="c4bbc-638">Polecenie „Get-AzureRmVmDiskEncryptionStatus” — rozwiązano problem zaobserwowany w przypadku maszyn wirtualnych bez dysków z danymi</span><span class="sxs-lookup"><span data-stu-id="c4bbc-638">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="c4bbc-639">Aktualizacja wersji biblioteki klienckiej obliczeń w celu naprawy następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="c4bbc-639">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="c4bbc-640">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="c4bbc-640">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="c4bbc-641">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="c4bbc-641">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="c4bbc-642">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="c4bbc-642">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="c4bbc-643">Naprawiono następujące polecenia cmdlet w celu poprawnego wyświetlania identyfikatora operacji i stanu operacji:</span><span class="sxs-lookup"><span data-stu-id="c4bbc-643">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="c4bbc-644">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c4bbc-644">Start-AzureRmVM</span></span>
    - <span data-ttu-id="c4bbc-645">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c4bbc-645">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="c4bbc-646">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c4bbc-646">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="c4bbc-647">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c4bbc-647">Set-AzureRmVM</span></span>
    - <span data-ttu-id="c4bbc-648">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="c4bbc-648">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="c4bbc-649">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c4bbc-649">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="c4bbc-650">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="c4bbc-650">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="c4bbc-651">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="c4bbc-651">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="c4bbc-652">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c4bbc-652">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="c4bbc-653">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c4bbc-653">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="c4bbc-654">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c4bbc-654">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="c4bbc-655">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c4bbc-655">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="c4bbc-656">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="c4bbc-656">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="c4bbc-657">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="c4bbc-657">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="c4bbc-658">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="c4bbc-658">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="c4bbc-659">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="c4bbc-659">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="c4bbc-660">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="c4bbc-660">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="c4bbc-661">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="c4bbc-661">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="c4bbc-662">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c4bbc-662">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="c4bbc-663">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="c4bbc-663">AzureRM.EventGrid</span></span>
* <span data-ttu-id="c4bbc-664">Usunięto warunki weryfikacji ValidateNotNullOrEmpty dla elementów SubjectBeginsWith/SubjectEndsWith w poleceniu cmdlet Update-AzureRmEventGridSubscription w celu umożliwienia zmiany tych parametrów na pusty ciąg w razie potrzeby.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-664">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="c4bbc-665">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c4bbc-665">AzureRM.KeyVault</span></span>
* <span data-ttu-id="c4bbc-666">Rozwiązano problem polegający na tym, że nie były zwracane tagi w przypadku uruchomienia polecenia Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="c4bbc-666">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="c4bbc-667">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="c4bbc-667">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="c4bbc-668">Publiczne udostępnienie poleceń cmdlet usługi Policy Insights</span><span class="sxs-lookup"><span data-stu-id="c4bbc-668">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="c4bbc-669">Użycie interfejsu API w wersji z 4.04.2018</span><span class="sxs-lookup"><span data-stu-id="c4bbc-669">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="c4bbc-670">Dodano element PolicyDefinitionReferenceId do wyników polecenia Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="c4bbc-670">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="c4bbc-671">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="c4bbc-671">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="c4bbc-672">Dodano parametr -Vault do poleceń cmdlet RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-672">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="c4bbc-673">W przypadku przekazania to polecenie przesłania polecenie cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-673">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="c4bbc-674">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c4bbc-674">AzureRM.Sql</span></span>
* <span data-ttu-id="c4bbc-675">Zaktualizowano przykład w pliku pomocy polecenia Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="c4bbc-675">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="c4bbc-676">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="c4bbc-676">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="c4bbc-677">Zaktualizowano plik pomocy polecenia Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="c4bbc-677">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="c4bbc-678">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="c4bbc-678">AzureRM.Websites</span></span>
* <span data-ttu-id="c4bbc-679">Zaktualizowano polecenie „Set-AzureRmWebApp”, aby nie zastępowało elementu AppSettings w przypadku użycia parametru -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="c4bbc-679">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="c4bbc-680">Zaktualizowano polecenie „New-AzureRmWebAppSlot” w celu umożliwienia obsługi parametru AppServicePlan jako parametru opcjonalnego</span><span class="sxs-lookup"><span data-stu-id="c4bbc-680">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="c4bbc-681">6.2.1 — czerwiec 2018</span><span class="sxs-lookup"><span data-stu-id="c4bbc-681">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="c4bbc-682">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c4bbc-682">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="c4bbc-683">Zaktualizowano model PSWorkspace w celu umożliwienia użycia typu jako parametru w sieci</span><span class="sxs-lookup"><span data-stu-id="c4bbc-683">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="c4bbc-684">6.2.0 — czerwiec 2018</span><span class="sxs-lookup"><span data-stu-id="c4bbc-684">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="c4bbc-685">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c4bbc-685">AzureRM.Profile</span></span>
* <span data-ttu-id="c4bbc-686">Naprawiono problem, który polegał na tym, że wersja 10.0.3 pliku Newtonsoft.Json nie była ładowana podczas importowania modułu</span><span class="sxs-lookup"><span data-stu-id="c4bbc-686">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c4bbc-687">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c4bbc-687">AzureRM.Compute</span></span>
* <span data-ttu-id="c4bbc-688">Funkcja aktualizacji maszyny wirtualnej usługi VMSS</span><span class="sxs-lookup"><span data-stu-id="c4bbc-688">VMSS VM Update feature</span></span>
    - <span data-ttu-id="c4bbc-689">Dodano polecenia cmdlet „Update-AzureRmVmssVM” i „New-AzureRmVMDataDisk”</span><span class="sxs-lookup"><span data-stu-id="c4bbc-689">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="c4bbc-690">Dodano parametr VirtualMachineScaleSetVM do polecenia cmdlet „Add-AzureRmVMDataDisk” w celu obsługi dodawania dysku danych do maszyny wirtualnej usługi VMSS.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-690">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="c4bbc-691">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="c4bbc-691">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="c4bbc-692">Zaktualizowano zestaw ADF .Net SDK do wersji 0.8.0-preview zawierającej następujące zmiany:</span><span class="sxs-lookup"><span data-stu-id="c4bbc-692">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="c4bbc-693">Dodano operację repozytorium do konfigurowania fabryki</span><span class="sxs-lookup"><span data-stu-id="c4bbc-693">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="c4bbc-694">Zaktualizowano usługę QuickBooks LinkedService w celu ujawnienia właściwości consumerKey i consumerSecret</span><span class="sxs-lookup"><span data-stu-id="c4bbc-694">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="c4bbc-695">Zaktualizowano wiele typów modeli, od SecretBase do Object</span><span class="sxs-lookup"><span data-stu-id="c4bbc-695">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="c4bbc-696">Dodano wyzwalacz zdarzeń obiektów blob</span><span class="sxs-lookup"><span data-stu-id="c4bbc-696">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="c4bbc-697">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c4bbc-697">AzureRM.KeyVault</span></span>
* <span data-ttu-id="c4bbc-698">Zaktualizowano dokumentację o przykładowe dane wyjściowe</span><span class="sxs-lookup"><span data-stu-id="c4bbc-698">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="c4bbc-699">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c4bbc-699">AzureRM.Network</span></span>
* <span data-ttu-id="c4bbc-700">Parametry włączania analizy ruchu w poleceniach cmdlet narzędzia Network Watcher</span><span class="sxs-lookup"><span data-stu-id="c4bbc-700">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c4bbc-701">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c4bbc-701">AzureRM.Resources</span></span>
* <span data-ttu-id="c4bbc-702">Rozwiązano problem z właściwością „Properties” obiektu „PSResource” zwracanego z polecenia „Get-AzureRmResource”</span><span class="sxs-lookup"><span data-stu-id="c4bbc-702">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="c4bbc-703">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="c4bbc-703">AzureRM.Scheduler</span></span>
* <span data-ttu-id="c4bbc-704">Rozwiązano problem z aktualizacją ServiceBusQueueJob, która nie ustawiała nowych wartości uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="c4bbc-704">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="c4bbc-705">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c4bbc-705">AzureRM.Sql</span></span>
* <span data-ttu-id="c4bbc-706">Zaktualizowano następujące polecenia cmdlet o opcjonalny parametr LicenseType</span><span class="sxs-lookup"><span data-stu-id="c4bbc-706">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="c4bbc-707">New-AzureRmSqlDatabase, Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c4bbc-707">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="c4bbc-708">New-AzureRmSqlElasticPool, Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c4bbc-708">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="c4bbc-709">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="c4bbc-709">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="c4bbc-710">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="c4bbc-710">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="c4bbc-711">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c4bbc-711">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="c4bbc-712">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="c4bbc-712">AzureRM.Websites</span></span>
* <span data-ttu-id="c4bbc-713">Polecenie „New-AzureRMWebApp” zostało zaktualizowane w celu używania typowych algorytmów z biblioteki strategii.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-713">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="c4bbc-714">6.1.0 — maj 2018 r.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-714">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="c4bbc-715">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c4bbc-715">AzureRM.Profile</span></span>
* <span data-ttu-id="c4bbc-716">Rozwiązano problem polegający na tym, że po uruchomieniu polecenia „Clear-AzureRmContext” pozostawał pusty kontekst o nazwie takiej jak poprzedni kontekst domyślny, co uniemożliwiało użytkownikowi utworzenie nowego kontekstu ze starą nazwą</span><span class="sxs-lookup"><span data-stu-id="c4bbc-716">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="c4bbc-717">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c4bbc-717">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="c4bbc-718">Włączono operacje kojarzenia/usuwania skojarzenia bramy w usłudze AS.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-718">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="c4bbc-719">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c4bbc-719">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="c4bbc-720">Dodano obsługę elementów ApiVersion, ApiRelease oraz ApiRevision</span><span class="sxs-lookup"><span data-stu-id="c4bbc-720">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="c4bbc-721">Dodano obsługę zaplecza ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c4bbc-721">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="c4bbc-722">Dodano obsługę rejestratora usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="c4bbc-722">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="c4bbc-723">Dodano obsługę rozpoznawania jednostki SKU „Podstawowa” jako prawidłowej jednostki SKU usługi API Management</span><span class="sxs-lookup"><span data-stu-id="c4bbc-723">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="c4bbc-724">Dodano obsługę instalowania certyfikatów wystawionych przez prywatny urząd certyfikacji jako certyfikatów głównych lub certyfikatów urzędu certyfikacji</span><span class="sxs-lookup"><span data-stu-id="c4bbc-724">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="c4bbc-725">Dodano obsługę akceptowania niestandardowych certyfikatów SSL za pomocą magazynu kluczy i wielu nazw hostów serwera proxy</span><span class="sxs-lookup"><span data-stu-id="c4bbc-725">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="c4bbc-726">Dodano obsługę tożsamości MSI</span><span class="sxs-lookup"><span data-stu-id="c4bbc-726">Added support for MSI identity</span></span>
* <span data-ttu-id="c4bbc-727">Dodano obsługę akceptowania zasad za pomocą adresu URL. UWAGA: następujące polecenia cmdlet staną się przestarzałe w przyszłym wydaniu</span><span class="sxs-lookup"><span data-stu-id="c4bbc-727">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="c4bbc-728">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="c4bbc-728">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="c4bbc-729">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4bbc-729">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="c4bbc-730">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="c4bbc-730">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="c4bbc-731">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="c4bbc-731">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="c4bbc-732">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="c4bbc-732">AzureRM.Batch</span></span>
* <span data-ttu-id="c4bbc-733">Wydano nowe polecenie cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="c4bbc-733">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="c4bbc-734">Wydano nowe polecenie cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="c4bbc-734">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="c4bbc-735">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="c4bbc-735">AzureRM.Consumption</span></span>
* <span data-ttu-id="c4bbc-736">Dodano nowe parametry polecenia cmdlet Get-AzureRmConsumptionUsageDetail: Expand, ResourceGroup, InstanceName, InstanceId, Tags oraz Top</span><span class="sxs-lookup"><span data-stu-id="c4bbc-736">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="c4bbc-737">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c4bbc-737">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="c4bbc-738">Poprawiono przykład dla polecenia Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="c4bbc-738">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="c4bbc-739">Rozwiązano problem powodujący wyjątek parametru o wartości null dla przypadku Recurse w poleceniu Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c4bbc-739">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="c4bbc-740">Poprawiono pliki pomocy dla poleceń Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl oraz Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c4bbc-740">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="c4bbc-741">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c4bbc-741">AzureRM.Network</span></span>
* <span data-ttu-id="c4bbc-742">Podniesiono wersję zestawu SDK sieci z 18.0.0-preview do 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="c4bbc-742">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="c4bbc-743">Dodano polecenie cmdlet służące do tworzenia konfiguracji protokołu</span><span class="sxs-lookup"><span data-stu-id="c4bbc-743">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="c4bbc-744">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4bbc-744">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="c4bbc-745">Dodano polecenie cmdlet służące do dodawania nowego połączenia obwodu do istniejącego obwodu usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="c4bbc-745">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="c4bbc-746">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c4bbc-746">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="c4bbc-747">Dodano polecenie cmdlet służące do usuwania połączenia obwodu z istniejącego obwodu usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="c4bbc-747">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="c4bbc-748">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c4bbc-748">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="c4bbc-749">Dodano polecenie cmdlet służące do pobierania połączenia obwodu</span><span class="sxs-lookup"><span data-stu-id="c4bbc-749">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="c4bbc-750">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c4bbc-750">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="c4bbc-751">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c4bbc-751">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="c4bbc-752">Naprawiono użycie uwierzytelniania serwera za pomocą wygenerowanych certyfikatów (problem nr 5998)</span><span class="sxs-lookup"><span data-stu-id="c4bbc-752">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="c4bbc-753">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c4bbc-753">AzureRM.Sql</span></span>
* <span data-ttu-id="c4bbc-754">Zaktualizowano polecenia cmdlet inspekcji w celu umożliwienia usuwania elementów AuditAction lub AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="c4bbc-754">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="c4bbc-755">Rozwiązano problem z poleceniem Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy, który powodował zakończenie polecenia niepowodzeniem podczas ustawiania nowych, elastycznych zasad przechowywania oraz zwrócenie komunikatu „Konfigurowanie zasad przechowywania długoterminowego za pomocą magazynu usługi Azure Recovery Service i zasad nie jest już obsługiwane.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-755">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="c4bbc-756">Prześlij żądanie z nowymi, elastycznymi zasadami przechowywania”.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-756">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="c4bbc-757">Zaktualizowano wszystkie polecenia cmdlet służące do tworzenia/aktualizowania elastycznej puli/bazy danych usługi Azure SQL Database w taki sposób, aby korzystały z nowego interfejsu API bazy danych, który obsługuje właściwość SKU na potrzeby właściwości powiązanych ze skalowaniem i warstwą.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-757">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="c4bbc-758">Zaktualizowane polecenia cmdlet to:</span><span class="sxs-lookup"><span data-stu-id="c4bbc-758">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="c4bbc-759">New-AzureRmSqlDatabase, Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c4bbc-759">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="c4bbc-760">New-AzureRmSqlElasticPool, Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c4bbc-760">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="c4bbc-761">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="c4bbc-761">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="c4bbc-762">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="c4bbc-762">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="c4bbc-763">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c4bbc-763">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="c4bbc-764">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="c4bbc-764">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="c4bbc-765">Zaktualizowano parametry polecenia „Get-AzureRmTrafficManagerProfile”, aby parametr -ResourceGroupName był wymagany, gdy został podany parametr -Name.</span><span class="sxs-lookup"><span data-stu-id="c4bbc-765">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
