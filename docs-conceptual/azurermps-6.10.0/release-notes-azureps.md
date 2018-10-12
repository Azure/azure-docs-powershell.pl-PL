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
ms.openlocfilehash: 6a33d1a85fc61d0281bf1183163185b0dc4d3a12
ms.sourcegitcommit: a749eb729f583c9d0dd86141bbd04984d77ae9ab
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/11/2018
ms.locfileid: "48882245"
---
# <a name="release-notes"></a><span data-ttu-id="f989b-103">Informacje o wersji</span><span class="sxs-lookup"><span data-stu-id="f989b-103">Release notes</span></span>

<span data-ttu-id="f989b-104">To jest lista zmian wprowadzonych w programie Azure PowerShell w tym wydaniu.</span><span class="sxs-lookup"><span data-stu-id="f989b-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6100---october-2018"></a><span data-ttu-id="f989b-105">6.10.0 — październik 2018 r.</span><span class="sxs-lookup"><span data-stu-id="f989b-105">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="f989b-106">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="f989b-106">Azure.Storage</span></span>
* <span data-ttu-id="f989b-107">Rozwiązano problem polegający na tym, że nie można skopiować pliku lub obiektu blob, gdy w miejscu docelowym występuje problem z metadanymi</span><span class="sxs-lookup"><span data-stu-id="f989b-107">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="f989b-108">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f989b-108">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="f989b-109">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="f989b-109">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="f989b-110">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f989b-110">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="f989b-111">Obsługa polecenia Get-AzureRmCognitiveServicesAccountSkus bez istniejącego konta.</span><span class="sxs-lookup"><span data-stu-id="f989b-111">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="f989b-112">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="f989b-112">AzureRM.Compute</span></span>
* <span data-ttu-id="f989b-113">Rozwiązano problem z poleceniem Get-AzureRmVM -ResourceGroupName <rg>, dzięki czemu można zwracać więcej niż 50 wyników, jeśli to konieczne</span><span class="sxs-lookup"><span data-stu-id="f989b-113">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="f989b-114">Dodano przykładowy zestaw SimpleParameterSet do pomocy polecenia cmdlet New-AzureRmVmss.</span><span class="sxs-lookup"><span data-stu-id="f989b-114">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="f989b-115">Usunięto błąd pisowni w komunikacie o postępie usługi Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="f989b-115">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="f989b-116">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f989b-116">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="f989b-117">Zaktualizowano zestaw ADF .Net SDK do wersji 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="f989b-117">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="f989b-118">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="f989b-118">AzureRM.Network</span></span>
* <span data-ttu-id="f989b-119">Dodano funkcję NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="f989b-119">Added NetworkProfile functionality.</span></span> <span data-ttu-id="f989b-120">Dodano nowe polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="f989b-120">new cmdlets added</span></span>
    - <span data-ttu-id="f989b-121">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f989b-121">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="f989b-122">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f989b-122">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="f989b-123">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f989b-123">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="f989b-124">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f989b-124">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="f989b-125">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="f989b-125">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="f989b-126">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="f989b-126">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="f989b-127">Dodano link skojarzenia usługi w modelu podsieci</span><span class="sxs-lookup"><span data-stu-id="f989b-127">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="f989b-128">Dodano polecenia cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap i Remove-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="f989b-128">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="f989b-129">Dodano polecenia cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig i Remove-AzureRmNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="f989b-129">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="f989b-130">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f989b-130">AzureRM.RedisCache</span></span>
* <span data-ttu-id="f989b-131">Jako parametru Size będzie można użyć dowolnego ciągu.</span><span class="sxs-lookup"><span data-stu-id="f989b-131">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="f989b-132">Dodano element P5 w menu podręcznym PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="f989b-132">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="f989b-133">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="f989b-133">AzureRM.Resources</span></span>
* <span data-ttu-id="f989b-134">Dodano brakujący parametr -Mode do polecenia Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f989b-134">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="f989b-135">Usunięto błąd polecenia Get-AzureRmProviderOperation w operacjach ze źródłem zawierającym użytkownika</span><span class="sxs-lookup"><span data-stu-id="f989b-135">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="f989b-136">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="f989b-136">AzureRM.Sql</span></span>
* <span data-ttu-id="f989b-137">Rozwiązano problem polegający na tym, że niektóre polecenia cmdlet kopii zapasowych nie rozpoznawały bieżącej subskrypcji platformy Azure</span><span class="sxs-lookup"><span data-stu-id="f989b-137">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="f989b-138">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="f989b-138">AzureRM.Storage</span></span>
* <span data-ttu-id="f989b-139">Dodano obsługę pobierania danych użycia zasobów magazynu w określonej lokalizacji i dodano komunikat ostrzegawczy w przypadku pobrania przestarzałych danych użycia globalnego zasobu magazynu.</span><span class="sxs-lookup"><span data-stu-id="f989b-139">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="f989b-140">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="f989b-140">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="f989b-141">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="f989b-141">AzureRM.Websites</span></span>
* <span data-ttu-id="f989b-142">Nowe polecenie cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl umożliwiające pobranie adresu URL elementu webhook ciągłe wdrażania kontenera</span><span class="sxs-lookup"><span data-stu-id="f989b-142">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="f989b-143">Nowe polecenia cmdlet New-AzureRMWebAppContainerPSSession i Enter-WebAppContainerPSSession umożliwiające zainicjowanie zdalnej sesji programu PowerShell w aplikacji kontenera systemu Windows</span><span class="sxs-lookup"><span data-stu-id="f989b-143">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="f989b-144">6.9.0 — wrzesień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="f989b-144">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="f989b-145">Ogólne</span><span class="sxs-lookup"><span data-stu-id="f989b-145">General</span></span>
* <span data-ttu-id="f989b-146">Element AzureRM.SignalR został dodany do modułu zbiorczego AzureRM</span><span class="sxs-lookup"><span data-stu-id="f989b-146">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="f989b-147">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="f989b-147">AzureRM.Profile</span></span>
* <span data-ttu-id="f989b-148">Drobne zmiany wspólnego kodu magazynu</span><span class="sxs-lookup"><span data-stu-id="f989b-148">Minor changes to the storage common code</span></span>
* <span data-ttu-id="f989b-149">Zaktualizowano pliki pomocy w celu uwzględnienia pełnych typów parametrów.</span><span class="sxs-lookup"><span data-stu-id="f989b-149">Updated help files to include full parameter types.</span></span>
- <span data-ttu-id="f989b-150">Zmieniono opcję -ServicePrincipal na nieobowiązkową w zestawie parametrów ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f989b-150">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="f989b-151">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="f989b-151">Azure.Storage</span></span>
* <span data-ttu-id="f989b-152">Obsługa tworzenia kontekstu magazynu przy użyciu protokołu OAuth.</span><span class="sxs-lookup"><span data-stu-id="f989b-152">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="f989b-153">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="f989b-153">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="f989b-154">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="f989b-154">AzureRM.Cdn</span></span>
* <span data-ttu-id="f989b-155">Dodano element Standard_Microsoft w jednostce SKU cen usługi CDN.</span><span class="sxs-lookup"><span data-stu-id="f989b-155">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="f989b-156">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="f989b-156">AzureRM.Compute</span></span>
* <span data-ttu-id="f989b-157">Przeniesiono zależności magazynu kluczy i magazynu do zależności wspólnych</span><span class="sxs-lookup"><span data-stu-id="f989b-157">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="f989b-158">Dodano obsługę kolejnych rozmiarów maszyn wirtualnych do poleceń cmdlet funkcji AEM</span><span class="sxs-lookup"><span data-stu-id="f989b-158">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="f989b-159">Dodano parametr PublicIPPrefix do polecenia New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="f989b-159">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="f989b-160">Dodano parametr ResourceId do polecenia cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="f989b-160">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="f989b-161">Dodano polecenie cmdlet Invoke-AzureRmVmssVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="f989b-161">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="f989b-162">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="f989b-162">AzureRM.Dns</span></span>
* <span data-ttu-id="f989b-163">Dodano obsługę rekordu aliasu podczas tworzenia rekordów DNS</span><span class="sxs-lookup"><span data-stu-id="f989b-163">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="f989b-164">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="f989b-164">AzureRM.Insights</span></span>
* <span data-ttu-id="f989b-165">Rozwiązano problemy nr 6833 i 7102 (obszar ustawień diagnostycznych)</span><span class="sxs-lookup"><span data-stu-id="f989b-165">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="f989b-166">Problemy z nazwą domyślną, np. „usługa”, podczas tworzenia i tworzenia/pobierania listy ustawień diagnostycznych</span><span class="sxs-lookup"><span data-stu-id="f989b-166">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="f989b-167">Problemy z tworzeniem ustawień diagnostycznych przy użyciu kategorii</span><span class="sxs-lookup"><span data-stu-id="f989b-167">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="f989b-168">Dodano komunikat o zakończeniu obsługi parametrów ziarn czasu metryk</span><span class="sxs-lookup"><span data-stu-id="f989b-168">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="f989b-169">Parametry typu Timegrain są nadal akceptowane (jest to zmiana niepowodująca niezgodności), ale są one ignorowane w zapleczu, ponieważ tylko wersja PT1M jest prawidłowa</span><span class="sxs-lookup"><span data-stu-id="f989b-169">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="f989b-170">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="f989b-170">AzureRM.Network</span></span>
* <span data-ttu-id="f989b-171">Zmiany poleceń cmdlet usługi LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f989b-171">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="f989b-172">LoadBalancerInboundNatPoolConfig: dodano parametry IdleTimeoutInMinutes, EnableFloatingIp i EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="f989b-172">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="f989b-173">LoadBalancerInboundNatRuleConfig: dodano parametr EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="f989b-173">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="f989b-174">LoadBalancerRuleConfig: dodano parametr EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="f989b-174">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="f989b-175">LoadBalancerProbeConfig: dodano obsługę wartości „Https” dla parametru Protocol</span><span class="sxs-lookup"><span data-stu-id="f989b-175">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="f989b-176">Dodano nowe polecenia dla nowego zasobu podrzędnego OutboundRule usługi LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f989b-176">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="f989b-177">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f989b-177">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="f989b-178">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f989b-178">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="f989b-179">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f989b-179">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="f989b-180">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f989b-180">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="f989b-181">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f989b-181">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="f989b-182">Dodano nową właściwość HostedWorkloads dla interfejsu PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f989b-182">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="f989b-183">Dodano nowe polecenia cmdlet dla funkcji Azure Firewall za pośrednictwem usługi ARM</span><span class="sxs-lookup"><span data-stu-id="f989b-183">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="f989b-184">Dodano polecenie Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="f989b-184">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="f989b-185">Dodano polecenie Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="f989b-185">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="f989b-186">Dodano polecenie New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="f989b-186">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="f989b-187">Dodano polecenie Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="f989b-187">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="f989b-188">Dodano polecenie New-AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="f989b-188">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="f989b-189">Dodano polecenie New-AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="f989b-189">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="f989b-190">Dodano polecenie New-AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="f989b-190">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="f989b-191">Dodano polecenie New-AzureRmFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="f989b-191">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="f989b-192">Dodano polecenie New-AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="f989b-192">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="f989b-193">Dodano polecenie New-AzureRmFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f989b-193">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="f989b-194">Dodano obsługę zaufanego certyfikatu głównego i konfiguracji skalowania automatycznego w usłudze Application Gateway</span><span class="sxs-lookup"><span data-stu-id="f989b-194">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="f989b-195">Dodano nowe polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f989b-195">New Cmdlets added:</span></span>
      - <span data-ttu-id="f989b-196">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f989b-196">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="f989b-197">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f989b-197">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="f989b-198">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f989b-198">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="f989b-199">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f989b-199">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="f989b-200">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f989b-200">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="f989b-201">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f989b-201">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="f989b-202">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f989b-202">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="f989b-203">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f989b-203">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="f989b-204">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f989b-204">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="f989b-205">Zaktualizowano polecenia cmdlet przy użyciu opcjonalnego parametru -TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f989b-205">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="f989b-206">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f989b-206">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="f989b-207">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f989b-207">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="f989b-208">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="f989b-208">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="f989b-209">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="f989b-209">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="f989b-210">Zaktualizowano polecenia cmdlet przy użyciu opcjonalnego parametru -AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f989b-210">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="f989b-211">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f989b-211">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="f989b-212">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f989b-212">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="f989b-213">Dodano polecenie cmdlet dla punktu końcowego interfejsu Get-AzureInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="f989b-213">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="f989b-214">Dodano obsługę wielu prefiksów adresów w podsieci.</span><span class="sxs-lookup"><span data-stu-id="f989b-214">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="f989b-215">Zaktualizowano następujące polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f989b-215">Updated cmdlets:</span></span>
  - <span data-ttu-id="f989b-216">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f989b-216">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="f989b-217">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f989b-217">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="f989b-218">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f989b-218">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="f989b-219">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f989b-219">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="f989b-220">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f989b-220">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="f989b-221">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f989b-221">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="f989b-222">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f989b-222">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="f989b-223">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f989b-223">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="f989b-224">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f989b-224">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="f989b-225">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f989b-225">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="f989b-226">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f989b-226">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="f989b-227">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f989b-227">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="f989b-228">New-AzureRmNetworkInterfaceIpConfig — Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f989b-228">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="f989b-229">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="f989b-229">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="f989b-230">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="f989b-230">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="f989b-231">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f989b-231">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="f989b-232">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f989b-232">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="f989b-233">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f989b-233">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="f989b-234">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f989b-234">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="f989b-235">Dodano polecenia cmdlet na potrzeby delegowania podsieci.</span><span class="sxs-lookup"><span data-stu-id="f989b-235">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="f989b-236">New-AzureRmDelegation: tworzy nowe delegowanie, które można dodać do podsieci</span><span class="sxs-lookup"><span data-stu-id="f989b-236">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="f989b-237">Remove-AzureRmDelegation: pobiera podsieć i usuwa z niej podaną nazwę delegowania</span><span class="sxs-lookup"><span data-stu-id="f989b-237">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="f989b-238">Add-AzureRmDelegation: pobiera podsieć i dodaje do niej podaną nazwę usługi jako delegowanie</span><span class="sxs-lookup"><span data-stu-id="f989b-238">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="f989b-239">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="f989b-239">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="f989b-240">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="f989b-240">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="f989b-241">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="f989b-241">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="f989b-242">Obsługa dysków zarządzanych</span><span class="sxs-lookup"><span data-stu-id="f989b-242">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="f989b-243">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f989b-243">AzureRM.RedisCache</span></span>
* <span data-ttu-id="f989b-244">Zaktualizowano zależność szczegółowych informacji.</span><span class="sxs-lookup"><span data-stu-id="f989b-244">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="f989b-245">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="f989b-245">AzureRM.Resources</span></span>
* <span data-ttu-id="f989b-246">Zaktualizowano polecenie New-AzureRmResourceGroupDeployment przy użyciu nowego parametru RollbackAction</span><span class="sxs-lookup"><span data-stu-id="f989b-246">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="f989b-247">Dodano obsługę elementu OnErrorDeployment przy użyciu nowego parametru.</span><span class="sxs-lookup"><span data-stu-id="f989b-247">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="f989b-248">Obsługa tożsamości zarządzanej w przypisaniach zasad.</span><span class="sxs-lookup"><span data-stu-id="f989b-248">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="f989b-249">Parametry z wartościami domyślnymi nie są już wymagane podczas przypisywania zasad za pomocą polecenia „New-AzureRmPolicyAssignment”</span><span class="sxs-lookup"><span data-stu-id="f989b-249">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="f989b-250">Dodano nowe polecenie cmdlet Get-AzureRmPolicyAlias służące do pobierania aliasów zasad</span><span class="sxs-lookup"><span data-stu-id="f989b-250">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="f989b-251">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f989b-251">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="f989b-252">Rozwiązano problem nr 7161</span><span class="sxs-lookup"><span data-stu-id="f989b-252">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="f989b-253">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="f989b-253">AzureRM.SignalR</span></span>
* <span data-ttu-id="f989b-254">Zaktualizowano nazwy jednostek SKU Bezpłatna_F1 i Standardowa_S1</span><span class="sxs-lookup"><span data-stu-id="f989b-254">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="f989b-255">Dodano pole wersji do obiektu PSSignalRResource i parametry połączenia do obiektu PSSignalRKeys.</span><span class="sxs-lookup"><span data-stu-id="f989b-255">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="f989b-256">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="f989b-256">AzureRM.Storage</span></span>
* <span data-ttu-id="f989b-257">Obsługa zasad niezmienności w elemencie AzureRm.Storage</span><span class="sxs-lookup"><span data-stu-id="f989b-257">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="f989b-258">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f989b-258">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="f989b-259">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f989b-259">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="f989b-260">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f989b-260">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="f989b-261">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f989b-261">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="f989b-262">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f989b-262">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="f989b-263">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="f989b-263">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="f989b-264">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="f989b-264">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="f989b-265">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="f989b-265">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="f989b-266">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="f989b-266">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="f989b-267">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="f989b-267">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="f989b-268">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="f989b-268">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="f989b-269">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="f989b-269">AzureRM.Websites</span></span>
* <span data-ttu-id="f989b-270">Dodano dwa nowe polecenia cmdlet: Get-AzureRmDeletedWebApp i Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="f989b-270">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="f989b-271">New-AzureRmAppServicePlan — dodano przełącznik funkcji Hyper-V na potrzeby tworzenia planu usługi App Service przy użyciu kontenera systemu Windows</span><span class="sxs-lookup"><span data-stu-id="f989b-271">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="f989b-272">New-AzureRmWebApp/New-AzureRmWebAppSlot/Set-AzureRmWebApp/Set-AzureRmWebAppSlot — dodano nowe parametry (ciąg –ContainerRegistryUser -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) na potrzeby tworzenia aplikacji kontenera systemu Windows oraz zarządzania nią</span><span class="sxs-lookup"><span data-stu-id="f989b-272">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="f989b-273">6.8.1 — sierpień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="f989b-273">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="f989b-274">Ogólne</span><span class="sxs-lookup"><span data-stu-id="f989b-274">General</span></span>
* <span data-ttu-id="f989b-275">Rozwiązano problem z nieustawionymi domyślnymi grupami zasobów.</span><span class="sxs-lookup"><span data-stu-id="f989b-275">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="f989b-276">Zaktualizowano wspólne zestawy środowiska uruchomieniowego</span><span class="sxs-lookup"><span data-stu-id="f989b-276">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="f989b-277">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f989b-277">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="f989b-278">Rozwiązano problem z nieustawionymi domyślnymi grupami zasobów.</span><span class="sxs-lookup"><span data-stu-id="f989b-278">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="f989b-279">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="f989b-279">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="f989b-280">Polecenia cmdlet Import-AzureRmApiManagementApi i \*-AzureRmApiManagementCertificate teraz obsługują ścieżki względne</span><span class="sxs-lookup"><span data-stu-id="f989b-280">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="f989b-281">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="f989b-281">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="f989b-282">CertificateInformation to możliwa do ustawienia właściwość pozwalająca poleceniu cmdlet Set-AzureRmApiManagement poprawnie działać.</span><span class="sxs-lookup"><span data-stu-id="f989b-282">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="f989b-283">Rozwiązano przez aktualizację do pakietu nuget 4.0.4-preview</span><span class="sxs-lookup"><span data-stu-id="f989b-283">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="f989b-284">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="f989b-284">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="f989b-285">W filtrze Odata naprawiono wyszukiwanie według nazwy dla produktu</span><span class="sxs-lookup"><span data-stu-id="f989b-285">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="f989b-286">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="f989b-286">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="f989b-287">W filtrze Odata naprawiono wyszukiwanie według nazwy dla interfejsu API</span><span class="sxs-lookup"><span data-stu-id="f989b-287">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="f989b-288">Dodano obsługę rejestratora AzureMonitor</span><span class="sxs-lookup"><span data-stu-id="f989b-288">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="f989b-289">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="f989b-289">AzureRM.Compute</span></span>
* <span data-ttu-id="f989b-290">Naprawiono problem polegający na braku elementu docelowego w danych wyjściowych błędu.</span><span class="sxs-lookup"><span data-stu-id="f989b-290">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="f989b-291">Rozwiązano problem z typem konta magazynu dla maszyny wirtualnej z dyskiem zarządzanym</span><span class="sxs-lookup"><span data-stu-id="f989b-291">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="f989b-292">Rozwiązano problem z nieustawionymi domyślnymi grupami zasobów.</span><span class="sxs-lookup"><span data-stu-id="f989b-292">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="f989b-293">Naprawiono polecenia cmdlet rozszerzenia AEM dla innych środowisk, na przykład Azure — Chiny</span><span class="sxs-lookup"><span data-stu-id="f989b-293">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="f989b-294">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="f989b-294">AzureRM.Network</span></span>
* <span data-ttu-id="f989b-295">Zmieniono domyślną prezentację danych wyjściowych polecenia cmdlet na widok tabeli</span><span class="sxs-lookup"><span data-stu-id="f989b-295">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="f989b-296">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="f989b-296">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="f989b-297">Naprawiono błąd w poleceniu Update-AzureRmPowerBIEmbeddedCapacity występujący podczas próby skalowania wstrzymanej pojemności</span><span class="sxs-lookup"><span data-stu-id="f989b-297">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="f989b-298">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="f989b-298">AzureRM.Resources</span></span>
* <span data-ttu-id="f989b-299">Rozwiązano problem z tworzeniem aplikacji zarządzanych z witryny MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="f989b-299">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="f989b-300">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f989b-300">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="f989b-301">Rozwiązane problemy</span><span class="sxs-lookup"><span data-stu-id="f989b-301">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="f989b-302">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="f989b-302">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="f989b-303">Dodano obsługę metody routingu MultiValue</span><span class="sxs-lookup"><span data-stu-id="f989b-303">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="f989b-304">Nowy parametr „MaxReturn” dla routingu MultiValue</span><span class="sxs-lookup"><span data-stu-id="f989b-304">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="f989b-305">Dodano obsługę metody routingu Subnet</span><span class="sxs-lookup"><span data-stu-id="f989b-305">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="f989b-306">Obsługa zakresów adresów IP (podsieci) w punktach końcowych</span><span class="sxs-lookup"><span data-stu-id="f989b-306">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="f989b-307">Dodano obsługę nagłówków niestandardowych w profilach</span><span class="sxs-lookup"><span data-stu-id="f989b-307">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="f989b-308">Dodano obsługę zakresów kodów oczekiwanego stanu w profilach</span><span class="sxs-lookup"><span data-stu-id="f989b-308">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="f989b-309">Dodano obsługę nagłówków niestandardowych w punktach końcowych</span><span class="sxs-lookup"><span data-stu-id="f989b-309">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="f989b-310">6.8.0 — sierpień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="f989b-310">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="f989b-311">Ogólne</span><span class="sxs-lookup"><span data-stu-id="f989b-311">General</span></span>
* <span data-ttu-id="f989b-312">Rozwiązano problem z nieustawionymi domyślnymi grupami zasobów.</span><span class="sxs-lookup"><span data-stu-id="f989b-312">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="f989b-313">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="f989b-313">AzureRM.Profile</span></span>
* <span data-ttu-id="f989b-314">Dodano właściwość wygasania do tokenów zwracanych podczas operacji Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="f989b-314">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="f989b-315">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="f989b-315">AzureRM.Compute</span></span>
* <span data-ttu-id="f989b-316">Naprawiono problem polegający na braku elementu docelowego w danych wyjściowych błędu.</span><span class="sxs-lookup"><span data-stu-id="f989b-316">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="f989b-317">Rozwiązano problem z typem konta magazynu dla maszyny wirtualnej z dyskiem zarządzanym</span><span class="sxs-lookup"><span data-stu-id="f989b-317">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="f989b-318">Naprawiono polecenia cmdlet rozszerzenia AEM dla innych środowisk, na przykład Azure — Chiny</span><span class="sxs-lookup"><span data-stu-id="f989b-318">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="f989b-319">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="f989b-319">AzureRM.IotHub</span></span>
* <span data-ttu-id="f989b-320">Naprawiono przykłady dla poleceń New-AzureRmIotHubExportDevices i New-AzureRmIotHubImportDevices</span><span class="sxs-lookup"><span data-stu-id="f989b-320">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="f989b-321">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="f989b-321">AzureRM.Network</span></span>
* <span data-ttu-id="f989b-322">Zmieniono domyślną reprezentację modeli na widok tabeli</span><span class="sxs-lookup"><span data-stu-id="f989b-322">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="f989b-323">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="f989b-323">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="f989b-324">Naprawiono błąd w poleceniu Update-AzureRmPowerBIEmbeddedCapacity występujący podczas próby skalowania wstrzymanej pojemności</span><span class="sxs-lookup"><span data-stu-id="f989b-324">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="f989b-325">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="f989b-325">AzureRM.Resources</span></span>
* <span data-ttu-id="f989b-326">Rozwiązano problem z tworzeniem aplikacji zarządzanej z witryny MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="f989b-326">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="f989b-327">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f989b-327">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="f989b-328">Rozwiązano problemy</span><span class="sxs-lookup"><span data-stu-id="f989b-328">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="f989b-329">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="f989b-329">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="f989b-330">Obsługa metody routingu MultiValue</span><span class="sxs-lookup"><span data-stu-id="f989b-330">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="f989b-331">Nowy parametr „MaxReturn” dla routingu MultiValue</span><span class="sxs-lookup"><span data-stu-id="f989b-331">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="f989b-332">Obsługa metody routingu Subnet</span><span class="sxs-lookup"><span data-stu-id="f989b-332">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="f989b-333">Obsługa zakresów adresów IP (podsieci) w punktach końcowych</span><span class="sxs-lookup"><span data-stu-id="f989b-333">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="f989b-334">Obsługa nagłówków niestandardowych w profilach</span><span class="sxs-lookup"><span data-stu-id="f989b-334">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="f989b-335">Obsługa zakresów kodów oczekiwanego stanu w profilach</span><span class="sxs-lookup"><span data-stu-id="f989b-335">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="f989b-336">Obsługa nagłówków niestandardowych w punktach końcowych</span><span class="sxs-lookup"><span data-stu-id="f989b-336">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="f989b-337">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="f989b-337">AzureRM.Websites</span></span>
* <span data-ttu-id="f989b-338">Rozwiązano problem z niepoprawnie ustawionymi domyślnymi grupami zasobów.</span><span class="sxs-lookup"><span data-stu-id="f989b-338">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="f989b-339">6.7.0 — sierpień 2018 r.</span><span class="sxs-lookup"><span data-stu-id="f989b-339">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="f989b-340">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="f989b-340">AzureRM.Profile</span></span>
* <span data-ttu-id="f989b-341">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-341">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="f989b-342">Dodaj identyfikator użytkownika do domyślnej nazwy kontekstu, aby uniknąć konfliktów kontekstów</span><span class="sxs-lookup"><span data-stu-id="f989b-342">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="f989b-343">Rozwiązanie problemu z poleceniem Clear-AzureRmContext, który powodował problemy w przypadku wybrania kontekstu nr 6398</span><span class="sxs-lookup"><span data-stu-id="f989b-343">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="f989b-344">Umożliwienie przekazywania domeny dzierżawy do parametru „-TenantId” polecenia „Connect-AzureRmAccount”</span><span class="sxs-lookup"><span data-stu-id="f989b-344">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="f989b-345">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="f989b-345">Azure.Storage</span></span>
* <span data-ttu-id="f989b-346">Usunięcie ograniczenia limitu przydziału udziału plików platformy Azure do 5 TB</span><span class="sxs-lookup"><span data-stu-id="f989b-346">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="f989b-347">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="f989b-347">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="f989b-348">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f989b-348">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="f989b-349">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-349">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="f989b-350">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f989b-350">Azure.AnalysisServices</span></span>
* <span data-ttu-id="f989b-351">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-351">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="f989b-352">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f989b-352">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="f989b-353">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-353">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="f989b-354">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="f989b-354">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="f989b-355">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-355">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="f989b-356">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="f989b-356">AzureRM.Automation</span></span>
* <span data-ttu-id="f989b-357">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-357">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="f989b-358">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="f989b-358">AzureRM.Backup</span></span>
* <span data-ttu-id="f989b-359">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-359">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="f989b-360">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="f989b-360">AzureRM.Batch</span></span>
* <span data-ttu-id="f989b-361">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-361">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="f989b-362">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="f989b-362">AzureRM.Billing</span></span>
* <span data-ttu-id="f989b-363">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-363">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="f989b-364">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="f989b-364">AzureRM.Cdn</span></span>
* <span data-ttu-id="f989b-365">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-365">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="f989b-366">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f989b-366">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="f989b-367">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-367">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="f989b-368">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="f989b-368">AzureRM.Compute</span></span>
* <span data-ttu-id="f989b-369">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-369">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="f989b-370">Dodanie parametru EvictionPolicy do polecenia New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="f989b-370">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="f989b-371">Użycie domyślnej lokalizacji w parametrze DiskFileParameterSet polecenia New-AzureRmVm, jeśli nie określono lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="f989b-371">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="f989b-372">Naprawienie opisu parametru w poleceniu Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="f989b-372">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="f989b-373">Naprawienie działania polecenia cmdlet Get-AzureRmVMDiskEncryptionStatus w przypadku niektórych scenariuszy powiązanych z pojedynczym przebiegiem</span><span class="sxs-lookup"><span data-stu-id="f989b-373">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="f989b-374">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="f989b-374">AzureRM.Consumption</span></span>
* <span data-ttu-id="f989b-375">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-375">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="f989b-376">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f989b-376">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="f989b-377">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-377">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="f989b-378">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f989b-378">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="f989b-379">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-379">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="f989b-380">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="f989b-380">AzureRM.DataFactories</span></span>
* <span data-ttu-id="f989b-381">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-381">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="f989b-382">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f989b-382">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="f989b-383">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-383">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="f989b-384">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="f989b-384">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="f989b-385">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-385">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="f989b-386">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f989b-386">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="f989b-387">Naprawienie debugowania, gdy parametr DebugPreference jest ustawiany w wierszu polecenia programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="f989b-387">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="f989b-388">Aktualizacja przykładu polecenia Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="f989b-388">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="f989b-389">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-389">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="f989b-390">Aktualizacja przykładu polecenia Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="f989b-390">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="f989b-391">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="f989b-391">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="f989b-392">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-392">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="f989b-393">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="f989b-393">AzureRM.Dns</span></span>
* <span data-ttu-id="f989b-394">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-394">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="f989b-395">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f989b-395">AzureRM.EventGrid</span></span>
* <span data-ttu-id="f989b-396">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-396">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="f989b-397">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="f989b-397">AzureRM.EventHub</span></span>
* <span data-ttu-id="f989b-398">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-398">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="f989b-399">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f989b-399">AzureRM.HDInsight</span></span>
* <span data-ttu-id="f989b-400">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-400">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="f989b-401">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="f989b-401">AzureRM.Insights</span></span>
* <span data-ttu-id="f989b-402">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-402">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="f989b-403">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="f989b-403">AzureRM.IotHub</span></span>
* <span data-ttu-id="f989b-404">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-404">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="f989b-405">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f989b-405">AzureRM.KeyVault</span></span>
* <span data-ttu-id="f989b-406">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-406">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="f989b-407">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f989b-407">AzureRM.LogicApp</span></span>
* <span data-ttu-id="f989b-408">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-408">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="f989b-409">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="f989b-409">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="f989b-410">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-410">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="f989b-411">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="f989b-411">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="f989b-412">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-412">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="f989b-413">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="f989b-413">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="f989b-414">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-414">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="f989b-415">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="f989b-415">AzureRM.Media</span></span>
* <span data-ttu-id="f989b-416">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-416">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="f989b-417">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="f989b-417">AzureRM.Network</span></span>
* <span data-ttu-id="f989b-418">Dodano przykład dla polecenia Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f989b-418">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="f989b-419">Dodano przykłady i opisy dla poleceń Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey oraz New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f989b-419">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="f989b-420">Dodano przykłady dla poleceń Remove-AzureRmVirtualNetworkGatewayIpConfig i Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f989b-420">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="f989b-421">Dodano przykład dla polecenia Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="f989b-421">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="f989b-422">Dodano przykład dla polecenia Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="f989b-422">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="f989b-423">Dodano przykład dla polecenia Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f989b-423">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="f989b-424">Ponownie wygenerowano polecenia cmdlet ApplicationSecurityGroup, RouteTable i Usage z użyciem najnowszej wersji generatora</span><span class="sxs-lookup"><span data-stu-id="f989b-424">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="f989b-425">Poprawiono czytelność komunikatu o błędzie dla polecenia Get-AzureRmVirtualNetworkSubnetConfig podczas próby pobrania podsieci, która nie istnieje</span><span class="sxs-lookup"><span data-stu-id="f989b-425">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="f989b-426">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="f989b-426">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="f989b-427">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-427">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="f989b-428">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f989b-428">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="f989b-429">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-429">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="f989b-430">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f989b-430">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="f989b-431">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-431">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="f989b-432">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="f989b-432">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="f989b-433">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-433">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="f989b-434">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f989b-434">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="f989b-435">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-435">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="f989b-436">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="f989b-436">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="f989b-437">Dodano filtr zasad do polecenia cmdlet Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="f989b-437">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="f989b-438">Polecenie zwraca listę elementów kopii zapasowej chronionych przez zasady o danym identyfikatorze.</span><span class="sxs-lookup"><span data-stu-id="f989b-438">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="f989b-439">Zaktualizowano przestrzeń nazw Microsoft.Azure.Management.RecoveryServices.Backup do wersji 3.0.0-preview.</span><span class="sxs-lookup"><span data-stu-id="f989b-439">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="f989b-440">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-440">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="f989b-441">Dodano parametr TargetResourceGroupName do polecenia Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="f989b-441">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="f989b-442">Grupa zasobów, do której są przywracane dyski zarządzane.</span><span class="sxs-lookup"><span data-stu-id="f989b-442">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="f989b-443">Ma zastosowanie do wykonywania kopii zapasowych maszyn wirtualnych z dyskami zarządzanymi.</span><span class="sxs-lookup"><span data-stu-id="f989b-443">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="f989b-444">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="f989b-444">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="f989b-445">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-445">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="f989b-446">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f989b-446">AzureRM.RedisCache</span></span>
* <span data-ttu-id="f989b-447">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-447">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="f989b-448">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="f989b-448">AzureRM.Relay</span></span>
* <span data-ttu-id="f989b-449">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-449">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="f989b-450">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="f989b-450">AzureRM.Resources</span></span>
* <span data-ttu-id="f989b-451">Obsługa wdrażania szablonów w zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f989b-451">Support template deployment at subscription scope.</span></span> <span data-ttu-id="f989b-452">Dodanie nowych poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f989b-452">Add new Cmdlets:</span></span>
    - <span data-ttu-id="f989b-453">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="f989b-453">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="f989b-454">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="f989b-454">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="f989b-455">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="f989b-455">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="f989b-456">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="f989b-456">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="f989b-457">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="f989b-457">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="f989b-458">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="f989b-458">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="f989b-459">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="f989b-459">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="f989b-460">Rozwiązanie problemu, w przypadku którego podczas przekazywania kontekstu do polecenia Set-AzureRmResource jest zgłaszany błąd</span><span class="sxs-lookup"><span data-stu-id="f989b-460">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="f989b-461">Naprawienie przykładu polecenia New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f989b-461">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="f989b-462">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-462">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="f989b-463">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="f989b-463">AzureRM.Scheduler</span></span>
* <span data-ttu-id="f989b-464">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-464">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="f989b-465">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f989b-465">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="f989b-466">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-466">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="f989b-467">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f989b-467">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="f989b-468">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-468">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="f989b-469">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="f989b-469">AzureRM.Sql</span></span>
* <span data-ttu-id="f989b-470">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-470">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="f989b-471">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="f989b-471">AzureRM.Storage</span></span>
* <span data-ttu-id="f989b-472">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-472">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="f989b-473">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="f989b-473">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="f989b-474">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-474">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="f989b-475">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="f989b-475">AzureRM.Tags</span></span>
* <span data-ttu-id="f989b-476">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-476">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="f989b-477">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="f989b-477">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="f989b-478">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-478">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="f989b-479">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="f989b-479">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="f989b-480">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-480">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="f989b-481">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="f989b-481">AzureRM.Websites</span></span>
* <span data-ttu-id="f989b-482">Zaktualizowano do najnowszej wersji środowiska Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-482">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="f989b-483">6.6.0 — lipiec 2018 r.</span><span class="sxs-lookup"><span data-stu-id="f989b-483">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="f989b-484">Ogólne</span><span class="sxs-lookup"><span data-stu-id="f989b-484">General</span></span>
* <span data-ttu-id="f989b-485">Zaktualizowano wszystkie pliki pomocy, aby uwzględniały pełne typy parametrów i poprawne typy wejściowe/wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="f989b-485">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="f989b-486">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="f989b-486">AzureRM.Profile</span></span>
* <span data-ttu-id="f989b-487">Zaktualizowano bibliotekę Common.Strategy, aby mogła ona weryfikować, czy bieżąca konfiguracja zasobu jest zgodna z zasobem docelowym.</span><span class="sxs-lookup"><span data-stu-id="f989b-487">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="f989b-488">Dodano typy ps1xml do biblioteki Common.Storage</span><span class="sxs-lookup"><span data-stu-id="f989b-488">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="f989b-489">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="f989b-489">Azure.Storage</span></span>
* <span data-ttu-id="f989b-490">Dodano obsługę pobierania kontekstu magazynu z profilu DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f989b-490">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="f989b-491">Dodano atrybut Ps1XmlAttribute do właściwości typów wyjściowych poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f989b-491">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="f989b-492">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f989b-492">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="f989b-493">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="f989b-493">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="f989b-494">Usunięto usterkę w maperze Automapper dotyczącą translacji obiektu PsApiManagementApi na obiekt ApiContract</span><span class="sxs-lookup"><span data-stu-id="f989b-494">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="f989b-495">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="f989b-495">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="f989b-496">Usunięto usterkę w elemencie File.Save dotyczącą przeciążania typem kodowania</span><span class="sxs-lookup"><span data-stu-id="f989b-496">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="f989b-497">Rozwiązano problem https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="f989b-497">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="f989b-498">Uaktualniono menedżer NuGet do wersji 4.0.3, co rozwiązuje problem z występowaniem wyjątku dotyczącego wzorca w parametrze apiId</span><span class="sxs-lookup"><span data-stu-id="f989b-498">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="f989b-499">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="f989b-499">AzureRM.Compute</span></span>
* <span data-ttu-id="f989b-500">Rozwiązanie problemu powodującego zakończenie niepowodzeniem tworzenia maszyny wirtualnej przy użyciu zestawu DiskFileParameterSet w poleceniu New-AzureRmVm z powodu zmiany nazwy typu konta magazynu PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="f989b-500">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="f989b-501">Poprawienie polecenia cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="f989b-501">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="f989b-502">Zaktualizowanie polecenia Get-AzureRmAvailabilitySet, aby umożliwić zwrócenie listy wszystkich zestawów dostępności w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f989b-502">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="f989b-503">(Parametr ResouceGroupName jest teraz opcjonalny).</span><span class="sxs-lookup"><span data-stu-id="f989b-503">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="f989b-504">Zaktualizowanie zestawu SimpleParameterSet polecenia „New-AzureRmVm”, aby umożliwić korzystanie z przyspieszonej łączności sieciowej na kwalifikujących się maszynach wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="f989b-504">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="f989b-505">Zaktualizowanie prostego zestawu parametrów polecenia New-AzureRmVmss w taki sposób, aby tworzenie zestawu skalowania maszyn wirtualnych kończyło się niepowodzeniem, gdy moduł równoważenia obciążenia określony przez użytkownika już istnieje.</span><span class="sxs-lookup"><span data-stu-id="f989b-505">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="f989b-506">Zaktualizowanie przykładu dla polecenia New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="f989b-506">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="f989b-507">Dodanie przykładu dla polecenia „New-AzureRmVM”</span><span class="sxs-lookup"><span data-stu-id="f989b-507">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="f989b-508">Zaktualizowanie opisu polecenia Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="f989b-508">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="f989b-509">Zaktualizowanie przykładu 1 dla polecenia Set-AzureRmVMBginfoExtension przez poprawienie pisowni i prefiksu.</span><span class="sxs-lookup"><span data-stu-id="f989b-509">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="f989b-510">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f989b-510">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="f989b-511">Zaktualizowano zestaw ADF .Net SDK do wersji 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="f989b-511">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="f989b-512">Obsługa udostępniania własnego środowiska Integration Runtime dla wielu fabryk danych.</span><span class="sxs-lookup"><span data-stu-id="f989b-512">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="f989b-513">Dodanie nowego parametru -SharedIntegrationRuntimeResourceId do polecenia cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-513">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="f989b-514">Dodanie nowego opcjonalnego parametru -LinkedDataFactoryName do polecenia cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="f989b-514">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="f989b-515">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f989b-515">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="f989b-516">Zaktualizowano zestaw SDK płaszczyzny danych (Microsoft.Azure.DataLake.Store) do wersji 1.1.9</span><span class="sxs-lookup"><span data-stu-id="f989b-516">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="f989b-517">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="f989b-517">AzureRM.EventHub</span></span>
* <span data-ttu-id="f989b-518">Zaktualizowano potokowanie elementów InputObject i ResourceId w poleceniach cmdlet usuwania</span><span class="sxs-lookup"><span data-stu-id="f989b-518">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="f989b-519">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="f989b-519">AzureRM.Insights</span></span>
* <span data-ttu-id="f989b-520">Naprawiono formatowanie typu OutputType w plikach pomocy</span><span class="sxs-lookup"><span data-stu-id="f989b-520">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="f989b-521">Użycie zestawu Microsoft.Azure.Management.Monitor SDK w wersji 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="f989b-521">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="f989b-522">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f989b-522">AzureRM.KeyVault</span></span>
* <span data-ttu-id="f989b-523">Rozwiązanie problemu z potokowaniem w poleceniu Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f989b-523">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="f989b-524">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="f989b-524">AzureRM.Network</span></span>
* <span data-ttu-id="f989b-525">Dodano przykłady dla poleceń cmdlet LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="f989b-525">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="f989b-526">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="f989b-526">AzureRM.Resources</span></span>
* <span data-ttu-id="f989b-527">Rozwiązanie problemu w przypadku podawania zarówno wartości, jak i nazwy tagu w poleceniu „Get-AzureRmResource”</span><span class="sxs-lookup"><span data-stu-id="f989b-527">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="f989b-528">Naprawienie scenariusza potokowania w poleceniu „Set-AzureRmResource”</span><span class="sxs-lookup"><span data-stu-id="f989b-528">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="f989b-529">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f989b-529">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="f989b-530">Zaktualizowano potokowanie elementów InputObject i ResourceId w poleceniach cmdlet usuwania</span><span class="sxs-lookup"><span data-stu-id="f989b-530">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="f989b-531">Rozwiązano kilka problemów</span><span class="sxs-lookup"><span data-stu-id="f989b-531">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="f989b-532">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="f989b-532">AzureRM.Sql</span></span>
* <span data-ttu-id="f989b-533">Dodanie obsługi zaawansowanej ochrony serwera przed zagrożeniami przy użyciu następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f989b-533">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="f989b-534">Enable-AzureRmSqlServerAdvancedThreatProtection, Disable-AzureRmSqlServerAdvancedThreatProtection, Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f989b-534">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="f989b-535">Dodanie obsługi oceny luk w zabezpieczeniach przy użyciu następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f989b-535">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="f989b-536">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings, Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings, Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="f989b-536">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="f989b-537">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline, Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline, Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="f989b-537">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="f989b-538">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan, Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord, Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="f989b-538">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="f989b-539">Poprawiono przykład w poleceniu Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f989b-539">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="f989b-540">Naprawienie niepoprawnej obsługi daty/godziny w przypadku podstawowej kultury innej niż Stany Zjednoczone w poleceniu Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="f989b-540">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="f989b-541">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="f989b-541">AzureRM.Storage</span></span>
* <span data-ttu-id="f989b-542">Dodanie atrybutu Ps1XmlAttribute do właściwości typów wyjściowych poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="f989b-542">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="f989b-543">Pokazywanie danych wyjściowych polecenia cmdlet StorageAccount w widoku tabeli</span><span class="sxs-lookup"><span data-stu-id="f989b-543">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="f989b-544">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f989b-544">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="f989b-545">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f989b-545">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="f989b-546">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f989b-546">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="f989b-547">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="f989b-547">AzureRM.Tags</span></span>
* <span data-ttu-id="f989b-548">Usunięcie niepoprawnej informacji z pomocy polecenia cmdlet Tag</span><span class="sxs-lookup"><span data-stu-id="f989b-548">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="f989b-549">6.5.0 — lipiec 2018 r.</span><span class="sxs-lookup"><span data-stu-id="f989b-549">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="f989b-550">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="f989b-550">AzureRM.Profile</span></span>
* <span data-ttu-id="f989b-551">Zaktualizowano pomoc dotyczącą polecenia „Get-AzureRmContextAutosaveSetting”</span><span class="sxs-lookup"><span data-stu-id="f989b-551">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="f989b-552">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="f989b-552">Azure.Storage</span></span>
* <span data-ttu-id="f989b-553">Dodano obsługę przekazywania obiektu blob lub pliku z tokenem sygnatury dostępu współdzielonego tylko do odczytu</span><span class="sxs-lookup"><span data-stu-id="f989b-553">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="f989b-554">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f989b-554">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="f989b-555">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f989b-555">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="f989b-556">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f989b-556">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="f989b-557">Dodano wymaganą właściwość ResourceGroupName do usługi AS.</span><span class="sxs-lookup"><span data-stu-id="f989b-557">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="f989b-558">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="f989b-558">AzureRM.Automation</span></span>
* <span data-ttu-id="f989b-559">Zaktualizowano pomoc i dodano przykład polecenia „New-AzureRMAutomationSchedule”</span><span class="sxs-lookup"><span data-stu-id="f989b-559">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="f989b-560">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="f989b-560">AzureRM.Compute</span></span>
* <span data-ttu-id="f989b-561">Dodano parametr -Tag do polecenia Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f989b-561">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="f989b-562">Dodano przykład polecenia „Add-AzureRmVmssExtension”</span><span class="sxs-lookup"><span data-stu-id="f989b-562">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="f989b-563">Dodano przykłady polecenia „Remove-AzureRmVmssExtension”</span><span class="sxs-lookup"><span data-stu-id="f989b-563">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="f989b-564">Zaktualizowano pomoc dotyczącą polecenia „Set-AzureRmVMAccessExtension”</span><span class="sxs-lookup"><span data-stu-id="f989b-564">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="f989b-565">Zaktualizowano atrybut SimpleParameterSet dla polecenia New-AzureRmVmss, aby domyślnie ustawiał parametr SinglePlacementGroup na wartość false oraz dodano parametr przełącznika „SinglePlacementGroup” umożliwiający użytkownikowi tworzenie zestawów VMSS w pojedynczej grupie umieszczania.</span><span class="sxs-lookup"><span data-stu-id="f989b-565">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="f989b-566">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="f989b-566">AzureRM.EventHub</span></span>
* <span data-ttu-id="f989b-567">Dodano właściwość tylko do odczytu „PendingReplicationOperationsCount” do klasy PSEventHubDRConfigurationAttributes, która umożliwia wyświetlenie liczby oczekujących operacji replikacji w czasie działania replikacji</span><span class="sxs-lookup"><span data-stu-id="f989b-567">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="f989b-568">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f989b-568">AzureRM.KeyVault</span></span>
* <span data-ttu-id="f989b-569">Zaktualizowano komunikat o błędzie dla polecenia Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f989b-569">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="f989b-570">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f989b-570">AzureRM.LogicApp</span></span>
* <span data-ttu-id="f989b-571">Naprawiono błąd „nie można rozpoznać zestawu parametrów” w poleceniu New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="f989b-571">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="f989b-572">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="f989b-572">AzureRM.Network</span></span>
* <span data-ttu-id="f989b-573">Włączono komunikację równorzędną między sieciami wirtualnymi w wielu dzierżawach dla polecenia Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="f989b-573">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="f989b-574">Zaktualizowano poniższe polecenia cmdlet usługi Application Gateway</span><span class="sxs-lookup"><span data-stu-id="f989b-574">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="f989b-575">New-AzureRmApplicationGateway: dodano obsługę flagi EnableFIPS i stref</span><span class="sxs-lookup"><span data-stu-id="f989b-575">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="f989b-576">New-AzureRmApplicationGatewaySku: dodano nowe jednostki SKU — Standard_v2 i WAF_v2</span><span class="sxs-lookup"><span data-stu-id="f989b-576">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="f989b-577">Set-AzureRmApplicationGatewaySku: dodano nowe jednostki SKU — Standard_v2 i WAF_v2</span><span class="sxs-lookup"><span data-stu-id="f989b-577">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="f989b-578">Ponownie wygenerowano polecenia cmdlet RouteTable z użyciem najnowszej wersji generatora</span><span class="sxs-lookup"><span data-stu-id="f989b-578">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="f989b-579">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="f989b-579">AzureRM.Relay</span></span>
* <span data-ttu-id="f989b-580">Zaktualizowano pliki markdown, naprawiono problem z nazwą parametru w przykładzie</span><span class="sxs-lookup"><span data-stu-id="f989b-580">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="f989b-581">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="f989b-581">AzureRM.Resources</span></span>
* <span data-ttu-id="f989b-582">Zaktualizowano polecenia cmdlet Roleassignment i roledefinition:</span><span class="sxs-lookup"><span data-stu-id="f989b-582">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="f989b-583">Usunięto dodatkowe wywołania polecenia roledefinition wykonywane w ramach stronicowania.</span><span class="sxs-lookup"><span data-stu-id="f989b-583">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="f989b-584">Naprawiono polecenie cmdlet Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="f989b-584">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="f989b-585">Naprawiono funkcjonalność parametru polecenia -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="f989b-585">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="f989b-586">Rozwiązano problem z poleceniem „Get-AzureRmResource”, który polegał na tym, że w parametrze „-ResourceType” była uwzględniana wielkość liter</span><span class="sxs-lookup"><span data-stu-id="f989b-586">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="f989b-587">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f989b-587">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="f989b-588">Dodano parametry top i skip do poleceń cmdlet „list”</span><span class="sxs-lookup"><span data-stu-id="f989b-588">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="f989b-589">Dodano polecenia cmdlet migracji przestrzeni nazw z warstwy Standardowa do warstwy Premium:</span><span class="sxs-lookup"><span data-stu-id="f989b-589">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="f989b-590">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="f989b-590">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="f989b-591">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="f989b-591">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="f989b-592">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="f989b-592">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="f989b-593">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="f989b-593">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="f989b-594">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="f989b-594">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="f989b-595">Dodano właściwość tylko do odczytu „PendingReplicationOperationsCount” do klasy PSServiceBusDRConfigurationAttributes, która umożliwia wyświetlenie liczby oczekujących operacji replikacji w czasie działania replikacji</span><span class="sxs-lookup"><span data-stu-id="f989b-595">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="f989b-596">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f989b-596">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="f989b-597">Zaktualizowano przykład dotyczący polecenia „New-AzureRmServiceFabricCluster”</span><span class="sxs-lookup"><span data-stu-id="f989b-597">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="f989b-598">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="f989b-598">AzureRM.Sql</span></span>
* <span data-ttu-id="f989b-599">Dodano nowe polecenia cmdlet dla przestrzeni nazw Management.Sql, aby umożliwić klientom dodawanie certyfikatu TDE do wystąpienia programu SQL Server lub wystąpienia zarządzanego</span><span class="sxs-lookup"><span data-stu-id="f989b-599">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="f989b-600">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="f989b-600">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="f989b-601">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="f989b-601">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="f989b-602">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="f989b-602">AzureRM.Websites</span></span>
* <span data-ttu-id="f989b-603">Polecenia `Set-AzureRmWebApp -AssignIdentity` i `Set-AzureRmWebAppSlot -AssignIdentity` po ustawieniu na wartość false spowodują teraz usunięcie właściwości Identity z obiektu lokacji. Usuwany jest także tag podglądu.</span><span class="sxs-lookup"><span data-stu-id="f989b-603">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="f989b-604">Zaktualizowano przykład dotyczący poleceń `Get-AzureRmWebAppMetrics` i `Get-AzureRmAppServicePlanMetrics`</span><span class="sxs-lookup"><span data-stu-id="f989b-604">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="f989b-605">Polecenie `Set-AzureRmWebApp -PhpVersion` obsługuje wartość off jako prawidłową wersję języka PHP</span><span class="sxs-lookup"><span data-stu-id="f989b-605">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="f989b-606">6.4.0 — lipiec 2018 r.</span><span class="sxs-lookup"><span data-stu-id="f989b-606">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="f989b-607">Ogólne</span><span class="sxs-lookup"><span data-stu-id="f989b-607">General</span></span>
* <span data-ttu-id="f989b-608">Naprawiono formatowanie typu OutputType w plikach pomocy dotyczących większości modułów</span><span class="sxs-lookup"><span data-stu-id="f989b-608">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="f989b-609">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="f989b-609">AzureRM.Profile</span></span>
* <span data-ttu-id="f989b-610">Dodano atrybut Ps1Xml do podstawowych typów danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="f989b-610">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="f989b-611">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="f989b-611">AzureRM.Compute</span></span>
* <span data-ttu-id="f989b-612">Funkcja tagów adresów IP dla zestawu skalowania maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="f989b-612">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="f989b-613">Dodano polecenie cmdlet „New-AzureRmVmssIpTagConfig”</span><span class="sxs-lookup"><span data-stu-id="f989b-613">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="f989b-614">Dodano parametr IpTag do polecenia New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="f989b-614">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="f989b-615">Funkcja automatycznego wycofywania systemu operacyjnego dla zestawu skalowania maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="f989b-615">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="f989b-616">Dodano parametry DisableAutoRollback do poleceń New-AzureRmVmssConfig i Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f989b-616">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="f989b-617">Funkcja historii uaktualniania systemu operacyjnego dla zestawu skalowania maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="f989b-617">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="f989b-618">Dodano parametr przełącznika OSUpgradeHistory do polecenia Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f989b-618">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="f989b-619">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="f989b-619">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="f989b-620">Dodano obsługę list ACL wykazu przy użyciu następujących poleceń:</span><span class="sxs-lookup"><span data-stu-id="f989b-620">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="f989b-621">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="f989b-621">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="f989b-622">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="f989b-622">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="f989b-623">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="f989b-623">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="f989b-624">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f989b-624">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="f989b-625">Dodano obsługę anulowania i śledzenia postępu dla poleceń Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="f989b-625">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="f989b-626">Dodano obsługę anulowania dla polecenia Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="f989b-626">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="f989b-627">Naprawiono opróżnianie komunikatów debugowania dla poleceń cmdlet wykonujących operacje cykliczne</span><span class="sxs-lookup"><span data-stu-id="f989b-627">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="f989b-628">Naprawiono lokalizację testu poleceń cmdlet DataLake</span><span class="sxs-lookup"><span data-stu-id="f989b-628">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="f989b-629">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="f989b-629">AzureRM.EventHub</span></span>
* <span data-ttu-id="f989b-630">Dodano opcjonalny parametr MaxCount do poleceń cmdlet tworzących listę operacji: Get-AzureRmEventHub i Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="f989b-630">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="f989b-631">Rozwiązano problem z poleceniem cmdlet New-AzureRmEventHub polegający na tym, że podczas tworzenia nowego centrum EventHub był wymagany co najmniej jeden parametr.</span><span class="sxs-lookup"><span data-stu-id="f989b-631">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="f989b-632">Udostępniono zestaw parametrów domyślnych.</span><span class="sxs-lookup"><span data-stu-id="f989b-632">Provided Default Parameter set.</span></span>
* <span data-ttu-id="f989b-633">Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmEventHubKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.</span><span class="sxs-lookup"><span data-stu-id="f989b-633">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="f989b-634">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f989b-634">AzureRM.KeyVault</span></span>
* <span data-ttu-id="f989b-635">Rozwiązano problem polegający na tym, że wszystkie zasoby były zwracane przez polecenie Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="f989b-635">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="f989b-636">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="f989b-636">AzureRM.Network</span></span>
* <span data-ttu-id="f989b-637">Uwidoczniono nowe jednostki SKU dla strefowo nadmiarowych bram VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="f989b-637">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="f989b-638">Dodano nowe polecenia dla funkcji interfejsów API partnerów usługi ExpressRoute za pośrednictwem usługi ARM</span><span class="sxs-lookup"><span data-stu-id="f989b-638">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="f989b-639">Dodano polecenie Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="f989b-639">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="f989b-640">Dodano polecenie Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="f989b-640">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="f989b-641">Dodano polecenie Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="f989b-641">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="f989b-642">Dodano polecenie Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="f989b-642">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="f989b-643">Dodano polecenie Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="f989b-643">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="f989b-644">Dodano polecenie Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="f989b-644">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="f989b-645">Dodano polecenie Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="f989b-645">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="f989b-646">Dodano polecenie Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f989b-646">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="f989b-647">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="f989b-647">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="f989b-648">Dodano polecenie cmdlet Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="f989b-648">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="f989b-649">To polecenie cmdlet pobiera identyfikator maszyny wirtualnej i sprawdza, czy maszyna wirtualna jest chroniona przez magazyn w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f989b-649">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="f989b-650">Jeśli taki magazyn istnieje, polecenie cmdlet wyświetla jego szczegóły.</span><span class="sxs-lookup"><span data-stu-id="f989b-650">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="f989b-651">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="f989b-651">AzureRM.Resources</span></span>
* <span data-ttu-id="f989b-652">Zaktualizowano polecenia cmdlet Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="f989b-652">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="f989b-653">Dodano obsługę wyświetlania listy wartości -Scope na poziomie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="f989b-653">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="f989b-654">Dodano obsługę pobierania poszczególnych przydziałów za pomocą wartości -Scope na poziomie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="f989b-654">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="f989b-655">Dodano przełączniki -Effective i -All do parametru kontroli</span><span class="sxs-lookup"><span data-stu-id="f989b-655">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="f989b-656">Zaktualizowano polecenia cmdlet Get/New/Remove/Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f989b-656">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="f989b-657">Dodano parametr -ManagementGroupName w celu zastosowania operacji do danej grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="f989b-657">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="f989b-658">Dodano parametr -SubscriptionId w celu zastosowania operacji do danej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="f989b-658">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="f989b-659">Zaktualizowano polecenia cmdlet Get/New/Remove/Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="f989b-659">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="f989b-660">Dodano parametr -ManagementGroupName w celu zastosowania operacji do danej grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="f989b-660">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="f989b-661">Dodano parametr -SubscriptionId w celu zastosowania operacji do danej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="f989b-661">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="f989b-662">Dodano obsługę odwołania do wpisu tajnego KeyVault w parametrach w przypadku używania elementu „TemplateParameterObject” w poleceniu „New-AzureRmResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="f989b-662">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="f989b-663">Rozwiązano problem polegający na tym, że parametr „-EndDate” był ignorowany w poleceniu „New-AzureRmADAppCredential”</span><span class="sxs-lookup"><span data-stu-id="f989b-663">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="f989b-664">Rozwiązano problem polegający na tym, że w poleceniu „Add-AzureRmADGroupMember” używano nieprawidłowego adres URL podczas zgłaszania żądania</span><span class="sxs-lookup"><span data-stu-id="f989b-664">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="f989b-665">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f989b-665">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="f989b-666">Dodano opcjonalny parametr -KeyValue do polecenia cmdlet New-AzureRmServiceBusKey, umożliwiając użytkownikowi wprowadzanie wartości elementu KeyValue.</span><span class="sxs-lookup"><span data-stu-id="f989b-666">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="f989b-667">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="f989b-667">AzureRM.Sql</span></span>
* <span data-ttu-id="f989b-668">Objaśniono punkty przywracania zdefiniowane przez użytkownika dla usługi SQLDW w pomocy polecenia New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="f989b-668">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="f989b-669">Zaktualizowano dokumentację parametru -ComputeGeneration w kilku poleceniach cmdlet</span><span class="sxs-lookup"><span data-stu-id="f989b-669">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="f989b-670">6.3.0 — czerwiec 2018</span><span class="sxs-lookup"><span data-stu-id="f989b-670">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="f989b-671">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="f989b-671">AzureRM.Profile</span></span>
* <span data-ttu-id="f989b-672">Zaktualizowano komunikaty o błędach dotyczące polecenia Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="f989b-672">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="f989b-673">Tworzenie kontekstu dla każdej subskrypcji w przypadku uruchomienia polecenia „Connect-AzureRmAccount” bez wcześniejszego kontekstu</span><span class="sxs-lookup"><span data-stu-id="f989b-673">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="f989b-674">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="f989b-674">Azure.Storage</span></span>
* <span data-ttu-id="f989b-675">Dodano informacje dotyczące parametru -Permissions w plikach pomocy.</span><span class="sxs-lookup"><span data-stu-id="f989b-675">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="f989b-676">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="f989b-676">AzureRM.Compute</span></span>
* <span data-ttu-id="f989b-677">Polecenie „Get-AzureRmVmDiskEncryptionStatus” — rozwiązano problem zaobserwowany w przypadku maszyn wirtualnych bez dysków z danymi</span><span class="sxs-lookup"><span data-stu-id="f989b-677">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="f989b-678">Aktualizacja wersji biblioteki klienckiej obliczeń w celu naprawy następujących poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f989b-678">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="f989b-679">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="f989b-679">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="f989b-680">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="f989b-680">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="f989b-681">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="f989b-681">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="f989b-682">Naprawiono następujące polecenia cmdlet w celu poprawnego wyświetlania identyfikatora operacji i stanu operacji:</span><span class="sxs-lookup"><span data-stu-id="f989b-682">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="f989b-683">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f989b-683">Start-AzureRmVM</span></span>
    - <span data-ttu-id="f989b-684">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f989b-684">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="f989b-685">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f989b-685">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="f989b-686">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f989b-686">Set-AzureRmVM</span></span>
    - <span data-ttu-id="f989b-687">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="f989b-687">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="f989b-688">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f989b-688">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="f989b-689">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="f989b-689">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="f989b-690">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="f989b-690">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="f989b-691">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f989b-691">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="f989b-692">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f989b-692">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="f989b-693">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f989b-693">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="f989b-694">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f989b-694">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="f989b-695">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="f989b-695">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="f989b-696">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="f989b-696">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="f989b-697">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="f989b-697">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="f989b-698">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="f989b-698">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="f989b-699">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="f989b-699">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="f989b-700">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="f989b-700">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="f989b-701">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f989b-701">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="f989b-702">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f989b-702">AzureRM.EventGrid</span></span>
* <span data-ttu-id="f989b-703">Usunięto warunki weryfikacji ValidateNotNullOrEmpty dla elementów SubjectBeginsWith/SubjectEndsWith w poleceniu cmdlet Update-AzureRmEventGridSubscription w celu umożliwienia zmiany tych parametrów na pusty ciąg w razie potrzeby.</span><span class="sxs-lookup"><span data-stu-id="f989b-703">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="f989b-704">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f989b-704">AzureRM.KeyVault</span></span>
* <span data-ttu-id="f989b-705">Rozwiązano problem polegający na tym, że nie były zwracane tagi w przypadku uruchomienia polecenia Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="f989b-705">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="f989b-706">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f989b-706">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="f989b-707">Publiczne udostępnienie poleceń cmdlet usługi Policy Insights</span><span class="sxs-lookup"><span data-stu-id="f989b-707">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="f989b-708">Użycie interfejsu API w wersji z 4.04.2018</span><span class="sxs-lookup"><span data-stu-id="f989b-708">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="f989b-709">Dodano element PolicyDefinitionReferenceId do wyników polecenia Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="f989b-709">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="f989b-710">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="f989b-710">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="f989b-711">Dodano parametr -Vault do poleceń cmdlet RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="f989b-711">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="f989b-712">W przypadku przekazania to polecenie przesłania polecenie cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="f989b-712">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="f989b-713">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="f989b-713">AzureRM.Sql</span></span>
* <span data-ttu-id="f989b-714">Zaktualizowano przykład w pliku pomocy polecenia Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="f989b-714">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="f989b-715">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="f989b-715">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="f989b-716">Zaktualizowano plik pomocy polecenia Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="f989b-716">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="f989b-717">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="f989b-717">AzureRM.Websites</span></span>
* <span data-ttu-id="f989b-718">Zaktualizowano polecenie „Set-AzureRmWebApp”, aby nie zastępowało elementu AppSettings w przypadku użycia parametru -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="f989b-718">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="f989b-719">Zaktualizowano polecenie „New-AzureRmWebAppSlot” w celu umożliwienia obsługi parametru AppServicePlan jako parametru opcjonalnego</span><span class="sxs-lookup"><span data-stu-id="f989b-719">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="f989b-720">6.2.1 — czerwiec 2018</span><span class="sxs-lookup"><span data-stu-id="f989b-720">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="f989b-721">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f989b-721">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="f989b-722">Zaktualizowano model PSWorkspace w celu umożliwienia użycia typu jako parametru w sieci</span><span class="sxs-lookup"><span data-stu-id="f989b-722">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="f989b-723">6.2.0 — czerwiec 2018</span><span class="sxs-lookup"><span data-stu-id="f989b-723">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="f989b-724">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="f989b-724">AzureRM.Profile</span></span>
* <span data-ttu-id="f989b-725">Naprawiono problem, który polegał na tym, że wersja 10.0.3 pliku Newtonsoft.Json nie była ładowana podczas importowania modułu</span><span class="sxs-lookup"><span data-stu-id="f989b-725">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="f989b-726">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="f989b-726">AzureRM.Compute</span></span>
* <span data-ttu-id="f989b-727">Funkcja aktualizacji maszyny wirtualnej usługi VMSS</span><span class="sxs-lookup"><span data-stu-id="f989b-727">VMSS VM Update feature</span></span>
    - <span data-ttu-id="f989b-728">Dodano polecenia cmdlet „Update-AzureRmVmssVM” i „New-AzureRmVMDataDisk”</span><span class="sxs-lookup"><span data-stu-id="f989b-728">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="f989b-729">Dodano parametr VirtualMachineScaleSetVM do polecenia cmdlet „Add-AzureRmVMDataDisk” w celu obsługi dodawania dysku danych do maszyny wirtualnej usługi VMSS.</span><span class="sxs-lookup"><span data-stu-id="f989b-729">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="f989b-730">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f989b-730">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="f989b-731">Zaktualizowano zestaw ADF .Net SDK do wersji 0.8.0-preview zawierającej następujące zmiany:</span><span class="sxs-lookup"><span data-stu-id="f989b-731">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="f989b-732">Dodano operację repozytorium do konfigurowania fabryki</span><span class="sxs-lookup"><span data-stu-id="f989b-732">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="f989b-733">Zaktualizowano usługę QuickBooks LinkedService w celu ujawnienia właściwości consumerKey i consumerSecret</span><span class="sxs-lookup"><span data-stu-id="f989b-733">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="f989b-734">Zaktualizowano wiele typów modeli, od SecretBase do Object</span><span class="sxs-lookup"><span data-stu-id="f989b-734">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="f989b-735">Dodano wyzwalacz zdarzeń obiektów blob</span><span class="sxs-lookup"><span data-stu-id="f989b-735">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="f989b-736">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f989b-736">AzureRM.KeyVault</span></span>
* <span data-ttu-id="f989b-737">Zaktualizowano dokumentację o przykładowe dane wyjściowe</span><span class="sxs-lookup"><span data-stu-id="f989b-737">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="f989b-738">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="f989b-738">AzureRM.Network</span></span>
* <span data-ttu-id="f989b-739">Parametry włączania analizy ruchu w poleceniach cmdlet narzędzia Network Watcher</span><span class="sxs-lookup"><span data-stu-id="f989b-739">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="f989b-740">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="f989b-740">AzureRM.Resources</span></span>
* <span data-ttu-id="f989b-741">Rozwiązano problem z właściwością „Properties” obiektu „PSResource” zwracanego z polecenia „Get-AzureRmResource”</span><span class="sxs-lookup"><span data-stu-id="f989b-741">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="f989b-742">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="f989b-742">AzureRM.Scheduler</span></span>
* <span data-ttu-id="f989b-743">Rozwiązano problem z aktualizacją ServiceBusQueueJob, która nie ustawiała nowych wartości uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="f989b-743">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="f989b-744">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="f989b-744">AzureRM.Sql</span></span>
* <span data-ttu-id="f989b-745">Zaktualizowano następujące polecenia cmdlet o opcjonalny parametr LicenseType</span><span class="sxs-lookup"><span data-stu-id="f989b-745">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="f989b-746">New-AzureRmSqlDatabase, Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f989b-746">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="f989b-747">New-AzureRmSqlElasticPool, Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f989b-747">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="f989b-748">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="f989b-748">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="f989b-749">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="f989b-749">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="f989b-750">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f989b-750">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="f989b-751">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="f989b-751">AzureRM.Websites</span></span>
* <span data-ttu-id="f989b-752">Polecenie „New-AzureRMWebApp” zostało zaktualizowane w celu używania typowych algorytmów z biblioteki strategii.</span><span class="sxs-lookup"><span data-stu-id="f989b-752">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="f989b-753">6.1.0 — maj 2018 r.</span><span class="sxs-lookup"><span data-stu-id="f989b-753">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="f989b-754">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="f989b-754">AzureRM.Profile</span></span>
* <span data-ttu-id="f989b-755">Rozwiązano problem polegający na tym, że po uruchomieniu polecenia „Clear-AzureRmContext” pozostawał pusty kontekst o nazwie takiej jak poprzedni kontekst domyślny, co uniemożliwiało użytkownikowi utworzenie nowego kontekstu ze starą nazwą</span><span class="sxs-lookup"><span data-stu-id="f989b-755">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="f989b-756">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f989b-756">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="f989b-757">Włączono operacje kojarzenia/usuwania skojarzenia bramy w usłudze AS.</span><span class="sxs-lookup"><span data-stu-id="f989b-757">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="f989b-758">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f989b-758">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="f989b-759">Dodano obsługę elementów ApiVersion, ApiRelease oraz ApiRevision</span><span class="sxs-lookup"><span data-stu-id="f989b-759">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="f989b-760">Dodano obsługę zaplecza ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f989b-760">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="f989b-761">Dodano obsługę rejestratora usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="f989b-761">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="f989b-762">Dodano obsługę rozpoznawania jednostki SKU „Podstawowa” jako prawidłowej jednostki SKU usługi API Management</span><span class="sxs-lookup"><span data-stu-id="f989b-762">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="f989b-763">Dodano obsługę instalowania certyfikatów wystawionych przez prywatny urząd certyfikacji jako certyfikatów głównych lub certyfikatów urzędu certyfikacji</span><span class="sxs-lookup"><span data-stu-id="f989b-763">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="f989b-764">Dodano obsługę akceptowania niestandardowych certyfikatów SSL za pomocą magazynu kluczy i wielu nazw hostów serwera proxy</span><span class="sxs-lookup"><span data-stu-id="f989b-764">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="f989b-765">Dodano obsługę tożsamości MSI</span><span class="sxs-lookup"><span data-stu-id="f989b-765">Added support for MSI identity</span></span>
* <span data-ttu-id="f989b-766">Dodano obsługę akceptowania zasad za pomocą adresu URL. UWAGA: następujące polecenia cmdlet staną się przestarzałe w przyszłym wydaniu</span><span class="sxs-lookup"><span data-stu-id="f989b-766">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="f989b-767">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="f989b-767">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="f989b-768">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="f989b-768">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="f989b-769">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="f989b-769">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="f989b-770">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="f989b-770">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="f989b-771">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="f989b-771">AzureRM.Batch</span></span>
* <span data-ttu-id="f989b-772">Wydano nowe polecenie cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="f989b-772">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="f989b-773">Wydano nowe polecenie cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="f989b-773">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="f989b-774">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="f989b-774">AzureRM.Consumption</span></span>
* <span data-ttu-id="f989b-775">Dodano nowe parametry polecenia cmdlet Get-AzureRmConsumptionUsageDetail: Expand, ResourceGroup, InstanceName, InstanceId, Tags oraz Top</span><span class="sxs-lookup"><span data-stu-id="f989b-775">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="f989b-776">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f989b-776">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="f989b-777">Poprawiono przykład dla polecenia Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="f989b-777">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="f989b-778">Rozwiązano problem powodujący wyjątek parametru o wartości null dla przypadku Recurse w poleceniu Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="f989b-778">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="f989b-779">Poprawiono pliki pomocy dla poleceń Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl oraz Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="f989b-779">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="f989b-780">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="f989b-780">AzureRM.Network</span></span>
* <span data-ttu-id="f989b-781">Podniesiono wersję zestawu SDK sieci z 18.0.0-preview do 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="f989b-781">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="f989b-782">Dodano polecenie cmdlet służące do tworzenia konfiguracji protokołu</span><span class="sxs-lookup"><span data-stu-id="f989b-782">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="f989b-783">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="f989b-783">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="f989b-784">Dodano polecenie cmdlet służące do dodawania nowego połączenia obwodu do istniejącego obwodu usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="f989b-784">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="f989b-785">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f989b-785">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="f989b-786">Dodano polecenie cmdlet służące do usuwania połączenia obwodu z istniejącego obwodu usługi ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="f989b-786">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="f989b-787">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f989b-787">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="f989b-788">Dodano polecenie cmdlet służące do pobierania połączenia obwodu</span><span class="sxs-lookup"><span data-stu-id="f989b-788">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="f989b-789">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f989b-789">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="f989b-790">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f989b-790">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="f989b-791">Naprawiono użycie uwierzytelniania serwera za pomocą wygenerowanych certyfikatów (problem nr 5998)</span><span class="sxs-lookup"><span data-stu-id="f989b-791">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="f989b-792">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="f989b-792">AzureRM.Sql</span></span>
* <span data-ttu-id="f989b-793">Zaktualizowano polecenia cmdlet inspekcji w celu umożliwienia usuwania elementów AuditAction lub AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="f989b-793">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="f989b-794">Rozwiązano problem z poleceniem Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy, który powodował zakończenie polecenia niepowodzeniem podczas ustawiania nowych, elastycznych zasad przechowywania oraz zwrócenie komunikatu „Konfigurowanie zasad przechowywania długoterminowego za pomocą magazynu usługi Azure Recovery Service i zasad nie jest już obsługiwane.</span><span class="sxs-lookup"><span data-stu-id="f989b-794">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="f989b-795">Prześlij żądanie z nowymi, elastycznymi zasadami przechowywania”.</span><span class="sxs-lookup"><span data-stu-id="f989b-795">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="f989b-796">Zaktualizowano wszystkie polecenia cmdlet służące do tworzenia/aktualizowania elastycznej puli/bazy danych usługi Azure SQL Database w taki sposób, aby korzystały z nowego interfejsu API bazy danych, który obsługuje właściwość SKU na potrzeby właściwości powiązanych ze skalowaniem i warstwą.</span><span class="sxs-lookup"><span data-stu-id="f989b-796">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="f989b-797">Zaktualizowane polecenia cmdlet to:</span><span class="sxs-lookup"><span data-stu-id="f989b-797">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="f989b-798">New-AzureRmSqlDatabase, Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f989b-798">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="f989b-799">New-AzureRmSqlElasticPool, Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f989b-799">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="f989b-800">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="f989b-800">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="f989b-801">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="f989b-801">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="f989b-802">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f989b-802">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="f989b-803">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="f989b-803">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="f989b-804">Zaktualizowano parametry polecenia „Get-AzureRmTrafficManagerProfile”, aby parametr -ResourceGroupName był wymagany, gdy został podany parametr -Name.</span><span class="sxs-lookup"><span data-stu-id="f989b-804">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
